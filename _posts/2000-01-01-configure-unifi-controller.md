---
title: Configure Unifi Controller
section: Getting Started
index: 1
---

Unifi controller needs to be configured to use Spotipo as an external portal. 

However recent versions of controller seems to have changed the external portal behaviour. So follow the below procedure.

## Enable Guest Settings with no authentication

{% include full-screenshot.html file="unifi-portal-settings.png" %}

## Configure Pre-Auth settings correctly

{% include full-screenshot.html file="unifi-portal-settings-preauth.png" %}

Remember to apply settings

## Figure out the site id

Each site in unifi controller is identified by a parameter called siteid. To identify this, login to Unifi controller and go the correct site.

Siteid will be part of the URL.

<pre>
  <code class="shell">
  https://unifi.xxxx.com/manage/site/SITEID/dashboard
  </code>
</pre>


## Enable redirection to Spotipo

Now you will need to replace the unifi's index.html file with the below script. This will redirect the Guest to correctly to spotipo.

This file is available in /var/lib/unifi/sites/SITEID/portal in case of Ubuntu/Debian

In windows this is available in ***


**Remember to replace SERVERADDRESS and SITEID**


    <!DOCTYPE HTML>
    <html lang="en-US">
        <head>
            <meta charset="UTF-8">
            <meta http-equiv="refresh" content="1;url=http://SERVERADDRESS/guest/s/SITEID/?ap=<unifi var="ap_mac" />&id=<unifi var="mac" />&ssid=<unifi var="ssid" />">

    </html>



