---
layout: post
title:  "FT SSO Setup - Federated SSO"
date:   2016-08-30 10:00:00
---

## Prerequisites
Your organization's identity provider needs to be part of the [UKAMF](https://www.ukfederation.org.uk/) or [OpenAthens](http://www.openathens.net/) federation.

**[UKAMF](https://www.ukfederation.org.uk/)** - UK Access Management Federation or UK Federation  - provides a solution for access to online services for educational and research organisations.  The UKAMF is a UK-based federation.  

**[OpenAthens](http://www.openathens.net/)** Is both a suite of commercial products and an access management federation, all owned by the company EduServ. The FT makes use of OpenAthens SP product to manage federated SSO as a service provider. The FT is also registered in OpenAthens Federation as a service provider. OpenAthens Federation is an international access management federation, promoted for any publisher as a service provider and any identity provider that can meet the federation requirements.

**[eduGAIN](http://services.geant.net/edugain/Pages/Home.aspx)** is a service that connects many federations around the world.  The UKAMF publishes its federation metadata (participant information) to eduGAIN, as do many other federations e.g. InCommon for USA, SurfConext for Netherlands, SWAMID for Sweden.  UKAMF will automatically import all eduGain metadata that meets its standards. This means most participants registered in eduGAIN are available to UKAMF.

## FT.com SSO integration
In order to integrate your organization IDP, we only need your **IDP entity id** as configured in the access management federation.
We will use this id to configure the SSO access in FT.com.

### FT.com federation metadata information
FT.com entity Id: `https://sso.ft.com/sso/sp/oa/metadata`

Supported Bindings:

* urn:oasis:names:tc:SAML:1.0:profiles:browser-post
* urn:oasis:names:tc:SAML:1.0:profiles:artifact-01
* urn:oasis:names:tc:SAML:2.0:bindings:HTTP-POST
* urn:oasis:names:tc:SAML:2.0:bindings:HTTP-Artifact

If you have any queries, please contact the [support team](b2bsupport@ft.com)

## FT.com Autolink feature
We support an autolink feature, this will allow existing FT.com users to login with their corporate credentials without having to do a one-off FT.com setup.
In order to allow this feature, your IDP needs to send the user's email address as part of the SAML assertions.

This can be configured in your IDP.


### Appendix 1 - OpenAthens Configuration - Add email to SAML response
These are the steps in OpenAthens to add the email address to the SAML response

OpenAthens admin console: [https://admin.openathens.net](https://admin.openathens.net)

Verify that email address is a releasable attribute:

* Go to [Schema Editor](https://admin.openathens.net/#SchemaEditor) section: `Menu > Preferences > Schema Editor`
* Open the Core Attributes item: `Personal Account > Core Attributes`
* Verify the properties for the email field. It needs to display `releasable`, see image.

![OpenAthens Schema Editor](/sso-support/assets/images/openathens-schema-editor.png)

Add email address to the SAML response:

* Go to [Attribute Release](https://admin.openathens.net/#ReleasePolicies) section: `Menu > Preferences > Attribute Release`
* Click edit on the `Global (all resources)` policy. Edit appears when you hover over the policy.
* Click on `email address`. It should be displayed with a tick.
* Click `Done`
* Click on `save changes`.

![OpenAthens Attribute Release](/sso-support/assets/images/openathens-release-attributes.png)
