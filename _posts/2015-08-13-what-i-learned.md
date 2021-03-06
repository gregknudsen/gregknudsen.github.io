---
layout: post
title: What I Learned This Week
excerpt: "Don't use 'content:url()'"
tags: [front end questions, code, future]
modified: 2015-09-07
comments: true
---

**** TO BE ASKED EVERY WEEK ****

> What did you learn this week?

####'content: url()' has MUCH less support than the 'background' property across browsers
  - WHY: This was an ongoing issue with [Brunzies](www.brunzies.com)'s index page - the image carousel. Uitmately, I found that using 'content:url();' was the solution. Then I realized that this did not work in Firefox. I did some research and found a (hacky) fix for that (used the :after pseudo class). As I started working for DataDreamers, I had to start working in a Windows 7 environment. When I checked IE11, the images didn't appear there - even with the Firefox. I did some more research and found the 'background: url();' property, and that worked for IE. In doing this, I experimented a little more and found that I didn't need the pseudo class fix for Firefox if I used the background property. And to continue this to its logical conclusion, using this worked across all platforms (even my dad's Android cell phone which was not originally displaying the images). The only addition I needed to make was adding the 'background-size: cover;' property. Clearly, this is the better way.

#### technical interviews are nerve wracking
  - WHY: As someone who has taken professional orchestral auditions, I have an idea about this. Of course, this is not an orchestral audition - an event I had spent most of my career trying to master. A technical interview puts me right back at my first audition...scared shitless. It's good, though. I just need to keep working and getting interviews, and I'll get better. 

#### I have a LONG way to go, but I'll get there (this will be the last time this answer appears, as it will always be true)
  - WHY: In reference to above, I kind of got my ass kicked this week. This can't be a hobby on the side if I want to make it my next career. Doing this project along with some others will help with this, but I would be lying if I said I wasn't a little worried and frustrated.

---

## General Question 
selected at random in irb 
{% highlight ruby %}
2.1.1 :002 > rand(19)
 => 12
{% endhighlight %}

> Name 3 ways to decrease page load (perceived or actual load time).

### My answer

minify assets, optimize images, use ajax to 'preload' content

## After research

I was actually pretty close on this. Where I would have gotten into trouble is if the interviewer had followed up on my third solution. I could not adequately describe _how_ to preload content. This is something I will look further into.

####Resources
[Link](http://www.bizreport.com/2011/03/top-3-ways-to-decrease-page-load-times.html) - bizreport.com<br>
[Link](http://www.raymondcamden.com/2015/04/10/front-end-interview-questions-part-5) - raymondcamden.com


 
  

---

##Coding Question
{% highlight ruby %}
2.1.1 :004 > rand(8)
 => 1 

{% endhighlight %}
---
> What is the value of foo?
{% highlight javascript %}
var foo = 10 + '20'
{% endhighlight %}


### My Answer
initial answer would be undefined, as you can't add a string to a number. Will brb after checking console...

### After testing in the console
{% highlight javascript %}
> var foo = 10 + '20';
> undefined
> foo;
> "1020"
{% endhighlight %}

Wrong! Damn it. Also, just ran it reverse and the result was '2010'. Now I remember...what could not be done is `var foo = 10 + 'bar'` 
But I ran it, and...
{% highlight javascript %}
> var foo = 10 + 'bar';
> undefined
> foo;
> "10bar"
{% endhighlight %}

Wrong again! Checking the console, that code is coerced into a string. Definitely need to remember this.

