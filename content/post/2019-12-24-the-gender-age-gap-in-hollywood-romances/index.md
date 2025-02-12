---
title: The Gender Age Gap in Hollywood Romances
author: Robert Huang
date: '2019-12-24'
slug: the-gender-age-gap-in-hollywood-romances
categories: []
tags:
  - film
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





Humphrey Bogart and Audrey Hepburn in *Sabrina* (1954),  Cary Grant and Grace Kelly in *To Catch a Thief* (1955), and more recently, Daniel Day Lewis and Vicky Krieps in *Phantom Thread* (2017). What is immediately noticeable when watching those films (at least for this viewer) is the huge age difference between the male leads and their on-screen romantic partners. Humphrey Bogart is nearly 30 years older than Audrey Hepburn. Cary Grant and Daniel Day Lewis are each about 25 years older than Grace Kelly and Vicky Krieps, respectively. It is unlikely that audiences are fazed watching romances matching men with younger women because of the age gap in real life marriages, but the examples presented are out of the norm and feature immense chasms. A question we can look into further is whether the age differences that Hollywood romances present to us are more extreme than what we see in reality. Has this age gap changed throughout time, and does it mirror the differences in actual relationships?

To answer those questions, we create a dataset of movies with the ages of the lead actors and actresses that are paired romantically. Using IMDb, American full-length features from 1930 to 2018 that list romance as one of its genres were sampled. Only the 25 most popular films from each year—the titles that received the most user votes for IMDb rating—were included. A lull in the Hollywood film industry from the 1960s to early 1980s led to fewer than 25 films fulfilling the above criteria in some years. This was especially apparent in 1975, with a low of eight qualifying titles. Despite this, our final dataset is made up of a robust 2,056 movies. The most popular films were used because we wanted to capture movies that were a part of mainstream culture and that a large number of people actually watched. This resulted in films that generally had wide theatrical releases across America, although there has been a shift toward streaming content in more recent years, with a number of Netflix releases in 2017 and 2018. One limitation of using the number of user votes as a measure of popularity is that this only applies to the films' statures today among IMDb users, not necessarily how they were considered at the time of their release.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-2-1.png" width="576" style="display: block; margin: auto;" />

For each film, we calculate the ages of the two actors involved in the main romance using the year of the film's release. The most difficult and time consuming stage of building the dataset was figuring out the romantic relationships. I have not seen all the movies included in the dataset, so this involved reading many plot summaries to deduce the two top billed actors that are paired. Something to keep in mind is that just because the film is categorized as a romance does not mean that the romance(s) featured in the film is a substantial part of the plot. Films that have romances but that are not tagged with the romance genre on IMDb are not included. An example is 1944's *Double Indemnity*, where the romantic relationship between Fred MacMurray and Barbara Stanwyck is a major part of the plot, but the film itself is not categorized as a romance.

