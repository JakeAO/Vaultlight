# Copilot Instructions for Vaultlight

These instructions apply to all Copilot-assisted edits in this repository.

## Core Priorities

1. Maintain consistency and cohesiveness across campaign content.
2. Preserve Jekyll site structure and build behavior.
3. Ask follow-up questions whenever requirements are unclear.
4. Keep cross-article links accurate and complete.

## 1) Consistency and Cohesiveness

- Match the established Vaultlight tone: noir, grounded, concise, and evocative.
- Reuse existing structure from `_templates/` for article types (`npc.md`, `location.md`, `session.md`, `faction.md`).
- Keep section ordering and heading styles aligned with existing content in `_world/`, `_sessions/`, `_info/`, and `_gm/`.
- Preserve front matter conventions used by each collection (for example: `layout`, `title`, `topic`, `summary`, and `index` where relevant).
- Keep additions scoped: do not rewrite large unrelated sections when only targeted updates are requested.

## 2) Jekyll Structure and Functionality

- Put new content in the correct source collection directories:
  - Public world content: `_world/...`
  - Public sessions: `_sessions/...`
  - Public rules/info: `_info/...`
  - GM-only content: `_gm/...`
- Do not manually edit generated output in `_site/`; treat it as build artifact only.
- Avoid breaking collection/topic organization used by listing pages (for example grouping by `topic` on `world.md`).
- Do not change permalinks, collection names, or front matter keys unless explicitly requested.
- Prefer internal links that are baseurl-safe, e.g.:
  - `[Gordon Hale]({{ '/world/npcs/gordon-hale/' | relative_url }})`

## 3) Clarifying Questions Are Required

Before making changes, ask concise follow-up questions if any ambiguity remains. Do **not** guess on unresolved details that affect structure, canon, or content.

Ask follow-ups when any of these are missing or unclear:
- Target article type or destination folder
- Canon facts (names, roles, timelines, relationships, revelations)
- Public vs GM visibility
- Desired scope (new article vs update existing article)
- Link targets when multiple entities could match

If ambiguity is minor and safe to proceed, state assumptions explicitly and keep them minimal.

## 4) Cross-Linking Standards

- When an article mentions another established entity (NPC, location, faction, session), link the first meaningful mention.
- Use canonical internal URLs that match generated site paths.
- When adding a new entity, check whether related articles should be updated with reciprocal references.
- Avoid over-linking repeated mentions in the same section.
- Ensure link text is the in-world name readers recognize.
- NEVER link to a GM-only article, whether from public content or other GM content.

Examples:
- Location mentioning NPC: `[Gordon Hale]({{ '/world/npcs/gordon-hale/' | relative_url }})`
- NPC mentioning location: `[Montrose Hotel]({{ '/world/locations/montrose-hotel/' | relative_url }})`

## 5) Quality Checklist Before Finishing

- Front matter is valid and complete for the article type.
- Markdown headings and section order match repository conventions.
- Internal links resolve to valid in-repo content paths.
- Changes are limited to requested scope and do not alter unrelated files.
- If prompt details were unclear, follow-up questions were asked before implementation.