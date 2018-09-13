To facilicate API access to mailgun, some additional configuration may be required. This is due to cURL not having the certificates needed to connect to HTTPS by default. To resolve this:
1. Download `cacert.pem` from [curl.haxx.se](https://curl.haxx.se/ca/cacert.pem).
2. Copy to a safe folder, such as `php/extras/ssl/cacert.pem`.
3. Add `curl.cainfo="path/to/cacert.pem"` to `php.ini`.
4. Restart server.

To run your migrations simply re-run the Bakery migrate from your command line, in UserFrosting's root directory:
$ php bakery migrate