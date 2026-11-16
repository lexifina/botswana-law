# Botswana: law history in git

<picture>
<source media="(prefers-color-scheme: dark)" srcset="data/effort-dark.svg">
<img alt="Botswana law in this repository: what it holds, changes by the year they took effect, completeness against the official sources, and the correctness of what is held" src="data/effort-light.svg" width="880">
</picture>

The law of Botswana as a git history: one file per section, one commit per version on the day it took effect, and the law that made each change as the commit's author. `git blame` names the law behind every paragraph; `git log` lists every change to a section; picking a date gives the text in force that day.

Part of [lexifina/global-law](https://github.com/lexifina/global-law), one git history for every country's law: this is Botswana's national law, which global-law reads at `botswana/national/acts/`.

**What is in it now:** the Penal Code (Cap. 08:01), in one version with 405 sections, as the publisher consolidated it to S.I. 93 of 2023: today's text, in force on 4 December 2024. The Constitution of Botswana, in 2 versions (2019 and 2021), is on the `preview` branch, not on `main` (see below). [`penal-code/README.md`](penal-code/README.md) lists every section of the Penal Code; [`data/versions.json`](data/versions.json) lists every version with its source.

Each act has its own folder, one file per section: `penal-code/s-202.md` is section 202 of the Penal Code, murder.

The text is in English, the language Botswana's laws are published in, as Botswana e-Laws prints it.

## Questions as git commands

| Question | Command |
| --- | --- |
| Every change to section 202 of the Penal Code | `git log -p --word-diff -- penal-code/s-202.md` |
| Which law wrote each line of section 202? | `git blame penal-code/s-202.md` |
| Every version of the Penal Code, with the day each took effect | `git log --format="%h %(trailers:key=In-force,valueonly,separator=) %an" -- penal-code ':!*/README.md'` |
| Section 202 as in force on 1 January 2025 | `python tools/on.py 2025-01-01 penal-code s-202` |

On `preview`, `git log -p --word-diff origin/preview -- constitution/s-068.md` shows what Act 1 of 2021 changed in section 68 of the Constitution.

**Outside git**, we also host this record publicly, for free:

- **[Ask Claude about Botswana law](https://global-law.lexifina.com/v1/try_claude?country=botswana)**: opens Claude with a first question ready.
- **[Ask ChatGPT](https://global-law.lexifina.com/v1/try_chatgpt?country=botswana)**: the same question in ChatGPT.
- **[Search Botswana law on our site](https://lexifina.com/law?country=botswana&q=murder)**: a search for "murder", with each provision's text and its versions, no account needed.
- **[Developer REST API](https://global-law.lexifina.com/v1/search_law?query=murder&jurisdiction=botswana)**: the same search as JSON, with no key. See the [documentation here](https://lexifina.com/api/global-law).

Both assistants read the record through the free Global law connector (MCP, `https://global-law.lexifina.com/mcp`); the first time, the chat gives you the link that adds it. Ask in English.

**Host it yourself easily.** All it takes is git and Python, and the tools run on your machine:

```sh
git clone --depth 1 https://github.com/lexifina/global-law && cd global-law
python3 tools/countries.py add botswana/national/acts
python3 tools/law.py show 2026-01-01 botswana/national/acts/penal-code/s-202.md
```

Opened in Claude Code, Cursor, VS Code or Codex, the clone also starts a local MCP server with the same tools ([MCP.md](https://github.com/lexifina/global-law/blob/main/MCP.md)).

## Dates

Each commit is dated at noon, Africa/Gaborone, on the day the version took effect, and carries it in its `In-force:` trailer:

- for an amending law, the "Date of Commencement" the e-Laws bulletin gives for it (Act 1 of 2021: 5 February 2021); a law that gives no day comes into operation on its publication in the Gazette (Interpretation Act, Cap. 01:04);
- for the oldest version of an act, a consolidation whose own as-at date the publisher does not state, the day the Internet Archive captured it, when it was in force at the latest: 4 December 2024 for the Penal Code (no open source gives the day S.I. 93 of 2023 took effect), 26 May 2019 for the Constitution.

The oldest version of each act is credited to the publisher, `Botswana e-Laws (Attorney General's Chambers, published by Blackhall Publishing)`, and its commit message lists the amendments it already holds. A later change is credited to the law the publisher's own amendment notes name ("[1 of 2021, s. 2(a).]"); a change they do not explain is the publisher's, labelled "unexplained".

## How it is checked

- `tools/check_repo.py` reads every version back from git on the day it took effect and on the day before, and compares it with the corpus: 0 mismatches, and no commit whose trailers git cannot parse (see [`REPRODUCE.md`](REPRODUCE.md)).
- **Today's text:** the Penal Code's amendment list on the publisher's page is the same on 4 December 2024 and 23 March 2026, and the e-Laws bulletin (searched 29 October 2026) lists no later amendment to it.
- **Credits:** each section credited to a law carries an amendment note naming that law, matching the sections the bulletin says it amends (Act 1 of 2021: "Amends: s 68").
- History is append-only: no merge commits, no commit dates that go backwards, and none after the build.
- [vulnerabilities/](vulnerabilities/): possible drafting mistakes in this law, found by global-law's detectors and checked by hand. Not run yet.

## What it does not show

- **The Constitution on `main`.** Act 29 of 2022 changed section 58 (57 to 61 Elected Members) and was commenced by S.I. 93 of 2024, but no open source gives the day: e-Laws says "Date of Commencement: On Notice" and the S.I. is members-only. Rather than guess, the Constitution stays on `preview`, as amended to 2021.
- **Earlier history.** Every change before an act's oldest version is folded into it; its commit message names them (for the Penal Code, Law 2 of 1964 to S.I. 93 of 2023).
- **Other law.** Every other consolidated act on e-Laws is members-only and was not read; there is no subsidiary legislation, case law or bill here.
- **Editorial matter.** Amendment and editorial notes are read for credits only, and Part and Chapter headings are left out; each file starts with its section's number and heading.
- **Changes within a line.** Each paragraph is one line, so blame credits a whole paragraph to the law that changed one word of it.

## Sources

| Source | Kind | Past versions | Notes |
| --- | --- | --- | --- |
| [Botswana e-Laws](https://e-laws.botswanalaws.com) (Attorney General's Chambers; Blackhall Publishing) | Official consolidation | no, today's text only | Only the Constitution's page is open; its bulletin gives each amending law's commencement and the sections it amends |
| [botswanalaws.com](https://botswanalaws.com), the same publisher's earlier site, through the [Internet Archive](https://web.archive.org/) | Official consolidation, archived | as captured: the Constitution on 2019-05-26, the Penal Code on 2024-12-04 and 2026-03-23 | The full text of each act's oldest version |

## Licence

See [`LICENSE`](LICENSE). The publisher's notice reads "Copyright (c) 2026. All right reserved. Government of Botswana."; it gives no licence to republish, and whether Botswana's Copyright and Neighbouring Rights Act excludes legislative texts from copyright has not been verified. Lexifina's own contributions (the arrangement of the history, the commit messages, the tables and the tools) are CC0 1.0.

No AI model wrote, translated or corrected legal text, and none runs when the history is built; the scripts were written by an AI model (see [`REPRODUCE.md`](REPRODUCE.md)).

## Visualisations

- [visualisations/](visualisations/): charts drawn from this repository. Not drawn yet.

## More

From [lexifina/global-law](https://github.com/lexifina/global-law):

- [FEATURES.md](https://github.com/lexifina/global-law/blob/main/FEATURES.md): every feature, and what every corpus must support (`git blame`, `law.py`, the MCP tools)
- [FAQ.md](https://github.com/lexifina/global-law/blob/main/FAQ.md): questions and answers · [CONTRIBUTING.md](https://github.com/lexifina/global-law/blob/main/CONTRIBUTING.md): proposing changes · [MCP.md](https://github.com/lexifina/global-law/blob/main/MCP.md): the MCP server · [REPRODUCE.md](https://github.com/lexifina/global-law/blob/main/REPRODUCE.md): how it was built · [CHANGELOG.md](https://github.com/lexifina/global-law/blob/main/CHANGELOG.md)
- [FRESHNESS.md](https://github.com/lexifina/global-law/blob/main/FRESHNESS.md): how current each corpus is · [Monitoring](https://github.com/lexifina/global-law/tree/main/monitoring): whether updates are running · [WATCHING.md](https://github.com/lexifina/global-law/blob/main/WATCHING.md): how each official source is watched for changes
- [performance/](https://github.com/lexifina/global-law/tree/main/performance): how fast the tools are, measured
- [visualisations/](https://github.com/lexifina/global-law/tree/main/visualisations): charts and bridges across the world's law
- [Vulnerabilities](https://github.com/lexifina/global-law/tree/main/vulnerabilities): mistakes in legislation as published
