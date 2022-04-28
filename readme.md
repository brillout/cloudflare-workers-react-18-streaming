Reproduction showing that Cloudflare Workers (`@cloudflare/wrangler@1.19.12`) doens't work with React 18 (`react@18.1.0`) wth SSR streaming (`renderToReadableStream()`).

1.  Installation:
    ```bash
    pnpm install
    ```
2.  Observe how it works with miniflare:
    ```bash
    pnpm run preview:miniflare
    ```
    Then go to [localhost:3000](http://localhost:3000).
3.  Observe how it doesn't work with wrangler:
    ```bash
    pnpm run preview:wrangler
    ```
    Then go to [localhost:3000](http://localhost:3000) and see how the following error is thrown: https://github.com/cloudflare/wrangler/issues/2235 (even though the flag `streams_enable_constructors` is enabled).
