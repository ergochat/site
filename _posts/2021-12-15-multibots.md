---
layout: post
title: Modular multi-bots with Ergo
author: slingamn
---
Ergo is the only major IRC server implementation to natively offer ["multiclient"](https://github.com/ergochat/ergo/blob/stable/docs/USERGUIDE.md#multiclient) functionality, where multiple client connections can share the same nickname and presence on the server. A potentially surprising use of this feature is that it can be used to "stack" bots: two separate IRC bot implementations, neither of which is aware of the other, can be combined into one as though they were a single modular bot. For example, right now on the [official irc.ergo.chat network](https://irc.ergo.chat), the `ErgoBot` nickname is actually controlled by two separate bots: one [slingamn/titlebot](https://github.com/slingamn/titlebot), which titles links, and one [slingamn/ghbot](https://github.com/slingamn/ghbot), which announces events from GitHub.

This has advantages relative to a conventional modular bot framework:

1. Each bot can be restarted independently without taking down the other, regardless of the language's support for hot code reloading
2. The two bots can run on separate hosts if necessary

but also disadvantages:

1. There's a greater chance of the bots conflicting with each other in some respect, particularly if they both have authentication systems or accept overlapping sets of commands. (However, the possibility of "bot wars" is mitigated by the standard technique of having bots only process `PRIVMSG` and only emit `NOTICE`.)
2. A separate connection, with separate message delivery, is required for each "module". In rare cases, this may have a significant load impact on the server.

If you have multiple bots and it seems like they won't conflict, try consolidating them! As usual with Ergo, you just need to configure them to use the exact same nickname, SASL account name, and SASL password. (If a bot doesn't support SASL, in a typical Ergo configuration you can authenticate it using `PASS` (server password) instead. For example, if the SASL account name is `pybot` and the SASL password is `hunter2`, you send `pybot:hunter2` as the server password.)
