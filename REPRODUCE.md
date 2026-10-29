# How this repository was made (Botswana)

This file is written by the build on 2026-10-29, the day the source data was retrieved.

## Sources

| Source | Address | Retrieved | Licence |
| --- | --- | --- | --- |
| Botswana e-Laws: Constitution of Botswana (open page) | <https://e-laws.botswanalaws.com/constitution-of-botswana/constitution-of-botswana/> | 2026-10-28 | All rights reserved, Government of Botswana (site footer) |
| botswanalaws.com (same publisher's previous site), Internet Archive capture 2019-05-26 | <https://web.archive.org/web/20190526221248id_/http://www.botswanalaws.com:80/principal-legislation/constitution-of-botswana> | 2026-10-28 | All rights reserved, Government of Botswana; read through the Internet Archive |
| botswanalaws.com, Internet Archive capture 2024-12-04 | <https://web.archive.org/web/20241204224821id_/https://botswanalaws.com/consolidated-statutes/principle-legislation/penal-code> | 2026-10-28 | All rights reserved, Government of Botswana; read through the Internet Archive |
| botswanalaws.com, Internet Archive capture 2026-03-23 (Penal Code page, members-only) | <https://web.archive.org/web/20260323141454id_/https://botswanalaws.com/consolidated-statutes/principle-legislation/penal-code> | 2026-10-28 | All rights reserved, Government of Botswana; read through the Internet Archive |
| Botswana e-Laws bulletin (WordPress API excerpts) | <https://e-laws.botswanalaws.com/wp-json/wp/v2/> | 2026-10-29 | All rights reserved, Government of Botswana |

Every word of law in this repository comes from these sources. Lexifina reads them and records each act's dated versions, and the laws that made each change, in one corpus file. This repository is built from that file.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `penal-code` | Penal Code (Cap. 08:01) | 1 | 2024-12-04 to 2024-12-04 |

The build made 1 commits:

| Commits | Kind |
| ---: | --- |
| 1 | first version of an act |
| 0 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `future`: laws not yet in force on 2026-10-29.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 0 laws in the record.
- 1 tags.

## Dates

Each commit is dated at noon (Africa/Gaborone) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: Interpretation Act (Cap. 01:04): an enactment comes into operation on the date of its publication in the Gazette unless it provides otherwise; amending Acts here name their own commencement ("Date of Commencement" in the e-Laws bulletin), which is used as given. https://e-laws.botswanalaws.com/principal-legislation/interpretation/

## How the history is built

`tools/build.py` turns the corpus into this history in one pass: one commit per law, on the day it took effect. The same corpus always gives the same commit hashes. `tools/check_repo.py` reads every version back from git and compares it with the corpus. `tools/on.py` shows the law as it stood on any date. The corpus format is described in `tools/SCHEMA.md`.

- Corpus: sha256 `4123212ef8e236c4b0e990a56478ad3b921ef6ee931f895c974700c6254a141f` (327007 bytes).
- Builder blob hashes (`git hash-object`): `build.py` `a4faa25af85facb64b956b372f6b528aafdd7ec1`, `check.py` `3d00541d258745461ab52b1b0cb4e1716a27a95d`, `on.py` `644a6c0857fbcc72562032b58d57aa113fee0641`.
- Python 3.12.10; git version 2.46.0.windows.1.

## Checks

1 versions of 1 acts read back from git on the day each took effect and on the day before: 0 mismatches. Trailers: 0 commits whose trailers git cannot parse. Health: 0 merge commits on main, 0 commit dates that go backwards, 0 commits dated after the build.

No second build of this corpus has been compared yet.

## Decisions made by hand

- Botswana e-Laws (e-laws.botswanalaws.com) is the official consolidation; only its Constitution page is open. Every other act is members-only and was never read or worked around; earlier full texts come only from Internet Archive captures of the publisher's previous site (botswanalaws.com) in which the members-only tag leaked.
- Text normalisation: hidden <input> notes, tags and footnote markers dropped; NBSP to space; curly quotes to straight; en and em dashes to "-"; runs of spaces collapsed. e-Laws amendment notes ("[1 of 2021, s. 2(a).]") are not text: they are read for credits only. The closing e-Laws editorial note on Act 9 of 2005's word substitutions is not part of any unit.
- Units: one file per section (s-NNN, s-051-a, s-020-to-029 for the repealed range) and per schedule (schedule-N). Chapter and part headings are not units.
- Penal Code: one version, the 2024-12-04 Internet Archive capture, consolidated to S.I. 93 of 2023 (Act 27 of 2021, commenced "On Notice"); dated by the capture day because the commencement date of S.I. 93 of 2023 is in no open source; credited to the publisher as the oldest version available.
- Penal Code is today's text: the 2026-03-23 capture of the same page lists the same amendments (last S.I. 93, 2023), and the e-Laws bulletin search lists no later Penal Code amendment (retrieved 2026-10-29).

## What AI did and did not do

The scripts that read the sources and build this repository were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- Claude Code with Claude Opus 5.5 (claude-opus-5-5) wrote Lexifina's code and chose the sources. No model wrote or altered legal text, and no model runs at build time.
