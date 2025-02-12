---
title: NBA Draft vs. Draft Boards
author: Robert Huang
date: '2019-08-13'
slug: nba-draft-vs-draft-boards
categories: []
tags:
  - nba
  - nba draft
---
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />




## Background

Heading into the NBA draft, the is a general consensus on the rough order that the current crop of prospects should be selected. This can be seen through the numerous draft boards for a given year available on many websites, created by both professional and amateur draft prognosticators. Analysts project who they think will have the best NBA careers using a combination of their own scouting abilities, some group think, and, for the more well-connected individuals, whatever information they may have gathered from league insiders or team executives.

While the public has an idea of where players will be selected, the NBA teams doing the actual selections have their own draft boards. Teams operate under more information than individuals not involved with the draft process, watching players work out in person, conducting interviews with the players and the people around them, and doing whatever background or medical checks are needed.

Even with all this information, teams sometimes make decisions that are baffling to NBA watchers, drafting players way ahead of where they are projected to go. Other players that are highly regarded going into the draft fall heavily. Most recently in the 2019 draft, Oregon center Bol Bol was originally projected to go in the middle of the first round, but watched team after team bypass him until he fell to the Denver Nuggets in the middle of the second round at 44.

Who were the players that rose and fell the most compared to their projected positions? Were the decisions to overdraft or skip over players the correct ones?


## Overview

We look at NBA drafts from 2008 to 2019 because of the number of available pre-draft rankings for this period. This number grows each year, with five boards used for 2008 and 22 used for 2019. The rankings come from a variety of sources, including major sports publications like ESPN and CBS Sports, draft specific sites like DraftExpress and NBADraft.net, and personal blogs by draft enthusiasts. The rankings utilized are always "big boards" as opposed to mock drafts. Big boards are pure rankings of the NBA potential of prospects, regardless of fit or intel on where a player will fall to a team. Mock drafts attempt to predict draft position, regardless of the author's beliefs about a player's outlook. These individual draft boards are aggregated together using a point system (100 points for 1st, 99 points for 2nd...) to produce overall rankings.



Player pre-draft rankings and actual draft positions are plotted below for an overview of the relationship between the two variables. As expected, there is a strong linear relationship between the two. Players are drafted roughly in the order of how analysts project their future NBA careers to turn out. This relationship is strong for the highest ranked players, but weakens as we move down either the board rankings or pick number, with the greatest variation at the end of the draft. This is not unusual as it becomes more difficult for scouts to differentiate players that deep into the pool.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-2-1.png" width="672" style="display: block; margin: auto;" />



Players that fall below the x = y line are reaches by teams, selected earlier than their pre-draft rankings. Players that fall above the line have slipped, selected below their pre-draft ranking. Considering only players that were drafted, 39% fell, 55% rose, and 7% were drafted at exactly their ranking. The larger percentage of players that rose is a result of there being only 60 picks in any draft but no limit on the number of players on draft boards. There are many players ranked inside the top 60 on draft boards that end up undrafted. These players are represented in the panel above the main plot.

The size and shade of the circles for each player correspond to their career Win Shares ranking among players from the same draft. Larger and darker circles represent players that have had better careers as of the 2018-19 NBA season. This is used as a quick look of the relationship between player quality and draft position, with players drafted earlier or ranked higher pre-draft generally having stronger careers. Note that this is not a definitive statement on the players, especially for players from more recent drafts that have not played many seasons.


## "Overdrafted"

