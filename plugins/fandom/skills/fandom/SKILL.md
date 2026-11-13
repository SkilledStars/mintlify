---
name: fandom
description: Research YouTube audiences with Fandom's MCP tools - who an audience is, creators to sponsor or advertise on, research reports, and campaigns with paused Google Ads drafts.
metadata:
  homepage: https://docs.fandom.ai/guides/skills
---

# Fandom

Fandom shows who an audience is on YouTube (the channels its people comment on, grouped by overlap, with real numbers) and turns that into creator lists, research reports and campaigns.

This skill needs Fandom's MCP server (`https://www.fandom.ai/mcp`). If its tools (such as `build_exploration_map`) aren't available, tell the person to connect it: https://docs.fandom.ai/guides/mcp. The server's own instructions and tool descriptions are the source of truth for arguments; this skill is the playbook.

## How to work

- **Map first.** Anything the person describes (an audience in words, a brand, a website, a channel, a list, a campaign) can be mapped at once with `build_exploration_map`. Maps, splits, groups, channel details and audience reports are free and change nothing: run them without asking.
- **Pass what they said.** Every tool takes channel names, @handles, YouTube channel or video links, websites, Fandom links, and the names of lists, projects, reports, brands, audiences and campaigns. Don't look ids up first.
- **Read how it was read.** Replies may start with "Read your request as: …". Mention a match only when it might not be what they meant.
- **Ask before anything paid or account-changing**: inclusion list runs, project builds, project lenses and reports, Trends watches, and any campaign, targeting or Google Ads change. Say what it will do, then wait for a yes.
- **Slow work**: a reply with `status: "working"` and a `jobId` means call `get_job` with that id until it's done. Never start the same thing again. List runs and project builds take minutes; follow them with `get_inclusion_list` or `get_project`.
- **Groups keep their names.** Refer to a map's group by its name in `within`, `segment` or a follow-up question.

## Pick the playbook

| They want | Read |
| --- | --- |
| Who an audience is, where else they gather, what they're into | [references/explore.md](references/explore.md) |
| Creators or channels to sponsor or advertise on | [references/lists.md](references/lists.md) |
| A research project with questions and a report to share | [references/projects.md](references/projects.md) |
| A campaign with targeting, or a Google Ads draft | [references/campaigns.md](references/campaigns.md) |

## Answer like an analyst

1. Lead with the finding in two or three sentences, in plain words.
2. Then a compact table, for example: group, channels, people, reach, fan density, top channels.
3. Name the comparison behind every multiple ("4.2× more common here than across YouTube").
4. Link the Fandom page from the reply's `url` so they can open it in the app.
5. End with the one next step that would help most, and offer it.

## Words to get right

- **People** are people who comment, not everyone who watches. Never claim ages, genders, incomes, watch time or private analytics; life stage and themes are inferred from what people comment on, and should be described that way.
- **Reach** is the share of the audience that also comments on a group's or channel's videos. **Fan density** is how many times more common the audience is there than across YouTube, or than the comparison the reply names.
- **Flags** on a list are a starting point for a brand-safety review, never a finding, and never a reason a channel was removed.
- **Google Ads campaigns are created paused.** Nothing spends until a person turns it on in Google Ads, and targeting reaches Google Ads when they sync the campaign in Fandom. Never say otherwise.
