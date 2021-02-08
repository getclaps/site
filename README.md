---
layout: landing
logo: |
  <clap-button text-placement="bottom" messages style="width:8rem;height:8rem;margin:0 auto;font-size:1.2rem"></clap-button>
description: >
  A zero-config **Clap Button** that combines [**Analytics**](#privacy-preserving-analytics) 
  with Cookie Clicker-like [**Engagement**](#cookie-clicker-like-engagement).
permalink: /
---

# Clap Button

{% include form.html %}
<!--end_header-->

* Table of Contents
{:toc .large-only}


## Privacy-Preserving Analytics

Clap Button doubles as a privacy-friendly analytics solution. 
It track pages, not people.

Unlike other analytics solutions, Clap Button also gives you insights along a second dimension: 
Claps, an anonymous, self-selected score of which parts users _love_.


## Cookie Clicker-like Engagement

Clap Button improves your SEO ranking by keeping users engaged on your site. 

The component is designed to draw attention and keeps visitors active with it's Cookie Clicker[^1]-like mechanics,
which are exploiting the fact that clicking something repeatedly is oddly satisfying.


## Living on the Edge

Clap Button is built on fully managed, globally distributed infrastructure. 
Response times are fast and it scales automatically to any load. 

***

## Zero-Config Example

The clap button is a custom element that can be added directly to the page. Here is a minimal example:

The example only works if your site is hosted on __localhost__ or with an [active subscription](#pricing) otherwise.
{:.note.smaller.mb2}

```html
<head>
  <script type="module" src="https://unpkg.com/@getclaps/button"></script>
</head>
<body>
  <clap-button></clap-button>
</body>
```
{:.larger}

This will render the following button:

<clap-button></clap-button>


## Pricing

The Clap Button backend service is __$5.00 per month__ per origin for early-adopters. 
Currently, this is limited to 25,000 views per month. Higher tier plans will be added on demand.

After you've completed the payment you'll be taken to your dashboard, where you'll be able to enter your domain. 
After this step, `<clap-button/>` will work immediately on your site. 

{% include form.html btn_size="btn-lg" cancel_url="/#pricing" %}

_Note that the Clap Button Dashboard is work in progress._
_You can view relevant information and manage your subscription._
_However, it is not looking super-pretty right now. See screenshot below:_
{:.note title="Important" style="margin-bottom:2rem"} 

<picture>
  <source srcset="assets/img/dashl.jpg" media="(prefers-color-scheme: dark)">
  <img src="assets/img/dashd.jpg" class="lead" alt="Logo" width="172" height="172">
</picture>

The Clap Button Dashboard
{:.figcaption}


## Limitations

Currently, usage it limited to smaller to medium-sized websites. 
The infrastructure supports much higher volumes, but metering is not implemented yet. 
[Please contact me](mailto:getclaps@qwtel.com) if that's something you're interested in.

<!-- Don't feel like typing an email to a human? [Subscribe to our newsletter](#subscribe) instead and get informed when high-volume plans arrive.
{:.note.smaller.mb2 title="Hey there!"} -->

Views per month
: 25,000

Dashboards per subscription
: 1

Pages per domain
: 10,000

Fragments per URL (e.g. `/path#fragment`)
: 64


## Close To Open Source

The web component and core of the backend are open sourced under [MIT](licenses/MIT.md) and can be used within the limits of this license.

Only the database layer and billing module remain closed source. You are free to provide your own implementation of the Data Access Objected based on the [public interface](https://github.com/getclaps/worker/blob/master/src/dao.ts).
See the [repository](https://github.com/getclaps/worker) for more.


[^1]: [Cookie Clicker](http://orteil.dashnet.org/cookieclicker/) is a popular online game that pioneered the "clicker" genre, where the main mechanic is clicking a single button. Much like clap buttons, it's using the fact that clicking something repeatedly is oddly satisfying.

[^2]: Note that claps will be deleted after 24 hours when they are hosted on localhost.


<style>
  .page > p { position: relative }
  .page > hr { margin: 4rem 0 }
</style>