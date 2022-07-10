---
title: Ergo IRC Specifications
layout: about
classes: about
logo: ergo-logo-dark-network.svg
---
Ergo emphasizes close collaboration with the [IRCv3 working group](https://ircv3.net/), which produces specifications for backwards-compatible extensions to the IRC protocol, implemented by multiple vendors. At any given time, our stable release will implement all, or nearly all, IRCv3 specifications, including those that are still in the drafting stage. See the [IRCv3 server support table](https://ircv3.net/software/servers) for the current status of our implementation; see the [IRCv3 specifications page](https://ircv3.net/irc/) for more information on any given specification.

In particular, we support the following extensions:

* [SASL](https://ircv3.net/irc/#account-authentication-and-registration), making account authentication a first-class protocol feature
* [Message tags](https://ircv3.net/specs/extensions/message-tags), allowing flexible metadata in messages
* [Labeled response](https://ircv3.net/specs/extensions/labeled-response), allowing precise correlation of sent commands with server replies
* [Chathistory](https://ircv3.net/specs/extensions/chathistory), allowing clients to receive messages sent while they were disconnected from the server
* [WebSocket](https://ircv3.net/specs/extensions/websocket), allowing browser-based clients to connect directly to Ergo

-----

In addition to specifications within the mainstream IRCv3 process, we support some of our own vendor extensions. Currently we support:

* [draft/relaymsg](https://github.com/ircv3/ircv3-specifications/pull/417), which allows stateless protocol bridges (with the appropriate permissions) to alter the sources of sent messages
* [ergo.chat/nope](/nope), a safeguard against incorrect client implementations of [capability negotiation](https://ircv3.net/specs/extensions/capability-negotiation)
