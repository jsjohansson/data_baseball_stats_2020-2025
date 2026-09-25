# Field reference - Excel workbooks

Every sheet in every workbook, with each column, the Baseball-Reference stat code behind it and the definition the site gives. Generated 2026-09-25 from the workbooks and their source data, so it matches the files exactly.

**108 sheets across 4 themed workbooks, 769,168 data rows, 3,756 columns documented.**

`MLB_Complete_Dataset_2020-2025.xlsx` contains all 108 of these sheets in one file - the same sheets, the same columns - so it is not repeated below.

## Sheet names

Excel caps a sheet name at 31 characters. One dataset in this collection exceeds that, so its sheet name is shortened. Everything else keeps its full name, identical to the CSV filename.

| Dataset (CSV name) | Sheet name in Excel |
| --- | --- |
| `Team_Advanced_Fielding_C_Baserunning` | `Team_Advanced_Fielding_C_Baseru` |

---

## Team Data

Workbook: `MLB_Team_Data_2020-2025.xlsx` - 12 sheets, 73,806 rows.

### Coaching_Staff

2,359 rows, 16 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Birth` | `flag` | Country of Birth |
| `DoB` | `date_of_birth` | Date of Birth |
| `Role` | `coach_type` | Coaching role, e.g. Manager, Pitching Coach, Bench Coach. |
| `Start Date` | `start_date` | First date of that coaching tenure within the season. |
| `End Date` | `end_date` | Last date of that coaching tenure within the season; blank if they finished the season in the role. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. Holds the coach's id on Coaching_Staff. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. Filter to 'data' for player-level analysis. |

### Current_40_Man_Roster

1,367 rows, 23 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Uni` | `uniform_number` | Uniform Number |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Birth` | `flag` | Country of Birth |
| `POS` | `POS` | Whether the player is a Pitcher or a Position player. |
| `OnActv` | `is_active` | Is on the Active Roster |
| `IL` | `is_dl` | Is on the Injured List |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `B` | `bats` | Batting Side - B or S - Switch Hitter - This is their primary designation for their career |
| `T` | `throws` | Throwing Hand |
| `Ht` | `height` | Height (ft & inches) |
| `Wt` | `weight` | Weight in Pounds |
| `DoB` | `date_of_birth` | Date of Birth |
| `1stYr` | `first_year` | First Year in Affiliated Baseball |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. Holds the coach's id on Coaching_Staff. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. Filter to 'data' for player-level analysis. |

### Full_Season_Roster

9,706 rows, 37 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank |
| `Player` | `name_display` | Player name. Baseball-Reference handedness markers have been stripped out into the Bats/Throws column. |
| `Age` | `age` | As of June 30 of the season in question. |
| `Birth` | `birth_country_and_flag` | Country of Birth |
| `B` | `bats` | Batting Side - B or S - Switch Hitter - This is their primary designation for their career |
| `T` | `throws` | Throwing Hand |
| `Ht` | `height` | Height (ft & inches) |
| `Wt` | `weight` | Weight in Pounds |
| `DoB` | `dob` | Date of Birth |
| `Yrs` | `experience` | Experience - Years the player was/has been in the major leagues. - 1st indicates their first year in the majors, - but does not indicate rookie status. - Includes parts of any seasons. |
| `G` | `games_all` | All games played |
| `GS` | `games_started_all` | Games Started |
| `Batting` | `games_batting` | Games appeared in the batting order, - but may not have batted. |
| `Defense` | `games_defense` | Games in lineup at a defensive position. |
| `P` | `games_at_p` | Games in lineup or announced as a pitcher |
| `C` | `games_at_c` | Games in lineup as a catcher |
| `1B` | `games_at_1b` | Games in lineup as a first baseman |
| `2B` | `games_at_2b` | Games in lineup as a second baseman |
| `3B` | `games_at_3b` | Games in lineup as a third baseman |
| `SS` | `games_at_ss` | Games in lineup as a shortstop |
| `LF` | `games_at_lf` | Games in lineup as a left fielder |
| `CF` | `games_at_cf` | Games in lineup as a center fielder |
| `RF` | `games_at_rf` | Games in lineup as a right fielder |
| `OF` | `games_at_of` | Games in lineup as an outfielder |
| `DH` | `games_at_dh` | Games in lineup as a designated hitter |
| `PH` | `games_at_ph` | Games in lineup as a pinch hitter - May have played another position as well. |
| `PR` | `games_at_pr` | Games in lineup as a pinch runner - May have played another position as well. |
| `Awards` | `awards` | Awards and honours for that season as listed by Baseball-Reference (e.g. AS = All-Star, MVP-1 = MVP winner). |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. Holds the coach's id on Coaching_Staff. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. Filter to 'data' for player-level analysis. |

### Schedule_Results

26,092 rows, 32 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Gm#` | `team_game` | Game Number - Which game out of all played by this team. |
| `Date` | `date_game` | A number in parentheses indicates which game of a doubleheader. - Click dates for box scores of games or standings on this day. |
| `Game_Date` | `identifier/derived` | ISO (YYYY-MM-DD) game date derived from the display Date column. |
| `Doubleheader_Game` | `identifier/derived` | Game 1 or 2 of a doubleheader; blank for single games. |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `Home_Away` | `identifier/derived` | Whether the team was Home or Away, derived from Baseball-Reference's '@' marker. |
| `Opp` | `opp_ID` | Opponent franchise code. |
| `Boxscore_URL` | `boxscore` | Direct link to the Baseball-Reference box score for that game. |
| `W/L` | `win_loss_result` | Win/Loss/Tie - -wo indicates it was a walkoff win or loss. Based on available play-by-play; may be missing some walk-offs before 1969. |
| `R` | `R` | Runs Scored/Allowed |
| `RA` | `RA` | Runs Allowed |
| `Inn` | `extra_innings` | Innings - Only shown if something other than 9 innings were played. |
| `W-L` | `win_loss_record` | Win Loss Record - Team’s overall record after this game. |
| `Rank` | `rank` | Position in the division standings after that game. |
| `GB` | `games_back` | Games Back of Division/League Leader - Computed as games over .500 of leader (W-L) minus games over .500 of team divided by two. - Typically computed at the end of play for a particular day. - Blank for 1st game of DH. |
| `Win` | `winning_pitcher` | Pitcher credited with the win. |
| `Loss` | `losing_pitcher` | Pitcher charged with the loss. |
| `Save` | `saving_pitcher` | Pitcher credited with the save; blank if none was awarded. |
| `Time` | `time_of_game` | Time of Game |
| `D/N` | `day_or_night` | Day or Night Game - Determined by the start time of the game as stated by RetroSheet. - We rely on their designation here. |
| `Attendance` | `attendance` | Attendance - Typically, tickets sold in home games. |
| `cLI` | `cli` | Championship Leverage Index - The importance of this game on the team's probability of winning the World Series (as calculated before the game). - 1.0 is average importance, below 1.0 is below average importance and above 1.0 is above average importance. |
| `Streak` | `win_loss_streak` | Win Loss Streak - + means a winning streak, - means a losing streak. |
| `Orig. Scheduled` | `reschedule` | Originally Scheduled Game Date - If this is a makeup game, the original game date. The reason for the reschedule is in parentheses. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. Filter to 'data' for player-level analysis. |

### Standard_Batting

5,797 rows, 43 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank |
| `Player` | `name_display` | Player name. Baseball-Reference handedness markers have been stripped out into the Bats/Throws column. |
| `Bats` | `derived` | Batting hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | As of June 30 of the season in question. |
| `Pos` | `team_position` | Position |
| `WAR` | `b_war` | Wins Above Replacement for position players - A single number that presents the number of wins the player added - to the team above what a replacement player (think AAA or AAAA) would add. - Scale: 8+ MVP Quality, 5+ All-Star Quality, 2+ Starter, - 0-2 Reserve, < 0 Replacement Level - Developed by Sean Smith of BaseballProjection.com |
| `G` | `b_games` | Games Played |
| `PA` | `b_pa` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `AB` | `b_ab` | At Bats |
| `R` | `b_r` | Runs Scored |
| `H` | `b_h` | Hits |
| `2B` | `b_doubles` | Doubles |
| `3B` | `b_triples` | Triples |
| `HR` | `b_hr` | Home Runs |
| `RBI` | `b_rbi` | Runs Batted In |
| `SB` | `b_sb` | Stolen Bases |
| `CS` | `b_cs` | Caught Stealing |
| `BB` | `b_bb` | Bases on Balls/Walks |
| `SO` | `b_so` | Strikeouts |
| `BA` | `b_batting_avg` | Hits/At Bats - For recent years, leaders need 3.1 PA - per team game played - Bold indicates either highest BA using current stats - or awarded title at end of year. |
| `OBP` | `b_onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) - For recent years, leaders need 3.1 PA - per team game played |
| `SLG` | `b_slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `OPS` | `b_onbase_plus_slugging` | On-Base + Slugging Percentages - For recent years, leaders need 3.1 PA - per team game played |
| `OPS+` | `b_onbase_plus_slugging_plus` | OPS+ - 100*[OBP/lg OBP + SLG/lg SLG - 1] - Adjusted to the player’s ballpark(s) |
| `rOBA` | `b_roba` | rOBA - A measure of a player's offensive contributions, weighted in proportion to each event's actual run value |
| `Rbat+` | `b_rbat_plus` | Rbat+ - Batting runs as computed for WAR, but indexed to the environment the player played in, where 100 is league average. |
| `TB` | `b_tb` | Total Bases - Singles + 2 x Doubles + 3 x Triples + 4 x Home Runs. |
| `GIDP` | `b_gidp` | Double Plays Grounded Into - Only includes standard 6-4-3, 4-3, etc. double plays. - First tracked in 1933. - For gamelogs only in seasons we have play-by-play, we include triple plays as well. - All official seasonal totals do not include GITP's. |
| `HBP` | `b_hbp` | Times Hit by a Pitch |
| `SH` | `b_sh` | Sacrifice Hits (Sacrifice Bunts) |
| `SF` | `b_sf` | Sacrifice Flies - First tracked in 1955. |
| `IBB` | `b_ibb` | Intentional Bases on Balls - First tracked in 1955. |
| `Pos_2` | `pos` | Positions Played - Positions are listed in order of games played at each. - * indicates the player appeared in at least 2/3rds of team games at that position (applies to a single season or a career total). - Positions after / indicate fewer than ten games played there. - 'H' indicates games as a pinch-hitter or pinch-runner. |
| `Awards` | `awards` | Awards and honours for that season as listed by Baseball-Reference (e.g. AS = All-Star, MVP-1 = MVP winner). |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. Holds the coach's id on Coaching_Staff. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. Filter to 'data' for player-level analysis. |

### Standard_Fielding

10,332 rows, 38 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank |
| `Player` | `name_display` | Player name. Baseball-Reference handedness markers have been stripped out into the Bats/Throws column. |
| `Age` | `age` | As of June 30 of the season in question. |
| `G` | `f_games_distinct` | Games Played |
| `GS` | `f_games_started` | Games Started |
| `CG` | `f_cg` | Complete Games at a Single Position |
| `Inn` | `f_innings` | Innings Played at Position |
| `Ch` | `f_chances` | Defensive Chances - Putouts + Assists + Errors |
| `PO` | `f_po` | Putouts |
| `A` | `f_assists` | Assists |
| `E` | `f_errors` | Errors Committed |
| `DP` | `f_dp` | Double Plays Turned |
| `Fld%` | `f_fielding_perc` | Fielding Percentage - (Putouts + Assists) / (Putouts + Assists + Errors) |
| `Rtot` | `f_tz_runs_total` | Total Zone Total Fielding Runs Above Avg - The number of runs above or below average the player was worth based on the number of plays made. - This number combines the R tz , R dp , R of , R catch numbers into a total defensive contribution. - See the glossary section for a more complete explanation. - Provided by BaseballProjection.com |
| `Rtot/yr` | `f_tz_runs_total_per_year` | Total Zone Total Fielding Runs Above Avg per 1,200 Inn - The number of runs above or below average the fielder was worth per 1,200 Innings (approx 135 games). - This number combines the R tz , R dp , R of , R catch numbers into a total defensive contribution. - See the glossary section for a more complete explanation. - Provided by BaseballProjection.com |
| `Rdrs` | `f_drs_total` | BIS Defensive Runs Saved Above Avg - The number of runs above or below average the player was worth based on their overall defense. - This number combines the R pm , R dp , and R good numbers into a total defensive contribution. - Provided by Baseball Info Solutions |
| `Rdrs/yr` | `f_drs_total_per_year` | BIS Defensive Runs Saved Above Avg per 1,200 Inn - The number of runs above or below average the fielder was worth per 1,200 Innings (approx 135 games). - This number combines the R pm , R dp , and R good numbers into a total defensive contribution. - For pitchers, this is set to 200 Innings. - Provided by Baseball Info Solutions |
| `RF/9` | `f_range_factor_per_nine` | Range Factor per 9 Inn - 9 * (Putouts + Assists) / Innings Played |
| `lgRF9` | `f_range_factor_per_nine_lg` | League Range Factor per 9 Inn - Average Range Factor the league - 9 * (Putouts + Assists) / Innings Played |
| `RF/G` | `f_range_factor_per_game` | Range Factor per Game - (Putouts + Assists) / Games Played |
| `lgRFG` | `f_range_factor_per_game_lg` | League Range Factor per Game - Average Range Factor for the league for chances per game - (Putouts + Assists) / Games Played |
| `PB` | `f_pb_catcher_only` | Passed Balls |
| `WP` | `f_wp_catcher_only` | Wild Pitches |
| `SB` | `f_sb_catcher_only` | Stolen Bases |
| `CS` | `f_cs_catcher_only` | Caught Stealing |
| `CS%` | `f_cs_perc_catcher_only` | Caught Stealing Percentage - CS / (SB + CS) |
| `Pick` | `f_pickoffs_catcher_only` | Pickoffs - Runner picked off a base. May include cases they were safe on an error. - Also includes Pickoff Caught Stealing plays. |
| `Pos` | `pos` | Positions Played - Positions are listed in order of games played at each. - * indicates the player appeared in at least 2/3rds of team games at that position (applies to a single season or a career total). - Positions after / indicate fewer than ten games played there. - 'H' indicates games as a pinch-hitter or pinch-runner. |
| `Awards` | `awards` | Awards and honours for that season as listed by Baseball-Reference (e.g. AS = All-Star, MVP-1 = MVP winner). |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. Holds the coach's id on Coaching_Staff. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. Filter to 'data' for player-level analysis. |

### Standard_Pitching

5,908 rows, 46 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank |
| `Player` | `name_display` | Player name. Baseball-Reference handedness markers have been stripped out into the Bats/Throws column. |
| `Throws` | `derived` | Throwing hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | As of June 30 of the season in question. |
| `Pos` | `team_position` | Position |
| `WAR` | `p_war` | Wins Above Replacement for Pitchers - A single number that presents the number of wins the player added - to the team above what a replacement player (think AAA or AAAA) would add. This value includes defensive support and includes additional value for high leverage situations. - Scale: 8+ MVP Quality, 5+ All-Star Quality, 2+ Starter, - 0-2 Reserve, < 0 Replacement Level - Developed by Sean Smith of BaseballProjection.com |
| `W` | `p_w` | Wins |
| `L` | `p_l` | Losses |
| `W-L%` | `p_win_loss_perc` | Win-Loss Percentage - W / (W + L) - For players, leaders need one decision for every ten team games. |
| `ERA` | `p_earned_run_avg` | 9 * ER / IP - For recent years, leaders need 1 IP - per team game played. - Bold indicates lowest ERA using current stats - Gold means awarded ERA title at end of year. |
| `G` | `p_g` | Games Pitched |
| `GS` | `p_gs` | Games Started |
| `GF` | `p_gf` | Games Finished |
| `CG` | `p_cg` | Complete Games |
| `SHO` | `p_sho` | Shutouts - No runs allowed and a complete game. |
| `SV` | `p_sv` | Saves |
| `IP` | `p_ip` | Innings Pitched |
| `H` | `p_h` | Hits Allowed |
| `R` | `p_r` | Runs Allowed |
| `ER` | `p_er` | Earned Runs Allowed |
| `HR` | `p_hr` | Home Runs Allowed |
| `BB` | `p_bb` | Bases on Balls/Walks |
| `IBB` | `p_ibb` | Intentional Bases on Balls - First tracked in 1955. |
| `SO` | `p_so` | Strikeouts |
| `HBP` | `p_hbp` | Times Hit by a Pitch |
| `BK` | `p_bk` | Balks |
| `WP` | `p_wp` | Wild Pitches |
| `BF` | `p_bfp` | Batters Faced |
| `ERA+` | `p_earned_run_avg_plus` | ERA+ - 100*[lgERA/ERA] - Adjusted to the player’s ballpark(s). |
| `FIP` | `p_fip` | Fielding Independent Pitching - this stat measures a pitcher's effectiveness at preventing HR, BB, HBP and causing SO - (13*HR + 3*(BB+HBP) - 2*SO)/IP + Constant lg - The constant is set so that each season major-league average FIP is the same as the major-league avg ERA |
| `WHIP` | `p_whip` | (BB + H)/IP - For recent years, leaders need 1 IP - per team game played |
| `H9` | `p_hits_per_nine` | 9 x H / IP - For recent years, leaders need 1 IP - per team game played |
| `HR9` | `p_hr_per_nine` | 9 x HR / IP - For recent years, leaders need 1 IP - per team game played |
| `BB9` | `p_bb_per_nine` | 9 x BB / IP - For recent years, leaders need 1 IP - per team game played |
| `SO9` | `p_so_per_nine` | 9 x SO / IP - For recent years, leaders need 1 IP - per team game played |
| `SO/BB` | `p_strikeouts_per_base_on_balls` | SO/W or SO/BB - For recent years, pitching leaders need 1 IP - per team game played. |
| `Awards` | `awards` | Awards and honours for that season as listed by Baseball-Reference (e.g. AS = All-Star, MVP-1 = MVP winner). |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. Holds the coach's id on Coaching_Staff. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. Filter to 'data' for player-level analysis. |

### Standings

180 rows, 12 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `W` | `W` | Wins |
| `L` | `L` | Losses |
| `W-L%` | `win_loss_perc` | Win-Loss Percentage - W / (W + L) - For players, leaders need one decision for every ten team games. - For managers, minimum to qualify for leading is 320 games. |
| `GB` | `games_back` | Games Back of Division/League Leader - Computed as games over .500 of leader (W-L) minus games over .500 of team divided by two. - Typically computed at the end of play for a particular day. - Blank for 1st game of DH. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. Filter to 'data' for player-level analysis. |

### Standings_Expanded

180 rows, 32 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Tm` | `team_name` | Team as listed in the source table. |
| `W` | `W` | Wins |
| `L` | `L` | Losses |
| `W-L%` | `win_loss_perc` | Win-Loss Percentage - W / (W + L) - For players, leaders need one decision for every ten team games. - For managers, minimum to qualify for leading is 320 games. |
| `R` | `R` | Runs Scored/Allowed |
| `RA` | `RA` | Runs Allowed |
| `Rdiff` | `run_diff` | Run Differential - Runs Scored - Runs Allowed - May be overall or per game |
| `SOS` | `strength_of_schedule` | Strength of Schedule - The number of runs per game their opponents are better (or worse) than the average team. - Average ML team for years with inter-league play and just their league for other years. |
| `SRS` | `simple_rating_system` | Simple Rating System - The number of runs per game they are better (or worse) than the average team. - Average ML team for years with inter-league play and just their league for other years. - SRS = Run Differential (R_diff) + Strength of Schedule (SOS) |
| `pythWL` | `record_pythag` | Pythagorean Win-Loss - Expected Win-Loss record based on the number of runs scored - and allowed by the team. |
| `Luck` | `luck_pythag` | Pythagorean Luck - The difference between the actual W-L and Pythagorean W-L. |
| `vEast` | `record_vs_east` | Win-loss record against East division clubs. |
| `vCent` | `record_vs_central` | Win-loss record against Central division clubs. |
| `vWest` | `record_vs_west` | Win-loss record against West division clubs. |
| `Inter` | `record_interleague` | Win-loss record in interleague play. |
| `Home` | `record_home` | Win-loss record at home. |
| `Road` | `record_road` | Win-loss record on the road. |
| `ExInn` | `record_xinn` | Win-loss record in extra-inning games. |
| `1Run` | `record_one_run` | Win-loss record in one-run games. |
| `vRHP` | `record_vs_rhp` | Win-loss record in games started by a right-handed pitcher. |
| `vLHP` | `record_vs_lhp` | Win-loss record in games started by a left-handed pitcher. |
| `≥.500` | `record_vs_over_500` | Win-loss record against teams that finished at or above .500. |
| `<.500` | `record_vs_under_500` | Win-loss record against teams that finished below .500. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. Filter to 'data' for player-level analysis. |

### Team_Season_Summary

180 rows, 27 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `W` | `identifier/derived` | Wins. |
| `L` | `identifier/derived` | Losses. |
| `Division_Finish` | `identifier/derived` | Finishing position within the division. |
| `Made_Postseason` | `identifier/derived` | True if the club reached the postseason that year. |
| `Postseason_Summary` | `identifier/derived` | Baseball-Reference's narrative summary of the club's postseason run. |
| `Runs_Scored` | `identifier/derived` | Runs scored over the season. |
| `Runs_Allowed` | `identifier/derived` | Runs allowed over the season. |
| `Pythagorean_W` | `identifier/derived` | Expected wins from runs scored and allowed. |
| `Pythagorean_L` | `identifier/derived` | Expected losses from runs scored and allowed. |
| `Manager` | `identifier/derived` | Manager for the season. |
| `General_Manager` | `identifier/derived` | General manager. |
| `Farm_Director` | `identifier/derived` | Director of player development. |
| `Scouting_Director` | `identifier/derived` | Director of scouting. |
| `Ballpark` | `identifier/derived` | Home ballpark. |
| `Attendance` | `identifier/derived` | Total home attendance for the season. |
| `Park_Factor_Batting_Multi` | `identifier/derived` | Multi-year batting park factor; over 100 favours hitters. |
| `Park_Factor_Pitching_Multi` | `identifier/derived` | Multi-year pitching park factor; over 100 favours hitters. |
| `Park_Factor_Batting_1yr` | `identifier/derived` | Single-year batting park factor; over 100 favours hitters. |
| `Park_Factor_Pitching_1yr` | `identifier/derived` | Single-year pitching park factor; over 100 favours hitters. |
| `Win_Pct` | `identifier/derived` | Winning percentage, W / (W + L). |

### Value_Batting

5,797 rows, 31 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank |
| `Player` | `name_display` | Player name. Baseball-Reference handedness markers have been stripped out into the Bats/Throws column. |
| `Bats` | `derived` | Batting hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | As of June 30 of the season in question. |
| `PA` | `b_pa` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `Rbat` | `b_runs_batting` | Runs Batting - Number of runs better or worse than average the player was as a hitter. - This is based on a modified version of wRAA. - See our about section for a full description of how this is calculated. |
| `Rbaser` | `b_runs_baserunning` | Runs from Baserunning - Number of runs better or worse than average the player was for all baserunning events. - SB, CS, PB, WP, Defensive Indifference. - Developed by Sean Smith of BaseballProjection.com |
| `Rdp` | `b_runs_double_plays` | Runs Grounded into Double Plays - Number of runs better or worse than average the player was at avoiding grounding into double plays. - Developed by Sean Smith of BaseballProjection.com |
| `Rfield` | `b_runs_fielding` | Runs from Fielding - Number of runs better or worse than average the player was for all fielding. - Fielding of balls in play, turning double plays, outfield arms and catcher defense are all included. - We use Baseball Info Solutions Defensive Runs Saved when available - (note that we do not use BIS catcher framing runs RszC ) and - Total Zone Rating from Sean Smith when not. - For Negro League seasons, we use Defensive Regression Analysis from Michael Humphreys. - Our WAR framework was developed by Sean Smith of BaseballProjection.com |
| `Rpos` | `b_runs_position` | Runs from Positional Scarcity - Number of runs above or below average due to positional differences. - Positions like C, SS, and 2B get a bonus. - Positions like 1B, DH, LF get a penalty. - Developed by Sean Smith of BaseballProjection.com |
| `RAA` | `b_raa` | Runs better than Avg - The number of runs this player is better than a league average player. |
| `WAA` | `b_waa` | Wins Above Average for position players - A single number that presents the number of wins the player added - to the team above what a league average player would add. - Scale: 6+ MVP Quality, 3+ All-Star Quality, 0 Starter, - -2-0 Reserve, < -2 Replacement Level - Developed by Sean Smith of BaseballProjection.com |
| `Rrep` | `b_runs_replacement` | Runs from Replacement Level - Number of runs an average player is better than a replacement player. - Replacement is set for a .294 team winning percentage. - Stronger leagues may get a larger bonus. - Developed by Sean Smith of BaseballProjection.com |
| `RAR` | `b_rar` | Runs Above Replacement Level - Total of other columns. The number of runs this player is better than a replacement player. Replacement is set for a .294 team winning percentage. Developed by Sean Smith of BaseballProjection.com |
| `WAR` | `b_war` | Wins Above Replacement for position players - A single number that presents the number of wins the player added - to the team above what a replacement player (think AAA or AAAA) would add. - Scale: 8+ MVP Quality, 5+ All-Star Quality, 2+ Starter, - 0-2 Reserve, < 0 Replacement Level - Developed by Sean Smith of BaseballProjection.com |
| `waaWL%` | `b_waa_win_perc` | Win-Loss% w/ Avg. Team - This is the win-loss of an otherwise average team in ONLY the games this player played in. - For example, for a pitcher this would only consider the games the pitcher threw in and ignoring games they did not play in. |
| `162WL%` | `b_waa_win_perc_162` | Win-Loss% w/ Avg. Team Season - This is the win-loss of an otherwise average team for an entire season giving them credit for only the games this player played in. - For example, for a pitcher this would be waaW-L% - in the games the pitcher threw in and a .500 record otherwise. |
| `oWAR` | `b_war_off` | Offensive Wins Above Replacement (everything but Fielding) - The same statistic as Wins Above Replacement for Position - Players (WAR), but with the fielding value excluded. - oWAR + dWAR does not equal WAR. - Adding would count positions twice. - Contains the factor for batting stats, baserunning, a positional adjustment, and the replacement player adjustment. - Factors developed by Sean Smith of BaseballProjection.com |
| `dWAR` | `b_war_def` | Defensive Wins Above Replacement for position players - A defensive measure of wins above replacement, but given - only the defensive stats of the player and his position adjustment. For this calculation, we use a - replacement level on defense is the league average. - Based on Baseball Info Solutions defensive runs saved from 2003 on - and total zone rating developed by Sean Smith of BaseballProjection.com previously |
| `oRAR` | `b_rar_off` | Offensive Runs above Replacement Level - oWAR + dWAR DOES NOT EQUAL WAR, pos would be counted 2x - Total of all columns except for fielding values - Includes batting, baserunning, positional adjustment, and a playing time adjustment - for the number of runs an average player is better than a replacement player. - Replacement is set for a .294 team winning percentage. - Developed by Sean Smith of BaseballProjection.com |
| `Pos` | `pos` | Positions Played - Positions are listed in order of games played at each. - * indicates the player appeared in at least 2/3rds of team games at that position (applies to a single season or a career total). - Positions after / indicate fewer than ten games played there. - 'H' indicates games as a pinch-hitter or pinch-runner. |
| `Awards` | `awards` | Awards and honours for that season as listed by Baseball-Reference (e.g. AS = All-Star, MVP-1 = MVP winner). |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. Holds the coach's id on Coaching_Staff. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. Filter to 'data' for player-level analysis. |

### Value_Pitching

5,908 rows, 33 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank |
| `Player` | `name_display` | Player name. Baseball-Reference handedness markers have been stripped out into the Bats/Throws column. |
| `Throws` | `derived` | Throwing hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | As of June 30 of the season in question. |
| `IP` | `p_ip` | Innings Pitched |
| `G` | `p_g` | Games Pitched |
| `GS` | `p_gs` | Games Started |
| `R` | `p_r` | Runs Allowed |
| `RA9` | `p_ra9` | Runs Allowed Per 9 IP - This is like ERA, but with unearned runs included. |
| `RA9opp` | `p_ra9_opp` | Opponents’ Runs Scored Per 9 Inn - The average number of runs scored by this pitcher's opposition, per 9 innings. We use park factors to convert the opponent scoring to a league-average context.For in progress seasons, we consider the teams’ last 365 days. Interleague road games are excluded from the avg, and when the pitcher faces an interleague opp at home, we modify the opponent run scoring by .20 runs per 9inning depending on whether the DH is added or removed from their lineup. We assume a league average pitcher would allow this many runs. |
| `RA9def` | `p_ra9_def` | Runs per 9 IP of support from defense - This is based on the team’s Baseball Info Solutions Defensive Runs Saved since 2003 and Total Zone Rating before that. Negro League seasons use Defensive Regression Analysis. Positive values mean the team defense was above average. Negative means it was below average. We take the team’s total balls in play, the balls in play for this pitcher and the team’s total runs saved and split the runs among all of the team’s pitchers. |
| `RA9role` | `p_ra9_role` | Runs per 9 IP difference for SP and RP - From 1960 on we assess factor for starters and relievers. In that time, relievers have averaged a much lower ERA, and this factor accounts for that difference. Previously, this was part of our replacement level calculation, but it has now been moved into Runs Above Avg. |
| `RA9extras` | `p_ra9_extras` | Runs per 9 IP difference for pitching in extra innings - Starting in 2020, MLB had teams begin every extra inning with a runner on second base. If this runner scores, it is charged to the pitcher who started the inning. We adjust the pitcher's expected runs by the run expectancy that is added by the runner being placed on second base (approx 0.6 runs) for each time they start an extra inning. |
| `PPFp` | `p_ppf_custom` | Park Factor customized for parks the pitcher threw in - From 1908 on, we have full gamelogs, so we can say exactly how many innings a pitcher threw in each park. These are 3-year park factors weighted by batters faced in each park. Note the one-game park factor is the team PPF/100 minus 1 times two plus one, since the factors on team pages are for home and road games combined. |
| `RA9avg` | `p_ra9_avg_pitcher` | Runs per 9 IP for an avg pitcher - Equals PPFp/100*(oppRA9 - RAdef + RArole) - This is our best estimate of what an average pitcher would do against these opponents, with this defense and in these parks. |
| `RAA` | `p_raa` | Runs better than Avg - IP*(RA9 avg - RA9)/9, then centered so the league average is always zero. - It is the number of runs this player is better than an average player. Adjusted for quality of opposition, parks pitched in and quality of team defense and recentered, so the league is zero. |
| `WAA` | `p_waa` | Wins Above Average for pitchers - A single number that presents the number of wins the player added - to the team above what a league average player would add. - Scale: 6+ MVP Quality, 3+ All-Star Quality, 0 Starter, - -2-0 Reserve, < -2 Replacement Level - Developed by Sean Smith of BaseballProjection.com |
| `gmLI` | `p_leverage_index_avg_rp` | Game-entering Leverage Index - Solely for relief appearances, this is the average of each appearances opening leverage index - weighted by the batters faced in that outing. - The average pressure the pitcher or batter saw in this game or season. - 1.0 is average pressure, below 1.0 is low pressure and above 1.0 is high pressure. |
| `WAAadj` | `p_waa_adj` | Wins Above Avg Adjustment - For relief pitchers, we multiply WAA by (1+gmLI)/2. This is done in recognition of the added importance of high leverage. WAA adj is the additional value of this leverage adjustment. Also, the manner in which this and the WAA calculations are performed cause the league total WAA to move away from zero, so we also do an operation to recenter the entire league. The recentering forces the league sum to 0 which is as it should be for Wins Above Average. So for the league as a whole, WAA+WAA adj will equal zero and WAR = WAA + WAA adj + Replacement value |
| `WAR` | `p_war` | Wins Above Replacement for Pitchers - A single number that presents the number of wins the player added - to the team above what a replacement player (think AAA or AAAA) would add. This value includes defensive support and includes additional value for high leverage situations. - Scale: 8+ MVP Quality, 5+ All-Star Quality, 2+ Starter, - 0-2 Reserve, < 0 Replacement Level - Developed by Sean Smith of BaseballProjection.com |
| `RAR` | `p_rar` | Runs better than Replacement Level - It is the number of runs this player is better than a replacement player. Replacement is set for a .294 team winning percentage. - Developed by Sean Smith of BaseballProjection.com |
| `waaWL%` | `p_waa_win_perc` | Win-Loss% w/ Avg. Team - This is the win-loss of an otherwise average team in ONLY the games this player played in. - For example, for a pitcher this would only consider the games the pitcher threw in and ignoring games they did not play in. |
| `162WL%` | `p_waa_win_perc_162` | Win-Loss% w/ Avg. Team Season - This is the win-loss of an otherwise average team for an entire season giving them credit for only the games this player played in. - For example, for a pitcher this would be waaW-L% - in the games the pitcher threw in and a .500 record otherwise. |
| `Awards` | `awards` | Awards and honours for that season as listed by Baseball-Reference (e.g. AS = All-Star, MVP-1 = MVP winner). |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. Holds the coach's id on Coaching_Staff. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. Filter to 'data' for player-level analysis. |

## Playoff Data

Workbook: `MLB_Playoff_Data_2020-2025.xlsx` - 8 sheets, 9,736 rows.

### Postseason_Advanced_Batting

1,840 rows, 27 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `team_name_abbr` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank |
| `Player` | `name_display` | Player name. Baseball-Reference handedness markers have been stripped out into the Bats/Throws column. |
| `Bats` | `derived` | Batting hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | As of June 30 of the season in question. |
| `Lg` | `comp_name_abbr` | League |
| `PA` | `b_pa` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `BAbip` | `b_batting_avg_bip` | Batting Avg. on Balls in Play (Hits - Home Runs)/(At Bats - SO - HR + Sac Flies) - This also measures how effectively the - defense turned balls into outs. |
| `ISO` | `b_iso_slugging` | (Total Bases - H)/At Bats or - (2B + 2*3B + 3*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `HR%` | `b_home_run_perc` | Home Run Percentage |
| `SO%` | `b_strikeout_perc` | Strikeout Percentage - Percentage of all plate appearances ending with a strikeout. - (SO)/(all plate appearances) |
| `BB%` | `b_base_on_balls_perc` | Base on Balls Percentage - Percentage of all plate appearances ending with a Base on Balls. - (BB)/(all plate appearances) |
| `WPA` | `b_wpa_bat` | Win Probability Added for Offensive Player |
| `cWPA` | `b_cwpa_bat` | Championship Win Probability Added for Offensive Player - Given average teams, this is the change in probability, displayed in percentage points. - See Win Expectancy explainer for details. |
| `RE24` | `b_baseout_runs` | Base-Out Runs Added - Given the bases occupied/out situation, how many runs did the batter - or baserunner add in the resulting play. - Compared to average, so 0 is average, and above 0 is better than average |
| `RS%` | `b_run_scoring_perc` | Run Scoring Percentage - Percentage of times a baserunner eventually scores a run. - (R - HR) / (H + HBP + BB - HR + G_pr) |
| `SB%` | `b_stolen_base_perc` | Stolen Base Percentage - SB / (SB + CS) |
| `Pos` | `pos` | Positions Played - Positions are listed in order of games played at each. - * indicates the player appeared in at least 2/3rds of team games at that position (applies to a single season or a career total). - Positions after / indicate fewer than ten games played there. - 'H' indicates games as a pinch-hitter or pinch-runner. |
| `Awards` | `awards` | Awards and honours for that season as listed by Baseball-Reference (e.g. AS = All-Star, MVP-1 = MVP winner). |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Postseason_Advanced_Pitching

862 rows, 31 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `team_name_abbr` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank |
| `Player` | `name_display` | Player name. Baseball-Reference handedness markers have been stripped out into the Bats/Throws column. |
| `Throws` | `derived` | Throwing hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | As of June 30 of the season in question. |
| `Lg` | `comp_name_abbr` | League |
| `IP` | `p_ip` | Innings Pitched |
| `BA` | `p_batting_avg` | Batting Average |
| `OBP` | `p_onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) |
| `SLG` | `p_slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB |
| `OPS` | `p_onbase_plus_slugging` | On-Base + Slugging Percentages |
| `BAbip` | `p_batting_avg_bip` | Batting Avg. on Balls in Play (Hits - Home Runs)/(At Bats - SO - HR + Sac Flies) - This also measures how effectively the - defense turned balls into outs. |
| `HR%` | `p_home_run_perc` | Home Run Percentage |
| `K%` | `p_strikeout_perc` | Strikeout Percentage - Percentage of all batters faced struck out. - (SO)/(BFP) |
| `BB%` | `p_base_on_balls_perc` | Base on Balls Percentage - Percentage of all batters faced ending with a Base on Balls. - (BB)/(BFP) |
| `LD%` | `p_ld_perc` | Line Drive Percentage - Percentage of all balls put into play (including home runs) that are line drives. - Batted ball type and location is not complete prior to 1988. |
| `GB%` | `p_gb_perc` | Ground Ball Percentage - Percentage of all balls put into play (including home runs) that are ground balls. - EXCLUDES Bunts - Batted ball type and location is not complete prior to 1988. |
| `FB%` | `p_fb_perc` | Fly Ball Percentage - Percentage of all balls put into play (including home runs) that are fly balls. - EXCLUDES Popups - Batted ball type and location is not complete prior to 1988. |
| `GB/FB` | `p_gb_fb_ratio` | Ground Ball to Fly Ball Ratio - Includes line drives as fly balls. - Batted ball type and location is not complete prior to 1988. |
| `WPA` | `p_wpa_def` | Win Probability Added by Pitcher - Given average teams, this is the change in probability. - See Win Expectancy explainer for details. |
| `cWPA` | `p_cwpa_def` | Championship Win Probability Added by Pitcher - Given average teams, this is the change in probability of winning the World Series, displayed in percentage points. - See Win Expectancy explainer for details. |
| `RE24` | `p_baseout_runs` | Base-Out Runs Saved - Given the bases occupied/out situation, how many runs did the pitcher - save in the resulting play. Compared to average, so 0 is average, and - above 0 is better than average |
| `Awards` | `awards` | Awards and honours for that season as listed by Baseball-Reference (e.g. AS = All-Star, MVP-1 = MVP winner). |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Postseason_Batting

1,908 rows, 38 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank |
| `Player` | `name_display` | Player name. Baseball-Reference handedness markers have been stripped out into the Bats/Throws column. |
| `Bats` | `derived` | Batting hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | As of June 30 of the season in question. |
| `G` | `b_games` | Games Played |
| `PA` | `b_pa` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `AB` | `b_ab` | At Bats |
| `R` | `b_r` | Runs Scored |
| `H` | `b_h` | Hits |
| `2B` | `b_doubles` | Doubles |
| `3B` | `b_triples` | Triples |
| `HR` | `b_hr` | Home Runs |
| `RBI` | `b_rbi` | Runs Batted In |
| `SB` | `b_sb` | Stolen Bases |
| `CS` | `b_cs` | Caught Stealing |
| `BB` | `b_bb` | Bases on Balls/Walks |
| `SO` | `b_so` | Strikeouts |
| `BA` | `b_batting_avg` | Hits/At Bats - For recent years, leaders need 3.1 PA - per team game played - Bold indicates either highest BA using current stats - or awarded title at end of year. |
| `OBP` | `b_onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) - For recent years, leaders need 3.1 PA - per team game played |
| `SLG` | `b_slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `OPS` | `b_onbase_plus_slugging` | On-Base + Slugging Percentages - For recent years, leaders need 3.1 PA - per team game played |
| `TB` | `b_tb` | Total Bases - Singles + 2 x Doubles + 3 x Triples + 4 x Home Runs. |
| `GIDP` | `b_gidp` | Double Plays Grounded Into - Only includes standard 6-4-3, 4-3, etc. double plays. - First tracked in 1933. - For gamelogs only in seasons we have play-by-play, we include triple plays as well. - All official seasonal totals do not include GITP's. |
| `HBP` | `b_hbp` | Times Hit by a Pitch |
| `SH` | `b_sh` | Sacrifice Hits (Sacrifice Bunts) |
| `SF` | `b_sf` | Sacrifice Flies - First tracked in 1955. |
| `IBB` | `b_ibb` | Intentional Bases on Balls - First tracked in 1955. |
| `Pos` | `pos` | Positions Played - Positions are listed in order of games played at each. - * indicates the player appeared in at least 2/3rds of team games at that position (applies to a single season or a career total). - Positions after / indicate fewer than ten games played there. - 'H' indicates games as a pinch-hitter or pinch-runner. |
| `Awards` | `awards` | Awards and honours for that season as listed by Baseball-Reference (e.g. AS = All-Star, MVP-1 = MVP winner). |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. Holds the coach's id on Coaching_Staff. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. Filter to 'data' for player-level analysis. |

### Postseason_Fielding

1,772 rows, 30 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank |
| `Player` | `name_display` | Player name. Baseball-Reference handedness markers have been stripped out into the Bats/Throws column. |
| `Age` | `age` | As of June 30 of the season in question. |
| `G` | `f_games_distinct` | Games Played |
| `GS` | `f_games_started` | Games Started |
| `CG` | `f_cg` | Complete Games at a Single Position |
| `Inn` | `f_innings` | Innings Played at Position |
| `Ch` | `f_chances` | Defensive Chances - Putouts + Assists + Errors |
| `PO` | `f_po` | Putouts |
| `A` | `f_assists` | Assists |
| `E` | `f_errors` | Errors Committed |
| `DP` | `f_dp` | Double Plays Turned |
| `Fld%` | `f_fielding_perc` | Fielding Percentage - (Putouts + Assists) / (Putouts + Assists + Errors) |
| `RF/9` | `f_range_factor_per_nine` | Range Factor per 9 Inn - 9 * (Putouts + Assists) / Innings Played |
| `RF/G` | `f_range_factor_per_game` | Range Factor per Game - (Putouts + Assists) / Games Played |
| `PB` | `f_pb_catcher_only` | Passed Balls |
| `SB` | `f_sb_catcher_only` | Stolen Bases |
| `CS` | `f_cs_catcher_only` | Caught Stealing |
| `CS%` | `f_cs_perc_catcher_only` | Caught Stealing Percentage - CS / (SB + CS) |
| `Pos` | `pos` | Positions Played - Positions are listed in order of games played at each. - * indicates the player appeared in at least 2/3rds of team games at that position (applies to a single season or a career total). - Positions after / indicate fewer than ten games played there. - 'H' indicates games as a pinch-hitter or pinch-runner. |
| `Awards` | `awards` | Awards and honours for that season as listed by Baseball-Reference (e.g. AS = All-Star, MVP-1 = MVP winner). |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. Holds the coach's id on Coaching_Staff. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. Filter to 'data' for player-level analysis. |

### Postseason_Pitching

930 rows, 43 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank |
| `Player` | `name_display` | Player name. Baseball-Reference handedness markers have been stripped out into the Bats/Throws column. |
| `Throws` | `derived` | Throwing hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | As of June 30 of the season in question. |
| `W` | `p_w` | Wins |
| `L` | `p_l` | Losses |
| `W-L%` | `p_win_loss_perc` | Win-Loss Percentage - W / (W + L) - For players, leaders need one decision for every ten team games. |
| `ERA` | `p_earned_run_avg` | 9 * ER / IP - For recent years, leaders need 1 IP - per team game played. - Bold indicates lowest ERA using current stats - Gold means awarded ERA title at end of year. |
| `G` | `p_g` | Games Pitched |
| `GS` | `p_gs` | Games Started |
| `GF` | `p_gf` | Games Finished |
| `CG` | `p_cg` | Complete Games |
| `SHO` | `p_sho` | Shutouts - No runs allowed and a complete game. |
| `SV` | `p_sv` | Saves |
| `IP` | `p_ip` | Innings Pitched |
| `H` | `p_h` | Hits Allowed |
| `R` | `p_r` | Runs Allowed |
| `ER` | `p_er` | Earned Runs Allowed |
| `HR` | `p_hr` | Home Runs Allowed |
| `BB` | `p_bb` | Bases on Balls/Walks |
| `IBB` | `p_ibb` | Intentional Bases on Balls - First tracked in 1955. |
| `SO` | `p_so` | Strikeouts |
| `HBP` | `p_hbp` | Times Hit by a Pitch |
| `BK` | `p_bk` | Balks |
| `WP` | `p_wp` | Wild Pitches |
| `BF` | `p_bfp` | Batters Faced |
| `FIP` | `p_fip` | Fielding Independent Pitching - this stat measures a pitcher's effectiveness at preventing HR, BB, HBP and causing SO - (13*HR + 3*(BB+HBP) - 2*SO)/IP + Constant lg - The constant is set so that each season major-league average FIP is the same as the major-league avg ERA |
| `WHIP` | `p_whip` | (BB + H)/IP - For recent years, leaders need 1 IP - per team game played |
| `H9` | `p_hits_per_nine` | 9 x H / IP - For recent years, leaders need 1 IP - per team game played |
| `HR9` | `p_hr_per_nine` | 9 x HR / IP - For recent years, leaders need 1 IP - per team game played |
| `BB9` | `p_bb_per_nine` | 9 x BB / IP - For recent years, leaders need 1 IP - per team game played |
| `SO9` | `p_so_per_nine` | 9 x SO / IP - For recent years, leaders need 1 IP - per team game played |
| `SO/BB` | `p_strikeouts_per_base_on_balls` | SO/W or SO/BB - For recent years, pitching leaders need 1 IP - per team game played. |
| `Awards` | `awards` | Awards and honours for that season as listed by Baseball-Reference (e.g. AS = All-Star, MVP-1 = MVP winner). |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. Holds the coach's id on Coaching_Staff. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. Filter to 'data' for player-level analysis. |

### Postseason_Roster

1,834 rows, 37 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank |
| `Player` | `name_display` | Player name. Baseball-Reference handedness markers have been stripped out into the Bats/Throws column. |
| `Age` | `age` | As of June 30 of the season in question. |
| `Birth` | `birth_country_and_flag` | Country of Birth |
| `B` | `bats` | Batting Side - B or S - Switch Hitter - This is their primary designation for their career |
| `T` | `throws` | Throwing Hand |
| `Ht` | `height` | Height (ft & inches) |
| `Wt` | `weight` | Weight in Pounds |
| `DoB` | `dob` | Date of Birth |
| `Yrs` | `experience` | Experience - Years the player was/has been in the major leagues. - 1st indicates their first year in the majors, - but does not indicate rookie status. - Includes parts of any seasons. |
| `G` | `games_all` | All games played |
| `GS` | `games_started_all` | Games Started |
| `Batting` | `games_batting` | Games appeared in the batting order, - but may not have batted. |
| `Defense` | `games_defense` | Games in lineup at a defensive position. |
| `P` | `games_at_p` | Games in lineup or announced as a pitcher |
| `C` | `games_at_c` | Games in lineup as a catcher |
| `1B` | `games_at_1b` | Games in lineup as a first baseman |
| `2B` | `games_at_2b` | Games in lineup as a second baseman |
| `3B` | `games_at_3b` | Games in lineup as a third baseman |
| `SS` | `games_at_ss` | Games in lineup as a shortstop |
| `LF` | `games_at_lf` | Games in lineup as a left fielder |
| `CF` | `games_at_cf` | Games in lineup as a center fielder |
| `RF` | `games_at_rf` | Games in lineup as a right fielder |
| `OF` | `games_at_of` | Games in lineup as an outfielder |
| `DH` | `games_at_dh` | Games in lineup as a designated hitter |
| `PH` | `games_at_ph` | Games in lineup as a pinch hitter - May have played another position as well. |
| `PR` | `games_at_pr` | Games in lineup as a pinch runner - May have played another position as well. |
| `Awards` | `awards` | Awards and honours for that season as listed by Baseball-Reference (e.g. AS = All-Star, MVP-1 = MVP winner). |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. Holds the coach's id on Coaching_Staff. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. Filter to 'data' for player-level analysis. |

### Postseason_Schedule_Results

522 rows, 27 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Gm#` | `team_game` | Game Number - Which game out of all played by this team. |
| `Date` | `date_game` | A number in parentheses indicates which game of a doubleheader. - Click dates for box scores of games or standings on this day. |
| `Game_Date` | `identifier/derived` | ISO (YYYY-MM-DD) game date derived from the display Date column. |
| `Doubleheader_Game` | `identifier/derived` | Game 1 or 2 of a doubleheader; blank for single games. |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `Home_Away` | `identifier/derived` | Whether the team was Home or Away, derived from Baseball-Reference's '@' marker. |
| `Opp` | `opp_ID` | Opponent franchise code. |
| `Boxscore_URL` | `boxscore` | Direct link to the Baseball-Reference box score for that game. |
| `W/L` | `win_loss_result` | Win/Loss/Tie - -wo indicates it was a walkoff win or loss. Based on available play-by-play; may be missing some walk-offs before 1969. |
| `R` | `R` | Runs Scored/Allowed |
| `RA` | `RA` | Runs Allowed |
| `Inn` | `extra_innings` | Innings - Only shown if something other than 9 innings were played. |
| `W-L` | `win_loss_record` | Win Loss Record - Team’s overall record after this game. |
| `Win` | `winning_pitcher` | Pitcher credited with the win. |
| `Loss` | `losing_pitcher` | Pitcher charged with the loss. |
| `Save` | `saving_pitcher` | Pitcher credited with the save; blank if none was awarded. |
| `Time` | `time_of_game` | Time of Game |
| `D/N` | `day_or_night` | Day or Night Game - Determined by the start time of the game as stated by RetroSheet. - We rely on their designation here. |
| `Attendance` | `attendance` | Attendance - Typically, tickets sold in home games. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. Filter to 'data' for player-level analysis. |

