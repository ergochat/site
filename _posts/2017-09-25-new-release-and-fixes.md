---
layout: post
title: v0.9.0, Fixes and Production Use
author: dan
---
Hey everyone, dan here! It's been a while since the last release and the last post, so let's go over what's changed since then and what's in mind for the future.

First of all, the new release. You can find the downloads [[here]](https://github.com/oragono/oragono/releases/tag/v0.9.0). In v0.9.0 comes:

- Crash fixes.

- Memory leak fixes.

- Bad nickname fixes.

- Slightly better testing support, and more inbuilt tests.

There is some new functionality, such as the +R flag allowing users to block all messages from unregistered users, but this release is mostly fixes and some updates for production use (such as allowing the HAProxy PROXY command for finer-grained TLS control).

Thanks to both [Euan Kemp (@euank)](https://euank.com/) and [Shivaram Lingamneni (@slingamn)](https://cs.stanford.edu/people/slingamn/) for the help with this release as well, it's much appreciated.

In terms of future plans, the ones laid out in the last post are basically still valid. I'm hoping to get IP Cloaking soon (but it is a complex feature), and other than that XLINE/DNSBL are the next ones in line. Work's been fairly busy lately so I haven't been able to spend as much time on this as I'd like to, but I'll always be here working on it :)

As always if you have any other ideas or want to send me feedback, feel free to pop into our <a href="ircs://irc.freenode.net:6697/#oragono">IRC channel (#oragono on Freenode)</a> or [send me an email](mailto:daniel@danieloaks.net)!

P.S. Let me know if you want to catch up at [freenode #live](https://freenode.live)! I'll be rocking around there somewhere with some of the other IRCv3 crew.
