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

## Enable required ports on the site

Please enable following ports in your firewall/AWS console if required.

<pre>
    <code class="shell"> 
    22
    80
    8081
    8080
    8443
    8880
    8843

    </code>
</pre>

## Figure out the site id

Each site in unifi controller is identified by a parameter called siteid. To identify this, login to Unifi controller and go the correct site.

Siteid will be part of the URL.

{% include full-screenshot.html file="unifi-controller-siteid.png" %}

## Enable redirection to Spotipo

Now you will need to replace the unifi's index.html file with the below script. This will redirect the Guest to correctly to spotipo.

This file is available in /var/lib/unifi/sites/{**SITEID**}/portal in case of Ubuntu/Debian

In windows this is available in C:\Users\ **WINDOWS USERNAME** \Ubiquiti UniFi\data\sites\ **SITEID**


**Remember to replace SERVERADDRESS and SITEID**


    <!DOCTYPE HTML>
    <html lang="en-US">
        <head>
            <meta charset="UTF-8">
            <meta http-equiv="refresh" content="1;url=http://SERVERADDRESS/guest/s/SITEID/?ap=<unifi var="ap_mac" />&id=<unifi var="mac" />&ssid=<unifi var="ssid" />">

    </html>



