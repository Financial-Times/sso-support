---
layout: post
title:  "FT SSO Setup - Federated SSO"
date:   2016-08-30 10:00:00
---

# Introduction
SSO config for federated SSO

## Prerequisites
Your corporate identity provider needs to support SAML. Our system supports SAML 1.2

Be part of the [UKAMF](https://www.ukfederation.org.uk/) or [OpenAthens](http://www.openathens.net/) federation.

If your organization is outside the UK, being part of the eduGAIN federation will work as well. UKAMF imports IDPs metadata from the eduGAIN federation if it is compatible with UKAMF metadata. The only condition is that your organization metadata needs to be compatible with the UKAMF.

## FT.com Autolink feature
We support an autolink feature, this will allow existing FT.com users to login with their corporate credentials without having to do a one-off FT.com setup.
In order to allow this feature, your IDP needs to send the user's email address as part of the SAML assertions.

This can be configured in your IDP.

## Configure IDP - Open Athens
SAML metadata url

## FT.com SSO integration
We need:
* IDP entity id

Configure your IDP:
*
