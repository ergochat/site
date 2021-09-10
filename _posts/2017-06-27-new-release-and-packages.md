---
layout: post
title: v0.8.1, Packages And Direction
author: dan
---
Hey everyone, this is the first post on the new News section of our site! I'm planning to make a post each time we release a new version of Oragono, so people can keep an eye on server updates just by following the RSS feed [here: feed.xml](https://oragono.io/feed.xml)

Let's talk about the new release. You can find it [[here]](https://github.com/oragono/oragono/releases/tag/v0.8.1). v0.8.1 adds:

 - A bunch of snomasks to help opers keep better oversight of what's going on on their servers.

 - A draft channel renaming capability (the IRCv3 proposal can be found [here](https://github.com/ircv3/ircv3-specifications/pull/308)).

 - The ability to kill matching users when you apply a ban with DLINE or KLINE.

 - Various other fixes and minor improvements.

As well, thanks to [Sean Enck (@enckse)](https://github.com/enckse) we have a new Arch Linux AUR package [here](https://aur.archlinux.org/packages/oragono/). This should help users on Arch more easily install Oragono for the first time!

We're also now a [Github organisation](https://github.com/oragono), which holds Oragono as well as some of the dependencies we've taken, modified and used.

In terms of future direction, there's a bunch of features I have planned. Let me quickly talk about each of them:

 - <strong>IP Cloaking:</strong> This is, rather than displaying IP addresses of connected clients you'd display something like <span class="noemph"><tt>4yfdxndgf3.jpbkkfnt3g.fhbk6ukspg.5jqti37n7o.test-cloaked</tt></span> instead. I'm pretty interested in this, and I'd say this is something I really want in the next release.

 - <strong>XLINE 'Insane' Protections:</strong> Basically, this stops you from accidentally banning half your network with a single command. With this protection, you'd need to add the INSANE paramter to your DLINE/KLINE command, if it bans more than x% of your network's users.

 - <strong>DNSBL (DNS Blacklist) Support:</strong> This is another one that most other IRCds out there already have, but Oragono doesn't. I think it makes sense to implement this within a few releases, but figuring out exactly how configurable to make it is gonna be the challenge.

 - <strong>Email Verification for Accounts:</strong> Right now, Oragono only supports registing for accounts with no sort of verification. I've been planning this for a while but it's still honestly on the backburner. Does anyone have a pressing need for this, and how should I implement it? Standard SMTP, using a mail daemon such as sendmail on the machine itself? If you'd like this, feel free to reach out and tell me!

 - <strong>Unit Testing:</strong> I want to start on this, but it's difficult to dive into it. I might look into this properly after the next release.

 - <strong>Extbans:</strong> I really want to do this, but it's on the backburner right now.

 - <strong>REST API and Web Interface:</strong> Nice, but entirely on the backburner right now.

 - <strong>S2S Linking Protocol:</strong> Heh. No time soon at all, look at [DanielOaks/dcmi](https://github.com/DanielOaks/dcmi) for more on this.

So that's how things are at the moment, and where I plan taking things forwards. Have any other ideas or want to send me feedback? Feel free to pop into our <a href="ircs://irc.freenode.net:6697/#oragono">IRC channel (#oragono on Freenode)</a> or [send me an email](mailto:daniel@danieloaks.net).

Thanks again to everyone submitting bugs, fixes, and just giving their feedback! It's exciting to have this be used and useful out there, and I hope we can keep making it better as we go.
