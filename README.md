# Session Management Sample App

POC for session management spec integration into Auth0.js

## OIDC Session Management

Currently in [draft 28](https://openid.net/specs/openid-connect-session-1_0.html#OPiframe), this spec provides a mechanism whereby state changes in end users' authentication can be detected without network traffic against the OP.

Makes use of two iFrames (one for OP, one for RP) with [postMessage](https://developer.mozilla.org/en-US/docs/Web/API/Window/postMessage) events for cross-iFrame communication.

## OP Setup

#### Create an API

Create a new API in the [APIs section](https://manage.auth0.com/#/apis) and provide an identifier for it.

#### Set the Client ID, Domain, and API URL

If you download the sample from the quickstart page, it will come pre-populated with the **client ID** and **domain** for your application. If you clone the repo directly from Github, rename the `auth0-variables.js.example` file to `auth0-variables.js` and provide the **client ID** and **domain** there.

#### Set Up `Allowed Web Origins` in the dashboard
In order to make `checkSession` work, you need to add the URL where the authorization request originates from, to the Allowed Web Origins list of your Auth0 client in the Dashboard under your client's Settings.

## License

This project is licensed under the MIT license. See the [LICENSE](LICENSE.txt) file for more info.
