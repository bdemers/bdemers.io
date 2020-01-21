---
title: Hugo to Firebase
type: post
date: 2018-02-01
author: bdemers
featured: hugo-firebase.png
featuredpath: /img
categories: 
- Hugo
- Firebase
- Travis-CI
---

Last time I created a simple Hugo based website, this time, we will deploy it. For free! With TLS!

OK, I am making a couple of assumptions here:

1. You already own a domain name (cheap but not free)
1. You are hosting your site in a GitHub repo (this is not required, but if you want to follow along, I'm going to use GitHub & Travis-CI)

**NOTE:** Since writing this I started using [Netlify](https://gohugo.io/hosting-and-deployment/hosting-on-netlify/) and I'd strongly recommend checking that out! 

## Firebase

I hadn't used Firebase before this; originally, I was going to use GitHub Pages + CloudFlare + LetsEncrypt + a CRON job.  That was a lot of moving parts, free but not cheap.  Other than reducing the complexity, there are a few other reasons I wanted to try out Firebase:

1. Unless you use GitHub's Jekyll build, you are required to check-in your generated/built artifacts into your `master` branch.
1. I didn't want to have a CRON job running on my laptop to update a certificate for a public site. I would then need to monitor that job, and I know for me, I'd forget about it, and the cert would be invalid.

Firebase is a CDN and can provide a TLS certificate for you (using LetsEncrypt).  That leaves us with needing three things:
1. A source repo
1. CI
1. A Firebase account

Just... like any other software project.  I'm using Github and Travis-CI. 

One last note about Firebase, they have tiered payment plans, I fall well within the free tier.

### Validated your Domain

Firebase is part of Google now, so naturally, you can [log in](https://console.firebase.google.com) with your Google account (or a domain account).

Follow the **Add Project** wizard to get started.

Next, in the left nav, click **Hosting**. This will instruct you to install an NPM package and log in.
```bash
$ npm install -g firebase-tools
```

Login (This kicks of a nifty OAuth flow in your browser):
```bash
$ firebase login
```

Initialize the Firebase project:
```bash
$ firebase init
```

Arrow key down to **Hosting: Configure and deploy Firebase Hosting sites** press Space then Enter.
Select the project you created in the Wizard above and press Enter.
Use all of the defaults (Press enter a bunch of times)


We haven't configured our custom domain yet (I'll get to that). To test the Firebase deployment, you will need to update your Hugo `config.toml`'s base URL:

```toml
baseURL = "https://<your-project-name>.firebaseapp.com/"
```

Build and deploy!
```
$ hugo && firebase deploy
```

Along the way I did receive a message to login again
```bash
$ firebase login --reauth
```
I'm assuming this was just updating a few OAuth scopes.

Browse to `https://<your-project-name>.firebaseapp.com/` and you should see your app!

## Custom Domain

Back in your browser, head back to the Firebase console (you should still be on the **Hosting** tab). Click the big blue **Connect Domain** button.

Follow along with this new wizard (you will need to update a DNS TXT record). I'm using a Google Apps managed domain and account, and I still had to do this.
This could take a while depending on your current DNS setup (I'm switching providers, and I needed to wait for the changes to propagate)


I stumbled on this for a while because my DNS provider (NameCheap) uses the `@` notation instead of the domain name `example.com`  directly.  After you pass the first validation screen Firebase does tell you to watch out for this...

## Continuous Deployments

Generate a API token:

```bash
$ firebase login:ci
```

You will once again be prompted through through browser.

The output will look something like this:
```txt
your-key-here

Example: firebase deploy --token "$FIREBASE_TOKEN"
```

```yml
language: node_js
node_js:
- "7"

install:
- wget https://github.com/gohugoio/hugo/releases/download/v0.34/hugo_0.34_Linux-64bit.tar.gz -O ../hugo.tar.gz
- tar -C .. -zxf ../hugo.tar.gz hugo

script:
- ../hugo
```

Add it to your travis.yml
```bash
travis encrypt "your-key-here"
```

```yml
deploy:
  provider: firebase
  skip_cleanup: true
  token:
    secure: "<a long string value>"
```

## Set it and Forget it

Okay, maybe not forget, but `git push` and let Travis CI take care of the rest!

That is all there is to it!
