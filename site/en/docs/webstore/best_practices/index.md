---
layout: "layouts/doc-post.njk"
title: Best Practices
date: 2017-08-30
description: >
  Best practices on how to implement your app and list it in the Chrome Web Store.
---

This page has advice on how you should implement your app and list it in the store. As the store
matures and we learn from developers' experiences, these recommendations will be updated.

## Design a high-quality extension

We encourage you to develop extensions that are of high quality. High-quality extensions conform to
standards of performance, security, and user experience, as summarized by the following guidelines:

* **Compliance:** Does the extension comply with our [program policies]? Extensions must not violate
any of these policies.

* **Manifest V3:** Is the extension built on Manifest V3? Manifest V3 is the current version of the
  Chrome extension platform and all High Quality extensions should use it. (See the [Manifest V3
  overview][mv3-overview].)

* **Security:** Is the extension safe for users? Make sure your extension does not pose security
  threats and does not use deceptive installation tactics (see [Stay secure][stay-secure] for a more
  in-depth discussion.)

* **User privacy:** Make sure that your extension handles user data appropriately and conforms to
  Chrome Web Store's data privacy requirements. (See this [FAQ][user-data-faq] for further details.)

* **Performance:** Does the extension function at an outstanding level? High-quality extensions
  don't just perform their intended action, they do so while using as few system resources as
  possible.

* **User experience:** Is the extension a joy to use? The extension itself should provide a
  good-looking, intuitive, and seamless user experience while also respecting the end user's
  privacy.

* **Store listing:** The extension's [Chrome Web Store listing][completing-listing] should sets the
  user's expectations and clearly communicates what the extension does.   All image assets (icon,
  tile, marquee, and screenshots) [should be provided][supplying-images]. Images should not be
  blurry or too busy. [Privacy information][dashboard-privacy] (permissions justifications, the extension's privacy policy, data use disclosures, etc.) must be accurate and up to date.

## Support Google Accounts

If your app requires user login, we recommend that you provide at least some support for Google
Accounts. The reason is that if a user purchases your app from the Chrome Web Store, odds are the
user is already logged into a Google Account whenever they use your app. Reducing the number of
logins improves the user's experience.

If you already have a login system, consider correlating the Google Account ID to the user account
in your system. You can do this by storing the user's OpenID URL from Google's OpenID service, in
the same way that you store other data that's associated with a user's account. When someone is
logged into a Google Account but not your login system, you can automatically log them into their
user account in your system.

See [Identifying the User][3] for more information about supporting Google Accounts.

## Keep ex-users' data for 30 days or more

You should keep users' data for at least 30 days after they cancel their subscription or uninstall
your app. Users might be unsubscribed for reasons beyond their control, and even if they do
intentionally unsubscribe or uninstall the app, they might come back.

## Cache license data

If you use a payment processor or other licensing manager, you may also want to cache the results
so that **(a)** Your user can still use the extension when they are offline, and **(b)** you
reduce the number of queries to the license server, reducing quota usage and traffic.

## Create a compelling store listing

The better your app's listing in the store, the more users will find and try your app. When choosing
your app's name, writing its description, and designing its logo, keep in mind Google's [Branding
Guidelines][7].

### Provide great images

See [Supplying Images][8] for guidelines on the images you should supply to the store.

### Choose your app's category well

The developer console lets you specify a category for each extension. Choose the category
that is most appropriate:

* Accessibility
* Blogging
* Developer Tools
* Fun
* News & Weather
* Photos
* Productivity
* Search Tools
* Shopping
* Social & Communication
* Sports


[3]: /docs/webstore/identify_user
[7]: /docs/webstore/branding
[8]: /docs/webstore/images
[9]: #top
[completing-listing]: /docs/webstore/cws-dashboard-listing/
[dashboard-privacy]: /docs/webstore/cws-dashboard-privacy/
[mv3-overview]: /docs/extensions/mv3/intro/mv3-overview/
[program policies]: /docs/webstore/program_policies/
[supplying-images]: /docs/webstore/images/
[stay-secure]: /docs/extensions/mv3/security/
[user-data-faq]: /docs/webstore/user_data/
