---
layout: post
title:  "A Guide to Federated Single Sign on (FSSO)"
date:   2016-08-31 10:00:00
---
This document provides information about a new service, Federated Single Sign On (FSSO), which allows users to access FT.com using their network ID’s,  available to FT corporate, government and education customers. This documentaddresses common questions from customers regarding the terms of use. This information should be used as a guide only.

1. [What is Federated Single Sign On (FSSO)?](#what-is-federated-single-sign-on)
1. [What is Federated access?](#what-is-federated-access)
1. [What is an Access Federation?](#what-is-an-access-federation)
1. [What are the benefits of FSSO for FTcustomers?](#what-are-the-benefits-of-fsso-for-ft-customers)
1. [What is involved in joining an Access Federation?](#what-is-involved-in-joining-an-access-federation)
1. [Where can I find a list of all the Federations that the Financial Times is currently a member of?](#where-can-i-find-a-list-of-all-the-federations-that-the-financial-times-is-currently-a-member-of)
1. [I can’t join my local federation as they only currently allow education or research institutions. What are my options?](#i-cant-join-my-local-federation-as-they-only-currently-allow-education-or-research-institutions-what-are-my-options)
1. [Once I am a member of Access Federation, how do I get set up to access FT content?](#once-i-am-a-member-of-access-federation-how-do-i-get-set-up-to-access-ft-content)
1. [If I am not currently part of an Access Federation, can I still be set up with single sign on?](#if-i-am-not-currently-part-of-an-access-federation-can-i-still-be-set-up-with-single-sign-on)
1. [How are FSSO users deprovisioned?](#how-are-fsso-users-deprovisioned)
1. [How are FSSO users reprovisioned?](#how-are-fsso-users-reprovisioned)
1. [What happens if FSSO is switched on / off midway through my contract?](#what-happens-if-fsso-is-switched-on-off-midway-through-my-contract)
1. [What is a WAYFLess URL?](#what-is-a-wayfless-url)
1. [Is FSSO dependent on IP address?](#is-fsso-dependent-on-ip-address)
1. [Does the FT provide mobile FSSO?](#does-the-ft-provide-mobile-fsso)
1. [Is FSSO compatible with Access Manager?](#is-fsso-compatible-with-access-manager)
1. [Is FSSO compatible with EzProxy?](#is-fsso-compatible-with-ezproxy)
1. [I have some questions about Federated Single Sign On. Who should I contact?](#i-have-some-questions-about-federated-single-sign-on-who-should-i-contact)

### What is Federated Single Sign On?
Federated SSO is an alternative access method which allows FT customers to have full access to FT.com without having to manually login when accessing the site via an agreed route. It allows for users to be deprovisioned when an individual leaves an organisation, after a 90 day grace period.

### What is Federated access?
Federated Access Management builds a trust relationship between identity providers (IdP) and service providers (SP). It devolves the responsibility for authentication to a user’s home organisation, and establishes authorisation through the secure exchange of information (known as attributes) between the two parties.

![Federated Access](/sso-support/images/federated-access.png)

### What is an Access Federation?
Federation members needing access to resources install identity provider (IdP) software, and members providing resources install service provider (SP) software. Members sign up to an agreed set of policies for exchanging information about users and resources. The federation operator acts as a registrar for this information, which describes the configuration of the members' identity and service providers. The information is known as metadata.

How authentication is carried out by the identity provider and how rights management is carried out by the service provider is left up to the respective parties. Thus, federated access management depends on a certain level of trust. These trust agreements are managed by federations. Federations are typically being established at a national level.

[The UK Access Management for Education & Research](https://www.ukfederation.org.uk) (the UK federation) is operated by [JISC Collections](http://www.jisc-collections.ac.uk/), in partnership with [EDINA](http://www.jisc-collections.ac.uk/) (a JISC data centre), on behalf of [JISC](http://www.jisc-collections.ac.uk/).
Examples of other federations include:

* [InCommon](http://www.incommonfederation.org/) in the US
* [SWITCHaai](http://www.switch.ch/aai/docs/AAI_Org_Processes.pdf) in Switzerland
* [HAKA](http://www.csc.fi/english/institutions/haka) in Finland
* [OpenAthens](https://docs.openathens.net/display/public/OAHF/Joining+the+federation) - not tied to a location

### What are the benefits of FSSO for FT customers?
Federated SSO allows users to access FT.com using their employee or education network IDs. In addition to more convenient access for end users, FSSO offers more control and transparency for the administration of the account.

* **Low integration costs.** Available to any organisation that is a member of an Access Federation.
* **Eliminates lost or forgotten passwords.** Users have just one password to remember.
* **Simplifies administration.** Enables control of passwords from a centralised resource and automatically provision users when they leave the organisation.
* **Improves network security.** Prevents unauthorized users from accessing subscription resources.

### What is involved in joining an Access Federation?
This depends on what your current SSO capabilities are. If you already have an existing SSO infrastructure, it may be easy to join the relevant Federation. Each Federation’s website contains details of the requirements for joining.

### Where can I find a list of all the Federations that the Financial Times is currently a member of?
The FT is a member of the entire participant Federations that make up EduGate. You can see a list of the [current member federations](http://www.edugain.org/technical/status.php) here. We are also a member of the [OpenAthens federation](http://www.openathens.net/).

### I can’t join my local federation as they only currently allow education or research institutions to join, what are my options?
The OpenAthens Federation is set up specifically to work with commercial organisations. Details on their [membership criteria can be found here](https://docs.openathens.net/display/public/OAHF/Eligibility+criteria).

### Once I am a member of an Access Federation, how do I get set up to access FT.com?
Once you are a member, you will just need to supply the FT with your EntityID, which your Access Federation will supply you with. We will use this ID to add the FSSO access method to your account.

### If I am not currently part of an Access Federation, can I still be set up with single sign on?
Unfortunately, not at the moment. Our current Single Sign On solutions require the client to be a member of an Access Federation.

### How are FSSO users deprovisioned?
If an FSSO enabled user doesn’t access via the FSSO route for 90 days the FT will assume that their access has been removed on the client’s side, and the user will be deprovisioned. Deprovisioned means that the user will be automatically moved from the relevant active user group to the organisation’s inactive user group. The user will be notified that this change has happened, and that will revert to having registered access to the site. The user will also be notified after 83 days of inactivity warning them that they will shortly lose their subscription access, if they do not log in before the 90 days cut off.

### How are FSSO users reprovisioned?
If a deprovisioned user accesses the site via the FSSO route, they will be automatically reprovisioned. This means that the FT will automatically recognise that the user is coming from an FSSO enabled organisation. They will be moved from the inactive user group and will become a member of the relevant active user group where they will regain their subscription access. This will be seamless and should not be visible by the end user.

### What happens if FSSO is switched on/off midway through a contract?
FSSO can be switched on or off at any point without causing issues. If you request that FSSO be turned off during a contract, access for all previously FSSO enabled users reverts back to normal FT.com access rules. All users will have access in line with the contracted end date of the group, and the users within the group will not be automatically deprovisioned. If FSSO is then reactivated, the automated deprovisioning will restart, whereby it will go back to identify previous FSSO users or deactivate users accordingly, if their accounts are still inactive.

### What is a WAYFLess URL?
As part of your FSSO fulfilment you will be supplied with a WAYFLess URL (Where are you from? URL). A WAYFLess URL can be used to link to FT.com directly from your portal or Intranet. All users accessing will be routed back via their Identity Provider and then taken backto FT.com. Depending on their status, they will either be logged in automatically or they will be directed to the relevant sign up page.

### Is FSSO dependent on IP address?
No, FSSO doesn’t use IP address to identify what organisation a user is from. That information is passed to us securely from the users Identity Provider. All information passed from the Identity Provider and/or Federation, is encrypted before it is passed over to the FT.

### Does the FT provide mobile FSSO?
At present we cannot offer FSSO to app.ft.com. To use the web app users will still need to login using the username and password they set up when they first visited FT.com. Accessing the full site on a mobile device via the agreed FSSO route will work correctly and they user will automatically be logged in. E.g. a user accessing FT.com via the FSSO link on their company intranet whilst on their IP will get logged in seamlessly to FT.com.

### Is FSSO compatible with Access Manager?
Yes. If your organisation is interested in using Access Manager as well as FSSO both can be enabled, as long as the Access Manager is updated to include the relevant WAYFLess URL. This is needed so the users are directed back through their IDP, which ensures they are identified and redirected to the correct page.

### Is FSSO compatible with EzProxy?
Yes, as FSSO isn’t dependent on your organisation’s IP address. Use of a web proxy such as EzProxy should not cause any problems.

### I have some questions about Federated Single Sign On. Who should I contact?
For any queries about the FT’s FSSO service, please [contact](mailto:b2bproductconsultants@ft.com) our dedicated Product Consultant team directly or visit [here](http://www.ft.com/integration).