### Postseason_Series_Results

68 rows, 13 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Series` | `identifier/derived` | Postseason round, e.g. World Series, ALCS. |
| `Series_Code` | `identifier/derived` | Short code for the round, e.g. WS, ALCS, NLDS1. |
| `Series_Result` | `identifier/derived` | Games won by each side, winner first. |
| `Winner_Wins` | `identifier/derived` | Games won by the winning club. |
| `Loser_Wins` | `identifier/derived` | Games won by the losing club. |
| `Winning_Team` | `identifier/derived` | Franchise code of the series winner. |
| `Winning_Team_Name` | `identifier/derived` | Full name of the series winner. |
| `Winning_Team_League` | `identifier/derived` | League of the series winner. |
| `Losing_Team` | `identifier/derived` | Franchise code of the series loser. |
| `Losing_Team_Name` | `identifier/derived` | Full name of the series loser. |
| `Losing_Team_League` | `identifier/derived` | League of the series loser. |
| `Series_URL` | `identifier/derived` | Baseball-Reference page for the series. |

## Advanced Stats

Workbook: `MLB_Advanced_Stats_2020-2025.xlsx` - 86 sheets, 192,326 rows.

### Advanced_Batting

6,062 rows, 39 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `team_name_abbr` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank |
| `Player` | `name_display` | Player name. Baseball-Reference handedness markers have been stripped out into the Bats/Throws column. |
| `Bats` | `derived` | Batting hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | As of June 30 of the season in question. |
| `Lg` | `comp_name_abbr` | League |
| `PA` | `b_pa` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `rOBA` | `b_roba` | rOBA - A measure of a player's offensive contributions, weighted in proportion to each event's actual run value |
| `Rbat+` | `b_rbat_plus` | Rbat+ - Batting runs as computed for WAR, but indexed to the environment the player played in, where 100 is league average. |
| `BAbip` | `b_batting_avg_bip` | Batting Avg. on Balls in Play (Hits - Home Runs)/(At Bats - SO - HR + Sac Flies) - This also measures how effectively the - defense turned balls into outs. |
| `ISO` | `b_iso_slugging` | (Total Bases - H)/At Bats or - (2B + 2*3B + 3*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `HR%` | `b_home_run_perc` | Home Run Percentage |
| `SO%` | `b_strikeout_perc` | Strikeout Percentage - Percentage of all plate appearances ending with a strikeout. - (SO)/(all plate appearances) |
| `BB%` | `b_base_on_balls_perc` | Base on Balls Percentage - Percentage of all plate appearances ending with a Base on Balls. - (BB)/(all plate appearances) |
| `EV` | `b_avg_exit_velo` | Average Exit Velocity - Average speed of the ball off the bat for balls put into play, measured in miles per hour. |
| `HardH%` | `b_hard_hit_perc` | Hard Hit Rate - Percent of balls in play with an exit velocity of 95 mph or more. |
| `LD%` | `b_ld_perc` | Line Drive Percentage - Percentage of all balls put into play (including home runs) that are line drives. - Batted ball type and location is not complete prior to 1988. |
| `GB%` | `b_gb_perc` | Ground Ball Percentage - Percentage of all balls put into play (including home runs) that are ground balls. - EXCLUDES Bunts - Batted ball type and location is not complete prior to 1988. |
| `FB%` | `b_fb_perc` | Fly Ball Percentage - Percentage of all balls put into play (including home runs) that are fly balls. - EXCLUDES Popups - Batted ball type and location is not complete prior to 1988. |
| `GB/FB` | `b_gb_fb_ratio` | Ground Ball to Fly Ball Ratio - Includes line drives as fly balls. - Batted ball type and location is not complete prior to 1988. |
| `Pull%` | `b_pull_perc` | Pull Percentage - Percentage of all balls put into play (including home runs) that are hit to the batter's pull side. - Batted ball type and location is not complete prior to 1988. |
| `Cent%` | `b_center_perc` | Center Percentage - Percentage of all balls put into play (including home runs) that are hit to the center of the field. - Batted ball type and location is not complete prior to 1988. |
| `Oppo%` | `b_oppo_perc` | Opposite-Field Percentage - Percentage of all balls put into play (including home runs) that are hit to the batter's opposite (push) side. - Batted ball type and location is not complete prior to 1988. |
| `WPA` | `b_wpa_bat` | Win Probability Added for Offensive Player |
| `cWPA` | `b_cwpa_bat` | Championship Win Probability Added for Offensive Player - Given average teams, this is the change in probability, displayed in percentage points. - See Win Expectancy explainer for details. |
| `RE24` | `b_baseout_runs` | Base-Out Runs Added - Given the bases occupied/out situation, how many runs did the batter - or baserunner add in the resulting play. - Compared to average, so 0 is average, and above 0 is better than average |
| `RS%` | `b_run_scoring_perc` | Run Scoring Percentage - Percentage of times a baserunner eventually scores a run. - (R - HR) / (H + HBP + BB - HR + G_pr) |
| `SB%` | `b_stolen_base_perc` | Stolen Base Percentage - SB / (SB + CS) |
| `XBT%` | `b_extra_bases_taken_perc` | Extra Bases Taken Percentage - Percentage of times the runner advanced more than one base on a single or more than two bases on a double, when possible. - Does not take into account the location or type of the ball in play. |
| `Pos` | `pos` | Positions Played - Positions are listed in order of games played at each. - * indicates the player appeared in at least 2/3rds of team games at that position (applies to a single season or a career total). - Positions after / indicate fewer than ten games played there. - 'H' indicates games as a pinch-hitter or pinch-runner. |
| `Awards` | `awards` | Awards and honours for that season as listed by Baseball-Reference (e.g. AS = All-Star, MVP-1 = MVP winner). |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Advanced_Fielding_1B

1,161 rows, 47 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `RHB%` | `PA_with_rhb_perc` | Percentage of PAs with a Right-Handed Batter |
| `BIP%` | `PA_with_bip_perc` | Percentage of PAs that ended with ball in play |
| `GBIP%` | `PA_with_gbip_perc` | Percentage of PAs that ended with ground ball in play (not a bunt). |
| `Fld` | `inplay_fielded` | Number of balls fielded - For many years, the fielder for non-out plays is - unknown and this information will not be presented. |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `FC` | `FC` | Fielder’s Choice - Play by fielder was made on a runner rather than the batter. |
| `Tot` | `PO_tot` | Total Putouts |
| `Cgt` | `PO_caught` | Putouts where the ball was caught in the air. |
| `Frc` | `PO_force` | Putouts from force plays. |
| `Tag` | `PO_tag` | Putouts where the runner was tagged. - Does not include tagging a batter or runner when a force is still possible. |
| `3U` | `PO_3u` | Putouts on unassisted putouts of the batter. |
| `Tot_2` | `A_tot` | Total Assists |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `Hm` | `A_H` | Assists where the ball was thrown to Home as a result of a ball in play. |
| `Rly` | `A_relay` | Assists where the ball was thrown as part of a relay. Only counts relays where the initial throw came from the outfield. |
| `Tot_3` | `E_tot` | Total Errors |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Fld_2` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Thr` | `E_throw` | Errors on throws. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Tot_4` | `DP_tot` | Total Double Plays - Note that the types of DPs listed after this column - will likely not total this value - as there are assorted other double plays not listed separately. |
| `363` | `DP_363` | 3-6-3 Double Plays - Any play where the first baseman started and ended the double play. |
| `361` | `DP_361` | 3-6-1 Double Plays - Any play where the first baseman started and ended by another fielder at first (P or 2B). |
| `36` | `DP_36` | 3-6 Double Plays - Any play where the first baseman started the DP with a force and ended by another fielder at second (2B or SS). |
| `GB` | `GDP` | Ground Ball Double Plays - Any ground ball double play where the fielder took part. |
| `GBs` | `GDP_start` | Ground Ball Double Plays Started - Any ground ball double play where the fielder had the first assist. |
| `LD` | `LDP` | Line Drive Double Plays - Any line drive double play where the fielder took part. |
| `LDs` | `LDP_start` | Line Drive Double Plays Started - Any line drive double play where the fielder recorded the first putout. |
| `LDf` | `LDP_finish` | Line Drive Double Plays Finished - Any line drive double play where the fielder recorded the second putout. |
| `bFld` | `inplay_bunt_fielded` | Number of bunts fielded - For many years, the fielder for non-out plays or the batted ball type is - unknown and this information will not be presented. |
| `bF2O%` | `inplay_bunt_fielded_outs_perc` | Percentage of bunts fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Advanced_Fielding_2B

1,144 rows, 46 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `RHB%` | `PA_with_rhb_perc` | Percentage of PAs with a Right-Handed Batter |
| `BIP%` | `PA_with_bip_perc` | Percentage of PAs that ended with ball in play |
| `GBIP%` | `PA_with_gbip_perc` | Percentage of PAs that ended with ground ball in play (not a bunt). |
| `Fld` | `inplay_fielded` | Number of balls fielded - For many years, the fielder for non-out plays is - unknown and this information will not be presented. |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `FC` | `FC` | Fielder’s Choice - Play by fielder was made on a runner rather than the batter. |
| `Tot` | `PO_tot` | Total Putouts |
| `Cgt` | `PO_caught` | Putouts where the ball was caught in the air. |
| `Frc` | `PO_force` | Putouts from force plays. |
| `Tag` | `PO_tag` | Putouts where the runner was tagged. - Does not include tagging a batter or runner when a force is still possible. |
| `Tot_2` | `A_tot` | Total Assists |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `Hm` | `A_H` | Assists where the ball was thrown to Home as a result of a ball in play. |
| `Rly` | `A_relay` | Assists where the ball was thrown as part of a relay. Only counts relays where the initial throw came from the outfield. |
| `Tot_3` | `E_tot` | Total Errors |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Fld_2` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Thr` | `E_throw` | Errors on throws. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Tot_4` | `DP_tot` | Total Double Plays - Note that the types of DPs listed after this column - will likely not total this value - as there are assorted other double plays not listed separately. |
| `643` | `DP_643` | 6-4-3 Double Plays |
| `543` | `DP_543` | 5-4-3 Double Plays |
| `463` | `DP_463` | 4-6-3 Double Plays |
| `43` | `DP_43` | 4-3 Double Plays - Second basemen tags runner or steps on second and throws to first. |
| `GB` | `GDP` | Ground Ball Double Plays - Any ground ball double play where the fielder took part. |
| `GBs` | `GDP_start` | Ground Ball Double Plays Started - Any ground ball double play where the fielder had the first assist. |
| `GBr` | `GDP_relay` | Ground Ball Double Plays Relayed - Any ground ball double play where the fielder had the first putout and second assist. |
| `LD` | `LDP` | Line Drive Double Plays - Any line drive double play where the fielder took part. |
| `LDs` | `LDP_start` | Line Drive Double Plays Started - Any line drive double play where the fielder recorded the first putout. |
| `LDf` | `LDP_finish` | Line Drive Double Plays Finished - Any line drive double play where the fielder recorded the second putout. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Advanced_Fielding_3B

1,139 rows, 44 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `RHB%` | `PA_with_rhb_perc` | Percentage of PAs with a Right-Handed Batter |
| `BIP%` | `PA_with_bip_perc` | Percentage of PAs that ended with ball in play |
| `GBIP%` | `PA_with_gbip_perc` | Percentage of PAs that ended with ground ball in play (not a bunt). |
| `Fld` | `inplay_fielded` | Number of balls fielded - For many years, the fielder for non-out plays is - unknown and this information will not be presented. |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `FC` | `FC` | Fielder’s Choice - Play by fielder was made on a runner rather than the batter. |
| `Tot` | `PO_tot` | Total Putouts |
| `Cgt` | `PO_caught` | Putouts where the ball was caught in the air. |
| `Frc` | `PO_force` | Putouts from force plays. |
| `Tag` | `PO_tag` | Putouts where the runner was tagged. - Does not include tagging a batter or runner when a force is still possible. |
| `Tot_2` | `A_tot` | Total Assists |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `Hm` | `A_H` | Assists where the ball was thrown to Home as a result of a ball in play. |
| `Rly` | `A_relay` | Assists where the ball was thrown as part of a relay. Only counts relays where the initial throw came from the outfield. |
| `Tot_3` | `E_tot` | Total Errors |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Fld_2` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Thr` | `E_throw` | Errors on throws. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Tot_4` | `DP_tot` | Total Double Plays - Note that the types of DPs listed after this column - will likely not total this value - as there are assorted other double plays not listed separately. |
| `543` | `DP_543` | 5-4-3 Double Plays |
| `53` | `DP_53` | 5-3 Double Plays - Third basemen tags runner or steps on third and throws to first. |
| `GB` | `GDP` | Ground Ball Double Plays - Any ground ball double play where the fielder took part. |
| `LD` | `LDP` | Line Drive Double Plays - Any line drive double play where the fielder took part. |
| `LDs` | `LDP_start` | Line Drive Double Plays Started - Any line drive double play where the fielder recorded the first putout. |
| `LDf` | `LDP_finish` | Line Drive Double Plays Finished - Any line drive double play where the fielder recorded the second putout. |
| `bFld` | `inplay_bunt_fielded` | Number of bunts fielded - For many years, the fielder for non-out plays or the batted ball type is - unknown and this information will not be presented. |
| `bF2O%` | `inplay_bunt_fielded_outs_perc` | Percentage of bunts fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Advanced_Fielding_C

712 rows, 42 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `ERA` | `earned_run_avg` | 9 * ER / IP - For recent years, leaders need 1 IP - per team game played. - Bold indicates lowest ERA using current stats - Gold means awarded ERA title at end of year. |
| `RA9` | `run_avg` | Run Average 9 * All Runs Allowed / Innings. |
| `Fld` | `inplay_fielded` | Number of balls fielded - For many years, the fielder for non-out plays is - unknown and this information will not be presented. |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `XI` | `XI` | Catcher Interference - Times a batter reached due to catcher’s interference. |
| `FC` | `FC` | Fielder’s Choice - Play by fielder was made on a runner rather than the batter. |
| `Tot` | `PO_tot` | Total Putouts |
| `Cgt` | `PO_caught` | Putouts where the ball was caught in the air. |
| `Frc` | `PO_force` | Putouts from force plays. |
| `Tag` | `PO_tag` | Putouts where the runner was tagged. - Does not include tagging a batter or runner when a force is still possible. |
| `SO` | `PO_k` | Putouts by the catcher due to a strikeout. |
| `Tot_2` | `A_tot` | Total Assists |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `3B` | `A_3B` | Assists where the ball was thrown to 3b as the result of a ball in play. |
| `K23` | `A_k23` | Assists on dropped third strikes and the ball thrown to 1b. |
| `Tot_3` | `E_tot` | Total Errors |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Fld_2` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Thr` | `E_throw` | Errors on throws. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Tot_4` | `DP_tot` | Total Double Plays - Note that the types of DPs listed after this column - will likely not total this value - as there are assorted other double plays not listed separately. |
| `263` | `DP_263` | 2-6 or 4-3 Double Plays - Any play where the catcher started the double play to second on to first. |
| `n23` | `DP_n23` | ?-2-3 Double Plays - Any double play with the bases loaded home on to first. |
| `GB` | `GDP` | Ground Ball Double Plays - Any ground ball double play where the fielder took part. |
| `bFld` | `inplay_bunt_fielded` | Number of bunts fielded - For many years, the fielder for non-out plays or the batted ball type is - unknown and this information will not be presented. |
| `bF2O%` | `inplay_bunt_fielded_outs_perc` | Percentage of bunts fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Advanced_Fielding_CF

1,106 rows, 52 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `Tot` | `E_tot` | Total Errors |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Fld` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Thr` | `E_throw` | Errors on throws. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Tot_2` | `A_tot` | Total Assists |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `3B` | `A_3B` | Assists where the ball was thrown to 3b as the result of a ball in play. |
| `Hm` | `A_H` | Assists where the ball was thrown to Home as a result of a ball in play. |
| `Opp` | `single_runner_on_first` | Total Plays with single and runner on first - Note: Plays where the runner on 2B stops at 3B are not included. |
| `Held` | `single_runner_on_first_held` | Total Plays with single and runner on first held to second |
| `Kill` | `single_runner_on_first_kill` | Total Plays with single and runner on first thrown out at third |
| `Opp_2` | `single_runner_on_second` | Total Plays with single and runner on second |
| `Held_2` | `single_runner_on_second_held` | Total Plays with single and runner on second held to third |
| `Kill_2` | `single_runner_on_second_kill` | Total Plays with single and runner on second thrown out at home. |
| `Opp_3` | `double_runner_on_first` | Total Plays with double and runner on first |
| `Held_3` | `double_runner_on_first_held` | Total Plays with double and runner on first held to third |
| `Kill_3` | `double_runner_on_first_kill` | Total Plays with double and runner on first thrown out at home. |
| `Opp_4` | `flyout_runner_on_third` | Total Plays with < 2 out, a flyout, and runner on third |
| `Held_4` | `flyout_runner_on_third_held` | Total Plays with < 2 out, a flyout, and runner on third held to third |
| `Kill_4` | `flyout_runner_on_third_kill` | Total Plays with < 2 out, a flyout, and runner on third thrown out at home. |
| `Opp_5` | `flyout_runner_on_second` | Total Plays with < 2 out, a flyout, and runner on second |
| `Held_5` | `flyout_runner_on_second_held` | Total Plays with < 2 out, a flyout, and runner on second held to second |
| `Kill_5` | `flyout_runner_on_second_kill` | Total Plays with < 2 out, a flyout, and runner on second thrown out at third. |
| `Opp_6` | `outfield_arm_opps` | Total Plays from five previous situations. |
| `Held_6` | `outfield_arm_held` | Total Plays from five previous situations where player did not advance. |
| `Held%` | `outfield_arm_held_perc` | Percentage of Plays from five previous situations where player did not advance. |
| `Adv` | `outfield_arm_adv` | Total Plays from five previous situations where baserunner advanced the extra base. |
| `Kill_6` | `outfield_arm_kills` | Total Plays from five previous situations where runner is thrown out attempting to advance. |
| `Kill%` | `outfield_arm_kill_perc` | Percentage of Plays from five previous situations where baserunner was thrown out trying to advance. |
| `Aother` | `A_other` | Assists other than kills from the five previous situations. |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `RHB%` | `PA_with_rhb_perc` | Percentage of PAs with a Right-Handed Batter |
| `BIP%` | `PA_with_bip_perc` | Percentage of PAs that ended with ball in play |
| `FBIP%` | `PA_with_fbip_perc` | Percentage of PAs that ended with a fly ball in play. |
| `Fld_2` | `inplay_fielded` | Number of balls fielded - For many years, the fielder for non-out plays is - unknown and this information will not be presented. |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Advanced_Fielding_C_Baserunning

712 rows, 33 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `PB` | `PB` | Passed Balls |
| `WP` | `WP` | Wild Pitches |
| `SBO` | `SB_opp` | Stolen Base Opportunities - Plate appearances through which a runner was on first or second with the next base open. |
| `SB` | `SB` | Stolen Bases |
| `CS` | `CS` | Caught Stealing |
| `CSctch` | `CS_catcher` | Caught Stealing by Catcher Caught stealings where the catcher registered an assist. - Pickoff Caught Stealing by the pitcher are included in the CS number. |
| `CS%` | `caught_stealing_perc` | Caught Stealing Percentage - CS / (SB + CS) |
| `SB2` | `SB_2` | Steals of 2nd Base |
| `CS2` | `CS_2` | Caught Stealing 2nd Base |
| `SB3` | `SB_3` | Steals of 3rd Base |
| `CS3` | `CS_3` | Caught Stealing 3rd Base |
| `SBH` | `SB_H` | Steals of Home |
| `CSH` | `CS_H` | Caught Stealing Home |
| `PO` | `pickoffs` | Pickoffs - Runner picked off a base. May include cases they were safe on an error. - Also includes Pickoff Caught Stealing plays. |
| `PCS` | `POCS` | Pickoff Caught Stealing - Runner picked off a base and or while attempting to steal. - Is included in CS numbers and PO numbers. |
| `RBA` | `runner_bases_added` | Runner Bases Added - Total bases added on baserunning plays while this player was a catcher including WP, PB, and SB. |
| `RK` | `runner_kills` | Runner Kills - Total baserunners thrown out by the catcher including CS, pickoffs and other outs attempting to advance. |
| `SBlev` | `SB_leverage` | Stolen Base Leverage Index - The importance of the context in which the base was stolen - Above one means higher than average pressure. - Below one means lower than average pressure. |
| `CSlev` | `CS_leverage` | Caught Stealing Leverage Index - The importance of the context in which the runner was caught - Above one means higher than average pressure. - Below one means lower than average pressure. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Advanced_Fielding_LF

