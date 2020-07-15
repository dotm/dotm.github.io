---
layout: post
title: "Distributed messaging platform succinctly explained"
---

A distributed messaging platform is just a mediator pattern. Messages flow in and out of the platform in the manner of publisher-subscriber (observer pattern).

It takes different types of messages from many producers. It then sends each message to the appropriate consumers based on the message's type (many consumers can subscribe to).

This is so that each producer doesn't need to know what consumers it needs to send for each type of message. The mediator decouples the producers and consumers.

The producers are publishers. The consumers are subscribers. Messages can be distributed either by push or pull mechanism.
