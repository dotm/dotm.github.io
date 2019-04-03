---
layout: post
title: "Fourth year of programming (2018)"
---

## Finish Learn You a Haskell for Great Good Book

I finished reading Learn You a Haskell for Great Good in the second week of March. It was a challenging and fun experience. I learned about Monoid, Functor, Applicative Functor, and Monad. Even though I learned a lot, I soon realized there are still much more to Haskell that I don’t know. The Typeclassopedia article lists even more Typeclass that I haven’t yet learned.

In my opinion, the most useful and practical gems I get from learning functional programming is these:
-use higher-order functions instead of manually coding the logic (e.g. map instead of looping)
-variable immutability reduces bugs occurrence and makes bugs easier to spot
-when writing a function, think about its output, then think about all the input you need to get that output, and then transform the inputs step-by-step until you get the output.

In short, functional programming helps me code faster with fewer bugs.

## Finish Head First Design Pattern Book

I finished reading Head First Design Pattern at the end of March. I have coded some of the patterns in Java to understand more about them.
In my opinion, Head First Design Pattern is more accessible than the Gang of Four’s book. This I think is directly caused by relatable example e.g. (Pizzas instead of complex UI most beginners haven’t encountered yet).
Since I mostly use JavaScript to create basic front-end UI in my job, design patterns are not really useful yet. But knowing basic design patterns as vocabularies will probably help me learn how to architect software systems.

## Learning Machine Learning and Python 3

I started learning about machine learning from 14 March. I started reading about the TensorFlow, but I ended up committing to learning from Andrew Ng’s Machine Learning Course first which use Octave (an open-source version of MatLab).

While learning machine learning, I realize that most of the production stack is written in Python and not MatLab. So I decide to learn Python 3 at the end of March. I finish the official tutorial in less than one week. Since my first language is Python 2, learning Python 3 is quite easy.
I finished the Machine Learning Course on 16 May; a few weeks before the deadline. It was an interesting experience and it stretched my mind quite a lot.

## Learning React Redux
I learned React+Redux for a few weeks at the end of May. I finally know why many front-end developers love them. It’s essentially functional programming applied to front-end framework.

## Trying to get into Apple Developer Academy

I got information that Apple opened an Apple Developer Academy in Indonesia. I applied on 16 May and got invited to their selection test on 26 May.

While waiting for the test, I continue reading the CLRS Algorithm book to brush up my algorithm knowledge and I continue (and finished) reading Sams Teach Yourself SQL in 10 Minutes to brush up my database skill, so that even if I’m not accepted, I can get an interview at a new job (I was hoping to go to a company who has automated unit testing in place).

The selection test consists of multiple choices. I thought that my test was unsatisfactory. But, then again I always think that getting a B+ on a test is unsatisfactory anyway. 

Luckily the examiner said that examinees still can add to our submitted portfolio to increase our chances of being accepted. And so, I finished my “Unit-tested Haskell implementation of Binary Search Tree” (impressive enough, no?) that I procrastinated on for quite a while, and submitted it the day after the test.

## Accepted to Apple Developer Academy

I was accepted to Apple Developer Academy on 5 June. So I shifted gear from reading CLRS to learning Swift 4.2 from the Swift Language Guide.
I finished learning Swift on 21 June. Because I have a long holiday (Eid al-Fitr), I can sprint read the Language Guide from Swift online documentation and do some experiment with it in repl.it which uses Swift 3.

## Learning at Apple Developer Academy and working remotely

I got permission to work remotely while I'm studying at Apple Developer Academy. I'm two months in, and both my study and my work is going pretty well.

In fact, after learning iOS development for two months, I have become quite comfortable in creating apps. I know roughly what's available on the platform and where to go to find the references to implement things I don't know about yet.

So, it takes one month to be good enough at Swift programming language and two months to be good enough with iOS development.

Aside from technical stuff, I also learned how to ideate, collaborate and solve problems in a team. I also learned how to create the core of an application that is extensible and how to delegate workload to my teammates.

I also finished reading Don't Make Me Think Revisited while in the Academy (29 July 2018). It opens my eyes to the importance of usability testing in designing software.

## Going into blockchain and dApp (decentralized application)

I've been keeping an eye on blockchain technology since April 2018. But I haven't got the time to start learning about it until mid-August.

In mid-August, I started reading the Mastering Bitcoin book (the free version on GitHub).

On 19 September, somehow, my employer asked me to learn about blockchain technology for my next work. I'm quite overjoyed. I started learning how to develop decentralized applications with Ethereum while also finishing the Mastering Bitcoin book.

Decentralized apps are like the usual applications, except that instead of being deployed on a centralized server, it's deployed on the decentralized public blockchain.

The currently most popular framework to develop dApp is Truffle. The backend is developed in a language called Solidity. The .sol code will then be compiled to become a smart contract (the back-end side of the dApp).

We can use any front-end framework for the dApp, but we need libraries such as web3.js to connect it to the decentralized back-end (the local or remote blockchain node).

## My First Live App and Going Backend
After three months of working on my own app (with a lot of procrastinating), my iOS app, SimpleSounder, is finally ready to sale on AppStore as of 23 Nov 2018. I built all of it alone (design, development, ideation). Though I still use AudioKit and UIKit as the framework.

Now I have two live apps in my portfolio. The other one is Bystanders, an app I made with my second mini-challenge group at Apple Developer Academy. Unlike SimpleSounder, in Bystanders I only contribute as the developer of the core of the application.

Also, in early December my employer asked me to pair with another senior backend developer to rewrite the internal web app of our company using microservices architecture. I only follow the design from my senior, but I'm glad that I can get some more experience with Node.js and MongoDB.