1,562 rows, 52 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `Tot` | `E_tot` | Total Errors |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Fld` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Thr` | `E_throw` | Errors on throws. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Tot_2` | `A_tot` | Total Assists |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `3B` | `A_3B` | Assists where the ball was thrown to 3b as the result of a ball in play. |
| `Hm` | `A_H` | Assists where the ball was thrown to Home as a result of a ball in play. |
| `Opp` | `single_runner_on_first` | Total Plays with single and runner on first - Note: Plays where the runner on 2B stops at 3B are not included. |
| `Held` | `single_runner_on_first_held` | Total Plays with single and runner on first held to second |
| `Kill` | `single_runner_on_first_kill` | Total Plays with single and runner on first thrown out at third |
| `Opp_2` | `single_runner_on_second` | Total Plays with single and runner on second |
| `Held_2` | `single_runner_on_second_held` | Total Plays with single and runner on second held to third |
| `Kill_2` | `single_runner_on_second_kill` | Total Plays with single and runner on second thrown out at home. |
| `Opp_3` | `double_runner_on_first` | Total Plays with double and runner on first |
| `Held_3` | `double_runner_on_first_held` | Total Plays with double and runner on first held to third |
| `Kill_3` | `double_runner_on_first_kill` | Total Plays with double and runner on first thrown out at home. |
| `Opp_4` | `flyout_runner_on_third` | Total Plays with < 2 out, a flyout, and runner on third |
| `Held_4` | `flyout_runner_on_third_held` | Total Plays with < 2 out, a flyout, and runner on third held to third |
| `Kill_4` | `flyout_runner_on_third_kill` | Total Plays with < 2 out, a flyout, and runner on third thrown out at home. |
| `Opp_5` | `flyout_runner_on_second` | Total Plays with < 2 out, a flyout, and runner on second |
| `Held_5` | `flyout_runner_on_second_held` | Total Plays with < 2 out, a flyout, and runner on second held to second |
| `Kill_5` | `flyout_runner_on_second_kill` | Total Plays with < 2 out, a flyout, and runner on second thrown out at third. |
| `Opp_6` | `outfield_arm_opps` | Total Plays from five previous situations. |
| `Held_6` | `outfield_arm_held` | Total Plays from five previous situations where player did not advance. |
| `Held%` | `outfield_arm_held_perc` | Percentage of Plays from five previous situations where player did not advance. |
| `Adv` | `outfield_arm_adv` | Total Plays from five previous situations where baserunner advanced the extra base. |
| `Kill_6` | `outfield_arm_kills` | Total Plays from five previous situations where runner is thrown out attempting to advance. |
| `Kill%` | `outfield_arm_kill_perc` | Percentage of Plays from five previous situations where baserunner was thrown out trying to advance. |
| `Aother` | `A_other` | Assists other than kills from the five previous situations. |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `RHB%` | `PA_with_rhb_perc` | Percentage of PAs with a Right-Handed Batter |
| `BIP%` | `PA_with_bip_perc` | Percentage of PAs that ended with ball in play |
| `FBIP%` | `PA_with_fbip_perc` | Percentage of PAs that ended with a fly ball in play. |
| `Fld_2` | `inplay_fielded` | Number of balls fielded - For many years, the fielder for non-out plays is - unknown and this information will not be presented. |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Advanced_Fielding_P

5,734 rows, 37 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `BIP%` | `PA_with_bip_perc` | Percentage of PAs that ended with ball in play |
| `GBIP%` | `PA_with_gbip_perc` | Percentage of PAs that ended with ground ball in play (not a bunt). |
| `Fld` | `inplay_fielded` | Number of balls fielded - For many years, the fielder for non-out plays is - unknown and this information will not be presented. |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `FC` | `FC` | Fielder’s Choice - Play by fielder was made on a runner rather than the batter. |
| `Tot` | `PO_tot` | Total Putouts |
| `Cgt` | `PO_caught` | Putouts where the ball was caught in the air. |
| `31` | `PO_31` | Putouts on first baseman (or other) to pitcher at first. |
| `Tot_2` | `A_tot` | Total Assists |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `Tot_3` | `E_tot` | Total Errors |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Fld_2` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Thr` | `E_throw` | Errors on throws. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Tot_4` | `DP_tot` | Total Double Plays - Note that the types of DPs listed after this column - will likely not total this value - as there are assorted other double plays not listed separately. |
| `163` | `DP_163` | 1-6 or 4-3 Double Plays - Any play where the pitcher started the double play to second on to first. |
| `GB` | `GDP` | Ground Ball Double Plays - Any ground ball double play where the fielder took part. |
| `LD` | `LDP` | Line Drive Double Plays - Any line drive double play where the fielder took part. |
| `bFld` | `inplay_bunt_fielded` | Number of bunts fielded - For many years, the fielder for non-out plays or the batted ball type is - unknown and this information will not be presented. |
| `bF2O%` | `inplay_bunt_fielded_outs_perc` | Percentage of bunts fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Advanced_Fielding_RF

1,452 rows, 52 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `Tot` | `E_tot` | Total Errors |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Fld` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Thr` | `E_throw` | Errors on throws. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Tot_2` | `A_tot` | Total Assists |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `3B` | `A_3B` | Assists where the ball was thrown to 3b as the result of a ball in play. |
| `Hm` | `A_H` | Assists where the ball was thrown to Home as a result of a ball in play. |
| `Opp` | `single_runner_on_first` | Total Plays with single and runner on first - Note: Plays where the runner on 2B stops at 3B are not included. |
| `Held` | `single_runner_on_first_held` | Total Plays with single and runner on first held to second |
| `Kill` | `single_runner_on_first_kill` | Total Plays with single and runner on first thrown out at third |
| `Opp_2` | `single_runner_on_second` | Total Plays with single and runner on second |
| `Held_2` | `single_runner_on_second_held` | Total Plays with single and runner on second held to third |
| `Kill_2` | `single_runner_on_second_kill` | Total Plays with single and runner on second thrown out at home. |
| `Opp_3` | `double_runner_on_first` | Total Plays with double and runner on first |
| `Held_3` | `double_runner_on_first_held` | Total Plays with double and runner on first held to third |
| `Kill_3` | `double_runner_on_first_kill` | Total Plays with double and runner on first thrown out at home. |
| `Opp_4` | `flyout_runner_on_third` | Total Plays with < 2 out, a flyout, and runner on third |
| `Held_4` | `flyout_runner_on_third_held` | Total Plays with < 2 out, a flyout, and runner on third held to third |
| `Kill_4` | `flyout_runner_on_third_kill` | Total Plays with < 2 out, a flyout, and runner on third thrown out at home. |
| `Opp_5` | `flyout_runner_on_second` | Total Plays with < 2 out, a flyout, and runner on second |
| `Held_5` | `flyout_runner_on_second_held` | Total Plays with < 2 out, a flyout, and runner on second held to second |
| `Kill_5` | `flyout_runner_on_second_kill` | Total Plays with < 2 out, a flyout, and runner on second thrown out at third. |
| `Opp_6` | `outfield_arm_opps` | Total Plays from five previous situations. |
| `Held_6` | `outfield_arm_held` | Total Plays from five previous situations where player did not advance. |
| `Held%` | `outfield_arm_held_perc` | Percentage of Plays from five previous situations where player did not advance. |
| `Adv` | `outfield_arm_adv` | Total Plays from five previous situations where baserunner advanced the extra base. |
| `Kill_6` | `outfield_arm_kills` | Total Plays from five previous situations where runner is thrown out attempting to advance. |
| `Kill%` | `outfield_arm_kill_perc` | Percentage of Plays from five previous situations where baserunner was thrown out trying to advance. |
| `Aother` | `A_other` | Assists other than kills from the five previous situations. |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `RHB%` | `PA_with_rhb_perc` | Percentage of PAs with a Right-Handed Batter |
| `BIP%` | `PA_with_bip_perc` | Percentage of PAs that ended with ball in play |
| `FBIP%` | `PA_with_fbip_perc` | Percentage of PAs that ended with a fly ball in play. |
| `Fld_2` | `inplay_fielded` | Number of balls fielded - For many years, the fielder for non-out plays is - unknown and this information will not be presented. |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Advanced_Fielding_SS

827 rows, 47 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `RHB%` | `PA_with_rhb_perc` | Percentage of PAs with a Right-Handed Batter |
| `BIP%` | `PA_with_bip_perc` | Percentage of PAs that ended with ball in play |
| `GBIP%` | `PA_with_gbip_perc` | Percentage of PAs that ended with ground ball in play (not a bunt). |
| `Fld` | `inplay_fielded` | Number of balls fielded - For many years, the fielder for non-out plays is - unknown and this information will not be presented. |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `FC` | `FC` | Fielder’s Choice - Play by fielder was made on a runner rather than the batter. |
| `Tot` | `PO_tot` | Total Putouts |
| `Cgt` | `PO_caught` | Putouts where the ball was caught in the air. |
| `Frc` | `PO_force` | Putouts from force plays. |
| `Tag` | `PO_tag` | Putouts where the runner was tagged. - Does not include tagging a batter or runner when a force is still possible. |
| `Tot_2` | `A_tot` | Total Assists |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `Hm` | `A_H` | Assists where the ball was thrown to Home as a result of a ball in play. |
| `Rly` | `A_relay` | Assists where the ball was thrown as part of a relay. Only counts relays where the initial throw came from the outfield. |
| `Tot_3` | `E_tot` | Total Errors |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Fld_2` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Thr` | `E_throw` | Errors on throws. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Tot_4` | `DP_tot` | Total Double Plays - Note that the types of DPs listed after this column - will likely not total this value - as there are assorted other double plays not listed separately. |
| `643` | `DP_643` | 6-4-3 Double Plays |
| `63` | `DP_63` | 6-3 Double Plays - Shortstop tags runner from first or steps on second and throws to first. |
| `463` | `DP_463` | 4-6-3 Double Plays |
| `163` | `DP_163` | 1-6 or 4-3 Double Plays - Any play where the pitcher started the double play to second on to first. |
| `363` | `DP_363` | 3-6-3 Double Plays - Any play where the first baseman started and ended the double play. |
| `GB` | `GDP` | Ground Ball Double Plays - Any ground ball double play where the fielder took part. |
| `GBs` | `GDP_start` | Ground Ball Double Plays Started - Any ground ball double play where the fielder had the first assist. |
| `GBr` | `GDP_relay` | Ground Ball Double Plays Relayed - Any ground ball double play where the fielder had the first putout and second assist. |
| `LD` | `LDP` | Line Drive Double Plays - Any line drive double play where the fielder took part. |
| `LDs` | `LDP_start` | Line Drive Double Plays Started - Any line drive double play where the fielder recorded the first putout. |
| `LDf` | `LDP_finish` | Line Drive Double Plays Finished - Any line drive double play where the fielder recorded the second putout. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Advanced_Pitching

6,341 rows, 33 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `team_name_abbr` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank |
| `Player` | `name_display` | Player name. Baseball-Reference handedness markers have been stripped out into the Bats/Throws column. |
| `Throws` | `derived` | Throwing hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | As of June 30 of the season in question. |
| `Lg` | `comp_name_abbr` | League |
| `IP` | `p_ip` | Innings Pitched |
| `BA` | `p_batting_avg` | Batting Average |
| `OBP` | `p_onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) |
| `SLG` | `p_slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB |
| `OPS` | `p_onbase_plus_slugging` | On-Base + Slugging Percentages |
| `BAbip` | `p_batting_avg_bip` | Batting Avg. on Balls in Play (Hits - Home Runs)/(At Bats - SO - HR + Sac Flies) - This also measures how effectively the - defense turned balls into outs. |
| `HR%` | `p_home_run_perc` | Home Run Percentage |
| `K%` | `p_strikeout_perc` | Strikeout Percentage - Percentage of all batters faced struck out. - (SO)/(BFP) |
| `BB%` | `p_base_on_balls_perc` | Base on Balls Percentage - Percentage of all batters faced ending with a Base on Balls. - (BB)/(BFP) |
| `EV` | `p_avg_exit_velo` | Average Exit Velocity - Average speed of the ball off the bat for balls put into play, measured in miles per hour. |
| `HardH%` | `p_hard_hit_perc` | Hard Hit Rate - Percent of balls in play with an exit velocity of 95 mph or more. |
| `LD%` | `p_ld_perc` | Line Drive Percentage - Percentage of all balls put into play (including home runs) that are line drives. - Batted ball type and location is not complete prior to 1988. |
| `GB%` | `p_gb_perc` | Ground Ball Percentage - Percentage of all balls put into play (including home runs) that are ground balls. - EXCLUDES Bunts - Batted ball type and location is not complete prior to 1988. |
| `FB%` | `p_fb_perc` | Fly Ball Percentage - Percentage of all balls put into play (including home runs) that are fly balls. - EXCLUDES Popups - Batted ball type and location is not complete prior to 1988. |
| `GB/FB` | `p_gb_fb_ratio` | Ground Ball to Fly Ball Ratio - Includes line drives as fly balls. - Batted ball type and location is not complete prior to 1988. |
| `WPA` | `p_wpa_def` | Win Probability Added by Pitcher - Given average teams, this is the change in probability. - See Win Expectancy explainer for details. |
| `cWPA` | `p_cwpa_def` | Championship Win Probability Added by Pitcher - Given average teams, this is the change in probability of winning the World Series, displayed in percentage points. - See Win Expectancy explainer for details. |
| `RE24` | `p_baseout_runs` | Base-Out Runs Saved - Given the bases occupied/out situation, how many runs did the pitcher - save in the resulting play. Compared to average, so 0 is average, and - above 0 is better than average |
| `Awards` | `awards` | Awards and honours for that season as listed by Baseball-Reference (e.g. AS = All-Star, MVP-1 = MVP winner). |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Awards_And_Honors

23 rows, 12 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Award` | `award_title` | Name of the award or honour. |
| `Player` | `name` | Player name. |
| `Stats` | `stats` | Baseball-Reference link label for the related stats page. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Baserunning_Batting

5,217 rows, 46 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Bats` | `derived` | Batting hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `PA` | `PA` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `ROE` | `ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `XI` | `XI` | Catcher Interference - Times a batter reached due to catcher’s interference. |
| `RS%` | `runs_scored_perc` | Run Scoring Percentage - Percentage of times a baserunner eventually scores a run. - (R - HR) / (H + HBP + BB - HR + G_pr) |
| `SBO` | `SB_opp` | Stolen Base Opportunities - Plate appearances through which a runner was on first or second with the next base open. |
| `SB` | `SB` | Stolen Bases |
| `CS` | `CS` | Caught Stealing |
| `SB%` | `stolen_base_perc` | Stolen Base Percentage - SB / (SB + CS) |
| `SB2` | `SB_2` | Steals of 2nd Base |
| `CS2` | `CS_2` | Caught Stealing 2nd Base |
| `SB3` | `SB_3` | Steals of 3rd Base |
| `CS3` | `CS_3` | Caught Stealing 3rd Base |
| `SBH` | `SB_H` | Steals of Home |
| `CSH` | `CS_H` | Caught Stealing Home |
| `PO` | `pickoffs` | Pickoffs - Runner picked off a base. May include cases they were safe on an error. - Also includes Pickoff Caught Stealing plays. |
| `PCS` | `POCS` | Pickoff Caught Stealing - Runner picked off a base and or while attempting to steal. - Is included in CS numbers and PO numbers. |
| `OOB` | `outs_on_base` | Outs on Base - Runner is put out while making a baserunning play. - Example plays: out advancing on a fly ball, out attempting to reach another base on a hit, - doubled off on a line drive, or out attempting to advance on a wild pitch or passed ball. - Does not include pickoffs, caught stealing, or force plays. |
| `OOB1` | `outs_on_base_1` | Outs on Base at 1st - Runner is put out while making a baserunning play. - Example plays: out advancing on a fly ball, out attempting to reach another base on a hit, - doubled off on a line drive, or out attempting to advance on a wild pitch or passed ball. - Does not include pickoffs, caught stealing, or force plays. |
| `OOB2` | `outs_on_base_2` | Outs on Base at 2nd - Runner is put out while making a baserunning play. - Example plays: out advancing on a fly ball, out attempting to reach another base on a hit, - doubled off on a line drive, or out attempting to advance on a wild pitch or passed ball. - Does not include pickoffs, caught stealing, or force plays. |
| `OOB3` | `outs_on_base_3` | Outs on Base at 3rd - Runner is put out while making a baserunning play. - Example plays: out advancing on a fly ball, out attempting to reach another base on a hit, - doubled off on a line drive, or out attempting to advance on a wild pitch or passed ball. - Does not include pickoffs, caught stealing, or force plays. |
| `OOBHm` | `outs_on_base_h` | Outs on Base at Home - Runner is put out while making a baserunning play. - Example plays: out advancing on a fly ball, out attempting to reach another base on a hit, - doubled off on a line drive, or out attempting to advance on a wild pitch or passed ball. - Does not include pickoffs, caught stealing, or force plays. |
| `BT` | `bases_taken` | Bases Taken - Bases advanced on fly balls, passed balls, wild pitches, balks, defensive indifference. |
| `XBT%` | `extra_bases_taken_perc` | Extra Bases Taken Percentage - Percentage of times the runner advanced more than one base on a single or more than two bases on a double, when possible. - Does not take into account the location or type of the ball in play. |
| `1stS` | `on_first_single` | On First, when a single is hit - Times a runner is on first and the batter hits a single. |
| `1stS2` | `on_first_single_12` | On First, when a single is hit and runner reaches second |
| `1stS3` | `on_first_single_13` | On First, when a single is hit and runner reaches third or scores |
| `1stD` | `on_first_double` | On First, when a double is hit - Times a runner is on first and the batter hits a double. |
| `1stD3` | `on_first_double_13` | On First, when a double is hit and runner reaches third |
| `1stDH` | `on_first_double_1H` | On First, when a double is hit and runner scores |
| `2ndS` | `on_second_single` | On Second, when a single is hit - Times a runner is on second and the batter hits a single. |
| `2ndS3` | `on_second_single_23` | On Second, when a single is hit and runner reaches third |
| `2ndSH` | `on_second_single_2H` | On Second, when a single is hit and runner scores |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Basesituation_Pitching

6,369 rows, 47 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Throws` | `derived` | Throwing hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `IP` | `IP` | Innings Pitched |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `H` | `H_all` | All Hits |
| `Inf` | `H_inf` | Infield Hits - Batted ball type and location is not complete prior to 1988. |
| `Bnt` | `H_bunt` | Bunt Hits - Batted ball type and location is not complete prior to 1988. |
| `All` | `HR_all` | Home Run Total |
| `GS` | `HR_gs` | Grand Slam Home Runs |
| `GSo` | `HR_gs_opp` | Grand Slam Opportunities - Plate Appearances with the Bases Loaded |
| `vRH` | `HR_vrh` | Home Runs off Right-Handers |
| `vLH` | `HR_vlh` | Home Runs off Left-Handers |
| `Hm` | `HR_hm` | Home Runs at Home |
| `Rd` | `HR_rd` | Home Runs on the Road |
| `<2,3B` | `lt_2_out_on_third_opp` | PAs with less than two out, runner on third |
| `Scr` | `lt_2_out_on_third_scored` | PAs with less than two out, runner on third and runner scored |
| `SO` | `lt_2_out_on_third_so` | PAs with less than two out, runner on third and pitcher struck out batter |
| `%` | `lt_2_out_on_third_perc` | PAs with less than two out, runner on third and runner scored |
| `ROE` | `ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `WP` | `WP` | Wild Pitches |
| `PB` | `PB` | Passed Balls |
| `SBO` | `SB_opp` | Stolen Base Opportunities - Plate appearances through which a runner was on first or second with the next base open. |
| `SB` | `SB` | Stolen Bases |
| `CS` | `CS` | Caught Stealing |
| `SB%` | `stolen_base_perc` | Stolen Base Percentage - SB / (SB + CS) |
| `SB2` | `SB_2` | Steals of 2nd Base |
| `CS2` | `CS_2` | Caught Stealing 2nd Base |
| `SB3` | `SB_3` | Steals of 3rd Base |
| `CS3` | `CS_3` | Caught Stealing 3rd Base |
| `SBH` | `SB_H` | Steals of Home |
| `CSH` | `CS_H` | Caught Stealing Home |
| `PO` | `pickoffs` | Pickoffs - Runner picked off a base. May include cases they were safe on an error. - Also includes Pickoff Caught Stealing plays. |
| `PCS` | `POCS` | Pickoff Caught Stealing - Runner picked off a base and or while attempting to steal. - Is included in CS numbers and PO numbers. |
| `BT` | `bases_taken` | Bases Taken - Bases advanced on fly balls, passed balls, wild pitches, balks, defensive indifference. |
| `PAu` | `PA_unknown` | Plate Appearances for which data is not known - Note that for many stats (like pitcher SLG, 2B, 3B allowed, WPA, HR direction, etc.) - this will mean that the totals given are incomplete. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Batting_Pitching

6,405 rows, 40 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Throws` | `derived` | Throwing hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `IP` | `IP` | Innings Pitched |
| `PAu` | `PA_unknown` | Plate Appearances for which data is not known - Note that for many stats (like pitcher SLG, 2B, 3B allowed, WPA, HR direction, etc.) - this will mean that the totals given are incomplete. |
| `G` | `G` | Games Played or Pitched |
| `PA` | `PA` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `AB` | `AB` | At Bats |
| `R` | `R` | Runs Scored/Allowed |
| `H` | `H` | Hits/Hits Allowed |
| `2B` | `2B` | Doubles Hit/Allowed |
| `3B` | `3B` | Triples Hit/Allowed |
| `HR` | `HR` | Home Runs Hit/Allowed |
| `SB` | `SB` | Stolen Bases |
| `CS` | `CS` | Caught Stealing |
| `BB` | `BB` | Bases on Balls/Walks |
| `SO` | `SO` | Strikeouts |
| `BA` | `batting_avg` | Hits/At Bats - For recent years, leaders need 3.1 PA - per team game played - Bold indicates either highest BA using current stats - or awarded title at end of year. |
| `OBP` | `onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) - For recent years, leaders need 3.1 PA - per team game played |
| `SLG` | `slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `OPS` | `onbase_plus_slugging` | On-Base + Slugging Percentages - For recent years, leaders need 3.1 PA - per team game played |
| `BAbip` | `batting_avg_bip` | Batting Avg. on Balls in Plays (Hits - Home Runs)/(At Bats - SO - HR + Sac Flies) - This also measures how effectively the - defense turned balls into outs. |
| `TB` | `TB` | Total Bases - Singles + 2 x Doubles + 3 x Triples + 4 x Home Runs. |
| `GDP` | `GIDP` | Double Plays Grounded Into - Only includes standard 6-4-3, 4-3, etc. double plays. - First tracked in 1933. - For gamelogs only in seasons we have play-by-play, we include triple plays as well. - All official seasonal totals do not include GITP's. |
| `HBP` | `HBP` | Times Hit by a Pitch. |
| `SH` | `SH` | Sacrifice Hits (Sacrifice Bunts) |
| `SF` | `SF` | Sacrifice Flies - First tracked in 1954. |
| `IBB` | `IBB` | Intentional Bases on Balls - First tracked in 1955. |
| `ROE` | `ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Cumulative_Batting

9,483 rows, 38 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Bats` | `derived` | Batting hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Yrs` | `seasons` | Years in major league baseball , or - Years matching criteria |
| `G` | `G` | Games Played - This includes all times that the player appeared on the lineup card. Pitchers in non-DH games that appeared on the lineup card but didn't bat will still have a game in this column. |
| `PA` | `PA` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `AB` | `AB` | At Bats |
| `R` | `R` | Runs Scored/Allowed |
| `H` | `H` | Hits/Hits Allowed |
| `2B` | `2B` | Doubles Hit/Allowed |
| `3B` | `3B` | Triples Hit/Allowed |
| `HR` | `HR` | Home Runs Hit/Allowed |
| `RBI` | `RBI` | Runs Batted In |
| `SB` | `SB` | Stolen Bases |
| `CS` | `CS` | Caught Stealing |
| `BB` | `BB` | Bases on Balls/Walks |
| `SO` | `SO` | Strikeouts |
| `BA` | `batting_avg` | Hits/At Bats - For recent years, leaders need 3.1 PA - per team game played - Bold indicates either highest BA using current stats - or awarded title at end of year. |
| `OBP` | `onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) - For recent years, leaders need 3.1 PA - per team game played |
| `SLG` | `slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `OPS` | `onbase_plus_slugging` | On-Base + Slugging Percentages - For recent years, leaders need 3.1 PA - per team game played |
| `OPS+` | `onbase_plus_slugging_plus` | OPS+ - 100*[OBP/lg OBP + SLG/lg SLG - 1] - Adjusted to the player’s ballpark(s) |
| `TB` | `TB` | Total Bases - Singles + 2 x Doubles + 3 x Triples + 4 x Home Runs. |
| `GDP` | `GIDP` | Double Plays Grounded Into - Only includes standard 6-4-3, 4-3, etc. double plays. - First tracked in 1933. - For gamelogs only in seasons we have play-by-play, we include triple plays as well. - All official seasonal totals do not include GITP's. |
| `HBP` | `HBP` | Times Hit by a Pitch. |
| `SH` | `SH` | Sacrifice Hits (Sacrifice Bunts) |
| `SF` | `SF` | Sacrifice Flies - First tracked in 1954. |
| `IBB` | `IBB` | Intentional Bases on Balls - First tracked in 1955. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Cumulative_Pitching

5,809 rows, 43 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Throws` | `derived` | Throwing hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Yrs` | `seasons` | Years in major league baseball , or - Years matching criteria |
| `W` | `W` | Wins |
| `L` | `L` | Losses |
| `W-L%` | `win_loss_perc` | Win-Loss Percentage - W / (W + L) - For players, leaders need one decision for every ten team games. - For managers, minimum to qualify for leading is 320 games. |
| `ERA` | `earned_run_avg` | 9 * ER / IP - For recent years, leaders need 1 IP - per team game played. - Bold indicates lowest ERA using current stats - Gold means awarded ERA title at end of year. |
| `G` | `G` | Games Played or Pitched |
| `GS` | `GS` | Games Started |
| `GF` | `GF` | Games Finished - Credited to the last pitcher to appear for a team in a game. - Complete Games are not counted as Games Finished. |
| `CG` | `CG` | Complete Game |
| `SHO` | `SHO` | Shutouts - No runs allowed and a complete game. |
| `SV` | `SV` | Saves |
| `IP` | `IP` | Innings Pitched |
| `H` | `H` | Hits/Hits Allowed |
| `R` | `R` | Runs Scored/Allowed |
| `ER` | `ER` | Earned Runs Allowed |
| `HR` | `HR` | Home Runs Hit/Allowed |
| `BB` | `BB` | Bases on Balls/Walks |
| `IBB` | `IBB` | Intentional Bases on Balls - First tracked in 1955. |
| `SO` | `SO` | Strikeouts |
| `HBP` | `HBP` | Times Hit by a Pitch. |
| `BK` | `BK` | Balks |
| `WP` | `WP` | Wild Pitches |
| `BF` | `batters_faced` | Batters Faced |
| `ERA+` | `earned_run_avg_plus` | ERA+ - 100*[lgERA/ERA] - Adjusted to the player’s ballpark(s). |
| `WHIP` | `whip` | (BB + H)/IP - For recent years, leaders need 1 IP - per team game played |
| `H9` | `hits_per_nine` | 9 x H / IP - For recent years, leaders need 1 IP - per team game played |
| `HR9` | `home_runs_per_nine` | 9 x HR / IP - For recent years, leaders need 1 IP - per team game played |
| `BB9` | `bases_on_balls_per_nine` | 9 x BB / IP - For recent years, leaders need 1 IP - per team game played |
| `SO9` | `strikeouts_per_nine` | 9 x SO / IP - For recent years, leaders need 1 IP - per team game played |
| `SO/W` | `strikeouts_per_base_on_balls` | SO/W or SO/BB - For recent years, pitching leaders need 1 IP - per team game played. - No batting leaders computed. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Cy_Young_Voting

128 rows, 40 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Award` | `derived` | Award being voted on. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Rank` | `rank` | Finishing position in the voting. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Tm` | `team_ID` | Team as printed in the source table. |
| `Vote Pts` | `points_won` | MVP is currently 14-9-8-...-3-2-1 - Others are currently 5-3-1. |
| `1st Place` | `votes_first` | Number of first-place votes received. |
| `Share` | `share` | Awards Share - Vote Pts/Max Pts Possible - Unanimous choice would be 100%. |
| `WAR` | `WAR_pitch` | Wins Above Replacement for Pitchers - A single number that presents the number of wins the player added - to the team above what a replacement player (think AAA or AAAA) would add. This value includes defensive support and includes additional value for high leverage situations. - Scale: 8+ MVP Quality, 5+ All-Star Quality, 2+ Starter, - 0-2 Reserve, < 0 Replacement Level - Developed by Sean Smith of BaseballProjection.com |
| `W` | `W` | Wins |
| `L` | `L` | Losses |
| `W-L%` | `win_loss_perc` | Win-Loss Percentage - W / (W + L) - For players, leaders need one decision for every ten team games. - For managers, minimum to qualify for leading is 320 games. |
| `ERA` | `earned_run_avg` | 9 * ER / IP - For recent years, leaders need 1 IP - per team game played. - Bold indicates lowest ERA using current stats - Gold means awarded ERA title at end of year. |
| `G` | `G_p` | Games Played or Pitched |
| `GS` | `GS` | Games Started |
| `GF` | `GF` | Games Finished - Credited to the last pitcher to appear for a team in a game. - Complete Games are not counted as Games Finished. |
| `CG` | `CG` | Complete Game |
| `SHO` | `SHO` | Shutouts - No runs allowed and a complete game. |
| `SV` | `SV` | Saves |
| `IP` | `IP` | Innings Pitched |
| `H` | `H_p` | Hits/Hits Allowed |
| `R` | `R` | Runs Scored/Allowed |
| `ER` | `ER` | Earned Runs Allowed |
| `HR` | `HR_p` | Home Runs Hit/Allowed |
| `BB` | `BB_p` | Bases on Balls/Walks |
| `IBB` | `IBB` | Intentional Bases on Balls - First tracked in 1955. |
| `SO` | `SO_p` | Strikeouts |
| `HBP` | `HBP_p` | Times Hit by a Pitch. |
| `BK` | `BK` | Balks |
| `WP` | `WP` | Wild Pitches |
| `BF` | `batters_faced` | Batters Faced |
| `WHIP` | `whip` | (BB + H)/IP - For recent years, leaders need 1 IP - per team game played |
| `ERA+` | `earned_run_avg_plus` | ERA+ - 100*[lgERA/ERA] - Adjusted to the player’s ballpark(s). |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Debuts_Batting

1,545 rows, 35 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Yrs` | `experience` | Experience - Years the player was/has been in the major leagues. - 1st indicates their first year in the majors, - but does not indicate rookie status. - Includes parts of any seasons. |
| `From` | `year_min` | First Year |
| `To` | `year_max` | Last Year |
| `ASG` | `allstar_games` | All-Star Game Selections - This does not indicate if the player played or not. |
| `WAR/pos` | `WAR_bat` | Wins Above Replacement for position players - A single number that presents the number of wins the player added - to the team above what a replacement player (think AAA or AAAA) would add. - Scale: 8+ MVP Quality, 5+ All-Star Quality, 2+ Starter, - 0-2 Reserve, < 0 Replacement Level - Developed by Sean Smith of BaseballProjection.com |
| `G` | `G` | Games Played or Pitched |
| `PA` | `PA` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `AB` | `AB` | At Bats |
| `R` | `R` | Runs Scored/Allowed |
| `H` | `H` | Hits/Hits Allowed |
| `2B` | `2B` | Doubles Hit/Allowed |
| `3B` | `3B` | Triples Hit/Allowed |
| `HR` | `HR` | Home Runs Hit/Allowed |
| `RBI` | `RBI` | Runs Batted In |
| `SB` | `SB` | Stolen Bases |
| `CS` | `CS` | Caught Stealing |
| `BB` | `BB` | Bases on Balls/Walks |
| `SO` | `SO` | Strikeouts |
| `BA` | `batting_avg` | Hits/At Bats - For recent years, leaders need 3.1 PA - per team game played - Bold indicates either highest BA using current stats - or awarded title at end of year. |
| `OBP` | `onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) - For recent years, leaders need 3.1 PA - per team game played |
| `SLG` | `slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `OPS` | `onbase_plus_slugging` | On-Base + Slugging Percentages - For recent years, leaders need 3.1 PA - per team game played |
| `Debut` | `debut` | Date of Major League debut. |
| `Age` | `age` | Age of player on day of debut or final game or for season rookie status was lost |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Debuts_Bio

1,539 rows, 27 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Age` | `age` | Age of player on day of debut or final game, YY.DDD - Age on June 30th of debut season is used if exact debut date is unknown |
| `Debut` | `debut` | Date of Major League debut. |
| `Last Game` | `final_game` | Date of most recent Major League game. |
| `Pos` | `pos_season` | Position - ’*’ indicates position played in 2/3rds of team games, - ’/’ less than 10 games played. - Players can receive ’*’ if their combined OF games >= 2/3rds of team games. - ’H’ indicates games as a pinch-hitter or pinch-runner. |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `WAR` | `WAR` | Wins Above Replacement - A single number that presents the number of wins the player added - to the team above what a replacement player (think AAA or AAAA) would add. - Scale for a single-season: 8+ MVP Quality, 5+ All-Star Quality, 2+ Starter, - 0-2 Reserve, < 0 Replacement Level - Developed by Sean Smith of BaseballProjection.com |
| `Ht` | `height` | Height (ft & inches) |
| `Wt` | `weight` | Weight in Pounds |
| `B` | `bats` | Batting Side - B or S - Switch Hitter - This is their primary designation for their career |
| `T` | `throws` | Throwing Hand |
| `Birthdate` | `birthdate` | Date of birth. |
| `Birthplace` | `birthplace` | Place of birth. |
| `Draft/Signing` | `draft` | Draft or signing details. |
| `Schools` | `school` | College or school attended. |
| `High School` | `high_school` | High school attended. |
| `Given Name` | `name_given` | Full given name at birth. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Debuts_Pitching

983 rows, 41 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Yrs` | `experience` | Experience - Years the player was/has been in the major leagues. - 1st indicates their first year in the majors, - but does not indicate rookie status. - Includes parts of any seasons. |
| `From` | `year_min` | First Year |
| `To` | `year_max` | Last Year |
| `ASG` | `allstar_games` | All-Star Game Selections - This does not indicate if the player played or not. |
| `WAR` | `WAR_pitch` | Wins Above Replacement for Pitchers - A single number that presents the number of wins the player added - to the team above what a replacement player (think AAA or AAAA) would add. This value includes defensive support and includes additional value for high leverage situations. - Scale: 8+ MVP Quality, 5+ All-Star Quality, 2+ Starter, - 0-2 Reserve, < 0 Replacement Level - Developed by Sean Smith of BaseballProjection.com |
| `W` | `W` | Wins |
| `L` | `L` | Losses |
| `W-L%` | `win_loss_perc` | Win-Loss Percentage - W / (W + L) - For players, leaders need one decision for every ten team games. - For managers, minimum to qualify for leading is 320 games. |
| `ERA` | `earned_run_avg` | 9 * ER / IP - For recent years, leaders need 1 IP - per team game played. - Bold indicates lowest ERA using current stats - Gold means awarded ERA title at end of year. |
| `G` | `G` | Games Played or Pitched |
| `GS` | `GS` | Games Started |
| `GF` | `GF` | Games Finished - Credited to the last pitcher to appear for a team in a game. - Complete Games are not counted as Games Finished. |
| `CG` | `CG` | Complete Game |
| `SHO` | `SHO` | Shutouts - No runs allowed and a complete game. |
| `SV` | `SV` | Saves |
| `IP` | `IP` | Innings Pitched |
| `H` | `H` | Hits/Hits Allowed |
| `R` | `R` | Runs Scored/Allowed |
| `ER` | `ER` | Earned Runs Allowed |
| `HR` | `HR` | Home Runs Hit/Allowed |
| `BB` | `BB` | Bases on Balls/Walks |
| `IBB` | `IBB` | Intentional Bases on Balls - First tracked in 1955. |
| `SO` | `SO` | Strikeouts |
| `HBP` | `HBP` | Times Hit by a Pitch. |
| `BK` | `BK` | Balks |
| `WP` | `WP` | Wild Pitches |
| `BF` | `batters_faced` | Batters Faced |
| `WHIP` | `whip` | (BB + H)/IP - For recent years, leaders need 1 IP - per team game played |
| `Debut` | `debut` | Date of Major League debut. |
| `Age` | `age` | Age of player on day of debut or final game or for season rookie status was lost |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Free_Agent_Batting

256 rows, 32 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Age` | `age` | Player's age on July 1st of next season |
| `From Team` | `from_team_ID` | Club the player came from. |
| `WAR3` | `WAR` | WAR from last three years |
| `G` | `G` | Games Played or Pitched |
| `PA` | `PA` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `AB` | `AB` | At Bats |
| `R` | `R` | Runs Scored/Allowed |
| `H` | `H` | Hits/Hits Allowed |
| `2B` | `2B` | Doubles Hit/Allowed |
| `3B` | `3B` | Triples Hit/Allowed |
| `HR` | `HR` | Home Runs Hit/Allowed |
| `RBI` | `RBI` | Runs Batted In |
| `SB` | `SB` | Stolen Bases |
| `CS` | `CS` | Caught Stealing |
| `BB` | `BB` | Bases on Balls/Walks |
| `SO` | `SO` | Strikeouts |
| `BA` | `batting_avg` | Hits/At Bats - For recent years, leaders need 3.1 PA - per team game played - Bold indicates either highest BA using current stats - or awarded title at end of year. |
| `OBP` | `onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) - For recent years, leaders need 3.1 PA - per team game played |
| `SLG` | `slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `OPS` | `onbase_plus_slugging` | On-Base + Slugging Percentages - For recent years, leaders need 3.1 PA - per team game played |
| `Pos` | `pos` | Position |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Free_Agent_Pitching

