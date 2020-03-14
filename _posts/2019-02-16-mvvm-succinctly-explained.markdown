---
layout: post
title: "MVVM succinctly explained"
---

MVVM is just MVC with the addition of ViewModel.

The view controller has a reference to the view model (e.g. as a property).

The view model handles the presentation logic that
was previously the responsibility of the view controller.

The view controller pushes model data into the view model as input.
The view model processes it into ready-to-display data as output.
Finally, the view controller uses the view model output to directly modify the view.