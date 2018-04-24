---
title: Prioritizing TMForum Open API Dependencies with Ersatz Visualizer
layout: post
permalink: 2018-04-24-dependency-graph-visualizer.html
published: true
---

[Here is an interactive visualization of our TMForum Open API dependency map](/depviz). Select an API node and drag it around to see how it's connected to all of the other TMForum Open APIs. It's an unreasonably fun way to prioritize your TMForum backlog 😄

When we sat down to build TMForum mocks for [the backlog you voted on](https://docs.google.com/forms/d/e/1FAIpQLSfSe94015z7HtFO7HCyavmtcLdF3ogxaWvUMMstmlPX-2GDJQ/viewform) we started with discovery. To build the dependency map we extracted metadata from the TMForum Open API specifciations manually. We then generated the visualization from that metadata.

Mapping the graph of dependencies within the TMForum Open APIs helped us invest our time more wisely. If there's an API several other backlog APIs depended on, we move that dependency to the front of the backlog. If there's a dependency that is important to the ecosystem but not important to our downstream consumers (like Party Management) we deprioritize it.

You can plan your TMForum build investments in the same way, and we'd like to help. [Get in touch with me](mailto:alex@ersatz.io) if you'd like your own copy of the dependency map, and [head over to our main page](http://ersatz.io/) to sign up for more updates.

Have fun playing with the dependency visualization!

<iframe src="https://raw.githubusercontent.com/ersatzio/ersatzio.github.io/master/assets/html/depmap.html"></iframe>