444 rows, 36 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Age` | `age` | Player's age on July 1st of next season |
| `From Team` | `from_team_ID` | Club the player came from. |
| `WAR3` | `WAR` | WAR from last three years |
| `W` | `W` | Wins |
| `L` | `L` | Losses |
| `W-L%` | `win_loss_perc` | Win-Loss Percentage - W / (W + L) - For players, leaders need one decision for every ten team games. - For managers, minimum to qualify for leading is 320 games. |
| `ERA` | `earned_run_avg` | 9 * ER / IP - For recent years, leaders need 1 IP - per team game played. - Bold indicates lowest ERA using current stats - Gold means awarded ERA title at end of year. |
| `G` | `G` | Games Played or Pitched |
| `GS` | `GS` | Games Started |
| `GF` | `GF` | Games Finished - Credited to the last pitcher to appear for a team in a game. - Complete Games are not counted as Games Finished. |
| `CG` | `CG` | Complete Game |
| `SHO` | `SHO` | Shutouts - No runs allowed and a complete game. |
| `SV` | `SV` | Saves |
| `IP` | `IP` | Innings Pitched |
| `H` | `H` | Hits/Hits Allowed |
| `R` | `R` | Runs Scored/Allowed |
| `ER` | `ER` | Earned Runs Allowed |
| `HR` | `HR` | Home Runs Hit/Allowed |
| `BB` | `BB` | Bases on Balls/Walks |
| `IBB` | `IBB` | Intentional Bases on Balls - First tracked in 1955. |
| `SO` | `SO` | Strikeouts |
| `HBP` | `HBP` | Times Hit by a Pitch. |
| `BK` | `BK` | Balks |
| `WP` | `WP` | Wild Pitches |
| `BF` | `batters_faced` | Batters Faced |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Free_Agent_Signings

2,457 rows, 41 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Date` | `tran_date` | Date of Signing |
| `To Team` | `to_team_ID` | Club the player signed with. |
| `From Team` | `from_team_ID` | Club the player came from. |
| `Age` | `age` | Player's age on July 1st of next season |
| `WAR3` | `WAR` | WAR from last three years |
| `Yrs` | `experience` | Experience - Years the player was/has been in the major leagues. - 1st indicates their first year in the majors, - but does not indicate rookie status. - Includes parts of any seasons. |
| `G` | `G` | Games Played or Pitched |
| `AB` | `AB` | At Bats |
| `R` | `R` | Runs Scored/Allowed |
| `H` | `H` | Hits/Hits Allowed |
| `HR` | `HR` | Home Runs Hit/Allowed |
| `RBI` | `RBI` | Runs Batted In |
| `SB` | `SB` | Stolen Bases |
| `BB` | `BB` | Bases on Balls/Walks |
| `BA` | `batting_avg` | Hits/At Bats - For recent years, leaders need 3.1 PA - per team game played - Bold indicates either highest BA using current stats - or awarded title at end of year. |
| `OBP` | `onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) - For recent years, leaders need 3.1 PA - per team game played |
| `SLG` | `slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `OPS` | `onbase_plus_slugging` | On-Base + Slugging Percentages - For recent years, leaders need 3.1 PA - per team game played |
| `W` | `W` | Wins |
| `L` | `L` | Losses |
| `ERA` | `earned_run_avg` | 9 * ER / IP - For recent years, leaders need 1 IP - per team game played. - Bold indicates lowest ERA using current stats - Gold means awarded ERA title at end of year. |
| `WHIP` | `whip` | (BB + H)/IP - For recent years, leaders need 1 IP - per team game played |
| `G_2` | `G_p` | Games Played or Pitched |
| `GS` | `GS` | Games Started |
| `SV` | `SV` | Saves |
| `IP` | `IP` | Innings Pitched |
| `H_2` | `H_p` | Hits/Hits Allowed |
| `HR_2` | `HR_p` | Home Runs Hit/Allowed |
| `BB_2` | `BB_p` | Bases on Balls/Walks |
| `SO` | `SO_p` | Strikeouts |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### MVP_Voting

266 rows, 40 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Award` | `derived` | Award being voted on. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Rank` | `rank` | Finishing position in the voting. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Tm` | `team_ID` | Team as printed in the source table. |
| `Vote Pts` | `points_won` | MVP is currently 14-9-8-...-3-2-1 - Others are currently 5-3-1. |
| `1st Place` | `votes_first` | Number of first-place votes received. |
| `Share` | `share` | Awards Share - Vote Pts/Max Pts Possible - Unanimous choice would be 100%. |
| `WAR` | `WAR` | Wins Above Replacement - A single number that presents the number of wins the player added - to the team above what a replacement player (think AAA or AAAA) would add. - Scale for a single-season: 8+ MVP Quality, 5+ All-Star Quality, 2+ Starter, - 0-2 Reserve, < 0 Replacement Level - Developed by Sean Smith of BaseballProjection.com |
| `G` | `G` | Games Played or Pitched |
| `AB` | `AB` | At Bats |
| `R` | `R` | Runs Scored/Allowed |
| `H` | `H` | Hits/Hits Allowed |
| `HR` | `HR` | Home Runs Hit/Allowed |
| `RBI` | `RBI` | Runs Batted In |
| `SB` | `SB` | Stolen Bases |
| `BB` | `BB` | Bases on Balls/Walks |
| `BA` | `batting_avg` | Hits/At Bats - For recent years, leaders need 3.1 PA - per team game played - Bold indicates either highest BA using current stats - or awarded title at end of year. |
| `OBP` | `onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) - For recent years, leaders need 3.1 PA - per team game played |
| `SLG` | `slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `OPS` | `onbase_plus_slugging` | On-Base + Slugging Percentages - For recent years, leaders need 3.1 PA - per team game played |
| `W` | `W` | Wins |
| `L` | `L` | Losses |
| `ERA` | `earned_run_avg` | 9 * ER / IP - For recent years, leaders need 1 IP - per team game played. - Bold indicates lowest ERA using current stats - Gold means awarded ERA title at end of year. |
| `WHIP` | `whip` | (BB + H)/IP - For recent years, leaders need 1 IP - per team game played |
| `G_2` | `G_p` | Games Played or Pitched |
| `GS` | `GS` | Games Started |
| `SV` | `SV` | Saves |
| `IP` | `IP` | Innings Pitched |
| `H_2` | `H_p` | Hits/Hits Allowed |
| `HR_2` | `HR_p` | Home Runs Hit/Allowed |
| `BB_2` | `BB_p` | Bases on Balls/Walks |
| `SO` | `SO_p` | Strikeouts |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Manager_Of_The_Year_Voting

81 rows, 21 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Award` | `derived` | Award being voted on. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Rank` | `rank` | Finishing position in the voting. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Tm` | `team_ID` | Team as printed in the source table. |
| `Vote Pts` | `points_won` | MVP is currently 14-9-8-...-3-2-1 - Others are currently 5-3-1. |
| `1st Place` | `votes_first` | Number of first-place votes received. |
| `Share` | `share` | Awards Share - Vote Pts/Max Pts Possible - Unanimous choice would be 100%. |
| `W` | `W` | Wins |
| `L` | `L` | Losses |
| `W-L%` | `win_loss_perc` | Win-Loss Percentage - W / (W + L) - For players, leaders need one decision for every ten team games. - For managers, minimum to qualify for leading is 320 games. |
| `Ties` | `ties` | Ties - Prior to lights and tarps it was common for games - to be called on account of darkness or rain - and then replayed in full at a later date. - Game stats from ties still counted. - Some leagues also do not play unlimited numbers of innings. |
| `G` | `G` | Games Played or Pitched |
| `Finish` | `finish` | Team’s Finish - For career totals these are the average of all - years weighted by the number games played or managed. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Manager_Record

201 rows, 25 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Mgr` | `manager` | Manager. |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `W` | `W` | Wins |
| `L` | `L` | Losses |
| `W-L%` | `win_loss_perc` | Win-Loss Percentage - W / (W + L) - For players, leaders need one decision for every ten team games. - For managers, minimum to qualify for leading is 320 games. |
| `Ties` | `ties` | Ties - Prior to lights and tarps it was common for games - to be called on account of darkness or rain - and then replayed in full at a later date. - Game stats from ties still counted. - Some leagues also do not play unlimited numbers of innings. |
| `G` | `G` | Games Played or Pitched |
| `Finish` | `finish` | Team’s Finish - For career totals these are the average of all - years weighted by the number games played or managed. |
| `Wpost` | `W_post` | Postseason Wins |
| `Lpost` | `L_post` | Postseason Losses |
| `W-L%post` | `win_loss_perc_post` | Postseason Win-Loss Percentage - W / (W + L). |
| `Challenges` | `mgr_challenge_count` | Replay Challenges - The replay system was introduced in the 2014 season. |
| `Overturned` | `mgr_overturn_count` | Successful Replay Challenges - The replay system was introduced in the 2014 season. |
| `Overturn%` | `mgr_replay_success_rate` | Successful Replay Challenge Percentage - The replay system was introduced in the 2014 season. - Managers must have 10 challenges to qualify for leaderboards. |
| `Ejections` | `mgr_ejections` | Manager Ejections - Only includes ejections as manager. Excludes ejections as a player or as a coach. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Manager_Tendencies

201 rows, 36 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Mgr` | `manager` | Manager. |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `G` | `manager_games` | Games Managed |
| `Ch` | `steal_2b_chances` | Chances to steal second base - Plate appearances with a runner on first and no runner on second. |
| `Att` | `steal_2b_attempts` | Attempts to steal second base - Times a runner stole or was caught stealing second base. |
| `Rate` | `steal_2b_rate` | Rate of attempting to steal second base - Attempts to steal second base divided by chances to steal second base. |
| `Rate+` | `steal_2b_rate_plus` | League-adjusted steal of 2nd rate - 100*(Steal 2nd Rate)/(League Steal 2nd Rate) |
| `Ch_2` | `steal_3b_chances` | Chances to steal third base - Plate appearances with a runner on second and no runner on third. |
| `Att_2` | `steal_3b_attempts` | Attempts to steal third base - Times a runner stole or was caught stealing third base. |
| `Rate_2` | `steal_3b_rate` | Rate of attempting to steal third base - Attempts to steal third base divided by chances to steal third base. |
| `Rate+_2` | `steal_3b_rate_plus` | League-adjusted steal of 3rd rate - 100*(Steal 3rd Rate)/(League Steal 3rd Rate) |
| `Ch_3` | `sac_bunt_chances` | Chances to sacrifice bunt - Plate appearances with a runner on first and no runner on second, or a runner on second and no runner on third, and a non-pitcher at the plate. |
| `Att_3` | `sac_bunts` | Sacrifice bunts by non-pitchers |
| `Rate_3` | `sac_bunt_rate` | Rate of attempting a sacrifice bunt - Sacrifice bunts divided by chances to sacrifice. Does not account for unsuccessful attempts (foul bunts, missed bunts). |
| `Rate+_3` | `sac_bunt_rate_plus` | League-adjusted sac bunt rate - 100*(Sac Bunt Rate)/(League Sac Bunt Rate) |
| `PA` | `ibb_chances` | Plate Appearances |
| `IBB` | `ibb` | Intentional Walks |
| `Rate_4` | `ibb_rate` | Rate of issuing intentional walks - Intentional walks divided by plate apparances. |
| `Rate+_4` | `ibb_rate_plus` | League-adjusted IBB rate - 100*(IBB Rate)/(League IBB Rate) |
| `PH/G` | `pinch_hitters` | Pinch Hitters Used Per Game |
| `PH/G+` | `pinch_hitters_plus` | League-adjusted Pinch Hitters Used Per Game - 100*(Pinch hitters per game)/(League pinch hitters per game) |
| `PR/G` | `pinch_runners` | Pinch Runners Used Per Game |
| `PR/G+` | `pinch_runners_plus` | League-adjusted Pinch Runners Used Per Game - 100*(Pinch runners per game)/(League pinch runners per game) |
| `P/G` | `pitchers_used_per_game` | Pitchers Used Per Game |
| `P/G+` | `pitchers_used_per_game_plus` | League-adjusted Pitchers Used Per Game - 100*(Pitchers per game)/(League pitchers per game) |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Neutral_Batting

4,303 rows, 32 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Bats` | `derived` | Batting hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `G` | `G` | Games Played - This includes all times that the player appeared on the lineup card. Pitchers in non-DH games that appeared on the lineup card but didn't bat will still have a game in this column. |
| `PA` | `PA` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `AB` | `AB` | At Bats |
| `R` | `R` | Runs Scored/Allowed |
| `H` | `H` | Hits/Hits Allowed |
| `2B` | `2B` | Doubles Hit/Allowed |
| `3B` | `3B` | Triples Hit/Allowed |
| `HR` | `HR` | Home Runs Hit/Allowed |
| `RBI` | `RBI` | Runs Batted In |
| `SB` | `SB` | Stolen Bases |
| `CS` | `CS` | Caught Stealing |
| `BB` | `BB` | Bases on Balls/Walks |
| `SO` | `SO` | Strikeouts |
| `BA` | `batting_avg` | Hits/At Bats - For recent years, leaders need 3.1 PA - per team game played - Bold indicates either highest BA using current stats - or awarded title at end of year. |
| `OBP` | `onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) - For recent years, leaders need 3.1 PA - per team game played |
| `SLG` | `slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `OPS` | `onbase_plus_slugging` | On-Base + Slugging Percentages - For recent years, leaders need 3.1 PA - per team game played |
| `RC` | `RC` | Runs Created - A set of formulas developed by Bill James and others - that estimates a player’s total contributions - to a team’s runs total. - This is computed with the "technical" formula when possible. - If SB or CS data is missing, the "basic" formula is used. - If HBP, IBB, SH, SF, or GIDP data is missing, the "stolen base" version of the formula is used. - Team Runs Created is the sum of player Runs Created. |
| `Gact` | `G_actual` | Games Actual - Stats are adjusted to 162 games, but this is the - actual number of games for this player for this split. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Neutral_Pitching

5,101 rows, 33 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Throws` | `derived` | Throwing hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `W` | `W` | Wins |
| `L` | `L` | Losses |
| `W-L%` | `win_loss_perc` | Win-Loss Percentage - W / (W + L) - For players, leaders need one decision for every ten team games. - For managers, minimum to qualify for leading is 320 games. |
| `ERA` | `earned_run_avg` | 9 * ER / IP - For recent years, leaders need 1 IP - per team game played. - Bold indicates lowest ERA using current stats - Gold means awarded ERA title at end of year. |
| `IP` | `IP` | Innings Pitched |
| `H` | `H` | Hits/Hits Allowed |
| `R` | `R` | Runs Scored/Allowed |
| `ER` | `ER` | Earned Runs Allowed |
| `HR` | `HR` | Home Runs Hit/Allowed |
| `BB` | `BB` | Bases on Balls/Walks |
| `SO` | `SO` | Strikeouts |
| `HBP` | `HBP` | Times Hit by a Pitch. |
| `WHIP` | `whip` | (BB + H)/IP - For recent years, leaders need 1 IP - per team game played |
| `H9` | `hits_per_nine` | 9 x H / IP - For recent years, leaders need 1 IP - per team game played |
| `BB9` | `bases_on_balls_per_nine` | 9 x BB / IP - For recent years, leaders need 1 IP - per team game played |
| `SO9` | `strikeouts_per_nine` | 9 x SO / IP - For recent years, leaders need 1 IP - per team game played |
| `SO/W` | `strikeouts_per_base_on_balls` | SO/W or SO/BB - For recent years, pitching leaders need 1 IP - per team game played. - No batting leaders computed. |
| `HR9` | `home_runs_per_nine` | 9 x HR / IP - For recent years, leaders need 1 IP - per team game played |
| `BFP` | `BFP` | Batters faced by the pitcher. |
| `Gact` | `G_actual` | Games Actual - Stats are adjusted to 162 games, but this is the - actual number of games for this player for this split. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Opening_Day_Lineups

180 rows, 21 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `Lg` | `lg_ID` | League - AL - American League (1901-present) - NL - National League (1876-present) - AA - American Association (1882-1891) - UA - Union Association (1884) - PL - Players League (1890) - FL - Federal League (1914-1915) - NA - National Association (1871-1875) - ANL - American Negro League (1929) - ECL - Eastern Colored League (1923-1928) - EWL - East-West League (1932) - NAL - Negro American League (1937-1948) - NNL - Negro National League (1920-1931) - NN2 - Negro National League 2 (1933-1948) - NSL - Negro Southern League (1932) |
| `C` | `C` | Primary catcher. |
| `1B` | `1B` | Singles |
| `2B` | `2B` | Doubles |
| `3B` | `3B` | Triples |
| `SS` | `SS` | Primary shortstop. |
| `LF` | `LF` | Primary left fielder. |
| `CF` | `CF` | Primary center fielder. |
| `RF` | `RF` | Primary right fielder. |
| `P` | `P` | Primary pitcher. |
| `DH` | `DH` | Primary designated hitter. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Pitches_Batting

5,190 rows, 43 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Bats` | `derived` | Batting hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `PA` | `PA_pitch` | Plate Appearances - The number of plate appearances for which we have pitch-by-pitch data. - Note that inning-ending baserunning outs are counted as a PA, - So these may be larger than batting PAs. |
| `Pit` | `pitches` | Number of pitches in the PA. |
| `Pit/PA` | `pitches_per_pa` | Pitches per Plate Appearance |
| `Str` | `strikes_total` | Strikes - Includes both pitches in the zone and those swung at out of the zone. |
| `Str%` | `strike_perc` | Strike Percentage - Strikes / Total Pitches (intentional balls excluded). |
| `L/Str` | `strike_looking_perc` | Strikes Looking / Strikes - All strikes looking divided by all strikes. |
| `S/Str` | `strike_swinging_perc` | Swinging Strike Percentage - Strikes Swinging (w/o contact) / Total Strikes. |
| `F/Str` | `strike_foul_perc` | Foul Ball Strikes Percentage - Pitches Fouled Off / Total Strikes Seen. |
| `I/Str` | `strike_inplay_perc` | Ball In Play Percentage - Balls put into Play (including home runs) / Total Strikes. |
| `AS/Str` | `all_strikes_swinging_perc` | Swung at Strikes Percentage - (Inplay + Foul + Swinging Strikes) / Total Strikes. |
| `I/Bll` | `ball_intent_perc` | Intentional Ball Percentage - Intentional Balls / All Balls. |
| `AS/Pit` | `pitches_swinging_perc` | Percentage of Pitches Swung At - (Inplay + Foul + Swinging Strikes) / (Total Pitches - intentional balls). |
| `Con` | `contact_perc` | Contact Percentage - (Foul + Inplay Strikes) / (Foul + Inplay + Swinging Strikes). |
| `1stS` | `first_pitch_swings_perc` | First Pitch Swinging Percentage - First Pitch Swinging / PA. |
| `30%` | `30_pitches_perc` | 3-0 Count Seen Percentage - 3-0 Counts / PA. |
| `30c` | `30_pitches` | 3-0 counts seen |
| `30s` | `30_swings` | Swinging on a 3-0 Count |
| `20%` | `20_pitches_perc` | 2-0 Count Seen Percentage - 2-0 Counts / PA. |
| `20c` | `20_pitches` | 2-0 counts seen |
| `20s` | `20_swings` | Swinging on a 2-0 Count |
| `31%` | `31_pitches_perc` | 3-1 Count Seen Percentage - 3-1 Counts / PA. |
| `31c` | `31_pitches` | 3-1 counts seen |
| `31s` | `31_swings` | Swinging on a 3-1 Count |
| `L/SO` | `SO_looking` | Strikeouts Looking |
| `S/SO` | `SO_swinging` | Strikeouts Swinging |
| `L/SO%` | `SO_looking_perc` | Strikeout Looking Percentage - Strikeouts Looking / All Strikeouts. |
| `PAu` | `PA_unknown` | Plate Appearances for which data is not known - Note that for many stats (like pitcher SLG, 2B, 3B allowed, WPA, HR direction, etc.) - this will mean that the totals given are incomplete. |
| `Pitu` | `pitches_unknown` | Pitches for which ball-strike results are not known |
| `Stru` | `strikes_unknown` | Strikes for which detailed results are not known |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Pitches_Pitching

6,369 rows, 44 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Throws` | `derived` | Throwing hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `IP` | `IP` | Innings Pitched |
| `PA` | `PA_pitch` | Plate Appearances - The number of plate appearances for which we have pitch-by-pitch data. - Note that inning-ending baserunning outs are counted as a PA, - So these may be larger than batting PAs. |
| `Pit` | `pitches` | Number of pitches in the PA. |
| `Pit/PA` | `pitches_per_pa` | Pitches per Plate Appearance |
| `Str` | `strikes_total` | Strikes - Includes both pitches in the zone and those swung at out of the zone. |
| `Str%` | `strike_perc` | Strike Percentage - Strikes / Total Pitches (intentional balls excluded). |
| `L/Str` | `strike_looking_perc` | Strikes Looking / Strikes - All strikes looking divided by all strikes. |
| `S/Str` | `strike_swinging_perc` | Swinging Strike Percentage - Strikes Swinging (w/o contact) / Total Strikes. |
| `F/Str` | `strike_foul_perc` | Foul Ball Strikes Percentage - Pitches Fouled Off / Total Strikes Seen. |
| `I/Str` | `strike_inplay_perc` | Ball In Play Percentage - Balls put into Play (including home runs) / Total Strikes. |
| `AS/Str` | `all_strikes_swinging_perc` | Swung at Strikes Percentage - (Inplay + Foul + Swinging Strikes) / Total Strikes. |
| `I/Bll` | `ball_intent_perc` | Intentional Ball Percentage - Intentional Balls / All Balls. |
| `AS/Pit` | `pitches_swinging_perc` | Percentage of Pitches Swung At - (Inplay + Foul + Swinging Strikes) / (Total Pitches - intentional balls). |
| `Con` | `contact_perc` | Contact Percentage - (Foul + Inplay Strikes) / (Foul + Inplay + Swinging Strikes). |
| `1st%` | `first_pitch_strike_perc` | First Pitch Strike Percentage - Percentage of plate appearances that - began 0-1 or with a ball in play. |
| `30%` | `30_pitches_perc` | 3-0 Count Seen Percentage - 3-0 Counts / PA. |
| `30c` | `30_pitches` | 3-0 counts seen |
| `30s` | `30_strikes` | Strikes on a 3-0 Count |
| `02%` | `02_pitches_perc` | 0-2 Count Seen Percentage - 0-2 Counts / PA. |
| `02c` | `02_pitches` | 0-2 counts seen |
| `02s` | `02_strikes` | Strikes thrown on an 0-2 Count |
| `02h` | `02_hits` | Hits given up on an 0-2 Count |
| `L/SO` | `SO_looking` | Strikeouts Looking |
| `S/SO` | `SO_swinging` | Strikeouts Swinging |
| `L/SO%` | `SO_looking_perc` | Strikeout Looking Percentage - Strikeouts Looking / All Strikeouts. |
| `3pK` | `SO_3_pitches` | 3-Pitch Strikeouts |
| `4pW` | `BB_4_pitches` | 4-pitch Walks |
| `PAu` | `PA_unknown` | Plate Appearances for which data is not known - Note that for many stats (like pitcher SLG, 2B, 3B allowed, WPA, HR direction, etc.) - this will mean that the totals given are incomplete. |
| `Pitu` | `pitches_unknown` | Pitches for which ball-strike results are not known |
| `Stru` | `strikes_unknown` | Strikes for which detailed results are not known |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Playoff_Odds

216 rows, 33 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `rk` | `rk` | Rank. |
| `Tm` | `team_name` | Team as listed in the source table. |
| `Lg` | `lg_ID` | League - AL - American League (1901-present) - NL - National League (1876-present) - AA - American Association (1882-1891) - UA - Union Association (1884) - PL - Players League (1890) - FL - Federal League (1914-1915) - NA - National Association (1871-1875) - ANL - American Negro League (1929) - ECL - Eastern Colored League (1923-1928) - EWL - East-West League (1932) - NAL - Negro American League (1937-1948) - NNL - Negro National League (1920-1931) - NN2 - Negro National League 2 (1933-1948) - NSL - Negro Southern League (1932) |
| `D` | `division` | Division |
| `SRS` | `ppr_srs` | SRS over the past 100 team games - This value does not include the regression factor. |
| `rSOS` | `ppr_opp_srs` | Strength of Remaining Schedule - Average SRS value of team's remaining opponents. |
| `W` | `ppr_cur_w` | Current Wins |
| `L` | `ppr_cur_l` | Current Losses |
| `W_2` | `ppr_rem_w` | Average Remaining Wins |
| `L_2` | `ppr_rem_l` | Average Remaining Losses |
| `W_3` | `ppr_avg_w` | Average Wins |
| `L_3` | `ppr_avg_l` | Average Losses |
| `Best` | `ppr_best` | 95th Percentile Wins |
| `Worst` | `ppr_worst` | 5th Percentile Wins |
| `Post` | `ppr_postseason` | Made Postseason |
| `WC` | `ppr_wildcard` | Wild Card Team |
| `Div` | `ppr_division` | Won Division |
| `LDS` | `ppr_LDS` | Reached LDS |
| `LCS` | `ppr_LCS` | Reached LCS |
| `Pennant` | `ppr_WS` | Reached World Series |
| `Win WS` | `ppr_champs` | Won World Series |
| `1 Day` | `ppr_change_1day` | Change in postseason odds since yesterday |
| `7 Days` | `ppr_change_7day` | Change in postseason odds since 7 days ago |
| `30 Days` | `ppr_change_30day` | Change in postseason odds since 30 days ago |
| `Bye` | `ppr_bye` | Earned first round bye |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Playoff_Scenarios

12 rows, 17 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Lg` | `lg_ID` | League - AL - American League (1901-present) - NL - National League (1876-present) - AA - American Association (1882-1891) - UA - Union Association (1884) - PL - Players League (1890) - FL - Federal League (1914-1915) - NA - National Association (1871-1875) - ANL - American Negro League (1929) - ECL - Eastern Colored League (1923-1928) - EWL - East-West League (1932) - NAL - Negro American League (1937-1948) - NNL - Negro National League (1920-1931) - NN2 - Negro National League 2 (1933-1948) - NSL - Negro Southern League (1932) |
| `Top Seed` | `ppr_top_seed` | Top Seeded Division Winner |
| `Division Winner` | `ppr_div_win_1` | Division Winner |
| `Division Winner_2` | `ppr_div_win_2` | Division Winner |
| `Wild Card` | `ppr_wc_1` | Wild Card Team |
| `Wild Card_2` | `ppr_wc_2` | Wild Card Team |
| `Wild Card_3` | `ppr_wc_3` | Wild Card Team |
| `ppr_wc_4` | `ppr_wc_4` | Probability of finishing as the fourth wild card. |
| `ppr_wc_5` | `ppr_wc_5` | Probability of finishing as the fifth wild card. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Ratio_Batting

5,190 rows, 30 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Bats` | `derived` | Batting hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `PA` | `PA` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `HR%` | `home_run_perc` | Home Run Percentage - Percentage of all plate appearances a home run was hit. - (HR)/(all plate appearances) |
| `SO%` | `strikeout_perc` | Strikeout Percentage - Percentage of all plate appearances ending with a Strikeout. - (SO)/(all plate appearances) |
| `BB%` | `base_on_balls_perc` | Base on Balls Percentage - Percentage of all plate appearances ending with a Base on Balls. - (BB)/(all plate appearances) |
| `XBH%` | `extra_base_hit_perc` | Extra Base Hit Percentage - Percentage of all plate appearances ending with an Extra Base Hit. - (2B + 3B + HR)/(all plate appearances) |
| `X/H%` | `extra_base_hit_per_hit_perc` | Percentage of all hits for extra bases - Percentage of all hits resulting in extra bases. - (2B + 3B + HR) / H ) |
| `SO/W` | `strikeouts_per_base_on_balls` | SO/W or SO/BB - For recent years, pitching leaders need 1 IP - per team game played. - No batting leaders computed. |
| `AB/SO` | `at_bats_per_strikeout` | At Bats Per Strikeout - For career marks this only includes AB’s for seasons where SO’s were tracked. |
| `AB/HR` | `at_bats_per_home_run` | At Bats Per Home Run |
| `AB/RBI` | `at_bats_per_rbi` | At Bats Per Run Batted In |
| `GB/FB` | `gb_fb_ratio` | Ground Ball to Fly Ball Ratio - Includes line drives as fly balls. - Batted ball type and location is not complete prior to 1988. |
| `GO/AO` | `go_ao_ratio` | Ground Outs to Air Outs - Double plays count as two. - Batted ball type and location is not complete prior to 1988. |
| `IP%` | `inplay_perc` | Balls In-Play Percentage - Percentage of all plate appearances with ball put into play. - (AB-SO-HR+SF)/(all plate appearances) |
| `LD%` | `line_drive_perc` | Line Drive Percentage - Percentage of all balls put into play (including home runs) that are line drives. - Batted ball type and location is not complete prior to 1988. |
| `HR/FB` | `home_run_fb_perc` | Percentage of Fly Balls that were Home Runs - Includes all fly balls to the outfield including line drives. - Batted ball type and location is not complete prior to 1988. |
| `IF/FB` | `infield_fb_perc` | Percentage of Fly Balls that were on the infield - Includes Line Drives. - Batted ball type and location is not complete prior to 1988. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Ratio_Pitching

6,405 rows, 32 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Throws` | `derived` | Throwing hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `IP` | `IP` | Innings Pitched |
| `Ptn%` | `PA_with_platoon_adv_perc` | Percentage of PA with the platoon advantage - Switch hitters should be 100% for most cases. - For pitchers, facing a batter of the same hand. - For batters, facing a pitcher of the opposite hand. |
| `HR%` | `home_run_perc` | Home Run Percentage - Percentage of all plate appearances a home run was hit. - (HR)/(all plate appearances) |
| `SO%` | `strikeout_perc` | Strikeout Percentage - Percentage of all plate appearances ending with a Strikeout. - (SO)/(all plate appearances) |
| `BB%` | `base_on_balls_perc` | Base on Balls Percentage - Percentage of all plate appearances ending with a Base on Balls. - (BB)/(all plate appearances) |
| `SO-BB%` | `strikeout_minus_base_on_balls_perc` | Strikeout - Base on Balls Percentage - The differential of all batters faced between Strikeouts and Base on Balls - (SO-BB)/(all plate appearances) |
| `XBH%` | `extra_base_hit_perc` | Extra Base Hit Percentage - Percentage of all plate appearances ending with an Extra Base Hit. - (2B + 3B + HR)/(all plate appearances) |
| `X/H%` | `extra_base_hit_per_hit_perc` | Percentage of all hits for extra bases - Percentage of all hits resulting in extra bases. - (2B + 3B + HR) / H ) |
| `GB/FB` | `gb_fb_ratio` | Ground Ball to Fly Ball Ratio - Includes line drives as fly balls. - Batted ball type and location is not complete prior to 1988. |
| `GO/AO` | `go_ao_ratio` | Ground Outs to Air Outs - Double plays count as two. - Batted ball type and location is not complete prior to 1988. |
| `IP%` | `inplay_perc` | Balls In-Play Percentage - Percentage of all plate appearances with ball put into play. - (AB-SO-HR+SF)/(all plate appearances) |
| `LD%` | `line_drive_perc` | Line Drive Percentage - Percentage of all balls put into play (including home runs) that are line drives. - Batted ball type and location is not complete prior to 1988. |
| `HR/FB` | `home_run_fb_perc` | Percentage of Fly Balls that were Home Runs - Includes all fly balls to the outfield including line drives. - Batted ball type and location is not complete prior to 1988. |
| `IF/FB` | `infield_fb_perc` | Percentage of Fly Balls that were on the infield - Includes Line Drives. - Batted ball type and location is not complete prior to 1988. |
| `Opp` | `GIDP_opp` | Opportunity for a Grounded Into Double Play - Runner on first with less than two outs. |
| `DP` | `GIDP_suc` | Grounded Into Double Play - Two or more outs via force outs on a ground ball. |
| `%` | `GIDP_perc` | Grounded Into Double Play Rate - Two or more outs via force outs on a ground ball. |
| `PAu` | `PA_unknown` | Plate Appearances for which data is not known - Note that for many stats (like pitcher SLG, 2B, 3B allowed, WPA, HR direction, etc.) - this will mean that the totals given are incomplete. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Reliever_Pitching

5,284 rows, 45 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Throws` | `derived` | Throwing hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `IP` | `IP` | Innings Pitched |
| `G` | `G` | Games Played or Pitched |
| `GR` | `GR` | Games in Relief |
| `GF` | `GF` | Games Finished - Credited to the last pitcher to appear for a team in a game. - Complete Games are not counted as Games Finished. |
| `Wgr` | `W_GR` | Wins in relief |
| `Lgr` | `L_GR` | Losses in relief |
| `SVOpp` | `SvOpp` | Save Opportunities - This is Saves + Blown Saves. - 1973 and before, there are 90+ games where a pitcher earned the save - under the current rule, but was not credited with a save. |
| `SV` | `SV` | Saves |
| `BSv` | `BSv` | Blown Saves - Pitcher entered the game in a save situation and lost the lead. |
| `SV%` | `SvOpp_perc` | Save Percentage - Saves/Save Opportunities - Save Opportunities is Saves + Blown Saves. - 1973 and before, there are 90+ games where a pitcher earned the save - under the current rule, but was not credited with a save. |
| `SVSit` | `SvSit` | Save Situations - Pitcher entered the game after the fifth inning in a save situation. - Or pitcher entered earlier in the game and did not get the win. - When the starter did not go five innings, it is - possible to enter in a save situation and get the win. - Save Situation Defn. (any of three): - 1. team has a lead of no more - than three runs and and at least three outs remaining. - 2. The tying run is either on base, at bat or on deck. - 3. At three innings remain in the game. - For our purposes, a save situation is only one - of the first two. |
| `Hold` | `Hold` | Holds - Pitcher entered the game in a save situation and did not get - the win (due to < 5 IP by starter) or save. - The pitcher then retires at least one batter and leaves the game - without having relinquished the lead at any point. - A pitcher can get a hold and a loss, but not a hold and a win - or a hold and a save. |
| `IR` | `inherited_runners` | Inherited Runners - Number of runners on base when pitcher entered the game. |
| `IS` | `inherited_score` | Inherited Score - Number or percentage of runners on base when pitcher entered the game who subsequently scored. - These runners show up in the previous pitcher’s ERA. |
| `IS%` | `inherited_score_perc` | Inherited Score Percentage - Percentage of runners on base when pitcher entered the game who subsequently scored. - These runners show up in the previous pitcher’s ERA. |
| `1stIP` | `inning_first_mode` | Most Common Inning to Enter Game - Ties go to the later inning. |
| `aLI` | `leverage_index_avg` | Average Leverage Index - The average pressure the pitcher or batter saw in this game or season. - 1.0 is average pressure, below 1.0 is low pressure and above 1.0 is high pressure. |
| `LevHi` | `enter_leverage_high` | Games entered with High Leverage - The first PA of the pitcher’s appearance - has a leverage of 1.5 or higher. |
| `LevMd` | `enter_leverage_med` | Games entered with Medium Leverage - The first PA of the pitcher’s appearance - has a leverage between 0.7 and 1.5. |
| `LevLo` | `enter_leverage_low` | Games entered with Low Leverage - The first PA of the pitcher’s appearance - has a leverage of 0.7 or lower. |
| `Ahd` | `enter_ahead` | Games Entered with Lead - Pitcher entered the game with his team in the lead. |
| `Tie` | `enter_tied` | Games Entered Tied - Pitcher entered the game tied. |
| `Bhd` | `enter_behind` | Games Entered Behind - Pitcher entered the game with his team trailing. |
| `Runr` | `enter_runners_on` | Games Entered With Runners On - Pitcher entered the game with runners on base. |
| `Empt` | `enter_empty` | Games Entered With Bases Empty - Pitcher entered the game with no runners on base. |
| `>3o` | `IPouts_gt3` | Games the pitcher completed more than three outs |
| `<3o` | `IPouts_lt3` | Games the pitcher completed fewer than three outs |
| `IPmult` | `IP_multi` | Games the pitcher pitched in more than one inning |
| `0DR` | `DR_0` | Zero Days Rest - Times the pitcher pitched on consecutive days, or both ends of a doubleheader. |
| `Out/GR` | `outs_per_GR` | Average Outs Recorded per Game in Relief |
| `Pit/GR` | `pitches_per_GR` | Pitches per Game in Relief |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Rookie_Of_The_Year_Voting

