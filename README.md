# WP-Web1.0
WordPress Web 1.0 theme for bhtooefr.org.

I've been dissatisfied with the state of the web for a while.

Modern web sites tend to use ridiculous amounts of JavaScript and CSS to render their user experience, massively increasing load times, bandwidth usage, CPU usage, and decreasing privacy, security, and battery life. Not to mention, accessibility can be harmed greatly by these sites, as accessibility tools have to chew through things like hidden elements and such to get to the content.

All of these factors also make it much harder to develop a web browser that operates on the modern web, to the point that the WebKit and Blink lineage of browsers dominates the browser marketplace to an extent that we haven't seen since the bad old days of Internet Explorer 6. Outside of Firefox, no major browser is independent of a large corporate parent (or an engine developed by a large corporation), and even Microsoft's Edge browser isn't seeing much market success.

I've decided that it's time to do something about that, at least in my little corner of the web.

The goal of this project is to create a theme for WordPress that harkens back to the best practices of Web 1.0 - the result should be clean, simple, and unstyled - think [motherfucking website](http://motherfuckingwebsite.com/). Semantics should be used properly to ensure that a user can apply their own CSS if they wish, and get a nice result, but it's the user agent's job to do styling, not mine, in my opinion. The result will naturally be responsive, without having to use things like CSS media queries to make it responsive.

Websites using this theme should render perfectly in any user agent that is compliant with RFCs [1866](https://tools.ietf.org/html/rfc1866) (Hypertext Markup Language - 2.0), [1942](https://tools.ietf.org/html/rfc1942) (HTML Tables), and [2070](https://tools.ietf.org/html/rfc2070) (Internationalization of the Hypertext Markup Language). However, features from newer HTML versions are fair game, if they enhance the experience for users of newer user agents without degrading it for older user agents, and don't deviate from the goal of clean, simple, and unstyled. (An example is the srcset attribute of img tags, which provides optional higher resolution images for user agents running on high resolution platforms. Older user agents will ignore this and receive a default image.)

Additionally, JavaScript shall be avoided at all costs. This theme will use none of its own JavaScript, and I'll investigate having a configuration option for whether to disable wp-emoji-release.min.js and wp-embed.min.js (both automatically enabled, both not very necessary, and both able to be disabled from a theme, AFAIK). I think I'll leave the Toolbar alone, though, as you'll only get it when logged in.
