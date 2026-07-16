# ClearFocus

A small, privacy-minded background removal tool that runs image segmentation in
the browser and exports the result as a transparent PNG.

[Try the live demo](https://remove-ashy-three.vercel.app)

## What it demonstrates

- Client-side image processing with `@imgly/background-removal`
- Dynamic model loading and progress feedback
- Drag-free, mobile-friendly upload and download flow
- A dependency-free interface built with semantic HTML, CSS and JavaScript

Images are processed in the browser. The segmentation model and its runtime are
loaded from third-party CDNs, so the first run requires a network connection.

## Run locally

Serve the directory with any static server:

```bash
python3 -m http.server 8081
```

Then open <http://localhost:8081>. Opening `index.html` directly may prevent the
browser from loading the ES module because of local-file security restrictions.

## Limitations

- Output quality depends on the upstream segmentation model.
- Large images can be slow or memory-intensive on mobile devices.
- There is currently no offline model cache or automated test suite.

## Tech

HTML, CSS, JavaScript, WebAssembly-backed browser inference, Vercel.
