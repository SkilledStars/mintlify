# Creators to sponsor or advertise on

For "find creators for…", "build a placement list", "which channels should we sponsor", or a pasted brief.

1. **Read the brief.** `propose_inclusion_list` with the brief, email or a few words. It saves nothing. Show the person the proposed seeds, topic, size and filters.
2. **Check the seeds.** `check_inclusion_channels` with the seed channels (names or links) says how much data each has: Tier A is ready, D can't be used. Suggest swapping weak seeds.
3. **Ask, then build.** Creating a list starts a paid run. Confirm the settings (seeds or topic, size, minimum subscribers, US only), then call `create_inclusion_list`.
4. **Follow it.** `get_inclusion_list` until the run is done (minutes). Don't start another run meanwhile.
5. **Read it.** `list_inclusion_list_channels`:
   - `ranked` is the list,
   - `full` is everything found,
   - `fan_density` shows channels a seed's commenters subscribe to far more than usual,
   - `flagged` shows brand-safety flags for review (`onList` says which are on the ranked list).
6. **Hand it over.** `export_inclusion_list` gives a link: `google_ads_csv` for placements, `full_csv`, or a `workbook`. Links last 24 hours.
7. **Change it.** `update_inclusion_list` edits settings (seeds, excluded channels, size, filters). Running it again (`run_inclusion_list`) is paid: ask first.

Good answer: how many channels, the top ten with why each fits, anything flagged on the list itself, and the download link.
