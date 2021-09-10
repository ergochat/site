---
title: ergo.chat/nope Capability
layout: spec
meta-description: A capability that cannot be requested
copyrights:
  -
    name: "Daniel Oaks"
    period: "2019-2021"
    email: "daniel@danieloaks.net"
  -
    name: "Shivaram Lingamneni"
    period: "2019-2021"
    email: "slingamn@cs.stanford.edu"
---
## Introduction
The [capability negotiation](https://ircv3.net/specs/core/capability-negotiation) method used in IRC lets clients request protocol changes from servers. It's important to make sure that servers can continue introducing new capabilities that may change the protocol in drastic, backwards-incompatible ways.

The `ergo.chat/nope` capability, inspired by the [GREASE](https://tools.ietf.org/html/draft-ietf-tls-grease-01) mechanism for TLS, is a capability that MUST NOT be requested by clients. Clients are not expected to implement this capability; rather, it is intended to help detect client implementations with incorrect capability handling. In particular, a client implementation that attempts to request all advertised capabilities (on the assumption that they will all be more or less backwards-compatible) will "fail deadly" in the presence of this capability.

## The Capability
The `ergo.chat/nope` capability has no value. If a client requests it during registration, the server sends an `ERROR` message with a suitable description and closes the connection. If a client requests it outside of registration, the server does not close the client's connection (as this could inspire adventurous users to tell others to "type `/QUOTE CAP REQ ergo.chat/nope`!").

## Future work
In the future we may consider randomly generating the capability name, similarly to the GREASE specification.
