---
title: 'django'
date: '2025-09-05T18:25:52+10:00'
draft: true
status: 'stub'
topics: ''
type: ''
---

I have dabbled with computers, data and analytics over the years, which has yielded a few 'ah ha' moments for me.

I started to 'get' the value of databases to store, access and aggregate data when I helped an organisation to replace a paper membership form with a web form front end to a database. A few keystrokes and I had a report with possible volleyball players, with the names, phone numbers and genders of possible players. This was definitely quicker than the previous approach of trying to find the hard copy forms, sifting and sorting the forms based on a quick look at the form.

Similiarly, having to wrestle with local database storage of an open dataset every time a new version was released (with new rows _and_ updates to existing rows) helped me see what a data pipeline was about.

But it took applying some R to TidyTuesday challenges to truly understand the transformative impact that computing had on research. My inevitable trial, error, search and repeat on my laptop was exhausting, but far less tedious than it would have been before personal computing. (Hard to conceive of booking compute slots on a shared computer to type in prepared hand-written code, then discovering an error or a bug, spending a week finding hard copy textbooks to help to debug, and re-writing the handwritten code - ready for the next one hour compute slot.)

Django provided me with two other 'ah ha' moments - this time for applications and software development. Pitched as the 'web framework for perfectionists with deadlines', Django is a mature python framework for web applications, that supports multiple database backends and a variety of front-ends. It plays nicely with version control systems (such as git), includes a capable test suite for the application and comes with a good administration tool allowing easy data management 'out of the box' and a number of community-contributed modules to extend it. 

Some tinkering showed that Django made it easy to write ways for people to input and update data with just a web browser. My first realisation was that this didn't have to be massive in scale. The framework made it easy enough to write bespoke applications for niche purposes. These use cases could be really small-scale and personal, like a task manager, a coffee tasting tracker or a kitchen cupboard inventory manager. My second realisation was that writing these applications was proper software development and Django included the right tools for it. Initially, I spent quite a lot of time using the application on the development server to enter data into the database on my computer, thinking that was me using the application. Over time, I understood that I was writing a piece of software, that would need to be deployed to a production server that would have its own, separate database (that I would need to keep backed-up). As I began to use git branches to develop and roll-out features, my suite of tests showed me what had stopped working as a result of unrelated code changes - without me having to manually visit each page in the application.

I am aware of the Shiny package, for developing web applications with R (originally, now also python). Despite having been a regular listener to the R Weekly Podcast (and its predecessor) I haven't explored Shiny fully, but it didn't immediately seem as mature or as capable as Django for data entry and management. I would be inclined to explore Shiny further if I needed to allow interactive exploration of datasets through a web browser.

It took me while to get comfortable with Django itself. Perhaps this was partly because I was also exploring python at the same time, so some of the mistakes were with the language and some were with the framework.

I prefer to determine the database design, first. This means mapping out and building the models and tge relationahips between them. Then, I map out the URLs and views required, and the matching templates. 