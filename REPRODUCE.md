# How this repository was made (Botswana)

## Sources

| Source | Address | Licence |
| --- | --- | --- |
| Botswana e-Laws (Attorney General's Chambers) | <https://elaws.gov.bw>, read through its public WordPress REST interface (`/wp-json/wp/v2/posts`, categories Constitution of Botswana and Principal Legislation) | Official legislative texts, outside copyright (Cap. 68:02, s 6(2)(b)); site footer "All rights reserved" |
| botswanalaws.com, Internet Archive captures | the Constitution 2019-05-26, the Penal Code 2024-12-04 | as above |

Requests go one at a time, about 1.2 seconds apart, and back off on 429 or 503. No login, challenge or block was
worked around. BotswanaLII (www.botswanalii.org) answers with a Cloudflare challenge and is not used.

## Build

The runner (Lexifina's `scripts/botswana-law/runner/`):

1. `bw_fetch.py posts` caches every e-Laws post (`content.rendered`, `date`, `modified`) by its id.
2. `bw_parse.py` splits each Blackhall-typeset page at its section anchors (`<a name="...sN">` in `p.Level-Iblue`)
   and its schedule headings into one text per section or schedule, normalising quotes, dashes and spaces; amendment
   notes are left out.
3. `bw_build.py` dates each page (see [`STRUCTURE.md`](STRUCTURE.md)), writes the act's folder and README, and
   appends one commit per new version to `main` with `git fast-import`, oldest day first; it pushes fast-forward only
   and checks the pushed head with `git ls-remote`.

A page whose sections carry no marks the parser knows is held back and listed in the runner's state, not guessed.

## Correction

Commit 9776ffa (a README and licence update, 2026-11-26) was made from a stale index and deleted the Constitution and every consolidated Act by mistake. The commits after eb26cba re-add them, one commit per version with the same dates, authors and text as before (the tree for constitution/ and laws/ is identical to d869d2a). The Penal Code's 2024 version is filed once more by the rename commit 3d5e58c's predecessor.