105 rows, 40 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Award` | `derived` | Award being voted on. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Rank` | `rank` | Finishing position in the voting. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Tm` | `team_ID` | Team as printed in the source table. |
| `Vote Pts` | `points_won` | MVP is currently 14-9-8-...-3-2-1 - Others are currently 5-3-1. |
| `1st Place` | `votes_first` | Number of first-place votes received. |
| `Share` | `share` | Awards Share - Vote Pts/Max Pts Possible - Unanimous choice would be 100%. |
| `WAR` | `WAR` | Wins Above Replacement - A single number that presents the number of wins the player added - to the team above what a replacement player (think AAA or AAAA) would add. - Scale for a single-season: 8+ MVP Quality, 5+ All-Star Quality, 2+ Starter, - 0-2 Reserve, < 0 Replacement Level - Developed by Sean Smith of BaseballProjection.com |
| `G` | `G` | Games Played or Pitched |
| `AB` | `AB` | At Bats |
| `R` | `R` | Runs Scored/Allowed |
| `H` | `H` | Hits/Hits Allowed |
| `HR` | `HR` | Home Runs Hit/Allowed |
| `RBI` | `RBI` | Runs Batted In |
| `SB` | `SB` | Stolen Bases |
| `BB` | `BB` | Bases on Balls/Walks |
| `BA` | `batting_avg` | Hits/At Bats - For recent years, leaders need 3.1 PA - per team game played - Bold indicates either highest BA using current stats - or awarded title at end of year. |
| `OBP` | `onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) - For recent years, leaders need 3.1 PA - per team game played |
| `SLG` | `slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `OPS` | `onbase_plus_slugging` | On-Base + Slugging Percentages - For recent years, leaders need 3.1 PA - per team game played |
| `W` | `W` | Wins |
| `L` | `L` | Losses |
| `ERA` | `earned_run_avg` | 9 * ER / IP - For recent years, leaders need 1 IP - per team game played. - Bold indicates lowest ERA using current stats - Gold means awarded ERA title at end of year. |
| `WHIP` | `whip` | (BB + H)/IP - For recent years, leaders need 1 IP - per team game played |
| `G_2` | `G_p` | Games Played or Pitched |
| `GS` | `GS` | Games Started |
| `SV` | `SV` | Saves |
| `IP` | `IP` | Innings Pitched |
| `H_2` | `H_p` | Hits/Hits Allowed |
| `HR_2` | `HR_p` | Home Runs Hit/Allowed |
| `BB_2` | `BB_p` | Bases on Balls/Walks |
| `SO` | `SO_p` | Strikeouts |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Rookies_Batting

1,337 rows, 36 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Yrs` | `experience` | Experience - Years the player was/has been in the major leagues. - 1st indicates their first year in the majors, - but does not indicate rookie status. - Includes parts of any seasons. |
| `From` | `year_min` | First Year |
| `To` | `year_max` | Last Year |
| `ASG` | `allstar_games` | All-Star Game Selections - This does not indicate if the player played or not. |
| `WAR/pos` | `WAR_bat` | Wins Above Replacement for position players - A single number that presents the number of wins the player added - to the team above what a replacement player (think AAA or AAAA) would add. - Scale: 8+ MVP Quality, 5+ All-Star Quality, 2+ Starter, - 0-2 Reserve, < 0 Replacement Level - Developed by Sean Smith of BaseballProjection.com |
| `G` | `G` | Games Played or Pitched |
| `PA` | `PA` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `AB` | `AB` | At Bats |
| `R` | `R` | Runs Scored/Allowed |
| `H` | `H` | Hits/Hits Allowed |
| `2B` | `2B` | Doubles Hit/Allowed |
| `3B` | `3B` | Triples Hit/Allowed |
| `HR` | `HR` | Home Runs Hit/Allowed |
| `RBI` | `RBI` | Runs Batted In |
| `SB` | `SB` | Stolen Bases |
| `CS` | `CS` | Caught Stealing |
| `BB` | `BB` | Bases on Balls/Walks |
| `SO` | `SO` | Strikeouts |
| `BA` | `batting_avg` | Hits/At Bats - For recent years, leaders need 3.1 PA - per team game played - Bold indicates either highest BA using current stats - or awarded title at end of year. |
| `OBP` | `onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) - For recent years, leaders need 3.1 PA - per team game played |
| `SLG` | `slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `OPS` | `onbase_plus_slugging` | On-Base + Slugging Percentages - For recent years, leaders need 3.1 PA - per team game played |
| `Debut` | `debut` | Date of Major League debut. |
| `Age` | `age` | Age of player on day of debut or final game or for season rookie status was lost |
| `Tm` | `team_ID` | Teams played for in this rookie season given players can have multiple seasons as a rookie |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Rookies_Pitching

