---
layout: post
title: Creating My Personal Website
date: 2023-01-15
categories: ["metapost", "web development", "jekyll"]
---
As a software engineer, it's almost a rite of passage to create your own personal website. Not only can it help you cultivate a personal brand, it can also help you learn skills that you might not normally pick up. At least, it certainly did for me.

The process began about six months ago, when I realized that I needed a single source of truth for my projects, socials, and professional presence. I had some experience with Python's [Flask](https://flask.palletsprojects.com/) from a previous internship, as well as hacking a frontend together with [jQuery](https://jquery.com) and [Bootstrap](https://getbootstrap.com).

So I set out on my journey to create a personal website to host my projects, socials, and blog. It did not go to plan.

# Iteration 1: Flask + Bootstrap

Given the experience that I had, I settled on hosting a Flask-and-Bootstrap-based all-in-one project repository, blog, and contact page, all hosted on AWS Lightsail. Seems easy enough, right?

_Wrong_: several bad design choices led me to a dead end. My first thought was to build all my new projects as Flask Blueprints, and then I could easily add them to my personal website as routes. However, this is extremely limiting (as you might imagine), and honestly somewhat boring.

Also, I went about developing my site completely backwards, spinning up my Lightsail server before having any content. After implementing about half of one of my projects, none of the blog, and none of the styling, I scrapped that idea.

Without having all of the projects wrapped up in the site itself, my website would be smaller (just a blog and contact me), so I would have less need for Bootstrap, which worked well since I wanted to style it myself. With all of these changes, I decided to do a complete rewrite, bringing me to...

# Iteration 2: Flask

I wanted to go for a sort of minimalist style (similar to the one you see now), so after fumbling around several web design blogs, I found a suitable font, color palette, and layout. I had a plan, and I was ready to execute.

I would host the website on Lightsail as before, this time just using Flask. I designed and wrote a landing page, then began working on routes for the blog, as well as the admin page. Oh yea, that's right, I thought I needed an admin page.

This was an ill-researched, badly thought-out attempt to create a page where I could write and edit blog posts, preview them, and post them, all without leaving my website. Now, I had to be able to write blog posts in Markdown, since I anticipated writing technical articles. This opened a floodgate of other concerns, including syntax highlighting, Markdown rendering and styling, and security.

I hacked together a sketchy, session-based login system (in cleartext, mind you), a rudimentary text editor, and an [HTML element based Markdown renderer](https://md-block.verou.me/). The renderer worked wonderfully, however, I had a few issues with my implementation.

The preview didn't work, the routes were a total mess, and my database was an unnecessary complication. I just remember thinking to myself, _there must be a better way..._

Turns out, I was not the first developer to want an easy, static, flexible blog builder. Enter [Jekyll](https://jekyllrb.com).

# Iteration 3: Jekyll

Jekyll is everything I could dream of in a static site generator. It supports Liquid, a magical templating engine that allows you to add content in a sort-of-pseudo-dynamic way to pages, and bears a passing resemblance to Flask's Jinja templating engine, which I am a big fan of. Oh, and it has _built-in blogging._ No database, no routes, no complicated admin page. And it handles Markdown and Sass compilation for you.

I was hooked. This is the last iteration. I nuked my Lightsail server, installed Ruby, installed Jekyll, and hit the ground running. I only needed three layouts: a landing page/contact me, the blog page, and the post page, and with Jekyll's rich templating system, this was a breeze. And I am writing this in Markdown. It has built in syntax highlighting. And it's totally static: no more money wasted on a Lightsail instance serving my content for 0 users per year. Ultimately, I decided to host my website on GitHub's wonderful Pages feature, which supports Jekyll natively and through GitHub actions.

Finally, I have to shout out [Serial Programmer](https://github.com/sharadcodes/jekyll-theme-serial-programmer), a wonderful Jekyll theme that helped me style my website. Well, that's a wrap! I hope this helps someone avoid a journey similar to mine. Seriously, if you need a static website or blog, and want to do it yourself, _USE JEKYLL._
