# Structure

| Folder | What it holds |
| --- | --- |
| `constitution/` | The Constitution of Botswana |
| `laws/cap-NN.NN-<slug>/` | A consolidated Act with a chapter number in the Laws of Botswana, e.g. `laws/cap-08.01-penal-code/` |
| `acts/<year>/<NNN>-<slug>/` | An Act that has no chapter number yet, by the year and number of the Act, e.g. `acts/2026/021-attorney-general-retiring-age/` |
| `subsidiary/<year>/<NNN>-<slug>/` | Subsidiary legislation, by the year and number of the statutory instrument that made it, e.g. `subsidiary/1999/076-declaration-of-official-uniforms-as-exclusive-order/`; files are its paragraphs, regulations or rules (`s-001.md`), or `text.md` when it has none |

Each act folder holds one file per section (`s-202.md` is section 202; `s-051-a.md` is section 51A; `s-020-to-029.md`
is a range the publisher prints as one repealed block) and per schedule (`schedule-1.md`), and a `README.md` with the
publisher's amendment list and the section headings. No folder holds more than 1,000 entries.

## Dates

Each version is one commit, dated 12:00 Africa/Gaborone on the day it took effect, which its `In-force:` trailer
repeats. `Date-basis:` says where that day comes from:

- `commencement`: the page's own "Date of Commencement" (for subsidiary legislation, the date printed under its title when it has not been amended), used when it is no earlier than the year of the last Act in
  the page's amendment list (the S.I.s after it are its commencement orders);
- `publisher-revision`: the day the Attorney General's Chambers last revised the page on e-Laws. The consolidated text
  was in force that day at the latest; the page does not give the day its last amendment took effect. Such commits
  are credited to the publisher.

No date in this repository is the day we downloaded anything.
