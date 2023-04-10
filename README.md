# Stimulus Web Authn

A Stimulus controller to implement web authn client side.

## Installation

```shell
$ yarn add stimulus-web-authn
```

## Usage

Register the controller with Stimulus:

```javascript
// application.js
import { Application } from "@hotwired/stimulus"
import WebAuthnController from "stimulus-web-authn"

const application = Application.start()
application.register("web-authn", WebAuthnController)
```

## Basic Example

```html
<div
  data-controller="web-authn"
  data-web-authn-loading-class="web-authn-loading"
  data-web-authn-challenge-url-value="https://myapp.com/two_factor_authentication/challenge/web_authn/new"
  data-web-authn-verification-url-value="https://myapp.com/two_factor_authentication/challenge/web_authn"
  data-web-authn-fallback-url-value="/two_factor_authentication/challenge">

  <p data-web-authn-target="error" />

  <button type="button" data-web-authn-target="button" data-action="web-authn#getCredential">
    Use security key
  </button>
</div>
```

## 👷‍♂️ Contributing

Do not hesitate to contribute to the project by adapting or adding features ! Bug reports or pull requests are welcome.

## 📝 License

This project is released under the [MIT](http://opensource.org/licenses/MIT) license.
