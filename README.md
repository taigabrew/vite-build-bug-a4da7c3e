# Vite build bug

Build ends with error if [inlined workers](https://github.com/vitejs/vite#inline-web-workers) is used in app.
`indexHtmlPath` in [build/index.ts](https://github.com/vitejs/vite/blob/2055b0c21c5fd7f9e69dc38e19ae092a6656962e/src/node/build/index.ts#L585) concatinates `outDir` twice because of createEmitPlugin double call

Vite version: v1.0.0-rc.9