---
layout: post
title:  "Domain + Github pages + Cloudflare"
date:   2015-07-30 20:04:00
categories: blog
---

We finally have a brand new domain - <https://fen4o.com> and it uses
[CloudFlare](https://www.cloudflare.com) for caching, force HTTPS and other
goodies.

Setup is easy:

* buy domain
* register at [CloudFlare](https://www.cloudflare.com)
* at your domain provider set Nameservers to point to CloudFlare's Nameservers
  (you can see those in the configuration for your site)
* add at least 2 CNAME records to your DNS record at CloudFlare

  * CNAME `your-domain.com` `your-github-name.github.io`
  * CNAME `www` `your-github-name.github.io`

    CloudFlare provides CNAME Flattening and you can safely use CNAME for root
    CNAME records.

* add `CNAME` file to `your-github-name.github.io` containing `your-domain.com`
* wait till domain information propagates

Cheap and quick to setup.

Try it!
