# Fandom API docs

Source for [docs.fandom.ai](https://docs.fandom.ai), built with [Mintlify](https://mintlify.com). Pushing to `main` publishes.

- Pages: `*.mdx` and `guides/`. Navigation and theme: `docs.json`.
- Don't put a page at `/mcp`: Mintlify serves its own docs-search MCP server there, so readers get raw JSON instead of the page. The guide lives at `guides/mcp`.
- The MCP guide's connection steps come from each app's own docs and change often. Recheck them when you touch that page.
- API reference: `api-reference/openapi.json`, generated from the app's operation catalog. Don't edit it by hand. From the app repo:

  ```bash
  npx tsx scripts/export-openapi.ts ../mintlify/api-reference/openapi.json https://www.fandom.ai/api/v1
  ```

  The first server is what the **Try it** panel calls.

- Preview locally: `npx mint dev`. Check links: `npx mint broken-links`.
