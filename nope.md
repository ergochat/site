---
title: ergo.chat/nope Capability
layout: spec
meta-description: A capability that cannot be requested
copyrights:
  -
    name: "Daniel Oaks"
    period: "2019"
    email: "daniel@danieloaks.net"
  -
    name: "Shivaram Lingamneni"
    period: "2019"
    email: "slingamn@cs.stanford.edu"
classes: spec about
---
## Introduction
The [capability negotiation](https://ircv3.net/specs/core/capability-negotiation) method used in IRC lets clients request protocol changes from servers. It's important to make sure that servers can continue introducing new capabilities that may change the protocol in drastic, backwards-incompatible ways.

The `ergo.chat/nope` capability, inspired by the [GREASE](https://tools.ietf.org/html/draft-ietf-tls-grease-01) mechanism for TLS, is a capability that MAY NOT be requested by clients to help ensure their capability request mechanisms are working correctly and only requesting capabilities which the client can actually support (rather than, for example, assuming that all capabilities advertised by the server are fairly benign and blindly requesting all of them).

We don't expect other clients to implement this feature. We're doing it to catch out clients and break them early so we can get them fixed.

## The Capability
The `ergo.chat/nope` capability has no value. If a client requests it during registration, the server sends an `ERROR` message with a suitable description and closes the connection. If a client requests it outside of registration, the server does not close the client's connection (as this could inspire adventurous users to tell others to "type `/QUOTE CAP REQ ergo.chat/nope`!").

## Future work
In the future we may consider randomly generating the capability name, similar to how the GREASE specification does.
