# Khet Chalo Website — Project Context

## What this is
Static site (plain `index.html` + `styles.css`, no build tooling/framework)
for **Khet Chalo** — a working farmhouse channel on the Yamuna Expressway
belt, near Jewar Airport. Content: daily farm life, vegetables, dairy, goats,
poultry. `assets/` holds photos (farm, cottage, fields, solar, etc.) used
directly by `index.html`.

No package.json, no backend here — this is the landing/brand site, separate
from the Instagram/Facebook/n8n content pipeline described in the
`khet-chalo-farm` skill (solar system specs, farm setup, teaser content
pipeline, khetchalo.shop).

## Who I'm working with
Maneesh (travelagentmaneesh@gmail.com) — not a developer, thinks in outcomes.
Communicates in Hinglish; prefers direct, concise answers over long option
surveys. See the `khet-chalo-farm` skill for hard-won facts about the actual
farm (solar/inverter/battery specs, move-in details) before quoting numbers
or making claims about the property.

**Where friction usually happens:** unfamiliarity with a given platform's UI
(hosting dashboard, DNS, social APIs), not technical skill — this used to
mean slow back-and-forth just to find where a setting lives.

## Standing workflow rules (apply every session, this repo and others)
0. **Check it yourself before asking — no exceptions.** If any tool already
   available in the session can answer the question, call it before asking
   the user. Never ask "do you have X", "is this connected", "does this
   repo/account exist", or "where do I find Y" when a tool call resolves it
   directly (`list_repos`, a connector's own list/search call, a web
   search, etc.). **Concrete failure to never repeat:** asked "are Khet
   Chalo and Shivnandini repos on GitHub?" instead of just calling
   `list_repos` — which was already available and used moments later
   anyway. Only ask the user when the answer needs their login/credentials,
   is a judgment call only they can make, or every available tool has
   already been checked and still can't tell.
1. **Check for a connected MCP/connector or plugin before doing anything
   manually.** Vercel, GitHub, n8n, HTML/CSS-to-Image, and other MCP tools
   may be available in a given session — use them directly instead of
   asking the user to click through a dashboard.
2. **If no connector exists for a platform, research it yourself first**
   (web search / fetch docs) instead of asking the user to go discover
   steps manually. Only ask when it genuinely needs their login, a
   judgment call, or an action only they can authorize.
3. **Chrome extension** (Claude in Chrome) is a fallback for directly
   seeing/interacting with a live site when no API/MCP path exists.
4. **Manual instructions to the user are the last resort**, not the default.
5. When blocked (missing connector auth, no repo access, etc.), say so
   plainly and point to the fix — don't guess or fabricate steps.

This same CLAUDE.md pattern also exists in `YEIDA_website` and
`shivnandiniinfra-website` — keep them consistent when updating the rules.

## Full portfolio
See `PORTFOLIO.md` in `travelagentmaneeshind/YEIDA_website` for the
complete map of all of Maneesh's web properties, Vercel projects/domains,
connector status, and known gaps (including a note that the Vercel project
matching this repo's name, `khet-chalo-website`, is a stale duplicate —
the live site runs from project `khet-chalo-website-8aqs`).
