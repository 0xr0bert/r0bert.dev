---
title: Manjaro is 🐕💩
author: Robert Greener
date: 2022-08-20
description: "How can manjaro forget to renew its SSL certificate for a FIFTH time!?"
tags: ["linux", "manjaro", "security"]
categories: ["linux", "security"]
---

Recently [manjaro](https://manjaro.org/), an [Arch Linux](https://archlinux.org/)-based distribution, forgot to renew its SSL certificate for at least the fifth time.
This is bonkers.
Briefly, an SSL certificate allows you to communicate with websites using encryption (https) rather than http.
Thanks to [Let's Encrypt](https://letsencrypt.org/) and [certbot](https://certbot.eff.org/), this is now very easy.
Once it's all set-up all that's needed is to enable the [systemd](https://systemd.io) timer `certbot-renewal`, and then it will literally never expire.
How manjaro's team let it expire even once, let alone FIVE times, is beyond me.
To let it fail so much is incompetence.

This is just a symptom of their poor attitude towards security that means it should be avoided by any serious users.
The bigger issue, IMHO anyways, is that they delay packages from Arch for 2 weeks "to ensure stability".
This is BS.
By delaying for 2 weeks, with little/no effort to backport security fixes, they expose manjaro systems to known vulnerabilities that could be fixed if they didn't bother delaying.
There is no good reason for this that I can see.
Not a lot really happens in those two weeks, so it seems pointless.

This is a shame though I think.
The idea of manjaro is great: an easy, user-friendly Linux distribution based on Arch.
Arch is excellent, exactly what I want, but it isn't suitable for your nan.
However, if someone made a derivative with an easy software centre, installation process, etc., that would be great.
It's just that the execution is poor.

I would not recommend manjaro to anyone.
Its approach to, and poor management of, basic security practices just rules it out of contention.
For the novice user, [Pop!\_OS](https://pop.system76.com/), and [elementary OS](https://elementary.io/) are great choices -- even [Ubuntu](https://ubuntu.com/) might be worth considering (though they have had well-publicised issues with data sharing and advertising).
For the intermediate user, [Debian](https://www.debian.org/) is great and very stable; [Fedora](https://getfedora.org/) is also excellent.
I would also recommend Arch -- it isn't as hard as you'd think, particularly with [archinstall](https://wiki.archlinux.org/title/Archinstall) being available now.
For the expert, Arch and [Gentoo](https://www.gentoo.org/) are the obvious choices.
