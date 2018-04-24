---
title: Prioritizing TMForum Open API Dependencies with the Ersatz Visualizer
layout: post
permalink: 2018-04-24-dependency-visualizer.html
published: true
---

Today we've released [an interactive visualization of our TMForum Open API dependency map](/depviz). Select an API node and drag it around to see how it's connected to all of the other TMForum Open APIs. It's an unreasonably fun way to see your TMForum dependencies 😄

When planning a large API development program there are first- and second- order requirements. The direct needs of the consumers of your APIs are first-order requirements: "as a consumer of the enterprise API platform, I would like to retrieve fulfillment information", for example. The dependencies of those first-order requirements are, of course, second-order: "the Customer Management API depends on the Party Management API", for example.

When you, our community, [voted on the order](https://docs.google.com/forms/d/e/1FAIpQLSfSe94015z7HtFO7HCyavmtcLdF3ogxaWvUMMstmlPX-2GDJQ/viewform) that we should build mock TMForum implementations, you gave us our first-order requirements. Then we went about solving for our second-order requirements.

We wanted to do this in a general way, so we manually extracted metadata from the TMForum Open API specifications which defined a complete TMForum dependency graph. We then used this information to prioritize our backlog: not just what you asked us for, but also the most efficient order for us to build it.

Thoughts?

[Get in touch with me](mailto:alex@ersatz.io) (alex@ersatz.io), especially if you'd like your own copy of our dependency metadata to prioritize your work. And [head over to our main page](http://ersatz.io/) to sign up for future updates.

Have fun playing with the visualizer!
