# How this repository was made (Botswana)

This file is written by the build on 2026-10-29, the day the source data was retrieved. Everything below is enough to rebuild this repository hash for hash.

## Sources

| Source | Address | Retrieved | Requests | Licence |
| --- | --- | --- | ---: | --- |
| Botswana e-Laws: Constitution of Botswana (open page) | <https://e-laws.botswanalaws.com/constitution-of-botswana/constitution-of-botswana/> | 2026-10-28 | 1 | All rights reserved, Government of Botswana (site footer) |
| botswanalaws.com (same publisher's previous site), Internet Archive capture 2019-05-26 | <https://web.archive.org/web/20190526221248id_/http://www.botswanalaws.com:80/principal-legislation/constitution-of-botswana> | 2026-10-28 | 1 | All rights reserved, Government of Botswana; read through the Internet Archive |
| botswanalaws.com, Internet Archive capture 2024-12-04 | <https://web.archive.org/web/20241204224821id_/https://botswanalaws.com/consolidated-statutes/principle-legislation/penal-code> | 2026-10-28 | 1 | All rights reserved, Government of Botswana; read through the Internet Archive |
| botswanalaws.com, Internet Archive capture 2026-03-23 (Penal Code page, members-only) | <https://web.archive.org/web/20260323141454id_/https://botswanalaws.com/consolidated-statutes/principle-legislation/penal-code> | 2026-10-28 | 1 | All rights reserved, Government of Botswana; read through the Internet Archive |
| Botswana e-Laws bulletin (WordPress API excerpts) | <https://e-laws.botswanalaws.com/wp-json/wp/v2/> | 2026-10-29 | 14 | All rights reserved, Government of Botswana |

Every response is cached by the sha256 of its URL, and the table above lists every source with its retrieval date. Lexifina keeps its fetch scripts privately; `tools/parse.py` reads only the cache and writes `corpus.json`, so the same cache always gives the same corpus.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `constitution` | Constitution of Botswana | 2 | 2019-05-26 to 2021-02-05 |
| `penal-code` | Penal Code (Cap. 08:01) | 1 | 2024-12-04 to 2024-12-04 |

The build made 3 commits:

| Commits | Kind |
| ---: | --- |
| 2 | first version of an act |
| 1 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `future`: laws not yet in force on 2026-10-29.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 1 laws in the record.
- 4 tags.

## Dates

Each commit is dated at noon (Africa/Gaborone) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: Interpretation Act (Cap. 01:04): an enactment comes into operation on the date of its publication in the Gazette unless it provides otherwise; amending Acts here name their own commencement ("Date of Commencement" in the e-Laws bulletin), which is used as given. https://e-laws.botswanalaws.com/principal-legislation/interpretation/

## Commands, in order

```sh
# fill the cache from the sources listed above (network; Lexifina's fetch scripts are kept privately)
python -X utf8 tools/parse.py                  # cache -> corpus.json (no network)
python -X utf8 tools/build.py <folder> --repo <empty folder> --docs-date 2026-10-29
python -X utf8 tools/check_repo.py <repo> --corpus <folder>/corpus.json --write
python -X utf8 tools/build.py <folder> --repo <another empty folder> --docs-date 2026-10-29 --compare <repo>
```

In the main Lexifina repository these files live as follows:
- `fetch.py`, `parse.py` and `repo/`: in `scripts/botswana-law/`.
- `build.py`, `check_repo.py` (`check.py` there) and `on.py`: in `scripts/gitlaw_common/`, with the corpus format in `SCHEMA.md`.

## Exact inputs

- `corpus.json` sha256 `dc0d839f5fe79d97c89e7faa95e93edd25189479cb84307415c4440bb383f272` (720901 bytes)
- Script blob hashes (`git hash-object`):

| Script | Blob |
| --- | --- |
| build.py | `2bfc4ac9df193a7be844556d7f69cdb9d93ec3f2` |
| check.py | `cd346c7ff9996d450240e3bab52bcae03b2bc865` |
| on.py | `644a6c0857fbcc72562032b58d57aa113fee0641` |
| fetch.py | `e0fa64b0530bba7dac731f3518d86bf7ccb00e8a` |
| parse.py | `3b936c3948c53b6627e4d825e0ae5828cd87781c` |

- Tools:
  - Python 3.14.0
  - git version 2.52.0.windows.1
  - curl 8.21.0 (Windows) libcurl/8.21.0 Schannel zlib/1.3.2 WinIDN WinLDAP

## Checks

1 versions of 1 acts read back from git on the day each took effect and on the day before: 0 mismatches. Trailers: 0 commits whose trailers git cannot parse. Health: 0 merge commits on main, 0 commit dates that go backwards, 0 commits dated after the build.

A second build from the same corpus into an empty folder gave identical hashes for all 1 history commits and 1 tags (history tip `6c013dce020ae610287922d293968fe991bf4750`).

These results are from the check run on the build before this one, from the same corpus.

## Decisions made by hand

- Botswana e-Laws (e-laws.botswanalaws.com) is the official consolidation; only its Constitution page is open. Every other act is members-only and was never read or worked around; earlier full texts come only from Internet Archive captures of the publisher's previous site (botswanalaws.com) in which the members-only tag leaked.
- Text normalisation: hidden <input> notes, tags and footnote markers dropped; NBSP to space; curly quotes to straight; en and em dashes to "-"; runs of spaces collapsed. e-Laws amendment notes ("[1 of 2021, s. 2(a).]") are not text: they are read for credits only. The closing e-Laws editorial note on Act 9 of 2005's word substitutions is not part of any unit.
- Units: one file per section (s-NNN, s-051-a, s-020-to-029 for the repealed range) and per schedule (schedule-N). Chapter and part headings are not units.
- Constitution v1 (2019-05-26): the 2019-05-26 Internet Archive capture, consolidated to S.I. 57 of 2018. Its own as-at date is not stated, so it is dated by the capture day and credited to the publisher as the oldest version available.
- Constitution v2 (2021-02-05): Act 1 of 2021, "Date of Commencement: 5th February, 2021. Amends: s 68" (e-Laws bulletin). s 68 is taken from today's e-Laws page, whose notes name Act 1 of 2021 for s 68(1) and (5) and no later Act for s 68; every other section stays as in 2019, because the amendment lists show no other change between S.I. 57 of 2018 and Act 1 of 2021.
- Act 29 of 2022 (amends s 58, commenced by S.I. 93 of 2024) is LEFT OUT: its bulletin says "Date of Commencement: On Notice", the S.I. 93 of 2024 page and the 2024 subsidiary-legislation list are members-only, and no other open source gives the day it took effect. So the last version here is not today's text, and this act is not marked verified (no corpus.d/10-constitution.PUBLISH).
- Today's e-Laws page also differs from the 2019 text in editorial ways no note explains (spelling such as "Authorisation", "Re-appointments", cross-reference style such as "(Cap. 01:04)"); those are not built, since they would be unexplained publisher changes on a day the source does not give.
- Penal Code: one version, the 2024-12-04 Internet Archive capture, consolidated to S.I. 93 of 2023 (Act 27 of 2021, commenced "On Notice"); dated by the capture day because the commencement date of S.I. 93 of 2023 is in no open source; credited to the publisher as the oldest version available.
- Penal Code is today's text: the 2026-03-23 capture of the same page lists the same amendments (last S.I. 93, 2023), and the e-Laws bulletin search lists no later Penal Code amendment (retrieved 2026-10-29).

## What AI did and did not do

The fetch, parse and check scripts were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above, through code that anyone can rerun.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- Claude Code with Claude Opus 5.5 (claude-opus-5-5) wrote fetch.py and parse.py and chose the sources. No model wrote or altered legal text, and no model runs at build time.
