---
title: Soccer National Teams - Player Birthplaces
author: Robert Huang
date: '2026-02-18'
output:
  bookdown::html_document2:
    number_sections: false
slug: soccer-national-teams-player-birthplaces
categories: []
tags:
  - sports
  - soccer
---
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />

<style>
p.caption{
  color: gray;
  text-align: left;
}
</style>



Today we look at the makeup of national team squads in international soccer tournaments in terms of where players were born. Teams are generally represented by players that are born and raised in that country, but there has been an increasing shift in players declaring for countries where they were not born in—and may not have grown up in. The reasons for this may be familial, geopolitical, or sociological, but we're going to concentrate on the data. Specifically, we analyze what percent of a national team's squad in major international tournaments is made up of players born in that country. The difficulty of obtaining more in depth background information on players means we can't answer questions about where players were raised.

Squad lists are pulled from [Wikipedia](https://en.wikipedia.org/) for all major international tournaments starting with the 1998 World Cup (1998-06-10) and ending with the 2025 CAF Cup of Nations (2025-12-21). The tournaments included are:

<table class="table" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption><span id="tab:unnamed-chunk-1"></span>Table 1: International tournaments inlcuded in the data.</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Confederation </th>
   <th style="text-align:left;"> Tournament </th>
   <th style="text-align:right;"> First </th>
   <th style="text-align:right;"> Last </th>
   <th style="text-align:right;"> # of Editions </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> AFC </td>
   <td style="text-align:left;"> Asian Cup </td>
   <td style="text-align:right;"> 2000 </td>
   <td style="text-align:right;"> 2023 </td>
   <td style="text-align:right;"> 7 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> Cup Of Nations </td>
   <td style="text-align:right;"> 2000 </td>
   <td style="text-align:right;"> 2025 </td>
   <td style="text-align:right;"> 14 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CONCACAF </td>
   <td style="text-align:left;"> Gold Cup </td>
   <td style="text-align:right;"> 2000 </td>
   <td style="text-align:right;"> 2025 </td>
   <td style="text-align:right;"> 14 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CONMEBOL </td>
   <td style="text-align:left;"> Copa America </td>
   <td style="text-align:right;"> 1999 </td>
   <td style="text-align:right;"> 2024 </td>
   <td style="text-align:right;"> 10 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> FIFA </td>
   <td style="text-align:left;"> Confederations Cup </td>
   <td style="text-align:right;"> 1999 </td>
   <td style="text-align:right;"> 2017 </td>
   <td style="text-align:right;"> 7 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> FIFA </td>
   <td style="text-align:left;"> World Cup </td>
   <td style="text-align:right;"> 1998 </td>
   <td style="text-align:right;"> 2022 </td>
   <td style="text-align:right;"> 7 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> OFC </td>
   <td style="text-align:left;"> Nations Cup </td>
   <td style="text-align:right;"> 1998 </td>
   <td style="text-align:right;"> 2024 </td>
   <td style="text-align:right;"> 8 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> UEFA </td>
   <td style="text-align:left;"> Euro </td>
   <td style="text-align:right;"> 2000 </td>
   <td style="text-align:right;"> 2024 </td>
   <td style="text-align:right;"> 7 </td>
  </tr>
</tbody>
</table>

This is the World Cup, every confederation's primary national team competition, and the now defunct Confederations Cup. Note that some tournaments like the Copa America and Gold Cup sometimes invite nations from outside their respective confederations to participate—those squads are also included in our dataset. We try to assign every player on the roster a country of birth based on a variety of sources—primarily Wikipedia, [Transfermarkt](https://www.transfermarkt.com/), [National Football Teams](https://www.national-football-teams.com/), and [FBref](https://fbref.com/). While every effort is made to ensure the accuracy of birthplace information, there are possibly cases of errors in the resulting dataset. There are many situations where different sources list conflicting birth countries or cities. Biological details are scant for most footballers from smaller nations, with finding reliable data more difficult the farther back in history we go.

<div class="figure" style="text-align: center">
<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-2-1.png" alt="Percent of data with missing birthplace for each tournament." width="912" />
<p class="caption"><span id="fig:unnamed-chunk-2"></span>Figure 1: Percent of data with missing birthplace for each tournament.</p>
</div>

This is especially true of the OFC Nations Cup from 1998 to 2012 where between 25% and 50% of birthplaces are unknown. Keep this in mind for any results related to the OFC. Most tournaments are close to complete; the only other competition with more than 10% missing data is the 2000 CAF Cup of Nations.

For the main metric we're going to focus on in this analysis, any player with a birth country matching the national team they play for is considered home born. If those two values do not match, they are considered a non-home born player. Aggregating this result for the entire squad gives an overall % home born statistic. The key here is that percentages are calculated using roster spots as the denominator, not players. This means that the same players may be counted multiple times if they appeared in multiple tournaments for a country. More precisely, the interpretation of percent home born is the percent of all roster spots that are home born, not percent of players that are home born. This method applies for the entire analysis.


## By Tournament

<div class="figure" style="text-align: center">
<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-3-1.png" alt="Percent of roster slots used for home born players at each tournament. Aggregate totals for all tournaments are shown in the facet labels next to the tournament names." width="912" />
<p class="caption"><span id="fig:unnamed-chunk-3"></span>Figure 2: Percent of roster slots used for home born players at each tournament. Aggregate totals for all tournaments are shown in the facet labels next to the tournament names.</p>
</div>

We start by plotting the trend of home born players for every event. While tournaments like the Copa America, World Cup, and Nations Cup have been consistent in their use of home born players with maybe a slight dip in more recent years, others like the Cup of Nations and Gold Cup have shown a sharper drop in the percent of home born players. The Cup of Nations has gone from over 90% home born to under 70% in the last 25 years. From 2000 to 2007, the Gold Cup was at 90% but has dropped to 70% in 2025. The Asian Cup is somewhere in between with a slower but consistent decline. While the rates of change vary across confederations, what is obvious is that we're seeing fewer squad positions for home born players—particularly in Africa and North America. The only tournaments without a change are the European Championship and Confederations Cup (last held in 2017).

<table class="table" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption><span id="tab:unnamed-chunk-4"></span>Table 2: Tournaments with the highest percentage of home born players.</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Confederation </th>
   <th style="text-align:left;"> Tournament </th>
   <th style="text-align:right;"> Year </th>
   <th style="text-align:right;"> Teams </th>
   <th style="text-align:right;"> # Players </th>
   <th style="text-align:right;"> # Home Born </th>
   <th style="text-align:right;"> % Home Born </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> CONMEBOL </td>
   <td style="text-align:left;"> Copa America </td>
   <td style="text-align:right;"> 2001 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 258 </td>
   <td style="text-align:right;"> 255 </td>
   <td style="text-align:right;"> 98.8% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CONMEBOL </td>
   <td style="text-align:left;"> Copa America </td>
   <td style="text-align:right;"> 2004 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 264 </td>
   <td style="text-align:right;"> 259 </td>
   <td style="text-align:right;"> 98.1% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CONMEBOL </td>
   <td style="text-align:left;"> Copa America </td>
   <td style="text-align:right;"> 2007 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 264 </td>
   <td style="text-align:right;"> 257 </td>
   <td style="text-align:right;"> 97.3% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> FIFA </td>
   <td style="text-align:left;"> Confederations Cup </td>
   <td style="text-align:right;"> 2013 </td>
   <td style="text-align:right;"> 8 </td>
   <td style="text-align:right;"> 184 </td>
   <td style="text-align:right;"> 179 </td>
   <td style="text-align:right;"> 97.3% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> OFC </td>
   <td style="text-align:left;"> Nations Cup </td>
   <td style="text-align:right;"> 2012 </td>
   <td style="text-align:right;"> 8 </td>
   <td style="text-align:right;"> 135 </td>
   <td style="text-align:right;"> 131 </td>
   <td style="text-align:right;"> 97.0% </td>
  </tr>
</tbody>
</table>

<table class="table" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption><span id="tab:unnamed-chunk-4"></span>Table 2: Tournaments with the lowest percentage of home born players.</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Confederation </th>
   <th style="text-align:left;"> Tournament </th>
   <th style="text-align:right;"> Year </th>
   <th style="text-align:right;"> Teams </th>
   <th style="text-align:right;"> # Players </th>
   <th style="text-align:right;"> # Home Born </th>
   <th style="text-align:right;"> % Home Born </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> Cup Of Nations </td>
   <td style="text-align:right;"> 2023 </td>
   <td style="text-align:right;"> 24 </td>
   <td style="text-align:right;"> 627 </td>
   <td style="text-align:right;"> 408 </td>
   <td style="text-align:right;"> 65.1% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> Cup Of Nations </td>
   <td style="text-align:right;"> 2025 </td>
   <td style="text-align:right;"> 24 </td>
   <td style="text-align:right;"> 644 </td>
   <td style="text-align:right;"> 437 </td>
   <td style="text-align:right;"> 67.9% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> Cup Of Nations </td>
   <td style="text-align:right;"> 2021 </td>
   <td style="text-align:right;"> 24 </td>
   <td style="text-align:right;"> 656 </td>
   <td style="text-align:right;"> 446 </td>
   <td style="text-align:right;"> 68.0% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CONCACAF </td>
   <td style="text-align:left;"> Gold Cup </td>
   <td style="text-align:right;"> 2025 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 411 </td>
   <td style="text-align:right;"> 290 </td>
   <td style="text-align:right;"> 70.6% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CONCACAF </td>
   <td style="text-align:left;"> Gold Cup </td>
   <td style="text-align:right;"> 2023 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 370 </td>
   <td style="text-align:right;"> 273 </td>
   <td style="text-align:right;"> 73.8% </td>
  </tr>
</tbody>
</table>

The 2001 Copa America was the most home born tournament—255 out of 258 roster spots were used by players born in the country of their national teams (almost 99%!). The Copa America also occupies the second and third spots with similarly high percentages. On the opposite end is the 2023 Cup of Nations—only 408 out of 627 roster spots were used by home born players (65%). Appropriately, the second and third positions are also taken by other editions of the Cup of Nations.

It's useful to point out that these results are dependent on the specific nations that participate in the tournaments. Teams have to qualify for these tournaments, so the participants are not the same for different editions of the same tournament. The number of home born players for an individual year could be a lot lower than other years if the rate is dragged down by a nation that depends heavily on outside born players, especially if they do not qualify for the other years.

## By Country

<div class="figure" style="text-align: center">
<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-5-1.png" alt="AFC - Percent of roster slots used for home born players at each tournament. Only teams that have participated in a least 3 tournaments are plotted." width="912" />
<p class="caption"><span id="fig:unnamed-chunk-5"></span>Figure 3: AFC - Percent of roster slots used for home born players at each tournament. Only teams that have participated in a least 3 tournaments are plotted.</p>
</div>

We dig a little deeper by looking at how the usage of home born players by individual countries has evolved over time, covering only national teams that have participated in at least 3 tournaments. Starting with the AFC, we see that a few countries experienced a dip in the use of home born players after years at a steady clip during the most recent running of the Asian Cup in 2023— namely Australia, Indonesia, Iraq, and Syria. Qatar has undergone the boldest transformation, going from 95% in the 2000 Asian Cup, to 73% in 2004, and then down to 65% or lower ever since. On the other end are countries that have never strayed from selecting players born inside their national limits such as China, Iran, Japan, South Korea, and Saudi Arabia.

<div class="figure" style="text-align: center">
<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-6-1.png" alt="CAF - Percent of roster slots used for home born players at each tournament. Only teams that have participated in a least 3 tournaments are plotted." width="912" />
<p class="caption"><span id="fig:unnamed-chunk-6"></span>Figure 4: CAF - Percent of roster slots used for home born players at each tournament. Only teams that have participated in a least 3 tournaments are plotted.</p>
</div>

As we saw with the aggregated Cup of Nations results earlier, the CAF features the most dramatic shift in home born usage out of all confederations. There were points in the early 2000s that all of Algeria, DR Congo, Morocco, and Senegal had squads that comprised of at least 90% home born talent, but that has completely changed. Now they all depend greatly on players born outside their borders, sometimes utilizing teams where a minority of the roster are home born. The Ivory Coast, Cameroon, Ghana, and Nigeria have also moved toward outside players albeit at a slower pace than the previous group. There are nations that have gone against the African grain: Egypt, South Africa, and Zambia are tournament regulars that continue to focus on squads based around home born players.

<div class="figure" style="text-align: center">
<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-7-1.png" alt="CONCACAF - Percent of roster slots used for home born players at each tournament. Only teams that have participated in a least 3 tournaments are plotted." width="912" />
<p class="caption"><span id="fig:unnamed-chunk-7"></span>Figure 5: CONCACAF - Percent of roster slots used for home born players at each tournament. Only teams that have participated in a least 3 tournaments are plotted.</p>
</div>

In CONCACAF, Costa Rica, Cuba, Honduras, and Panama have seen almost no movement away from their nearly 100% home born player squads. Haiti is the only country showing clear downward movement while the change down for Guatemala, Mexico, and Trinidad & Tobago is slighter. Others like Canada, Jamaica, and the United States bounce up and down in their use of non-home born players. Curacao is an outlier in the sense that it has never had a roster made up of more than half home born players in any of its 3 Gold Cup appearances.

<div class="figure" style="text-align: center">
<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-8-1.png" alt="CONMEBOL - Percent of roster slots used for home born players at each tournament. Only teams that have participated in a least 3 tournaments are plotted." width="912" />
<p class="caption"><span id="fig:unnamed-chunk-8"></span>Figure 6: CONMEBOL - Percent of roster slots used for home born players at each tournament. Only teams that have participated in a least 3 tournaments are plotted.</p>
</div>

Unlike the other confederations, none of the CONMEBOL nations show a pattern in the usage of home born players. This is expected as CONMEBOL came out on top as the home-heaviest confederation in a previous graph. In fact, Bolivia's 82% home player rate in the 1999 Copa America (18/22 players) is the lowest by a CONMEBOL nation in any tournament, a target many countries in the rest of the world would struggle to reach. Colombia has somehow not used a single outside born player since 1999 even though they had 17 tournaments to do so. Brazil nearly matched that feat but included Andreas Pereira, born to Brazilian parents in Belgium, in their 2024 Copa America squad.

<div class="figure" style="text-align: center">
<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-9-1.png" alt="UEFA - Percent of roster slots used for home born players at each tournament. Only teams that have participated in a least 3 tournaments are plotted." width="912" />
<p class="caption"><span id="fig:unnamed-chunk-9"></span>Figure 7: UEFA - Percent of roster slots used for home born players at each tournament. Only teams that have participated in a least 3 tournaments are plotted.</p>
</div>

UEFA is similar to CONMEBOL in that no nation is moving towards using fewer home born players. This is not too much of a shock—UEFA and CONMEBOL are home to the strongest footballing nations in the world along with the best footballing infrastructures. These countries do not need to go searching for prospects outside of their own borders. The only UEFA nations in the plot to rely on non-home born players are two countries located in the British Isles—the Republic of Ireland and Wales (both using English born players with family ties).

<div class="figure" style="text-align: center">
<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-10-1.png" alt="OFC - Percent of roster slots used for home born players at each tournament. Only teams that have participated in a least 3 tournaments are plotted." width="912" />
<p class="caption"><span id="fig:unnamed-chunk-10"></span>Figure 8: OFC - Percent of roster slots used for home born players at each tournament. Only teams that have participated in a least 3 tournaments are plotted.</p>
</div>

The OFC is graphed for completeness. Other than New Zealand, we will not read too much into the results since we're missing so much data for these rosters.

What we learn is that for the last 25 years, countries across the world are either decreasing their usage of home born footballers or holding steady. Almost no country is drifting in the other direction—using more home born players than they have historically—except maybe Equatorial Guinea, which we will go into more detail later.

## Overall Country

<div class="figure" style="text-align: center">
<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-11-1.png" alt="Overall home born percentages for each national team. Denominators are roster spots, not players. All teams are included regardless of the number of tournament entered." width="912" />
<p class="caption"><span id="fig:unnamed-chunk-11"></span>Figure 9: Overall home born percentages for each national team. Denominators are roster spots, not players. All teams are included regardless of the number of tournament entered.</p>
</div>

Stats for all tournaments are summarized into a single number for each country and plotted for comparison above. Note that unlike the line plots, all countries are shown regardless of the number of tournaments they competed in. Let's remind everyone that the denominator is roster spots, not players, so the statistic is % of all roster spots used for home born players. Results are slightly weighted toward recent tournaments because of the increase in squad sizes at tournaments since 2020, but this does not have that big of an effect in skewing the numbers.

We see that CONMEBOL is a unique confederation with all its nations building rosters around home born footballers—every CONMEBOL country spends over 90% of their roster spots on players born inside the country. OFC is similar if Samoa is ignored, but remember that there is a large chunk of OFC players with unknown birthplaces. Confirming earlier conclusions, CAF and CONCACAF are the two confederations that depend most on outside talent as each have multiple nations that use less than half their squad places on players born inside the country. The AFC and UEFA are somewhere in the middle of the extremes, each with only one country below the 50% home born mark—the Philippines and Albania, respectively.

## Country Details

We move on to examining the composition of rosters for some countries of interest, starting with the teams with the lowest home born percentages.

<table class="table" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption><span id="tab:unnamed-chunk-12"></span>Table 3: Countries where % home born is less than 50%.</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Confederation </th>
   <th style="text-align:left;"> Country </th>
   <th style="text-align:right;"> # Tournaments </th>
   <th style="text-align:right;"> # Players </th>
   <th style="text-align:right;"> # Home Born </th>
   <th style="text-align:right;"> % Home Born </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> COM </td>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 54 </td>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 5.6% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> AFC </td>
   <td style="text-align:left;"> PHI </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 17.4% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CONCACAF </td>
   <td style="text-align:left;"> GUY </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 26.1% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CONCACAF </td>
   <td style="text-align:left;"> CUW </td>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 70 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 27.1% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> EQG </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 127 </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 28.3% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CONCACAF </td>
   <td style="text-align:left;"> SUR </td>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 49 </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 34.7% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> UEFA </td>
   <td style="text-align:left;"> ALB </td>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 49 </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 38.8% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> ALG </td>
   <td style="text-align:right;"> 13 </td>
   <td style="text-align:right;"> 309 </td>
   <td style="text-align:right;"> 147 </td>
   <td style="text-align:right;"> 47.6% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> RWA </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 47.6% </td>
  </tr>
</tbody>
</table>

The table above shows the 9 countries since June 1998 with less than 50% of their rosters being made up of home born players. For some of the teams, we will go into detail about where these players were born.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-13-1.png" width="480" style="display: block; margin: auto;" />

The Comoros, a former French overseas territory, leads the international footballing world in the use of outside players. They've taken part in two CAF Cup of Nations (2021 and 2025) and have allotted only 3 of its 54 total squad slots to players born in the Comoros itself—just under 6%. Over 75% (42/54) of their squad were born in France, maybe not too surprising because of the Comoros's standing as a soccer nation compared to France. Neighboring Mayotte adds 13% (7/54) and Reunion, not that much farther away, adds another 4% (2/54). Both Mayotte and Reunion are departments of France with national teams of their own, but they are not eligible for the World Cup or Africa Cup of Nations as the players from French overseas departments also qualify for the mainland France national team. Of the 3 players that were born in the Comoros, 2 played for youth teams in France (Abdallah Ali Mohamed and Rafiki Saïd), leaving just one player (Ibroihim Djoudja) that was actually developed in the Comoros.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-14-1.png" width="480" style="display: block; margin: auto;" />

The Philippines have participated in one tournament—the 2019 Asian Cup—where they spent just 4 out of 23 positions on home born players (17%, more than double the standard set by the Comoros). They draw from a much wider and balanced range of countries than the Comoros with Germany (Patrick Reichelt, Stephan Schröck) being the biggest source. Other players with Filipino heritage from England (Phil Younghusband - most capped and highest goalscorer for the Philippines), Spain (Carli de Murga), Denmark (Kevin Ray Mendoza), Australia (Iain Ramsay), Austria (Stephan Palla), the UAE (Luke Woodland), and the United States (Miguel Tanton) make up the rest of their roster.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-15-1.png" width="480" style="display: block; margin: auto;" />

Curacao, while not an independent country, is similar to the Comoros in that it draws from countries it has political and geographical ties to—in this case, the Netherlands and Bonaire. Curacao is a part of the Netherlands, and mainland Netherlands born players generate 70% of it squad (including Leandro Bacuna - most capped). Neighboring Bonaire—which together with Curacao, Aruba, Saba, Sint Eustatius, and Sint Maarten once formed the Netherlands Antilles—provides a single player (Ayrton Statie) that took part in 2 editions of the Gold Cup. Unlike the Comoros, a lot more of Curacao's rosters spots (19 total or 27%) are used by Curacao born players.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-16-1.png" width="480" style="display: block; margin: auto;" />

Equatorial Guinea is a former Spanish colony and gets over 60% of its squad from its descendants in Spain (Emilio Nsue - leading goalscorer). Its national football team has drawn [criticism](https://www.espn.com/soccer/story/_/id/37391514/naturalisation-new-level) in the past for its use of naturalized players without cultural connections to the country—players from Cameroon (Viera Ellong), Brazil (Danilo Clementino), Ivory Coast (Fousseny Kamissoko), Liberia (Lawrence Doe), and Nigeria (Daniel Ekedo)—but this practice appears to have died down with rosters now made up of only Equatorial Guinea born players and Spain born players with Equatoguinean heritage. We already saw some evidence of this where Equatorial Guinea seemed like the only nation to have an increasing trend toward using home born players, specifically when comparing their 2012/2015 Cup of Nations to their 2021/2023/2025 Cup of Nations.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-17-1.png" width="480" style="display: block; margin: auto;" />

Albania is the only UEFA nation under 50% and pulls from players with Albanian heritage across Europe. Albania itself provides the majority of the roster, but Switzerland, one of the top destinations of Kosovar-Albanian emigration, and Kosovo are the other key contributors. As a side note, 15 out of Switzerland's 240 roster spots have been used by Kosovo born players who grew up in Switzerland—namely Albert Bunjaku (1 squad), Milaim Rama (1 squad), Valon Behrami (6 squads), and Xherdan Shaqiri (7 squads)—the most of any non-Swiss country.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-18-1.png" width="480" style="display: block; margin: auto;" />

While Algeria had a 91% home born squad for the 2000 Cup of Nations, that number has dropped down to less than 50% for 10 out of the 11 tournaments they've entered since 2004. About half their squad slots have been taken by players with Algerian roots born in France, including Algeria's two most capped players: Aïssa Mandi and Riyad Mahrez. This 40%/50% split between players born in Algeria/France has been pretty constant for Algerian squads since the 2004 Cup of Nations. The only tournament in this range where there were more Algerian born players (16) than French born players (11) was the 2021 Cup of Nations.

We won't go into a detailed breakdown of these countries, but over 50% of Guyana's squad was born in England (Guyana was formerly British Guiana) and over 50% of Suriname's squad was born in the Netherlands (Suriname was previously a constituent country of the Netherlands).

<table class="table" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption><span id="tab:unnamed-chunk-19"></span>Table 4: Specific squads sent to tournaments (not aggregated) where the percentage of home born players is less than 10%.</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Confederation </th>
   <th style="text-align:left;"> Tournament </th>
   <th style="text-align:right;"> Year </th>
   <th style="text-align:right;"> Country </th>
   <th style="text-align:right;"> # Players </th>
   <th style="text-align:right;"> # Home Born </th>
   <th style="text-align:right;"> % Home Born </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> Cup Of Nations </td>
   <td style="text-align:right;"> 2025 </td>
   <td style="text-align:right;"> COM </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 3.8% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CONCACAF </td>
   <td style="text-align:left;"> Gold Cup </td>
   <td style="text-align:right;"> 2025 </td>
   <td style="text-align:right;"> CUW </td>
   <td style="text-align:right;"> 24 </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 4.2% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> Cup Of Nations </td>
   <td style="text-align:right;"> 2021 </td>
   <td style="text-align:right;"> COM </td>
   <td style="text-align:right;"> 28 </td>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 7.1% </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> Cup Of Nations </td>
   <td style="text-align:right;"> 2012 </td>
   <td style="text-align:right;"> EQG </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 8.7% </td>
  </tr>
</tbody>
</table>

Instead of aggregating teams, has anyone ever entered a tournament without a single home born player? There are 4 cases where a national team sent a squad with over 90% "foreign" players: Equatorial Guinea in the 2012 Cup of Nations, the Comoros in both the 2021 and 2025 Cup of Nations, and Curacao in the 2025 Gold Cup. Comoros and Curacao were each just one player away from a perfect non-home born roster in 2025. With the Comoros, that home born player was Rafiki Saïd, already at a French youth team before reaching his teens. Similarly for Curacao, their sole home born player at that tournament was Tahith Chong—joined Dutch side Feyenoord at age 10 and represented the Netherlands at multiple youth levels.

## Birth Countries

Instead of keying in on a national team and then studying the various birth countries of its roster, we can look at the data from the opposite direction to answer the question: Which birth countries provide the most players to other nations?

<table class="table" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption><span id="tab:unnamed-chunk-20"></span>Table 5: Number of roster spots taken by players born in country. Countries that have taken more than 50 spots for other (non home) nations shown.</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Confederation </th>
   <th style="text-align:left;"> Birth Country </th>
   <th style="text-align:right;"> # of Spots for Birth Country </th>
   <th style="text-align:right;"> # of Spots for Other Countries </th>
   <th style="text-align:right;"> Total Countries </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> UEFA </td>
   <td style="text-align:left;"> FRA </td>
   <td style="text-align:right;"> 310 </td>
   <td style="text-align:right;"> 1079 </td>
   <td style="text-align:right;"> 42 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> UEFA </td>
   <td style="text-align:left;"> ENG </td>
   <td style="text-align:right;"> 297 </td>
   <td style="text-align:right;"> 341 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> UEFA </td>
   <td style="text-align:left;"> NED </td>
   <td style="text-align:right;"> 242 </td>
   <td style="text-align:right;"> 169 </td>
   <td style="text-align:right;"> 24 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> UEFA </td>
   <td style="text-align:left;"> GER </td>
   <td style="text-align:right;"> 355 </td>
   <td style="text-align:right;"> 168 </td>
   <td style="text-align:right;"> 36 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> UEFA </td>
   <td style="text-align:left;"> ESP </td>
   <td style="text-align:right;"> 356 </td>
   <td style="text-align:right;"> 135 </td>
   <td style="text-align:right;"> 22 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CONCACAF </td>
   <td style="text-align:left;"> USA </td>
   <td style="text-align:right;"> 525 </td>
   <td style="text-align:right;"> 111 </td>
   <td style="text-align:right;"> 27 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CONMEBOL </td>
   <td style="text-align:left;"> ARG </td>
   <td style="text-align:right;"> 392 </td>
   <td style="text-align:right;"> 105 </td>
   <td style="text-align:right;"> 18 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CONMEBOL </td>
   <td style="text-align:left;"> BRA </td>
   <td style="text-align:right;"> 546 </td>
   <td style="text-align:right;"> 95 </td>
   <td style="text-align:right;"> 24 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> CIV </td>
   <td style="text-align:right;"> 321 </td>
   <td style="text-align:right;"> 78 </td>
   <td style="text-align:right;"> 16 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> UEFA </td>
   <td style="text-align:left;"> SUI </td>
   <td style="text-align:right;"> 191 </td>
   <td style="text-align:right;"> 69 </td>
   <td style="text-align:right;"> 21 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> UEFA </td>
   <td style="text-align:left;"> POR </td>
   <td style="text-align:right;"> 267 </td>
   <td style="text-align:right;"> 56 </td>
   <td style="text-align:right;"> 9 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> UEFA </td>
   <td style="text-align:left;"> BIH </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 50 </td>
   <td style="text-align:right;"> 9 </td>
  </tr>
</tbody>
</table>

The above table shows all birth countries that have supplied more than 50 roster positions for other nations. A good number of these are some of the strongest footballing nations in the world—France, England, Germany, Spain, Argentina, and Brazil have won World Cups. These countries have ultra competitive national teams where securing a place on the squad is difficult, maybe pushing candidates with ties to other nations to seek alternative routes into big tournaments. We take a closer look at some of these countries.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-21-1.png" width="480" style="display: block; margin: auto;" />

The most extreme case is France. Since the 1998 World Cup, 310 spots on the French national team have been used for French born players. Compare that to the 1,079 spots allotted to French born players for other national teams. Yes, that's 3.5 times more French born footballers on roster sheets outside of mainland France than for France itself. There are 42 countries that have benefited from this (including France itself), with more than 60% going to the CAF—Pierre-Emerick Aubameyang (Gabon), Kalidou Koulibaly (Senegal), and Sofiane Feghouli (Algeria) are examples. Most of these are independent African states with a history of French colonization. There are 3 French overseas departments with their own national teams that have qualified for the CONCACAF Gold Cup—Guadeloupe, Martinique, and French Guiana. France has also provided players to every confederation. In addition to CAF, UEFA, and CONCACAF, each of AFC, CONMEBOL, and OFC have 6 slots taken by French born players.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-22-1.png" width="480" style="display: block; margin: auto;" />

England does not provide the volume of players for other countries like France—no country even comes close—but is not that far behind in terms of number of countries represented with 40. Over half of tournament roster spots taken up by English born players are for national teams not named England, and like France, it has also touched every confederation. In UEFA, the other countries of the British Isles—the Republic of Ireland (Kevin Kilbane), Northern Ireland (Oliver Norwood), Scotland (Scott McTominay), and Wales (Ashley Williams)—receive the most players. In CONCACAF, we see countries that gained independence from the United Kingdom—Jamaica (Wes Morgan), Grenada (Aaron Pierre), Trinidad and Tobago (Shaka Hislop), etc. It's a similar story for CAF with Nigeria (Ademola Lookman), Ghana (Antoine Semenyo), and Zimbabwe (Jordan Zemura).

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-23-1.png" width="480" style="display: block; margin: auto;" />

Coming in third is the Netherlands, supplying 169 roster spots for countries outside of mainland Netherlands. Curacao (Eloy Room and many other of their most capped players) and Suriname (Shaquille Pinas) are countries with Dutch links. Moroccans (Hakim Ziyech) form one of the largest minority groups in the Netherlands. Cape Verde (Garry Rodrigues) is an unexpected entry here given its relatively small diaspora in the Netherlands.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-24-1.png" width="480" style="display: block; margin: auto;" />

While the bulk of German born players in international tournaments represent Germany, 168 spots have been for other countries. Turkey, Croatia, and the USA are the main benefactors. There are large numbers of Germans of either Turkish (Hakan Çalhanoğlu) or Croatian (Niko Kovač) descent and many have gone on the represent those two countries in football. The German born American players are mostly children of U.S. servicemen based in Germany (Jermaine Jones, John Brooks).

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-25-1.png" width="480" style="display: block; margin: auto;" />

We covered Equatorial Guinea before, learning that they're adept at utilizing foreign born players with or without Equatoguinean ties. If you see a Spanish born player in a tournament, there's a 15% chance that they could be representing Equatorial Guinea—a number that could have been higher had Equatorial Guinea qualified for more Cup of Nations. The second largest group plays for Morocco (Achraf Hakimi)—this is in line with Moroccans being the largest minority group in Spain.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-26-1.png" width="480" style="display: block; margin: auto;" />

The United States is a source of players for a variety of CONCACAF teams, with El Salvador (Gerson Mayen), Haiti (Derrick Etienne Jr.), and Guatemala (Darwin Lom) standing out. While there are large diasporas from many countries across the world located in the U.S., there are unlikely to be footballers who declare for prominent UEFA and CONMEBOL nations. The U.S. is not a soccer powerhouse and the countries that are have enough talent of their own without having to go scouting for players in the U.S.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-27-1.png" width="480" style="display: block; margin: auto;" /><img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-27-2.png" width="480" style="display: block; margin: auto;" />

A fun comparison is between Argentina and Brazil, rival South American countries that are among the world's most successful national teams. They have taken up 105 and 95 roster spots for the rest of the world, respectively (but definitely never playing for each other). The largest chunk of footballers born in Argentina but not playing for Argentina play for other CONMEBOL members, albeit for different reasons. Paraguay and Chile are examples of countries with Argentinian players with Argentinian heritage (Roberto Acuña for Paraguay and Matías Fernández for Chile) while Ecuador includes naturalized players born in Argentina (Hernán Galíndez). On the other hand, since the 1998 World Cup there are no examples of Brazilian born players representing another CONMEBOL nation. When Brazilians do play for another country, they are more likely to be naturalized citizens instead of having familial links to the other country (Pepe for Portugal, Cacau for Germany, or José Clayton for Tunisia) .

Note that these numbers are heavily skewed by the nations that show up in the data set. For example, one of the biggest reasons France has such a huge gap over other countries is that the big nations they provide players for—Algeria, Senegal, Cameroon, etc.—are also strong at soccer and thus qualify for tournaments year after year, pushing the French numbers up. This is actually more evidence for the prowess of French soccer—these other countries are preforming amazingly well using teams full of French born players.

## Other Findings of Note

* National teams only using home born players

<table class="table" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption><span id="tab:unnamed-chunk-28"></span>Table 6: National teams that have only used home born players.</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Confederation </th>
   <th style="text-align:left;"> Country </th>
   <th style="text-align:right;"> # of Tournaments </th>
   <th style="text-align:right;"> # of Players </th>
   <th style="text-align:right;"> # Home Born </th>
   <th style="text-align:right;"> # Unknown Birthplace </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> CONMEBOL </td>
   <td style="text-align:left;"> COL </td>
   <td style="text-align:right;"> 17 </td>
   <td style="text-align:right;"> 388 </td>
   <td style="text-align:right;"> 388 </td>
   <td style="text-align:right;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> AFC </td>
   <td style="text-align:left;"> KSA </td>
   <td style="text-align:right;"> 14 </td>
   <td style="text-align:right;"> 322 </td>
   <td style="text-align:right;"> 322 </td>
   <td style="text-align:right;"> 3 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CONCACAF </td>
   <td style="text-align:left;"> CUB </td>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 179 </td>
   <td style="text-align:right;"> 179 </td>
   <td style="text-align:right;"> 7 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> AFC </td>
   <td style="text-align:left;"> KUW </td>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 86 </td>
   <td style="text-align:right;"> 86 </td>
   <td style="text-align:right;"> 4 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> NAM </td>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 68 </td>
   <td style="text-align:right;"> 68 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> AFC </td>
   <td style="text-align:left;"> TKM </td>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 43 </td>
   <td style="text-align:right;"> 43 </td>
   <td style="text-align:right;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> BOT </td>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 47 </td>
   <td style="text-align:right;"> 47 </td>
   <td style="text-align:right;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> MWI </td>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 51 </td>
   <td style="text-align:right;"> 51 </td>
   <td style="text-align:right;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> AFC </td>
   <td style="text-align:left;"> YEM </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> LBR </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CONCACAF </td>
   <td style="text-align:left;"> BER </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 0 </td>
  </tr>
</tbody>
</table>

There are 11 national teams that have built rosters made up of only players born in their own country. The most impressive of these is Colombia, which achieved this after having competed in 17 tournaments with 388 possible roster spots. It is the only Spanish-speaking CONMEBOL nation not to have featured an Argentine born player on any of their squads. Conversely, no Colombia born player has played for any other CONMEBOL nation. Saudi Arabia is not that far behind with 14 tournaments and 322 roster spots, and Cuba is a little farther back with 9 tournaments and 179 roster spots (do note that Saudi Arabia and Cuba are missing birthplaces for 3 and 7 entries, respectively). The rest of the countries on this list have participated in fewer tournaments.

* National teams featuring the widest range of birth countries

<table class="table" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption><span id="tab:unnamed-chunk-29"></span>Table 7: National teams that have featured players born in at least 10 different countries.</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Confederation </th>
   <th style="text-align:left;"> Country </th>
   <th style="text-align:right;"> # of Countries </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> CONCACAF </td>
   <td style="text-align:left;"> CAN </td>
   <td style="text-align:right;"> 25 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CONCACAF </td>
   <td style="text-align:left;"> USA </td>
   <td style="text-align:right;"> 21 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> AFC </td>
   <td style="text-align:left;"> LIB </td>
   <td style="text-align:right;"> 19 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> AFC </td>
   <td style="text-align:left;"> QAT </td>
   <td style="text-align:right;"> 18 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> AFC </td>
   <td style="text-align:left;"> AUS </td>
   <td style="text-align:right;"> 16 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> UEFA </td>
   <td style="text-align:left;"> FRA </td>
   <td style="text-align:right;"> 14 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> UEFA </td>
   <td style="text-align:left;"> POR </td>
   <td style="text-align:right;"> 14 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> UEFA </td>
   <td style="text-align:left;"> SUI </td>
   <td style="text-align:right;"> 12 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> GHA </td>
   <td style="text-align:right;"> 11 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> TUN </td>
   <td style="text-align:right;"> 11 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> OFC </td>
   <td style="text-align:left;"> NZL </td>
   <td style="text-align:right;"> 11 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> UEFA </td>
   <td style="text-align:left;"> GER </td>
   <td style="text-align:right;"> 11 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> GUI </td>
   <td style="text-align:right;"> 10 </td>
  </tr>
</tbody>
</table>

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-30-1.png" width="480" style="display: block; margin: auto;" />

Canada is the most international team, with players born in 25 different countries across 3 federations donning the Canadian national shirt. There is no one country that stands out as a contributor (outside of Canada itself) although a mix of UEFA nations comprise the biggest bucket. Canada is also represented by Majrekar James of Dominica and Carl Fletcher of Montserrat, two nations that have never qualified for a major national tournament but were able to spawn players for this national side.

* National teams featuring the widest range of birth continents

<table class="table" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption><span id="tab:unnamed-chunk-31"></span>Table 8: National teams that have featured players born in at least 5 different confederations.</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Confederation </th>
   <th style="text-align:left;"> Country </th>
   <th style="text-align:right;"> # of Countries </th>
   <th style="text-align:right;"> # of Confederations </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> AFC </td>
   <td style="text-align:left;"> AUS </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 5 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> AFC </td>
   <td style="text-align:left;"> LIB </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 5 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> AFC </td>
   <td style="text-align:left;"> PLE </td>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 5 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CONCACAF </td>
   <td style="text-align:left;"> USA </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 5 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> OFC </td>
   <td style="text-align:left;"> NZL </td>
   <td style="text-align:right;"> 11 </td>
   <td style="text-align:right;"> 5 </td>
  </tr>
</tbody>
</table>

There is no national team that has been represented by players born in all 6 confederations; the closest are the 5 countries topping out at 5 confederations. Australia is missing a player from CONCACAF, Liberia and Palestine are missing players from OFC, New Zealand is missing a player from CONMEBOL, and the United States is missing a player from CAF.

* Countries that have birthed players for every confederation

<table class="table" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption><span id="tab:unnamed-chunk-32"></span>Table 9: Countries that have provided players for all 6 confederations.</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Confederation </th>
   <th style="text-align:left;"> Country </th>
   <th style="text-align:right;"> # of Countries </th>
   <th style="text-align:right;"> # of Confederations </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> CAF </td>
   <td style="text-align:left;"> RSA </td>
   <td style="text-align:right;"> 7 </td>
   <td style="text-align:right;"> 6 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> CONCACAF </td>
   <td style="text-align:left;"> USA </td>
   <td style="text-align:right;"> 27 </td>
   <td style="text-align:right;"> 6 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> UEFA </td>
   <td style="text-align:left;"> ENG </td>
   <td style="text-align:right;"> 40 </td>
   <td style="text-align:right;"> 6 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> UEFA </td>
   <td style="text-align:left;"> FRA </td>
   <td style="text-align:right;"> 42 </td>
   <td style="text-align:right;"> 6 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> UEFA </td>
   <td style="text-align:left;"> GER </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> 6 </td>
  </tr>
</tbody>
</table>

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-33-1.png" width="480" style="display: block; margin: auto;" />

Players born France, England, Germany, the United States, and South Africa have gone on to represent every confederation. South Africa is the most interesting case because of its efficiency in completing this feat with just 13 roster spots for other national teams. You'd expect this for France, England, Germany, and the United States—they've each taken up over 100 roster spots for other countries, so every confederation could have been covered just by luck. South Africa provided each of Australia (OFC - Keanu Baccus), Portugal (UEFA - Dimas Teixeira), USA/Canada (CONCACAF - Roy Wegerle/Kevin Harmse), and Chile (CONMEBOL - Mark Gonzalez) with a single player; New Zealand is the relative outlier, getting 3 unique players from South Africa (Deklan Wynne, Storm Roux, Daniel Ellensohn).

## Limitations

This analysis only uses birthplace, which as mentioned may not be accurate as there's a scarcity of biographical references for many of the lesser known players. A more complete study should also consider where players were raised. Players could be born in one country but spend their childhood in another, having the ability to choose from multiple national teams to represent. Yassine Bounou was born in Canada to Moroccan parents, but moved to Morocco at the age of 3 and grew up there. He represents the Moroccan team and counts as a non-home player in this analysis. Folarin Balogun was born in the United States to Nigerian parents, moved to the United Kingdom when he was a month old, eventually growing up in England. He later chose to play for the U.S. team, counting as a home player in the data. A better analysis should take into account all these intricacies, but this seems an impossible task. Given the difficulty of finding birthplaces for many players, getting entire histories of their childhoods is nigh impossible when we have a dataset of tens of thousands of players.
