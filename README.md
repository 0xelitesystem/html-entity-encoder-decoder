# HTML Entity Encoder and Decoder

Encode text to HTML entities and decode entities back to text, in your browser. No server, no tracking, no third-party scripts.

**Live demo:** https://0xelitesystem.github.io/html-entity-encoder-decoder/

## Use

Open `index.html` in any modern browser, or visit the GitHub Pages link in the repo description.

Pick a mode and type. The output updates live.

Encode mode has two options:

- Encode only the dangerous 5 (`&`, `<`, `>`, `"`, `'`), which is what you usually want to make text safe to drop into HTML
- Encode all non-ASCII characters to numeric entities, useful for transports that only handle plain ASCII

Decode mode turns entities back into text and understands:

- Named entities (`&amp;`, `&copy;`, `&mdash;`, and the common set)
- Decimal numeric entities (`&#169;`)
- Hex numeric entities (`&#xA9;`, case-insensitive)

There is a Copy button on the output and a "move output to input" button so you can round-trip (encode, then decode the result) to confirm it matches.

## Why this exists

Plenty of online entity tools exist, but most carry ads, trackers, or a pile of third-party scripts for a job that is a few lines of JavaScript. This is the same idea, single file, no analytics, no signup, MIT licensed.

## Privacy

Everything runs in your browser. Your input and the encoded or decoded output never leave your machine. Verify by viewing the page source or by opening DevTools and watching the network tab, no requests are made.

## Run locally

```bash
git clone https://github.com/0xelitesystem/html-entity-encoder-decoder
cd html-entity-encoder-decoder
# Open index.html in your browser, or:
python -m http.server 8000
```

## Contribute

Issues and PRs welcome:

- Missing named entities you rely on
- Decoding edge cases (malformed entities, surrogate ranges)
- UI improvements (keep it minimal, no frameworks)
- Translations

Don't add: analytics, tracking, external scripts, npm dependencies. The whole point of this tool is no surveillance.

## Build

There is no build. It's a single HTML file.

## License

MIT.

## Related

- [base64-url-encoder-decoder](https://github.com/0xelitesystem/base64-url-encoder-decoder), encode and decode Base64 and Base64URL
- [json-formatter-and-validator](https://github.com/0xelitesystem/json-formatter-and-validator), format and validate JSON in your browser
- [slug-generator](https://github.com/0xelitesystem/slug-generator), turn text into clean URL slugs
