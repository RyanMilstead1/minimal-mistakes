---
layout: single
title: Seventeen Days
thumbnail-path: "assets/images/seventeen-days.jpg"
short-description: Seventeen Days Interactive is a theory-based interactive film created by Carnegie Mellon University designed to educate young women about contraception and sexually transmitted infections (STIs).
order: 5

---

{:.center}
![]({{ site.baseurl}}/portfolio/assets/images/seventeen-days.png)

## Overview
Seventeen Days Interactive is a theory-based interactive app created by Carnegie Mellon University’s Center for Risk Perception and Communication and designed to educate young women about contraception and sexually transmitted infections (STIs). The app presents scenarios involving decisions that young women face in romantic relationships. The app identifies choice points, suggests risk-reduction strategies, and asks viewers to think about what they would do in a similar situation. The app is interactive, allowing viewers to choose what they want to watch. Viewers are given the opportunity to mentally practice how they would respond in hypothetical situations through the frequent use of “cognitive rehearsal.”

The app centers around a pregnancy scare, presenting educational content through six vignettes, a condom demonstration, and four mini-documentaries. The mini documentaries focus on contraception, STIs and anatomy. They are varied in their approach, including real life stories, dramatized video, interactive features, clinical expertise and mechanical demonstrations.

## Technologies

The backend of the application runs on a Ruby on Rails api and the backend as well as the video catalogue for the application are hosted on AWS. The frontend is built with Ionic and AngularJS. The application utilizes a modified implementation of the videogular angular plugin to create the interactive video experience.

## My Contributions

I worked on all aspects of the project. Initially it was built on a backend service but we needed more customization options so I re-wrote the backend as a Ruby on Rails api with custom authorization built on the devise gem. I also helped to expand the original frontend of the application from a static single path format to a multiple version format, creating different forms of the app that could service a classroom layout with segmented lessons. I also implemented users roles and unique licensing for the application that would show users specific content based on their attached license. Additionally, I worked on implementing a simple survey functionality for the app as well as basic user logging and app interaction which aided in feedback for Carnegie Mellon's research.
