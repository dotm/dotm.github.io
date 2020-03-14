---
layout: post
title: "Redux succinctly explained"
---

In Redux, the data-store is a state object. The composite UI view is based on the state of the data store. The view can only change when the state change. The state can only change when the data store receives a command object. The command object is processed by a reducer to create a new state. Because Redux uses a reducer, the state is never modified, only changed.