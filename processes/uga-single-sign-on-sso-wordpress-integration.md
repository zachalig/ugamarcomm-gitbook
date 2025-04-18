---
icon: shop-lock
---

# UGA Single Sign-on (SSO) WordPress Integration

_Note:_ This guide is an incomplete work in progress based on rough notes during the integration of [Game Changers](https://gamechangers.uga.edu).

1. Create a SSO Integration Request via EITS [https://uga.teamdynamix.com/TDClient/2060/Portal/Requests/ServiceDet?ID=36868](https://uga.teamdynamix.com/TDClient/2060/Portal/Requests/ServiceDet?ID=36868)
2. Supply them with dev, stage, and test URLs.
3. They will reply asking you to test on the development environment.
4. Create a Test MyID using this ticket. [https://uga.teamdynamix.com/TDClient/2060/Portal/Requests/TicketRequests/NewForm?ID=ZNBLPgnzuY8\_\&RequestorType=Service](https://uga.teamdynamix.com/TDClient/2060/Portal/Requests/TicketRequests/NewForm?ID=ZNBLPgnzuY8_\&RequestorType=Service)
5. I use a WordPress plugin called “Authorizer”. Base settings off previously configured SSO website.
6. For dev and stage environments, you’ll use the hostnames [sso.dev.uga.edu](http://sso.dev.uga.edu/) and [sso.stage.uga.edu](http://sso.stage.uga.edu/) respectively.
