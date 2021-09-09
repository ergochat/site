---
title: Ergo IRC Server
layout: about
classes: about
---
<a class="logo" href="/">
    <img src="img/ergo-logo-dark.svg" title="Ergo IRC Server">
</a>

Ergo is a modern IRCd (IRC server software) written in Go.

Our core design principles are:

* Being simple to set up and use.
* Combining the features of an ircd, a services framework, and a bouncer (integrated account management, history storage, and bouncer functionality).
* Bleeding-edge [IRCv3 support](https://ircv3.net/software/servers.html) suitable for use as an IRCv3 reference implementation.
* High customizability via a rehashable (i.e., reloadable at runtime) YAML config.

For more information, see our GitHub pages:

* [Main project page](https://github.com/ergochat/ergo)
* [Download a release](https://github.com/ergochat/ergo/releases)
* [Operator manual](https://github.com/ergochat/ergo/blob/master/docs/MANUAL.md)
* [End user guide](https://github.com/ergochat/ergo/blob/master/docs/USERGUIDE.md)

-----

`irc.ergo.chat` is the official self-hosted IRC network of the Ergo project. It hosts the official support channel for Ergo (`#ergo`). Other communities are welcome – come find us in `#ergo` and ask if you're interested in hosting your project or community here.

To connect directly, configure your IRC client with:

```
Host:     irc.ergo.chat
Port:     6697
SSL/TLS:  true
```

The main channels are `#ergo` (the support/development channel) and `#chat` (for socializing).

You can also use one of our web clients: [Kiwi](https://ergo.chat/kiwi/) or [gamja](https://ergo.chat/gamja/).

By default, all hostnames on ergo.chat are cryptographically "cloaked" so that your IP address information is not visible to other users (although it is visible to server administrators).

-----

If you would like to anonymize your connection against the administrators as well, we are accessible via the Tor network, although you may be banned from some channels until you register a nickname:

```
Host:     vrw7zcuarwx4oeju3iikiz3jffrvuijsysyznqf53mxizxrebomfnrid.onion
Port:     6667
SSL/TLS:  false
```

-----

For information on Ergo's distinctive features, see the [official user guide](https://github.com/ergochat/ergo/blob/master/docs/USERGUIDE.md).
