### CometD-Z85
[Z85](https://rfc.zeromq.org/spec/32/) encoding/decoding implementation with automatic padding.

```javascript
const Z85 = require('cometd-Z85');

// The source bytes (e.g. from an image).
const imageBytes = [0xC, 0x0, 0xF, 0xF, 0xE];

// Z85-encode the bytes into a string.
const string = Z85.encode(imageBytes);

// The encoded image bytes can be stored in a JSON field.
const json = {
  image: string
};


// A Z85-encoded image in a JSON field.
const string = json.image;

// Z85-decode into bytes.
const buffer = Z85.decode(string);

// Use the bytes in a Blob.
const blob = new Blob([buffer], { type: 'image/png' });
```
