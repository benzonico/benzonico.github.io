---
layout: post
title:  "Changing of IDE"
categories: ide
---
I switched of IDE recently, moving away from Eclipse to IntelliJ. Let me tell you the story of that journey. 

I am a children of Eclipse. I grew up as a Java developer with Eclipse. My first contact with Java was at school and teachers made us Emacs at first but quickly moved us to Eclipse. And I have been using it since then : so that has been 10 years now... (I did not count years before writing them down : I feel old now). 

A few weeks ago I was assigned the task to implement the support of Java 8 in SonarQube (this will probably lead to the writing of some other posts). And the first task to complete this is to fiddle around with the language to see what you can do.
Problem is : For Java8 support in Eclipse you have to download a special version and a plugin under development and fiddle with that. On the other hand IntelliJ was claiming to support it much better so I decided to give it a try. 

And I won't switch back ! Here are some of the reasons why : 

- The keyboard mapping is really well thought. I actually have a lot of examples about why it suits me better :

  - Relaunch last unit test : IDEA : `Shift`+`F10` Eclipse : custom mapping
  - Go to any view in IDE : IDEA `Alt`+n where n is a number identifiying a view, Eclipse : `Alt`+`Shift`+`Q` then letter designing the view
  - Go to Unit test : IDEA : `Ctrl`+`Shift`+`T` Eclipse : no mapping (AFAIK)
  - Getting back to the code : IDEA `Esc` Eclipse : `F12`
  - and son on... 

  The thing is that I realized it took me some months to learn Eclipse shortcuts and some days to get IDEA ones.

- The magic menu `Ctrl`+`Shift`+`A` : it opens a menu where you can type any action to perform it, it is really helpful to learn the IDE. Eclipse tried to mimic that with `Ctrl`+`F3` but you gotta to admit it is just too slow (probably because it also looks up for classes) and does not work well (you don't really find what you are looking for). 

- One thing I get used to do using Eclipse was to change the default color of parameters and local variable to have a clear view of what is what (default configuration is black for all of them). I did not felt the need to bother with that in IntelliJ as the default theme has sufficient highlights and the move of your cursor also gives you sufficient feedback.

In order to be a great developer you have to master your tool and I really think that IDEA is a nice tool to master. Don't get me wrong though I really think Eclipse is totally fine (I know how this subject can degenerate in a troll war in not time) but for _me_, I am feeling more and more comfortable with IDEA in far less time than with Eclipse and that's why I don't think I'll switch back. 
