---
title: Prioritizing TMForum Open API Dependencies with the Ersatz Visualizer
layout: post
permalink: 2018-04-24-dependency-visualizer.html
published: true
---

We've released [an interactive visualization of our TMForum Open API dependency map](/depviz). Select an API node and drag it around to see how it's connected to all of the other TMForum Open APIs. It's an unreasonably fun way to see your TMForum dependencies 😄

When you're planning a large API development program the first thing you want to do is collect requirements from the business side: why are we doing this? What are our business goals?

Those are your first order requirements. You can then analyze your first order requirements to plan the most efficient way to build them. For example, if every first order requirement needs customer information, you might decide that building a "Customer API" makes good sense. In this case "Customer API" would be a second order requirement.

When you, our community, [voted on the order](https://docs.google.com/forms/d/e/1FAIpQLSfSe94015z7HtFO7HCyavmtcLdF3ogxaWvUMMstmlPX-2GDJQ/viewform) that we should build mock TMForum implementations, you gave us our first-order requirements. Then we went about solving for our second-order requirements.

We wanted to do this in a way that benefitted the TMForum community, and so we decided on an approach that generalizes across TMForum implementation programs.

First, we manually extracted metadata from the TMForum Open API specifications. Next, we used that metadata to build a complete TMForum dependency graph. We then used this information to prioritize our backlog: not just what you asked us for, but also the most efficient order for us to build it.

[The visualizer we've released](/depviz) is itself generated from that extracted TMForum metadata. You can use the same requirement mapping approach, and the same metadata, to prioritize your TMForum Open API implementation efforts.

[Get in touch with me](mailto:alex@ersatz.io) at alex@ersatz.io if you'd like a copy of our dependency metadata to help prioritize your work, and [head over to our main page](http://ersatz.io/) to sign up for future updates.

Have fun playing with the visualizer!
