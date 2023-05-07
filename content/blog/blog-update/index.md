---
title: "Hello, world! (again)"
date: 2023-05-02T17:16:49-05:00
slug: blog-update
summary: "I'm not a hacker, but I am cheap; or: migrating from Octopress to Hugo"
published: true
---

For 9 years, this blog (and its 3 posts) has run on [Github Pages](https://pages.github.com/) and [Octopress.](http://octopress.org/ "Octopress: A blogging framework for hackers") Octopress bills itself as "a blogging framework for hackers" and I'm not a hacker. But I'm comfortable enough messing around with the command line and [Homebrew,](https://brew.sh/ 'Homebrew: The Missing Package Manager for MacOs') and I *am* cheap. I will happily break something, fix it only to break something else, etc., etc., to not have to pay for a website.

Okay, that's unfair. I'm also a simple person who only wants to write ~~for free~~ on the Internet. I don't need databases or a way to take anyone's money. I've also written for sites such as [GameCritics.com](https://gamecritics.com/tera-kirk/ 'Tera Kirk at GameCritics.com') and the now-defunct *Monsters at Play,* hand-coding my reviews in HTML. ([Markdown](https://daringfireball.net/projects/markdown/ 'Daring Fireball: Markdown') was a godsend in 2004 and I've never looked back.)

All this to say: I'm no Edward Snowden, but I appreciate [static site generators](https://en.wikipedia.org/wiki/Static_site_generator 'Wikipedia: Static site generator') for their text-focused simplicity and cheapness. And as I said at the start, Sweet Perdition ran on Octopress for a long time.

But Octopress was one dude's personal framework for a static site generator called Jekyll, and he doesn't seem to be working on it anymore. (The last update was in 2015.) Time for this 3-post blog to modernize.

Moving to regular [Jekyll](https://jekyllrb.com/) would be natural--after all, it's been around since 2008 and still going strong. But in addition to being cheap, I'm also lazy: I didn't feel like putting the Ruby programming language and its gem ecosystem on my computer (including a whole other version of Ruby) just to write words on the Internet. So I went with [Hugo](https://gohugo.io/) instead.

I've been enjoying Hugo so far. It's nice not having to set up a whole bunch of other programs just to run it--there's less chance for things to break that way. It took some time to get my links how I want them. Your text files (blog posts) are kept in a folder called "post," so the blog links were: www.sweet-perdition.net/post/blog-post. I wanted the links to be: www.sweet-perdition.net/blog-post. 

After lots of Googling, I learned to write the following in my config.toml file:

```toml

[permalinks:]
	post = '/:slug'
```

And voila. But one of the nice things about Hugo is that you can make all kinds of sites with it--not just blogs. What if I wanted a blog *and* other things? (What if I learn enough to be a hacker someday and want a place to put my projects?). 

So I've renamed the "post" folder to "blog" and now my config.toml file says:

```toml

[permalinks]
post = '/blog/:slug'
```
and the blog links now read: www.sweet-perdition.net/blog/blog-post

With that, I'll go back to writing about horror movies of varying quality, video games, and whatever else--hopefully at a greater average than once every three years.
