---
layout: post
title:  "Howdy World (again)"
date: 2022-05-14 12:20:23 -0700
categories: blog website
---

I'm revamping my blog. As a reasonable first-topic, I figured I'd explain what choices I made for hosting/etc 

**tl;dr: [GoDaddy](https://www.godaddy.com/) + [GitHub Pages](https://pages.github.com/)**

# How it started

 I'd originally configured this website [valbaca.com]() to point to my [dev.to posts](https://dev.to/val_baca). My primary concern is it should be easy to write posts and have them automatically show up on this website. So I guess the first requirement was that it be super easy to start writing. I didn't want to be mucking around with HTML (or ERB or any template langauge) when I'm just trying to get throughts out of my head. Markdown is fine. Actually it's great.

 So here's what my old website stack was...roughly:

 1. Domain name registrar: [GoDaddy](https://www.godaddy.com/)
 2. Routing & Hosting: [Netlify](https://www.netlify.com/)
 3. Tech: [jekyll](https://jekyllrb.com/docs/) generated from [stackbit](https://www.stackbit.com/)


Why these? Mostly because dev.to had instructions on how to set it all up. The main challenge was getting DNS records working. That's always a part of website setup that confounds me. Maybe I should read more [zines from Julia Evans](https://wizardzines.com/zines/dns/).

But somewhere or somehow along the way, the stackbit aspect broke.

Netlify builds of the site started failing out of nowhere. They gave errors like:

```
10:40:49 AM: fetching data for project from https://api.stackbit.com/pull/abc-my-stack-secret-123
```

The secret was coming from the ENV variables configured in Netlify, but I couldn't find where it actually originally came from. I logged into stackbit but even though I had an account, everything was empty. No projects. Nothing under Accounts or Settings. Just a dead-end.

I decided to just abandon stackbit entirely. I wasn't even sure what it was pulled in for anyway. I didn't like this unknown complexity in my **supposedly simple** blog.

# Starting over

It's not like I had many (any?) posts, so I decided to start from scratch. So now we're going with:

1. Domain name registrar: still [GoDaddy](https://www.godaddy.com/)
2. DNS Routing: still [Netlify](https://www.netlify.com/)
3. Hosting: [GitHub Pages](https://pages.github.com/)

I'd already pointed my domain at Netlify, so I simply deleted the website within Netlify (keeping the domain within Netlify) to the GitHub pages via DNS Records.

It took about an hour for the HTTPS to become available within GitHub, but otherwise, was a snap by following [GitHub's instructions](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)

One thing I learned is that `@` means "the current domain" in DNS Record-speak.

However, Netlify is still an extra hop in the process and another account I don't want to think about.


# Finalize

To finish it all up, I just needed to cut out Netlify altogether.

*An Aside*: After what's been going on with [Heroku](https://status.heroku.com/incidents/2413), I'm just tired of having extra accounts and companies in what's supposed to just be a super plain text blog. 


Thankfully, this was also simple. Just repeated the [GitHub's instructions](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site) but on GoDaddy and now the stack is just:

1. Domain name registrar and DNS Routing: [GoDaddy](https://www.godaddy.com/)
2. Hosting: [GitHub Pages](https://pages.github.com/)
3. Tech: just [jekyll](https://jekyllrb.com/docs/)


# Now

Initially, I wasn't super thrilled that GitHub uses a Ruby-powered site generator. That's a personal bias because Ruby causes me nothing but headaches at work; in particular, [nokogiri](https://nokogiri.org/) is a ruby gem I never want to hear about again.

**However** Jekyll has already impressed me with a clean style, simple and fast startup, and live-reloading.

I lost the dev.to integration, but honestly not torn-up over that loss. It's a topic for another post, but I think dev.to has fallen into a "newb-friendly" trap. In an (admirable!) effort to be very beginner friendly, the content has fallen to the lowest-common denominator and the posts mostly lacking in any substance. Posts like ["What `var` means in JavaScript! 😱 "](https://dev.to/paritho/3-reasons-to-use-var-in-javascript-1hoe) or ["200 Resources EVERY developer needs"](https://dev.to/suniljoshi19/top-42-react-resources-every-developer-should-bookmark-latest-24pb) abound. I also cannot complain too much. I had literally two posts. I'm the problem too. Anyway...I think I can hookup publishing via RSS anyway. By cutting out dev.to as a primary concern, I greatly simplified the whole site.


# Conclusion

Someone just setting up their page for the first time should have a much simpler time, but I wanted to share my process of unwinding my overly complicated initial blog stack to what I have now.

Coming soon...
- More meaty posts
- Musing about languages, especially:
    - Langauges I'm actually using now: Kotlin and TypeScript
    - Working through [Crafting Interpreters](https://craftinginterpreters.com/) using Kotlin: [klox](https://github.com/valbaca/klox)
    - Languages I think about more than I write: Rust, Go, Clojure, and Crystal
- Hobbies:
    - Getting back into Magic The Gathering, especially Commander
    - Learning Guitar