---
layout: post
title:  "What I Learned This Week"
date:   2015-08-13 20:30:43
---

**** TO BE ASKED EVERY WEEK ****

>What did you learn this week?

* 'content: url()' has MUCH less support than the 'background' property across browsers
  - WHY: This was an ongoing issue with [Brunzies](www.brunzies.com)'s index page - the image carousel. Uitmately, I found that using 'content:url();' was the solution. Then I realized that this did not work in Firefox. I did some research and found a (hacky) fix for that (used the :after pseudo class). As I started working for DataDreamers, I had to start working in a Windows 7 environment. When I checked IE11, the images didn't appear there - even with the Firefox. I did some more research and found the 'background: url();' property, and that worked for IE. In doing this, I experimented a little more and found that I didn't need the pseudo class fix for Firefox if I used the background property. And to continue this to its logical conclusion, using this worked across all platforms (even my dad's Android cell phone which was not originally displaying the images). The only addition I needed to make was adding the 'background-size: cover;' property. Clearly, this is the better way. 
* technical interviews are nerve wracking
  - WHY: As someone who has taken professional orchestral auditions, I have an idea about this. Of course, this is not an orchestral audition - an event I had spent most of my career trying to master. A technical interview puts me right back at my first audition...scared shitless. It's good, though. I just need to keep working and getting interviews, and I'll get better. 
* I have a LONG way to go, but I'll get there (this will be the last time this answer appears, as it will always be true)
  - WHY: In reference to above, I kind of got my ass kicked this week. This can't be a hobby on the side if I want to make it my next career. Doing this project along with some others will help with this, but I would be lying if I said I wasn't a little worried and frustrated.

---
** General Question 
selected at random in irb 
```
2.1.1 :002 > rand(19)
 => 12
```

>Name 3 ways to decrease page load (perceived or actual load time).

*** My answer

minify assets, optimize images, use ajax to 'preload' content

** After research

I was actually pretty close on this. Where I would have gotten into trouble is if the interviewer had followed up on my third solution. I could not adequately describe _how_ to preload content. This is something I will look further into.

#####Resources
[link](http://www.bizreport.com/2011/03/top-3-ways-to-decrease-page-load-times.html) (first hit on google - from 2011)
 > * First, optimize, optimize, optimize. Check the types of images you are using on-site and ensure the file format is appropriate. 
 > * Second, minimize HTTP requests. Rather than forcing your site to request multiple files for images, content or ads, combine some pages.
 > * Finally, resize elements before they are uploaded into the HTML.

[link](http://www.raymondcamden.com/2015/04/10/front-end-interview-questions-part-5) 
 > * Minimize images
 > * Minimize and combine JavaScript files
 > * Minimize, combine, and “prune” CSS files


 
  

---
## Coding Question
```
2.1.1 :004 > rand(8)
 => 1 
``` 
---
```
var foo = 10 + '20'
```

>What is the value of foo?

### My Answer
initial answer would be undefined, as you can't add a string to a number. Will brb after checking console...

### Correct answer
```
var foo = 10 + '20';
undefined
foo;
"1020"
```

Wrong! Damn it. Also, just ran it reverse and the result was '2010'. Now I remember...what could not be done is `var foo = 10 + 'bar'` 
But I ran it, and...
```
var foo = 10 + 'bar';
undefined
foo;
"10bar"
```
Wrong again! Checking the console, that code is coerced into a string. Definitely need to remember this.