<div style="border: 1px solid #ddd; padding: 0px; overflow-y: scroll; height:500px; "><table class="table table-striped table-hover table-condensed table-responsive" style="width: auto !important; margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> Year </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Team </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Player </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> College </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Games </th>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> Pick </th>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> Rank </th>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> Difference </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 2014 </td>
   <td style="text-align:left;"> TOR </td>
   <td style="text-align:left;"> Bruno Caboclo </td>
   <td style="text-align:left;">  </td>
   <td style="text-align:left;"> 69 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 127 </td>
   <td style="text-align:right;"> -107 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2009 </td>
   <td style="text-align:left;"> CLE </td>
   <td style="text-align:left;"> Christian Eyenga </td>
   <td style="text-align:left;">  </td>
   <td style="text-align:left;"> 51 </td>
   <td style="text-align:right;"> 30 </td>
   <td style="text-align:right;"> 65 </td>
   <td style="text-align:right;"> -35 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2014 </td>
   <td style="text-align:left;"> OKC </td>
   <td style="text-align:left;"> Josh Huestis </td>
   <td style="text-align:left;"> Stanford </td>
   <td style="text-align:left;"> 76 </td>
   <td style="text-align:right;"> 29 </td>
   <td style="text-align:right;"> 61 </td>
   <td style="text-align:right;"> -32 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2016 </td>
   <td style="text-align:left;"> PHO </td>
   <td style="text-align:left;"> Georgios Papagiannis </td>
   <td style="text-align:left;">  </td>
   <td style="text-align:left;"> 39 </td>
   <td style="text-align:right;"> 13 </td>
   <td style="text-align:right;"> 44 </td>
   <td style="text-align:right;"> -31 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2013 </td>
   <td style="text-align:left;"> IND </td>
   <td style="text-align:left;"> Solomon Hill </td>
   <td style="text-align:left;"> Arizona </td>
   <td style="text-align:left;"> 305 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 51 </td>
   <td style="text-align:right;"> -28 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2015 </td>
   <td style="text-align:left;"> LAL </td>
   <td style="text-align:left;"> Larry Nance Jr. </td>
   <td style="text-align:left;"> Wyoming </td>
   <td style="text-align:left;"> 259 </td>
   <td style="text-align:right;"> 27 </td>
   <td style="text-align:right;"> 54 </td>
   <td style="text-align:right;"> -27 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2019 </td>
   <td style="text-align:left;"> GSW </td>
   <td style="text-align:left;"> Jordan Poole </td>
   <td style="text-align:left;"> Michigan </td>
   <td style="text-align:left;">  </td>
   <td style="text-align:right;"> 28 </td>
   <td style="text-align:right;"> 55 </td>
   <td style="text-align:right;"> -27 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2012 </td>
   <td style="text-align:left;"> IND </td>
   <td style="text-align:left;"> Miles Plumlee </td>
   <td style="text-align:left;"> Duke </td>
   <td style="text-align:left;"> 346 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 52 </td>
   <td style="text-align:right;"> -26 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2016 </td>
   <td style="text-align:left;"> BOS </td>
   <td style="text-align:left;"> Guerschon Yabusele </td>
   <td style="text-align:left;">  </td>
   <td style="text-align:left;"> 74 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 41 </td>
   <td style="text-align:right;"> -25 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2011 </td>
   <td style="text-align:left;"> SAS </td>
   <td style="text-align:left;"> Cory Joseph </td>
   <td style="text-align:left;"> Texas </td>
   <td style="text-align:left;"> 528 </td>
   <td style="text-align:right;"> 29 </td>
   <td style="text-align:right;"> 51 </td>
   <td style="text-align:right;"> -22 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2008 </td>
   <td style="text-align:left;"> BOS </td>
   <td style="text-align:left;"> J.R. Giddens </td>
   <td style="text-align:left;"> New Mexico </td>
   <td style="text-align:left;"> 38 </td>
   <td style="text-align:right;"> 30 </td>
   <td style="text-align:right;"> 51 </td>
   <td style="text-align:right;"> -21 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2013 </td>
   <td style="text-align:left;"> MIN </td>
   <td style="text-align:left;"> Andre Roberson </td>
   <td style="text-align:left;"> Colorado </td>
   <td style="text-align:left;"> 295 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 46 </td>
   <td style="text-align:right;"> -20 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2011 </td>
   <td style="text-align:left;"> NYK </td>
   <td style="text-align:left;"> Iman Shumpert </td>
   <td style="text-align:left;"> Georgia Tech </td>
   <td style="text-align:left;"> 446 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> -19 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2016 </td>
   <td style="text-align:left;"> MIL </td>
   <td style="text-align:left;"> Thon Maker </td>
   <td style="text-align:left;">  </td>
   <td style="text-align:left;"> 195 </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 29 </td>
   <td style="text-align:right;"> -19 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2016 </td>
   <td style="text-align:left;"> TOR </td>
   <td style="text-align:left;"> Pascal Siakam </td>
   <td style="text-align:left;"> New Mexico State </td>
   <td style="text-align:left;"> 216 </td>
   <td style="text-align:right;"> 27 </td>
   <td style="text-align:right;"> 45 </td>
   <td style="text-align:right;"> -18 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2013 </td>
   <td style="text-align:left;"> PHO </td>
   <td style="text-align:left;"> Nemanja Nedovic </td>
   <td style="text-align:left;">  </td>
   <td style="text-align:left;"> 24 </td>
   <td style="text-align:right;"> 30 </td>
   <td style="text-align:right;"> 47 </td>
   <td style="text-align:right;"> -17 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2016 </td>
   <td style="text-align:left;"> IND </td>
   <td style="text-align:left;"> Caris LeVert </td>
   <td style="text-align:left;"> Michigan </td>
   <td style="text-align:left;"> 168 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 37 </td>
   <td style="text-align:right;"> -17 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2008 </td>
   <td style="text-align:left;"> SAC </td>
   <td style="text-align:left;"> Jason Thompson </td>
   <td style="text-align:left;"> Rider </td>
   <td style="text-align:left;"> 588 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 28 </td>
   <td style="text-align:right;"> -16 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2009 </td>
   <td style="text-align:left;"> POR </td>
   <td style="text-align:left;"> Victor Claver </td>
   <td style="text-align:left;">  </td>
   <td style="text-align:left;"> 80 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 37 </td>
   <td style="text-align:right;"> -15 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2010 </td>
   <td style="text-align:left;"> CHI </td>
   <td style="text-align:left;"> Kevin Seraphin </td>
   <td style="text-align:left;">  </td>
   <td style="text-align:left;"> 423 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 32 </td>
   <td style="text-align:right;"> -15 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2016 </td>
   <td style="text-align:left;"> DEN </td>
   <td style="text-align:left;"> Juan Hernangomez </td>
   <td style="text-align:left;">  </td>
   <td style="text-align:left;"> 157 </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 30 </td>
   <td style="text-align:right;"> -15 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2018 </td>
   <td style="text-align:left;"> LAC </td>
   <td style="text-align:left;"> Jerome Robinson </td>
   <td style="text-align:left;"> Boston College </td>
   <td style="text-align:left;"> 33 </td>
   <td style="text-align:right;"> 13 </td>
   <td style="text-align:right;"> 28 </td>
   <td style="text-align:right;"> -15 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2019 </td>
   <td style="text-align:left;"> SAS </td>
   <td style="text-align:left;"> Luka Samanic </td>
   <td style="text-align:left;">  </td>
   <td style="text-align:left;">  </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 34 </td>
   <td style="text-align:right;"> -15 </td>
  </tr>
