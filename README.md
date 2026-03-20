# Blog

Personal blog built with Astro.

Content lives in:

- `src/data/blog` for posts
- `src/data/tools` for external app/tool links
- `src/pages/index.md` for the homepage/about copy

## Development

Requires Node.js `24`.

```bash
npm install
npm run dev
```

## Build

```bash
npm run build
npm run preview
```

## Notes

- Search is generated with Pagefind during `npm run build`.
- Site-wide metadata is configured in `src/config.ts`.
- The project started from [AstroPaper](https://github.com/satnaing/astro-paper).
