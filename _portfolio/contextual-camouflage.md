---
layout: single
title: Contextual Camouflage
thumbnail-path: "assets/images/contextual-camouflage.png"
permalink: "portfolio/contextual-camouflage.html"
short-description: Contextual Camouflage aims to transform research into a living narrative using a web based application, GIS technology, and user input to paint a picture of the prevalence of mental disorders in the community.
order: 3

---

{:.center}
![]({{ site.baseurl }}/portfolio/assets/images/contextual-camouflage.png)

## Overview
*This project was a part of Steel City Codefest 2017 and is still in development*

Contextual Camouflage aims to transform research into a living narrative using a web based application, GIS technology, and user input to paint a picture of the prevalence of mental disorders in the community. Contextual Camouflage is a web app that uses geographic information systems (GIS) to gather mental health data anonymously based on user input and present it in real time via a heat map. The web app will also provide resources and present current research. Users can opt-in to have their (non-)personal data used in research. There will also be a public installation of the heat map projected at target location(s).

## Technologies

The backend of the application runs on a Ruby on Rails api hosted on AWS and the frontend is built with Ember. The application utilizes the geocoder gem to roughly determine user location when submitting information about their illness experiences.

## My Contributions

I work mainly on the backend api for this project. I helped design the schema for the database and the relational models, built out the controllers for several of the models and worked on the geolocation implementation. I'm also working on the api test coverage utilizing rspec.
