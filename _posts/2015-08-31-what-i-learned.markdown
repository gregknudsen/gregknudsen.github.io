---
layout: post
title:  "What I Learned This Week"
date:   2015-08-31 20:30:43
---

**** TO BE ASKED EVERY WEEK ****

 - I'm upset with myself for taking so long between posts. No excuses, but it has been for good reason. I've taken on an internship posisition with a local company here in Sarasota doing mainly front end work but also some Django development. It's been a great learning experience for sure. I've actually been disappointed with my output, but the CEO of the company (who is also a coder of over 15 years) said I was doing a good job, so I'll take that for what it's worth. I want writing this blog to be a normal event, so I wanted to add another entry. I'ma actually at the office for the company, but it's a good time to take a break and do this. Onto the post!

>What did you learn this week?

* knock down the house of cards
  - What I mean: One of the tasks I was assigned last week for my internship was to add cookies to a minor function of the website. It was to reassign the cookie when a display was clicked. There are only two possible displays, so the javascript file it is in uses true/false to determine the display. Of course, assigning cookies to this would mean the user could leave the page, come back and see the same display every time. To make a long story short (that I might make longer in a future post), even with the help of the CEO, it is not working. To reference the house of cards, when I started working on this assignment, I was very hesitant to alter the existing code. I thought I'd make what I had to do 'fit'. I actually tried to recreate this effect (and succeeded) on my own machine with a completely different example using jQuery. So I tried to gingerly add some of those ideas to my assignment - not succeeding. When I showed my own code to the CEO, his first response was, "That makes a lot of sense to me. Why don't you do that in our project?" My first response was, "Well, that's not how your code is set up." After thinking about that for a second, I realized how backwards it is. When trying something new, DON'T BE AFRAID TO BREAK THINGS!!! It's actually one of the foundational ideas I learned at DBC - be a two year old...break things, fall down. The get up and start over. YOU WILL NOT DIE!! After all, this is why there is git. :)


---
** HTML Question 
selected at random in irb 
```
2.1.1 :001 > rand(13)
 => 1
```

>1.  What does a doctype do?

*** My answer

doctype tells the browser what type of document it is. I know that I have only ever seen this at the top of HTML pages, so I assume it's main purpose is to announce an HTML page is about to be loaded.

** After research

I was partially correct, in that I missed a few important details. doctype (which means 'Document Type Declaration') is a declaration, not an html tag. If an html page does not have a doctype at the top, you cannot use an html validator. Having this declaration insures the browser will use (or at least make a best effort to use) the latest version of html.

#####Resources
[[link]](http://stackoverflow.com/questions/7695044/what-does-doctype-html-do)
I particularly like the seatbelt analogy - you won't know something is wrong until you need it. :)


 
  

---
## Javascript Question
```
Math.floor((Math.random() * 48) + 1);
// 41 
``` 
---


>41.  What language constructions do you use for iterating over object properties and array items?

### My Answer

Using a for loop. I believe there is a forEach method one could use.

** After research

I see now I only really addressed the array items portion of the question. I wasn't too sure about the object properties. I found a great Stack Overflow thread on this. It seems that Object.keys(theObject) creates an array of all the prperties. *Actually this is only true if hasOwnProperty returns true*
I found, with the object (taken from the stack thread)
{% highlight javascript %}
var obj = {
    name: "Simon",
    age: "20",
    clothing: {
        style: "simple",
        isCool: false
    }
}
{% endhighlight %}
That the the 'for...in' worked well.

{% highlight javascript %}
for (property in obj) {
  console.log(obj[property])
}
>> Simon
>> 20
>> Object {style: "simple", isCool: false}

{% endhighlight %}

#####Resources
Here is the [link](http://stackoverflow.com/questions/8312459/iterate-through-object-properties) 
 

