# MLB Data, 2020-2025 - complete reference

Major League Baseball data for **all 30 clubs across the 2020-2025 seasons**, scraped from
[Baseball-Reference](https://www.baseball-reference.com/) and normalised into one tidy table
per statistical category.

**6 seasons · 108 datasets · 769,168 rows · 3,756 documented columns.** Built 2026-09-25.

## What is in this document

This is the complete reference for the dataset: the three separate READMEs merged into one,
with nothing removed. If you prefer them apart, they are still in place at
`README.md`, `1_Source_Data_CSV/README.md` and `2_Excel_Workbooks/README.md`.

| Part | Covers |
| --- | --- |
| [Part 1 - Overview](#part-1---overview) | What the dataset is, how it is laid out, which form to use |
| [Part 2 - Source data (CSV)](#part-2---source-data-csv) | File inventory, common fields, joining, the full field glossary, caveats, method |
| [Part 3 - Excel workbooks](#part-3---excel-workbooks) | The workbooks sheet by sheet, how they are built, working in Excel, size limits |

Two further references sit alongside this document: the complete per-column field references
in [`1_Source_Data_CSV/FIELD_REFERENCE.md`](1_Source_Data_CSV/FIELD_REFERENCE.md) and
[`2_Excel_Workbooks/FIELD_REFERENCE.md`](2_Excel_Workbooks/FIELD_REFERENCE.md), and the join
maps [`JOIN_DIAGRAM.svg`](JOIN_DIAGRAM.svg) and
[`JOIN_DIAGRAM_Detailed.svg`](JOIN_DIAGRAM_Detailed.svg).


---

## Part 1 - Overview

Major League Baseball data for **all 30 clubs across the 2020-2025 seasons**, scraped from
[Baseball-Reference](https://www.baseball-reference.com/) and normalised into one tidy table
per statistical category.

**6 seasons · 108 datasets · 769,168 rows · 3,756 documented columns.** Built 2026-09-25.

### The two folders

| Folder | What it holds | Start here if... |
| --- | --- | --- |
| [`1_Source_Data_CSV/`](1_Source_Data_CSV/) | The dataset itself: 108 CSVs across four categories, plus the field reference and a Frictionless data package | ...you are loading into Tableau, Python, R or a database, or publishing the data |
| [`2_Excel_Workbooks/`](2_Excel_Workbooks/) | The same data compiled into 5 Excel workbooks | ...you work in Excel |

[`JOIN_DIAGRAM.svg`](JOIN_DIAGRAM.svg) shows how the tables join together - the keys, the five grains, a worked example and the traps. [`JOIN_DIAGRAM_Detailed.svg`](JOIN_DIAGRAM_Detailed.svg) is the table-by-table version, with key fields, cardinality and exact join predicates.

Each folder has its own README covering its contents in detail. Nothing is duplicated
between them in substance: **folder 2 is built from folder 1**, which is the canonical form.

### Which should I use?

**To publish or share the data** - `1_Source_Data_CSV/`. Open format, readable by anything,
diffable, and `datapackage.json` describes every file with schemas and SHA-256 checksums.

**To read or edit by hand** - `2_Excel_Workbooks/`.

Every table carries `Season`, `Team`, `League` and `Division`, and `Player_ID` is a stable key
across all of them, so building a model on top of this is straightforward if you need one.

### What is in the data

| Category | Datasets | Rows |
| --- | ---: | ---: |
| Regular season | 12 | 73,806 |
| Playoffs | 8 | 9,736 |
| Advanced & league | 86 | 192,326 |
| Game level | 2 | 493,300 |
| **Total** | **108** | **769,168** |

Standard and advanced batting, pitching and fielding; WAR components; standings; schedules and
results; rosters, coaching staffs and transactions; award voting; and game-level batting orders
and defensive lineups.

---

## Part 2 - Source data (CSV)

Everything below describes the CSV files in `1_Source_Data_CSV/`, which are the canonical form of the dataset.

The complete dataset as scraped from [Baseball-Reference](https://www.baseball-reference.com/):
**108 datasets, 769,168 rows, 3,756 documented columns**, covering all 30 MLB clubs across
the 2020-2025 seasons. One tidy table per statistical category, every row carrying its own
season, team, league and division.

`1_Source_Data_CSV/` is the canonical form of the data. The Excel workbooks in `../2_Excel_Workbooks/`
are built from these files.

Encoding is UTF-8 with BOM, so Excel opens them correctly and accented names render properly.
Each subfolder carries its own `Data_Dictionary.csv` defining every column in it.

| Reference | What it is |
| --- | --- |
| [`FIELD_REFERENCE.md`](1_Source_Data_CSV/FIELD_REFERENCE.md) | Every column of every dataset, with its Baseball-Reference stat code and definition |
| [`datapackage.json`](1_Source_Data_CSV/datapackage.json) | Frictionless descriptor: schemas, row counts and SHA-256 checksums for every file |
| `<folder>/Data_Dictionary.csv` | The same definitions as data, per folder |
| [`../JOIN_DIAGRAM.svg`](JOIN_DIAGRAM.svg) | How the tables join together: the keys, the five grains, a worked example and the traps |
| [`../JOIN_DIAGRAM_Detailed.svg`](JOIN_DIAGRAM_Detailed.svg) | The same, table by table: named tables, key fields, cardinality and exact join predicates |

### Files

#### `regular_season/`

Player and team data as Baseball-Reference presents it on each club's season page.

| File | Rows | Columns |
| --- | ---: | ---: |
| `Coaching_Staff.csv` | 2,359 | 16 |
| `Current_40_Man_Roster.csv` | 1,367 | 23 |
| `Full_Season_Roster.csv` | 9,706 | 37 |
| `Schedule_Results.csv` | 26,092 | 32 |
| `Standard_Batting.csv` | 5,797 | 43 |
| `Standard_Fielding.csv` | 10,332 | 38 |
| `Standard_Pitching.csv` | 5,908 | 46 |
| `Standings.csv` | 180 | 12 |
| `Standings_Expanded.csv` | 180 | 32 |
| `Team_Season_Summary.csv` | 180 | 27 |
| `Value_Batting.csv` | 5,797 | 31 |
| `Value_Pitching.csv` | 5,908 | 33 |

#### `playoffs/`

Postseason equivalents. Clubs that missed the postseason have no rows.

| File | Rows | Columns |
| --- | ---: | ---: |
| `Postseason_Advanced_Batting.csv` | 1,840 | 27 |
| `Postseason_Advanced_Pitching.csv` | 862 | 31 |
| `Postseason_Batting.csv` | 1,908 | 38 |
| `Postseason_Fielding.csv` | 1,772 | 30 |
| `Postseason_Pitching.csv` | 930 | 43 |
| `Postseason_Roster.csv` | 1,834 | 37 |
| `Postseason_Schedule_Results.csv` | 522 | 27 |
| `Postseason_Series_Results.csv` | 68 | 13 |

#### `advanced/`

Advanced and situational splits plus team- and league-level aggregates, sourced from league pages so they cover every player in the majors.

| File | Rows | Columns |
| --- | ---: | ---: |
| `Advanced_Batting.csv` | 6,062 | 39 |
| `Advanced_Fielding_1B.csv` | 1,161 | 47 |
| `Advanced_Fielding_2B.csv` | 1,144 | 46 |
| `Advanced_Fielding_3B.csv` | 1,139 | 44 |
| `Advanced_Fielding_C.csv` | 712 | 42 |
| `Advanced_Fielding_CF.csv` | 1,106 | 52 |
| `Advanced_Fielding_C_Baserunning.csv` | 712 | 33 |
| `Advanced_Fielding_LF.csv` | 1,562 | 52 |
| `Advanced_Fielding_P.csv` | 5,734 | 37 |
| `Advanced_Fielding_RF.csv` | 1,452 | 52 |
| `Advanced_Fielding_SS.csv` | 827 | 47 |
| `Advanced_Pitching.csv` | 6,341 | 33 |
| `Awards_And_Honors.csv` | 23 | 12 |
| `Baserunning_Batting.csv` | 5,217 | 46 |
| `Basesituation_Pitching.csv` | 6,369 | 47 |
| `Batting_Pitching.csv` | 6,405 | 40 |
| `Cumulative_Batting.csv` | 9,483 | 38 |
| `Cumulative_Pitching.csv` | 5,809 | 43 |
| `Cy_Young_Voting.csv` | 128 | 40 |
| `Debuts_Batting.csv` | 1,545 | 35 |
| `Debuts_Bio.csv` | 1,539 | 27 |
| `Debuts_Pitching.csv` | 983 | 41 |
| `Free_Agent_Batting.csv` | 256 | 32 |
| `Free_Agent_Pitching.csv` | 444 | 36 |
| `Free_Agent_Signings.csv` | 2,457 | 41 |
| `MVP_Voting.csv` | 266 | 40 |
| `Manager_Of_The_Year_Voting.csv` | 81 | 21 |
| `Manager_Record.csv` | 201 | 25 |
| `Manager_Tendencies.csv` | 201 | 36 |
| `Neutral_Batting.csv` | 4,303 | 32 |
| `Neutral_Pitching.csv` | 5,101 | 33 |
| `Opening_Day_Lineups.csv` | 180 | 21 |
| `Pitches_Batting.csv` | 5,190 | 43 |
| `Pitches_Pitching.csv` | 6,369 | 44 |
| `Playoff_Odds.csv` | 216 | 33 |
| `Playoff_Scenarios.csv` | 12 | 17 |
| `Ratio_Batting.csv` | 5,190 | 30 |
| `Ratio_Pitching.csv` | 6,405 | 32 |
| `Reliever_Pitching.csv` | 5,284 | 45 |
| `Rookie_Of_The_Year_Voting.csv` | 105 | 40 |
| `Rookies_Batting.csv` | 1,337 | 36 |
| `Rookies_Pitching.csv` | 885 | 42 |
| `Sabermetric_Batting.csv` | 6,174 | 37 |
| `Situational_Batting.csv` | 5,190 | 52 |
| `Standard_Fielding_By_Position.csv` | 18,324 | 53 |
| `Starter_Pitching.csv` | 2,508 | 47 |
| `Team_Advanced_Batting.csv` | 192 | 31 |
| `Team_Advanced_Fielding_1B.csv` | 192 | 43 |
| `Team_Advanced_Fielding_2B.csv` | 192 | 42 |
| `Team_Advanced_Fielding_3B.csv` | 192 | 40 |
| `Team_Advanced_Fielding_C.csv` | 192 | 38 |
| `Team_Advanced_Fielding_CF.csv` | 192 | 48 |
| `Team_Advanced_Fielding_C_Baserunning.csv` | 192 | 29 |
| `Team_Advanced_Fielding_LF.csv` | 192 | 48 |
| `Team_Advanced_Fielding_P.csv` | 192 | 33 |
| `Team_Advanced_Fielding_RF.csv` | 192 | 48 |
| `Team_Advanced_Fielding_SS.csv` | 192 | 43 |
| `Team_Advanced_Pitching.csv` | 192 | 26 |
| `Team_Appearances.csv` | 180 | 27 |
| `Team_Attendance.csv` | 186 | 15 |
| `Team_Baserunning_Batting.csv` | 192 | 41 |
| `Team_Basesituation_Pitching.csv` | 192 | 42 |
| `Team_Batting_Pitching.csv` | 192 | 35 |
| `Team_Fielding_By_Position.csv` | 1,920 | 48 |
| `Team_Miscellaneous.csv` | 180 | 26 |
| `Team_Pitches_Batting.csv` | 192 | 39 |
| `Team_Pitches_Pitching.csv` | 192 | 39 |
| `Team_Pitching_Staffs.csv` | 180 | 20 |
| `Team_Ratio_Batting.csv` | 192 | 25 |
| `Team_Ratio_Pitching.csv` | 192 | 27 |
| `Team_Reliever_Pitching.csv` | 192 | 39 |
| `Team_Sabermetric_Batting.csv` | 192 | 31 |
| `Team_Situational_Batting.csv` | 192 | 47 |
| `Team_Standard_Batting.csv` | 192 | 37 |
| `Team_Standard_Fielding.csv` | 192 | 27 |
| `Team_Standard_Pitching.csv` | 192 | 44 |
| `Team_Starter_Pitching.csv` | 192 | 41 |
| `Team_Starting_Lineups.csv` | 180 | 20 |
| `Team_Value_Batting.csv` | 186 | 27 |
| `Team_Value_Pitching.csv` | 186 | 29 |
| `Team_Win_Probability_Batting.csv` | 192 | 30 |
| `Team_Win_Probability_Pitching.csv` | 192 | 31 |
| `Transactions.csv` | 20,428 | 8 |
| `Uniform_Numbers.csv` | 9,602 | 9 |
| `Win_Probability_Batting.csv` | 5,185 | 35 |
| `Win_Probability_Pitching.csv` | 6,405 | 36 |

#### `game_level/`

Every batting order and defensive alignment, one row per player per game.

| File | Rows | Columns |
| --- | ---: | ---: |
| `Batting_Orders.csv` | 234,828 | 18 |
| `Defensive_Lineups.csv` | 258,472 | 17 |


### Common fields

These appear on nearly every dataset, so any file can be filtered, joined or stacked the same way.

| Field | Meaning |
| --- | --- |
| `Season` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | Baseball-Reference franchise code, e.g. `NYY`. `2TM`/`3TM` marks a combined line for a player who changed clubs mid-season. |
| `Team_Name` | Full club name as of that season. |
| `League` / `League_Name` | `AL` / `NL`, and American League / National League. |
| `Division` / `Division_Full` | `East`, `Central`, `West`, and e.g. `AL East`. |
| `Position` | Fielding position the row covers (per-position fielding datasets only). |
| `Row_Type` | `data` for player rows, `summary` for footer rows such as Team Totals. |
| `Player_ID` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Bats` / `Throws` | Handedness (L/R/S), split out of the player name. |

#### Four things to understand before you analyse

**1. Filter `Row_Type = 'data'` for player-level work.** Baseball-Reference's player
tables end with footer rows - *Team Totals*, *Non-Pitcher Totals*, *Rank in 2 AL*. They are
preserved because they are useful, but flagged. Left in, they are counted alongside the very
players who make them up.

**2. Join on `Player_ID`, never on name.** `Player_ID` (e.g. `judgeaa01`) is stable across
seasons and datasets. Names are not unique and change spelling. On `Coaching_Staff` the field
holds the coach's or manager's id.

**3. Player names are clean.** Baseball-Reference renders names with a handedness marker
appended - `Shohei Ohtani*` for a left-handed bat, `#` for a switch hitter - which silently
breaks any filter or join on name. Those markers are stripped from the name and moved into an
explicit `Bats` or `Throws` column.

**4. Team-scoped and league-wide files count traded players differently.** The
`regular_season` files are **team-scoped**: a player traded mid-season appears once for each
club. The `advanced` files come from league pages and are **league-wide**: that player appears
once, with `Team` set to `2TM` or `3TM`. Both are correct - but do not union them, or traded
players are counted twice.

### Joining the data

There are no lookup tables. Every dataset carries its own identifiers, so tables are joined
directly on natural keys. [`../JOIN_DIAGRAM_Detailed.svg`](JOIN_DIAGRAM_Detailed.svg) draws
this table by table; what follows is the same information as text.

#### The join keys, exactly

| Field | Type | Example | Present in | Notes |
| --- | --- | --- | --- | --- |
| `Season` | integer | `2007` | all 108 datasets | Always an integer, never text. |
| `Team` | text | `BOS`, `FLA` | 107 of 108 | Baseball-Reference franchise code, 2-3 characters. Can be `2TM`/`3TM` on league-wide tables. |
| `Player_ID` | text | `ortizda01` | 67 of 108 | Stable Baseball-Reference id. The only safe person key. |
| `Position` | text | `C`, `1B`, `LF` | 24 of 108 | Value sets differ between tables - see below. |
| `Gm#` | integer | `1` to `163` | `Schedule_Results` only | Team game number. 163 occurs: makeup and tie-break games. |
| `Game_Num` | integer | `1` to `163` | `Batting_Orders`, `Defensive_Lineups` | The same concept as `Gm#`, spelled differently. |
| `Boxscore_URL` | text | `.../BOS200704020.shtml` | `Schedule_Results` only | Identifies the game itself. 44,632 distinct values, each appearing on two rows. |
| `Row_Type` | text | `data` / `summary` | 102 of 108 | Filter to `data` before joining or totalling. |

#### The predicates

```sql
-- any player table to any team table
ON a.Season = b.Season AND a.Team = b.Team

-- player table to player table (Standard + Value + Advanced)
ON a.Season = b.Season AND a.Team = b.Team AND a.Player_ID = b.Player_ID

-- lineups to schedule: note the two different column names
ON a.Season = b.Season AND a.Team = b.Team AND a.Game_Num = b."Gm#"

-- both clubs in the same game
ON a.Boxscore_URL = b.Boxscore_URL AND a.Team <> b.Team
```

#### Field-name traps

These are the differences that produce a silently wrong answer rather than an error.

- **`Gm#` versus `Game_Num`.** `Schedule_Results` names the game number `Gm#`; the two lineup
  tables name it `Game_Num`. Same meaning. The `#` needs quoting in SQL.
- **`Position` values differ by table.** `Standard_Fielding_By_Position` uses `OF` and has no
  `DH`; `Defensive_Lineups` uses `DH` and has no `OF`. An inner join on `Position` between the
  two drops both silently.
- **`Player` versus `Name`.** Team-page tables call the name column `Player`; league-page
  tables call it `Name`. In `Batting_Orders` and `Defensive_Lineups`, `Player` holds a
  **surname only** (`Ortiz`). Join on `Player_ID`, never on a name.
- **`Pos` is not `Position`.** On batting and pitching tables, `Pos` is a Baseball-Reference
  code string such as `*D/3`. It is not a position key; only `Position` is joinable.
- **`Team` versus `Tm`.** Some tables carry both. `Team` is the clean franchise code and is
  what the identifiers are built on; `Tm` is whatever the source table printed.

#### Grain, and why joins multiply rows

| Grain | Datasets | Join safely to |
| --- | ---: | --- |
| Team x season | 39 | anything, on `Season` + `Team` - always the "one" side |
| Player x team x season | 54 | each other 1:1, and up to team x season |
| Player x team x season x position | 24 | player tables, **after aggregating** |
| Team x game / player x game | 4 | the schedule, and up to player x season |

Fielding is one row per player **per position**. Joined to a batting table without aggregating
first, it multiplies that player's batting line by the number of positions he appeared at. Sum
the fielding to the player, or filter to a single `Position`, before joining.


### Glossary

Every distinct field across the dataset, grouped by what it measures. Definitions are
Baseball-Reference's own. For the per-dataset breakdown see
[`FIELD_REFERENCE.md`](1_Source_Data_CSV/FIELD_REFERENCE.md).

#### Identifiers and derived fields

70 fields.

| Field | Source code | Meaning |
| --- | --- | --- |
| `Attendance` | `attendance` | Attendance - Typically, tickets sold in home games. |
| `Award` | `award_title` | Name of the award or honour. |
| `Ballpark` | `identifier/derived` | Home ballpark. |
| `Bats` | `derived` | Batting hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Batting_Order_Slot` | `parsed` | Spot in the batting order, 1 through 9. |
| `Current_Attendance` | `parsed` | Total home attendance this season. |
| `Current_Attendance_Per_Game` | `parsed` | Average home attendance this season. |
| `Current_Home_Games` | `parsed` | Home dates played in this season. |
| `Date` | `date_game` | A number in parentheses indicates which game of a doubleheader. - Click dates for box scores of games or standings on this day. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Finish` | `identifier/derived` | Finishing position within the division. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Doubleheader_Game` | `identifier/derived` | Game 1 or 2 of a doubleheader; blank for single games. |
| `Farm_Director` | `identifier/derived` | Director of player development. |
| `Game_Date` | `identifier/derived` | ISO (YYYY-MM-DD) game date derived from the display Date column. |
| `Game_Num` | `parsed` | Team game number within the season. |
| `General_Manager` | `identifier/derived` | General manager. |
| `Home_Away` | `identifier/derived` | Whether the team was Home or Away, derived from Baseball-Reference's '@' marker. |
| `L` | `ppr_cur_l` | Current Losses |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Loser_Wins` | `identifier/derived` | Games won by the losing club. |
| `Losing_Team` | `identifier/derived` | Franchise code of the series loser. |
| `Losing_Team_League` | `identifier/derived` | League of the series loser. |
| `Losing_Team_Name` | `identifier/derived` | Full name of the series loser. |
| `Made_Postseason` | `identifier/derived` | True if the club reached the postseason that year. |
| `Manager` | `identifier/derived` | Manager for the season. |
| `Opp_Started_LHP` | `parsed` | True when the opponent started a left-handed pitcher. |
| `Opponent` | `parsed` | Opponent franchise code. |
| `Park_Factor_Batting_1yr` | `identifier/derived` | Single-year batting park factor; over 100 favours hitters. |
| `Park_Factor_Batting_Multi` | `identifier/derived` | Multi-year batting park factor; over 100 favours hitters. |
| `Park_Factor_Pitching_1yr` | `identifier/derived` | Single-year pitching park factor; over 100 favours hitters. |
| `Park_Factor_Pitching_Multi` | `identifier/derived` | Multi-year pitching park factor; over 100 favours hitters. |
| `Player` | `name_display` | Player name. Baseball-Reference handedness markers have been stripped out into the Bats/Throws column. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. Holds the coach's id on Coaching_Staff. |
| `Players_Involved` | `parsed` | All player ids mentioned, comma separated. |
| `Position` | `parsed` | Fielding position the player occupied in that game. |
| `Postseason_Summary` | `identifier/derived` | Baseball-Reference's narrative summary of the club's postseason run. |
| `Prior_Attendance` | `parsed` | Total home attendance the previous season. |
| `Prior_Attendance_Per_Game` | `parsed` | Average home attendance the previous season. |
| `Prior_Home_Games` | `parsed` | Home dates played the previous season. |
| `Pythagorean_L` | `identifier/derived` | Expected losses from runs scored and allowed. |
| `Pythagorean_W` | `identifier/derived` | Expected wins from runs scored and allowed. |
| `Result` | `parsed` | W, L or T for the team in this row. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. Filter to 'data' for player-level analysis. |
| `Runs_Allowed` | `identifier/derived` | Runs allowed over the season. |
| `Runs_Scored` | `identifier/derived` | Runs scored over the season. |
| `Score` | `parsed` | Final score as printed, team runs first. |
| `Scouting_Director` | `identifier/derived` | Director of scouting. |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Series` | `identifier/derived` | Postseason round, e.g. World Series, ALCS. |
| `Series_Code` | `identifier/derived` | Short code for the round, e.g. WS, ALCS, NLDS1. |
| `Series_Result` | `identifier/derived` | Games won by each side, winner first. |
| `Series_URL` | `identifier/derived` | Baseball-Reference page for the series. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `Teams_Involved` | `parsed` | All clubs mentioned, comma separated. |
| `Throws` | `derived` | Throwing hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Transaction` | `parsed` | Full transaction text. |
| `Transaction_Date` | `parsed` | Date as printed by Baseball-Reference. |
| `Uniform_Number` | `parsed` | Jersey number worn that season. |
| `W` | `ppr_cur_w` | Current Wins |
| `Weekday` | `parsed` | Day of the week as printed by Baseball-Reference. |
| `Win_Pct` | `identifier/derived` | Winning percentage, W / (W + L). |
| `Winner_Wins` | `identifier/derived` | Games won by the winning club. |
| `Winning_Team` | `identifier/derived` | Franchise code of the series winner. |
| `Winning_Team_League` | `identifier/derived` | League of the series winner. |
| `Winning_Team_Name` | `identifier/derived` | Full name of the series winner. |
| `YoY_Attendance_Diff` | `parsed` | Change in total attendance versus the previous season. |
| `YoY_Attendance_Diff_Per_Game` | `parsed` | Change in attendance per game versus the previous season. |

#### Batting

153 fields.

| Field | Source code | Meaning |
| --- | --- | --- |
| `#Bat` | `batters_used` | Number of Players used in Games |
| `%_2` | `GIDP_perc` | Grounded Into Double Play Rate - Two or more outs via force outs on a ground ball. |
| `%_3` | `productive_outs_perc` | Productive Outs Percentage - Created by Elias and ESPN for three possible situations. - Successful Sac for a pitcher with one out. - Advancing any runner with none out. - Driving in a baserunner with the second out of the inning. - Failed means the batter m... |
| `%_4` | `lt_2_out_on_third_perc` | PAs with less than two out, runner on third and runner scored |
| `%_5` | `no_out_on_second_perc` | PAs with none out, runner on second and runner advanced Rate |
| `0,2B` | `no_out_on_second_opp` | PAs with no out, runner on second |
| `162WL%` | `b_waa_win_perc_162` | Win-Loss% w/ Avg. Team Season - This is the win-loss of an otherwise average team for an entire season giving them credit for only the games this player played in. - For example, for a pitcher this would be waaW-L% - in the games the pitcher threw in and a... |
| `1stD` | `on_first_double` | On First, when a double is hit - Times a runner is on first and the batter hits a double. |
| `1stD3` | `on_first_double_13` | On First, when a double is hit and runner reaches third |
| `1stDH` | `on_first_double_1H` | On First, when a double is hit and runner scores |
| `1stS` | `on_first_single` | On First, when a single is hit - Times a runner is on first and the batter hits a single. |
| `1stS2` | `on_first_single_12` | On First, when a single is hit and runner reaches second |
| `1stS3` | `on_first_single_13` | On First, when a single is hit and runner reaches third or scores |
| `20%` | `20_pitches_perc` | 2-0 Count Seen Percentage - 2-0 Counts / PA. |
| `20c` | `20_pitches` | 2-0 counts seen |
| `20s` | `20_swings` | Swinging on a 2-0 Count |
| `2ndS` | `on_second_single` | On Second, when a single is hit - Times a runner is on second and the batter hits a single. |
| `2ndS3` | `on_second_single_23` | On Second, when a single is hit and runner reaches third |
| `2ndSH` | `on_second_single_2H` | On Second, when a single is hit and runner scores |
| `30%` | `30_pitches_perc` | 3-0 Count Seen Percentage - 3-0 Counts / PA. |
| `30c` | `30_pitches` | 3-0 counts seen |
| `30s` | `30_swings` | Swinging on a 3-0 Count |
| `31%` | `31_pitches_perc` | 3-1 Count Seen Percentage - 3-1 Counts / PA. |
| `31c` | `31_pitches` | 3-1 counts seen |
| `31s` | `31_swings` | Swinging on a 3-1 Count |
| `AB` | `PH_ab` | Pinch Hit At Bats |
| `AB/HR` | `at_bats_per_home_run` | At Bats Per Home Run |
| `AB/RBI` | `at_bats_per_rbi` | At Bats Per Run Batted In |
| `AB/SO` | `at_bats_per_strikeout` | At Bats Per Strikeout - For career marks this only includes AB’s for seasons where SO’s were tracked. |
| `acLI` | `cli_avg` | Average Championship Leverage Index - The average pressure the pitcher or batter saw in this game or season. - 1.0 is average pressure, below 1.0 is low pressure and above 1.0 is high pressure. |
| `AIR` | `batter_air` | Hitting AIR - measures the offensive level of the leagues and parks the - player played in relative to an all-time - average of a .335 OBP and .400 Slugging Percentage. Over 100 - indicates a favorable setting for hitters, under 100 a favorable - setting fo... |
| `AS/Pit` | `pitches_swinging_perc` | Percentage of Pitches Swung At - (Inplay + Foul + Swinging Strikes) / (Total Pitches - intentional balls). |
| `AS/Str` | `all_strikes_swinging_perc` | Swung at Strikes Percentage - (Inplay + Foul + Swinging Strikes) / Total Strikes. |
| `ASG` | `allstar_games` | All-Star Game Selections - This does not indicate if the player played or not. |
| `Att` | `SH_att` | Sacrifice Bunts Attempted - Only includes unsuccessful bunts made and bunt strikeouts. - Failing to bunt early in the count and then swinging away later are not included. - Pre-1954 SH attempt counts are unavailable. |
| `Awards` | `awards` | Awards and honours for that season as listed by Baseball-Reference (e.g. AS = All-Star, MVP-1 = MVP winner). |
| `BA` | `b_batting_avg` | Hits/At Bats - For recent years, leaders need 3.1 PA - per team game played - Bold indicates either highest BA using current stats - or awarded title at end of year. |
| `BAbip` | `batting_avg_bip` | Batting Avg. on Balls in Plays (Hits - Home Runs)/(At Bats - SO - HR + Sac Flies) - This also measures how effectively the - defense turned balls into outs. |
| `BB%` | `b_base_on_balls_perc` | Base on Balls Percentage - Percentage of all plate appearances ending with a Base on Balls. - (BB)/(all plate appearances) |
| `boLI` | `bo_leverage_index_avg` | Base-Out Leverage - The average base-out leverage seen across all plays. |
| `BR` | `baserunners_tot` | Total Number of Baserunners when batter at plate |
| `BRS` | `drove_in_tot` | Baserunners who Scored - Total runners scored by batter (may not be by RBIs) |
| `BRS%` | `baserunners_scored_perc` | Percentage of all baserunners who scored on the batter’s play - (not necessarily with an RBI). |
| `BT` | `bases_taken` | Bases Taken - Bases advanced on fly balls, passed balls, wild pitches, balks, defensive indifference. |
| `BtRuns` | `abRuns` | Adjusted Batting Runs - A set of formulas developed by Gary Gillette, Pete Palmer and others - that estimates a player’s total contributions - to a team’s runs total via linear weights. - 0.0 is an avg performance, <0 is worse than avg and >0 is better than... |
| `BtWins` | `abWins` | Adjusted Batting Wins - A set of formulas developed by Gary Gillette, Pete Palmer and others - that estimates a player’s total contributions - to a team’s wins with his bat. - 0.0 is an avg performance, <0 is worse than avg and >0 is better than avg |
| `cClutch` | `cwpa_clutch` | cWPA Clutch - cWPA (overall)/acLI - cWPA/cLI (as shown) - The difference between context dependent cWPA and the context-neutral cWPA. - Displayed in percentage points. |
| `Cent%` | `b_center_perc` | Center Percentage - Percentage of all balls put into play (including home runs) that are hit to the center of the field. - Batted ball type and location is not complete prior to 1988. |
| `Clutch` | `wpa_clutch` | WPA Clutch - WPA (overall)/aLI - WPA/LI (as shown) - The difference between context dependent WPA and the context-neutral WPA. |
| `Con` | `contact_perc` | Contact Percentage - (Foul + Inplay Strikes) / (Foul + Inplay + Swinging Strikes). |
| `CS` | `b_cs` | Caught Stealing |
| `cWPA` | `adv_bat_cwpa_bat` | Championship Win Probability Added for Offensive Player - Given average teams, this is the change in probability of winning the World Series, displayed in percentage points. - See Win Expectancy explainer for details. |
| `cWPA+` | `cwpa_def_pos` | Championship Win Probability Added - Sum of positive events for this pitcher. - Displayed in percentage points. |
| `cWPA-` | `cwpa_def_neg` | Championship Win Probability Subtracted - Sum of negative events for this pitcher. - Displayed in percentage points. |
| `Debut` | `debut` | Date of Major League debut. |
| `dWAR` | `b_war_def` | Defensive Wins Above Replacement for position players - A defensive measure of wins above replacement, but given - only the defensive stats of the player and his position adjustment. For this calculation, we use a - replacement level on defense is the leagu... |
| `EV` | `b_avg_exit_velo` | Average Exit Velocity - Average speed of the ball off the bat for balls put into play, measured in miles per hour. |
| `F/Str` | `strike_foul_perc` | Foul Ball Strikes Percentage - Pitches Fouled Off / Total Strikes Seen. |
| `From` | `year_min` | First Year |
| `From Team` | `from_team_ID` | Club the player came from. |
| `Gact` | `G_actual` | Games Actual - Stats are adjusted to 162 games, but this is the - actual number of games for this player for this split. |
| `GIDP` | `b_gidp` | Double Plays Grounded Into - Only includes standard 6-4-3, 4-3, etc. double plays. - First tracked in 1933. - For gamelogs only in seasons we have play-by-play, we include triple plays as well. - All official seasonal totals do not include GITP's. |
| `GO/AO` | `go_ao_ratio` | Ground Outs to Air Outs - Double plays count as two. - Batted ball type and location is not complete prior to 1988. |
| `HardH%` | `b_hard_hit_perc` | Hard Hit Rate - Percent of balls in play with an exit velocity of 95 mph or more. |
| `HR` | `HR` | Home Runs Hit/Allowed |
| `HR%` | `home_run_perc` | Home Run Percentage - Percentage of all plate appearances a home run was hit. - (HR)/(all plate appearances) |
| `HR/FB` | `home_run_fb_perc` | Percentage of Fly Balls that were Home Runs - Includes all fly balls to the outfield including line drives. - Batted ball type and location is not complete prior to 1988. |
| `I/Bll` | `ball_intent_perc` | Intentional Ball Percentage - Intentional Balls / All Balls. |
| `I/Str` | `strike_inplay_perc` | Ball In Play Percentage - Balls put into Play (including home runs) / Total Strikes. |
| `IF/FB` | `infield_fb_perc` | Percentage of Fly Balls that were on the infield - Includes Line Drives. - Batted ball type and location is not complete prior to 1988. |
| `IP%` | `inplay_perc` | Balls In-Play Percentage - Percentage of all plate appearances with ball put into play. - (AB-SO-HR+SF)/(all plate appearances) |
| `ISO` | `b_iso_slugging` | (Total Bases - H)/At Bats or - (2B + 2*3B + 3*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `L/SO` | `SO_looking` | Strikeouts Looking |
| `L/SO%` | `SO_looking_perc` | Strikeout Looking Percentage - Strikeouts Looking / All Strikeouts. |
| `L/Str` | `strike_looking_perc` | Strikes Looking / Strikes - All strikes looking divided by all strikes. |
| `Lg` | `lg_ID` | League - AL - American League (1901-present) - NL - National League (1876-present) - AA - American Association (1882-1891) - UA - Union Association (1884) - PL - Players League (1890) - FL - Federal League (1914-1915) - NA - National Association (1871-1875)... |
| `lgBA` | `batting_avg_lg` | League Batting Average - The batting average a league average - (non-pitcher) would have had in the same park(s). |
| `lgOBP` | `onbase_perc_lg` | League On-base Percentage - The on-base percentage a league average - (non-pitcher) would have had in the same park(s). |
| `lgOPS` | `onbase_plus_slugging_lg` | League On-Base + Slugging - The OPS a league average - (non-pitcher) would have had in the same park(s). |
| `lgSLG` | `slugging_perc_lg` | League Slugging Percentage - The slugging percentage a league average - (non-pitcher) would have had in the same park(s). |
| `LOB` | `LOB` | Runners Left On Base |
| `OBP` | `b_onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) - For recent years, leaders need 3.1 PA - per team game played |
| `OOB` | `outs_on_base` | Outs on Base - Runner is put out while making a baserunning play. - Example plays: out advancing on a fly ball, out attempting to reach another base on a hit, - doubled off on a line drive, or out attempting to advance on a wild pitch or passed ball. - Does... |
| `OOB1` | `outs_on_base_1` | Outs on Base at 1st - Runner is put out while making a baserunning play. - Example plays: out advancing on a fly ball, out attempting to reach another base on a hit, - doubled off on a line drive, or out attempting to advance on a wild pitch or passed ball.... |
| `OOB2` | `outs_on_base_2` | Outs on Base at 2nd - Runner is put out while making a baserunning play. - Example plays: out advancing on a fly ball, out attempting to reach another base on a hit, - doubled off on a line drive, or out attempting to advance on a wild pitch or passed ball.... |
| `OOB3` | `outs_on_base_3` | Outs on Base at 3rd - Runner is put out while making a baserunning play. - Example plays: out advancing on a fly ball, out attempting to reach another base on a hit, - doubled off on a line drive, or out attempting to advance on a wild pitch or passed ball.... |
| `OOBHm` | `outs_on_base_h` | Outs on Base at Home - Runner is put out while making a baserunning play. - Example plays: out advancing on a fly ball, out attempting to reach another base on a hit, - doubled off on a line drive, or out attempting to advance on a wild pitch or passed ball... |
| `Oppo%` | `b_oppo_perc` | Opposite-Field Percentage - Percentage of all balls put into play (including home runs) that are hit to the batter's opposite (push) side. - Batted ball type and location is not complete prior to 1988. |
| `OPS` | `b_onbase_plus_slugging` | On-Base + Slugging Percentages - For recent years, leaders need 3.1 PA - per team game played |
| `OPS+` | `b_onbase_plus_slugging_plus` | OPS+ - 100*[OBP/lg OBP + SLG/lg SLG - 1] - Adjusted to the player’s ballpark(s) |
| `oRAR` | `b_rar_off` | Offensive Runs above Replacement Level - oWAR + dWAR DOES NOT EQUAL WAR, pos would be counted 2x - Total of all columns except for fielding values - Includes batting, baserunning, positional adjustment, and a playing time adjustment - for the number of runs... |
| `Outs` | `outs_made` | Outs Made - (At Bats - Hits) + Double Plays Grounded Into - + Sac. Flies + Sac. Hits + Caught Stealing. |
| `oWAR` | `b_war_off` | Offensive Wins Above Replacement (everything but Fielding) - The same statistic as Wins Above Replacement for Position - Players (WAR), but with the fielding value excluded. - oWAR + dWAR does not equal WAR. - Adding would count positions twice. - Contains... |
| `OWn%` | `offensive_winning_perc` | Offensive Winning Percentage - The percentage of games a team with nine of this player - batting would win. Assumes average pitching and defense. - This uses the Pythagorean win pct formula with the player's RC/G for runs scored and the league's R/9 as runs... |
| `PA` | `b_pa` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `PA_2` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `PHlev` | `PH_leverage` | Pinch Hit Leverage Index - The importance of the context in which the Pinch Hitter was used - Above one means higher than average pressure. - Below one means lower than average pressure. |
| `Pit` | `pitches` | Number of pitches in the PA. |
| `Pit/PA` | `pitches_per_pa` | Pitches per Plate Appearance |
| `Pitu` | `pitches_unknown` | Pitches for which ball-strike results are not known |
| `Plays` | `wpa_plays` | Plays included in WPA calculations - For batters, this includes all batting plays and baserunning plays where they were the lead baserunner whose state changed. |
| `Pos` | `pos` | Positions Played - Positions are listed in order of games played at each. - * indicates the player appeared in at least 2/3rds of team games at that position (applies to a single season or a career total). - Positions after / indicate fewer than ten games p... |
| `Pos_2` | `pos` | Positions Played - Positions are listed in order of games played at each. - * indicates the player appeared in at least 2/3rds of team games at that position (applies to a single season or a career total). - Positions after / indicate fewer than ten games p... |
| `Pos Summary` | `pos_summary` | Positions Played - The positions either followed by the games played at that position - or in order of games or innings played. - For a single season, * indicates they played at least 2/3rds of the team games there. - Positions after / indicate less than te... |
| `Pull%` | `b_pull_perc` | Pull Percentage - Percentage of all balls put into play (including home runs) that are hit to the batter's pull side. - Batted ball type and location is not complete prior to 1988. |
| `PwrSpd` | `power_speed_number` | Power/Speed Number - 2 x (Home Runs x Stolen Bases)/(Stolen Bases + Home Runs) - The harmonic mean of HR and SB. - To do well you need a lot of both. - Developed by Bill James. |
| `R/G` | `runs_per_game` | Runs Scored Per Game |
| `RAA` | `p_raa` | Runs better than Avg - IP*(RA9 avg - RA9)/9, then centered so the league average is always zero. - It is the number of runs this player is better than an average player. Adjusted for quality of opposition, parks pitched in and quality of team defense and re... |
| `RAR` | `runs_above_rep` | Runs above Replacement Level - Total of other columns It is the number of runs this player is better than a replacement player. Replacement is set for a .294 team winning percentage. Developed by Sean Smith of BaseballProjection.com |
| `Rbaser` | `b_runs_baserunning` | Runs from Baserunning - Number of runs better or worse than average the player was for all baserunning events. - SB, CS, PB, WP, Defensive Indifference. - Developed by Sean Smith of BaseballProjection.com |
| `Rbat` | `b_runs_batting` | Runs Batting - Number of runs better or worse than average the player was as a hitter. - This is based on a modified version of wRAA. - See our about section for a full description of how this is calculated. |
| `Rbat+` | `b_rbat_plus` | Rbat+ - Batting runs as computed for WAR, but indexed to the environment the player played in, where 100 is league average. |
| `RBI` | `PH_rbi` | Pinch Hit Runs Batted In |
| `RC` | `RC` | Runs Created - A set of formulas developed by Bill James and others - that estimates a player’s total contributions - to a team’s runs total. - This is computed with the "technical" formula when possible. - If SB or CS data is missing, the "basic" formula i... |
| `RC/G` | `RCpG` | Runs Created per Game - Runs created per (approximately) 27 outs used. - Can be thought of as the runs produced by a lineup of 9 of this player. |
| `Rdp` | `tz_runs_infield` | Total Zone Infield Double Play Runs Above Avg - The number of runs above or below average the player was worth based on double plays turned and opportunities given. - See the glossary section for a more complete explanation. - Provided by BaseballProjection... |
| `RE24` | `b_baseout_runs` | Base-Out Runs Added - Given the bases occupied/out situation, how many runs did the batter - or baserunner add in the resulting play. - Compared to average, so 0 is average, and above 0 is better than average |
| `RE24/boLI` | `re24_boli` | Situational Runs - The summation of for each play the change in run-expectancy divided by the base-out leverage |
| `REW` | `rew_bat` | Base-Out Wins Added (REW) - This is the number of wins above average the player was worth by their performance measured by the 24 - base-out situations across every play in the game. |
| `Rfield` | `b_runs_fielding` | Runs from Fielding - Number of runs better or worse than average the player was for all fielding. - Fielding of balls in play, turning double plays, outfield arms and catcher defense are all included. - We use Baseball Info Solutions Defensive Runs Saved wh... |
| `rOBA` | `b_roba` | rOBA - A measure of a player's offensive contributions, weighted in proportion to each event's actual run value |
| `Rpos` | `b_runs_position` | Runs from Positional Scarcity - Number of runs above or below average due to positional differences. - Positions like C, SS, and 2B get a bonus. - Positions like 1B, DH, LF get a penalty. - Developed by Sean Smith of BaseballProjection.com |
| `Rrep` | `b_runs_replacement` | Runs from Replacement Level - Number of runs an average player is better than a replacement player. - Replacement is set for a .294 team winning percentage. - Stronger leagues may get a larger bonus. - Developed by Sean Smith of BaseballProjection.com |
| `RS%` | `b_run_scoring_perc` | Run Scoring Percentage - Percentage of times a baserunner eventually scores a run. - (R - HR) / (H + HBP + BB - HR + G_pr) |
| `S/SO` | `SO_swinging` | Strikeouts Swinging |
| `S/Str` | `strike_swinging_perc` | Swinging Strike Percentage - Strikes Swinging (w/o contact) / Total Strikes. |
| `Salary` | `Salary` | These values may not include every bonus the player received in a season. - They are also often missing values for mid-season callups or players acquired in-season. - Post-1984 seasons are mostly complete, pre-1985 is mostly incomplete. |
| `SB` | `b_sb` | Stolen Bases |
| `SB%` | `b_stolen_base_perc` | Stolen Base Percentage - SB / (SB + CS) |
| `SecA` | `secondary_avg` | Secondary Average - (Total Bases - Hits + BB + SB - CS) / AB - Over .500, excellent; < 200, poor |
| `SF` | `b_sf` | Sacrifice Flies - First tracked in 1955. |
| `SH` | `b_sh` | Sacrifice Hits (Sacrifice Bunts) |
| `SLG` | `b_slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `SO%` | `b_strikeout_perc` | Strikeout Percentage - Percentage of all plate appearances ending with a strikeout. - (SO)/(all plate appearances) |
| `Str` | `strikes_total` | Strikes - Includes both pitches in the zone and those swung at out of the zone. |
| `Str%` | `strike_perc` | Strike Percentage - Strikes / Total Pitches (intentional balls excluded). |
| `Stru` | `strikes_unknown` | Strikes for which detailed results are not known |
| `Suc` | `SH_suc` | Successful Sacrifice Bunts |
| `Suc_2` | `productive_outs` | Productive Outs Made - Created by Elias and ESPN for three possible situations. - Successful Sac for a pitcher with one out. - Advancing any runner with none out. - Driving in a baserunner with the second out of the inning. - Failed means the batter made an... |
| `TB` | `b_tb` | Total Bases - Singles + 2 x Doubles + 3 x Triples + 4 x Home Runs. |
| `To` | `year_max` | Last Year |
| `TotA` | `total_avg` | Total Average - Developed by Thomas Boswell of the Washington Post - (Total Bases + HBP + BB + SB) / (AB - H + CS + GIDP) |
| `WAA` | `b_waa` | Wins Above Average for position players - A single number that presents the number of wins the player added - to the team above what a league average player would add. - Scale: 6+ MVP Quality, 3+ All-Star Quality, 0 Starter, - -2-0 Reserve, < -2 Replacement... |
| `waaWL%` | `b_waa_win_perc` | Win-Loss% w/ Avg. Team - This is the win-loss of an otherwise average team in ONLY the games this player played in. - For example, for a pitcher this would only consider the games the pitcher threw in and ignoring games they did not play in. |
| `WAR/pos` | `WAR_bat` | Wins Above Replacement for position players - A single number that presents the number of wins the player added - to the team above what a replacement player (think AAA or AAAA) would add. - Scale: 8+ MVP Quality, 5+ All-Star Quality, 2+ Starter, - 0-2 Rese... |
| `WAR3` | `WAR` | WAR from last three years |
| `WPA` | `adv_bat_wpa_bat` | Win Probability Added for Offensive Player - Given average teams, this is the change in probability - caused by this batter during the game. - See Win Expectancy explainer for details. |
| `WPA+` | `wpa_def_pos` | Win Probability Added - Sum of positive events for this pitcher. |
| `WPA-` | `wpa_def_neg` | Win Probability Subtracted - Sum of negative events for this pitcher. |
| `WPA/LI` | `wpa_li_bat` | Situational Wins (WPA/LI) - It is the sum of WPA divided by the leverage index for each play. - WPA depends greatly on the context of the at bats. - This stat does not. |
| `X/H%` | `extra_base_hit_per_hit_perc` | Percentage of all hits for extra bases - Percentage of all hits resulting in extra bases. - (2B + 3B + HR) / H ) |
| `XBH%` | `extra_base_hit_perc` | Extra Base Hit Percentage - Percentage of all plate appearances ending with an Extra Base Hit. - (2B + 3B + HR)/(all plate appearances) |
| `XBT%` | `b_extra_bases_taken_perc` | Extra Bases Taken Percentage - Percentage of times the runner advanced more than one base on a single or more than two bases on a double, when possible. - Does not take into account the location or type of the ball in play. |

#### Pitching

138 fields.

| Field | Source code | Meaning |
| --- | --- | --- |
| `#1` | `sp_1` | Primary starting pitcher #1 in the rotation. |
| `#2` | `sp_2` | Primary starting pitcher #2 in the rotation. |
| `#2_2` | `bu_2` | Second-most-used bullpen arm. |
| `#3` | `sp_3` | Primary starting pitcher #3 in the rotation. |
| `#3_2` | `bu_3` | Third-most-used bullpen arm. |
| `#4` | `sp_4` | Primary starting pitcher #4 in the rotation. |
| `#4_2` | `bu_4` | Fourth-most-used bullpen arm. |
| `#5` | `sp_5` | Primary starting pitcher #5 in the rotation. |
| `#P` | `pitchers_used` | Number of Pitchers used in Games |
| `%` | `SH_perc` | Sacrifice Bunts Success Rate - Only includes unsuccessful bunts made and bunt strikeouts. - Failing to bunt early in the count and then swinging away later are not included. - Pre-1954 SH attempt counts are unavailable. |
| `02%` | `02_pitches_perc` | 0-2 Count Seen Percentage - 0-2 Counts / PA. |
| `02c` | `02_pitches` | 0-2 counts seen |
| `02h` | `02_hits` | Hits given up on an 0-2 Count |
| `02s` | `02_strikes` | Strikes thrown on an 0-2 Count |
| `0DR` | `DR_0` | Zero Days Rest - Times the pitcher pitched on consecutive days, or both ends of a doubleheader. |
| `100-119` | `pitches_100to119` | GS with 100 to 119 pitches |
| `1st%` | `first_pitch_strike_perc` | First Pitch Strike Percentage - Percentage of plate appearances that - began 0-1 or with a ball in play. |
| `1stIP` | `inning_first_mode` | Most Common Inning to Enter Game - Ties go to the later inning. |
| `3pK` | `SO_3_pitches` | 3-Pitch Strikeouts |
| `4pW` | `BB_4_pitches` | 4-pitch Walks |
| `80-99` | `pitches_80to99` | GS with 80 to 99 pitches |
| `<2,3B` | `lt_2_out_on_third_opp` | PAs with less than two out, runner on third |
| `<3o` | `IPouts_lt3` | Games the pitcher completed fewer than three outs |
| `<80` | `pitches_lt80` | GS with under 80 pitches |
| `>3o` | `IPouts_gt3` | Games the pitcher completed more than three outs |
| `Age` | `age` | Age of player on day of debut or final game, YY.DDD - Age on June 30th of debut season is used if exact debut date is unknown |
| `Ahd` | `enter_ahead` | Games Entered with Lead - Pitcher entered the game with his team in the lead. |
| `aLI` | `leverage_index_avg` | Average Leverage Index - The average pressure the pitcher or batter saw in this game or season. - 1.0 is average pressure, below 1.0 is low pressure and above 1.0 is high pressure. |
| `All` | `HR_all` | Home Run Total |
| `BB` | `b_bb` | Bases on Balls/Walks |
| `BB9` | `p_bb_per_nine` | 9 x BB / IP - For recent years, leaders need 1 IP - per team game played |
| `Best` | `ppr_best` | 95th Percentile Wins |
| `BF` | `p_bfp` | Batters Faced |
| `BFP` | `BFP` | Batters faced by the pitcher. |
| `Bhd` | `enter_behind` | Games Entered Behind - Pitcher entered the game with his team trailing. |
| `BK` | `p_bk` | Balks |
| `Bnt` | `H_bunt` | Bunt Hits - Batted ball type and location is not complete prior to 1988. |
| `BQR` | `bequeathed_runners` | Bequeathed Runners - Number of runners on base when pitcher left the game. - This includes both starts and games in relief. |
| `BQS` | `bequeathed_score` | Bequeathed Runners Score - Number or percentage of runners on base when pitcher left the game who subsequently scored. - These runners show up in the pitcher’s ERA. - This includes both starts and games in relief. |
| `BSv` | `BSv` | Blown Saves - Pitcher entered the game in a save situation and lost the lead. |
| `CG` | `f_cg` | Complete Games at a Single Position |
| `Closer` | `cl` | Primary closer. |
| `cSho` | `SHO_cg` | Shutouts - No runs allowed and a complete game. |
| `Empt` | `enter_empty` | Games Entered With Bases Empty - Pitcher entered the game with no runners on base. |
| `ER` | `p_er` | Earned Runs Allowed |
| `ERA` | `p_earned_run_avg` | 9 * ER / IP - For recent years, leaders need 1 IP - per team game played. - Bold indicates lowest ERA using current stats - Gold means awarded ERA title at end of year. |
| `ERA+` | `p_earned_run_avg_plus` | ERA+ - 100*[lgERA/ERA] - Adjusted to the player’s ballpark(s). |
| `FB%` | `p_fb_perc` | Fly Ball Percentage - Percentage of all balls put into play (including home runs) that are fly balls. - EXCLUDES Popups - Batted ball type and location is not complete prior to 1988. |
| `FIP` | `p_fip` | Fielding Independent Pitching - this stat measures a pitcher's effectiveness at preventing HR, BB, HBP and causing SO - (13*HR + 3*(BB+HBP) - 2*SO)/IP + Constant lg - The constant is set so that each season major-league average FIP is the same as the major-... |
| `G` | `G` | Games Played - This includes all times that the player appeared on the lineup card. Pitchers in non-DH games that appeared on the lineup card but didn't bat will still have a game in this column. |
| `GB%` | `p_gb_perc` | Ground Ball Percentage - Percentage of all balls put into play (including home runs) that are ground balls. - EXCLUDES Bunts - Batted ball type and location is not complete prior to 1988. |
| `GB/FB` | `p_gb_fb_ratio` | Ground Ball to Fly Ball Ratio - Includes line drives as fly balls. - Batted ball type and location is not complete prior to 1988. |
| `GDP` | `GIDP` | Double Plays Grounded Into - Only includes standard 6-4-3, 4-3, etc. double plays. - First tracked in 1933. - For gamelogs only in seasons we have play-by-play, we include triple plays as well. - All official seasonal totals do not include GITP's. |
| `GF` | `GF` | Games Finished - Credited to the last pitcher to appear for a team in a game. - Complete Games are not counted as Games Finished. |
| `gmLI` | `p_leverage_index_avg_rp` | Game-entering Leverage Index - Solely for relief appearances, this is the average of each appearances opening leverage index - weighted by the batters faced in that outing. - The average pressure the pitcher or batter saw in this game or season. - 1.0 is av... |
| `GmScA` | `game_score_avg` | Average Game Score |
| `GR` | `GR` | Games in Relief |
| `GS` | `HR_gs` | Grand Slam Home Runs |
| `GSo` | `HR_gs_opp` | Grand Slam Opportunities - Plate Appearances with the Bases Loaded |
| `H` | `H` | Hits/Hits Allowed |
| `H9` | `p_hits_per_nine` | 9 x H / IP - For recent years, leaders need 1 IP - per team game played |
| `HBP` | `HBP` | Times Hit by a Pitch. |
| `Hold` | `Hold` | Holds - Pitcher entered the game in a save situation and did not get - the win (due to < 5 IP by starter) or save. - The pitcher then retires at least one batter and leaves the game - without having relinquished the lead at any point. - A pitcher can get a... |
| `HR9` | `p_hr_per_nine` | 9 x HR / IP - For recent years, leaders need 1 IP - per team game played |
| `IBB` | `b_ibb` | Intentional Bases on Balls - First tracked in 1955. |
| `Inf` | `H_inf` | Infield Hits - Batted ball type and location is not complete prior to 1988. |
| `IP` | `HR_iphr` | Inside-The-Park Home Runs - Note that batted ball type and location data is incomplete prior to 1988. |
| `IP/GS` | `innings_per_start` | Innings Pitched per Game Started |
| `IPmult` | `IP_multi` | Games the pitcher pitched in more than one inning |
| `IR` | `inherited_runners` | Inherited Runners - Number of runners on base when pitcher entered the game. |
| `IS` | `inherited_score` | Inherited Score - Number or percentage of runners on base when pitcher entered the game who subsequently scored. - These runners show up in the previous pitcher’s ERA. |
| `IS%` | `inherited_score_perc` | Inherited Score Percentage - Percentage of runners on base when pitcher entered the game who subsequently scored. - These runners show up in the previous pitcher’s ERA. |
| `K%` | `p_strikeout_perc` | Strikeout Percentage - Percentage of all batters faced struck out. - (SO)/(BFP) |
| `LD%` | `p_ld_perc` | Line Drive Percentage - Percentage of all balls put into play (including home runs) that are line drives. - Batted ball type and location is not complete prior to 1988. |
| `lDR` | `DR_long` | Long Days Rest - More than four days rest. |
| `LevHi` | `enter_leverage_high` | Games entered with High Leverage - The first PA of the pitcher’s appearance - has a leverage of 1.5 or higher. |
| `LevLo` | `enter_leverage_low` | Games entered with Low Leverage - The first PA of the pitcher’s appearance - has a leverage of 0.7 or lower. |
| `LevMd` | `enter_leverage_med` | Games entered with Medium Leverage - The first PA of the pitcher’s appearance - has a leverage between 0.7 and 1.5. |
| `Lgr` | `L_GR` | Losses in relief |
| `Lgs` | `L_GS` | Losses in games started |
| `Lsv` | `L_saved` | Losses Saved - At the time of his last batter - the pitcher was in position for a loss, - but team came back to tie or take lead. |
| `Ltm` | `L_team` | Team Losses in games started |
| `Ltuf` | `L_tough` | Tough Losses - Losses in quality starts |
| `Max` | `pitches_max` | Most pitches in a start |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `ND` | `no_decision_GS` | No Decisions in Games Started |
| `Out/GR` | `outs_per_GR` | Average Outs Recorded per Game in Relief |
| `PAu` | `PA_unknown` | Plate Appearances for which data is not known - Note that for many stats (like pitcher SLG, 2B, 3B allowed, WPA, HR direction, etc.) - this will mean that the totals given are incomplete. |
| `Pit/GR` | `pitches_per_GR` | Pitches per Game in Relief |
| `Pit/GS` | `pitches_per_start` | Pitches per Game Started |
| `PPFp` | `p_ppf_custom` | Park Factor customized for parks the pitcher threw in - From 1908 on, we have full gamelogs, so we can say exactly how many innings a pitcher threw in each park. These are 3-year park factors weighted by batters faced in each park. Note the one-game park fa... |
| `PtchR` | `apRuns` | Adjusted Pitching Runs - A set of formulas developed by Gary Gillette, Pete Palmer and others - that estimates a pitcher’s total contributions - to a team’s runs total via linear weights. - 0.0 is an avg performance, <0 is worse than avg and >0 is better th... |
| `PtchW` | `apWins` | Adjusted Pitching Wins - A set of formulas developed by Gary Gillette, Pete Palmer and others - that estimates a pitcher’s total contributions - to a team’s wins with his arm. - 0.0 is an avg performance, <0 is worse than avg and >0 is better than avg |
| `Ptn%` | `PA_with_platoon_adv_perc` | Percentage of PA with the platoon advantage - Switch hitters should be 100% for most cases. - For pitchers, facing a batter of the same hand. - For batters, facing a pitcher of the opposite hand. |
| `QS` | `QS` | Quality Start - Pitcher pitched at least 6 innings - and allowed 3 or fewer earned runs in a start. |
| `QS%` | `quality_start_perc` | Quality Start Percentage - Percentage of starts that were quality starts (≥ 6 IP, ≤ 3 ER). |
| `R` | `R` | Runs Scored/Allowed |
| `RA/G` | `runs_allowed_per_game` | Runs Allowed Per Game |
| `RA9` | `p_ra9` | Runs Allowed Per 9 IP - This is like ERA, but with unearned runs included. |
| `RA9avg` | `p_ra9_avg_pitcher` | Runs per 9 IP for an avg pitcher - Equals PPFp/100*(oppRA9 - RAdef + RArole) - This is our best estimate of what an average pitcher would do against these opponents, with this defense and in these parks. |
| `RA9def` | `p_ra9_def` | Runs per 9 IP of support from defense - This is based on the team’s Baseball Info Solutions Defensive Runs Saved since 2003 and Total Zone Rating before that. Negro League seasons use Defensive Regression Analysis. Positive values mean the team defense was... |
| `RA9extras` | `p_ra9_extras` | Runs per 9 IP difference for pitching in extra innings - Starting in 2020, MLB had teams begin every extra inning with a runner on second base. If this runner scores, it is charged to the pitcher who started the inning. We adjust the pitcher's expected runs... |
| `RA9opp` | `p_ra9_opp` | Opponents’ Runs Scored Per 9 Inn - The average number of runs scored by this pitcher's opposition, per 9 innings. We use park factors to convert the opponent scoring to a league-average context.For in progress seasons, we consider the teams’ last 365 days.... |
| `RA9role` | `p_ra9_role` | Runs per 9 IP difference for SP and RP - From 1960 on we assess factor for starters and relievers. In that time, relievers have averaged a much lower ERA, and this factor accounts for that difference. Previously, this was part of our replacement level calcu... |
| `Rd` | `HR_rd` | Home Runs on the Road |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `RS/GS` | `run_support_cg` | Run Support per Game - Runs scored/27 outs in the entire - game when the pitcher started. |
| `RS/IP` | `run_support_pg` | Run Support per Innings - Runs scored/27 outs while the pitcher was in the game as the pitcher. |
| `Runr` | `enter_runners_on` | Games Entered With Runners On - Pitcher entered the game with runners on base. |
| `Scr` | `lt_2_out_on_third_scored` | PAs with less than two out, runner on third and runner scored |
| `sDR` | `DR_short` | Short Days Rest - Less than four days rest. |
| `SHO` | `p_sho` | Shutouts - No runs allowed and a complete game. |
| `SO` | `lt_2_out_on_third_so` | PAs with less than two out, runner on third and pitcher struck out batter |
| `SO-BB%` | `strikeout_minus_base_on_balls_perc` | Strikeout - Base on Balls Percentage - The differential of all batters faced between Strikeouts and Base on Balls - (SO-BB)/(all plate appearances) |
| `SO/BB` | `p_strikeouts_per_base_on_balls` | SO/W or SO/BB - For recent years, pitching leaders need 1 IP - per team game played. |
| `SO/W` | `strikeouts_per_base_on_balls` | SO/W or SO/BB - For recent years, pitching leaders need 1 IP - per team game played. - No batting leaders computed. |
| `SO9` | `p_so_per_nine` | 9 x SO / IP - For recent years, leaders need 1 IP - per team game played |
| `SV` | `p_sv` | Saves |
| `SV%` | `SvOpp_perc` | Save Percentage - Saves/Save Opportunities - Save Opportunities is Saves + Blown Saves. - 1973 and before, there are 90+ games where a pitcher earned the save - under the current rule, but was not credited with a save. |
| `SVOpp` | `SvOpp` | Save Opportunities - This is Saves + Blown Saves. - 1973 and before, there are 90+ games where a pitcher earned the save - under the current rule, but was not credited with a save. |
| `SVSit` | `SvSit` | Save Situations - Pitcher entered the game after the fifth inning in a save situation. - Or pitcher entered earlier in the game and did not get the win. - When the starter did not go five innings, it is - possible to enter in a save situation and get the wi... |
| `Tie` | `enter_tied` | Games Entered Tied - Pitcher entered the game tied. |
| `tmW-L%` | `win_loss_perc_team` | Team Win-Loss Percentage - Wtm / (Wtm + Ltm) - The win-loss percentage of the team in games started by this pitcher. |
| `tSho` | `SHO_team` | Shutouts by a team - No runs allowed in a game by one or more pitchers. |
| `vLH` | `HR_vlh` | Home Runs off Left-Handers |
| `vRH` | `HR_vrh` | Home Runs off Right-Handers |
| `W-L%` | `win_loss_perc` | Win-Loss Percentage - W / (W + L) - For players, leaders need one decision for every ten team games. - For managers, minimum to qualify for leading is 320 games. |
| `WAAadj` | `p_waa_adj` | Wins Above Avg Adjustment - For relief pitchers, we multiply WAA by (1+gmLI)/2. This is done in recognition of the added importance of high leverage. WAA adj is the additional value of this leverage adjustment. Also, the manner in which this and the WAA cal... |
| `WAR` | `p_war` | Wins Above Replacement for Pitchers - A single number that presents the number of wins the player added - to the team above what a replacement player (think AAA or AAAA) would add. This value includes defensive support and includes additional value for high... |
| `Wchp` | `W_cheap` | Cheap Wins - Wins in starts with < 6 IP or more than 3 ER - Or wins in non-quality starts. |
| `Wgr` | `W_GR` | Wins in relief |
| `Wgs` | `W_GS` | Wins in games started |
| `WHIP` | `p_whip` | (BB + H)/IP - For recent years, leaders need 1 IP - per team game played |
| `Wlst` | `W_lost` | Wins Lost - At the time the pitcher faced his final batter - the pitcher was in position for a win, - but game was blown by bullpen. |
| `WP` | `f_wp_catcher_only` | Wild Pitches |
| `Wrst` | `game_score_worst` | Worst Game Score |
| `Wtm` | `W_team` | Team Wins in games started |
| `≥120` | `pitches_ge120` | GS with 120 or more pitches |

#### Fielding and appearances

120 fields.

| Field | Source code | Meaning |
| --- | --- | --- |
| `#Fld` | `fielders_used` | Number of Players used as Fielders |
| `163` | `DP_163` | 1-6 or 4-3 Double Plays - Any play where the pitcher started the double play to second on to first. |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `263` | `DP_263` | 2-6 or 4-3 Double Plays - Any play where the catcher started the double play to second on to first. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `31` | `PO_31` | Putouts on first baseman (or other) to pitcher at first. |
| `36` | `DP_36` | 3-6 Double Plays - Any play where the first baseman started the DP with a force and ended by another fielder at second (2B or SS). |
| `361` | `DP_361` | 3-6-1 Double Plays - Any play where the first baseman started and ended by another fielder at first (P or 2B). |
| `363` | `DP_363` | 3-6-3 Double Plays - Any play where the first baseman started and ended the double play. |
| `3B` | `A_3B` | Assists where the ball was thrown to 3b as the result of a ball in play. |
| `3U` | `PO_3u` | Putouts on unassisted putouts of the batter. |
| `43` | `DP_43` | 4-3 Double Plays - Second basemen tags runner or steps on second and throws to first. |
| `463` | `DP_463` | 4-6-3 Double Plays |
| `53` | `DP_53` | 5-3 Double Plays - Third basemen tags runner or steps on third and throws to first. |
| `543` | `DP_543` | 5-4-3 Double Plays |
| `63` | `DP_63` | 6-3 Double Plays - Shortstop tags runner from first or steps on second and throws to first. |
| `643` | `DP_643` | 6-4-3 Double Plays |
| `A` | `f_assists` | Assists |
| `Adv` | `outfield_arm_adv` | Total Plays from five previous situations where baserunner advanced the extra base. |
| `Aother` | `A_other` | Assists other than kills from the five previous situations. |
| `bF2O%` | `inplay_bunt_fielded_outs_perc` | Percentage of bunts fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `bFld` | `inplay_bunt_fielded` | Number of bunts fielded - For many years, the fielder for non-out plays or the batted ball type is - unknown and this information will not be presented. |
| `BIP%` | `PA_with_bip_perc` | Percentage of PAs that ended with ball in play |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Cgt` | `PO_caught` | Putouts where the ball was caught in the air. |
| `Ch` | `steal_2b_chances` | Chances to steal second base - Plate appearances with a runner on first and no runner on second. |
| `CS%` | `f_cs_perc_catcher_only` | Caught Stealing Percentage - CS / (SB + CS) |
| `CS2` | `CS_2` | Caught Stealing 2nd Base |
| `CS3` | `CS_3` | Caught Stealing 3rd Base |
| `CSctch` | `CS_catcher` | Caught Stealing by Catcher Caught stealings where the catcher registered an assist. - Pickoff Caught Stealing by the pitcher are included in the CS number. |
| `CSH` | `CS_H` | Caught Stealing Home |
| `CSlev` | `CS_leverage` | Caught Stealing Leverage Index - The importance of the context in which the runner was caught - Above one means higher than average pressure. - Below one means lower than average pressure. |
| `DefEff` | `defensive_efficiency` | Defensive Efficiency - Percentage of balls in play converted into outs - This is an estimate based on team defensive and pitching stats. - We utilize two estimates of plays made. - One using innings pitched, strikeouts, double plays and outfield assists. -... |
| `DP` | `GIDP_suc` | Grounded Into Double Play - Two or more outs via force outs on a ground ball. |
| `E` | `f_errors` | Errors Committed |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `FBIP%` | `PA_with_fbip_perc` | Percentage of PAs that ended with a fly ball in play. |
| `FC` | `FC` | Fielder’s Choice - Play by fielder was made on a runner rather than the batter. |
| `Fld` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Fld%` | `f_fielding_perc` | Fielding Percentage - (Putouts + Assists) / (Putouts + Assists + Errors) |
| `Fld_2` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Frc` | `PO_force` | Putouts from force plays. |
| `G_team` | `G_team` | Games played by the team while the player was on the roster. |
| `GB` | `games_back` | Games Back of Division/League Leader - Computed as games over .500 of leader (W-L) minus games over .500 of team divided by two. - Typically computed at the end of play for a particular day. - Blank for 1st game of DH. |
| `GBIP%` | `PA_with_gbip_perc` | Percentage of PAs that ended with ground ball in play (not a bunt). |
| `GBr` | `GDP_relay` | Ground Ball Double Plays Relayed - Any ground ball double play where the fielder had the first putout and second assist. |
| `GBs` | `GDP_start` | Ground Ball Double Plays Started - Any ground ball double play where the fielder had the first assist. |
| `Held` | `single_runner_on_first_held` | Total Plays with single and runner on first held to second |
| `Held%` | `outfield_arm_held_perc` | Percentage of Plays from five previous situations where player did not advance. |
| `Held_2` | `single_runner_on_second_held` | Total Plays with single and runner on second held to third |
| `Held_3` | `double_runner_on_first_held` | Total Plays with double and runner on first held to third |
| `Held_4` | `flyout_runner_on_third_held` | Total Plays with < 2 out, a flyout, and runner on third held to third |
| `Held_5` | `flyout_runner_on_second_held` | Total Plays with < 2 out, a flyout, and runner on second held to second |
| `Held_6` | `outfield_arm_held` | Total Plays from five previous situations where player did not advance. |
| `Hm` | `A_H` | Assists where the ball was thrown to Home as a result of a ball in play. |
| `Inn` | `extra_innings` | Innings - Only shown if something other than 9 innings were played. |
| `K23` | `A_k23` | Assists on dropped third strikes and the ball thrown to 1b. |
| `Kill` | `single_runner_on_first_kill` | Total Plays with single and runner on first thrown out at third |
| `Kill%` | `outfield_arm_kill_perc` | Percentage of Plays from five previous situations where baserunner was thrown out trying to advance. |
| `Kill_2` | `single_runner_on_second_kill` | Total Plays with single and runner on second thrown out at home. |
| `Kill_3` | `double_runner_on_first_kill` | Total Plays with double and runner on first thrown out at home. |
| `Kill_4` | `flyout_runner_on_third_kill` | Total Plays with < 2 out, a flyout, and runner on third thrown out at home. |
| `Kill_5` | `flyout_runner_on_second_kill` | Total Plays with < 2 out, a flyout, and runner on second thrown out at third. |
| `Kill_6` | `outfield_arm_kills` | Total Plays from five previous situations where runner is thrown out attempting to advance. |
| `LD` | `LDP` | Line Drive Double Plays - Any line drive double play where the fielder took part. |
| `LDf` | `LDP_finish` | Line Drive Double Plays Finished - Any line drive double play where the fielder recorded the second putout. |
| `LDs` | `LDP_start` | Line Drive Double Plays Started - Any line drive double play where the fielder recorded the first putout. |
| `lgRF9` | `f_range_factor_per_nine_lg` | League Range Factor per 9 Inn - Average Range Factor the league - 9 * (Putouts + Assists) / Innings Played |
| `lgRFG` | `f_range_factor_per_game_lg` | League Range Factor per Game - Average Range Factor for the league for chances per game - (Putouts + Assists) / Games Played |
| `n23` | `DP_n23` | ?-2-3 Double Plays - Any double play with the bases loaded home on to first. |
| `Opp` | `single_runner_on_first` | Total Plays with single and runner on first - Note: Plays where the runner on 2B stops at 3B are not included. |
| `Opp_2` | `productive_outs_opp` | Productive Outs Made or Failed - Created by Elias and ESPN for three possible situations. - Successful Sac for a pitcher with one out. - Advancing any runner with none out. - Driving in a baserunner with the second out of the inning. - Failed means the batt... |
| `Opp_3` | `double_runner_on_first` | Total Plays with double and runner on first |
| `Opp_4` | `flyout_runner_on_third` | Total Plays with < 2 out, a flyout, and runner on third |
| `Opp_5` | `flyout_runner_on_second` | Total Plays with < 2 out, a flyout, and runner on second |
| `Opp_6` | `outfield_arm_opps` | Total Plays from five previous situations. |
| `PB` | `f_pb_catcher_only` | Passed Balls |
| `PCS` | `POCS` | Pickoff Caught Stealing - Runner picked off a base and or while attempting to steal. - Is included in CS numbers and PO numbers. |
| `Pick` | `f_pickoffs_catcher_only` | Pickoffs - Runner picked off a base. May include cases they were safe on an error. - Also includes Pickoff Caught Stealing plays. |
| `PO` | `pickoffs` | Pickoffs - Runner picked off a base. May include cases they were safe on an error. - Also includes Pickoff Caught Stealing plays. |
| `PO_2` | `pickoffs` | Pickoffs - Runner picked off a base. May include cases they were safe on an error. - Also includes Pickoff Caught Stealing plays. |
| `Rair` | `bis_runs_air` | BIS Infield Air Ball Runs Above Avg - The number of runs above or below average the player was worth based on infield air balls. - Provided by Baseball Info Solutions |
| `RBA` | `runner_bases_added` | Runner Bases Added - Total bases added on baserunning plays while this player was a catcher including WP, PB, and SB. |
| `Rbnt` | `bis_runs_bunts` | BIS Bunts Fielded Runs Above Avg - The number of runs above or below average the player was worth solely on bunts. - Provided by Baseball Info Solutions |
| `Rctch` | `tz_runs_catcher` | Total Zone Catcher Runs Above Avg - The number of runs above or below average the catcher was worth based on baserunner kills and baserunner advances. - See the glossary section for a more complete explanation. - Provided by BaseballProjection.com |
| `Rdp_2` | `bis_runs_infield` | BIS Infield Double Play Runs Above Avg - The number of runs above or below average the player was worth based on double plays turned and opportunities given. - Provided by Baseball Info Solutions |
| `Rdrs` | `bis_runs_total_team` | BIS Defensive Runs Saved Above Avg - The number of runs above or below average the team was worth based on their overall defense. - This number combines the individual players' defensive runs saved as well as team-level runs saved from shifting and position... |
| `Rdrs/yr` | `bis_runs_total_per_season_team` | BIS Defensive Runs Saved Above Avg per 1,200 Inn - The number of runs above or below average the team's fielders were worth per 1,200 Innings (approx 135 games). - This number combines the R pm , R dp , and R good numbers into a total defensive contribution... |
| `RerC` | `bis_runs_catcher_er` | BIS Catcher Pitch Calling Runs Above Avg - The number of runs above or below average the catcher was for the pitcher ERA. - Provided by Baseball Info Solutions |
| `RF/9` | `f_range_factor_per_nine` | Range Factor per 9 Inn - 9 * (Putouts + Assists) / Innings Played |
| `RF/G` | `f_range_factor_per_game` | Range Factor per Game - (Putouts + Assists) / Games Played |
| `Rgood` | `bis_runs_good_plays` | BIS Good Plays/Misplays Runs Above Avg - The number of runs above or below average the player was worth based on plays where they made an exceptional contribution or obviously misplayed the situation. - Provided by Baseball Info Solutions |
| `RHB%` | `PA_with_rhb_perc` | Percentage of PAs with a Right-Handed Batter |
| `RK` | `runner_kills` | Runner Kills - Total baserunners thrown out by the catcher including CS, pickoffs and other outs attempting to advance. |
| `Rly` | `A_relay` | Assists where the ball was thrown as part of a relay. Only counts relays where the initial throw came from the outfield. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Rof` | `tz_runs_outfield` | Total Zone Outfield Arm Runs Above Avg - The number of runs above or below average the player was worth based on baserunner kills and baserunner advances. - See the glossary section for a more complete explanation. - Provided by BaseballProjection.com |
| `Rof_2` | `bis_runs_outfield` | BIS Outfield Arm Runs Above Avg - The number of runs above or below average the player was worth based on baserunner kills and baserunner advance. - Provided by Baseball Info Solutions |
| `Rpm` | `bis_runs_field` | BIS Plus/Minus Fielding Runs Above Avg - The number of runs above or below average the player was worth based on fielding plays made. - This number combines the R range , R air , and R throw numbers. - This number does not include OF kills, or double plays... |
| `Rrange` | `bis_runs_range` | BIS Infield Range Runs Above Avg - The number of runs above or below average the player was worth based on his performance between when the ball was hit and when the fielder gets to the ball (or fails to). - Provided by Baseball Info Solutions |
| `RsbC` | `bis_runs_catcher_sb` | BIS Catcher Runs Above Avg - The number of runs above or below average the catcher was worth based on baserunner kills and baserunner advances. - Provided by Baseball Info Solutions |
| `RsbP` | `bis_runs_pitcher_sb` | BIS Pitcher SB Runs Above Avg - The number of runs above or below average the pitcher was worth based on baserunner kills and baserunner advances. - Provided by Baseball Info Solutions |
| `RszC` | `bis_runs_catcher_sz` | BIS Catcher Strike Zone Runs Above Avg - The number of runs above or below average the catcher was worth based on catcher framing. - Provided by Baseball Info Solutions |
| `Rthrow` | `bis_runs_throwing` | BIS Infield Throwing Runs Above Avg - The number of runs above or below average the player was worth based on how he completes the play given where he fielded the ball, how hard it was hit, and the speed of the runner. - Provided by Baseball Info Solutions |
| `Rtot` | `f_tz_runs_total` | Total Zone Total Fielding Runs Above Avg - The number of runs above or below average the player was worth based on the number of plays made. - This number combines the R tz , R dp , R of , R catch numbers into a total defensive contribution. - See the gloss... |
| `Rtot/yr` | `f_tz_runs_total_per_year` | Total Zone Total Fielding Runs Above Avg per 1,200 Inn - The number of runs above or below average the fielder was worth per 1,200 Innings (approx 135 games). - This number combines the R tz , R dp , R of , R catch numbers into a total defensive contributio... |
| `Rtz` | `tz_runs_field` | Total Zone Fielding Runs Above Avg - The number of runs above or below average the player was worth based on fielding plays made. - This number does not include OF kills, or double plays turned. - See the glossary section for a more complete explanation. -... |
| `SB2` | `SB_2` | Steals of 2nd Base |
| `SB3` | `SB_3` | Steals of 3rd Base |
| `SBH` | `SB_H` | Steals of Home |
| `SBlev` | `SB_leverage` | Stolen Base Leverage Index - The importance of the context in which the base was stolen - Above one means higher than average pressure. - Below one means lower than average pressure. |
| `SBO` | `SB_opp` | Stolen Base Opportunities - Plate appearances through which a runner was on first or second with the next base open. |
| `Tag` | `PO_tag` | Putouts where the runner was tagged. - Does not include tagging a batter or runner when a force is still possible. |
| `Thr` | `E_throw` | Errors on throws. |
| `Tm` | `team_ID` | Teams played for in this rookie season given players can have multiple seasons as a rookie |
| `Tot` | `PO_tot` | Total Putouts |
| `Tot_2` | `A_tot` | Total Assists |
| `Tot_3` | `E_tot` | Total Errors |
| `Tot_4` | `DP_tot` | Total Double Plays - Note that the types of DPs listed after this column - will likely not total this value - as there are assorted other double plays not listed separately. |
| `XI` | `XI` | Catcher Interference - Times a batter reached due to catcher’s interference. |

#### Team, standings and season context

58 fields.

| Field | Source code | Meaning |
| --- | --- | --- |
| `#A-S` | `team_allstars` | All-Stars - Number of Players who were named to the All-Star game in this season |
| `#a-tA-S` | `team_allstars_alltime` | All-time All-Stars - Number of Players on team who were named to the All-Star game at some point in their careers. Includes AL vs NL and East vs West All-Star games. |
| `#HOF` | `team_hofers` | Hall of Famers - Number of Players currently in the Hall of Fame |
| `1 Day` | `ppr_change_1day` | Change in postseason odds since yesterday |
| `1Run` | `record_one_run` | Win-loss record in one-run games. |
| `30 Days` | `ppr_change_30day` | Change in postseason odds since 30 days ago |
| `7 Days` | `ppr_change_7day` | Change in postseason odds since 7 days ago |
| `<.500` | `record_vs_under_500` | Win-loss record against teams that finished below .500. |
| `Attend/G` | `attendance_per_game` | Attend/G - Typically, tickets sold per home game. - Also, all single-admission doubleheaders are counted only once in the attendance total and a zero is used for the other game of the doubleheader. Both games are counted in the denominator. |
| `BatAge` | `age_bat` | Batters’ average age - Weighted by AB + Games Played |
| `BPF` | `bpf` | Batting Park Factor - 100 - Neutral - < 100 - Favors Pitchers - > 100 - Favors Batters. |
| `Bye` | `ppr_bye` | Earned first round bye |
| `Chall` | `challenges` | Manager Challenges using instant replay. |
| `D` | `division` | Division |
| `Div` | `ppr_division` | Won Division |
| `Division Winner` | `ppr_div_win_1` | Division Winner |
| `Division Winner_2` | `ppr_div_win_2` | Division Winner |
| `Est. Payroll` | `payroll` | These values may not include every bonus the team paid in a season, - or players called up or acquired mid-season. |
| `ExInn` | `record_xinn` | Win-loss record in extra-inning games. |
| `Home` | `record_home` | Win-loss record at home. |
| `Inter` | `record_interleague` | Win-loss record in interleague play. |
| `L_2` | `ppr_rem_l` | Average Remaining Losses |
| `L_3` | `ppr_avg_l` | Average Losses |
| `LCS` | `ppr_LCS` | Reached LCS |
| `LDS` | `ppr_LDS` | Reached LDS |
| `Luck` | `luck_pythag` | Pythagorean Luck - The difference between the actual W-L and Pythagorean W-L. |
| `Managers` | `managers` | Manager(s) used during the season. |
| `PAge` | `age_pit` | Pitchers’ average age - Weighted by 3*GS + G + SV |
| `Pennant` | `ppr_WS` | Reached World Series |
| `Post` | `ppr_postseason` | Made Postseason |
| `PPF` | `ppf` | Pitching Park Factor - 100 - Neutral - < 100 - Favors Pitchers - > 100 - Favors Batters. |
| `ppr_wc_4` | `ppr_wc_4` | Probability of finishing as the fourth wild card. |
| `ppr_wc_5` | `ppr_wc_5` | Probability of finishing as the fifth wild card. |
| `pythWL` | `record_pythag` | Pythagorean Win-Loss - Expected Win-Loss record based on the number of runs scored - and allowed by the team. |
| `Rdiff` | `run_diff` | Run Differential - Runs Scored - Runs Allowed - May be overall or per game |
| `rk` | `rk` | Rank. |
| `Road` | `record_road` | Win-loss record on the road. |
| `rSOS` | `ppr_opp_srs` | Strength of Remaining Schedule - Average SRS value of team's remaining opponents. |
| `SOS` | `strength_of_schedule` | Strength of Schedule - The number of runs per game their opponents are better (or worse) than the average team. - Average ML team for years with inter-league play and just their league for other years. |
| `SRS` | `simple_rating_system` | Simple Rating System - The number of runs per game they are better (or worse) than the average team. - Average ML team for years with inter-league play and just their league for other years. - SRS = Run Differential (R_diff) + Strength of Schedule (SOS) |
| `Stadium` | `stadium` | Stadium - Team’s home parks for that season. |
| `Succ` | `challenges_success` | Successful Manager Challenges using instant replay. |
| `Succ%` | `challenges_success_perc` | Percentage of Manager Challenges using instant replay Successful. |
| `Top Seed` | `ppr_top_seed` | Top Seeded Division Winner |
| `vCent` | `record_vs_central` | Win-loss record against Central division clubs. |
| `vEast` | `record_vs_east` | Win-loss record against East division clubs. |
| `vLHP` | `record_vs_lhp` | Win-loss record in games started by a left-handed pitcher. |
| `vRHP` | `record_vs_rhp` | Win-loss record in games started by a right-handed pitcher. |
| `vWest` | `record_vs_west` | Win-loss record against West division clubs. |
| `W_2` | `ppr_rem_w` | Average Remaining Wins |
| `W_3` | `ppr_avg_w` | Average Wins |
| `WC` | `ppr_wildcard` | Wild Card Team |
| `Wild Card` | `ppr_wc_1` | Wild Card Team |
| `Wild Card_2` | `ppr_wc_2` | Wild Card Team |
| `Wild Card_3` | `ppr_wc_3` | Wild Card Team |
| `Win WS` | `ppr_champs` | Won World Series |
| `Worst` | `ppr_worst` | 5th Percentile Wins |
| `≥.500` | `record_vs_over_500` | Win-loss record against teams that finished at or above .500. |

#### Game level: schedule, lineups and results

13 fields.

| Field | Source code | Meaning |
| --- | --- | --- |
| `Boxscore_URL` | `boxscore` | Direct link to the Baseball-Reference box score for that game. |
| `cLI` | `cli` | Championship Leverage Index - The importance of this game on the team's probability of winning the World Series (as calculated before the game). - 1.0 is average importance, below 1.0 is below average importance and above 1.0 is above average importance. |
| `D/N` | `day_or_night` | Day or Night Game - Determined by the start time of the game as stated by RetroSheet. - We rely on their designation here. |
| `Gm#` | `team_game` | Game Number - Which game out of all played by this team. |
| `Loss` | `losing_pitcher` | Pitcher charged with the loss. |
| `Orig. Scheduled` | `reschedule` | Originally Scheduled Game Date - If this is a makeup game, the original game date. The reason for the reschedule is in parentheses. |
| `RA` | `RA` | Runs Allowed |
| `Save` | `saving_pitcher` | Pitcher credited with the save; blank if none was awarded. |
| `Streak` | `win_loss_streak` | Win Loss Streak - + means a winning streak, - means a losing streak. |
| `Time` | `time_of_game` | Time of Game |
| `W-L` | `win_loss_record` | Win Loss Record - Team’s overall record after this game. |
| `W/L` | `win_loss_result` | Win/Loss/Tie - -wo indicates it was a walkoff win or loss. Based on available play-by-play; may be missing some walk-offs before 1969. |
| `Win` | `winning_pitcher` | Pitcher credited with the win. |

#### Roster, personnel and transactions

35 fields.

| Field | Source code | Meaning |
| --- | --- | --- |
| `1stYr` | `first_year` | First Year in Affiliated Baseball |
| `B` | `bats` | Batting Side - B or S - Switch Hitter - This is their primary designation for their career |
| `Batting` | `games_batting` | Games appeared in the batting order, - but may not have batted. |
| `Birth` | `flag` | Country of Birth |
| `Birthdate` | `birthdate` | Date of birth. |
| `Birthplace` | `birthplace` | Place of birth. |
| `C` | `games_at_c` | Games in lineup as a catcher |
| `CF` | `games_at_cf` | Games in lineup as a center fielder |
| `Defense` | `games_defense` | Games in lineup at a defensive position. |
| `DH` | `games_at_dh` | Games in lineup as a designated hitter |
| `DoB` | `date_of_birth` | Date of Birth |
| `Draft/Signing` | `draft` | Draft or signing details. |
| `End Date` | `end_date` | Last date of that coaching tenure within the season; blank if they finished the season in the role. |
| `Given Name` | `name_given` | Full given name at birth. |
| `High School` | `high_school` | High school attended. |
| `Ht` | `height` | Height (ft & inches) |
| `IL` | `is_dl` | Is on the Injured List |
| `Last Game` | `final_game` | Date of most recent Major League game. |
| `LF` | `games_at_lf` | Games in lineup as a left fielder |
| `OF` | `games_at_of` | Games in lineup as an outfielder |
| `OnActv` | `is_active` | Is on the Active Roster |
| `P` | `games_at_p` | Games in lineup or announced as a pitcher |
| `PH` | `games_at_ph` | Games in lineup as a pinch hitter - May have played another position as well. |
| `POS` | `POS` | Whether the player is a Pitcher or a Position player. |
| `PR` | `games_at_pr` | Games in lineup as a pinch runner - May have played another position as well. |
| `RF` | `games_at_rf` | Games in lineup as a right fielder |
| `Role` | `coach_type` | Coaching role, e.g. Manager, Pitching Coach, Bench Coach. |
| `Schools` | `school` | College or school attended. |
| `SS` | `games_at_ss` | Games in lineup as a shortstop |
| `Start Date` | `start_date` | First date of that coaching tenure within the season. |
| `T` | `throws` | Throwing Hand |
| `To Team` | `to_team_ID` | Club the player signed with. |
| `Uni` | `uniform_number` | Uniform Number |
| `Wt` | `weight` | Weight in Pounds |
| `Yrs` | `experience` | Experience - Years the player was/has been in the major leagues. - 1st indicates their first year in the majors, - but does not indicate rookie status. - Includes parts of any seasons. |

#### Managers

26 fields.

| Field | Source code | Meaning |
| --- | --- | --- |
| `Att_2` | `steal_3b_attempts` | Attempts to steal third base - Times a runner stole or was caught stealing third base. |
| `Att_3` | `sac_bunts` | Sacrifice bunts by non-pitchers |
| `Ch_2` | `steal_3b_chances` | Chances to steal third base - Plate appearances with a runner on second and no runner on third. |
| `Ch_3` | `sac_bunt_chances` | Chances to sacrifice bunt - Plate appearances with a runner on first and no runner on second, or a runner on second and no runner on third, and a non-pitcher at the plate. |
| `Challenges` | `mgr_challenge_count` | Replay Challenges - The replay system was introduced in the 2014 season. |
| `Ejections` | `mgr_ejections` | Manager Ejections - Only includes ejections as manager. Excludes ejections as a player or as a coach. |
| `Lpost` | `L_post` | Postseason Losses |
| `Mgr` | `manager` | Manager. |
| `Overturn%` | `mgr_replay_success_rate` | Successful Replay Challenge Percentage - The replay system was introduced in the 2014 season. - Managers must have 10 challenges to qualify for leaderboards. |
| `Overturned` | `mgr_overturn_count` | Successful Replay Challenges - The replay system was introduced in the 2014 season. |
| `P/G` | `pitchers_used_per_game` | Pitchers Used Per Game |
| `P/G+` | `pitchers_used_per_game_plus` | League-adjusted Pitchers Used Per Game - 100*(Pitchers per game)/(League pitchers per game) |
| `PH/G` | `pinch_hitters` | Pinch Hitters Used Per Game |
| `PH/G+` | `pinch_hitters_plus` | League-adjusted Pinch Hitters Used Per Game - 100*(Pinch hitters per game)/(League pinch hitters per game) |
| `PR/G` | `pinch_runners` | Pinch Runners Used Per Game |
| `PR/G+` | `pinch_runners_plus` | League-adjusted Pinch Runners Used Per Game - 100*(Pinch runners per game)/(League pinch runners per game) |
| `Rate` | `steal_2b_rate` | Rate of attempting to steal second base - Attempts to steal second base divided by chances to steal second base. |
| `Rate+` | `steal_2b_rate_plus` | League-adjusted steal of 2nd rate - 100*(Steal 2nd Rate)/(League Steal 2nd Rate) |
| `Rate+_2` | `steal_3b_rate_plus` | League-adjusted steal of 3rd rate - 100*(Steal 3rd Rate)/(League Steal 3rd Rate) |
| `Rate+_3` | `sac_bunt_rate_plus` | League-adjusted sac bunt rate - 100*(Sac Bunt Rate)/(League Sac Bunt Rate) |
| `Rate+_4` | `ibb_rate_plus` | League-adjusted IBB rate - 100*(IBB Rate)/(League IBB Rate) |
| `Rate_2` | `steal_3b_rate` | Rate of attempting to steal third base - Attempts to steal third base divided by chances to steal third base. |
| `Rate_3` | `sac_bunt_rate` | Rate of attempting a sacrifice bunt - Sacrifice bunts divided by chances to sacrifice. Does not account for unsuccessful attempts (foul bunts, missed bunts). |
| `Rate_4` | `ibb_rate` | Rate of issuing intentional walks - Intentional walks divided by plate apparances. |
| `W-L%post` | `win_loss_perc_post` | Postseason Win-Loss Percentage - W / (W + L). |
| `Wpost` | `W_post` | Postseason Wins |

#### Awards and voting

11 fields.

| Field | Source code | Meaning |
| --- | --- | --- |
| `1st Place` | `votes_first` | Number of first-place votes received. |
| `BB_2` | `BB_p` | Bases on Balls/Walks |
| `Finish` | `finish` | Team’s Finish - For career totals these are the average of all - years weighted by the number games played or managed. |
| `G_2` | `G_p` | Games Played or Pitched |
| `H_2` | `H_p` | Hits/Hits Allowed |
| `HR_2` | `HR_p` | Home Runs Hit/Allowed |
| `Rank` | `rank` | Position in the division standings after that game. |
| `Share` | `share` | Awards Share - Vote Pts/Max Pts Possible - Unanimous choice would be 100%. |
| `Stats` | `stats` | Baseball-Reference link label for the related stats page. |
| `Ties` | `ties` | Ties - Prior to lights and tarps it was common for games - to be called on account of darkness or rain - and then replayed in full at a later date. - Game stats from ties still counted. - Some leagues also do not play unlimited numbers of innings. |
| `Vote Pts` | `points_won` | MVP is currently 14-9-8-...-3-2-1 - Others are currently 5-3-1. |


### Notes and caveats

- **2020 was a 60-game season.** COVID-shortened, so 2020 counting stats are roughly 37% of a
  normal year. Compare rates, not totals. Attendance is blank for 2020 because games were
  played without spectators.
- **Three franchises changed code inside this window.** The Marlins are `FLA` for 2007-2011 and `MIA` from 2012; the Rays are `TBD` in 2007 and `TBR` from 2008; the Athletics are `OAK` through 2024 and `ATH` from 2025. Each pair is one franchise - group them together to trend across the full period.
- **The Astros switched leagues in 2013**, moving from the NL Central to the AL West. `League` and `Division` are read per team-season, so the data is correct, but any league-level aggregation across the era has to expect Houston to change sides.
- **The postseason field changed size repeatedly**: 8 teams 2007-2011, 10 from 2012 when the wild card game arrived, 16 in the expanded 2020 season, 10 again in 2021, and 12 from 2022. Postseason counting stats are not comparable across those formats.
- **The designated hitter was not universal until 2022.** Before that (2020 excepted) National League pitchers batted, which depresses NL team batting lines and inflates pitcher plate appearances relative to the AL.
- **Older Athletics seasons.** `OAK` for 2020-2024, `ATH` from 2025, when the club
  left Oakland. Same franchise - treat them as one to trend across all six seasons.
- **`Current_40_Man_Roster` is a snapshot, not history.** Baseball-Reference publishes a 40-man
  roster only for the *current* season. What is here is the live 40-man for all 30 clubs as of
  the build date, marked `Season = 2026`. It also lists injured-list players who do not count
  against the 40; filter to a blank `IL` for the true 40-man. For historical roster composition
  use `Full_Season_Roster`.
- **Playoff files only cover teams that qualified.** Clubs that missed the postseason have no rows.
- **There is no postseason Value Batting / Value Pitching.** Baseball-Reference does not publish
  WAR-based value tables for postseason play.
- **Game-level names are surnames only.** `Batting_Orders` and `Defensive_Lineups` print
  surnames as they appear in the grid, so join on `Player_ID`, which is captured in full.
- **Blank cells mean "not applicable", not zero.**

### What is not here

- **Player splits** (monthly, platoon, home/away by player) are disallowed by
  Baseball-Reference's `robots.txt`, which blocks `/players/split.cgi`, `/teams/split.cgi` and
  `/leagues/split.cgi`. They were not collected.
- **Statcast metrics** (exit velocity, barrel rate, sprint speed) are not published by
  Baseball-Reference; they come from Baseball Savant, a separate source.
- **Transaction types are not classified.** `Transactions` captures the full text with players
  and clubs linked out, but does not label a row as a trade, signing or IL move.
- **Baseball-Reference's "Team Output" table was skipped.** Its cells concatenate a team name
  and a value into one string, so it cannot be parsed into tidy columns.

### Method

Pages were fetched at a 3+ second crawl delay, honouring the `Crawl-delay: 3` directive
in the site's `robots.txt`; only `/teams/`, `/leagues/` and `/awards/` paths were requested,
none of which robots.txt disallows. Tables the site embeds inside HTML comments - fielding,
value, coaches, roster and most advanced tables - were extracted along with the visible ones.
Columns are keyed to Baseball-Reference's own `data-stat` codes, so the extraction is resilient
to display changes, and those codes are preserved in the data dictionary so any column can be
traced back to its source. Accented names are stored as proper UTF-8.

---

## Part 3 - Excel workbooks

Everything below describes the workbooks in `2_Excel_Workbooks/`, which are built from the CSVs above. The data caveats in [Notes and caveats](#notes-and-caveats) apply equally here.

The complete MLB dataset for 2020-2025 compiled into Excel: **108 datasets, 769,168 rows, 3,756 columns**, covering all 30 clubs across 19 seasons.

Nothing in the workbooks is unique to Excel. Every workbook is built from the CSVs in [`../1_Source_Data_CSV/`](1_Source_Data_CSV/) and verified sheet by sheet against them - every sheet matched row-for-row and column-for-column at build time.

| Reference | What it is |
| --- | --- |
| [`FIELD_REFERENCE.md`](2_Excel_Workbooks/FIELD_REFERENCE.md) | Every sheet, every column, with stat codes and definitions |
| [`../JOIN_DIAGRAM.svg`](JOIN_DIAGRAM.svg) | How the sheets join to each other |
| [`../JOIN_DIAGRAM_Detailed.svg`](JOIN_DIAGRAM_Detailed.svg) | Table-by-table detail: key fields, cardinality, exact join predicates |
| `Data_Dictionary` sheet | The same definitions, inside each workbook |

### The five workbooks

| Workbook | Sheets | Rows | Size | Covers |
| --- | ---: | ---: | ---: | --- |
| `MLB_Team_Data_2020-2025.xlsx` | 12 | 73,806 | 12 MB | Core regular-season data: batting, pitching, fielding, value/WAR, rosters, coaching staffs, schedules, standings |
| `MLB_Playoff_Data_2020-2025.xlsx` | 8 | 9,736 | 1 MB | Postseason batting, pitching, fielding, rosters, schedules and series results |
| `MLB_Advanced_Stats_2020-2025.xlsx` | 86 | 192,326 | 32 MB | Advanced, situational and league/team aggregates, award voting, transactions |
| `MLB_Game_Level_2020-2025.xlsx` | 2 | 493,300 | 32 MB | Batting orders and defensive lineups, one row per player per game |
| `MLB_Complete_Dataset_2020-2025.xlsx` | 108 | 769,168 | 78 MB | **All four above in one file** |

The four themed workbooks do not overlap - together they hold all 108 datasets exactly once. Complete Dataset duplicates all four, so take the themed set **or** Complete, never both.

### What is in each workbook

#### `MLB_Team_Data_2020-2025.xlsx`

12 data sheets, 73,806 rows, 12 MB. Plus a `Contents` sheet and a `Data_Dictionary` sheet.

| Sheet | Rows | Columns |
| --- | ---: | ---: |
| `Coaching_Staff` | 2,359 | 16 |
| `Current_40_Man_Roster` | 1,367 | 23 |
| `Full_Season_Roster` | 9,706 | 37 |
| `Schedule_Results` | 26,092 | 32 |
| `Standard_Batting` | 5,797 | 43 |
| `Standard_Fielding` | 10,332 | 38 |
| `Standard_Pitching` | 5,908 | 46 |
| `Standings` | 180 | 12 |
| `Standings_Expanded` | 180 | 32 |
| `Team_Season_Summary` | 180 | 27 |
| `Value_Batting` | 5,797 | 31 |
| `Value_Pitching` | 5,908 | 33 |

#### `MLB_Playoff_Data_2020-2025.xlsx`

8 data sheets, 9,736 rows, 1 MB. Plus a `Contents` sheet and a `Data_Dictionary` sheet.

| Sheet | Rows | Columns |
| --- | ---: | ---: |
| `Postseason_Advanced_Batting` | 1,840 | 27 |
| `Postseason_Advanced_Pitching` | 862 | 31 |
| `Postseason_Batting` | 1,908 | 38 |
| `Postseason_Fielding` | 1,772 | 30 |
| `Postseason_Pitching` | 930 | 43 |
| `Postseason_Roster` | 1,834 | 37 |
| `Postseason_Schedule_Results` | 522 | 27 |
| `Postseason_Series_Results` | 68 | 13 |

#### `MLB_Advanced_Stats_2020-2025.xlsx`

86 data sheets, 192,326 rows, 32 MB. Plus a `Contents` sheet and a `Data_Dictionary` sheet.

| Sheet | Rows | Columns |
| --- | ---: | ---: |
| `Advanced_Batting` | 6,062 | 39 |
| `Advanced_Fielding_1B` | 1,161 | 47 |
| `Advanced_Fielding_2B` | 1,144 | 46 |
| `Advanced_Fielding_3B` | 1,139 | 44 |
| `Advanced_Fielding_C` | 712 | 42 |
| `Advanced_Fielding_CF` | 1,106 | 52 |
| `Advanced_Fielding_C_Baserunning` | 712 | 33 |
| `Advanced_Fielding_LF` | 1,562 | 52 |
| `Advanced_Fielding_P` | 5,734 | 37 |
| `Advanced_Fielding_RF` | 1,452 | 52 |
| `Advanced_Fielding_SS` | 827 | 47 |
| `Advanced_Pitching` | 6,341 | 33 |
| `Awards_And_Honors` | 23 | 12 |
| `Baserunning_Batting` | 5,217 | 46 |
| `Basesituation_Pitching` | 6,369 | 47 |
| `Batting_Pitching` | 6,405 | 40 |
| `Cumulative_Batting` | 9,483 | 38 |
| `Cumulative_Pitching` | 5,809 | 43 |
| `Cy_Young_Voting` | 128 | 40 |
| `Debuts_Batting` | 1,545 | 35 |
| `Debuts_Bio` | 1,539 | 27 |
| `Debuts_Pitching` | 983 | 41 |
| `Free_Agent_Batting` | 256 | 32 |
| `Free_Agent_Pitching` | 444 | 36 |
| `Free_Agent_Signings` | 2,457 | 41 |
| `MVP_Voting` | 266 | 40 |
| `Manager_Of_The_Year_Voting` | 81 | 21 |
| `Manager_Record` | 201 | 25 |
| `Manager_Tendencies` | 201 | 36 |
| `Neutral_Batting` | 4,303 | 32 |
| `Neutral_Pitching` | 5,101 | 33 |
| `Opening_Day_Lineups` | 180 | 21 |
| `Pitches_Batting` | 5,190 | 43 |
| `Pitches_Pitching` | 6,369 | 44 |
| `Playoff_Odds` | 216 | 33 |
| `Playoff_Scenarios` | 12 | 17 |
| `Ratio_Batting` | 5,190 | 30 |
| `Ratio_Pitching` | 6,405 | 32 |
| `Reliever_Pitching` | 5,284 | 45 |
| `Rookie_Of_The_Year_Voting` | 105 | 40 |
| `Rookies_Batting` | 1,337 | 36 |
| `Rookies_Pitching` | 885 | 42 |
| `Sabermetric_Batting` | 6,174 | 37 |
| `Situational_Batting` | 5,190 | 52 |
| `Standard_Fielding_By_Position` | 18,324 | 53 |
| `Starter_Pitching` | 2,508 | 47 |
| `Team_Advanced_Batting` | 192 | 31 |
| `Team_Advanced_Fielding_1B` | 192 | 43 |
| `Team_Advanced_Fielding_2B` | 192 | 42 |
| `Team_Advanced_Fielding_3B` | 192 | 40 |
| `Team_Advanced_Fielding_C` | 192 | 38 |
| `Team_Advanced_Fielding_CF` | 192 | 48 |
| `Team_Advanced_Fielding_C_Baseru` *(`Team_Advanced_Fielding_C_Baserunning`)* | 192 | 29 |
| `Team_Advanced_Fielding_LF` | 192 | 48 |
| `Team_Advanced_Fielding_P` | 192 | 33 |
| `Team_Advanced_Fielding_RF` | 192 | 48 |
| `Team_Advanced_Fielding_SS` | 192 | 43 |
| `Team_Advanced_Pitching` | 192 | 26 |
| `Team_Appearances` | 180 | 27 |
| `Team_Attendance` | 186 | 15 |
| `Team_Baserunning_Batting` | 192 | 41 |
| `Team_Basesituation_Pitching` | 192 | 42 |
| `Team_Batting_Pitching` | 192 | 35 |
| `Team_Fielding_By_Position` | 1,920 | 48 |
| `Team_Miscellaneous` | 180 | 26 |
| `Team_Pitches_Batting` | 192 | 39 |
| `Team_Pitches_Pitching` | 192 | 39 |
| `Team_Pitching_Staffs` | 180 | 20 |
| `Team_Ratio_Batting` | 192 | 25 |
| `Team_Ratio_Pitching` | 192 | 27 |
| `Team_Reliever_Pitching` | 192 | 39 |
| `Team_Sabermetric_Batting` | 192 | 31 |
| `Team_Situational_Batting` | 192 | 47 |
| `Team_Standard_Batting` | 192 | 37 |
| `Team_Standard_Fielding` | 192 | 27 |
| `Team_Standard_Pitching` | 192 | 44 |
| `Team_Starter_Pitching` | 192 | 41 |
| `Team_Starting_Lineups` | 180 | 20 |
| `Team_Value_Batting` | 186 | 27 |
| `Team_Value_Pitching` | 186 | 29 |
| `Team_Win_Probability_Batting` | 192 | 30 |
| `Team_Win_Probability_Pitching` | 192 | 31 |
| `Transactions` | 20,428 | 8 |
| `Uniform_Numbers` | 9,602 | 9 |
| `Win_Probability_Batting` | 5,185 | 35 |
| `Win_Probability_Pitching` | 6,405 | 36 |

#### `MLB_Game_Level_2020-2025.xlsx`

2 data sheets, 493,300 rows, 32 MB. Plus a `Contents` sheet and a `Data_Dictionary` sheet.

| Sheet | Rows | Columns |
| --- | ---: | ---: |
| `Batting_Orders` | 234,828 | 18 |
| `Defensive_Lineups` | 258,472 | 17 |

#### `MLB_Complete_Dataset_2020-2025.xlsx`

All 108 sheets listed above, in one file, plus `Contents` and `Data_Dictionary`. At 78 MB it is slow to open and will use several GB of memory; prefer a themed workbook, or the CSVs, unless you specifically need everything in one place.

### How every workbook is built

- **`Contents`** is the first sheet: every sheet in that workbook with its row and column count, so you can see the shape of the file before opening anything.
- **`Data_Dictionary`** is the last sheet: every column in that workbook with its Baseball-Reference stat code and definition, filtered to just that workbook's datasets.
- **Row 1 is frozen** on every sheet, so headers stay visible when scrolling.
- **AutoFilter is on** for every sheet, so each column has a filter dropdown immediately.
- **Column widths are fitted** to the content, capped so wide text columns do not push the sheet off screen.

### Sheet naming

Sheet names match the CSV filenames exactly, with one exception: Excel caps a sheet name at 31 characters.

| Dataset | Sheet name | Why |
| --- | --- | --- |
| `Team_Advanced_Fielding_C_Baserunning` | `Team_Advanced_Fielding_C_Baseru` | 36 characters, over the 31-character limit |

The data in that sheet is complete and identical to the CSV - only the label is shortened.

### Working with these in Excel

#### Filter `Row_Type` before you total anything

102 of the 108 sheets carry a `Row_Type` column. Baseball-Reference ends its player tables with footer rows - *Team Totals*, *Non-Pitcher Totals*, *Rank in 2 AL* - and those rows are preserved here because they are useful, but they sit in the same sheet as the players. Any sum, average or pivot that does not exclude them counts the team twice: once as the players, once as the total.

Set the `Row_Type` filter to `data` first, or add `Row_Type = "data"` as a report filter in a pivot table.

#### Pivot tables

Each sheet is a clean rectangular range with a header row, so `Ctrl+T` will turn any sheet into a table and pivot cleanly. `Season`, `Team`, `League` and `Division` are on nearly every sheet and make natural row or filter fields.

#### Joining sheets

There are no lookup tables - every sheet carries its own identifiers. To combine sheets, match on:

- `Season` + `Team` for anything team-level
- `Season` + `Team` + `Player_ID` for player-level
- add `Position` for the per-position fielding sheets
- `Season` + `Team` + `Gm#`/`Game_Num` for game-level

For more than a couple of sheets, Power Query (Data > Get Data) handles this far better than `XLOOKUP` across 800,000-row sheets. [`../JOIN_DIAGRAM_Detailed.svg`](JOIN_DIAGRAM_Detailed.svg) sets out the full picture, including the grain of each group and the traps.

#### Watch the grain when combining

Joining a player-season sheet to a team-season sheet is many-to-one and safe. Joining two sheets at different grains without aggregating first multiplies rows - the usual way a total comes out several times too large.

### Size and limits

| Largest sheets | Rows | Share of Excel's 1,048,576-row limit |
| --- | ---: | ---: |
| `Defensive_Lineups` | 258,472 | 25% |
| `Batting_Orders` | 234,828 | 22% |
| `Schedule_Results` | 26,092 | 2% |

No sheet exceeds the limit, so nothing is split - each workbook is a single file covering all 19 seasons. `Defensive_Lineups` is the one to watch: it grows by around 48,000 rows a season, so it would cross the limit in roughly four more seasons.

The trade-off for keeping them whole is size. Advanced Stats and Game Level are around 100 MB each and Complete Dataset is 252 MB - slow to open, heavy on memory, and too large to attach to most email. **If you are loading this into Tableau, Power BI, Python, R or a database, use the CSVs instead**: they are faster, smaller and do not have the row ceiling.

---

## Attribution

Data is sourced from Baseball-Reference.com, a Sports Reference LLC property, and
remains their copyright. **No open licence is granted or implied here.** When sharing this
dataset or anything derived from it, credit **Baseball-Reference.com** as the source, and
consult Sports Reference about commercial use or redistribution.
