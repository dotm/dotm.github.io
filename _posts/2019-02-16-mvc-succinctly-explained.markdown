---
layout: post
title: "MVC succinctly explained"
---

Views are composites. One view can have one or many controllers acting as the view's strategies. The model is a publisher observed by the controller. The controller renders the view and updates the view when the model publishes new data. The controllers also change the state of the model when an event happens (e.g. a user submits a form through the view, a scheduler runs programmatically, etc.)