885 rows, 42 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Yrs` | `experience` | Experience - Years the player was/has been in the major leagues. - 1st indicates their first year in the majors, - but does not indicate rookie status. - Includes parts of any seasons. |
| `From` | `year_min` | First Year |
| `To` | `year_max` | Last Year |
| `ASG` | `allstar_games` | All-Star Game Selections - This does not indicate if the player played or not. |
| `WAR` | `WAR_pitch` | Wins Above Replacement for Pitchers - A single number that presents the number of wins the player added - to the team above what a replacement player (think AAA or AAAA) would add. This value includes defensive support and includes additional value for high leverage situations. - Scale: 8+ MVP Quality, 5+ All-Star Quality, 2+ Starter, - 0-2 Reserve, < 0 Replacement Level - Developed by Sean Smith of BaseballProjection.com |
| `W` | `W` | Wins |
| `L` | `L` | Losses |
| `W-L%` | `win_loss_perc` | Win-Loss Percentage - W / (W + L) - For players, leaders need one decision for every ten team games. - For managers, minimum to qualify for leading is 320 games. |
| `ERA` | `earned_run_avg` | 9 * ER / IP - For recent years, leaders need 1 IP - per team game played. - Bold indicates lowest ERA using current stats - Gold means awarded ERA title at end of year. |
| `G` | `G` | Games Played or Pitched |
| `GS` | `GS` | Games Started |
| `GF` | `GF` | Games Finished - Credited to the last pitcher to appear for a team in a game. - Complete Games are not counted as Games Finished. |
| `CG` | `CG` | Complete Game |
| `SHO` | `SHO` | Shutouts - No runs allowed and a complete game. |
| `SV` | `SV` | Saves |
| `IP` | `IP` | Innings Pitched |
| `H` | `H` | Hits/Hits Allowed |
| `R` | `R` | Runs Scored/Allowed |
| `ER` | `ER` | Earned Runs Allowed |
| `HR` | `HR` | Home Runs Hit/Allowed |
| `BB` | `BB` | Bases on Balls/Walks |
| `IBB` | `IBB` | Intentional Bases on Balls - First tracked in 1955. |
| `SO` | `SO` | Strikeouts |
| `HBP` | `HBP` | Times Hit by a Pitch. |
| `BK` | `BK` | Balks |
| `WP` | `WP` | Wild Pitches |
| `BF` | `batters_faced` | Batters Faced |
| `WHIP` | `whip` | (BB + H)/IP - For recent years, leaders need 1 IP - per team game played |
| `Debut` | `debut` | Date of Major League debut. |
| `Age` | `age` | Age of player on day of debut or final game or for season rookie status was lost |
| `Tm` | `team_ID` | Teams played for in this rookie season given players can have multiple seasons as a rookie |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Sabermetric_Batting

6,174 rows, 37 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Bats` | `derived` | Batting hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `PA` | `PA` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `Outs` | `outs_made` | Outs Made - (At Bats - Hits) + Double Plays Grounded Into - + Sac. Flies + Sac. Hits + Caught Stealing. |
| `RC` | `RC` | Runs Created - A set of formulas developed by Bill James and others - that estimates a player’s total contributions - to a team’s runs total. - This is computed with the "technical" formula when possible. - If SB or CS data is missing, the "basic" formula is used. - If HBP, IBB, SH, SF, or GIDP data is missing, the "stolen base" version of the formula is used. - Team Runs Created is the sum of player Runs Created. |
| `RC/G` | `RCpG` | Runs Created per Game - Runs created per (approximately) 27 outs used. - Can be thought of as the runs produced by a lineup of 9 of this player. |
| `AIR` | `batter_air` | Hitting AIR - measures the offensive level of the leagues and parks the - player played in relative to an all-time - average of a .335 OBP and .400 Slugging Percentage. Over 100 - indicates a favorable setting for hitters, under 100 a favorable - setting for pitchers. |
| `BAbip` | `batting_avg_bip` | Batting Avg. on Balls in Plays (Hits - Home Runs)/(At Bats - SO - HR + Sac Flies) - This also measures how effectively the - defense turned balls into outs. |
| `BA` | `batting_avg` | Hits/At Bats - For recent years, leaders need 3.1 PA - per team game played - Bold indicates either highest BA using current stats - or awarded title at end of year. |
| `lgBA` | `batting_avg_lg` | League Batting Average - The batting average a league average - (non-pitcher) would have had in the same park(s). |
| `OBP` | `onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) - For recent years, leaders need 3.1 PA - per team game played |
| `lgOBP` | `onbase_perc_lg` | League On-base Percentage - The on-base percentage a league average - (non-pitcher) would have had in the same park(s). |
| `SLG` | `slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `lgSLG` | `slugging_perc_lg` | League Slugging Percentage - The slugging percentage a league average - (non-pitcher) would have had in the same park(s). |
| `OPS` | `onbase_plus_slugging` | On-Base + Slugging Percentages - For recent years, leaders need 3.1 PA - per team game played |
| `lgOPS` | `onbase_plus_slugging_lg` | League On-Base + Slugging - The OPS a league average - (non-pitcher) would have had in the same park(s). |
| `OPS+` | `onbase_plus_slugging_plus` | OPS+ - 100*[OBP/lg OBP + SLG/lg SLG - 1] - Adjusted to the player’s ballpark(s) |
| `OWn%` | `offensive_winning_perc` | Offensive Winning Percentage - The percentage of games a team with nine of this player - batting would win. Assumes average pitching and defense. - This uses the Pythagorean win pct formula with the player's RC/G for runs scored and the league's R/9 as runs allowed. |
| `BtRuns` | `abRuns` | Adjusted Batting Runs - A set of formulas developed by Gary Gillette, Pete Palmer and others - that estimates a player’s total contributions - to a team’s runs total via linear weights. - 0.0 is an avg performance, <0 is worse than avg and >0 is better than avg |
| `BtWins` | `abWins` | Adjusted Batting Wins - A set of formulas developed by Gary Gillette, Pete Palmer and others - that estimates a player’s total contributions - to a team’s wins with his bat. - 0.0 is an avg performance, <0 is worse than avg and >0 is better than avg |
| `TotA` | `total_avg` | Total Average - Developed by Thomas Boswell of the Washington Post - (Total Bases + HBP + BB + SB) / (AB - H + CS + GIDP) |
| `SecA` | `secondary_avg` | Secondary Average - (Total Bases - Hits + BB + SB - CS) / AB - Over .500, excellent; < 200, poor |
| `ISO` | `isolated_slugging_perc` | (Total Bases - H)/At Bats or - (2B + 2*3B + 3*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `PwrSpd` | `power_speed_number` | Power/Speed Number - 2 x (Home Runs x Stolen Bases)/(Stolen Bases + Home Runs) - The harmonic mean of HR and SB. - To do well you need a lot of both. - Developed by Bill James. |
| `Pos Summary` | `pos_summary` | Positions Played - The positions either followed by the games played at that position - or in order of games or innings played. - For a single season, * indicates they played at least 2/3rds of the team games there. - Positions after / indicate less than ten games played at those positions. - For career, a + sign means more than 300 games at that position and - a - sign means less than 30 games. - 'H' indicates games as a pinch-hitter or pinch-runner. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Situational_Batting

5,190 rows, 52 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Bats` | `derived` | Batting hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `PA` | `PA` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `PA_2` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `Ptn%` | `PA_with_platoon_adv_perc` | Percentage of PA with the platoon advantage - Switch hitters should be 100% for most cases. - For pitchers, facing a batter of the same hand. - For batters, facing a pitcher of the opposite hand. |
| `H` | `H_all` | All Hits |
| `Inf` | `H_inf` | Infield Hits - Batted ball type and location is not complete prior to 1988. |
| `Bnt` | `H_bunt` | Bunt Hits - Batted ball type and location is not complete prior to 1988. |
| `AB` | `PH_ab` | Pinch Hit At Bats |
| `H_2` | `PH_h` | Pinch Hits |
| `HR` | `PH_hr` | Pinch Hit Home Runs |
| `RBI` | `PH_rbi` | Pinch Hit Runs Batted In |
| `PHlev` | `PH_leverage` | Pinch Hit Leverage Index - The importance of the context in which the Pinch Hitter was used - Above one means higher than average pressure. - Below one means lower than average pressure. |
| `All` | `HR_all` | Home Run Total |
| `GS` | `HR_gs` | Grand Slam Home Runs |
| `GSo` | `HR_gs_opp` | Grand Slam Opportunities - Plate Appearances with the Bases Loaded |
| `vRH` | `HR_vrh` | Home Runs off Right-Handers |
| `vLH` | `HR_vlh` | Home Runs off Left-Handers |
| `Hm` | `HR_hm` | Home Runs at Home |
| `Rd` | `HR_rd` | Home Runs on the Road |
| `IP` | `HR_iphr` | Inside-The-Park Home Runs - Note that batted ball type and location data is incomplete prior to 1988. |
| `Att` | `SH_att` | Sacrifice Bunts Attempted - Only includes unsuccessful bunts made and bunt strikeouts. - Failing to bunt early in the count and then swinging away later are not included. - Pre-1954 SH attempt counts are unavailable. |
| `Suc` | `SH_suc` | Successful Sacrifice Bunts |
| `%` | `SH_perc` | Sacrifice Bunts Success Rate - Only includes unsuccessful bunts made and bunt strikeouts. - Failing to bunt early in the count and then swinging away later are not included. - Pre-1954 SH attempt counts are unavailable. |
| `Opp` | `GIDP_opp` | Opportunity for a Grounded Into Double Play - Runner on first with less than two outs. |
| `DP` | `GIDP_suc` | Grounded Into Double Play - Two or more outs via force outs on a ground ball. |
| `%_2` | `GIDP_perc` | Grounded Into Double Play Rate - Two or more outs via force outs on a ground ball. |
| `Opp_2` | `productive_outs_opp` | Productive Outs Made or Failed - Created by Elias and ESPN for three possible situations. - Successful Sac for a pitcher with one out. - Advancing any runner with none out. - Driving in a baserunner with the second out of the inning. - Failed means the batter made an out without advancing the runner(s). |
| `Suc_2` | `productive_outs` | Productive Outs Made - Created by Elias and ESPN for three possible situations. - Successful Sac for a pitcher with one out. - Advancing any runner with none out. - Driving in a baserunner with the second out of the inning. - Failed means the batter made an out without advancing the runner(s). |
| `%_3` | `productive_outs_perc` | Productive Outs Percentage - Created by Elias and ESPN for three possible situations. - Successful Sac for a pitcher with one out. - Advancing any runner with none out. - Driving in a baserunner with the second out of the inning. - Failed means the batter made an out without advancing the runner(s). |
| `BR` | `baserunners_tot` | Total Number of Baserunners when batter at plate |
| `BRS` | `drove_in_tot` | Baserunners who Scored - Total runners scored by batter (may not be by RBIs) |
| `BRS%` | `baserunners_scored_perc` | Percentage of all baserunners who scored on the batter’s play - (not necessarily with an RBI). |
| `<2,3B` | `lt_2_out_on_third_opp` | PAs with less than two out, runner on third |
| `Scr` | `lt_2_out_on_third_scored` | PAs with less than two out, runner on third and runner scored |
| `%_4` | `lt_2_out_on_third_perc` | PAs with less than two out, runner on third and runner scored |
| `0,2B` | `no_out_on_second_opp` | PAs with no out, runner on second |
| `Adv` | `no_out_on_second_adv` | PAs with none out, runner on second and runner advanced |
| `%_5` | `no_out_on_second_perc` | PAs with none out, runner on second and runner advanced Rate |
| `PAu` | `PA_unknown` | Plate Appearances for which data is not known - Note that for many stats (like pitcher SLG, 2B, 3B allowed, WPA, HR direction, etc.) - this will mean that the totals given are incomplete. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Standard_Fielding_By_Position

18,324 rows, 53 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `Lg` | `lg_ID` | League - AL - American League (1901-present) - NL - National League (1876-present) - AA - American Association (1882-1891) - UA - Union Association (1884) - PL - Players League (1890) - FL - Federal League (1914-1915) - NA - National Association (1871-1875) - ANL - American Negro League (1929) - ECL - Eastern Colored League (1923-1928) - EWL - East-West League (1932) - NAL - Negro American League (1937-1948) - NNL - Negro National League (1920-1931) - NN2 - Negro National League 2 (1933-1948) - NSL - Negro Southern League (1932) |
| `G` | `G` | Games Played or Pitched |
| `GS` | `GS` | Games Started |
| `CG` | `CG` | Complete Game |
| `Inn` | `Inn_def` | Innings Played in Field |
| `Ch` | `chances` | Defensive Chances - Putouts + Assists + Errors |
| `PO` | `PO` | Putouts |
| `A` | `A` | Assists |
| `E` | `E_def` | Errors Committed |
| `DP` | `DP_def` | Double Plays Turned |
| `Fld%` | `fielding_perc` | Fielding Percentage - (Putouts + Assists) / (Putouts + Assists + Errors) |
| `Rtot` | `tz_runs_total` | Total Zone Total Fielding Runs Above Avg - The number of runs above or below average the player was worth based on the number of plays made. - This number combines the R tz , R dp , R of , R catch numbers into a total defensive contribution. - See the glossary section for a more complete explanation. - Provided by BaseballProjection.com |
| `Rtot/yr` | `tz_runs_total_per_season` | Total Zone Total Fielding Runs Above Avg per 1,200 Inn - The number of runs above or below average the fielder was worth per 1,200 Innings (approx 135 games). - This number combines the R tz , R dp , R of , R catch numbers into a total defensive contribution. - See the glossary section for a more complete explanation. - Provided by BaseballProjection.com |
| `Rtz` | `tz_runs_field` | Total Zone Fielding Runs Above Avg - The number of runs above or below average the player was worth based on fielding plays made. - This number does not include OF kills, or double plays turned. - See the glossary section for a more complete explanation. - Provided by BaseballProjection.com |
| `Rdp` | `tz_runs_infield` | Total Zone Infield Double Play Runs Above Avg - The number of runs above or below average the player was worth based on double plays turned and opportunities given. - See the glossary section for a more complete explanation. - Provided by BaseballProjection.com |
| `Rdrs` | `bis_runs_total` | BIS Defensive Runs Saved Above Avg - The number of runs above or below average the player was worth based on their overall defense. - This number combines the R pm , R dp , and R good numbers into a total defensive contribution. - Provided by Baseball Info Solutions |
| `Rdrs/yr` | `bis_runs_total_per_season` | BIS Defensive Runs Saved Above Avg per 1,200 Inn - The number of runs above or below average the fielder was worth per 1,200 Innings (approx 135 games). - This number combines the R pm , R dp , and R good numbers into a total defensive contribution. - For pitchers, this is set to 200 Innings. - Provided by Baseball Info Solutions |
| `Rpm` | `bis_runs_field` | BIS Plus/Minus Fielding Runs Above Avg - The number of runs above or below average the player was worth based on fielding plays made. - This number combines the R range , R air , and R throw numbers. - This number does not include OF kills, or double plays turned. - Provided by Baseball Info Solutions |
| `Rgood` | `bis_runs_good_plays` | BIS Good Plays/Misplays Runs Above Avg - The number of runs above or below average the player was worth based on plays where they made an exceptional contribution or obviously misplayed the situation. - Provided by Baseball Info Solutions |
| `Rair` | `bis_runs_air` | BIS Infield Air Ball Runs Above Avg - The number of runs above or below average the player was worth based on infield air balls. - Provided by Baseball Info Solutions |
| `Rrange` | `bis_runs_range` | BIS Infield Range Runs Above Avg - The number of runs above or below average the player was worth based on his performance between when the ball was hit and when the fielder gets to the ball (or fails to). - Provided by Baseball Info Solutions |
| `Rthrow` | `bis_runs_throwing` | BIS Infield Throwing Runs Above Avg - The number of runs above or below average the player was worth based on how he completes the play given where he fielded the ball, how hard it was hit, and the speed of the runner. - Provided by Baseball Info Solutions |
| `Rbnt` | `bis_runs_bunts` | BIS Bunts Fielded Runs Above Avg - The number of runs above or below average the player was worth solely on bunts. - Provided by Baseball Info Solutions |
| `RF/9` | `range_factor_per_nine` | Range Factor per 9 Inn - 9 * (Putouts + Assists) / Innings Played |
| `RF/G` | `range_factor_per_game` | Range Factor per Game - (Putouts + Assists) / Games Played |
| `Rdp_2` | `bis_runs_infield` | BIS Infield Double Play Runs Above Avg - The number of runs above or below average the player was worth based on double plays turned and opportunities given. - Provided by Baseball Info Solutions |
| `Rctch` | `tz_runs_catcher` | Total Zone Catcher Runs Above Avg - The number of runs above or below average the catcher was worth based on baserunner kills and baserunner advances. - See the glossary section for a more complete explanation. - Provided by BaseballProjection.com |
| `RszC` | `bis_runs_catcher_sz` | BIS Catcher Strike Zone Runs Above Avg - The number of runs above or below average the catcher was worth based on catcher framing. - Provided by Baseball Info Solutions |
| `RsbC` | `bis_runs_catcher_sb` | BIS Catcher Runs Above Avg - The number of runs above or below average the catcher was worth based on baserunner kills and baserunner advances. - Provided by Baseball Info Solutions |
| `RerC` | `bis_runs_catcher_er` | BIS Catcher Pitch Calling Runs Above Avg - The number of runs above or below average the catcher was for the pitcher ERA. - Provided by Baseball Info Solutions |
| `PB` | `PB` | Passed Balls |
| `WP` | `WP` | Wild Pitches |
| `SB` | `SB` | Stolen Bases |
| `CS` | `CS` | Caught Stealing |
| `CS%` | `caught_stealing_perc` | Caught Stealing Percentage - CS / (SB + CS) |
| `Rof` | `tz_runs_outfield` | Total Zone Outfield Arm Runs Above Avg - The number of runs above or below average the player was worth based on baserunner kills and baserunner advances. - See the glossary section for a more complete explanation. - Provided by BaseballProjection.com |
| `Rof_2` | `bis_runs_outfield` | BIS Outfield Arm Runs Above Avg - The number of runs above or below average the player was worth based on baserunner kills and baserunner advance. - Provided by Baseball Info Solutions |
| `RsbP` | `bis_runs_pitcher_sb` | BIS Pitcher SB Runs Above Avg - The number of runs above or below average the pitcher was worth based on baserunner kills and baserunner advances. - Provided by Baseball Info Solutions |
| `PO_2` | `pickoffs` | Pickoffs - Runner picked off a base. May include cases they were safe on an error. - Also includes Pickoff Caught Stealing plays. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Starter_Pitching

2,508 rows, 47 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Throws` | `derived` | Throwing hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `IP` | `IP` | Innings Pitched |
| `G` | `G` | Games Played or Pitched |
| `GS` | `GS` | Games Started |
| `Wgs` | `W_GS` | Wins in games started |
| `Lgs` | `L_GS` | Losses in games started |
| `ND` | `no_decision_GS` | No Decisions in Games Started |
| `Wchp` | `W_cheap` | Cheap Wins - Wins in starts with < 6 IP or more than 3 ER - Or wins in non-quality starts. |
| `Ltuf` | `L_tough` | Tough Losses - Losses in quality starts |
| `Wtm` | `W_team` | Team Wins in games started |
| `Ltm` | `L_team` | Team Losses in games started |
| `tmW-L%` | `win_loss_perc_team` | Team Win-Loss Percentage - Wtm / (Wtm + Ltm) - The win-loss percentage of the team in games started by this pitcher. |
| `Wlst` | `W_lost` | Wins Lost - At the time the pitcher faced his final batter - the pitcher was in position for a win, - but game was blown by bullpen. |
| `Lsv` | `L_saved` | Losses Saved - At the time of his last batter - the pitcher was in position for a loss, - but team came back to tie or take lead. |
| `CG` | `CG` | Complete Game |
| `SHO` | `SHO` | Shutouts - No runs allowed and a complete game. |
| `QS` | `QS` | Quality Start - Pitcher pitched at least 6 innings - and allowed 3 or fewer earned runs in a start. |
| `QS%` | `quality_start_perc` | Quality Start Percentage - Percentage of starts that were quality starts (≥ 6 IP, ≤ 3 ER). |
| `GmScA` | `game_score_avg` | Average Game Score |
| `Best` | `game_score_best` | Best Game Score |
| `Wrst` | `game_score_worst` | Worst Game Score |
| `BQR` | `bequeathed_runners` | Bequeathed Runners - Number of runners on base when pitcher left the game. - This includes both starts and games in relief. |
| `BQS` | `bequeathed_score` | Bequeathed Runners Score - Number or percentage of runners on base when pitcher left the game who subsequently scored. - These runners show up in the pitcher’s ERA. - This includes both starts and games in relief. |
| `sDR` | `DR_short` | Short Days Rest - Less than four days rest. |
| `lDR` | `DR_long` | Long Days Rest - More than four days rest. |
| `RS/GS` | `run_support_cg` | Run Support per Game - Runs scored/27 outs in the entire - game when the pitcher started. |
| `RS/IP` | `run_support_pg` | Run Support per Innings - Runs scored/27 outs while the pitcher was in the game as the pitcher. |
| `IP/GS` | `innings_per_start` | Innings Pitched per Game Started |
| `Pit/GS` | `pitches_per_start` | Pitches per Game Started |
| `<80` | `pitches_lt80` | GS with under 80 pitches |
| `80-99` | `pitches_80to99` | GS with 80 to 99 pitches |
| `100-119` | `pitches_100to119` | GS with 100 to 119 pitches |
| `≥120` | `pitches_ge120` | GS with 120 or more pitches |
| `Max` | `pitches_max` | Most pitches in a start |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Advanced_Batting

192 rows, 31 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `rOBA` | `rOBA` | rOBA - A measure of a player's offensive contributions, weighted in proportion to each event's actual run value |
| `Rbat+` | `Rbat_plus` | Rbat+ - Batting runs as computed for WAR, but indexed to the environment the player played in, where 100 is league average. |
| `BAbip` | `adv_bat_babip` | Batting Avg. on Balls in Plays (Hits - Home Runs)/(At Bats - SO - HR + Sac Flies) - This also measures how effectively the - defense turned balls into outs. |
| `ISO` | `adv_bat_iso` | (Total Bases - H)/At Bats or - (2B + 2*3B + 3*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `HR%` | `adv_bat_home_run_perc` | Home Run Percentage - Percentage of all plate appearances a home run was hit. - (HR)/(all plate appearances) |
| `SO%` | `adv_bat_strikeout_perc` | Strikeout Percentage - Percentage of all plate appearances ending with a Strikeout. - (SO)/(all plate appearances) |
| `BB%` | `adv_bat_base_on_balls_perc` | Base on Balls Percentage - Percentage of all plate appearances ending with a Base on Balls. - (BB)/(all plate appearances) |
| `EV` | `adv_bat_exit_velo` | Average Exit Velocity - Average speed of the ball off the bat for balls put into play, measured in miles per hour. |
| `HardH%` | `adv_bat_hard_hit_perc` | Hard Hit Rate - Percent of balls in play with an exit velocity of 95 mph or more. |
| `LD%` | `adv_bat_ld_perc` | Line Drive Percentage - Percentage of all balls put into play (including home runs) that are line drives. - Batted ball type and location is not complete prior to 1988. |
| `GB%` | `adv_bat_gb_perc` | Ground Ball Percentage - Percentage of all balls put into play (including home runs) that are ground balls. - EXCLUDES Bunts - Batted ball type and location is not complete prior to 1988. |
| `FB%` | `adv_bat_fb_perc` | Fly Ball Percentage - Percentage of all balls put into play (including home runs) that are fly balls. - EXCLUDES Popups - Batted ball type and location is not complete prior to 1988. |
| `GB/FB` | `adv_bat_gb_fb_ratio` | Ground Ball to Fly Ball Ratio - Includes line drives as fly balls. - Batted ball type and location is not complete prior to 1988. |
| `Pull%` | `adv_bat_pull_perc` | Pull Percentage - Percentage of all balls put into play (including home runs) that are hit to the batter's pull side. - Batted ball type and location is not complete prior to 1988. |
| `Cent%` | `adv_bat_cent_perc` | Center Percentage - Percentage of all balls put into play (including home runs) that are hit to the center of the field. - Batted ball type and location is not complete prior to 1988. |
| `Oppo%` | `adv_bat_oppo_perc` | Opposite-Field Percentage - Percentage of all balls put into play (including home runs) that are hit to the batter's opposite (push) side. - Batted ball type and location is not complete prior to 1988. |
| `WPA` | `adv_bat_wpa_bat` | Win Probability Added for Offensive Player - Given average teams, this is the change in probability - caused by this batter during the game. - See Win Expectancy explainer for details. |
| `cWPA` | `adv_bat_cwpa_bat` | Championship Win Probability Added for Offensive Player - Given average teams, this is the change in probability of winning the World Series, displayed in percentage points. - See Win Expectancy explainer for details. |
| `RE24` | `adv_bat_re24_bat` | Base-Out Runs Added - Given the bases occupied/out situation, how many runs did the batter - or baserunner add in the resulting play. - Compared to average, so 0 is average, and above 0 is better than average |
| `RS%` | `adv_bat_runs_scored_perc` | Run Scoring Percentage - Percentage of times a baserunner eventually scores a run. - (R - HR) / (H + HBP + BB - HR + G_pr) |
| `SB%` | `adv_bat_stolen_base_perc` | Stolen Base Percentage - SB / (SB + CS) |
| `XBT%` | `adv_bat_extra_bases_taken_perc` | Extra Bases Taken Percentage - Percentage of times the runner advanced more than one base on a single or more than two bases on a double, when possible. - Does not take into account the location or type of the ball in play. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Advanced_Fielding_1B

192 rows, 43 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `RHB%` | `PA_with_rhb_perc` | Percentage of PAs with a Right-Handed Batter |
| `BIP%` | `PA_with_bip_perc` | Percentage of PAs that ended with ball in play |
| `GBIP%` | `PA_with_gbip_perc` | Percentage of PAs that ended with ground ball in play (not a bunt). |
| `Fld` | `inplay_fielded` | Number of balls fielded - For many years, the fielder for non-out plays is - unknown and this information will not be presented. |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `FC` | `FC` | Fielder’s Choice - Play by fielder was made on a runner rather than the batter. |
| `Tot` | `PO_tot` | Total Putouts |
| `Cgt` | `PO_caught` | Putouts where the ball was caught in the air. |
| `Frc` | `PO_force` | Putouts from force plays. |
| `Tag` | `PO_tag` | Putouts where the runner was tagged. - Does not include tagging a batter or runner when a force is still possible. |
| `3U` | `PO_3u` | Putouts on unassisted putouts of the batter. |
| `Tot_2` | `A_tot` | Total Assists |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `Hm` | `A_H` | Assists where the ball was thrown to Home as a result of a ball in play. |
| `Rly` | `A_relay` | Assists where the ball was thrown as part of a relay. Only counts relays where the initial throw came from the outfield. |
| `Tot_3` | `E_tot` | Total Errors |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Fld_2` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Thr` | `E_throw` | Errors on throws. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Tot_4` | `DP_tot` | Total Double Plays - Note that the types of DPs listed after this column - will likely not total this value - as there are assorted other double plays not listed separately. |
| `363` | `DP_363` | 3-6-3 Double Plays - Any play where the first baseman started and ended the double play. |
| `361` | `DP_361` | 3-6-1 Double Plays - Any play where the first baseman started and ended by another fielder at first (P or 2B). |
| `36` | `DP_36` | 3-6 Double Plays - Any play where the first baseman started the DP with a force and ended by another fielder at second (2B or SS). |
| `GB` | `GDP` | Ground Ball Double Plays - Any ground ball double play where the fielder took part. |
| `GBs` | `GDP_start` | Ground Ball Double Plays Started - Any ground ball double play where the fielder had the first assist. |
| `LD` | `LDP` | Line Drive Double Plays - Any line drive double play where the fielder took part. |
| `LDs` | `LDP_start` | Line Drive Double Plays Started - Any line drive double play where the fielder recorded the first putout. |
| `LDf` | `LDP_finish` | Line Drive Double Plays Finished - Any line drive double play where the fielder recorded the second putout. |
| `bFld` | `inplay_bunt_fielded` | Number of bunts fielded - For many years, the fielder for non-out plays or the batted ball type is - unknown and this information will not be presented. |
| `bF2O%` | `inplay_bunt_fielded_outs_perc` | Percentage of bunts fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Advanced_Fielding_2B

192 rows, 42 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `RHB%` | `PA_with_rhb_perc` | Percentage of PAs with a Right-Handed Batter |
| `BIP%` | `PA_with_bip_perc` | Percentage of PAs that ended with ball in play |
| `GBIP%` | `PA_with_gbip_perc` | Percentage of PAs that ended with ground ball in play (not a bunt). |
| `Fld` | `inplay_fielded` | Number of balls fielded - For many years, the fielder for non-out plays is - unknown and this information will not be presented. |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `FC` | `FC` | Fielder’s Choice - Play by fielder was made on a runner rather than the batter. |
| `Tot` | `PO_tot` | Total Putouts |
| `Cgt` | `PO_caught` | Putouts where the ball was caught in the air. |
| `Frc` | `PO_force` | Putouts from force plays. |
| `Tag` | `PO_tag` | Putouts where the runner was tagged. - Does not include tagging a batter or runner when a force is still possible. |
| `Tot_2` | `A_tot` | Total Assists |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `Hm` | `A_H` | Assists where the ball was thrown to Home as a result of a ball in play. |
| `Rly` | `A_relay` | Assists where the ball was thrown as part of a relay. Only counts relays where the initial throw came from the outfield. |
| `Tot_3` | `E_tot` | Total Errors |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Fld_2` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Thr` | `E_throw` | Errors on throws. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Tot_4` | `DP_tot` | Total Double Plays - Note that the types of DPs listed after this column - will likely not total this value - as there are assorted other double plays not listed separately. |
| `643` | `DP_643` | 6-4-3 Double Plays |
| `543` | `DP_543` | 5-4-3 Double Plays |
| `463` | `DP_463` | 4-6-3 Double Plays |
| `43` | `DP_43` | 4-3 Double Plays - Second basemen tags runner or steps on second and throws to first. |
| `GB` | `GDP` | Ground Ball Double Plays - Any ground ball double play where the fielder took part. |
| `GBs` | `GDP_start` | Ground Ball Double Plays Started - Any ground ball double play where the fielder had the first assist. |
| `GBr` | `GDP_relay` | Ground Ball Double Plays Relayed - Any ground ball double play where the fielder had the first putout and second assist. |
| `LD` | `LDP` | Line Drive Double Plays - Any line drive double play where the fielder took part. |
| `LDs` | `LDP_start` | Line Drive Double Plays Started - Any line drive double play where the fielder recorded the first putout. |
| `LDf` | `LDP_finish` | Line Drive Double Plays Finished - Any line drive double play where the fielder recorded the second putout. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Advanced_Fielding_3B

192 rows, 40 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `RHB%` | `PA_with_rhb_perc` | Percentage of PAs with a Right-Handed Batter |
| `BIP%` | `PA_with_bip_perc` | Percentage of PAs that ended with ball in play |
| `GBIP%` | `PA_with_gbip_perc` | Percentage of PAs that ended with ground ball in play (not a bunt). |
| `Fld` | `inplay_fielded` | Number of balls fielded - For many years, the fielder for non-out plays is - unknown and this information will not be presented. |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `FC` | `FC` | Fielder’s Choice - Play by fielder was made on a runner rather than the batter. |
| `Tot` | `PO_tot` | Total Putouts |
| `Cgt` | `PO_caught` | Putouts where the ball was caught in the air. |
| `Frc` | `PO_force` | Putouts from force plays. |
| `Tag` | `PO_tag` | Putouts where the runner was tagged. - Does not include tagging a batter or runner when a force is still possible. |
| `Tot_2` | `A_tot` | Total Assists |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `Hm` | `A_H` | Assists where the ball was thrown to Home as a result of a ball in play. |
| `Rly` | `A_relay` | Assists where the ball was thrown as part of a relay. Only counts relays where the initial throw came from the outfield. |
| `Tot_3` | `E_tot` | Total Errors |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Fld_2` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Thr` | `E_throw` | Errors on throws. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Tot_4` | `DP_tot` | Total Double Plays - Note that the types of DPs listed after this column - will likely not total this value - as there are assorted other double plays not listed separately. |
| `543` | `DP_543` | 5-4-3 Double Plays |
| `53` | `DP_53` | 5-3 Double Plays - Third basemen tags runner or steps on third and throws to first. |
| `GB` | `GDP` | Ground Ball Double Plays - Any ground ball double play where the fielder took part. |
| `LD` | `LDP` | Line Drive Double Plays - Any line drive double play where the fielder took part. |
| `LDs` | `LDP_start` | Line Drive Double Plays Started - Any line drive double play where the fielder recorded the first putout. |
| `LDf` | `LDP_finish` | Line Drive Double Plays Finished - Any line drive double play where the fielder recorded the second putout. |
| `bFld` | `inplay_bunt_fielded` | Number of bunts fielded - For many years, the fielder for non-out plays or the batted ball type is - unknown and this information will not be presented. |
| `bF2O%` | `inplay_bunt_fielded_outs_perc` | Percentage of bunts fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Advanced_Fielding_C

192 rows, 38 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `ERA` | `earned_run_avg` | 9 * ER / IP - For recent years, leaders need 1 IP - per team game played. - Bold indicates lowest ERA using current stats - Gold means awarded ERA title at end of year. |
| `RA9` | `run_avg` | Run Average 9 * All Runs Allowed / Innings. |
| `Fld` | `inplay_fielded` | Number of balls fielded - For many years, the fielder for non-out plays is - unknown and this information will not be presented. |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `XI` | `XI` | Catcher Interference - Times a batter reached due to catcher’s interference. |
| `FC` | `FC` | Fielder’s Choice - Play by fielder was made on a runner rather than the batter. |
| `Tot` | `PO_tot` | Total Putouts |
| `Cgt` | `PO_caught` | Putouts where the ball was caught in the air. |
| `Frc` | `PO_force` | Putouts from force plays. |
| `Tag` | `PO_tag` | Putouts where the runner was tagged. - Does not include tagging a batter or runner when a force is still possible. |
| `SO` | `PO_k` | Putouts by the catcher due to a strikeout. |
| `Tot_2` | `A_tot` | Total Assists |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `3B` | `A_3B` | Assists where the ball was thrown to 3b as the result of a ball in play. |
| `K23` | `A_k23` | Assists on dropped third strikes and the ball thrown to 1b. |
| `Tot_3` | `E_tot` | Total Errors |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Fld_2` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Thr` | `E_throw` | Errors on throws. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Tot_4` | `DP_tot` | Total Double Plays - Note that the types of DPs listed after this column - will likely not total this value - as there are assorted other double plays not listed separately. |
| `263` | `DP_263` | 2-6 or 4-3 Double Plays - Any play where the catcher started the double play to second on to first. |
| `n23` | `DP_n23` | ?-2-3 Double Plays - Any double play with the bases loaded home on to first. |
| `GB` | `GDP` | Ground Ball Double Plays - Any ground ball double play where the fielder took part. |
| `bFld` | `inplay_bunt_fielded` | Number of bunts fielded - For many years, the fielder for non-out plays or the batted ball type is - unknown and this information will not be presented. |
| `bF2O%` | `inplay_bunt_fielded_outs_perc` | Percentage of bunts fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Advanced_Fielding_CF

192 rows, 48 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `Tot` | `E_tot` | Total Errors |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Fld` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Thr` | `E_throw` | Errors on throws. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Tot_2` | `A_tot` | Total Assists |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `3B` | `A_3B` | Assists where the ball was thrown to 3b as the result of a ball in play. |
| `Hm` | `A_H` | Assists where the ball was thrown to Home as a result of a ball in play. |
| `Opp` | `single_runner_on_first` | Total Plays with single and runner on first - Note: Plays where the runner on 2B stops at 3B are not included. |
| `Held` | `single_runner_on_first_held` | Total Plays with single and runner on first held to second |
| `Kill` | `single_runner_on_first_kill` | Total Plays with single and runner on first thrown out at third |
| `Opp_2` | `single_runner_on_second` | Total Plays with single and runner on second |
| `Held_2` | `single_runner_on_second_held` | Total Plays with single and runner on second held to third |
| `Kill_2` | `single_runner_on_second_kill` | Total Plays with single and runner on second thrown out at home. |
| `Opp_3` | `double_runner_on_first` | Total Plays with double and runner on first |
| `Held_3` | `double_runner_on_first_held` | Total Plays with double and runner on first held to third |
| `Kill_3` | `double_runner_on_first_kill` | Total Plays with double and runner on first thrown out at home. |
| `Opp_4` | `flyout_runner_on_third` | Total Plays with < 2 out, a flyout, and runner on third |
| `Held_4` | `flyout_runner_on_third_held` | Total Plays with < 2 out, a flyout, and runner on third held to third |
| `Kill_4` | `flyout_runner_on_third_kill` | Total Plays with < 2 out, a flyout, and runner on third thrown out at home. |
| `Opp_5` | `flyout_runner_on_second` | Total Plays with < 2 out, a flyout, and runner on second |
| `Held_5` | `flyout_runner_on_second_held` | Total Plays with < 2 out, a flyout, and runner on second held to second |
| `Kill_5` | `flyout_runner_on_second_kill` | Total Plays with < 2 out, a flyout, and runner on second thrown out at third. |
| `Opp_6` | `outfield_arm_opps` | Total Plays from five previous situations. |
| `Held_6` | `outfield_arm_held` | Total Plays from five previous situations where player did not advance. |
| `Held%` | `outfield_arm_held_perc` | Percentage of Plays from five previous situations where player did not advance. |
| `Adv` | `outfield_arm_adv` | Total Plays from five previous situations where baserunner advanced the extra base. |
| `Kill_6` | `outfield_arm_kills` | Total Plays from five previous situations where runner is thrown out attempting to advance. |
| `Kill%` | `outfield_arm_kill_perc` | Percentage of Plays from five previous situations where baserunner was thrown out trying to advance. |
| `Aother` | `A_other` | Assists other than kills from the five previous situations. |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `RHB%` | `PA_with_rhb_perc` | Percentage of PAs with a Right-Handed Batter |
| `BIP%` | `PA_with_bip_perc` | Percentage of PAs that ended with ball in play |
| `FBIP%` | `PA_with_fbip_perc` | Percentage of PAs that ended with a fly ball in play. |
| `Fld_2` | `inplay_fielded` | Number of balls fielded - For many years, the fielder for non-out plays is - unknown and this information will not be presented. |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Advanced_Fielding_C_Baseru  *(dataset `Team_Advanced_Fielding_C_Baserunning`)*

192 rows, 29 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `PB` | `PB` | Passed Balls |
| `WP` | `WP` | Wild Pitches |
| `SBO` | `SB_opp` | Stolen Base Opportunities - Plate appearances through which a runner was on first or second with the next base open. |
| `SB` | `SB` | Stolen Bases |
| `CS` | `CS` | Caught Stealing |
| `CSctch` | `CS_catcher` | Caught Stealing by Catcher Caught stealings where the catcher registered an assist. - Pickoff Caught Stealing by the pitcher are included in the CS number. |
| `CS%` | `caught_stealing_perc` | Caught Stealing Percentage - CS / (SB + CS) |
| `SB2` | `SB_2` | Steals of 2nd Base |
| `CS2` | `CS_2` | Caught Stealing 2nd Base |
| `SB3` | `SB_3` | Steals of 3rd Base |
| `CS3` | `CS_3` | Caught Stealing 3rd Base |
| `SBH` | `SB_H` | Steals of Home |
| `CSH` | `CS_H` | Caught Stealing Home |
| `PO` | `pickoffs` | Pickoffs - Runner picked off a base. May include cases they were safe on an error. - Also includes Pickoff Caught Stealing plays. |
| `PCS` | `POCS` | Pickoff Caught Stealing - Runner picked off a base and or while attempting to steal. - Is included in CS numbers and PO numbers. |
| `RBA` | `runner_bases_added` | Runner Bases Added - Total bases added on baserunning plays while this player was a catcher including WP, PB, and SB. |
| `RK` | `runner_kills` | Runner Kills - Total baserunners thrown out by the catcher including CS, pickoffs and other outs attempting to advance. |
| `SBlev` | `SB_leverage` | Stolen Base Leverage Index - The importance of the context in which the base was stolen - Above one means higher than average pressure. - Below one means lower than average pressure. |
| `CSlev` | `CS_leverage` | Caught Stealing Leverage Index - The importance of the context in which the runner was caught - Above one means higher than average pressure. - Below one means lower than average pressure. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Advanced_Fielding_LF

192 rows, 48 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `Tot` | `E_tot` | Total Errors |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Fld` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Thr` | `E_throw` | Errors on throws. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Tot_2` | `A_tot` | Total Assists |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `3B` | `A_3B` | Assists where the ball was thrown to 3b as the result of a ball in play. |
| `Hm` | `A_H` | Assists where the ball was thrown to Home as a result of a ball in play. |
| `Opp` | `single_runner_on_first` | Total Plays with single and runner on first - Note: Plays where the runner on 2B stops at 3B are not included. |
| `Held` | `single_runner_on_first_held` | Total Plays with single and runner on first held to second |
| `Kill` | `single_runner_on_first_kill` | Total Plays with single and runner on first thrown out at third |
| `Opp_2` | `single_runner_on_second` | Total Plays with single and runner on second |
| `Held_2` | `single_runner_on_second_held` | Total Plays with single and runner on second held to third |
| `Kill_2` | `single_runner_on_second_kill` | Total Plays with single and runner on second thrown out at home. |
| `Opp_3` | `double_runner_on_first` | Total Plays with double and runner on first |
| `Held_3` | `double_runner_on_first_held` | Total Plays with double and runner on first held to third |
| `Kill_3` | `double_runner_on_first_kill` | Total Plays with double and runner on first thrown out at home. |
| `Opp_4` | `flyout_runner_on_third` | Total Plays with < 2 out, a flyout, and runner on third |
| `Held_4` | `flyout_runner_on_third_held` | Total Plays with < 2 out, a flyout, and runner on third held to third |
| `Kill_4` | `flyout_runner_on_third_kill` | Total Plays with < 2 out, a flyout, and runner on third thrown out at home. |
| `Opp_5` | `flyout_runner_on_second` | Total Plays with < 2 out, a flyout, and runner on second |
| `Held_5` | `flyout_runner_on_second_held` | Total Plays with < 2 out, a flyout, and runner on second held to second |
| `Kill_5` | `flyout_runner_on_second_kill` | Total Plays with < 2 out, a flyout, and runner on second thrown out at third. |
| `Opp_6` | `outfield_arm_opps` | Total Plays from five previous situations. |
| `Held_6` | `outfield_arm_held` | Total Plays from five previous situations where player did not advance. |
| `Held%` | `outfield_arm_held_perc` | Percentage of Plays from five previous situations where player did not advance. |
| `Adv` | `outfield_arm_adv` | Total Plays from five previous situations where baserunner advanced the extra base. |
| `Kill_6` | `outfield_arm_kills` | Total Plays from five previous situations where runner is thrown out attempting to advance. |
| `Kill%` | `outfield_arm_kill_perc` | Percentage of Plays from five previous situations where baserunner was thrown out trying to advance. |
| `Aother` | `A_other` | Assists other than kills from the five previous situations. |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `RHB%` | `PA_with_rhb_perc` | Percentage of PAs with a Right-Handed Batter |
| `BIP%` | `PA_with_bip_perc` | Percentage of PAs that ended with ball in play |
| `FBIP%` | `PA_with_fbip_perc` | Percentage of PAs that ended with a fly ball in play. |
| `Fld_2` | `inplay_fielded` | Number of balls fielded - For many years, the fielder for non-out plays is - unknown and this information will not be presented. |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Advanced_Fielding_P

192 rows, 33 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `BIP%` | `PA_with_bip_perc` | Percentage of PAs that ended with ball in play |
| `GBIP%` | `PA_with_gbip_perc` | Percentage of PAs that ended with ground ball in play (not a bunt). |
| `Fld` | `inplay_fielded` | Number of balls fielded - For many years, the fielder for non-out plays is - unknown and this information will not be presented. |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `FC` | `FC` | Fielder’s Choice - Play by fielder was made on a runner rather than the batter. |
| `Tot` | `PO_tot` | Total Putouts |
| `Cgt` | `PO_caught` | Putouts where the ball was caught in the air. |
| `31` | `PO_31` | Putouts on first baseman (or other) to pitcher at first. |
| `Tot_2` | `A_tot` | Total Assists |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `Tot_3` | `E_tot` | Total Errors |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Fld_2` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Thr` | `E_throw` | Errors on throws. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Tot_4` | `DP_tot` | Total Double Plays - Note that the types of DPs listed after this column - will likely not total this value - as there are assorted other double plays not listed separately. |
| `163` | `DP_163` | 1-6 or 4-3 Double Plays - Any play where the pitcher started the double play to second on to first. |
| `GB` | `GDP` | Ground Ball Double Plays - Any ground ball double play where the fielder took part. |
| `LD` | `LDP` | Line Drive Double Plays - Any line drive double play where the fielder took part. |
| `bFld` | `inplay_bunt_fielded` | Number of bunts fielded - For many years, the fielder for non-out plays or the batted ball type is - unknown and this information will not be presented. |
| `bF2O%` | `inplay_bunt_fielded_outs_perc` | Percentage of bunts fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Advanced_Fielding_RF

192 rows, 48 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `Tot` | `E_tot` | Total Errors |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Fld` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Thr` | `E_throw` | Errors on throws. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Tot_2` | `A_tot` | Total Assists |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `3B` | `A_3B` | Assists where the ball was thrown to 3b as the result of a ball in play. |
| `Hm` | `A_H` | Assists where the ball was thrown to Home as a result of a ball in play. |
| `Opp` | `single_runner_on_first` | Total Plays with single and runner on first - Note: Plays where the runner on 2B stops at 3B are not included. |
| `Held` | `single_runner_on_first_held` | Total Plays with single and runner on first held to second |
| `Kill` | `single_runner_on_first_kill` | Total Plays with single and runner on first thrown out at third |
| `Opp_2` | `single_runner_on_second` | Total Plays with single and runner on second |
| `Held_2` | `single_runner_on_second_held` | Total Plays with single and runner on second held to third |
| `Kill_2` | `single_runner_on_second_kill` | Total Plays with single and runner on second thrown out at home. |
| `Opp_3` | `double_runner_on_first` | Total Plays with double and runner on first |
| `Held_3` | `double_runner_on_first_held` | Total Plays with double and runner on first held to third |
| `Kill_3` | `double_runner_on_first_kill` | Total Plays with double and runner on first thrown out at home. |
| `Opp_4` | `flyout_runner_on_third` | Total Plays with < 2 out, a flyout, and runner on third |
| `Held_4` | `flyout_runner_on_third_held` | Total Plays with < 2 out, a flyout, and runner on third held to third |
| `Kill_4` | `flyout_runner_on_third_kill` | Total Plays with < 2 out, a flyout, and runner on third thrown out at home. |
| `Opp_5` | `flyout_runner_on_second` | Total Plays with < 2 out, a flyout, and runner on second |
| `Held_5` | `flyout_runner_on_second_held` | Total Plays with < 2 out, a flyout, and runner on second held to second |
| `Kill_5` | `flyout_runner_on_second_kill` | Total Plays with < 2 out, a flyout, and runner on second thrown out at third. |
| `Opp_6` | `outfield_arm_opps` | Total Plays from five previous situations. |
| `Held_6` | `outfield_arm_held` | Total Plays from five previous situations where player did not advance. |
| `Held%` | `outfield_arm_held_perc` | Percentage of Plays from five previous situations where player did not advance. |
| `Adv` | `outfield_arm_adv` | Total Plays from five previous situations where baserunner advanced the extra base. |
| `Kill_6` | `outfield_arm_kills` | Total Plays from five previous situations where runner is thrown out attempting to advance. |
| `Kill%` | `outfield_arm_kill_perc` | Percentage of Plays from five previous situations where baserunner was thrown out trying to advance. |
| `Aother` | `A_other` | Assists other than kills from the five previous situations. |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `RHB%` | `PA_with_rhb_perc` | Percentage of PAs with a Right-Handed Batter |
| `BIP%` | `PA_with_bip_perc` | Percentage of PAs that ended with ball in play |
| `FBIP%` | `PA_with_fbip_perc` | Percentage of PAs that ended with a fly ball in play. |
| `Fld_2` | `inplay_fielded` | Number of balls fielded - For many years, the fielder for non-out plays is - unknown and this information will not be presented. |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Advanced_Fielding_SS

192 rows, 43 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `RHB%` | `PA_with_rhb_perc` | Percentage of PAs with a Right-Handed Batter |
| `BIP%` | `PA_with_bip_perc` | Percentage of PAs that ended with ball in play |
| `GBIP%` | `PA_with_gbip_perc` | Percentage of PAs that ended with ground ball in play (not a bunt). |
| `Fld` | `inplay_fielded` | Number of balls fielded - For many years, the fielder for non-out plays is - unknown and this information will not be presented. |
| `F2O%` | `inplay_fielded_outs_perc` | Percentage of balls fielded that resulted in outs - For many years the fielder for non-out plays is - unknown and this information will not be presented. |
| `FC` | `FC` | Fielder’s Choice - Play by fielder was made on a runner rather than the batter. |
| `Tot` | `PO_tot` | Total Putouts |
| `Cgt` | `PO_caught` | Putouts where the ball was caught in the air. |
| `Frc` | `PO_force` | Putouts from force plays. |
| `Tag` | `PO_tag` | Putouts where the runner was tagged. - Does not include tagging a batter or runner when a force is still possible. |
| `Tot_2` | `A_tot` | Total Assists |
| `1B` | `A_1B` | Assists where the ball was thrown to 1b as the result of a ball in play. |
| `2B` | `A_2B` | Assists where the ball was thrown to 2b as the result of a ball in play. |
| `Hm` | `A_H` | Assists where the ball was thrown to Home as a result of a ball in play. |
| `Rly` | `A_relay` | Assists where the ball was thrown as part of a relay. Only counts relays where the initial throw came from the outfield. |
| `Tot_3` | `E_tot` | Total Errors |
| `Cch` | `E_catch` | Errors on catches (dropped or missed throws where a player receives an assist - Cases where a player misses a throw as in a relay are likely in Fld errors). |
| `Fld_2` | `E_field` | Errors made while fielding the ball (catching a fly ball, ground balls, also includes muffed relays or missed catches on plays where no assist is given and miscellaneous errors where our account is unclear). |
| `Thr` | `E_throw` | Errors on throws. |
| `ROE` | `E_ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Tot_4` | `DP_tot` | Total Double Plays - Note that the types of DPs listed after this column - will likely not total this value - as there are assorted other double plays not listed separately. |
| `643` | `DP_643` | 6-4-3 Double Plays |
| `63` | `DP_63` | 6-3 Double Plays - Shortstop tags runner from first or steps on second and throws to first. |
| `463` | `DP_463` | 4-6-3 Double Plays |
| `163` | `DP_163` | 1-6 or 4-3 Double Plays - Any play where the pitcher started the double play to second on to first. |
| `363` | `DP_363` | 3-6-3 Double Plays - Any play where the first baseman started and ended the double play. |
| `GB` | `GDP` | Ground Ball Double Plays - Any ground ball double play where the fielder took part. |
| `GBs` | `GDP_start` | Ground Ball Double Plays Started - Any ground ball double play where the fielder had the first assist. |
| `GBr` | `GDP_relay` | Ground Ball Double Plays Relayed - Any ground ball double play where the fielder had the first putout and second assist. |
| `LD` | `LDP` | Line Drive Double Plays - Any line drive double play where the fielder took part. |
| `LDs` | `LDP_start` | Line Drive Double Plays Started - Any line drive double play where the fielder recorded the first putout. |
| `LDf` | `LDP_finish` | Line Drive Double Plays Finished - Any line drive double play where the fielder recorded the second putout. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Advanced_Pitching

192 rows, 26 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `BA` | `adv_pitch_batting_avg` | Hits/At Bats - For recent years, leaders need 3.1 PA - per team game played - Bold indicates either highest BA using current stats - or awarded title at end of year. |
| `OBP` | `adv_pitch_onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) - For recent years, leaders need 3.1 PA - per team game played |
| `SLG` | `adv_pitch_slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `OPS` | `adv_pitch_onbase_plus_slugging` | On-Base + Slugging Percentages - For recent years, leaders need 3.1 PA - per team game played |
| `BAbip` | `adv_pitch_babip` | Batting Avg. on Balls in Plays (Hits - Home Runs)/(At Bats - SO - HR + Sac Flies) - This also measures how effectively the - defense turned balls into outs. |
| `HR%` | `adv_pitch_home_run_perc` | Home Run Percentage - Percentage of all plate appearances a home run was hit. - (HR)/(all plate appearances) |
| `SO%` | `adv_pitch_strikeout_perc` | Strikeout Percentage - Percentage of all plate appearances ending with a Strikeout. - (SO)/(all plate appearances) |
| `BB%` | `adv_pitch_base_on_balls_perc` | Base on Balls Percentage - Percentage of all plate appearances ending with a Base on Balls. - (BB)/(all plate appearances) |
| `EV` | `adv_pitch_exit_velo` | Average Exit Velocity - Average speed of the ball off the bat for balls put into play, measured in miles per hour. |
| `HardH%` | `adv_pitch_hard_hit_perc` | Hard Hit Rate - Percent of balls in play with an exit velocity of 95 mph or more. |
| `LD%` | `adv_pitch_ld_perc` | Line Drive Percentage - Percentage of all balls put into play (including home runs) that are line drives. - Batted ball type and location is not complete prior to 1988. |
| `GB%` | `adv_pitch_gb_perc` | Ground Ball Percentage - Percentage of all balls put into play (including home runs) that are ground balls. - EXCLUDES Bunts - Batted ball type and location is not complete prior to 1988. |
| `FB%` | `adv_pitch_fb_perc` | Fly Ball Percentage - Percentage of all balls put into play (including home runs) that are fly balls. - EXCLUDES Popups - Batted ball type and location is not complete prior to 1988. |
| `GB/FB` | `adv_pitch_gb_fb_ratio` | Ground Ball to Fly Ball Ratio - Includes line drives as fly balls. - Batted ball type and location is not complete prior to 1988. |
| `WPA` | `adv_pitch_wpa_def` | Win Probability Added by Pitcher - Given average teams, this is the change in probability. - See Win Expectancy explainer for details. |
| `cWPA` | `adv_pitch_cwpa_def` | Championship Win Probability Added by Pitcher - Given average teams, this is the change in probability of winning the World Series, displayed in percentage points. - See Win Expectancy explainer for details. |
| `RE24` | `adv_pitch_re24_def` | Base-Out Runs Saved - Given the bases occupied/out situation, how many runs did the pitcher - save in the resulting play. Compared to average, so 0 is average, and - above 0 is better than average |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Appearances

180 rows, 27 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `G_team` | `G_team` | Games played by the team while the player was on the roster. |
| `G` | `G_all` | All games played |
| `GS` | `GS` | Games Started |
| `Batting` | `G_batting` | Games appeared in the batting order, - but may not have batted. |
| `Defense` | `G_defense` | Games in lineup at a defensive position. |
| `P` | `G_p_app` | Games in lineup or announced as a pitcher |
| `C` | `G_c` | Games in lineup as a catcher |
| `1B` | `G_1b` | Games in lineup as a first baseman |
| `2B` | `G_2b` | Games in lineup as a second baseman |
| `3B` | `G_3b` | Games in lineup as a third baseman |
| `SS` | `G_ss` | Games in lineup as a shortstop |
| `LF` | `G_lf_app` | Games in lineup as a left fielder |
| `CF` | `G_cf_app` | Games in lineup as a center fielder |
| `RF` | `G_rf_app` | Games in lineup as a right fielder |
| `OF` | `G_of_app` | Games in lineup as an outfielder |
| `DH` | `G_dh` | Games in lineup as a designated hitter |
| `PH` | `G_ph` | Games in lineup as a pinch hitter - May have played another position as well. |
| `PR` | `G_pr` | Games in lineup as a pinch runner - May have played another position as well. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Attendance

186 rows, 15 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Current_Home_Games` | `parsed` | Home dates played in this season. |
| `Current_Attendance` | `parsed` | Total home attendance this season. |
| `Current_Attendance_Per_Game` | `parsed` | Average home attendance this season. |
| `Prior_Home_Games` | `parsed` | Home dates played the previous season. |
| `Prior_Attendance` | `parsed` | Total home attendance the previous season. |
| `Prior_Attendance_Per_Game` | `parsed` | Average home attendance the previous season. |
| `YoY_Attendance_Diff` | `parsed` | Change in total attendance versus the previous season. |
| `YoY_Attendance_Diff_Per_Game` | `parsed` | Change in attendance per game versus the previous season. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Baserunning_Batting

192 rows, 41 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `R/G` | `runs_per_game` | Runs Scored Per Game |
| `ROE` | `ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `XI` | `XI` | Catcher Interference - Times a batter reached due to catcher’s interference. |
| `RS%` | `runs_scored_perc` | Run Scoring Percentage - Percentage of times a baserunner eventually scores a run. - (R - HR) / (H + HBP + BB - HR + G_pr) |
| `SBO` | `SB_opp` | Stolen Base Opportunities - Plate appearances through which a runner was on first or second with the next base open. |
| `SB` | `SB` | Stolen Bases |
| `CS` | `CS` | Caught Stealing |
| `SB%` | `stolen_base_perc` | Stolen Base Percentage - SB / (SB + CS) |
| `SB2` | `SB_2` | Steals of 2nd Base |
| `CS2` | `CS_2` | Caught Stealing 2nd Base |
| `SB3` | `SB_3` | Steals of 3rd Base |
| `CS3` | `CS_3` | Caught Stealing 3rd Base |
| `SBH` | `SB_H` | Steals of Home |
| `CSH` | `CS_H` | Caught Stealing Home |
| `PO` | `pickoffs` | Pickoffs - Runner picked off a base. May include cases they were safe on an error. - Also includes Pickoff Caught Stealing plays. |
| `PCS` | `POCS` | Pickoff Caught Stealing - Runner picked off a base and or while attempting to steal. - Is included in CS numbers and PO numbers. |
| `OOB` | `outs_on_base` | Outs on Base - Runner is put out while making a baserunning play. - Example plays: out advancing on a fly ball, out attempting to reach another base on a hit, - doubled off on a line drive, or out attempting to advance on a wild pitch or passed ball. - Does not include pickoffs, caught stealing, or force plays. |
| `OOB1` | `outs_on_base_1` | Outs on Base at 1st - Runner is put out while making a baserunning play. - Example plays: out advancing on a fly ball, out attempting to reach another base on a hit, - doubled off on a line drive, or out attempting to advance on a wild pitch or passed ball. - Does not include pickoffs, caught stealing, or force plays. |
| `OOB2` | `outs_on_base_2` | Outs on Base at 2nd - Runner is put out while making a baserunning play. - Example plays: out advancing on a fly ball, out attempting to reach another base on a hit, - doubled off on a line drive, or out attempting to advance on a wild pitch or passed ball. - Does not include pickoffs, caught stealing, or force plays. |
| `OOB3` | `outs_on_base_3` | Outs on Base at 3rd - Runner is put out while making a baserunning play. - Example plays: out advancing on a fly ball, out attempting to reach another base on a hit, - doubled off on a line drive, or out attempting to advance on a wild pitch or passed ball. - Does not include pickoffs, caught stealing, or force plays. |
| `OOBHm` | `outs_on_base_h` | Outs on Base at Home - Runner is put out while making a baserunning play. - Example plays: out advancing on a fly ball, out attempting to reach another base on a hit, - doubled off on a line drive, or out attempting to advance on a wild pitch or passed ball. - Does not include pickoffs, caught stealing, or force plays. |
| `BT` | `bases_taken` | Bases Taken - Bases advanced on fly balls, passed balls, wild pitches, balks, defensive indifference. |
| `XBT%` | `extra_bases_taken_perc` | Extra Bases Taken Percentage - Percentage of times the runner advanced more than one base on a single or more than two bases on a double, when possible. - Does not take into account the location or type of the ball in play. |
| `1stS` | `on_first_single` | On First, when a single is hit - Times a runner is on first and the batter hits a single. |
| `1stS2` | `on_first_single_12` | On First, when a single is hit and runner reaches second |
| `1stS3` | `on_first_single_13` | On First, when a single is hit and runner reaches third or scores |
| `1stD` | `on_first_double` | On First, when a double is hit - Times a runner is on first and the batter hits a double. |
| `1stD3` | `on_first_double_13` | On First, when a double is hit and runner reaches third |
| `1stDH` | `on_first_double_1H` | On First, when a double is hit and runner scores |
| `2ndS` | `on_second_single` | On Second, when a single is hit - Times a runner is on second and the batter hits a single. |
| `2ndS3` | `on_second_single_23` | On Second, when a single is hit and runner reaches third |
| `2ndSH` | `on_second_single_2H` | On Second, when a single is hit and runner scores |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Basesituation_Pitching

192 rows, 42 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `RA/G` | `runs_allowed_per_game` | Runs Allowed Per Game |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `H` | `H_all` | All Hits |
| `Inf` | `H_inf` | Infield Hits - Batted ball type and location is not complete prior to 1988. |
| `Bnt` | `H_bunt` | Bunt Hits - Batted ball type and location is not complete prior to 1988. |
| `All` | `HR_all` | Home Run Total |
| `GS` | `HR_gs` | Grand Slam Home Runs |
| `GSo` | `HR_gs_opp` | Grand Slam Opportunities - Plate Appearances with the Bases Loaded |
| `vRH` | `HR_vrh` | Home Runs off Right-Handers |
| `vLH` | `HR_vlh` | Home Runs off Left-Handers |
| `Hm` | `HR_hm` | Home Runs at Home |
| `Rd` | `HR_rd` | Home Runs on the Road |
| `<2,3B` | `lt_2_out_on_third_opp` | PAs with less than two out, runner on third |
| `Scr` | `lt_2_out_on_third_scored` | PAs with less than two out, runner on third and runner scored |
| `SO` | `lt_2_out_on_third_so` | PAs with less than two out, runner on third and pitcher struck out batter |
| `%` | `lt_2_out_on_third_perc` | PAs with less than two out, runner on third and runner scored |
| `ROE` | `ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `WP` | `WP` | Wild Pitches |
| `PB` | `PB` | Passed Balls |
| `SBO` | `SB_opp` | Stolen Base Opportunities - Plate appearances through which a runner was on first or second with the next base open. |
| `SB` | `SB` | Stolen Bases |
| `CS` | `CS` | Caught Stealing |
| `SB%` | `stolen_base_perc` | Stolen Base Percentage - SB / (SB + CS) |
| `SB2` | `SB_2` | Steals of 2nd Base |
| `CS2` | `CS_2` | Caught Stealing 2nd Base |
| `SB3` | `SB_3` | Steals of 3rd Base |
| `CS3` | `CS_3` | Caught Stealing 3rd Base |
| `SBH` | `SB_H` | Steals of Home |
| `CSH` | `CS_H` | Caught Stealing Home |
| `PO` | `pickoffs` | Pickoffs - Runner picked off a base. May include cases they were safe on an error. - Also includes Pickoff Caught Stealing plays. |
| `PCS` | `POCS` | Pickoff Caught Stealing - Runner picked off a base and or while attempting to steal. - Is included in CS numbers and PO numbers. |
| `BT` | `bases_taken` | Bases Taken - Bases advanced on fly balls, passed balls, wild pitches, balks, defensive indifference. |
| `PAu` | `PA_unknown` | Plate Appearances for which data is not known - Note that for many stats (like pitcher SLG, 2B, 3B allowed, WPA, HR direction, etc.) - this will mean that the totals given are incomplete. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Batting_Pitching

192 rows, 35 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `RA/G` | `runs_allowed_per_game` | Runs Allowed Per Game |
| `PAu` | `PA_unknown` | Plate Appearances for which data is not known - Note that for many stats (like pitcher SLG, 2B, 3B allowed, WPA, HR direction, etc.) - this will mean that the totals given are incomplete. |
| `G` | `G` | Games Played or Pitched |
| `PA` | `PA` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `AB` | `AB` | At Bats |
| `R` | `R` | Runs Scored/Allowed |
| `H` | `H` | Hits/Hits Allowed |
| `2B` | `2B` | Doubles Hit/Allowed |
| `3B` | `3B` | Triples Hit/Allowed |
| `HR` | `HR` | Home Runs Hit/Allowed |
| `SB` | `SB` | Stolen Bases |
| `CS` | `CS` | Caught Stealing |
| `BB` | `BB` | Bases on Balls/Walks |
| `SO` | `SO` | Strikeouts |
| `BA` | `batting_avg` | Hits/At Bats - For recent years, leaders need 3.1 PA - per team game played - Bold indicates either highest BA using current stats - or awarded title at end of year. |
| `OBP` | `onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) - For recent years, leaders need 3.1 PA - per team game played |
| `SLG` | `slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `OPS` | `onbase_plus_slugging` | On-Base + Slugging Percentages - For recent years, leaders need 3.1 PA - per team game played |
| `BAbip` | `batting_avg_bip` | Batting Avg. on Balls in Plays (Hits - Home Runs)/(At Bats - SO - HR + Sac Flies) - This also measures how effectively the - defense turned balls into outs. |
| `TB` | `TB` | Total Bases - Singles + 2 x Doubles + 3 x Triples + 4 x Home Runs. |
| `GDP` | `GIDP` | Double Plays Grounded Into - Only includes standard 6-4-3, 4-3, etc. double plays. - First tracked in 1933. - For gamelogs only in seasons we have play-by-play, we include triple plays as well. - All official seasonal totals do not include GITP's. |
| `HBP` | `HBP` | Times Hit by a Pitch. |
| `SH` | `SH` | Sacrifice Hits (Sacrifice Bunts) |
| `SF` | `SF` | Sacrifice Flies - First tracked in 1954. |
| `IBB` | `IBB` | Intentional Bases on Balls - First tracked in 1955. |
| `ROE` | `ROE` | Reached On Error - Times a batter reached due to an error - DOES NOT include a fielder’s choice where no out was recorded. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Fielding_By_Position

1,920 rows, 48 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Position` | `identifier/derived` | Fielding position this row covers. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `#Fld` | `fielders_used` | Number of Players used as Fielders |
| `RA/G` | `runs_allowed_per_game` | Runs Allowed Per Game |
| `G` | `G` | Games Played or Pitched |
| `GS` | `GS` | Games Started |
| `CG` | `CG` | Complete Game |
| `Inn` | `Inn_def` | Innings Played in Field |
| `Ch` | `chances` | Defensive Chances - Putouts + Assists + Errors |
| `PO` | `PO` | Putouts |
| `A` | `A` | Assists |
| `E` | `E_def` | Errors Committed |
| `DP` | `DP_def` | Double Plays Turned |
| `Fld%` | `fielding_perc` | Fielding Percentage - (Putouts + Assists) / (Putouts + Assists + Errors) |
| `Rtot` | `tz_runs_total` | Total Zone Total Fielding Runs Above Avg - The number of runs above or below average the player was worth based on the number of plays made. - This number combines the R tz , R dp , R of , R catch numbers into a total defensive contribution. - See the glossary section for a more complete explanation. - Provided by BaseballProjection.com |
| `Rtot/yr` | `tz_runs_total_per_season` | Total Zone Total Fielding Runs Above Avg per 1,200 Inn - The number of runs above or below average the fielder was worth per 1,200 Innings (approx 135 games). - This number combines the R tz , R dp , R of , R catch numbers into a total defensive contribution. - See the glossary section for a more complete explanation. - Provided by BaseballProjection.com |
| `Rtz` | `tz_runs_field` | Total Zone Fielding Runs Above Avg - The number of runs above or below average the player was worth based on fielding plays made. - This number does not include OF kills, or double plays turned. - See the glossary section for a more complete explanation. - Provided by BaseballProjection.com |
| `Rdp` | `tz_runs_infield` | Total Zone Infield Double Play Runs Above Avg - The number of runs above or below average the player was worth based on double plays turned and opportunities given. - See the glossary section for a more complete explanation. - Provided by BaseballProjection.com |
| `Rdrs` | `bis_runs_total_team` | BIS Defensive Runs Saved Above Avg - The number of runs above or below average the team was worth based on their overall defense. - This number combines the individual players' defensive runs saved as well as team-level runs saved from shifting and positioning into a total team defensive contribution. - Provided by Baseball Info Solutions |
| `Rdrs/yr` | `bis_runs_total_per_season_team` | BIS Defensive Runs Saved Above Avg per 1,200 Inn - The number of runs above or below average the team's fielders were worth per 1,200 Innings (approx 135 games). - This number combines the R pm , R dp , and R good numbers into a total defensive contribution. - For pitchers, this is set to 200 Innings. - This does not include any team-level runs saved from positioning or shifting. - Provided by Baseball Info Solutions |
| `Rpm` | `bis_runs_field` | BIS Plus/Minus Fielding Runs Above Avg - The number of runs above or below average the player was worth based on fielding plays made. - This number combines the R range , R air , and R throw numbers. - This number does not include OF kills, or double plays turned. - Provided by Baseball Info Solutions |
| `Rgood` | `bis_runs_good_plays` | BIS Good Plays/Misplays Runs Above Avg - The number of runs above or below average the player was worth based on plays where they made an exceptional contribution or obviously misplayed the situation. - Provided by Baseball Info Solutions |
| `Rair` | `bis_runs_air` | BIS Infield Air Ball Runs Above Avg - The number of runs above or below average the player was worth based on infield air balls. - Provided by Baseball Info Solutions |
| `Rrange` | `bis_runs_range` | BIS Infield Range Runs Above Avg - The number of runs above or below average the player was worth based on his performance between when the ball was hit and when the fielder gets to the ball (or fails to). - Provided by Baseball Info Solutions |
| `Rthrow` | `bis_runs_throwing` | BIS Infield Throwing Runs Above Avg - The number of runs above or below average the player was worth based on how he completes the play given where he fielded the ball, how hard it was hit, and the speed of the runner. - Provided by Baseball Info Solutions |
| `Rbnt` | `bis_runs_bunts` | BIS Bunts Fielded Runs Above Avg - The number of runs above or below average the player was worth solely on bunts. - Provided by Baseball Info Solutions |
| `Rdp_2` | `bis_runs_infield` | BIS Infield Double Play Runs Above Avg - The number of runs above or below average the player was worth based on double plays turned and opportunities given. - Provided by Baseball Info Solutions |
| `Rctch` | `tz_runs_catcher` | Total Zone Catcher Runs Above Avg - The number of runs above or below average the catcher was worth based on baserunner kills and baserunner advances. - See the glossary section for a more complete explanation. - Provided by BaseballProjection.com |
| `RszC` | `bis_runs_catcher_sz` | BIS Catcher Strike Zone Runs Above Avg - The number of runs above or below average the catcher was worth based on catcher framing. - Provided by Baseball Info Solutions |
| `RsbC` | `bis_runs_catcher_sb` | BIS Catcher Runs Above Avg - The number of runs above or below average the catcher was worth based on baserunner kills and baserunner advances. - Provided by Baseball Info Solutions |
| `RerC` | `bis_runs_catcher_er` | BIS Catcher Pitch Calling Runs Above Avg - The number of runs above or below average the catcher was for the pitcher ERA. - Provided by Baseball Info Solutions |
| `PB` | `PB` | Passed Balls |
| `WP` | `WP` | Wild Pitches |
| `SB` | `SB` | Stolen Bases |
| `CS` | `CS` | Caught Stealing |
| `CS%` | `caught_stealing_perc` | Caught Stealing Percentage - CS / (SB + CS) |
| `Rof` | `tz_runs_outfield` | Total Zone Outfield Arm Runs Above Avg - The number of runs above or below average the player was worth based on baserunner kills and baserunner advances. - See the glossary section for a more complete explanation. - Provided by BaseballProjection.com |
| `Rof_2` | `bis_runs_outfield` | BIS Outfield Arm Runs Above Avg - The number of runs above or below average the player was worth based on baserunner kills and baserunner advance. - Provided by Baseball Info Solutions |
| `RsbP` | `bis_runs_pitcher_sb` | BIS Pitcher SB Runs Above Avg - The number of runs above or below average the pitcher was worth based on baserunner kills and baserunner advances. - Provided by Baseball Info Solutions |
| `PO_2` | `pickoffs` | Pickoffs - Runner picked off a base. May include cases they were safe on an error. - Also includes Pickoff Caught Stealing plays. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Miscellaneous

180 rows, 26 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `Stadium` | `stadium` | Stadium - Team’s home parks for that season. |
| `Attendance` | `attendance` | Attendance - Typically, tickets sold in home games. |
| `Attend/G` | `attendance_per_game` | Attend/G - Typically, tickets sold per home game. - Also, all single-admission doubleheaders are counted only once in the attendance total and a zero is used for the other game of the doubleheader. Both games are counted in the denominator. |
| `BatAge` | `age_bat` | Batters’ average age - Weighted by AB + Games Played |
| `PAge` | `age_pit` | Pitchers’ average age - Weighted by 3*GS + G + SV |
| `BPF` | `bpf` | Batting Park Factor - 100 - Neutral - < 100 - Favors Pitchers - > 100 - Favors Batters. |
| `PPF` | `ppf` | Pitching Park Factor - 100 - Neutral - < 100 - Favors Pitchers - > 100 - Favors Batters. |
| `#HOF` | `team_hofers` | Hall of Famers - Number of Players currently in the Hall of Fame |
| `#A-S` | `team_allstars` | All-Stars - Number of Players who were named to the All-Star game in this season |
| `#a-tA-S` | `team_allstars_alltime` | All-time All-Stars - Number of Players on team who were named to the All-Star game at some point in their careers. Includes AL vs NL and East vs West All-Star games. |
| `Est. Payroll` | `payroll` | These values may not include every bonus the team paid in a season, - or players called up or acquired mid-season. |
| `Time` | `time_of_game` | Time of Game |
| `Chall` | `challenges` | Manager Challenges using instant replay. |
| `Succ` | `challenges_success` | Successful Manager Challenges using instant replay. |
| `Succ%` | `challenges_success_perc` | Percentage of Manager Challenges using instant replay Successful. |
| `Managers` | `managers` | Manager(s) used during the season. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Pitches_Batting

192 rows, 39 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `R/G` | `runs_per_game` | Runs Scored Per Game |
| `PA` | `PA_pitch` | Plate Appearances - The number of plate appearances for which we have pitch-by-pitch data. - Note that inning-ending baserunning outs are counted as a PA, - So these may be larger than batting PAs. |
| `Pit` | `pitches` | Number of pitches in the PA. |
| `Pit/PA` | `pitches_per_pa` | Pitches per Plate Appearance |
| `Str` | `strikes_total` | Strikes - Includes both pitches in the zone and those swung at out of the zone. |
| `Str%` | `strike_perc` | Strike Percentage - Strikes / Total Pitches (intentional balls excluded). |
| `L/Str` | `strike_looking_perc` | Strikes Looking / Strikes - All strikes looking divided by all strikes. |
| `S/Str` | `strike_swinging_perc` | Swinging Strike Percentage - Strikes Swinging (w/o contact) / Total Strikes. |
| `F/Str` | `strike_foul_perc` | Foul Ball Strikes Percentage - Pitches Fouled Off / Total Strikes Seen. |
| `I/Str` | `strike_inplay_perc` | Ball In Play Percentage - Balls put into Play (including home runs) / Total Strikes. |
| `AS/Str` | `all_strikes_swinging_perc` | Swung at Strikes Percentage - (Inplay + Foul + Swinging Strikes) / Total Strikes. |
| `I/Bll` | `ball_intent_perc` | Intentional Ball Percentage - Intentional Balls / All Balls. |
| `AS/Pit` | `pitches_swinging_perc` | Percentage of Pitches Swung At - (Inplay + Foul + Swinging Strikes) / (Total Pitches - intentional balls). |
| `Con` | `contact_perc` | Contact Percentage - (Foul + Inplay Strikes) / (Foul + Inplay + Swinging Strikes). |
| `1stS` | `first_pitch_swings_perc` | First Pitch Swinging Percentage - First Pitch Swinging / PA. |
| `30%` | `30_pitches_perc` | 3-0 Count Seen Percentage - 3-0 Counts / PA. |
| `30c` | `30_pitches` | 3-0 counts seen |
| `30s` | `30_swings` | Swinging on a 3-0 Count |
| `20%` | `20_pitches_perc` | 2-0 Count Seen Percentage - 2-0 Counts / PA. |
| `20c` | `20_pitches` | 2-0 counts seen |
| `20s` | `20_swings` | Swinging on a 2-0 Count |
| `31%` | `31_pitches_perc` | 3-1 Count Seen Percentage - 3-1 Counts / PA. |
| `31c` | `31_pitches` | 3-1 counts seen |
| `31s` | `31_swings` | Swinging on a 3-1 Count |
| `L/SO` | `SO_looking` | Strikeouts Looking |
| `S/SO` | `SO_swinging` | Strikeouts Swinging |
| `L/SO%` | `SO_looking_perc` | Strikeout Looking Percentage - Strikeouts Looking / All Strikeouts. |
| `PAu` | `PA_unknown` | Plate Appearances for which data is not known - Note that for many stats (like pitcher SLG, 2B, 3B allowed, WPA, HR direction, etc.) - this will mean that the totals given are incomplete. |
| `Pitu` | `pitches_unknown` | Pitches for which ball-strike results are not known |
| `Stru` | `strikes_unknown` | Strikes for which detailed results are not known |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Pitches_Pitching

192 rows, 39 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `RA/G` | `runs_allowed_per_game` | Runs Allowed Per Game |
| `PA` | `PA_pitch` | Plate Appearances - The number of plate appearances for which we have pitch-by-pitch data. - Note that inning-ending baserunning outs are counted as a PA, - So these may be larger than batting PAs. |
| `Pit` | `pitches` | Number of pitches in the PA. |
| `Pit/PA` | `pitches_per_pa` | Pitches per Plate Appearance |
| `Str` | `strikes_total` | Strikes - Includes both pitches in the zone and those swung at out of the zone. |
| `Str%` | `strike_perc` | Strike Percentage - Strikes / Total Pitches (intentional balls excluded). |
| `L/Str` | `strike_looking_perc` | Strikes Looking / Strikes - All strikes looking divided by all strikes. |
| `S/Str` | `strike_swinging_perc` | Swinging Strike Percentage - Strikes Swinging (w/o contact) / Total Strikes. |
| `F/Str` | `strike_foul_perc` | Foul Ball Strikes Percentage - Pitches Fouled Off / Total Strikes Seen. |
| `I/Str` | `strike_inplay_perc` | Ball In Play Percentage - Balls put into Play (including home runs) / Total Strikes. |
| `AS/Str` | `all_strikes_swinging_perc` | Swung at Strikes Percentage - (Inplay + Foul + Swinging Strikes) / Total Strikes. |
| `I/Bll` | `ball_intent_perc` | Intentional Ball Percentage - Intentional Balls / All Balls. |
| `AS/Pit` | `pitches_swinging_perc` | Percentage of Pitches Swung At - (Inplay + Foul + Swinging Strikes) / (Total Pitches - intentional balls). |
| `Con` | `contact_perc` | Contact Percentage - (Foul + Inplay Strikes) / (Foul + Inplay + Swinging Strikes). |
| `1st%` | `first_pitch_strike_perc` | First Pitch Strike Percentage - Percentage of plate appearances that - began 0-1 or with a ball in play. |
| `30%` | `30_pitches_perc` | 3-0 Count Seen Percentage - 3-0 Counts / PA. |
| `30c` | `30_pitches` | 3-0 counts seen |
| `30s` | `30_strikes` | Strikes on a 3-0 Count |
| `02%` | `02_pitches_perc` | 0-2 Count Seen Percentage - 0-2 Counts / PA. |
| `02c` | `02_pitches` | 0-2 counts seen |
| `02s` | `02_strikes` | Strikes thrown on an 0-2 Count |
| `02h` | `02_hits` | Hits given up on an 0-2 Count |
| `L/SO` | `SO_looking` | Strikeouts Looking |
| `S/SO` | `SO_swinging` | Strikeouts Swinging |
| `L/SO%` | `SO_looking_perc` | Strikeout Looking Percentage - Strikeouts Looking / All Strikeouts. |
| `3pK` | `SO_3_pitches` | 3-Pitch Strikeouts |
| `4pW` | `BB_4_pitches` | 4-pitch Walks |
| `PAu` | `PA_unknown` | Plate Appearances for which data is not known - Note that for many stats (like pitcher SLG, 2B, 3B allowed, WPA, HR direction, etc.) - this will mean that the totals given are incomplete. |
| `Pitu` | `pitches_unknown` | Pitches for which ball-strike results are not known |
| `Stru` | `strikes_unknown` | Strikes for which detailed results are not known |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Pitching_Staffs

180 rows, 20 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Tm` | `team_name` | Team as listed in the source table. |
| `#1` | `sp_1` | Primary starting pitcher #1 in the rotation. |
| `#2` | `sp_2` | Primary starting pitcher #2 in the rotation. |
| `#3` | `sp_3` | Primary starting pitcher #3 in the rotation. |
| `#4` | `sp_4` | Primary starting pitcher #4 in the rotation. |
| `#5` | `sp_5` | Primary starting pitcher #5 in the rotation. |
| `Closer` | `cl` | Primary closer. |
| `#2_2` | `bu_2` | Second-most-used bullpen arm. |
| `#3_2` | `bu_3` | Third-most-used bullpen arm. |
| `#4_2` | `bu_4` | Fourth-most-used bullpen arm. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Ratio_Batting

192 rows, 25 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `R/G` | `runs_per_game` | Runs Scored Per Game |
| `HR%` | `home_run_perc` | Home Run Percentage - Percentage of all plate appearances a home run was hit. - (HR)/(all plate appearances) |
| `SO%` | `strikeout_perc` | Strikeout Percentage - Percentage of all plate appearances ending with a Strikeout. - (SO)/(all plate appearances) |
| `BB%` | `base_on_balls_perc` | Base on Balls Percentage - Percentage of all plate appearances ending with a Base on Balls. - (BB)/(all plate appearances) |
| `XBH%` | `extra_base_hit_perc` | Extra Base Hit Percentage - Percentage of all plate appearances ending with an Extra Base Hit. - (2B + 3B + HR)/(all plate appearances) |
| `X/H%` | `extra_base_hit_per_hit_perc` | Percentage of all hits for extra bases - Percentage of all hits resulting in extra bases. - (2B + 3B + HR) / H ) |
| `SO/W` | `strikeouts_per_base_on_balls` | SO/W or SO/BB - For recent years, pitching leaders need 1 IP - per team game played. - No batting leaders computed. |
| `AB/SO` | `at_bats_per_strikeout` | At Bats Per Strikeout - For career marks this only includes AB’s for seasons where SO’s were tracked. |
| `AB/HR` | `at_bats_per_home_run` | At Bats Per Home Run |
| `AB/RBI` | `at_bats_per_rbi` | At Bats Per Run Batted In |
| `GB/FB` | `gb_fb_ratio` | Ground Ball to Fly Ball Ratio - Includes line drives as fly balls. - Batted ball type and location is not complete prior to 1988. |
| `GO/AO` | `go_ao_ratio` | Ground Outs to Air Outs - Double plays count as two. - Batted ball type and location is not complete prior to 1988. |
| `IP%` | `inplay_perc` | Balls In-Play Percentage - Percentage of all plate appearances with ball put into play. - (AB-SO-HR+SF)/(all plate appearances) |
| `LD%` | `line_drive_perc` | Line Drive Percentage - Percentage of all balls put into play (including home runs) that are line drives. - Batted ball type and location is not complete prior to 1988. |
| `HR/FB` | `home_run_fb_perc` | Percentage of Fly Balls that were Home Runs - Includes all fly balls to the outfield including line drives. - Batted ball type and location is not complete prior to 1988. |
| `IF/FB` | `infield_fb_perc` | Percentage of Fly Balls that were on the infield - Includes Line Drives. - Batted ball type and location is not complete prior to 1988. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Ratio_Pitching

