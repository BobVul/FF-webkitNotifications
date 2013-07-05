FF-webkitNotifications
======================

A shim implementing the webkitNotifications API for Firefox.

---

With Firefox 22 came an implementation of the [draft Web Notifications](http://www.w3.org/TR/notifications/) standard. Unfortunately, many sites use the [Chromium implementation](http://www.chromium.org/developers/design-documents/desktop-notifications/api-specification), which causes several problems, due to it being experimental:

* It is slightly different from the current draft
* It is prefixed making it `window.webkitNotifications` instead of  `window.Notifications`

With Chromium [currently supporting](http://caniuse.com/notifications) the official draft API, hopefully more sites will start using it. In the meantime, however, many sites are still using the prefixed version, which is not and probably will never be fully compatible with the Firefox version.

This userscript is intended to translate calls to `webkitNotifications` intended for Chromium to calls to `Notifications` as implemented in Firefox 22 and newer. This should hopefully allow websites using the older API to operate correctly on Firefox.

---

Previously, the [HTML Desktop Notifications](https://addons.mozilla.org/en-us/firefox/addon/html-notifications/) add-on did a good job of providing a working implementation of `webkitNotifications`. However, with the introduction of native support, the maintainer has decided to discontinue the add-on.

---

Thanks to [Oliver Salzburg](https://github.com/oliversalzburg) for the userscript template (used with permission) and other assistance.

---

Current test page at [http://jsbin.com/eniqus/1/](http://jsbin.com/eniqus/1/)