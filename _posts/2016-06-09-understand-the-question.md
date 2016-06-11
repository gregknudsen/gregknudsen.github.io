---
layout: post
title: Understand the Question
excerpt: "It's good to be back"
tags: [blog, employment, algorithm, launchcode, interview]
comments: true
---

I was having a conversation with my son, Benjamin, recently. As I was giving him some pretzels close to bedtime, he kept on asking for more - more than usual. Our conversation went something like this: 

> Benjamin: Daddy, I want more pretzels!

> Me: Ok, Ben, but why do you think you're so hungry? 

> Benjamin: Because I want them.

> Me: I know you want them, but why do you think you're so hungry?

> Benjamin: Because you've got pretzels!

> Me: Yes, I do have them right here, and I'll give you more, but **why** do you think you're so hungry?

> Benjamin: Because I want the pretzels.

> Me: (Surrendering) Ok, Ben, here you go. And the reason why you're so hungry is because you didn't eat enough dinner.

The question I posed to him was straight forward, and there was a reletively clear answer. However, as you can read from his responses, Benjamin clearly didn't understand the question being presented to him. It was as though he was answering a different question. 

So here's the deal. Benjamin is 4. He's incredibly intelligent, but he's not at an age where he can quickly correlate the cause and effect relationship of 'not eating enough dinner' to 2 hourse later thinking, 'I'm really hungry right now, and I want more preztels!'

---

I had an online interview last week with a company called [Launchcode](https://www.launchcode.org/). It was composed of four parts, which they, thankfully, shared with me in an email the day before. The first was a 'get to know you' conversation followed by asking me about my past experience - tech and non tech. Those two parts were fairly interconnected and went well. The third part, though not always needed, was to be a little coding exercise. A part of the process to get to the interview portion for Launchcode was a coding challenge consisting of 3 problems in 90 minutes using [Hackerrank](https://www.hackerrank.com)(which is a **very** cool site, btw). Depending on how an applicant did on that coding challenge determined if the coding challenge during the interview was necessary. I wouldn't say I bombed the 90 minute challenge, but I did not solve any of the problems. Therefore, I knew this would be part of my interview. The last part was to be a recap of the interview and what the steps would be (if) moving forward.

When the time came for the coding challenge, he gave me a link to a simple online editor with screenshare. Here is the problem he presented me. 

Given the array ``var arr = [2,3,5,-2,1,5]``, return the index of the highest number(s) in the array.

After clarifying how exactly he wanted me to solve the problem (javascript, psuedocode, etc...), I proceeded to proceed writing javascript. He was also asking me to think out loud to hear my thought process, which I did to some degree. Here's close to what I came up with.

```
var arr = [2,3,5,-2,1,5]

var sortedArr = arr.sort();

for (var i = 0; i <= arr; i++){
	if (arr[i] => sortedArr[i]){
		console.log(arr[i]);
	};
};
```

For someone reading this who is a software developer, I don't need to tell you that the code above doesn't work (for a whole host of reasons). That, however, is not the most important issue here. He gave me the problem, and I proceeded to solve, or at least attempt to solve, a completely different one. He asked for the **index** of the highest number(s), not simply to identify them and how many there are. When the interviewer very nicely pointed this out me, I went on to put together a reasonable solution.

This issue of understanding the question is something I need to really focus on going forward. It particularly tends to affect me on problems such as these - algorithms. I've noticed that my mind starts to race much faster than I need it to. When this happens, I start to write code way too soon. Instead, I need to take a deep breath and really make sure I **understand the question**.

###### For what it's worth, I was happy to learn that I will be moving forward into Launchcode's system, so if a Launchcode partner company has a position that matches my preferences, I could be set up for an interview with them.





















