---
title: Configure Email Login
section: Getting Started
index: 3
---

## Enable Email Login

Select Email Login in Authentication methods and remember to press Finish

{% include full-screenshot.html file="enable-email-login-unifi.png" %}

## Configure Email Login Fields

Press the config button to configure the fields asked from guest while logging in.

{% include full-screenshot.html file="email-fields-unifi-hotspot.png" %}


## Configure Session Control

Here you can specify the limits that will be applied to a guest device after logging in.

{% include full-screenshot.html file="email-session-control.png" %}

## Configure Login Policy

Here you can specify how frequently a device will be presented with the landing page.

It can be set to Onetime/Monthly/Always.A device's MAC address is used to identify the guest next time he/she logs in. 

If the option is set to monthly, guest will be shown landing page once in 30 days.

{% include full-screenshot.html file="email-login-policy.png" %}