192 rows, 27 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `RA/G` | `runs_allowed_per_game` | Runs Allowed Per Game |
| `Ptn%` | `PA_with_platoon_adv_perc` | Percentage of PA with the platoon advantage - Switch hitters should be 100% for most cases. - For pitchers, facing a batter of the same hand. - For batters, facing a pitcher of the opposite hand. |
| `HR%` | `home_run_perc` | Home Run Percentage - Percentage of all plate appearances a home run was hit. - (HR)/(all plate appearances) |
| `SO%` | `strikeout_perc` | Strikeout Percentage - Percentage of all plate appearances ending with a Strikeout. - (SO)/(all plate appearances) |
| `BB%` | `base_on_balls_perc` | Base on Balls Percentage - Percentage of all plate appearances ending with a Base on Balls. - (BB)/(all plate appearances) |
| `SO-BB%` | `strikeout_minus_base_on_balls_perc` | Strikeout - Base on Balls Percentage - The differential of all batters faced between Strikeouts and Base on Balls - (SO-BB)/(all plate appearances) |
| `XBH%` | `extra_base_hit_perc` | Extra Base Hit Percentage - Percentage of all plate appearances ending with an Extra Base Hit. - (2B + 3B + HR)/(all plate appearances) |
| `X/H%` | `extra_base_hit_per_hit_perc` | Percentage of all hits for extra bases - Percentage of all hits resulting in extra bases. - (2B + 3B + HR) / H ) |
| `GB/FB` | `gb_fb_ratio` | Ground Ball to Fly Ball Ratio - Includes line drives as fly balls. - Batted ball type and location is not complete prior to 1988. |
| `GO/AO` | `go_ao_ratio` | Ground Outs to Air Outs - Double plays count as two. - Batted ball type and location is not complete prior to 1988. |
| `IP%` | `inplay_perc` | Balls In-Play Percentage - Percentage of all plate appearances with ball put into play. - (AB-SO-HR+SF)/(all plate appearances) |
| `LD%` | `line_drive_perc` | Line Drive Percentage - Percentage of all balls put into play (including home runs) that are line drives. - Batted ball type and location is not complete prior to 1988. |
| `HR/FB` | `home_run_fb_perc` | Percentage of Fly Balls that were Home Runs - Includes all fly balls to the outfield including line drives. - Batted ball type and location is not complete prior to 1988. |
| `IF/FB` | `infield_fb_perc` | Percentage of Fly Balls that were on the infield - Includes Line Drives. - Batted ball type and location is not complete prior to 1988. |
| `Opp` | `GIDP_opp` | Opportunity for a Grounded Into Double Play - Runner on first with less than two outs. |
| `DP` | `GIDP_suc` | Grounded Into Double Play - Two or more outs via force outs on a ground ball. |
| `%` | `GIDP_perc` | Grounded Into Double Play Rate - Two or more outs via force outs on a ground ball. |
| `PAu` | `PA_unknown` | Plate Appearances for which data is not known - Note that for many stats (like pitcher SLG, 2B, 3B allowed, WPA, HR direction, etc.) - this will mean that the totals given are incomplete. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Reliever_Pitching

192 rows, 39 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `G` | `G` | Games Played or Pitched |
| `GR` | `GR` | Games in Relief |
| `GF` | `GF` | Games Finished - Credited to the last pitcher to appear for a team in a game. - Complete Games are not counted as Games Finished. |
| `Wgr` | `W_GR` | Wins in relief |
| `Lgr` | `L_GR` | Losses in relief |
| `SVOpp` | `SvOpp` | Save Opportunities - This is Saves + Blown Saves. - 1973 and before, there are 90+ games where a pitcher earned the save - under the current rule, but was not credited with a save. |
| `SV` | `SV` | Saves |
| `BSv` | `BSv` | Blown Saves - Pitcher entered the game in a save situation and lost the lead. |
| `SV%` | `SvOpp_perc` | Save Percentage - Saves/Save Opportunities - Save Opportunities is Saves + Blown Saves. - 1973 and before, there are 90+ games where a pitcher earned the save - under the current rule, but was not credited with a save. |
| `SVSit` | `SvSit` | Save Situations - Pitcher entered the game after the fifth inning in a save situation. - Or pitcher entered earlier in the game and did not get the win. - When the starter did not go five innings, it is - possible to enter in a save situation and get the win. - Save Situation Defn. (any of three): - 1. team has a lead of no more - than three runs and and at least three outs remaining. - 2. The tying run is either on base, at bat or on deck. - 3. At three innings remain in the game. - For our purposes, a save situation is only one - of the first two. |
| `Hold` | `Hold` | Holds - Pitcher entered the game in a save situation and did not get - the win (due to < 5 IP by starter) or save. - The pitcher then retires at least one batter and leaves the game - without having relinquished the lead at any point. - A pitcher can get a hold and a loss, but not a hold and a win - or a hold and a save. |
| `IR` | `inherited_runners` | Inherited Runners - Number of runners on base when pitcher entered the game. |
| `IS` | `inherited_score` | Inherited Score - Number or percentage of runners on base when pitcher entered the game who subsequently scored. - These runners show up in the previous pitcher’s ERA. |
| `IS%` | `inherited_score_perc` | Inherited Score Percentage - Percentage of runners on base when pitcher entered the game who subsequently scored. - These runners show up in the previous pitcher’s ERA. |
| `1stIP` | `inning_first_mode` | Most Common Inning to Enter Game - Ties go to the later inning. |
| `aLI` | `leverage_index_avg` | Average Leverage Index - The average pressure the pitcher or batter saw in this game or season. - 1.0 is average pressure, below 1.0 is low pressure and above 1.0 is high pressure. |
| `LevHi` | `enter_leverage_high` | Games entered with High Leverage - The first PA of the pitcher’s appearance - has a leverage of 1.5 or higher. |
| `LevMd` | `enter_leverage_med` | Games entered with Medium Leverage - The first PA of the pitcher’s appearance - has a leverage between 0.7 and 1.5. |
| `LevLo` | `enter_leverage_low` | Games entered with Low Leverage - The first PA of the pitcher’s appearance - has a leverage of 0.7 or lower. |
| `Ahd` | `enter_ahead` | Games Entered with Lead - Pitcher entered the game with his team in the lead. |
| `Tie` | `enter_tied` | Games Entered Tied - Pitcher entered the game tied. |
| `Bhd` | `enter_behind` | Games Entered Behind - Pitcher entered the game with his team trailing. |
| `Runr` | `enter_runners_on` | Games Entered With Runners On - Pitcher entered the game with runners on base. |
| `Empt` | `enter_empty` | Games Entered With Bases Empty - Pitcher entered the game with no runners on base. |
| `>3o` | `IPouts_gt3` | Games the pitcher completed more than three outs |
| `<3o` | `IPouts_lt3` | Games the pitcher completed fewer than three outs |
| `IPmult` | `IP_multi` | Games the pitcher pitched in more than one inning |
| `0DR` | `DR_0` | Zero Days Rest - Times the pitcher pitched on consecutive days, or both ends of a doubleheader. |
| `Out/GR` | `outs_per_GR` | Average Outs Recorded per Game in Relief |
| `Pit/GR` | `pitches_per_GR` | Pitches per Game in Relief |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Sabermetric_Batting

