---
layout: post
title: "Front-end scalability"
---

As far as I know, the most pressing scalability concern in the front-end is making sure that the local state is consistent.

In the back-end, we may serve millions of clients. But, in the front-end, we only have one client. So performance is not as big of a concern as in the back-end.

However, we are not serving only static pages anymore. With the rising complexity of web apps, we need to deal with a lot of states that affect how the app's UI behaves.

The more features added to the app, the more state we have to manage.

In my opinion, the way to make sure that the app can grow (incorporate more features) in a scalable way is by:

- using a strongly-typed language to prevent type error (for example inserting "1" instead of the integer 1)
- using a unidirectional flow architecture to prevent state-related error (invalid states that is hard to manage because the app has a lot of side effects)
- using unit-testing and integration testing to prevent specification error (the app 'works' as we tell it to, but we told it to do the wrong thing).

Ensuring no memory leaks happen also becomes harder as the app grows. In this case, code review may help prevent oversights.

Most likely, there are other concerns and solutions that I've missed. I'll add them later as I become more experienced.