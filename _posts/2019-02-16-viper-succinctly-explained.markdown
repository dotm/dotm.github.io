---
layout: post
title: "VIPER succinctly explained"
---

The View/ViewController is responsible for displaying things from the Presenter and relays user input back to the Presenter.

The Interactor is responsible for business logic and interacting with data storage or other kinds of data sources.

The Presenter is the mediator between the View, Interactor, and Router. It handles user input by requesting or posting data to the Interactor, or by asking the Router to navigate things. It's also responsible for the presentation logic used to process received data from the Interactor.

Entity is another name for Model.

The Router handles the navigation between pages. Each page can have different VIPE.