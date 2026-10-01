# Zero-card Cloudflare Pages setup

This project serves the original binary `tgsuser3998.mobileconfig` from a Pages Function. The payload is embedded directly in `functions/d/[token].js` as base64. It needs **no R2, D1, KV, Durable Objects, or other storage binding**.

## Deploy

1. Create a Cloudflare Pages project and upload/connect the contents of this ZIP.
2. Use the Pages Functions-compatible project layout as included. No external build step is needed.
3. Deploy. Download via `https://<your-pages-domain>/d/<any-token>`.

The `[token]` segment is retained for URL compatibility; any token returns the same embedded profile. Add token validation in the function if your application requires it.

## Integrity

- Payload size: 230079 bytes
- SHA-256: `6f97bf8647579e38656101f42a40b05c7f87cdbd0dd6cbe96c0aacd77ba3e798`
- Embedded Base64 is decoded to the same original bytes in the function.
