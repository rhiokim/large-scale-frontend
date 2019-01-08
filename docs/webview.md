# Webview

If you make Webview based web application, need to consider follow things

## Development

* defining the version and environments android/ios
* multiple webview with microservice for SRE
  * display products/reservation/payment/social/profile
  * domain strategy
* design web components
  * native e.g.) alert, toast
  * global scope components. e.g.) dialog
  * common components. e.g.) header, footer, container, page, icon
* cookie control
* firebase/google analytics
* design page routing path
* applink, deeplink
* CORS issue (local env)
* version logic.

## Build

* code splitting
* optimization
* service worker
* nginx configuration

## Invoke Native

* from web to native
  * webview close point
  * interaction with 2 more webview transactions
* from native to web
  * callback

## Deploy

* environments local/development/staging/prodcution
* resource 404 not found

## Testing & Debuging

* web app testing with local env
* android
  * chrome://inspect

## Logging

* sentry - third party
* server (node.js)