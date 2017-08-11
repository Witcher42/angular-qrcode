[DEBPRECATED] Angular QR Code *it*
====================

> [angular-qrcode](https://github.com/monospaced/angular-qrcode) now support both element and attribute, I will close this repository some days later.

*This repository is forked from [angular-qrcode](https://github.com/monospaced/angular-qrcode) written by [monospaced](https://github.com/monospaced). And it's based on v6.0.3 of angular-qrcode.*

*The modifies are:*

* *both element and attribute are supported*
* *require the new [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) by default*
* *no bower support*

```html
<div qrcode></div>
<!-- or -->
<qrcode></qrcode>
```

An AngularJS directive to create QR Codes using Kazuhiko Arase’s [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) library.

[See it in action](http://monospaced.github.io/angular-qrcode).

Usage
-----

as element

```html
<qrcode data="string"></qrcode>
```

with QR options

```html
<qrcode version="2" error-correction-level="M" size="200" data="string"></qrcode>
```

as a downloadable image

```html
<qrcode data="string" download></qrcode>
```

as a link to URL

```html
<qrcode data="http://example.com" href="http://example.com"></qrcode>
```

`download` and `href` can’t be used on the same element (if `download` is present, `href` will be ignored)

with expressions, observe changes

```html
<qrcode version="{{version}}" error-correction-level="{{level}}" size="{{size}}" data="{{var}} href={{var}} download"></qrcode>
```

Options
-------

Permitted values

* version: 1-10

* error-correction-level: 'L', 'M', 'Q', 'H'

* size: integer

* download: boolean

* href: URL

The amount of data (measured in bits) must be within capacity according to the selected version and error correction level, see http://www.qrcode.com/en/about/version.html.

Install
-------

```shell
npm install angular-qrcode-it
```

Include the [qrcode generator library](https://raw.github.com/monospaced/bower-qrcode-generator/master/js/qrcode.js) and the `angular-qrcode.js` script provided by this component in your app, and add `monospaced.qrcode` to your app’s dependencies.

Demo
----------------

[monospaced.github.io/angular-qrcode](http://monospaced.github.io/angular-qrcode)

Reference
----------------

[QR Code versions](http://www.qrcode.com/en/about/version.html)

[QR Code error correction](http://www.qrcode.com/en/about/error_correction.html)