For a baseline to compare to, we need to know the age gap between real-life couples in relationships throughout the last 70 years. The paper ["The May-December relationship since 1850: Age homogamy in the U.S."](https://paa2008.princeton.edu/papers/80695) by Karen Rolf and Joseph P. Ferrie has summarized data on the age differences between husbands and wives using Census results since 1850. While the study is only limited to marriages, it should provide a good enough estimate for our analysis. The results from the paper are not surprising, with husbands on average being older than wives in every Census. This difference gets smaller with each Census, with a gap of 4.7 years in 1900 shrinking to a gap of only 2.3 years in 2000.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-3-1.png" width="576" style="display: block; margin: auto;" />



How does Hollywood compare to real life? We start with an overview of all films from 1930 to 2018. The mean age of the lead actors in our 2,056 film sample is 36.8 with a standard deviation of 9.7 years. For actresses, this is 30.7 and 8, respectively. Male romantic leads are generally older than female leads, regardless of whether they are paired as couples, and also show more variation in age. The histograms of actor and actress ages also suggest that there is ageism in Hollywood, especially for female actors. There are fewer lead roles for actresses going into their 40s compared to the amount for male actors of the same age. Films starring actors in their 40s still make up a sizable portion of our dataset, with men not hitting their Hollywood shelf life until their 50s. Romantic roles for men range in age from the mid-20s to mid-40s while most roles for women are bunched up into the smaller range between the mid-20s and mid-30s.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-5-1.png" width="576" style="display: block; margin: auto;" />

The mean age difference between male and female pairings in romances is 6.2 years with a standard deviation of 8.9. The age differences range from -54 (actress is 54 years older than the actor) to 42 (actor is 42 years older than the actress), with the largest proportion of movies featuring men paired with younger women. This result can be seen in both the histogram of age differences above and the following scatter plot.


```
## `geom_smooth()` using formula = 'y ~ x'
```

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-6-1.png" width="576" style="display: block; margin: auto;" />

Actor-actress pairings for all 2,056 films are plotted against one another. Points above the black line are films where the actress is older than the actor in the romance; points below the line are films where the actor is older. Men are older than their love interests in 75% of films while women are older than their love interests in only 21% of films. About 4% feature romances between leads born in the same year. Note that age calculations only use birth years. Because of that, age differences are not exact, but they should all be within one year of their true values.

The blue line in the plot models the relationship between the ages of romantic leads. Men start off with similar aged love interests, but the age gap between the leads grow as male movie stars start to age. Actors in their 20s are generally paired with actresses that are similar in age. As men enter their 30s, they are more likely to be paired with actresses younger than they are. Even as actors enter their mid-30s and 40s, they continue to have female love interests that are still in their early 30s. Given that an actor is 50-years-old, his love interest has an average age of 35. In fact, there are few cases where an actor 50 or older is paired with an actress older than he is. By that time, the men are generally 18.2 years older than their co-stars.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-7-1.png" width="576" style="display: block; margin: auto;" />


```
## `summarise()` has grouped output by 'year.rd'. You can override using the
## `.groups` argument.
```

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-8-1.png" width="576" style="display: block; margin: auto;" />

We now consider year as a variable to see if age in film has changed over time. For each decade, the mean age differences between actors are plotted in black along with their 95% confidence intervals. These values are benchmarked against the Census results of age differences between married couples. The age differences between couples we see on screen are always higher than what we see in real life, no matter the era. While the age gap between married couples has declined in every Census since 1930, the Hollywood age gap shows much more variation. The 1950s has the greatest age disparity, with men on average being 10 years older than their screen partners. As seen in the plot of average actor age, this number was driven by actors being much older in the 1950s compared to other periods. The average lead romantic role for men in that era was 41-years-old; they were under 40 in every other decade. The dip in age difference in the 1970s was the result of a spike in average lead actress age to 33, higher than in any other decade. The caveat with results from the 70s is that there were a way smaller sample of films—romances or otherwise—from that period because that era saw the end of the studio system and the rise of New Hollywood. Unlike the 1930s to 1950s when mainstream romances made up a large part of studio releases, the 1970s featured more independent works, including a number of foreign and exploitation films.

<table class="table table-striped table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption><span id="tab:unnamed-chunk-9"></span>Table 1: (\#tab:unnamed-chunk-9)Films with the largest age gaps between couples - older actor</caption>
 <thead>
  <tr>
   <th style="text-align:right;"> Year </th>
   <th style="text-align:left;"> Title </th>
   <th style="text-align:left;"> Actress </th>
   <th style="text-align:right;"> Actress Age </th>
   <th style="text-align:left;"> Actor </th>
   <th style="text-align:right;"> Actor Age </th>
   <th style="text-align:right;"> Age Difference </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 1952 </td>
   <td style="text-align:left;"> Limelight </td>
   <td style="text-align:left;"> Claire Bloom </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:left;"> Charles Chaplin </td>
   <td style="text-align:right;"> 63 </td>
   <td style="text-align:right;"> 42 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1989 </td>
   <td style="text-align:left;"> Ghosts Can't Do It </td>
   <td style="text-align:left;"> Bo Derek </td>
   <td style="text-align:right;"> 33 </td>
   <td style="text-align:left;"> Anthony Quinn </td>
   <td style="text-align:right;"> 74 </td>
   <td style="text-align:right;"> 41 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2009 </td>
   <td style="text-align:left;"> Whatever Works </td>
   <td style="text-align:left;"> Evan Rachel Wood </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:left;"> Larry David </td>
   <td style="text-align:right;"> 62 </td>
   <td style="text-align:right;"> 40 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1999 </td>
   <td style="text-align:left;"> Entrapment </td>
   <td style="text-align:left;"> Catherine Zeta-Jones </td>
   <td style="text-align:right;"> 30 </td>
   <td style="text-align:left;"> Sean Connery </td>
   <td style="text-align:right;"> 69 </td>
   <td style="text-align:right;"> 39 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1948 </td>
   <td style="text-align:left;"> Mr. Peabody and the Mermaid </td>
   <td style="text-align:left;"> Ann Blyth </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:left;"> William Powell </td>
   <td style="text-align:right;"> 56 </td>
   <td style="text-align:right;"> 36 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2017 </td>
   <td style="text-align:left;"> The Hero </td>
   <td style="text-align:left;"> Laura Prepon </td>
   <td style="text-align:right;"> 37 </td>
   <td style="text-align:left;"> Sam Elliott </td>
   <td style="text-align:right;"> 73 </td>
   <td style="text-align:right;"> 36 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1973 </td>
   <td style="text-align:left;"> Breezy </td>
   <td style="text-align:left;"> Kay Lenz </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:left;"> William Holden </td>
   <td style="text-align:right;"> 55 </td>
   <td style="text-align:right;"> 35 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1945 </td>
   <td style="text-align:left;"> The Great Flamarion </td>
   <td style="text-align:left;"> Mary Beth Hughes </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:left;"> Erich von Stroheim </td>
   <td style="text-align:right;"> 60 </td>
   <td style="text-align:right;"> 34 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2005 </td>
   <td style="text-align:left;"> Shopgirl </td>
   <td style="text-align:left;"> Claire Danes </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:left;"> Steve Martin </td>
   <td style="text-align:right;"> 60 </td>
   <td style="text-align:right;"> 34 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1955 </td>
   <td style="text-align:left;"> Daddy Long Legs </td>
   <td style="text-align:left;"> Leslie Caron </td>
   <td style="text-align:right;"> 24 </td>
   <td style="text-align:left;"> Fred Astaire </td>
   <td style="text-align:right;"> 56 </td>
   <td style="text-align:right;"> 32 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1959 </td>
   <td style="text-align:left;"> Operation Petticoat </td>
   <td style="text-align:left;"> Joan O'Brien </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:left;"> Cary Grant </td>
   <td style="text-align:right;"> 55 </td>
   <td style="text-align:right;"> 32 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1984 </td>
   <td style="text-align:left;"> Blame It on Rio </td>
   <td style="text-align:left;"> Michelle Johnson </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:left;"> Michael Caine </td>
   <td style="text-align:right;"> 51 </td>
   <td style="text-align:right;"> 32 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1995 </td>
   <td style="text-align:left;"> Mighty Aphrodite </td>
   <td style="text-align:left;"> Mira Sorvino </td>
   <td style="text-align:right;"> 28 </td>
   <td style="text-align:left;"> Woody Allen </td>
   <td style="text-align:right;"> 60 </td>
   <td style="text-align:right;"> 32 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1996 </td>
   <td style="text-align:left;"> Everyone Says I Love You </td>
   <td style="text-align:left;"> Julia Roberts </td>
   <td style="text-align:right;"> 29 </td>
   <td style="text-align:left;"> Woody Allen </td>
   <td style="text-align:right;"> 61 </td>
   <td style="text-align:right;"> 32 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1996 </td>
   <td style="text-align:left;"> Surviving Picasso </td>
   <td style="text-align:left;"> Natascha McElhone </td>
   <td style="text-align:right;"> 27 </td>
   <td style="text-align:left;"> Anthony Hopkins </td>
   <td style="text-align:right;"> 59 </td>
   <td style="text-align:right;"> 32 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1967 </td>
   <td style="text-align:left;"> Doctor Dolittle </td>
   <td style="text-align:left;"> Samantha Eggar </td>
   <td style="text-align:right;"> 28 </td>
   <td style="text-align:left;"> Rex Harrison </td>
   <td style="text-align:right;"> 59 </td>
   <td style="text-align:right;"> 31 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2002 </td>
   <td style="text-align:left;"> Hollywood Ending </td>
   <td style="text-align:left;"> Téa Leoni </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:left;"> Woody Allen </td>
   <td style="text-align:right;"> 67 </td>
   <td style="text-align:right;"> 31 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1954 </td>
   <td style="text-align:left;"> Sabrina </td>
   <td style="text-align:left;"> Audrey Hepburn </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:left;"> Humphrey Bogart </td>
   <td style="text-align:right;"> 55 </td>
   <td style="text-align:right;"> 30 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1957 </td>
   <td style="text-align:left;"> Funny Face </td>
   <td style="text-align:left;"> Audrey Hepburn </td>
   <td style="text-align:right;"> 28 </td>
   <td style="text-align:left;"> Fred Astaire </td>
   <td style="text-align:right;"> 58 </td>
   <td style="text-align:right;"> 30 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1957 </td>
   <td style="text-align:left;"> The Pride and the Passion </td>
   <td style="text-align:left;"> Sophia Loren </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:left;"> Cary Grant </td>
   <td style="text-align:right;"> 53 </td>
   <td style="text-align:right;"> 30 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1958 </td>
   <td style="text-align:left;"> Houseboat </td>
   <td style="text-align:left;"> Sophia Loren </td>
   <td style="text-align:right;"> 24 </td>
   <td style="text-align:left;"> Cary Grant </td>
   <td style="text-align:right;"> 54 </td>
   <td style="text-align:right;"> 30 </td>
  </tr>
</tbody>
</table>

Next, we take a closer look at the films that host the most extreme age differences. The table above shows all movies that feature romances between men that are at least 30 years older than their love interests. There were 21 films that fulfilled this criteria, with examples from nearly every decade. *Limelight* (1952) features a relationship between 63-year-old Charles Chaplin and 21-year-old Claire Bloom, an age difference of 42 years. This was a common occurence for Chaplin, both on and off screen. Chaplin's two other films in the dataset, *City Lights* (1931) and *Modern Times* (1936), give him love interests that are 19 and 21 years younger than him, respectively. Golden Raspberry Award winner for Worst Picture *Ghosts Can't Do It* (1989) pairs 74-year-old Anthony Quinn with 33-year-old Bo Derek, 41 years his junior. The film was written and directed by Derek's husband, John Derek, who was 30 years older than her. Both Cary Grant and Woody Allen appear on the list three times, appearing in multiple films while paired with younger love interests. Cary Grant had a career that spanned four decades, with the films in the table all from the latter part of it in the late fifties. Woody Allen wrote and directed all the films he starred in, always pairing himself with younger women. *Whatever Works* (2009), the third film on the list, did not star Allen, but was written and directed by him. Audrey Hepburn and Sophia Loren both appear twice for being paired with older actors. Loren was actually paired with Cary Grant in two different movies, one year after the other. Two of the more famous examples of romances between a much older man and a younger woman both feature Audrey Hepburn. *Sabrina* (1954) and *Funny Face* (1957) gave Hepburn co-stars that were 30 years older than her. *Sabrina* actually features a love triangle for Hepburn, where the other man—William Holden—is still 11 years older than her.

<table class="table table-striped table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption><span id="tab:unnamed-chunk-10"></span>Table 3: (\#tab:unnamed-chunk-10)Films with the largest age gaps between couples - older actress</caption>
 <thead>
  <tr>
   <th style="text-align:right;"> Year </th>
   <th style="text-align:left;"> Title </th>
   <th style="text-align:left;"> Actress </th>
   <th style="text-align:right;"> Actress Age </th>
   <th style="text-align:left;"> Actor </th>
   <th style="text-align:right;"> Actor Age </th>
   <th style="text-align:right;"> Age Difference </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 1977 </td>
   <td style="text-align:left;"> Sextette </td>
   <td style="text-align:left;"> Mae West </td>
   <td style="text-align:right;"> 85 </td>
   <td style="text-align:left;"> Timothy Dalton </td>
   <td style="text-align:right;"> 31 </td>
   <td style="text-align:right;"> -54 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1971 </td>
   <td style="text-align:left;"> Harold and Maude </td>
   <td style="text-align:left;"> Ruth Gordon </td>
   <td style="text-align:right;"> 75 </td>
   <td style="text-align:left;"> Bud Cort </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> -52 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2015 </td>
   <td style="text-align:left;"> Hello, My Name Is Doris </td>
   <td style="text-align:left;"> Sally Field </td>
   <td style="text-align:right;"> 69 </td>
   <td style="text-align:left;"> Max Greenfield </td>
   <td style="text-align:right;"> 35 </td>
   <td style="text-align:right;"> -34 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1961 </td>
   <td style="text-align:left;"> The Roman Spring of Mrs. Stone </td>
   <td style="text-align:left;"> Vivien Leigh </td>
   <td style="text-align:right;"> 48 </td>
   <td style="text-align:left;"> Warren Beatty </td>
   <td style="text-align:right;"> 24 </td>
   <td style="text-align:right;"> -24 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1972 </td>
   <td style="text-align:left;"> Heat </td>
   <td style="text-align:left;"> Sylvia Miles </td>
   <td style="text-align:right;"> 48 </td>
   <td style="text-align:left;"> Joe Dallesandro </td>
   <td style="text-align:right;"> 24 </td>
   <td style="text-align:right;"> -24 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1993 </td>
   <td style="text-align:left;"> Arizona Dream </td>
   <td style="text-align:left;"> Faye Dunaway </td>
   <td style="text-align:right;"> 52 </td>
   <td style="text-align:left;"> Johnny Depp </td>
   <td style="text-align:right;"> 30 </td>
   <td style="text-align:right;"> -22 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1979 </td>
   <td style="text-align:left;"> An Almost Perfect Affair </td>
   <td style="text-align:left;"> Monica Vitti </td>
   <td style="text-align:right;"> 48 </td>
   <td style="text-align:left;"> Keith Carradine </td>
   <td style="text-align:right;"> 30 </td>
   <td style="text-align:right;"> -18 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1983 </td>
   <td style="text-align:left;"> Class </td>
   <td style="text-align:left;"> Jacqueline Bisset </td>
   <td style="text-align:right;"> 39 </td>
   <td style="text-align:left;"> Andrew McCarthy </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> -18 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1987 </td>
   <td style="text-align:left;"> Moonstruck </td>
   <td style="text-align:left;"> Cher </td>
   <td style="text-align:right;"> 41 </td>
   <td style="text-align:left;"> Nicolas Cage </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> -18 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1977 </td>
   <td style="text-align:left;"> The Turning Point </td>
   <td style="text-align:left;"> Anne Bancroft </td>
   <td style="text-align:right;"> 46 </td>
   <td style="text-align:left;"> Mikhail Baryshnikov </td>
   <td style="text-align:right;"> 29 </td>
   <td style="text-align:right;"> -17 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1945 </td>
   <td style="text-align:left;"> A Royal Scandal </td>
   <td style="text-align:left;"> Tallulah Bankhead </td>
   <td style="text-align:right;"> 43 </td>
   <td style="text-align:left;"> William Eythe </td>
   <td style="text-align:right;"> 27 </td>
   <td style="text-align:right;"> -16 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1960 </td>
   <td style="text-align:left;"> The Fugitive Kind </td>
   <td style="text-align:left;"> Anna Magnani </td>
   <td style="text-align:right;"> 52 </td>
   <td style="text-align:left;"> Marlon Brando </td>
   <td style="text-align:right;"> 36 </td>
   <td style="text-align:right;"> -16 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1990 </td>
   <td style="text-align:left;"> Tune in Tomorrow... </td>
   <td style="text-align:left;"> Barbara Hershey </td>
   <td style="text-align:right;"> 42 </td>
   <td style="text-align:left;"> Keanu Reeves </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> -16 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1952 </td>
   <td style="text-align:left;"> Come Back, Little Sheba </td>
   <td style="text-align:left;"> Shirley Booth </td>
   <td style="text-align:right;"> 54 </td>
   <td style="text-align:left;"> Burt Lancaster </td>
   <td style="text-align:right;"> 39 </td>
   <td style="text-align:right;"> -15 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1978 </td>
   <td style="text-align:left;"> Moment by Moment </td>
   <td style="text-align:left;"> Lily Tomlin </td>
   <td style="text-align:right;"> 39 </td>
   <td style="text-align:left;"> John Travolta </td>
   <td style="text-align:right;"> 24 </td>
   <td style="text-align:right;"> -15 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 1983 </td>
   <td style="text-align:left;"> A Night in Heaven </td>
   <td style="text-align:left;"> Lesley Ann Warren </td>
   <td style="text-align:right;"> 37 </td>
   <td style="text-align:left;"> Christopher Atkins </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> -15 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2017 </td>
   <td style="text-align:left;"> Home Again </td>
   <td style="text-align:left;"> Reese Witherspoon </td>
   <td style="text-align:right;"> 41 </td>
   <td style="text-align:left;"> Pico Alexander </td>
   <td style="text-align:right;"> 26 </td>
   <td style="text-align:right;"> -15 </td>
  </tr>
</tbody>
</table>

The second table shows all films where women have romances with men at least 15 years younger than they are. While the less strict threshold still results in a shorter list than the previous one for older men, it is topped by the two films with the largest age differences in the entire dataset. *Sextette* (1977) has 85-year-old Mae West married to 31-year-old Timothy Dalton, although this relationship seems to be played as a joke (I have not seen the movie). Not far behind is 1971's *Harold and Maude*, where the leads are separated by 52 years and that age difference drives the story. Other than these two outliers, the rest of the films in the table show age differences that are smaller than the corresponding group of films for men. One noticeable difference between the two tables is that the older actress list includes only two films from before 1960; the older actor list is made up of a much larger proportion of pre-1960s movies.


```
## `summarise()` has grouped output by 'actor.id'. You can override using the
## `.groups` argument.
## `summarise()` has grouped output by 'actress.id'. You can override using the
## `.groups` argument.
```

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-11-1.png" width="672" style="display: block; margin: auto;" />

Given that there are actors and actresses in the sample that are represented by multiple films, we are able to look into whether some stars are always matched with older or younger love interests. All actors with at least 10 films in our dataset are plotted along with 95% confidence intervals for mean age difference. There are 31 actors that fulfill this criteria, and every one has an average age difference greater than zero. A reminder that filmographies for actors are not exhaustive, even for romances.

Topping the list of actors is Fred Astaire who starred in 17 films in the dataset and was on average, 18 years older than the leading lady. Astaire has been paired with actresses at least 30 years younger than him twice and has not had a romance with anyone younger than him. The actress closest in age to him was regular co-star Ginger Rogers (they headlined 7 films together in our sample), still 12 years his junior.

<table class="table table-striped table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption><span id="tab:unnamed-chunk-12"></span>Table 5: (\#tab:unnamed-chunk-12)Fred Astaire's co-stars</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Co-Star </th>
   <th style="text-align:right;"> Age Difference </th>
   <th style="text-align:right;"> # of Films </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Ginger Rogers </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 7 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Sarah Churchill </td>
   <td style="text-align:right;"> 15 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Joan Fontaine </td>
   <td style="text-align:right;"> 18 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Rita Hayworth </td>
   <td style="text-align:right;"> 19 </td>
   <td style="text-align:right;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Vera-Ellen </td>
   <td style="text-align:right;"> 22 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Cyd Charisse </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Judy Garland </td>
   <td style="text-align:right;"> 23 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Audrey Hepburn </td>
   <td style="text-align:right;"> 30 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Leslie Caron </td>
   <td style="text-align:right;"> 32 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
</tbody>
</table>

Most of the actors with large samples of films were stars from the Classic Hollywood era, the 1930s to 1960s. One reason for this was the studio system casting the same group of lead actors in their major releases. Another possible reason is that the older films that receive the most IMDb votes—our criteria for being selected into the sample—may be driven by how popular the actors are rather than the films' popularity at the time of their releases. The number of votes received by more recent releases are likely a better reflection of their actual standing today.

Of all actors with at least 10 romances, Rock Hudson is closest in age to his co-stars, on average only 1.5 years older than the leading ladies. Hudson starred opposite actresses across a range of ages. He was 13 years older than both Claudia Cardinale in *Blindfold* (1966) and Paula Prentiss in *Man's Favorite Sport?* (1964), but he was also paired with Doris Day, three years his senior, in three romantic comedies and Jane Wyman, eight years his senior, in two Douglas Sirk melodramas. 

<table class="table table-striped table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption><span id="tab:unnamed-chunk-13"></span>Table 7: (\#tab:unnamed-chunk-13)Rock Hudson's co-stars</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Co-Star </th>
   <th style="text-align:right;"> Age Difference </th>
   <th style="text-align:right;"> # of Films </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Jane Wyman </td>
   <td style="text-align:right;"> -8 </td>
   <td style="text-align:right;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Jennifer Jones </td>
   <td style="text-align:right;"> -6 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Donna Reed </td>
   <td style="text-align:right;"> -4 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Doris Day </td>
   <td style="text-align:right;"> -3 </td>
   <td style="text-align:right;"> 3 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Dorothy Malone </td>
   <td style="text-align:right;"> -1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Gina Lollobrigida </td>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Gena Rowlands </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Leslie Caron </td>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Mary Peach </td>
   <td style="text-align:right;"> 9 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Julie Andrews </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Claudia Cardinale </td>
   <td style="text-align:right;"> 13 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Paula Prentiss </td>
   <td style="text-align:right;"> 13 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
</tbody>
</table>

There are actors that have been on average, younger than their love interests, but are not included in the above graph because they have fewer than 10 films in the sample. There is a group of actors from the 1980s to 2000s where this is true: John Travola is 1.7 years younger in nine films, Ben Affleck is 2.3 years younger in seven films, Ashton Kutcher is 2.8 years younger in eight films, and Nicolas Cage is 4.3 years younger in seven films. On the opposite end, Humphrey Bogart is only listed for seven films and was on average 21 years older than the lead actress. This total only includes one of his pairings with real-life wife Lauren Bacall—25 years younger—because many of their romances were in film noirs not included in the sample.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-14-1.png" width="672" style="display: block; margin: auto;" />

For women, Audrey Hepburn starred in 14 romances and was on average 13.6 years younger than her love interest. Hepburn was only in her early twenties in the 1950s and was paired with major actors such as Humphrey Bogart, Fred Astaire, Gary Cooper, Cary Grant, and Henry Fonda, all of who started their careers in the 1930s or earlier. She was not casted regularly with actors her own age until a little later in her career.

<table class="table table-striped table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption><span id="tab:unnamed-chunk-15"></span>Table 9: (\#tab:unnamed-chunk-15)Audrey Hepburn's co-stars</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Co-Star </th>
   <th style="text-align:right;"> Age Difference </th>
   <th style="text-align:right;"> # of Films </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Anthony Perkins </td>
   <td style="text-align:right;"> -3 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Peter O'Toole </td>
   <td style="text-align:right;"> -3 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Ben Gazzara </td>
   <td style="text-align:right;"> -1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Sean Connery </td>
   <td style="text-align:right;"> -1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> George Peppard </td>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> William Holden </td>
   <td style="text-align:right;"> 11 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Gregory Peck </td>
   <td style="text-align:right;"> 13 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Burt Lancaster </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Rex Harrison </td>
   <td style="text-align:right;"> 21 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Henry Fonda </td>
   <td style="text-align:right;"> 24 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Cary Grant </td>
   <td style="text-align:right;"> 25 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Gary Cooper </td>
   <td style="text-align:right;"> 28 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Fred Astaire </td>
   <td style="text-align:right;"> 30 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Humphrey Bogart </td>
   <td style="text-align:right;"> 30 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
</tbody>
</table>

On the opposite end is Irene Dunne, who in 10 films was about 4.5 years older than her love interest. In fact, Dunne has never had an on screen love interest that was more than a year older than her (at least in this sample). Randolph Scott is the closest in age, but both Scott and her were born in the same year. Cary Grant, her most frequent romantic co-lead, was six years younger than Dunne.

<table class="table table-striped table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption><span id="tab:unnamed-chunk-16"></span>Table 11: (\#tab:unnamed-chunk-16)Irene Dunne's co-stars</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Co-Star </th>
   <th style="text-align:right;"> Age Difference </th>
   <th style="text-align:right;"> # of Films </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Alan Marshal </td>
   <td style="text-align:right;"> -11 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Allan Jones </td>
   <td style="text-align:right;"> -9 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Cary Grant </td>
   <td style="text-align:right;"> -6 </td>
   <td style="text-align:right;"> 3 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Melvyn Douglas </td>
   <td style="text-align:right;"> -3 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Spencer Tracy </td>
   <td style="text-align:right;"> -2 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Charles Boyer </td>
   <td style="text-align:right;"> -1 </td>
   <td style="text-align:right;"> 2 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Randolph Scott </td>
   <td style="text-align:right;"> 0 </td>
   <td style="text-align:right;"> 1 </td>
  </tr>
</tbody>
</table>

The next three actresses that were on average older than their male co-stars—Joan Crawford, Marion Davies, and Jean Arthur—all started their careers in the 20s and 30s. This is also true of Dunne who was a star in the 30s and 40s. It is surprising that the bottom of the list does not include a larger number of newer actresses, given that age differences between film couples became smaller in the more recent decades. Loosening the film count requirement down from 10 to 5 brings in more actresses from 1970s and beyond, but Dunne, Crawford, Davies, and Arthur still have the most negative mean age differences. At the top of the graph, if we drop the requirement to five, Sophia Loren would end up with the largest value. Loren appeared in seven films and was on average 19.3 years younger than her romantic partners.

Lastly, we look at romances between same-sex couples. This was a much more difficult dataset to build because there are few mainstream Hollywood films centered on gay and lesbian romances, and the ones that we have are all from the last few decades. The most popular films from IMDb, regardless of year, with the tags "gay romance," "gay relationship," "lesbian romance," or "lesbian relationship" were sampled. To allow for more films, we looked at all English-language films—regardless of whether they were American—resulting in the addition of a few films from the United Kingdom and Australia into the dataset. This gave a final sample of only 83 films, 40 featuring relationships between two women and 43 featuring relationships between two men. The earliest title was from 1968, but most were from the 1990s and after. Compare this to the dataset for opposite-sex couples which maxed out at 25 American titles per year but still had 2,056 films.



The mean age difference between lesbian couples is 6.7 years with a standard deviation of 7.5. The mean age difference between gay couples is 7.7 years with a standard deviation of 6. Both values are larger than the average age difference between opposite-sex couples of 6.2 years, with this number going down to 4.7 years if only films since 1990 are considered, to better match the same-sex dataset.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-18-1.png" width="576" style="display: block; margin: auto;" />

As we did previously for opposite sex couples, we plot the ages of couples for all films. Instead of using gender on the x- and y-axes, we plot the younger person in the relationship against the older person. There is little difference between the two graphs, with gay and lesbian romances pairing couples with similar age differences. Most of the lead actors in same-sex romances are in their 20s and 30s, with the average woman at 33.3-years-old and the average man at 34.1-years-old. If we look at the same statistics for opposite-sex couples since 1990, we see that the average lead actress is 31.5-years-old and the average lead actor is 36.2-years-old. Gay romances skew a little younger and lesbian romances skew a little older compared to opposite-sex romances. There are also very few actors and actresses over the age of 50 starring in gay and lesbian romances.
