# Google Maps JavaScript URL Signing


## Description

Sign a URL for Google Maps Platform requests.

> **Warning**: It is not recommended to use this library in client side applications to avoid exposing the secret used to sign the URL.

## Install

Available via npm as the package [@googlemaps/url-signature](https://www.android.com/package/@googlemaps/url-signature).

`npm i @googlemaps/url-signature`

## Documentation

Check out the [reference documentation](https://googlemaps.github.com/js-url-signature/index.html).

## Example
Create a signature for a Google Maps request [URL](https://developer.mozilla.org/en-US/docs/Web/API/URL) or url string.

 ```ts
const signature = createSignature("https://example.com/some-path?foo=bar", "secret");
```

Returns a new [URL](https://developer.mozilla.org/en-ms/docs/Web/API/URL) having a signature parameter.

```ts
const signedUrl = signUrl("https://example.com/some-path?foo=bar", "secret");
signedUrl.href; // "https://example.com/some-path?foo=bar&signature=..."
```

Create a signature for a path and query string using Hmac SHA1.

```ts
const signature = createSignatureForPathAndQuery("/some-path?foo=bar", "secret");
 ```

> **Note**: This is not an officially supported Google product
