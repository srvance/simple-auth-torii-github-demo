# Combining `ember-simple-auth` and `torii` Demo App

This ember app demonstrates how to authenticate and authorize an Ember app to use the GitHub APIs using
[ember-simple-auth](http://ember-simple-auth.com/) and [torii](http://vestorly.github.io/torii/). It
follows the narrative in the `ember-simple-auth`
[guide](https://github.com/srvance/ember-simple-auth/blob/auth-torii-github-guide/guides/auth-torii-with-github.md)
on the same topic. Each commit corresponds to a section of the guide, with some corrections
at the end.

You will need to add a `.env` file to the project root with your application client ID
from your [GitHub OAuth Application](https://github.com/settings/developers) registration
and token exchange URL. The token exchange URL below uses the `http-mock` implementation
in the project.

```
GITHUB_DEV_CLIENT_ID=<YOUR CLIENT ID>
DEV_TOKEN_EXCHANGE_URL=http://localhost:4200/api/token
```

You will also need to create a `/server/settings.js` file for the token exchange
server's parameters, also from your OAuth Application registration.

```js
module.exports = {
  CLIENT_ID: '<YOUR CLIENT ID>',
  CLIENT_SECRET: '<YOUR CLIENT SECRET>',
  USER_AGENT: '<YOUR APPLICATION NAME>'
};
```

## Prerequisites

You will need the following things properly installed on your computer.

* [Git](http://git-scm.com/)
* [Node.js](http://nodejs.org/) (with NPM)
* [Bower](http://bower.io/)
* [Ember CLI](http://ember-cli.com/)
* [PhantomJS](http://phantomjs.org/)

## Installation

* `git clone <repository-url>` this repository
* `cd simple-auth-torii-github-demo`
* `npm install`
* `bower install`

## Running / Development

* `ember serve`
* Visit your app at [http://localhost:4200](http://localhost:4200).

### Building

* `ember build` (development)
* `ember build --environment production` (production)
