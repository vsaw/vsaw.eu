---
title: "Facebook's ambition towards PGP and what could come next..."
tags: Tech IT-Security Idea
excerpt_separator: <!--more-->
---

On June 1st [Facebook offered to encrypt Emails with PGP](https://www.facebook.com/notes/protecting-the-graph/securing-email-communications-from-facebook/1611941762379302).

> It's very important to us that the people who use Facebook feel safe and can trust that their connection to Facebook is secure
>
> ...
>
> To enhance the privacy of this email content, today we are gradually rolling out an experimental new feature that enables people to add [OpenPGP](http://www.openpgp.org/) [public keys](https://tools.ietf.org/html/rfc4880) to their profile;

<!--more-->

It makes sense in a way as Notifications about Posts in your Groups may contain sensitive information that you don't want your Email provider to know about.

The interesting thing about this is that the Public Key info is also available on Facebook's [Graph API](https://developers.facebook.com/docs/graph-api/reference/v2.4/user).

## SKS Wrapper to Facebook's Graph API
Based on the Chat [Michael Duergner](https://twitter.com/duergner) and I had on [Twitter](https://twitter.com/_vsaw/status/619486319547387904) we came up with an idea how to put these keys into more widespread use:

The idea is pretty simple, a thin [Key server](https://en.wikipedia.org/wiki/Key_server_%28cryptographic%29) could take requests from PGP clients and then look for PGP keys with the same public email address on Facebook's Graph.

Of course I don't know how many users have a public Email address on Facebook and how many use PGP but potentially it could have the great advantage that you can be sure the reach the person with the associated Facebook account, something [keybase.io](https://keybase.io/) is also trying to achieve.
