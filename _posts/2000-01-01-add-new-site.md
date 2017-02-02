---
title: Add new site
section: Getting Started
index: 2
---

Spotipo follows UniFi controller's philosophy of organizing networks into sites. Each site represent a physical location that can be independently managed. Site will be associated with a Client.

## Create a site

Select Add New Site option by clicking Dashboard selector.

{% include full-screenshot.html file="add-site.png" %}

## Provide basic details

Enter basic details like a Name for this site, select the client and timezone info. Save changes.

{% include full-screenshot.html file="add-site-details.png" %}

## Switch to site view

After adding basic details, you should be able to see the site you just added listed in the dashboard selector. Click on it to switch to Site View

{% include full-screenshot.html file="site-view.png" %}


## Configure UniFi Site Name

Go to the settings tab and select the corresponding site in controller.

{% include full-screenshot.html file="site-general-settings.png" %}

## Configure Login methods

Go to the Authentication tab and select the Login methods you want to enable for this. Reffer to each methods documentation for further details.

{% include full-screenshot.html file="login-methods.png" %}

## Configure Reports

Currently only text reports are supported. Details of the guests logged in can be mailed monthly/weekly to client's emails.

{% include full-screenshot.html file="reports.png" %}

## Configure Redirects

Guests can be redirected to a URL of your choosing after logging in. However note that some mobile browsers automatically close the windows after detecting an internet connection.

{% include full-screenshot.html file="redirects.png" %}

