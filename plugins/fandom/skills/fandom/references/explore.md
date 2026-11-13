# Who is this audience?

For "who are X on YouTube", "what else do fans of Y watch", "who buys from site.com", "compare A and B".

1. **Map it.** `build_exploration_map` with the person's own words as the source: a description, a channel name or @handle, a website, a brand, a list or a project. Combine sources when they name several (up to 8). Default size is fine; use 160 for "everything".
2. **Read the groups.** Each group has people, reach, fan density, top channels and a description. The `core` groups are the audience asked about; `adjacent` groups share its commenters.
3. **Split when it helps.** `split_exploration_map` with `split`:
   - `groups` (the default) or `sub_groups` inside an opened group,
   - `themes` for what else they're into,
   - `life_stage` for the stage of life their comments point to,
   - `compare` with up to 4 products or interests,
   - `custom` with a few words ("price sensitivity").
   Open a group first with `within: [{ group: "its name" }]`. Filter with `filter: "brand-safe"`, `"family"`, or words.
4. **Explain a segment.** `get_exploration_segment` says what's behind one theme, life stage, product or custom group.
5. **Rank channels.** `list_exploration_channels` sorts by reach, fan density (`ratio`), sponsor fit, hidden gems, subscribers or name; `search` finds a channel by name or @handle; `download: true` adds a CSV.
6. **Go further.**
   - `get_map_channel`: one channel's panel on the map.
   - `get_fan_subscriptions`: what these fans subscribe to beyond the map.
   - `get_exploration_macro_view`: the wider landscape, about 1,500 channels.
   - A group's `expand` source maps that group on its own.
7. **Write it up.** `create_audience_report` turns the map into a written report (`save: true` keeps it in the workspace).
8. **Keep it.** `create_audience_from_channels` saves chosen channels as an audience, or as a draft campaign. That changes the workspace, so ask first.

Good first answer: the two or three groups that matter most, each with people, reach, fan density and three channels, plus the map link and one suggested split.
