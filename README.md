# Fandom API docs

Source for [docs.fandom.ai](https://docs.fandom.ai), built with [Mintlify](https://mintlify.com). Pushing to `main` publishes.

- Pages: `*.mdx` and `guides/`. Navigation and theme: `docs.json`.
- API reference: `api-reference/openapi.json`, generated from the app's operation catalog. Don't edit it by hand. From the app repo:

  ```bash
  npx tsx scripts/export-openapi.ts ../mintlify/api-reference/openapi.json https://www.fandom.ai/api/v1
  ```

  The first server is what the **Try it** panel calls.

- Preview locally: `npx mint dev`. Check links: `npx mint broken-links`.
