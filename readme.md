# MaxMind GeoIP for Dashboard

[Dashboard](https://github.com/userdashboard/dashboard) is a NodeJS project that provides a reusable account management system for web applications.  This module adds [MaxMind GeoIP](https://maxmind.com) lookup and binds a Country object to each HttpRequest.

## Development status

MaxMind GeoIP module is ready to use.  The following work remains:

- add routes to expose more of MaxMind's functionality, please help

## Import this module

Edit your `package.json` to activate the module:

    "dashboard": {
      "modules": [
        "@userdashboard/maxmind-geoip
      ]
    }

Install the module with NPM:

    $ npm install @userdashboard/maxmind-geoip

## Startup configuration variables

Check `start-dev.sh` to see the rest of the `env` variables that configure Dashboard:

    $ node main.js

# Dashboard

Dashboard proxies your application server to create a single website where pages like signing in or changing your password are provided by Dashboard.  Your application server can be anything you want, and use Dashboard's API to access data as required.  Using modules you can expand Dashboard to include organizations, subscriptions powered by Stripe, or a Stripe Connect platform.

## Support and documentation

Join the freenode IRC #dashboard chatroom for support.  [Web IRC client](https://kiwiirc.com/nextclient/)

- [Developer documentation home](https://userdashboard.github.io/home)
- [Administrator documentation home](https://userdashboard.github.io/administrators/home)
- [User documentation home](https://userdashboard.github.io/users/home)

### Case studies 

`Hastebin` is an open source pastebin web application.  It started as a service for anonymous guests only, and was transformed with Dashboard and modules into a web application for registered users, with support for sharing posts with organizations and paid subscriptions.

- [Hastebin - free web application](https://userdashboard.github.io/integrations/converting-hastebin-free-saas.html)
- [Hastebin - subscription web application](https://userdashboard.github.io/integrations/converting-hastebin-subscription-saas.html)

## Screenshots of Dashboard with Maxmind GeoIP

The user and administration documentation contain screenshots demonstrating Dashboard and its modules in use. 

| ![Guest landing page](https://userdashboard.github.io/outline.png?raw=true) | 
|:---------------------------------------------------------------------------------------------------------------:|
| How content is separated between dashboard and application servers |

| ![Administration page](https://userdashboard.github.io/integrations/convert-hastebin-subscription-saas/12-owner-views-customers-subscriptions.png?raw=true) |
|:---------------------------------------------------------------------------------------------------------------:|
| Administration page provided by Dashboard |

| ![Example app integrating Dashboard ](https://userdashboard.github.io/integrations/convert-hastebin-subscription-saas/9-second-customer-creating-post-shared-with-organization.png?raw=true) |
|:---------------------------------------------------------------------------------------------------------------:|
| Dashboard's header with content served by application server |

## Dashboard modules

Additional APIs, content and functionality can be added by `npm install` and nominating Dashboard modules in your `package.json`.  You can read more about this on the [Dashboard package.json documentation](https://userdashboard.github.io/dashboard-package-json.html)

    "dashboard": {
      "modules": [ "package", "package2" ]
    }

Modules can supplement the global.sitemap with additional routes which automatically maps them into the `Private API` shared as global.api.

| Name | Description | Package   | Repository |
|------|-------------|-----------|------------|
| MaxMind GeoIP | IP address-based geolocation | [@userdashboard/maxmind-geoip](https://npmjs.com/package/userdashboard/maxmind-geoip)| [github](https://github.com/userdashboard/maxmind-geoip) |
| Organizations | User created groups | [@userdashboard/organizations](https://npmjs.com/package/userdashboard/organizations) | [github](https://github.com/userdashboard/organizations) |
| Stripe Subscriptions | SaaS functionality | [@userdashboard/stripe-subscriptions](https://npmjs.com/package/userdashboard/stripe-subscriptions) | [github](https://github.com/userdashboard/stripe-subscriptions) |
| Stripe Connect | Marketplace functionality | [@userdashboard/stripe-connect](https://npmjs.com/package/userdashboard/stripe-connect) | [github](https://github.com/userdashboard/stripe-connect)

#### Development

Development takes place on [Github](https://github.com/userdashboard/maxmind-geoip) with releases on [NPM](https://www.npmjs.com/package/@userdashboard/maxmind-geoip).

#### License

This software is distributed under the MIT license.
