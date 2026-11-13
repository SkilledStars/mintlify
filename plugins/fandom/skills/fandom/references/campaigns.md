# A campaign with targeting, and a Google Ads draft

For "set up a campaign", "what targeting would reach…", or "put it in Google Ads". Every step here changes the workspace, so confirm what you'll create before each one.

1. **See what's there.** `get_workspace` or `search_workspace`. Reuse an existing brand, audience or data store when one fits.
2. **Brand.** `create_brand` with a name, website and description (campaigns inherit them).
3. **Data.** `create_data_store` with the YouTube channels or videos the audience watches. It collects for minutes: check `get_data_store` until it's `ready`.
   - Shortcut from a map: `create_audience_from_channels` saves map channels as a data store and an audience in one step.
4. **Audience.** `create_audience` with the data stores and a plain description of the people.
5. **Campaign.** `create_campaign` with the brand, audiences, campaign type, budget and a bidding strategy (needed later for Google Ads). Targeting starts generating.
6. **Targeting.** `get_campaign_targeting` until each audience is `ready` (30–90 seconds). Change terms with `edit_campaign_targeting` (add or remove). There is no approval step.
7. **Google Ads.** `create_google_ads_campaign` creates it **paused** (Search, Demand Gen or Display; not Video), without targeting. The person syncs it in Fandom to send the targeting, and turns it on in Google Ads to spend.
8. **Results.** `get_google_ads_performance` for an account's numbers over 7, 14, 30 or 90 days.

Good answer: what was created, the targeting highlights, the campaign link, and the two steps left in the app (sync, then turn it on).
