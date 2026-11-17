# A campaign with targeting, and a Google Ads draft

For "set up a campaign", "what targeting would reach…", or "put it in Google Ads". Every step here changes the workspace, so confirm what you'll create before each one.

1. **See what's there.** `get_workspace` or `search_workspace`. Reuse an existing brand, audience or data store when one fits.
2. **Brand.** `create_brand` with a name, website and description (campaigns inherit them).
3. **Data.** `create_data_store` with the YouTube channels or videos the audience watches. It collects for minutes: check `get_data_store` until it's `ready`.
   - Shortcut from a map: `create_audience_from_channels` saves map channels as a data store and an audience in one step.
4. **Audience.** `create_audience` with the data stores and a plain description of the people.
5. **Campaign.** `create_campaign` with the brand, audiences, campaign type, budget and a bidding strategy (needed later for Google Ads). Targeting starts generating.
6. **Targeting.** `get_campaign_targeting` until each audience is `ready` (30–90 seconds). Change terms with `edit_campaign_targeting` (add or remove). There is no approval step.
7. **Google Ads.** `create_google_ads_campaign` creates it **paused** (Search, Demand Gen or Display; not Video), without targeting.
8. **Sync.** `get_google_ads_sync_status` says what's waiting. `sync_campaign_to_google_ads` sends settings, then each audience's targeting into its own ad group, then saved creative, as the page's Sync (ask first). If Google Ads was changed since the last sync it sends nothing: show `check_google_ads_changes`, settle with `resolve_google_ads_changes` (both sides' edits by default), then sync again. Video targeting can't be pushed: `export_campaign_targeting` gives the Google Ads Editor file.
9. **Existing campaigns.** `list_google_ads_campaigns` then `import_google_ads_campaign` brings one in with its ad groups as audiences.
10. **Results.** `get_campaign_performance` for one campaign (summary, by ad group or by day), `get_google_ads_performance` for an account.

Good answer: what was created or synced (what Google Ads confirmed, and anything it refused), the campaign link, and the one step left: turning it on in Google Ads.
