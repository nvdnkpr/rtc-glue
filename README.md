# rtc-glue

Glue is a high-level approach to building WebRTC applications. It is
primarily designed for web application coders who would prefer to spend
their time in HTML and CSS rather than JS.

## Example Usage

Glue works by looking for HTML tags that follow particular conventions
with regards to named attributed, etc.  For instance, consider the
following HTML:

```html
<html>
<body>
<script src="index.js"></script>
</body>
</html>
```

When combined with this simple JS gives you the following:

```js
var glue = require('rtc-glue')(document);
var quickconnect = require('rtc-quickconnect');

// when we get a peer connect them in the html
quickconnect.on('peer', glue.connect);
```