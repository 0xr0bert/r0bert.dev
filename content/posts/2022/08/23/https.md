---
title: HTTPS 🔒 should be compulsory
author: Robert Greener
date: 2022-08-23
description: "Browsers should enforce HTTPS"
tags: ["security"]
categories: ["security"]
---

[Recently]({{< ref "/posts/2022/08/20/manjaro.md" >}}), I spoke about how it was completely incompetent for forgetting to renew its SSL certificate for a fifth time.
This got me thinking about HTTPS (SSL-encrypted HTTP traffic).
HTTPS should be compulsory and browsers should refuse to serve non-encrypted websites to users.

In 2015, Mozilla, the creators of Firefox, [announced](https://blog.mozilla.org/security/2015/04/30/deprecating-non-secure-http/) their intention to deprecate non-secure HTTP.
Seven years later, HTTP still exists.
Albeit, it certainly isn't very common these days, but in some places it does still exists.
Now is the time for us to enforce HTTPS.

HTTP has a number of insecurities. 
The first, and foremost, is that it allows for man-in-the-middle (MITM) attacks.
With an unencrypted and unsigned connection, it allows rogue actors to perform man-in-the-middle attacks.
This allows them to sniff your traffic and even alter it if desired.
This is unacceptable in the modern web.

Another flaw is that it isn't possible to validate who you're talking to.
Suppose, in a hypothetical scenario, someone manages to steal the domain paypal.com.
If you visit <https://paypal.com> now, and were to click on the padlock icon up near your URL bar, you would see that it says the certificate is issued to PayPal, Inc., San Jose, CA, USA.
This is an Extended Validation SSL certificate that we can use to be sure that the owner of the certificate is who we think it is.
If paypal.com was stolen, it would not have this certificate.

Things are generally moving in the direction of HTTP deprecation.
The HTTP Strict Transport Security (HSTS) policy allows websites to specify that they should be HTTPS-only.
The browser will then refuse all traffic that is not HTTPS, and will not allow incorrect certificates.
However, this mostly relies on trust-on-first-use.
The browser must first visit the site to learn that the HSTS policy applies.
There are some exceptions to this.
Google Chrome, Mozilla Firefox, and Microsoft Edge implement a HSTS preloaded list.
This specifies which domains have this policy before ever visiting them.
All domains with the `.dev` TLD have this in place.

HTTPS is now on nearly every website.
It is time to flick the switch and disable those that do not have it supported.
Those still actively maintained and not using HTTPS can switch very easily, with services such as [Let's Encrypt](https://letsencrypt.org/) (and for free!).
Encrypted internet for all!