</tbody>
</table></div>

We look at the players that had the largest difference between their pre-draft rankings and actual pick positions, starting with the ones that went earlier than more highly regarded players. This list is limited to only players drafted in the first round. The second round is generally viewed as more difficult to predict and a crapshoot compared to the first. Given the lower stakes, teams reach for players they like regardless of other available prospects. Teams sometimes do not have enough roster slots or do not want to use cap space to take on more players and will instead pick international prospects to stash overseas for a period of time.

Bruno Caboclo tops the list of draft reaches by a significant margin. Entering the 2014 draft ranked all the way at 127 (and completed off the boards of many analysts), the Toronto Raptors shocked the NBA community when they selected him at 20. Caboclo projected as a raw project then and has not done much to change that perception today. Rather than for anything on the court, he is still most remembered as being described by commentator [Fran Fraschilla](https://youtu.be/6CtQbGI1258) as being "two years away from being two years away" after the selection was made during the draft broadcast.

The next two players, Christian Eyenga and Josh Huestis, were drafted about 30 places above their board ranking, but both were basically second round picks. [Georgios Papagiannis](https://www.sactownroyalty.com/2018/2/28/16993924/why-did-georgios-papagiannis-get-picked-so-high), viewed as a mid-second round talent, was selected in the late lottery in 2016 by the Phoenix Suns who then traded him to the Sacramento Kings. He was waived by the Kings in 2018 before his first contract was up and is now back playing is his home country of Greece. In the same draft, the Milwaukee Bucks swung for the fences with Thon Maker at 10. Despite some flashes, he was traded away to the Pistons while still on his rookie contract. Guerschon Yabusele went 25 places ahead of his ranking and is no longer with the Celtics after only two seasons. Jason Thompson was not the the 12th best player in the 2008 draft, but actually provided the Kings with seven seasons as a starter.

There are players on the above list that outperform their draft positions, difficult to do given that their pick number is already inflated. Pascal Siakam and Caris LeVert are the obvious standouts. Siakam was probably ranked too low because he did not possess much offensive upside, and Levert was ranked lower than his talent level because of medical concerns. Despite those worries, both have proven that they should have been considered way earlier than where they were actually picked (at 27 and 20, respectively).


## "Underdrafted"

<div style="border: 1px solid #ddd; padding: 0px; overflow-y: scroll; height:500px; "><table class="table table-striped table-hover table-condensed table-responsive" style="width: auto !important; margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> Year </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Team </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Player </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> College </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;"> Games </th>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> Pick </th>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> Rank </th>
   <th style="text-align:right;position: sticky; top:0; background-color: #FFFFFF;"> Difference </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 2010 </td>
   <td style="text-align:left;"> ORL </td>
   <td style="text-align:left;"> Stanley Robinson </td>
   <td style="text-align:left;"> Connecticut </td>
   <td style="text-align:left;"> 0 </td>
   <td style="text-align:right;"> 59 </td>
   <td style="text-align:right;"> 28 </td>
   <td style="text-align:right;"> 31 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2010 </td>
   <td style="text-align:left;"> DAL </td>
   <td style="text-align:left;"> Solomon Alabi </td>
   <td style="text-align:left;"> Florida State </td>
   <td style="text-align:left;"> 26 </td>
   <td style="text-align:right;"> 50 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 28 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2017 </td>
   <td style="text-align:left;"> IND </td>
   <td style="text-align:left;"> Ike Anigbogu </td>
   <td style="text-align:left;"> UCLA </td>
   <td style="text-align:left;"> 14 </td>
   <td style="text-align:right;"> 47 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 27 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2019 </td>
   <td style="text-align:left;"> MIA </td>
   <td style="text-align:left;"> Bol Bol </td>
   <td style="text-align:left;"> Oregon </td>
   <td style="text-align:left;">  </td>
   <td style="text-align:right;"> 44 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 27 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2018 </td>
   <td style="text-align:left;"> HOU </td>
   <td style="text-align:left;"> De'Anthony Melton </td>
   <td style="text-align:left;"> USC </td>
   <td style="text-align:left;"> 50 </td>
   <td style="text-align:right;"> 46 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 26 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2010 </td>
   <td style="text-align:left;"> LAC </td>
   <td style="text-align:left;"> Willie Warren </td>
   <td style="text-align:left;"> Oklahoma </td>
   <td style="text-align:left;"> 19 </td>
   <td style="text-align:right;"> 54 </td>
   <td style="text-align:right;"> 29 </td>
   <td style="text-align:right;"> 25 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2016 </td>
   <td style="text-align:left;"> BOS </td>
   <td style="text-align:left;"> Demetrius Jackson </td>
   <td style="text-align:left;"> Notre Dame </td>
   <td style="text-align:left;"> 26 </td>
   <td style="text-align:right;"> 45 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 23 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2013 </td>
   <td style="text-align:left;"> MEM </td>
   <td style="text-align:left;"> Jamaal Franklin </td>
   <td style="text-align:left;"> San Diego State </td>
   <td style="text-align:left;"> 24 </td>
   <td style="text-align:right;"> 41 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 22 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2018 </td>
   <td style="text-align:left;"> MIN </td>
   <td style="text-align:left;"> Keita Bates-Diop </td>
   <td style="text-align:left;"> Ohio State </td>
   <td style="text-align:left;"> 30 </td>
   <td style="text-align:right;"> 48 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 22 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2008 </td>
   <td style="text-align:left;"> LAC </td>
   <td style="text-align:left;"> DeAndre Jordan </td>
   <td style="text-align:left;"> Texas A&amp;M </td>
   <td style="text-align:left;"> 819 </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 21 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2016 </td>
   <td style="text-align:left;"> BOS </td>
   <td style="text-align:left;"> Deyonta Davis </td>
   <td style="text-align:left;"> Michigan State </td>
   <td style="text-align:left;"> 107 </td>
   <td style="text-align:right;"> 31 </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 21 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2013 </td>
   <td style="text-align:left;"> MIN </td>
   <td style="text-align:left;"> Lorenzo Brown </td>
   <td style="text-align:left;"> NC State </td>
   <td style="text-align:left;"> 103 </td>
   <td style="text-align:right;"> 52 </td>
   <td style="text-align:right;"> 32 </td>
   <td style="text-align:right;"> 20 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2008 </td>
   <td style="text-align:left;"> NJN </td>
   <td style="text-align:left;"> Chris Douglas-Roberts </td>
   <td style="text-align:left;"> Memphis </td>
   <td style="text-align:left;"> 222 </td>
   <td style="text-align:right;"> 40 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 19 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2010 </td>
   <td style="text-align:left;"> LAL </td>
   <td style="text-align:left;"> Devin Ebanks </td>
   <td style="text-align:left;"> West Virginia </td>
   <td style="text-align:left;"> 63 </td>
   <td style="text-align:right;"> 43 </td>
   <td style="text-align:right;"> 24 </td>
   <td style="text-align:right;"> 19 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2019 </td>
   <td style="text-align:left;"> ORL </td>
   <td style="text-align:left;"> Talen Horton-Tucker </td>
   <td style="text-align:left;"> Iowa State </td>
   <td style="text-align:left;">  </td>
   <td style="text-align:right;"> 46 </td>
   <td style="text-align:right;"> 27 </td>
   <td style="text-align:right;"> 19 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2009 </td>
   <td style="text-align:left;"> DET </td>
   <td style="text-align:left;"> Chase Budinger </td>
   <td style="text-align:left;"> Arizona </td>
   <td style="text-align:left;"> 407 </td>
   <td style="text-align:right;"> 44 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 18 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2013 </td>
   <td style="text-align:left;"> UTA </td>
   <td style="text-align:left;"> Erick Green </td>
   <td style="text-align:left;"> Virginia Tech </td>
   <td style="text-align:left;"> 52 </td>
   <td style="text-align:right;"> 46 </td>
   <td style="text-align:right;"> 28 </td>
   <td style="text-align:right;"> 18 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2013 </td>
   <td style="text-align:left;"> SAS </td>
   <td style="text-align:left;"> Deshaun Thomas </td>
   <td style="text-align:left;"> Ohio State </td>
   <td style="text-align:left;"> 0 </td>
   <td style="text-align:right;"> 58 </td>
   <td style="text-align:right;"> 40 </td>
   <td style="text-align:right;"> 18 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2010 </td>
   <td style="text-align:left;"> SAC </td>
   <td style="text-align:left;"> Hassan Whiteside </td>
   <td style="text-align:left;"> Marshall </td>
   <td style="text-align:left;"> 343 </td>
   <td style="text-align:right;"> 33 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 17 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2017 </td>
   <td style="text-align:left;"> PHI </td>
   <td style="text-align:left;"> Jawun Evans </td>
   <td style="text-align:left;"> Oklahoma State </td>
   <td style="text-align:left;"> 56 </td>
   <td style="text-align:right;"> 39 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 17 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2009 </td>
   <td style="text-align:left;"> POR </td>
   <td style="text-align:left;"> Patrick Mills </td>
   <td style="text-align:left;"> Saint Mary's (CA) </td>
   <td style="text-align:left;"> 605 </td>
   <td style="text-align:right;"> 55 </td>
   <td style="text-align:right;"> 39 </td>
   <td style="text-align:right;"> 16 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2011 </td>
   <td style="text-align:left;"> MEM </td>
   <td style="text-align:left;"> Josh Selby </td>
   <td style="text-align:left;"> Kansas </td>
   <td style="text-align:left;"> 38 </td>
   <td style="text-align:right;"> 49 </td>
   <td style="text-align:right;"> 33 </td>
   <td style="text-align:right;"> 16 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2012 </td>
   <td style="text-align:left;"> MIL </td>
   <td style="text-align:left;"> Doron Lamb </td>
   <td style="text-align:left;"> Kentucky </td>
   <td style="text-align:left;"> 100 </td>
   <td style="text-align:right;"> 42 </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 16 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2008 </td>
   <td style="text-align:left;"> BOS </td>
   <td style="text-align:left;"> Semih Erden </td>
   <td style="text-align:left;">  </td>
   <td style="text-align:left;"> 69 </td>
   <td style="text-align:right;"> 60 </td>
   <td style="text-align:right;"> 45 </td>
   <td style="text-align:right;"> 15 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2009 </td>
   <td style="text-align:left;"> MEM </td>
   <td style="text-align:left;"> Sam Young </td>
   <td style="text-align:left;"> Pittsburgh </td>
   <td style="text-align:left;"> 249 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 15 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2009 </td>
   <td style="text-align:left;"> SAS </td>
   <td style="text-align:left;"> DeJuan Blair </td>
   <td style="text-align:left;"> Pittsburgh </td>
   <td style="text-align:left;"> 424 </td>
   <td style="text-align:right;"> 37 </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 15 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2010 </td>
   <td style="text-align:left;"> PHO </td>
   <td style="text-align:left;"> Gani Lawal </td>
   <td style="text-align:left;"> Georgia Tech </td>
   <td style="text-align:left;"> 1 </td>
   <td style="text-align:right;"> 46 </td>
   <td style="text-align:right;"> 31 </td>
   <td style="text-align:right;"> 15 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2013 </td>
   <td style="text-align:left;"> POR </td>
   <td style="text-align:left;"> Jeff Withey </td>
   <td style="text-align:left;"> Kansas </td>
   <td style="text-align:left;"> 206 </td>
   <td style="text-align:right;"> 39 </td>
   <td style="text-align:right;"> 24 </td>
   <td style="text-align:right;"> 15 </td>
  </tr>
</tbody>
</table></div>

On the flip side, there are players who slipped in the draft, selected much later than expected. There is no player that slid down the draft as much as Bruno Caboclo climbed—also mathematically impossible given only 60 draft picks. At the top of the table is Stanley Robinson—originally projected as a late first round talent—who fell to the end of the second round, about 30 slots lower than expected. This decision turned out to be correct as Robinson has yet to appear in an NBA game as of the 2018-19 season.

Also in this group is the aforementioned Bol Bol, who with a pre-draft ranking of 17 is one of the more highly rated prospects to have fallen down a large number of spots in the draft. Deyonta Davis's projection as a lottery pick makes him the highest ranked player to have fell at least 15 spots. As with Stanley Robinson, this appears to be the right decision by NBA teams as he has not developed much of a career in the three seasons since he was drafted. We will wait and see with Bol Bol.

There are also successes on the list: DeAndre Jordan, ranked as a late lottery pick, fell to the second round but has made three All-NBA teams and one All-Star game; Hassan Whiteside, despite his faults, has put up counting stats that far exceed players drafted in the lottery; Patty Mills, a major depth piece for Spurs for multiple years, has proven that he should have been selected way above his board ranking of 39; DeJuan Blair, who fell to the second round because of injury concerns, has outperformed many players ahead of him. Jordan and Whiteside—probably the best players of this group—had two of the higher pre-draft rankings relative to the others, suggesting that what they have achieved in the NBA should not been too surprising to scouts.

Most of the other players above are second rounds picks with careers that are consistent with the average second rounder, spending one to three seasons in the NBA, always with sporadic playing time. This sometimes has less to do with talent, as teams do not feel the need to invest as much with players selected this low in the draft especially when compared to first rounders. Front offices may have a greater incentive to make sure youngsters selected early have every chance to succeed, given the criticism they may receive for having failed to make the most of a prized draft asset—in this case, the pick itself.

<table class="table table-striped table-hover table-condensed table-responsive" style="width: auto !important; margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:right;"> Year </th>
   <th style="text-align:left;"> Player </th>
   <th style="text-align:right;"> Rank </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 2015 </td>
   <td style="text-align:left;"> Christian Wood </td>
   <td style="text-align:right;"> 28 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2019 </td>
   <td style="text-align:left;"> Jontay Porter </td>
   <td style="text-align:right;"> 32 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2015 </td>
   <td style="text-align:left;"> Jonathan Holmes </td>
   <td style="text-align:right;"> 33 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2012 </td>
   <td style="text-align:left;"> Kevin Jones </td>
   <td style="text-align:right;"> 37 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2015 </td>
   <td style="text-align:left;"> Michael Frazier </td>
   <td style="text-align:right;"> 37 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2013 </td>
   <td style="text-align:left;"> C.J. Leslie </td>
   <td style="text-align:right;"> 38 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2015 </td>
   <td style="text-align:left;"> Robert Upshaw </td>
   <td style="text-align:right;"> 38 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2016 </td>
   <td style="text-align:left;"> Gary Payton II </td>
   <td style="text-align:right;"> 38 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2017 </td>
   <td style="text-align:left;"> Cameron Oliver </td>
   <td style="text-align:right;"> 38 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2017 </td>
   <td style="text-align:left;"> Johnathan Motley </td>
   <td style="text-align:right;"> 39 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2019 </td>
   <td style="text-align:left;"> Terence Davis </td>
   <td style="text-align:right;"> 39 </td>
  </tr>
</tbody>
</table>

We also look at players ranked higher than 40 on pre-draft boards that slipped completely out of the draft. Only one player since 2008, UNLV's Christian Wood, was projected as a first round talent to have gone undrafted. Wood did sign with a team after the draft and debuted in the NBA in the same season. This cannot be said of most of the other players in the above group, although many are still young enough for that to happen sometime in the future.

One key difference between the group of players that fell up in the draft and the group that fell down is the number of international players. Of the 23 players that climbed at least 15 spots, 10 played professionally overseas as prospects. Only 1 of the 28 players that fell at least 15 slots played internationally; the rest played college basketball in the US. Every player on the undrafted list also played NCAA basketball. This quirk could be the result of teams having better information on international players compared to the average draft analyst. A lot less video and English language articles on foreign players are available, affecting where analysts will slot them on their draft boards. College players, on the other hand, may be overrated by analysts, given the visibility of these athletes on TV or major sports websites. How many full games of Bruno Cabocolo playing in the Brazilian basketball league has the average scout watched? Stanley Robinson, on the other hand, played numerous games in his UConn career that were broadcast nationally.
