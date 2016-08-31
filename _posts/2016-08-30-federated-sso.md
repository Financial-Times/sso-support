---
layout: post
title:  "FT SSO Setup - Federated SSO"
date:   2016-08-30 10:00:00
---

# Introduction
SSO config for federated SSO

## Prerequisites
Your organization's identity provider needs to support SAML.

Be part of the [UKAMF](https://www.ukfederation.org.uk/) or [OpenAthens](http://www.openathens.net/) federation.

OpenAthens Is both a suite of commercial products and an access management federation, all owned by the company EduServ. The FT makes use of OpenAthens SP product to manage federated SSO as a service provider. The FT is also registered in OpenAthens Federation as a service provider. OpenAthens Federation is an international access management federation, promoted for any publisher as a service provider and any identity provider that can meet the federation requirements.

eduGAIN is a service that connects many federations around the world.  The UKAMF publishes its federation metadata (participant information) to eduGAIN, as do many other federations e.g. InCommon for USA, SurfConext for Netherlands, SWAMID for Sweden.  UKAMF will automatically import all eduGain metadata that meets its standards. This means most participants registered in eduGAIN are available to UKAMF.

## FT.com Autolink feature
We support an autolink feature, this will allow existing FT.com users to login with their corporate credentials without having to do a one-off FT.com setup.
In order to allow this feature, your IDP needs to send the user's email address as part of the SAML assertions.

This can be configured in your IDP.

## FT.com SSO integration
In order to integrate your organization IDP, we only need the entity id as configured in the access management federation.
We will use this id to configure the SSO access in FT.com.

## Configure IDP - OpenAthens
These are the steps in OpenAthens to add the email address to the SAML response
