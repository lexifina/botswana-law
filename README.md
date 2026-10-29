# Botswana: law history in git

The law of Botswana as a git history: one file per section, one commit per law on the day it took effect, and the law that made each change as the commit's author. `git blame` names the law behind every paragraph; `git log` lists every change to a section; `tools/on.py` gives the text in force on any day.

It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law), which places it at `bw/`. The text is the official consolidation published for the Attorney General's Chambers by Blackhall Publishing as [Botswana e-Laws](https://e-laws.botswanalaws.com), read from its one open page and from archived copies of the same publisher's earlier site.

**What is in it**

| Folder | Act | Versions | History | On `main` |
| --- | --- | ---: | --- | --- |
| `penal-code/` | Penal Code (Cap. 08:01) | 1 | 2024-12-04 | yes: today's text |
| `constitution/` | Constitution of Botswana | 2 | 2019-05-26 to 2021-02-05 | no: held on the `preview` branch (see below) |

- **Penal Code.** One version: the consolidated text to S.I. 93 of 2023, as the publisher's site showed it on 4 December 2024. The same page's amendment list on 23 March 2026 is unchanged, and the e-Laws bulletin lists no later amendment, so it is today's text. Its history before 2024 is not open anywhere, so the first commit is the "oldest version available".
- **Constitution.** The text to S.I. 57 of 2018 (captured 26 May 2019), then Act 1 of 2021 (section 68, in force 5 February 2021). Act 29 of 2022 changed section 58 (57 to 61 Elected Members), commenced by S.I. 93 of 2024, but no open source gives the day it took effect: e-Laws says "Date of Commencement: On Notice" and the S.I. itself is members-only. That change is left out rather than guessed, so the Constitution here is not today's text and is not on `main`.

Each folder's `README.md` lists every section, how often it changed and when.

## A lawyer's questions as git commands

| Question | Command |
| --- | --- |
| What did s 3 say on 2025-01-01? | `python tools/on.py 2025-01-01 penal-code s-003` |
| The same, with raw git (bash) | `git show $(git rev-list -1 --before="2025-01-01T23:59:59Z" main -- penal-code/s-003.md):penal-code/s-003.md` |
| The same, in PowerShell | `$r = git rev-list -1 --before="2025-01-01T23:59:59Z" main -- penal-code/s-003.md; git show "$($r):penal-code/s-003.md"` |
| Which law wrote each line? | `git blame constitution/s-068.md` |
| Every change, word by word | `git log -p --word-diff constitution/s-068.md` |
| Every law in the record, in order | `git log --reverse --format="%ad %an" --date=short main` |
| Everything one law changed | `git show law/<key>` (tags `law/<key>` mark each law's commit) |
| The whole act on a date | `python tools/on.py 2025-01-01 penal-code` |

After a rebuild, refresh tags with `git fetch --force --tags`: a plain fetch keeps stale tags.

## Dates

- Each commit is dated at **noon, Africa/Gaborone, on the day the change took effect**. The day is also in the `In-force:` trailer, which the tools read.
- **Amending Acts** are dated by the "Date of Commencement" the e-Laws bulletin gives for them (Act 1 of 2021: 5 February 2021).
- **The oldest version of each act** is a consolidation whose own as-at date the publisher does not state. It is dated by the day the Internet Archive captured it: the text was in force on that day at the latest.
- `--before="YYYY-MM-DD"` alone uses your clock's time of day, so a law that took effect that day may be missed before noon. Use `T23:59:59Z` as above, or the tool.

## How it is checked

- Every version is read back from git on the day it took effect and on the day before (`tools/check_repo.py`); both must match `corpus.json`. Results are in `REPRODUCE.md`.
- **Today's text:** the Penal Code's amendment list on the publisher's page is the same on 2024-12-04 and 2026-03-23, and the e-Laws bulletin (searched 2026-10-29) lists no later Penal Code amendment.
- **Credits:** each section credited to Act 1 of 2021 is one whose e-Laws amendment note names that Act ("[1 of 2021, s. 2(a).]"), matching the bulletin's "Amends: s 68".
- The repository is rebuilt from the same data a second time and must give identical hashes.

## What "author" means

The author of a commit is the law that made the change, with an e-mail address that cannot exist, so `git blame` and `git log --author` name laws. The committer is always Lexifina.

- **Credits come only from the publisher's own amendment notes and bulletin.** Anything they do not explain is committed by the publisher and labelled "unexplained".
- **The first commit** of each act is the oldest version available (a consolidation), credited to the publisher.
- Blame credits whole lines (one paragraph per line). Use `git log -p --word-diff` to see exactly which words each change made.

## What it does not show

- **Earlier history.** Every change before the oldest version is folded into it. The amendment list printed in that version's commit message names them (for the Constitution: L.N. 83 of 1966 to S.I. 57 of 2018; for the Penal Code: Law 2 of 1964 to S.I. 93 of 2023).
- **Act 29 of 2022** (Constitution, s 58): no open source gives its in-force day, so it is not in the history.
- **The publisher's later editorial changes.** Today's e-Laws Constitution differs from the 2019 text in spelling ("authorise" for "authorize"), hyphenation and cross-reference style in about 30 sections. No note explains when; they are not built.
- **Editorial notes** (amendment notes, the closing editorial note on Act 9 of 2005's word substitutions) are not text: they are read for credits only. Chapter and Part headings are left out; each file starts with its own number and heading.
- **Other acts.** Every other consolidated act on e-Laws is members-only. It was not read, and nothing here works round that.

## How it is built

Lexifina reads the sources listed here and records each act's dated versions, and the laws that made each change, in one corpus file. `tools/build.py` writes this repository from that file, and the same corpus always gives the same commit hashes; `REPRODUCE.md` gives the details and the checks. A model (Claude) wrote Lexifina's code; it wrote no legal text, and no model runs when the history is built.

## Sources

| Source | What it gives | Used for |
| --- | --- | --- |
| [Botswana e-Laws](https://e-laws.botswanalaws.com) (Attorney General's Chambers; Blackhall Publishing) | The consolidated Constitution to S.I. 93 of 2024, with amendment notes; bulletin excerpts with commencement dates. Every other act is members-only | Section 68 as amended in 2021; credits; dates |
| [botswanalaws.com](https://botswanalaws.com) (the same publisher's earlier site), through the [Internet Archive](https://web.archive.org/) | Full consolidated texts in captures where the members-only tag leaked: the Constitution (2019-05-26), the Penal Code (2024-12-04) | The oldest version of each act |
| [elaws.gov.bw](https://www.elaws.gov.bw) (the Attorney General's earlier e-Laws) | Does not connect; archived captures hold the Constitution only as one chapter export | Not used |
| [BotswanaLII](https://www.botswanalii.org) | – | Not used |
| [Parliament of Botswana](https://www.parliament.gov.bw) | Hansard, order papers and Bills; no Acts | Not used |

Research guides that cover every country: [GlobaLex](https://www.nyulawglobal.org/globalex/) and the [Law Library of Congress Guide to Law Online](https://www.loc.gov/research-centers/law-library-of-congress/researcher-resources/guide-to-law-online/).

## Licence

See [LICENSE](LICENSE). The publisher states: "Copyright © 2026. All right reserved. Government of Botswana." Whether Botswana's Copyright and Neighbouring Rights Act excludes legislative texts from copyright has not been verified, so this repository is private. Lexifina's arrangement, messages, tables and tools are CC0.

This repository is not legal advice. Botswana's laws are published in English, so there is no separate summary in Setswana.
