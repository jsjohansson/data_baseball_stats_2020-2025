# Dataset metadata

| | |
| --- | --- |
| Title | MLB Data, 2020-2025 |
| Version | 1.0.0 |
| Created | 2026-09-25 |
| Source | [Baseball-Reference.com](https://www.baseball-reference.com/) (Sports Reference LLC) |
| Temporal coverage | 2020-2025 regular seasons and postseasons, plus a current 40-man snapshot marked 2026 |
| Entities | All 30 Major League Baseball clubs, both leagues, all six divisions |
| Datasets | 108 |
| Rows | 769,168 |
| Documented fields | 3,756 |
| Primary format | CSV, UTF-8 with BOM |
| Machine-readable descriptor | [`1_Source_Data_CSV/datapackage.json`](1_Source_Data_CSV/datapackage.json) |
| Field documentation | [`1_Source_Data_CSV/FIELD_REFERENCE.md`](1_Source_Data_CSV/FIELD_REFERENCE.md) |
| Join guidance | [`JOIN_DIAGRAM.svg`](JOIN_DIAGRAM.svg) and [`JOIN_DIAGRAM_Detailed.svg`](JOIN_DIAGRAM_Detailed.svg) |

## Contents

| Category | Datasets | Rows |
| --- | ---: | ---: |
| Regular season | 12 | 73,806 |
| Playoffs | 8 | 9,736 |
| Advanced & league | 86 | 192,326 |
| Game level | 2 | 493,300 |
| **Total** | **108** | **769,168** |

## Distributions

| Form | Location |
| --- | --- |
| Source CSV (canonical) | `1_Source_Data_CSV/` |
| Excel workbooks | `2_Data_Workbooks/` |

Folder 2 is derived from folder 1 and contains no data that is not in it.

## Join keys

Every dataset carries its own identifiers; there are no lookup tables.

| Field | Type | Present in | Role |
| --- | --- | --- | --- |
| `Season` | integer | 108 of 108 | Season year |
| `Team` | text | 107 of 108 | Franchise code; `2TM`/`3TM` on league-wide tables |
| `Player_ID` | text | 67 of 108 | Stable person key |
| `Position` | text | 24 of 108 | Fielding position; value sets differ between tables |
| `Gm#` / `Game_Num` | integer | 4 of 108 | Team game number, 1-163; named `Gm#` on the schedule and `Game_Num` on the lineup tables |
| `Boxscore_URL` | text | `Schedule_Results` | Identifies a game; 44,632 distinct, two rows each |
| `Row_Type` | text | 102 of 108 | `data` or `summary`; filter to `data` before aggregating |

Full guidance, including the field-name traps and exact predicates, is in
[`JOIN_DIAGRAM_Detailed.svg`](JOIN_DIAGRAM_Detailed.svg) and the
[source-data README](1_Source_Data_CSV/README.md#joining-the-data).

## Provenance

Pages were fetched at a 3+ second crawl delay, honouring the `Crawl-delay: 3` directive
in the site's `robots.txt`; only `/teams/`, `/leagues/` and `/awards/` paths were requested,
none of which robots.txt disallows. Tables the site embeds inside HTML comments - fielding,
value, coaches, roster and most advanced tables - were extracted along with the visible ones.
Columns are keyed to Baseball-Reference's own `data-stat` codes, so the extraction is resilient
to display changes, and those codes are preserved in the data dictionary so any column can be
traced back to its source. Accented names are stored as proper UTF-8.

### Validation performed

- Game-level batting orders reconciled against the schedule independently for all six seasons.
- Known results checked against the data: MVP winners, World Series outcomes, season leaders.
- Every Excel sheet verified row-for-row and column-for-column against its CSV.
- All 3,756 columns confirmed to carry a definition.
- Full sweep for character-encoding corruption in accented names; zero found.

## Known limitations

- 2020 was a 60-game COVID-shortened season; compare rates rather than counting stats.
- The Athletics use franchise code `OAK` for 2020-2024 and `ATH` from 2025; same franchise.
- `Current_40_Man_Roster` is a live snapshot marked Season 2026, not a historical series.
- Player splits are disallowed by the site's robots.txt and were not collected.
- Statcast metrics are not published by Baseball-Reference and are not included.
- `regular_season` files are team-scoped; `advanced` files are league-wide with 2TM/3TM rows.
  Do not union the two.
- Rows where `Row_Type` is `summary` are table footers such as Team Totals, not players.

## Rights and citation

Data is sourced from Baseball-Reference.com, a Sports Reference LLC property, and
remains their copyright. **No open licence is granted or implied here.** When sharing this
dataset or anything derived from it, credit **Baseball-Reference.com** as the source, and
consult Sports Reference about commercial use or redistribution.

> Baseball-Reference.com, Sports Reference LLC. MLB season data, 2020-2025. Retrieved 2026-09-25.
