---
title: Configure Facebook Login
section: Getting Started
index: 5
---

## Assign a domain name to the spotipo server

Spotipo must be hosted on a server accessible via domain name. Please refer to [Configure Unifi Controller,Configure Unifi Controller] and in **step 5 you are using a domain name (FQDN) as the SERVERADDRESS**

Guest must be redirected to landing page using domain name (FQDN) not via IP address.

## Pre-Authorize facebook IPs

Guest must be able to access facebook without logging in for FB login to work. 

Please add following IPs to the **Pre-Authorized list** in Unifi controller

<pre>
    <code class="shell"> 
        129.134.0.0/16
        157.240.0.0/16
        173.252.64.0/18
        179.60.192.0/22
        185.60.216.0/22
        204.15.20.0/22
        31.13.24.0/21
        31.13.64.0/18
        45.64.40.0/22
        66.220.144.0/20
        69.63.176.0/20
        69.171.224.0/19
        74.119.76.0/22
        103.4.96.0/22
    </code>
</pre>

## Create a facebook APP

Go to https://developers.facebook.com and create a new APP by providing relevent details

{% include full-screenshot.html file="fb-create-app.png" %}

## Add and configure Facebook Login

After creating new APP, go to Products and add Facebook Login.

{% include full-screenshot.html file="fb-app-add-login.png" %}

## Configure OAuth settings

Configure OAuth settings using the domain name (FQDN) of your server.

You must have configured it in Step1

{% include full-screenshot.html file="fb-app-oauth-settings.png" %}


## Choose Website as the platform

Go to Dashboard tab and add WWW as the platform.

{% include full-screenshot.html file="fb-app-choose-platform.png" %}



{% include full-screenshot.html file="fb-app-choose-website.png" %}

## Configure Site URL

Scroll down and enter the domain name(FQDN) of your server as the site URL
{% include full-screenshot.html file="fb-app-site-url.png" %}

## Configure app domain

Go to Dashboard and configure App domain.

{% include full-screenshot.html file="fb-app-domain.png" %}

## Note down the APP ID and APP Secret

You need to provide these two while configuring Facebook Login in Spotipo.

{% include full-screenshot.html file="fb-app-id-secret.png" %}


## Enable Facebook Login in Spotipo

Go to Settings-> Authentication Methods and enable Facebook Login. Make sure to configure FB APP ID and Secret correctly.

{% include full-screenshot.html file="fb-settings.png" %}


Here you can see quick video.

<iframe width="560" height="315" src="https://www.youtube.com/embed/CKgyezNzcdY" frameborder="0" allowfullscreen></iframe>