192 rows, 31 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `R/G` | `runs_per_game` | Runs Scored Per Game |
| `Outs` | `outs_made` | Outs Made - (At Bats - Hits) + Double Plays Grounded Into - + Sac. Flies + Sac. Hits + Caught Stealing. |
| `RC` | `RC` | Runs Created - A set of formulas developed by Bill James and others - that estimates a player’s total contributions - to a team’s runs total. - This is computed with the "technical" formula when possible. - If SB or CS data is missing, the "basic" formula is used. - If HBP, IBB, SH, SF, or GIDP data is missing, the "stolen base" version of the formula is used. - Team Runs Created is the sum of player Runs Created. |
| `RC/G` | `RCpG` | Runs Created per Game - Runs created per (approximately) 27 outs used. - Can be thought of as the runs produced by a lineup of 9 of this player. |
| `AIR` | `batter_air` | Hitting AIR - measures the offensive level of the leagues and parks the - player played in relative to an all-time - average of a .335 OBP and .400 Slugging Percentage. Over 100 - indicates a favorable setting for hitters, under 100 a favorable - setting for pitchers. |
| `BAbip` | `batting_avg_bip` | Batting Avg. on Balls in Plays (Hits - Home Runs)/(At Bats - SO - HR + Sac Flies) - This also measures how effectively the - defense turned balls into outs. |
| `BA` | `batting_avg` | Hits/At Bats - For recent years, leaders need 3.1 PA - per team game played - Bold indicates either highest BA using current stats - or awarded title at end of year. |
| `lgBA` | `batting_avg_lg` | League Batting Average - The batting average a league average - (non-pitcher) would have had in the same park(s). |
| `OBP` | `onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) - For recent years, leaders need 3.1 PA - per team game played |
| `lgOBP` | `onbase_perc_lg` | League On-base Percentage - The on-base percentage a league average - (non-pitcher) would have had in the same park(s). |
| `SLG` | `slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `lgSLG` | `slugging_perc_lg` | League Slugging Percentage - The slugging percentage a league average - (non-pitcher) would have had in the same park(s). |
| `OPS` | `onbase_plus_slugging` | On-Base + Slugging Percentages - For recent years, leaders need 3.1 PA - per team game played |
| `lgOPS` | `onbase_plus_slugging_lg` | League On-Base + Slugging - The OPS a league average - (non-pitcher) would have had in the same park(s). |
| `OPS+` | `onbase_plus_slugging_plus` | OPS+ - 100*[OBP/lg OBP + SLG/lg SLG - 1] - Adjusted to the player’s ballpark(s) |
| `OWn%` | `offensive_winning_perc` | Offensive Winning Percentage - The percentage of games a team with nine of this player - batting would win. Assumes average pitching and defense. - This uses the Pythagorean win pct formula with the player's RC/G for runs scored and the league's R/9 as runs allowed. |
| `BtRuns` | `abRuns` | Adjusted Batting Runs - A set of formulas developed by Gary Gillette, Pete Palmer and others - that estimates a player’s total contributions - to a team’s runs total via linear weights. - 0.0 is an avg performance, <0 is worse than avg and >0 is better than avg |
| `BtWins` | `abWins` | Adjusted Batting Wins - A set of formulas developed by Gary Gillette, Pete Palmer and others - that estimates a player’s total contributions - to a team’s wins with his bat. - 0.0 is an avg performance, <0 is worse than avg and >0 is better than avg |
| `TotA` | `total_avg` | Total Average - Developed by Thomas Boswell of the Washington Post - (Total Bases + HBP + BB + SB) / (AB - H + CS + GIDP) |
| `SecA` | `secondary_avg` | Secondary Average - (Total Bases - Hits + BB + SB - CS) / AB - Over .500, excellent; < 200, poor |
| `ISO` | `isolated_slugging_perc` | (Total Bases - H)/At Bats or - (2B + 2*3B + 3*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `PwrSpd` | `power_speed_number` | Power/Speed Number - 2 x (Home Runs x Stolen Bases)/(Stolen Bases + Home Runs) - The harmonic mean of HR and SB. - To do well you need a lot of both. - Developed by Bill James. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Situational_Batting

192 rows, 47 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `R/G` | `runs_per_game` | Runs Scored Per Game |
| `PA` | `PA_pbp` | Plate Appearances - The number of plate appearances for which we have play-by-play data. - Note that batted ball type and location data is incomplete prior to 1988. |
| `Ptn%` | `PA_with_platoon_adv_perc` | Percentage of PA with the platoon advantage - Switch hitters should be 100% for most cases. - For pitchers, facing a batter of the same hand. - For batters, facing a pitcher of the opposite hand. |
| `H` | `H_all` | All Hits |
| `Inf` | `H_inf` | Infield Hits - Batted ball type and location is not complete prior to 1988. |
| `Bnt` | `H_bunt` | Bunt Hits - Batted ball type and location is not complete prior to 1988. |
| `AB` | `PH_ab` | Pinch Hit At Bats |
| `H_2` | `PH_h` | Pinch Hits |
| `HR` | `PH_hr` | Pinch Hit Home Runs |
| `RBI` | `PH_rbi` | Pinch Hit Runs Batted In |
| `PHlev` | `PH_leverage` | Pinch Hit Leverage Index - The importance of the context in which the Pinch Hitter was used - Above one means higher than average pressure. - Below one means lower than average pressure. |
| `All` | `HR_all` | Home Run Total |
| `GS` | `HR_gs` | Grand Slam Home Runs |
| `GSo` | `HR_gs_opp` | Grand Slam Opportunities - Plate Appearances with the Bases Loaded |
| `vRH` | `HR_vrh` | Home Runs off Right-Handers |
| `vLH` | `HR_vlh` | Home Runs off Left-Handers |
| `Hm` | `HR_hm` | Home Runs at Home |
| `Rd` | `HR_rd` | Home Runs on the Road |
| `IP` | `HR_iphr` | Inside-The-Park Home Runs - Note that batted ball type and location data is incomplete prior to 1988. |
| `Att` | `SH_att` | Sacrifice Bunts Attempted - Only includes unsuccessful bunts made and bunt strikeouts. - Failing to bunt early in the count and then swinging away later are not included. - Pre-1954 SH attempt counts are unavailable. |
| `Suc` | `SH_suc` | Successful Sacrifice Bunts |
| `%` | `SH_perc` | Sacrifice Bunts Success Rate - Only includes unsuccessful bunts made and bunt strikeouts. - Failing to bunt early in the count and then swinging away later are not included. - Pre-1954 SH attempt counts are unavailable. |
| `Opp` | `GIDP_opp` | Opportunity for a Grounded Into Double Play - Runner on first with less than two outs. |
| `DP` | `GIDP_suc` | Grounded Into Double Play - Two or more outs via force outs on a ground ball. |
| `%_2` | `GIDP_perc` | Grounded Into Double Play Rate - Two or more outs via force outs on a ground ball. |
| `Opp_2` | `productive_outs_opp` | Productive Outs Made or Failed - Created by Elias and ESPN for three possible situations. - Successful Sac for a pitcher with one out. - Advancing any runner with none out. - Driving in a baserunner with the second out of the inning. - Failed means the batter made an out without advancing the runner(s). |
| `Suc_2` | `productive_outs` | Productive Outs Made - Created by Elias and ESPN for three possible situations. - Successful Sac for a pitcher with one out. - Advancing any runner with none out. - Driving in a baserunner with the second out of the inning. - Failed means the batter made an out without advancing the runner(s). |
| `%_3` | `productive_outs_perc` | Productive Outs Percentage - Created by Elias and ESPN for three possible situations. - Successful Sac for a pitcher with one out. - Advancing any runner with none out. - Driving in a baserunner with the second out of the inning. - Failed means the batter made an out without advancing the runner(s). |
| `BR` | `baserunners_tot` | Total Number of Baserunners when batter at plate |
| `BRS` | `drove_in_tot` | Baserunners who Scored - Total runners scored by batter (may not be by RBIs) |
| `BRS%` | `baserunners_scored_perc` | Percentage of all baserunners who scored on the batter’s play - (not necessarily with an RBI). |
| `<2,3B` | `lt_2_out_on_third_opp` | PAs with less than two out, runner on third |
| `Scr` | `lt_2_out_on_third_scored` | PAs with less than two out, runner on third and runner scored |
| `%_4` | `lt_2_out_on_third_perc` | PAs with less than two out, runner on third and runner scored |
| `0,2B` | `no_out_on_second_opp` | PAs with no out, runner on second |
| `Adv` | `no_out_on_second_adv` | PAs with none out, runner on second and runner advanced |
| `%_5` | `no_out_on_second_perc` | PAs with none out, runner on second and runner advanced Rate |
| `PAu` | `PA_unknown` | Plate Appearances for which data is not known - Note that for many stats (like pitcher SLG, 2B, 3B allowed, WPA, HR direction, etc.) - this will mean that the totals given are incomplete. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Standard_Batting

192 rows, 37 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `#Bat` | `batters_used` | Number of Players used in Games |
| `BatAge` | `age_bat` | Batters’ average age - Weighted by AB + Games Played |
| `R/G` | `runs_per_game` | Runs Scored Per Game |
| `G` | `G` | Games Played or Pitched |
| `PA` | `PA` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `AB` | `AB` | At Bats |
| `R` | `R` | Runs Scored/Allowed |
| `H` | `H` | Hits/Hits Allowed |
| `2B` | `2B` | Doubles |
| `3B` | `3B` | Triples |
| `HR` | `HR` | Home Runs Hit/Allowed |
| `RBI` | `RBI` | Runs Batted In |
| `SB` | `SB` | Stolen Bases |
| `CS` | `CS` | Caught Stealing |
| `BB` | `BB` | Bases on Balls/Walks |
| `SO` | `SO` | Strikeouts |
| `BA` | `batting_avg` | Hits/At Bats - For recent years, leaders need 3.1 PA - per team game played - Bold indicates either highest BA using current stats - or awarded title at end of year. |
| `OBP` | `onbase_perc` | (H + BB + HBP)/(At Bats + BB + HBP + SF) - For recent years, leaders need 3.1 PA - per team game played |
| `SLG` | `slugging_perc` | Total Bases/At Bats or - (1B + 2*2B + 3*3B + 4*HR)/AB - For recent years, leaders need 3.1 PA - per team game played |
| `OPS` | `onbase_plus_slugging` | On-Base + Slugging Percentages - For recent years, leaders need 3.1 PA - per team game played |
| `OPS+` | `onbase_plus_slugging_plus` | OPS+ - 100*[OBP/lg OBP + SLG/lg SLG - 1] - Adjusted to the player’s ballpark(s) |
| `TB` | `TB` | Total Bases - Singles + 2 x Doubles + 3 x Triples + 4 x Home Runs. |
| `GDP` | `GIDP` | Double Plays Grounded Into - Only includes standard 6-4-3, 4-3, etc. double plays. - First tracked in 1933. - For gamelogs only in seasons we have play-by-play, we include triple plays as well. - All official seasonal totals do not include GITP's. |
| `HBP` | `HBP` | Times Hit by a Pitch. |
| `SH` | `SH` | Sacrifice Hits (Sacrifice Bunts) |
| `SF` | `SF` | Sacrifice Flies - First tracked in 1954. |
| `IBB` | `IBB` | Intentional Bases on Balls - First tracked in 1955. |
| `LOB` | `LOB` | Runners Left On Base |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Standard_Fielding

192 rows, 27 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `#Fld` | `fielders_used` | Number of Players used as Fielders |
| `RA/G` | `runs_allowed_per_game` | Runs Allowed Per Game |
| `DefEff` | `defensive_efficiency` | Defensive Efficiency - Percentage of balls in play converted into outs - This is an estimate based on team defensive and pitching stats. - We utilize two estimates of plays made. - One using innings pitched, strikeouts, double plays and outfield assists. - And the other with batters faced, strikeouts, hits allowed, walks allowed, hbp, and .71 * errors committed (avg percent of errors that result in an ROE) - Total plays available are plays made + hits allowed - home runs + error committed estimate. |
| `G` | `G` | Games Played or Pitched |
| `GS` | `GS` | Games Started |
| `CG` | `CG` | Complete Game |
| `Inn` | `Inn_def` | Innings Played in Field |
| `Ch` | `chances` | Defensive Chances - Putouts + Assists + Errors |
| `PO` | `PO` | Putouts |
| `A` | `A` | Assists |
| `E` | `E_def` | Errors Committed |
| `DP` | `DP_def` | Double Plays Turned |
| `Fld%` | `fielding_perc` | Fielding Percentage - (Putouts + Assists) / (Putouts + Assists + Errors) |
| `Rtot` | `tz_runs_total` | Total Zone Total Fielding Runs Above Avg - The number of runs above or below average the player was worth based on the number of plays made. - This number combines the R tz , R dp , R of , R catch numbers into a total defensive contribution. - See the glossary section for a more complete explanation. - Provided by BaseballProjection.com |
| `Rtot/yr` | `tz_runs_total_per_season` | Total Zone Total Fielding Runs Above Avg per 1,200 Inn - The number of runs above or below average the fielder was worth per 1,200 Innings (approx 135 games). - This number combines the R tz , R dp , R of , R catch numbers into a total defensive contribution. - See the glossary section for a more complete explanation. - Provided by BaseballProjection.com |
| `Rdrs` | `bis_runs_total_team` | BIS Defensive Runs Saved Above Avg - The number of runs above or below average the team was worth based on their overall defense. - This number combines the individual players' defensive runs saved as well as team-level runs saved from shifting and positioning into a total team defensive contribution. - Provided by Baseball Info Solutions |
| `Rdrs/yr` | `bis_runs_total_per_season_team` | BIS Defensive Runs Saved Above Avg per 1,200 Inn - The number of runs above or below average the team's fielders were worth per 1,200 Innings (approx 135 games). - This number combines the R pm , R dp , and R good numbers into a total defensive contribution. - For pitchers, this is set to 200 Innings. - This does not include any team-level runs saved from positioning or shifting. - Provided by Baseball Info Solutions |
| `Rgood` | `bis_runs_good_plays` | BIS Good Plays/Misplays Runs Above Avg - The number of runs above or below average the player was worth based on plays where they made an exceptional contribution or obviously misplayed the situation. - Provided by Baseball Info Solutions |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Standard_Pitching

192 rows, 44 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `#P` | `pitchers_used` | Number of Pitchers used in Games |
| `PAge` | `age_pitch` | Pitchers’ average age - Weighted by 3*GS + G + SV |
| `RA/G` | `runs_allowed_per_game` | Runs Allowed Per Game |
| `W` | `W` | Wins |
| `L` | `L` | Losses |
| `W-L%` | `win_loss_perc` | Win-Loss Percentage - W / (W + L) - For players, leaders need one decision for every ten team games. - For managers, minimum to qualify for leading is 320 games. |
| `ERA` | `earned_run_avg` | 9 * ER / IP - For recent years, leaders need 1 IP - per team game played. - Bold indicates lowest ERA using current stats - Gold means awarded ERA title at end of year. |
| `G` | `G` | Games Played or Pitched |
| `GS` | `GS` | Games Started |
| `GF` | `GF` | Games Finished - Credited to the last pitcher to appear for a team in a game. - Complete Games are not counted as Games Finished. |
| `CG` | `CG` | Complete Game |
| `tSho` | `SHO_team` | Shutouts by a team - No runs allowed in a game by one or more pitchers. |
| `cSho` | `SHO_cg` | Shutouts - No runs allowed and a complete game. |
| `SV` | `SV` | Saves |
| `IP` | `IP` | Innings Pitched |
| `H` | `H` | Hits/Hits Allowed |
| `R` | `R` | Runs Scored/Allowed |
| `ER` | `ER` | Earned Runs Allowed |
| `HR` | `HR` | Home Runs Hit/Allowed |
| `BB` | `BB` | Bases on Balls/Walks |
| `IBB` | `IBB` | Intentional Bases on Balls - First tracked in 1955. |
| `SO` | `SO` | Strikeouts |
| `HBP` | `HBP` | Times Hit by a Pitch. |
| `BK` | `BK` | Balks |
| `WP` | `WP` | Wild Pitches |
| `BF` | `batters_faced` | Batters Faced |
| `ERA+` | `earned_run_avg_plus` | ERA+ - 100*[lgERA/ERA] - Adjusted to the player’s ballpark(s). |
| `FIP` | `fip` | Fielding Independent Pitching - this stat measures a pitcher's effectiveness at preventing HR, BB, HBP and causing SO - (13*HR + 3*(BB+HBP) - 2*SO)/IP + Constant lg - The constant is set so that each season major-league average FIP is the same as the major-league avg ERA |
| `WHIP` | `whip` | (BB + H)/IP - For recent years, leaders need 1 IP - per team game played |
| `H9` | `hits_per_nine` | 9 x H / IP - For recent years, leaders need 1 IP - per team game played |
| `HR9` | `home_runs_per_nine` | 9 x HR / IP - For recent years, leaders need 1 IP - per team game played |
| `BB9` | `bases_on_balls_per_nine` | 9 x BB / IP - For recent years, leaders need 1 IP - per team game played |
| `SO9` | `strikeouts_per_nine` | 9 x SO / IP - For recent years, leaders need 1 IP - per team game played |
| `SO/W` | `strikeouts_per_base_on_balls` | SO/W or SO/BB - For recent years, pitching leaders need 1 IP - per team game played. - No batting leaders computed. |
| `LOB` | `LOB` | Runners Left On Base |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Starter_Pitching

192 rows, 41 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `G` | `G` | Games Played or Pitched |
| `GS` | `GS` | Games Started |
| `Wgs` | `W_GS` | Wins in games started |
| `Lgs` | `L_GS` | Losses in games started |
| `ND` | `no_decision_GS` | No Decisions in Games Started |
| `Wchp` | `W_cheap` | Cheap Wins - Wins in starts with < 6 IP or more than 3 ER - Or wins in non-quality starts. |
| `Ltuf` | `L_tough` | Tough Losses - Losses in quality starts |
| `Wtm` | `W_team` | Team Wins in games started |
| `Ltm` | `L_team` | Team Losses in games started |
| `tmW-L%` | `win_loss_perc_team` | Team Win-Loss Percentage - Wtm / (Wtm + Ltm) - The win-loss percentage of the team in games started by this pitcher. |
| `Wlst` | `W_lost` | Wins Lost - At the time the pitcher faced his final batter - the pitcher was in position for a win, - but game was blown by bullpen. |
| `Lsv` | `L_saved` | Losses Saved - At the time of his last batter - the pitcher was in position for a loss, - but team came back to tie or take lead. |
| `CG` | `CG` | Complete Game |
| `SHO` | `SHO` | Shutouts - No runs allowed and a complete game. |
| `QS` | `QS` | Quality Start - Pitcher pitched at least 6 innings - and allowed 3 or fewer earned runs in a start. |
| `QS%` | `quality_start_perc` | Quality Start Percentage - Percentage of starts that were quality starts (≥ 6 IP, ≤ 3 ER). |
| `GmScA` | `game_score_avg` | Average Game Score |
| `Best` | `game_score_best` | Best Game Score |
| `Wrst` | `game_score_worst` | Worst Game Score |
| `BQR` | `bequeathed_runners` | Bequeathed Runners - Number of runners on base when pitcher left the game. - This includes both starts and games in relief. |
| `BQS` | `bequeathed_score` | Bequeathed Runners Score - Number or percentage of runners on base when pitcher left the game who subsequently scored. - These runners show up in the pitcher’s ERA. - This includes both starts and games in relief. |
| `sDR` | `DR_short` | Short Days Rest - Less than four days rest. |
| `lDR` | `DR_long` | Long Days Rest - More than four days rest. |
| `RS/GS` | `run_support_cg` | Run Support per Game - Runs scored/27 outs in the entire - game when the pitcher started. |
| `RS/IP` | `run_support_pg` | Run Support per Innings - Runs scored/27 outs while the pitcher was in the game as the pitcher. |
| `IP/GS` | `innings_per_start` | Innings Pitched per Game Started |
| `Pit/GS` | `pitches_per_start` | Pitches per Game Started |
| `<80` | `pitches_lt80` | GS with under 80 pitches |
| `80-99` | `pitches_80to99` | GS with 80 to 99 pitches |
| `100-119` | `pitches_100to119` | GS with 100 to 119 pitches |
| `≥120` | `pitches_ge120` | GS with 120 or more pitches |
| `Max` | `pitches_max` | Most pitches in a start |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Starting_Lineups

180 rows, 20 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Tm` | `team_name` | Team as listed in the source table. |
| `C` | `c` | Primary catcher. |
| `1B` | `1b` | Primary first baseman. |
| `2B` | `2b` | Primary second baseman. |
| `3B` | `3b` | Primary third baseman. |
| `SS` | `ss` | Primary shortstop. |
| `LF` | `lf` | Primary left fielder. |
| `CF` | `cf` | Primary center fielder. |
| `RF` | `rf` | Primary right fielder. |
| `DH` | `dh` | Primary designated hitter. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Value_Batting

186 rows, 27 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `G` | `G` | Games Played or Pitched |
| `PA` | `PA` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `Rbat` | `runs_bat` | Runs Batting - Number of runs better or worse than average the player was as a hitter. - This is based on a modified version of wRAA. - See our about section for a full description of how this is calculated. |
| `Rbaser` | `runs_br` | Runs from Baserunning - Number of runs better or worse than average the player was for all baserunning events. - SB, CS, PB, WP, Defensive Indifference. - Developed by Sean Smith of BaseballProjection.com |
| `Rdp` | `runs_dp` | Runs Grounded into Double Plays - Number of runs better or worse than average the player was at avoiding grounding into double plays. - Developed by Sean Smith of BaseballProjection.com |
| `Rfield` | `runs_fielding` | Runs from Fielding - Number of runs better or worse than average the player was for all fielding. - Fielding of balls in play, turning double plays, outfield arms and catcher defense are all included. - We use Baseball Info Solutions Defensive Runs Saved when available - (note that we do not use BIS catcher framing runs RszC ) and - Total Zone Rating from Sean Smith when not. - For Negro League seasons, we use Defensive Regression Analysis from Michael Humphreys. - Our WAR framework was developed by Sean Smith of BaseballProjection.com |
| `Rpos` | `runs_pos` | Runs from Positional Scarcity - Number of runs above or below average due to positional differences. - Positions like C, SS, and 2B get a bonus. - Positions like 1B, DH, LF get a penalty. - Developed by Sean Smith of BaseballProjection.com |
| `RAA` | `runs_above_avg_bat` | Runs better than Avg - It is the number of runs this player is better than a league average player. |
| `WAA` | `WAA` | Wins Above Avg - This is the wins added by this player above that of an average player. We compute the waaW-L% using a PythagenPat conversion and then subtract .500 and multiply by the number of games played. |
| `Rrep` | `runs_replacement` | Runs from Replacement Level - Number of runs an average player is better than a replacement player. - Replacement is set for a .294 team winning percentage. - Stronger leagues may get a larger bonus. - Developed by Sean Smith of BaseballProjection.com |
| `RAR` | `runs_above_rep` | Runs above Replacement Level - Total of other columns It is the number of runs this player is better than a replacement player. Replacement is set for a .294 team winning percentage. Developed by Sean Smith of BaseballProjection.com |
| `WAR` | `WAR` | Wins Above Replacement - A single number that presents the number of wins the player added - to the team above what a replacement player (think AAA or AAAA) would add. - Scale for a single-season: 8+ MVP Quality, 5+ All-Star Quality, 2+ Starter, - 0-2 Reserve, < 0 Replacement Level - Developed by Sean Smith of BaseballProjection.com |
| `waaWL%` | `waa_win_perc` | Win-Loss% w/ Avg. Team - This is the win-loss of an otherwise average team in ONLY the games this player played in. - For example, for a pitcher this would only consider the games the pitcher threw in and ignoring games they did not play in. |
| `162WL%` | `waa_win_perc_162` | Win-Loss% w/ Avg. Team Season - This is the win-loss of an otherwise average team for an entire season giving them credit for only the games this player played in. - For example, for a pitcher this would be waaW-L% - in the games the pitcher threw in and a .500 record otherwise. |
| `oWAR` | `WAR_off` | Offensive Wins Above Replacement (everything but Fielding) - The same statistic as Wins Above Replacement for Position - Players (WAR), but with the fielding value excluded. - oWAR + dWAR does not equal WAR. - Adding would count positions twice. - Contains the factor for batting stats, baserunning, a positional adjustment, and the replacement player adjustment. - Factors developed by Sean Smith of BaseballProjection.com |
| `dWAR` | `WAR_def` | Defensive Wins Above Replacement for position players - A defensive measure of wins above replacement, but given - only the defensive stats of the player and his position adjustment. For this calculation, we use a - replacement level on defense is the league average. - Based on Baseball Info Solutions defensive runs saved from 2003 on - and total zone rating developed by Sean Smith of BaseballProjection.com previously |
| `oRAR` | `runs_above_rep_off` | Offensive Runs above Replacement Level - oWAR + dWAR DOES NOT EQUAL WAR, pos would be counted 2x - Total of all columns except for fielding values - Includes batting, baserunning, positional adjustment, and a playing time adjustment - for the number of runs an average player is better than a replacement player. - Replacement is set for a .294 team winning percentage. - Developed by Sean Smith of BaseballProjection.com |
| `Salary` | `Salary` | These values may not include every bonus the player received in a season. - They are also often missing values for mid-season callups or players acquired in-season. - Post-1984 seasons are mostly complete, pre-1985 is mostly incomplete. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Value_Pitching

186 rows, 29 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `IP` | `IP` | Innings Pitched |
| `G` | `G` | Games Played or Pitched |
| `GS` | `GS` | Games Started |
| `R` | `R` | Runs Scored/Allowed |
| `RA9` | `runs_avg` | Runs Allowed Per 9 IP - This is like ERA, but with unearned runs included. |
| `RA9opp` | `opp_runs_avg` | Opponents’ Runs Scored Per 9 Inn - The average number of runs scored by this pitcher's opposition, per 9 innings. We use park factors to convert the opponent scoring to a league-average context.For in progress seasons, we consider the teams’ last 365 days. Interleague road games are excluded from the avg, and when the pitcher faces an interleague opp at home, we modify the opponent run scoring by .20 runs per 9inning depending on whether the DH is added or removed from their lineup. We assume a league average pitcher would allow this many runs. |
| `RA9def` | `runs_avg_defense` | Runs per 9 IP of support from defense - This is based on the team’s Baseball Info Solutions Defensive Runs Saved since 2003 and Total Zone Rating before that. Negro League seasons use Defensive Regression Analysis. Positive values mean the team defense was above average. Negative means it was below average. We take the team’s total balls in play, the balls in play for this pitcher and the team’s total runs saved and split the runs among all of the team’s pitchers. |
| `RA9role` | `runs_avg_sprp` | Runs per 9 IP difference for SP and RP - From 1960 on we assess factor for starters and relievers. In that time, relievers have averaged a much lower ERA, and this factor accounts for that difference. Previously, this was part of our replacement level calculation, but it has now been moved into Runs Above Avg. |
| `RA9extras` | `runs_avg_extras` | Runs per 9 IP difference for pitching in extra innings - Starting in 2020, MLB had teams begin every extra inning with a runner on second base. If this runner scores, it is charged to the pitcher who started the inning. We adjust the pitcher's expected runs by the run expectancy that is added by the runner being placed on second base (approx 0.6 runs) for each time they start an extra inning. |
| `PPFp` | `PPF_custom` | Park Factor customized for parks the pitcher threw in - From 1908 on, we have full gamelogs, so we can say exactly how many innings a pitcher threw in each park. These are 3-year park factors weighted by batters faced in each park. Note the one-game park factor is the team PPF/100 minus 1 times two plus one, since the factors on team pages are for home and road games combined. |
| `RA9avg` | `runs_avg_avg_pitcher` | Runs per 9 IP for an avg pitcher - Equals PPFp/100*(oppRA9 - RAdef + RArole) - This is our best estimate of what an average pitcher would do against these opponents, with this defense and in these parks. |
| `RAA` | `runs_above_avg_pitch` | Runs better than Avg - IP*(RA9 avg - RA9)/9, then centered so the league average is always zero. - It is the number of runs this player is better than an average player. Adjusted for quality of opposition, parks pitched in and quality of team defense and recentered, so the league is zero. |
| `WAA` | `WAA` | Wins Above Avg - This is the wins added by this player above that of an average player. We compute the waaW-L% using a PythagenPat conversion and then subtract .500 and multiply by the number of games played. |
| `gmLI` | `GR_leverage_index_avg` | game-entering Leverage Index - Solely for relief appearances, this is the average of each appearances opening leverage index - weighted by the batters faced in that outing. - The average pressure the pitcher or batter saw in this game or season. - 1.0 is average pressure, below 1.0 is low pressure and above 1.0 is high pressure. |
| `WAAadj` | `WAA_adj` | Wins Above Avg Adjustment - For relief pitchers, we multiply WAA by (1+gmLI)/2. This is done in recognition of the added importance of high leverage. WAA adj is the additional value of this leverage adjustment. Also, the manner in which this and the WAA calculations are performed cause the league total WAA to move away from zero, so we also do an operation to recenter the entire league. The recentering forces the league sum to 0 which is as it should be for Wins Above Average. So for the league as a whole, WAA+WAA adj will equal zero and WAR = WAA + WAA adj + Replacement value |
| `WAR` | `WAR_pitch` | Wins Above Replacement for Pitchers - A single number that presents the number of wins the player added - to the team above what a replacement player (think AAA or AAAA) would add. This value includes defensive support and includes additional value for high leverage situations. - Scale: 8+ MVP Quality, 5+ All-Star Quality, 2+ Starter, - 0-2 Reserve, < 0 Replacement Level - Developed by Sean Smith of BaseballProjection.com |
| `RAR` | `runs_above_rep_pitch` | Runs better than Replacement Level - It is the number of runs this player is better than a replacement player. Replacement is set for a .294 team winning percentage. - Developed by Sean Smith of BaseballProjection.com |
| `waaWL%` | `waa_win_perc` | Win-Loss% w/ Avg. Team - This is the win-loss of an otherwise average team in ONLY the games this player played in. - For example, for a pitcher this would only consider the games the pitcher threw in and ignoring games they did not play in. |
| `162WL%` | `waa_win_perc_162` | Win-Loss% w/ Avg. Team Season - This is the win-loss of an otherwise average team for an entire season giving them credit for only the games this player played in. - For example, for a pitcher this would be waaW-L% - in the games the pitcher threw in and a .500 record otherwise. |
| `Salary` | `Salary` | These values may not include every bonus the player received in a season. - They are also often missing values for mid-season callups or players acquired in-season. - Post-1984 seasons are mostly complete, pre-1985 is mostly incomplete. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Win_Probability_Batting

192 rows, 30 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `R/G` | `runs_per_game` | Runs Scored Per Game |
| `BtRuns` | `abRuns` | Adjusted Batting Runs - A set of formulas developed by Gary Gillette, Pete Palmer and others - that estimates a player’s total contributions - to a team’s runs total via linear weights. - 0.0 is an avg performance, <0 is worse than avg and >0 is better than avg |
| `BtWins` | `abWins` | Adjusted Batting Wins - A set of formulas developed by Gary Gillette, Pete Palmer and others - that estimates a player’s total contributions - to a team’s wins with his bat. - 0.0 is an avg performance, <0 is worse than avg and >0 is better than avg |
| `Plays` | `wpa_plays` | Plays included in WPA calculations - For batters, this includes all batting plays and baserunning plays where they were the lead baserunner whose state changed. |
| `WPA` | `wpa_bat` | Win Probability Added for Offensive Player - Given average teams, this is the change in probability - caused by this batter during the game. - See Win Expectancy explainer for details. |
| `WPA+` | `wpa_bat_pos` | Win Probability Added - Sum of positive events for this batter. |
| `WPA-` | `wpa_bat_neg` | Win Probability Subtracted - Sum of negative events for this batter. |
| `aLI` | `leverage_index_avg` | Average Leverage Index - The average pressure the pitcher or batter saw in this game or season. - 1.0 is average pressure, below 1.0 is low pressure and above 1.0 is high pressure. |
| `WPA/LI` | `wpa_li_bat` | Situational Wins (WPA/LI) - It is the sum of WPA divided by the leverage index for each play. - WPA depends greatly on the context of the at bats. - This stat does not. |
| `Clutch` | `wpa_clutch` | WPA Clutch - WPA (overall)/aLI - WPA/LI (as shown) - The difference between context dependent WPA and the context-neutral WPA. |
| `cWPA` | `cwpa_bat` | Championship Win Probability Added for Offensive Player - Given average teams, this is the change in probability of winning the World Series, displayed in percentage points. - See Win Expectancy explainer for details. |
| `cWPA+` | `cwpa_bat_pos` | Championship Win Probability Added - Sum of positive events for this batter. - Displayed in percentage points. |
| `cWPA-` | `cwpa_bat_neg` | Championship Win Probability Subtracted - Sum of negative events for this batter. - Displayed in percentage points. |
| `acLI` | `cli_avg` | Average Championship Leverage Index - The average pressure the pitcher or batter saw in this game or season. - 1.0 is average pressure, below 1.0 is low pressure and above 1.0 is high pressure. |
| `cClutch` | `cwpa_clutch` | cWPA Clutch - cWPA (overall)/acLI - cWPA/cLI (as shown) - The difference between context dependent cWPA and the context-neutral cWPA. - Displayed in percentage points. |
| `RE24` | `re24_bat` | Base-Out Runs Added - Given the bases occupied/out situation, how many runs did the batter - or baserunner add in the resulting play. - Compared to average, so 0 is average, and above 0 is better than average |
| `REW` | `rew_bat` | Base-Out Wins Added (REW) - This is the number of wins above average the player was worth by their performance measured by the 24 - base-out situations across every play in the game. |
| `boLI` | `bo_leverage_index_avg` | Base-Out Leverage - The average base-out leverage seen across all plays. |
| `RE24/boLI` | `re24_boli` | Situational Runs - The summation of for each play the change in run-expectancy divided by the base-out leverage |
| `PHlev` | `PH_leverage` | Pinch Hit Leverage Index - The importance of the context in which the Pinch Hitter was used - Above one means higher than average pressure. - Below one means lower than average pressure. |
| `AB` | `PH_ab` | Pinch Hit At Bats |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Team_Win_Probability_Pitching

192 rows, 31 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Tm` | `team_name` | Team as listed in the source table. |
| `RA/G` | `runs_allowed_per_game` | Runs Allowed Per Game |
| `PtchR` | `apRuns` | Adjusted Pitching Runs - A set of formulas developed by Gary Gillette, Pete Palmer and others - that estimates a pitcher’s total contributions - to a team’s runs total via linear weights. - 0.0 is an avg performance, <0 is worse than avg and >0 is better than avg |
| `PtchW` | `apWins` | Adjusted Pitching Wins - A set of formulas developed by Gary Gillette, Pete Palmer and others - that estimates a pitcher’s total contributions - to a team’s wins with his arm. - 0.0 is an avg performance, <0 is worse than avg and >0 is better than avg |
| `Plays` | `wpa_plays` | Plays included in WPA calculations - For batters, this includes all batting plays and baserunning plays where they were the lead baserunner whose state changed. |
| `WPA` | `wpa_def` | Win Probability Added by Pitcher - Given average teams, this is the change in probability. - See Win Expectancy explainer for details. |
| `WPA+` | `wpa_def_pos` | Win Probability Added - Sum of positive events for this pitcher. |
| `WPA-` | `wpa_def_neg` | Win Probability Subtracted - Sum of negative events for this pitcher. |
| `aLI` | `leverage_index_avg` | Average Leverage Index - The average pressure the pitcher or batter saw in this game or season. - 1.0 is average pressure, below 1.0 is low pressure and above 1.0 is high pressure. |
| `WPA/LI` | `wpa_li_def` | Situational Wins (WPA/LI) - It is the sum of WPA divided by the leverage index for each play. - WPA depends greatly on the context of the at bats. - This stat does not. |
| `Clutch` | `wpa_clutch` | WPA Clutch - WPA (overall)/aLI - WPA/LI (as shown) - The difference between context dependent WPA and the context-neutral WPA. |
| `cWPA` | `cwpa_def` | Championship Win Probability Added by Pitcher - Given average teams, this is the change in probability of winning the World Series, displayed in percentage points. - See Win Expectancy explainer for details. |
| `cWPA+` | `cwpa_def_pos` | Championship Win Probability Added - Sum of positive events for this pitcher. - Displayed in percentage points. |
| `cWPA-` | `cwpa_def_neg` | Championship Win Probability Subtracted - Sum of negative events for this pitcher. - Displayed in percentage points. |
| `acLI` | `cli_avg` | Average Championship Leverage Index - The average pressure the pitcher or batter saw in this game or season. - 1.0 is average pressure, below 1.0 is low pressure and above 1.0 is high pressure. |
| `cClutch` | `cwpa_clutch` | cWPA Clutch - cWPA (overall)/acLI - cWPA/cLI (as shown) - The difference between context dependent cWPA and the context-neutral cWPA. - Displayed in percentage points. |
| `RE24` | `re24_def` | Base-Out Runs Saved - Given the bases occupied/out situation, how many runs did the pitcher - save in the resulting play. Compared to average, so 0 is average, and - above 0 is better than average |
| `REW` | `rew_def` | Base-Out Wins Saved - This is the number of wins above average the player was worth by their performance - measured by the 24 base-out situations. |
| `boLI` | `bo_leverage_index_avg` | Base-Out Leverage - The average base-out leverage seen across all plays. |
| `RE24/boLI` | `re24_boli` | Situational Runs - The summation of for each play the change in run-expectancy divided by the base-out leverage |
| `LevHi` | `enter_leverage_high` | Games entered with High Leverage - The first PA of the pitcher’s appearance - has a leverage of 1.5 or higher. |
| `LevMd` | `enter_leverage_med` | Games entered with Medium Leverage - The first PA of the pitcher’s appearance - has a leverage between 0.7 and 1.5. |
| `LevLo` | `enter_leverage_low` | Games entered with Low Leverage - The first PA of the pitcher’s appearance - has a leverage of 0.7 or lower. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Transactions

20,428 rows, 8 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `parsed` | Season year of the transactions page. |
| `Transaction_Date` | `parsed` | Date as printed by Baseball-Reference. |
| `Date` | `parsed` | ISO (YYYY-MM-DD) transaction date. |
| `Transaction` | `parsed` | Full transaction text. |
| `Team` | `parsed` | First club mentioned. |
| `Teams_Involved` | `parsed` | All clubs mentioned, comma separated. |
| `Player_ID` | `parsed` | First player mentioned. |
| `Players_Involved` | `parsed` | All player ids mentioned, comma separated. |

### Uniform_Numbers

9,602 rows, 9 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Uniform_Number` | `parsed` | Jersey number worn that season. |
| `Player` | `parsed` | Player name. |
| `Player_ID` | `parsed` | Baseball-Reference player id. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |

### Win_Probability_Batting

5,185 rows, 35 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Bats` | `derived` | Batting hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `PA` | `PA` | Plate Appearances - When available, we use actual plate appearances from play-by-play game accounts - Otherwise estimated using AB + BB + HBP + SF + SH, - which excludes catcher interferences. - When this color click for a summary of each PA. |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `BtRuns` | `abRuns` | Adjusted Batting Runs - A set of formulas developed by Gary Gillette, Pete Palmer and others - that estimates a player’s total contributions - to a team’s runs total via linear weights. - 0.0 is an avg performance, <0 is worse than avg and >0 is better than avg |
| `BtWins` | `abWins` | Adjusted Batting Wins - A set of formulas developed by Gary Gillette, Pete Palmer and others - that estimates a player’s total contributions - to a team’s wins with his bat. - 0.0 is an avg performance, <0 is worse than avg and >0 is better than avg |
| `Plays` | `wpa_plays` | Plays included in WPA calculations - For batters, this includes all batting plays and baserunning plays where they were the lead baserunner whose state changed. |
| `WPA` | `wpa_bat` | Win Probability Added for Offensive Player - Given average teams, this is the change in probability - caused by this batter during the game. - See Win Expectancy explainer for details. |
| `WPA+` | `wpa_bat_pos` | Win Probability Added - Sum of positive events for this batter. |
| `WPA-` | `wpa_bat_neg` | Win Probability Subtracted - Sum of negative events for this batter. |
| `aLI` | `leverage_index_avg` | Average Leverage Index - The average pressure the pitcher or batter saw in this game or season. - 1.0 is average pressure, below 1.0 is low pressure and above 1.0 is high pressure. |
| `WPA/LI` | `wpa_li_bat` | Situational Wins (WPA/LI) - It is the sum of WPA divided by the leverage index for each play. - WPA depends greatly on the context of the at bats. - This stat does not. |
| `Clutch` | `wpa_clutch` | WPA Clutch - WPA (overall)/aLI - WPA/LI (as shown) - The difference between context dependent WPA and the context-neutral WPA. |
| `cWPA` | `cwpa_bat` | Championship Win Probability Added for Offensive Player - Given average teams, this is the change in probability of winning the World Series, displayed in percentage points. - See Win Expectancy explainer for details. |
| `cWPA+` | `cwpa_bat_pos` | Championship Win Probability Added - Sum of positive events for this batter. - Displayed in percentage points. |
| `cWPA-` | `cwpa_bat_neg` | Championship Win Probability Subtracted - Sum of negative events for this batter. - Displayed in percentage points. |
| `acLI` | `cli_avg` | Average Championship Leverage Index - The average pressure the pitcher or batter saw in this game or season. - 1.0 is average pressure, below 1.0 is low pressure and above 1.0 is high pressure. |
| `cClutch` | `cwpa_clutch` | cWPA Clutch - cWPA (overall)/acLI - cWPA/cLI (as shown) - The difference between context dependent cWPA and the context-neutral cWPA. - Displayed in percentage points. |
| `RE24` | `re24_bat` | Base-Out Runs Added - Given the bases occupied/out situation, how many runs did the batter - or baserunner add in the resulting play. - Compared to average, so 0 is average, and above 0 is better than average |
| `REW` | `rew_bat` | Base-Out Wins Added (REW) - This is the number of wins above average the player was worth by their performance measured by the 24 - base-out situations across every play in the game. |
| `boLI` | `bo_leverage_index_avg` | Base-Out Leverage - The average base-out leverage seen across all plays. |
| `RE24/boLI` | `re24_boli` | Situational Runs - The summation of for each play the change in run-expectancy divided by the base-out leverage |
| `PHlev` | `PH_leverage` | Pinch Hit Leverage Index - The importance of the context in which the Pinch Hitter was used - Above one means higher than average pressure. - Below one means lower than average pressure. |
| `AB` | `PH_ab` | Pinch Hit At Bats |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

### Win_Probability_Pitching

6,405 rows, 36 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Division_Full` | `identifier/derived` | League and division combined, e.g. "AL East". |
| `Rk` | `ranker` | Rank - This is a count of the rows from top to bottom. - It is recalculated following the sorting of a column. |
| `Name` | `player` | Player Name - Bold can mean player is active for this team - or player has appeared in the majors - * means LHP or LHB, - # means switch hitter, - + can mean HOFer. |
| `Throws` | `derived` | Throwing hand (L/R/S), derived from the handedness marker Baseball-Reference appends to the player name. |
| `Age` | `age` | Player’s age at midnight of June 30th of that year |
| `Tm` | `team_ID` | Team as listed in the source table. |
| `IP` | `IP` | Innings Pitched |
| `PtchR` | `apRuns` | Adjusted Pitching Runs - A set of formulas developed by Gary Gillette, Pete Palmer and others - that estimates a pitcher’s total contributions - to a team’s runs total via linear weights. - 0.0 is an avg performance, <0 is worse than avg and >0 is better than avg |
| `PtchW` | `apWins` | Adjusted Pitching Wins - A set of formulas developed by Gary Gillette, Pete Palmer and others - that estimates a pitcher’s total contributions - to a team’s wins with his arm. - 0.0 is an avg performance, <0 is worse than avg and >0 is better than avg |
| `Plays` | `wpa_plays` | Plays included in WPA calculations - For batters, this includes all batting plays and baserunning plays where they were the lead baserunner whose state changed. |
| `WPA` | `wpa_def` | Win Probability Added by Pitcher - Given average teams, this is the change in probability. - See Win Expectancy explainer for details. |
| `WPA+` | `wpa_def_pos` | Win Probability Added - Sum of positive events for this pitcher. |
| `WPA-` | `wpa_def_neg` | Win Probability Subtracted - Sum of negative events for this pitcher. |
| `aLI` | `leverage_index_avg` | Average Leverage Index - The average pressure the pitcher or batter saw in this game or season. - 1.0 is average pressure, below 1.0 is low pressure and above 1.0 is high pressure. |
| `WPA/LI` | `wpa_li_def` | Situational Wins (WPA/LI) - It is the sum of WPA divided by the leverage index for each play. - WPA depends greatly on the context of the at bats. - This stat does not. |
| `Clutch` | `wpa_clutch` | WPA Clutch - WPA (overall)/aLI - WPA/LI (as shown) - The difference between context dependent WPA and the context-neutral WPA. |
| `cWPA` | `cwpa_def` | Championship Win Probability Added by Pitcher - Given average teams, this is the change in probability of winning the World Series, displayed in percentage points. - See Win Expectancy explainer for details. |
| `cWPA+` | `cwpa_def_pos` | Championship Win Probability Added - Sum of positive events for this pitcher. - Displayed in percentage points. |
| `cWPA-` | `cwpa_def_neg` | Championship Win Probability Subtracted - Sum of negative events for this pitcher. - Displayed in percentage points. |
| `acLI` | `cli_avg` | Average Championship Leverage Index - The average pressure the pitcher or batter saw in this game or season. - 1.0 is average pressure, below 1.0 is low pressure and above 1.0 is high pressure. |
| `cClutch` | `cwpa_clutch` | cWPA Clutch - cWPA (overall)/acLI - cWPA/cLI (as shown) - The difference between context dependent cWPA and the context-neutral cWPA. - Displayed in percentage points. |
| `RE24` | `re24_def` | Base-Out Runs Saved - Given the bases occupied/out situation, how many runs did the pitcher - save in the resulting play. Compared to average, so 0 is average, and - above 0 is better than average |
| `REW` | `rew_def` | Base-Out Wins Saved - This is the number of wins above average the player was worth by their performance - measured by the 24 base-out situations. |
| `boLI` | `bo_leverage_index_avg` | Base-Out Leverage - The average base-out leverage seen across all plays. |
| `RE24/boLI` | `re24_boli` | Situational Runs - The summation of for each play the change in run-expectancy divided by the base-out leverage |
| `LevHi` | `enter_leverage_high` | Games entered with High Leverage - The first PA of the pitcher’s appearance - has a leverage of 1.5 or higher. |
| `LevMd` | `enter_leverage_med` | Games entered with Medium Leverage - The first PA of the pitcher’s appearance - has a leverage between 0.7 and 1.5. |
| `LevLo` | `enter_leverage_low` | Games entered with Low Leverage - The first PA of the pitcher’s appearance - has a leverage of 0.7 or lower. |
| `Player_ID` | `identifier/derived` | Baseball-Reference's stable player identifier - the join key across datasets. |
| `Row_Type` | `identifier/derived` | 'data' for player rows; 'summary' for footer rows such as Team Totals. |

## Game Level

Workbook: `MLB_Game_Level_2020-2025.xlsx` - 2 sheets, 493,300 rows.

### Batting_Orders

234,828 rows, 18 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Game_Num` | `parsed` | Team game number within the season. |
| `Game_Date` | `parsed` | ISO (YYYY-MM-DD) game date. |
| `Weekday` | `parsed` | Day of the week as printed by Baseball-Reference. |
| `Home_Away` | `parsed` | Home or Away. |
| `Opponent` | `parsed` | Opponent franchise code. |
| `Result` | `parsed` | W, L or T for the team in this row. |
| `Score` | `parsed` | Final score as printed, team runs first. |
| `Opp_Started_LHP` | `parsed` | True when the opponent started a left-handed pitcher. |
| `Batting_Order_Slot` | `parsed` | Spot in the batting order, 1 through 9. |
| `Player` | `parsed` | Player surname as printed in the grid. |
| `Position` | `parsed` | Fielding position the player occupied in that game. |
| `Player_ID` | `parsed` | Baseball-Reference player id from the cell link. |

### Defensive_Lineups

258,472 rows, 17 columns.

| Column | Source code | Description |
| --- | --- | --- |
| `Season` | `identifier/derived` | Season year. 2020-2025 for season data; 2026 on the current 40-man snapshot. |
| `Team` | `identifier/derived` | Baseball-Reference franchise code (e.g. NYY). The Athletics are OAK through 2024 and ATH from 2025. 2TM/3TM marks a combined line for a player who changed clubs. |
| `Team_Name` | `identifier/derived` | Full club name as of that season. |
| `League` | `identifier/derived` | AL or NL. |
| `League_Name` | `identifier/derived` | American League or National League. |
| `Division` | `identifier/derived` | East, Central or West. |
| `Game_Num` | `parsed` | Team game number within the season. |
| `Game_Date` | `parsed` | ISO (YYYY-MM-DD) game date. |
| `Weekday` | `parsed` | Day of the week as printed by Baseball-Reference. |
| `Home_Away` | `parsed` | Home or Away. |
| `Opponent` | `parsed` | Opponent franchise code. |
| `Result` | `parsed` | W, L or T for the team in this row. |
| `Score` | `parsed` | Final score as printed, team runs first. |
| `Opp_Started_LHP` | `parsed` | True when the opponent started a left-handed pitcher. |
| `Position` | `parsed` | Fielding position for this lineup slot. |
| `Player` | `parsed` | Player surname as printed in the grid. |
| `Player_ID` | `parsed` | Baseball-Reference player id from the cell link. |
