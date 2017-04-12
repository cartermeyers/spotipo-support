---
title: Install PRO License
section: Installation
index: 0
---

Spotipo PRO is available on Ubuntu(14.04+) and Debian (8+)

## Get License

You should have received a license key by email after purchasing spotipo PRO. If you haven't already, please get a trial license from <a href="https://customer.spotipo.com/free-trial/">here</a>.

## Apply License

Go to Dashboard -> Manage -> General Settings and paste the license key you have received over email. Save the changes

{% include full-screenshot.html file="spotipo_pro_license_apply.png" %}

## Restart spotipo

Spotipo needs to be restarted for license to take effect.

<pre>
  <code class="shell">
  sudo service supervisor restart
  </code>
</pre>
