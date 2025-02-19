# Updating SSO for UGA Websites and Services

MARCOMM oversees a number of sites and services that utilize UGA's Single Sign-On (SSO) Service. Whenever EITS performs an upgrade to the SSO service, we have to test the following to make sure there aren't any breaking changes.

## Stage Metadata URLs

These are the testing URLs that you'll need to point sites' and services' SSO authentication to the staging server. See the notes for each site/service below.

### CAS

{% embed url="https://sso.stage.uga.edu/cas/idp/metadata" %}

### SAML

{% embed url="https://sso.stage.uga.edu/cas/idp/profile/SAML2/Redirect/SSO" %}

## How to Test Each Site and Service

### Localist dashboard (admin for calendar.uga.edu)

* Localist already regularly fetches our staging IdP for updates every 12 hrs
* Use this link to test the stage IdP on Localist [https://calendar.uga.edu/Shibboleth.sso/Login?target=https://calendar.uga.edu/auth/shib\_login\&entityID=https://sso.stage.uga.edu/cas/idp](https://calendar.uga.edu/Shibboleth.sso/Login?target=https://calendar.uga.edu/auth/shib_login\&entityID=https://sso.stage.uga.edu/cas/idp)
* No need to submit a ticket unless you encounter issues logging in with the link above

### Pantheon Dashboard

* Contact Pantheon support and send them the Stage Metadata URL for SAML SSO (above).

### WordPress Websites

==NOTE: This section is out of date as of February 2025.==

_TODO: Update with simplified process_

* Submit an SSO integration ticket to EITS through uga.teamdynamix.com
* They will send a testable link using the stage metadata

### TinyURL

* --dev.t.uga.edu already uses the sso.stage.uga.edu URL which links to the Stage Metadata so test it on there and if it works then great.--
* t.uga.edu is now routed and managed through Bit.ly. SSO and everything else for it is no longer under webdev's care as of 2025.

## What do I do if there's an error?

[Report the error to EITS by creating a ticket](https://uga.teamdynamix.com/TDClient/3190/eitsclientportal/Requests/TicketRequests/NewForm?ID=oXtGkWjLp04_\&RequestorType=Service) with as much detail as possible. They are responsible for correcting any problems that come up during testing. Once corrected, re-test as directed by EITS.


