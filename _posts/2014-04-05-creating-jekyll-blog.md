---
layout: post
title:  "What's running this blog"
categories: jekyll
---

Let's do a meta article and explain what's the stack behind this blog. 

My main concern when I decided to open this blog was to keep things as simple as possible while I wanted enough flexibility to do whatever would cross my mind (and my time would allow me to build). So that's why I did not even bother to look at wordpress or blogger, I did not want something fully integrated where you click everywhere to configure some limited stuff. 

As I am a developer using git and github at work, I looked at how to host a blog on github and they created a nice ruby framework called [jekyll](http://jekyllrb.com/, "Jekyll Website")... Let's try that out then. 

###What should it looks like
I created a simple `index.html` and its css file to have a rough idea on what it should look like. I am no designer (as you can see right now) so I tried to keep things as simple as possible.

###Installing jekyll on your machine
Ok let's install jekyll and run a website locally. On ubuntu 13.10, there is a small trick because you have to install latest ruby version but it is not really hard, you fire up a terminal and type : 

```
~ $ sudo apt-get install ruby1.9.1-dev
~ $ sudo gem install jekyll
~ $ jekyll new myblog
~ $ cd myblog
~/myblog $ jekyll serve
```

So now go to `http://localhost:4000` and voilà, a new blog is running on your machine. 
Time to fiddle with some files to put your content up looking like you want.

###Design
If you have a look at the generated `index.html` file it contains a loop iterating through blog posts to display them. This file starts with the following lines : 

```
layout: default
title: Random Access Thoughts on Development
```

This means that it uses the layout (ie: template) called `default` that you can find in the `_layouts` folder with the file name `default.html`.
You can customize those two files and modify the css which you will (surprisingly) find in the `css` directory to make the website looks like you dream of.

###Write your blog post
If you look at the `_posts` folder you should find a sample post with some information inside it. In jekyll you can write your blog posts using markdown which is a great thing as it is a little less boring to format text for web than html.
So you can create your file : name it using the same format : `YEAR-MONTH-DAY-title.md` title is not relevant but for you to know what the file is about, however the date is what jekyll will use to order your posts.

Then the file starts with something like : 

```
layout: post
title:  "What's running this blog"
categories: jekyll
```

Which once again state that the html layout that should be used is the one for posts, what is the title of your post and the categories. You can even specify more variables in there for advanced functions but let's keep things simple for now. Write and format your content and let's see it in your browser.

###Checking things out
When you navigate to `http://localhost:4000` you will normally see that nothing has changed even though you added your post. You will need to restart your server to see the changes. 

> WAAAAAAAAT ? I will have to restart the server EVERY SINGLE TIME ? 

Please don't shout like that and thankfully, no. You have to start the server using `-w` option to let it watch your files and regenerate the website on file change.

```
$ jekyll -w serve
```

Good now you have a nice tool for your blog, one little detail though... it is still running only on your machine which slightly limit the audience it can get.

###Putting all this online
So the first idea was to host it on github, let's do that then. 
Create a repository that you will name `$username.github.io` (where $username is your github username) then add, commit and push all the files into it. And that's it. Wait for github to generate your site and your first post is up at `http://$username.github.io`. Afterwards, when you want to add a post, you'll just need to push your new post file and wait for github to regenerate the website.

So here you are, a totally free blog hosted on github than you can update using a simple `git push`.
