---
title: NBA Hometowns
author: Robert Huang
date: '2020-04-27'
slug: nba-hometowns
categories: []
tags:
  - nba
---

<link href="{{< blogdown/postref >}}index_files/htmltools-fill/fill.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<link href="{{< blogdown/postref >}}index_files/datatables-css/datatables-crosstalk.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/datatables-binding/datatables.js"></script>
<script src="{{< blogdown/postref >}}index_files/jquery/jquery-3.6.0.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/dt-core/css/jquery.dataTables.min.css" rel="stylesheet" />
<link href="{{< blogdown/postref >}}index_files/dt-core/css/jquery.dataTables.extra.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/dt-core/js/jquery.dataTables.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/crosstalk/css/crosstalk.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/crosstalk/js/crosstalk.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/htmltools-fill/fill.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<link href="{{< blogdown/postref >}}index_files/datatables-css/datatables-crosstalk.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/datatables-binding/datatables.js"></script>
<script src="{{< blogdown/postref >}}index_files/jquery/jquery-3.6.0.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/dt-core/css/jquery.dataTables.min.css" rel="stylesheet" />
<link href="{{< blogdown/postref >}}index_files/dt-core/css/jquery.dataTables.extra.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/dt-core/js/jquery.dataTables.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/crosstalk/css/crosstalk.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/crosstalk/js/crosstalk.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<link href="{{< blogdown/postref >}}index_files/htmltools-fill/fill.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<link href="{{< blogdown/postref >}}index_files/datatables-css/datatables-crosstalk.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/datatables-binding/datatables.js"></script>
<script src="{{< blogdown/postref >}}index_files/jquery/jquery-3.6.0.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/dt-core/css/jquery.dataTables.min.css" rel="stylesheet" />
<link href="{{< blogdown/postref >}}index_files/dt-core/css/jquery.dataTables.extra.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/dt-core/js/jquery.dataTables.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/crosstalk/css/crosstalk.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/crosstalk/js/crosstalk.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/htmltools-fill/fill.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<link href="{{< blogdown/postref >}}index_files/datatables-css/datatables-crosstalk.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/datatables-binding/datatables.js"></script>
<script src="{{< blogdown/postref >}}index_files/jquery/jquery-3.6.0.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/dt-core/css/jquery.dataTables.min.css" rel="stylesheet" />
<link href="{{< blogdown/postref >}}index_files/dt-core/css/jquery.dataTables.extra.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/dt-core/js/jquery.dataTables.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/crosstalk/css/crosstalk.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/crosstalk/js/crosstalk.min.js"></script>

## Background

NBA players come from all across the United States, but some areas of the country have greater reputations as centers of basketball activity than others. Which American cities have produced the most NBA players and has this changed throughout the NBA’s history? Are basketball hotbeds from the 1960s still producing the same number of players today or has the game shifted geographically? We will try to answer these questions.

First, all players must be assigned to a single hometown. This is not a simple task as there is not a precise definition for hometown. Should it be birthplace, elementary school city, middle school city, or high school city? It would be simple if all of these places were consistent for each player, but players move around, transfer between many educational institutions, or attend boarding schools in cities they have no real connection to. Ideally for us, hometown should be something like the permanent city of residence where the player spends most of his basketball life before leaving for college or the NBA. This database does not exist, but we can estimate it using biographical data that is freely available. For most players, this will be their high school city. If the high school is a boarding school (ex: Oak Hill Academy in Mouth of Wilson, VA; Findlay Prep in Henderson, NV; Hargrave Military Academy in Chatham, VA) or a pit stop along a string of multiple transfers, we try to find the player’s main residence before moving. A lot of this information is available in either [Basketball Reference](https://www.basketball-reference.com/) or the player’s college athletic program roster/biography/media guide. [Peach Basket Society](http://peachbasketsociety.blogspot.com/) is incredibly useful for the NBA/BAA’s earlier days. Even with the breadth of biographical information at hand, there are many cases where a hometown is difficult to define (try settling on a city for Shaquille O’Neal or Bill Laimbeer).

The cities from the various sources are inconsistent in the level of detail. For example, Khalid Reeves graduated from Christ the King in Middle Village, Queens, New York, NY. Basketball Reference lists the city as Middle Village, NY. Smush Parker graduated from Newton High School in Elmhurst, Queens, New York, NY. His high school city is listed as Queens, NY. For consistency, cities are grouped into Core Based Statistical Areas (CBSA) as defined by the United States Office of Management and Budget. Using this definition, multiple counties can be grouped together into metropolitan or micropolitan areas. This results in New York, Newark, Jersey City, and other surrounding places being grouped into the New York metropolitan area while Philadelphia, Camden, Wilmington, and other surrounding areas being grouped into the Philadelphia metropolitan area. Not all cities can be categorized into CBSAs; cities that cannot be assigned will use their counties instead.

## Leading Hometowns

<div class="datatables html-widget html-fill-item" id="htmlwidget-1" style="width:100%;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-1">{"x":{"filter":"none","vertical":false,"data":[["NY-NJ-PA","CA","IL-IN-WI","PA-NJ-DE-MD","DC-VA-MD-WV","MI","GA","CA","TX","TX","IN","PA","TN-MS-AR","MD","MO-IL","MN-WI","OH-KY-IN","WA","MA-NH","CA","FL","KY-IN","OR-WA","OH","WI","MO-KS","MS","OH","LA","VA","NC-SC","OH","AL","CA","LA","AZ","MI","OH","OK","VA-NC","NY","CO","FL","OH","TN","CA","CT","FL","NV","TX","CA","NC","NY","CA","OH","RI-MA","AR","CT","GA","KY","NC","NE-IA","OK","MI","FL","IN","KS","NJ","WI","AL","CA","FL","LA","MI","PA","SC","IL","IN","IN-MI","NC","PA","UT","UT","WV","CT","GA-SC","IN","LA","MI","MI","NC","NY","NY","TX","CA","FL","IN","IN-KY","KY","MS","NC","TN-KY","WV-OH","AL","CO","FL","GA","GA-AL","IA","IA-IL","IL","IN","MA-CT","MS","NC","OH","OH-PA","PA-NJ","SC","TX","UT","VA","WV-KY-OH","AR","AZ","CO","CT","FL","FL","IA","IL","IL","IN","IN","KY","LA","MA","MD-WV","MN-WI","NC","NC","NC","NY","PA","SC-NC","TN","TN","TX","TX","WA","WI","AL","AL","AR","AR","AR-OK","CA","CA","CA","CO","FL","GA","GA-AL","IA","IL","IN","IN","LA","MI","MO","MS","MS","NC","NJ","NM","NY","OK","OK","PA","PA","SC","TN","TN","TN-GA","VA","WI","WY","AK","AL","AL","AL","AL","AL","AL","AZ","CA","CA","CA","CT","FL","FL","FL","GA","GA","IL","IL","IL","IL","IL","IL","IL-MO","IN","IN","IN","IN","IN","KS","KY","KY","KY","KY","KY","KY-IL","LA","LA","LA","LA","LA","LA","LA","LA","MD-DE","MI","MI","MI","MI","MN","MN","MO","MO-IL","MS","NC","NC","NC","NC","NC","NE","NM","NV","OH","OH","OH","OH","OH","OK","OK","OR","PA","PA","PA","SC","SC","TN","TX","TX","TX","TX","TX","VA","VA","WA","WA","WA","WI","WI","WI-MN","WV","WY","AK","AL","AL","AL","AL","AL","AL-GA","AR","AR","AR","AR","AR","AR","AR","AR","AR","AR","CA","CA","CA","CA","CA","CA","CA","CA","FL","FL","FL","FL","GA","GA","GA","GA","GA","GA","GA","GA","GA","GA","GA","GA","GA","HI","IA","IA","IA","IA","IA","IA","IA","IA","IA","IA","IA-IL-MO","IA-NE-SD","ID","ID","ID","ID","IL","IL","IL","IL","IL","IL","IL","IL","IL","IL","IL","IL","IL","IL","IN","IN","IN","IN","IN","IN","IN","IN","IN","IN","KS","KS","KS","KS","KS","KS","KS","KS","KS","KY","KY","KY","KY","KY","KY","KY","KY","KY","KY","KY","KY","KY","KY","KY","KY","KY","KY","KY","LA","LA","LA","LA","LA","LA","LA","LA","MI","MI","MI","MI","MI","MN","MN","MN","MN","MN","MN","MN","MO","MO","MO","MO","MO","MO","MO","MO","MO","MO","MO","MO","MO","MS","MS","MS","MS","MS","MS","MS","MS","MS","MS","MS","MS","MS","MS","MS","MS","MS","MS-LA","MT","MT","MT","MT","MT","NC","NC","NC","NC","NC","NC","NC","NC","NC","NC","NC","NC","NC","NC","NC","NC","ND","ND","ND-MN","NE","NE","NH","NM","NM","NY","NY","NY","NY","NY","NY","NY","OH","OH","OH","OH","OH","OH","OK","OK","OK","OK","OR","OR","OR","OR","PA","PA","PA","PA","PA","PA","PA","SC","SC","SC","SC","SC","SC","SC","SD","SD","SD","TN","TN","TN","TN","TN-VA","TX","TX","TX","TX","TX","TX","TX","TX","TX","TX","TX","TX","TX","TX","TX","TX","TX","TX","TX","TX","TX","UT","UT-ID","VA","VA","VA","VA","VA","VA","VA-WV","WA","WA","WA","WA","WA","WA","WA","WA","WA","WI","WI","WI","WI","WI","WI","WI","WI","WI-MI","WV","WV","WV","WV-OH","WV-VA","WY","WY","WY"],["New York, NY","Los Angeles, CA","Chicago, IL","Philadelphia, PA","Washington, DC","Detroit, MI","Atlanta, GA","San Francisco, CA","Dallas, TX","Houston, TX","Indianapolis, IN","Pittsburgh, PA","Memphis, TN","Baltimore, MD","St. Louis, MO","Minneapolis, MN","Cincinnati, OH","Seattle, WA","Boston, MA","Riverside, CA","Miami, FL","Louisville, KY","Portland, OR","Columbus, OH","Milwaukee, WI","Kansas City, MO","Jackson, MS","Cleveland, OH","Baton Rouge, LA","Richmond, VA","Charlotte, NC","Dayton, OH","Birmingham, AL","San Diego, CA","New Orleans, LA","Phoenix, AZ","Flint, MI","Toledo, OH","Oklahoma City, OK","Virginia Beach, VA","Buffalo, NY","Denver, CO","Orlando, FL","Akron, OH","Nashville, TN","San Jose, CA","Hartford, CT","Tampa, FL","Las Vegas, NV","San Antonio, TX","Sacramento, CA","Raleigh, NC","Rochester, NY","Fresno, CA","Canton, OH","Providence, RI","Little Rock, AR","Bridgeport, CT","Macon, GA","Lexington, KY","Winston, NC","Omaha, NE","Tulsa, OK","Lansing, MI","Jacksonville, FL","Fort Wayne, IN","Wichita, KS","Trenton, NJ","Racine, WI","Montgomery, AL","Bakersfield, CA","Lakeland, FL","Monroe, LA","Grand Rapids, MI","Scranton, PA","Columbia, SC","Peoria, IL","Muncie, IN","South Bend, IN","Greensboro, NC","Harrisburg, PA","Provo, UT","Salt Lake City, UT","Charleston, WV","New Haven, CT","Augusta, GA","Terre Haute, IN","Shreveport, LA","Niles, MI","Saginaw, MI","Durham, NC","Albany, NY","Syracuse, NY","Beaumont, TX","Santa Maria, CA","Pensacola, FL","Washington, IN","Evansville, IN","London, KY","Gulfport, MS","Kinston, NC","Clarksville, TN","Wheeling, WV","Mobile, AL","Boulder, CO","Ocala, FL","Savannah, GA","Columbus, GA","Des Moines, IA","Davenport, IA","Springfield, IL","Elkhart, IN","Worcester, MA","Meridian, MS","Fayetteville, NC","Springfield, OH","Youngstown, OH","Allentown, PA","Greenville, SC","Austin, TX","Ogden, UT","Roanoke, VA","Huntington, WV","Desha County, AR","Tucson, AZ","Colorado Springs, CO","Norwich, CT","Cape Coral, FL","Deltona, FL","Ames, IA","Carbondale, IL","Rockford, IL","Jasper, IN","Warsaw, IN","Owensboro, KY","Lake Charles, LA","Springfield, MA","Hagerstown, MD","Duluth, MN","Rocky Mount, NC","Washington, NC","Wilmington, NC","Poughkeepsie, NY","Altoona, PA","Myrtle Beach, SC","Cleveland, TN","Knoxville, TN","Killeen, TX","Longview, TX","Spokane, WA","Madison, WI","Talladega, AL","Tuscaloosa, AL","Ashley County, AR","Pine Bluff, AR","Fort Smith, AR","Oxnard, CA","Stockton, CA","Visalia, CA","Greeley, CO","North Port, FL","Albany, GA","LaGrange, GA","Cedar Rapids, IA","Centralia, IL","Marion, IN","Michigan City, IN","Ruston, LA","Ann Arbor, MI","Poplar Bluff, MO","Greenwood, MS","Hattiesburg, MS","Burlington, NC","Atlantic City, NJ","Hobbs, NM","Binghamton, NY","Lawton, OK","Washita County, OK","Johnstown, PA","Lancaster, PA","Charleston, SC","Brownsville, TN","Hardeman County, TN","Chattanooga, TN","Staunton, VA","Sheboygan, WI","Cheyenne, WY","Anchorage, AK","Crenshaw County, AL","Marengo County, AL","Dothan, AL","Enterprise, AL","Florence, AL","Huntsville, AL","Prescott Valley, AZ","Modesto, CA","Santa Cruz, CA","Vallejo, CA","Torrington, CT","Crestview, FL","Gainesville, FL","Port St. Lucie, FL","Brunswick, GA","Milledgeville, GA","Franklin County, IL","Hamilton County, IL","Kankakee, IL","Lincoln, IL","Mount Vernon, IL","Ottawa, IL","Quincy, IL","Bloomington, IN","Lafayette, IN","New Castle, IN","Peru, IN","Richmond, IN","Liberal, KS","Bowling Green, KY","Campbellsville, KY","Johnson County, KY","Logan County, KY","Marshall County, KY","Paducah, KY","Alexandria, LA","DeRidder, LA","Bienville Parish, LA","Claiborne Parish, LA","Madison Parish, LA","Lafayette, LA","Minden, LA","Morgan City, LA","Salisbury, MD","Van Buren County, MI","Kalamazoo, MI","Muskegon, MI","Traverse City, MI","Murray County, MN","St. Cloud, MN","Columbia, MO","Cape Girardeau, MO","Clarksdale, MS","Asheville, NC","Greenville, NC","Hickory, NC","Laurinburg, NC","Roanoke Rapids, NC","Scottsbluff, NE","Albuquerque, NM","Reno, NV","Bellefontaine, OH","Chillicothe, OH","Mansfield, OH","New Philadelphia, OH","Sandusky, OH","Enid, OK","Caddo County, OK","Eugene, OR","Erie, PA","Pottsville, PA","Reading, PA","Newberry, SC","Orangeburg, SC","Perry County, TN","Athens, TX","College Station, TX","El Paso, TX","Huntsville, TX","Nacogdoches, TX","Halifax County, VA","Westmoreland County, VA","Aberdeen, WA","Bellingham, WA","Bremerton, WA","Eau Claire, WI","Janesville, WI","La Crosse, WI","Wyoming County, WV","Hot Springs County, WY","Juneau, AK","Covington County, AL","Macon County, AL","Monroe County, AL","Alexander City, AL","Decatur, AL","Eufaula, AL","Conway County, AR","Cross County, AR","Jackson County, AR","Johnson County, AR","Camden, AR","El Dorado, AR","Fayetteville, AR","Hope, AR","Jonesboro, AR","Russellville, AR","Plumas County, CA","Chico, CA","Eureka, CA","Hanford, CA","Merced, CA","Salinas, CA","Santa Rosa, CA","Ukiah, CA","Washington County, FL","Naples, FL","Palm Bay, FL","Tallahassee, FL","Appling County, GA","Emanuel County, GA","Mitchell County, GA","Randolph County, GA","Telfair County, GA","Washington County, GA","Cordele, GA","Hinesville, GA","Rome, GA","Thomaston, GA","Thomasville, GA","Toccoa, GA","Warner Robins, GA","Hilo, HI","Allamakee County, IA","Clayton County, IA","Fremont County, IA","Hardin County, IA","Palo Alto County, IA","Plymouth County, IA","Dubuque, IA","Iowa City, IA","Mason City, IA","Pella, IA","Fort Madison, IA","Sioux City, IA","Blackfoot, ID","Boise City, ID","Pocatello, ID","Twin Falls, ID","Bloomington, IL","Champaign, IL","Charleston, IL","Crawford County, IL","De Witt County, IL","Montgomery County, IL","Pike County, IL","Wabash County, IL","Danville, IL","Decatur, IL","Freeport, IL","Rochelle, IL","Sterling, IL","Taylorville, IL","Bedford, IN","Orange County, IN","Perry County, IN","Ripley County, IN","Tipton County, IN","Crawfordsville, IN","Frankfort, IN","Huntington, IN","Kendallville, IN","Plymouth, IN","Coffeyville, KS","Dodge City, KS","Haskell County, KS","Scott County, KS","Manhattan, KS","McPherson, KS","Ottawa, KS","Topeka, KS","Winfield, KS","Breckinridge County, KY","Caldwell County, KY","Crittenden County, KY","Harlan County, KY","Hart County, KY","Lewis County, KY","Lyon County, KY","Mercer County, KY","Ohio County, KY","Perry County, KY","Trimble County, KY","Union County, KY","Webster County, KY","Madisonville, KY","Mayfield, KY","Maysville, KY","Mount Sterling, KY","Richmond, KY","Somerset, KY","Catahoula Parish, LA","Jackson Parish, LA","Richland Parish, LA","West Carroll Parish, LA","Winn Parish, LA","Fort Polk South, LA","Houma, LA","Natchitoches, LA","Alpena, MI","Battle Creek, MI","Bay City, MI","Oceana County, MI","Jackson, MI","Brainerd, MN","Grand Rapids, MN","Clearwater County, MN","Lac qui Parle County, MN","Pine County, MN","Rochester, MN","Winona, MN","Branson, MO","Fort Leonard Wood, MO","Jefferson City, MO","Kirksville, MO","Gasconade County, MO","Iron County, MO","Shelby County, MO","Stoddard County, MO","Marshall, MO","Mexico, MO","Sedalia, MO","Sikeston, MO","Springfield, MO","Cleveland, MS","Columbus, MS","Greenville, MS","Indianola, MS","Chickasaw County, MS","Humphreys County, MS","Jefferson Davis County, MS","Lawrence County, MS","Monroe County, MS","Sharkey County, MS","Union County, MS","Walthall County, MS","Laurel, MS","McComb, MS","Picayune, MS","Starkville, MS","Vicksburg, MS","Natchez, MS","Great Falls, MT","Custer County, MT","Deer Lodge County, MT","Hill County, MT","Missoula, MT","Elizabeth City, NC","Forest City, NC","Goldsboro, NC","Henderson, NC","New Bern, NC","Avery County, NC","Bertie County, NC","Columbus County, NC","Duplin County, NC","Greene County, NC","Polk County, NC","Sampson County, NC","Tyrrell County, NC","Rockingham, NC","Shelby, NC","Wilson, NC","Burke County, ND","Williston, ND","Grand Forks, ND","Lincoln, NE","Hamilton County, NE","Concord, NH","Los Alamos, NM","Quay County, NM","Glens Falls, NY","Hudson, NY","Jamestown, NY","Sullivan County, NY","Ogdensburg, NY","Seneca Falls, NY","Watertown, NY","Findlay, OH","Greenville, OH","Lima, OH","Highland County, OH","Wapakoneta, OH","Zanesville, OH","Altus, OK","Ardmore, OK","McAlester, OK","Shawnee, OK","Coos Bay, OR","Corvallis, OR","Medford, OR","Salem, OR","Bloomsburg, PA","Lebanon, PA","New Castle, PA","Tioga County, PA","Sayre, PA","Sunbury, PA","Williamsport, PA","Bennettsville, SC","Gaffney, SC","Spartanburg, SC","Sumter, SC","Dillon County, SC","Williamsburg County, SC","Union, SC","Brookings, SD","Mitchell, SD","Hutchinson County, SD","Jackson, TN","Lewisburg, TN","Martin, TN","Paris, TN","Kingsport, TN","Abilene, TX","Amarillo, TX","Bay City, TX","Brownsville, TX","Corpus Christi, TX","Corsicana, TX","Jacksonville, TX","Lubbock, TX","Stephenville, TX","Sulphur Springs, TX","Waco, TX","Cass County, TX","Eastland County, TX","Gonzales County, TX","Grimes County, TX","Hill County, TX","Knox County, TX","Parmer County, TX","San Augustine County, TX","Tyler County, TX","Wichita Falls, TX","Emery County, UT","Logan, UT","Danville, VA","Harrisonburg, VA","Alleghany County, VA","Brunswick County, VA","Lee County, VA","Mecklenburg County, VA","Winchester, VA","Ellensburg, WA","Kennewick, WA","Mount Vernon, WA","Olympia, WA","Port Angeles, WA","Walla Walla, WA","Wenatchee, WA","Jefferson County, WA","Pend Oreille County, WA","Baraboo, WI","Beaver Dam, WI","Fond du Lac, WI","Green Bay, WI","Manitowoc, WI","Oshkosh, WI","Wausau, WI","Barron County, WI","Marinette, WI","Beckley, WV","Clarksburg, WV","Greenbrier County, WV","Weirton, WV","Bluefield, WV","Casper, WY","Laramie, WY","Lincoln County, WY"],[444,243,239,149,118,104,82,74,69,62,55,53,44,43,43,40,40,40,39,34,32,32,31,30,30,28,27,27,26,26,25,25,24,23,23,21,21,20,20,19,18,17,17,17,17,16,16,16,15,15,14,14,14,13,13,13,12,12,12,12,12,12,12,11,10,10,10,10,10,9,9,9,9,9,9,9,8,8,8,8,8,8,8,8,7,7,7,7,7,7,7,7,7,7,6,6,6,6,6,6,6,6,6,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,4,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1],["Kareem Abdul-Jabbar","Paul Pierce","Juwan Howard","Kobe Bryant","Grant Hill","Kevin Willis","Dale Ellis","Jason Kidd","Kurt Thomas","Clyde Drexler","Oscar Robertson","Brad Davis","Michael Cage","Carmelo Anthony","Jo Jo White","Kris Humphries","LaSalle Thompson","Jason Terry","Patrick Ewing","Reggie Miller","Otis Thorpe","Wes Unseld","A.C. Green","Herb Williams","Terry Porter","Earl Watson","Lindsey Hunter","Charles Oakley","Hot Rod Williams","Moses Malone","Antawn Jamison","Johnny Green","Charles Barkley","Chris Dudley","Avery Johnson","Richard Jefferson","Glen Rice","Jim Jackson","Alvan Adams","Joe Smith","Clifford Robinson","Chauncey Billups","Darryl Dawkins","LeBron James","Corey Brewer","Kurt Rambis","Rick Mahorn","Marreese Speights","Greg Anthony","Shaquille O'Neal","Bill Cartwright","Nate McMillan","Walter Dukes","Bruce Bowen","Dick Snyder","Ernie DiGregorio","Derek Fisher","Calvin Murphy","Jeff Malone","Shelvin Mack","Chris Paul","Bob Boozer","John Starks","Magic Johnson","Truck Robinson","Henry James","Antoine Carr","Dahntay Jones","Caron Butler","Ben Wallace","Lonnie Shelton","Tracy McGrady","Benoit Benjamin","Chris Kaman","Bob Sura","Alex English","Shaun Livingston","Allen Leavell","Tom Abernethy","Lou Hudson","Billy Owens","Justin Hamilton","Fred Roberts","Jerry West","Ryan Gomes","Michael Curry","Clyde Lovellette","Robert Parish","Chet Walker","Jason Richardson","John Lucas","Pat Riley","Danny Schayes","Stephen Jackson","Mike Bratz","Reggie Evans","Tyler Zeller","Calbert Cheaney","Frank Selvy","Mahmoud Abdul-Rauf","Jerry Stackhouse","Trenton Hassell","John Havlicek","DeMarcus Cousins","Tom Chambers","Eddie Johnson","Pervis Ellison","Sam Mitchell","Matt Bullard","Don Nelson","Andre Iguodala","Shawn Kemp","Michael Bradley","Antonio McDyess","Eric Maynor","Wayne Embry","Jack Marin","Aaron Gray","Kevin Garnett","Luke Jackson","Arnie Ferrin","J.J. Redick","Hal Greer","Caldwell Jones","Fat Lever","Pat Garrity","Harold Pressley","Walt Wesley","Vince Carter","Fred Hoiberg","Troy Hudson","Fred VanVleet","Don Buse","Mason Plumlee","Cliff Hagan","Tierre Brown","Travis Best","Dennis Scott","Kevin McHale","Buck Williams","Dominique Wilkins","Michael Jordan","Rich Rinaldi","Doug West","Chucky Brown","Alvin Scott","Elston Turner","Brian Skinner","David Wesley","John Stockton","Wesley Matthews","Gerald Wallace","Pete Chilcutt","Scottie Pippen","Andrew Lang","Jim King","Jamaal Wilkes","Scott Brooks","Jack Rocker","Jason Smith","Howard Porter","Dontonio Wingfield","Gar Heard","Al Eberhard","Dick Garrett","Zach Randolph","Ron Reed","Paul Millsap","Bob Elliott","Tyler Hansbrough","Willie Norwood","Purvis Short","Geoff Crompton","Chris Ford","Bill Bridges","Bill Gabor","Stacey King","Gary Hill","Pat Cummings","Wally Walker","Anthony Johnson","Tony Delk","Bailey Howell","Anthony Roberts","Dell Curry","Joe Wolf","James Johnson","Mario Chalmers","Chuck Person","Theo Ratliff","Jim Farmer","Doug Sims","Leon Douglas","Keith Askins","Bayard Forrest","Chuck Hayes","Kenny Sears","Brandon Armstrong","Chuck Aleksinas","Tom Hammonds","Vernon Maxwell","Larry Sanders","Kwame Brown","Horace Grant","Doug Collins","Jerry Sloan","Jack Sikma","Brian Cook","Nate Hawthorne","Joe Ruklick","Gary Phillips","Jared Jeffries","Carl Shaeffer","Kent Benson","Kyle Macy","John Logan","Martin Lewis","Odie Spears","Clem Haskins","Donnie Butcher","Bubba Wells","Joe Holland","Phil Rollins","Paul Thompson","Mike Sanders","Marcus Fizer","Karl Malone","James Silas","David Benoit","Jackie Moreland","Dave Johnson","Tal Skinner","Kenny McIntosh","Chris Crawford","Deyonta Davis","Dan Majerle","Arvid Kramer","Mark Olberding","Harold Kottman","Chico Vaughn","Earl Barron","Brad Daugherty","Mitchell Wiggins","Bob Warlick","Sam Jones","Delaney Rudd","Eric Piatkowski","Daniel Santiago","Luke Babbitt","Don Otten","Neil Johnston","Larry Siegfried","Frankie Baumholtz","Dick Schnittker","Mark Price","Aubrey Davis","Danny Ainge","Essie Hollis","George Senesky","Donyell Marshall","Trevor Booker","Harold Jamison","Bob Harris","Jake Carter","Bill Closs","Kenny Thomas","Frank Gates","John Hargis","Terry Davis","Justin Anderson","Rod Derline","Luke Ridnour","Marvin Williams","Chuck Mencel","Bill Hanzlik","Tom Black","Mike D'Antoni","John Pilch","Carlos Boozer","Robert Horry","Rory White","John Drew","Jamario Moon","Bud Stallworth","Travis Grant","Jimmy Oliver","Jeff Martin","Jim Barnes","Ron Moore","Tom Patterson","James Anderson","Ronnie Brewer","Paul Silas","Malik Monk","Corliss Williamson","Bill Stricker","Isaac Austin","Darrell Brown","Pete Verhoeven","Gerald Madkins","Orlando Johnson","Josh Akognon","Phil Jordon","Artis Gilmore","Jonathan Isaac","Will Perdue","Clemon Johnson","Frankie King","Tony Mitchell","Jumaine Jones","Donnell Harvey","Wayne Cooper","Greg Minor","Tree Rollins","Jordan McRae","Mike Glenn","Darrell Lockhart","Charlie Ward","Dale Davis","Al Thornton","Red Rocha","Brett Szabo","Raef LaFrentz","Barry Yates","Nick Collison","Loren Meyer","Dave Gunther","Kevin Kunnert","Matt Fish","Dean Oliver","Kyle Korver","Ryan Bowen","Kirk Hinrich","Steve Hayes","Gary Freeman","Dale Wilkinson","Andy Toolson","Keita Bates-Diop","Brian Cardinal","Rex Morgan","Meyers Leonard","Gene Vance","Ed Dahler","Lew Hitch","Archie Dees","Keon Clark","Dave Scholz","Kim Hughes","Dan Godfread","Fran Curran","Johnny Orr","Jack Turner","Larry Bird","Tommy Kron","Steve Green","Darrell Elston","Earl Gardner","Ward Williams","Ralph Johnson","Brad Miller","Scott Skiles","Scott Hastings","Willie Cauley-Stein","Otto Schnellbacher","Ron Baker","Dick Knostman","Steve Henson","Semi Ojeleye","Paul Shirley","Bob Brannum","Butch Beard","Greg Smith","Blackie Towery","Wah Wah Jones","Clarence Glover","Ralph Davis","Joe Fulks","Jack Coleman","John Oldham","Johnny Cox","Jack Tingle","Larry Johnson","Virgil Vaughn","Frank Ramsey","Adrian Smith","Darius Miller","Dan Swartz","Tex Ritter","Reggie Hanson","Ervin Johnson","Bob Hopkins","Elvin Hayes","Mel McGaha","P.J. Brown","Nikita Wilson","Mark Davis","Joe Dumars","Harvey Marlatt","Nate Huffman","Matt Costello","Paul Griffin","Phil Martin","Whitey Skoog","Doug Bolstorff","Arnie Johnson","Jeff Nordgaard","Vern Mikkelsen","Randy Breuer","Clint Wager","Steven Hill","John Brown","OG Anunoby","Scott Sims","Don Anielak","Chris Carr","Norm Stewart","Win Wilfong","Joe Kleine","Tyronn Lue","Kim Anderson","Otto Porter","Anthony Tolliver","Johnny O'Bryant","Clarence Weatherspoon","Larry Smith","Sam Lacey","Terry Catledge","Spencer Haywood","Al Jefferson","Erick Dampier","Dwayne Whitfield","Slick Watts","John Stroud","George Johnson","Kenny Payne","Mike Green","Jonathan Bender","Travis Outlaw","Michael Phelps","Jim Ware","Josh Huestis","Jack Cotton","Ed Kalafat","Ray Kuka","Larry Krystkowiak","Kenny Williams","Belus Smawley","Mike Evans","Dave Henderson","Walt Bellamy","Tom Burleson","Kent Bazemore","Jerrod Mustaf","M.L. Carr","Blue Edwards","Harthorne Wingo","Chris King","Brian Rowsom","Mel Gibson","David Thompson","Jamie Watson","Les Jepsen","Phil Jackson","Glenn Hansen","Alex Stivrins","Tom Kropp","Matt Bonner","Alex Kirk","Chick Halbert","Jimmer Fredette","Tyler Lydon","George Carter","Maurice Martin","Rick Carlisle","John Schweitz","Lou Spicer","Dave Sorenson","Bob Brown","John McCullough","Don Grate","Evan Eschmeyer","Kevin Martin","Bob Priddy","Cecil Hankins","Claude Overton","Ken Corley","Mel Counts","Dave Gambee","Kyle Singler","Josh Davis","Joe Colone","Sam Bowie","Herschel Baltimore","Tom McMillen","Bob Weiss","John Barr","Alize Johnson","Cozell McQueen","Mikki Moore","Garland O'Shields","Ray Allen","Raymond Felton","Mike Gibson","Clifford Ray","Ray Ellefson","Mike Miller","Jared Reiner","Todd Mundt","Marcus Haislip","Popeye Jones","Dan King","Bob Hogsett","Andrae Patterson","Gene Wiley","LaBradford Smith","Tom Barker","Adrian Caldwell","Wesley Johnson","Bob Burrow","Craig Ehlo","Jim Spruill","Bob Carpenter","Kenrich Williams","John Barber","Grady Lewis","Carlton McKinney","Chris Andersen","Mike Harris","Howie Shannon","Price Brookfield","Terry Teagle","Zelmo Beaty","Jack Maddox","Shawn Bradley","Ariel Maughan","Johnny Newman","Ralph Sampson","Linton Townes","Bryant Stith","Jim Palmer","Jerome Kersey","Erick Green","Byron Beck","Gene Conley","Mark Hendrickson","John Greig","Bernie Fryer","Red Morrison","Joe Harris","John Stroeder","Jacob Wiley","Paul Cloyd","Greg Stiemsma","Travis Diener","Tony Bennett","Logan Vander Velden","Wayne Kreklow","Frank Schade","Henry Ellenson","Mel Peterson","Tamar Slay","Bob Wilson","Bimbo Coles","Ron Williams","Rod Thorn","Floyd Volker","Kenny Sailors","Vern Gardner"],["Kareem Abdul-Jabbar","Paul Pierce","Shawn Marion","Wilt Chamberlain","David Robinson","George Gervin","Dwight Howard","Bill Russell","LaMarcus Aldridge","Clyde Drexler","Oscar Robertson","Jack Twyman","Michael Cage","Carmelo Anthony","Ed Macauley","Kris Humphries","Jerry Lucas","Jason Terry","Patrick Ewing","Reggie Miller","Otis Thorpe","Wes Unseld","A.C. Green","Michael Redd","Terry Porter","Lucius Allen","Monta Ellis","Charles Oakley","Bob Pettit","Moses Malone","Stephen Curry","Ron Harper","Charles Barkley","Cliff Levingston","Avery Johnson","Richard Jefferson","Glen Rice","Steve Mix","Blake Griffin","Allen Iverson","Bob Lanier","Chauncey Billups","Darryl Dawkins","LeBron James","Clyde Lee","Kurt Rambis","Marcus Camby","Matt Geiger","Greg Anthony","Shaquille O'Neal","Kevin Johnson","Nate McMillan","Walter Dukes","Brook Lopez","Dick Snyder","Earl Shannon","Sidney Moncrief","Calvin Murphy","Jeff Malone","Melvin Turpin","Chris Paul","Bob Boozer","John Starks","Magic Johnson","Truck Robinson","Herm Schaefer","Antoine Carr","Bud Palmer","Caron Butler","Ben Wallace","Lonnie Shelton","Tracy McGrady","Willis Reed","Loy Vaught","Bob Sura","Alex English","Shaun Livingston","Allen Leavell","Tom Abernethy","Bob McAdoo","Bob Davies","Justin Hamilton","Fred Roberts","Jerry West","Ryan Gomes","Michael Curry","Clyde Lovellette","Robert Parish","Chet Walker","Jason Richardson","John Lucas","Luther Rackley","Larry Costello","Stephen Jackson","Don Ford","Reggie Evans","Cody Zeller","Calbert Cheaney","Frank Selvy","Mahmoud Abdul-Rauf","Cedric Maxwell","Chris Whitney","John Havlicek","DeMarcus Cousins","Tom Chambers","Eddie Johnson","Pervis Ellison","Sam Mitchell","Matt Bullard","Don Nelson","Andre Iguodala","Shawn Kemp","Stan Stutz","Antonio McDyess","Eric Maynor","Wayne Embry","Jack Marin","Aaron Gray","Kevin Garnett","Luke Jackson","Arnie Ferrin","J.J. Redick","Hal Greer","Caldwell Jones","Fat Lever","Reggie Jackson","Harold Pressley","Walt Wesley","Vince Carter","Harrison Barnes","Troy Hudson","Fred VanVleet","Don Buse","Mason Plumlee","Cliff Hagan","Edmund Lawrence","Travis Best","Dennis Scott","Kevin McHale","Buck Williams","Dominique Wilkins","Michael Jordan","Rich Rinaldi","Johnny Moore","Ramon Sessions","Alvin Scott","Elston Turner","Brian Skinner","David Wesley","John Stockton","Wesley Matthews","Gerald Wallace","Pete Chilcutt","Scottie Pippen","Andrew Lang","Jim King","Jamaal Wilkes","Scott Brooks","Jack Rocker","Jason Smith","Howard Porter","Dontonio Wingfield","Gar Heard","Al Eberhard","Dike Eddleman","Zach Randolph","John Janisch","Paul Millsap","Bob Elliott","Tyler Hansbrough","Willie Norwood","Purvis Short","Jesse Branson, Geoff Crompton, JamesOn Curry","Chris Ford","Bill Bridges","Bill Gabor","Stacey King","Bud Koper","Pat Cummings","Wally Walker","Khris Middleton","Tony Delk","Bailey Howell","Anthony Roberts","Dell Curry","Sam Dekker","James Johnson","Mario Chalmers","Wesley Person","Theo Ratliff","Jim Farmer","Emanuel Terry","Leon Douglas","Keith Askins","Bayard Forrest","Chuck Hayes","Kenny Sears","Jabari Bird","Jordan Williams","Tom Hammonds","Vernon Maxwell","Larry Sanders","Kwame Brown","Horace Grant","Doug Collins","Jerry Sloan","Jack Sikma","Brian Cook","Walt Kirk","Jerry Nagel, Joe Ruklick","Gary Phillips","Jared Jeffries","Dick Atha, Carl Shaeffer","Kent Benson","Kyle Macy","John Logan","Melvin Sanders","Odie Spears","Clem Haskins","Donnie Butcher","Bubba Wells","Joe Holland","Kenny Rollins","Paul Thompson","Mike Sanders","Marcus Fizer","Karl Malone","James Silas","David Benoit","Jackie Moreland","Shawn Long","Tal Skinner","Shayne Whittington","Don Boven","Deyonta Davis","Dan Majerle","Trevor Winter","Mark Olberding","Harold Kottman","Chico Vaughn","Earnie Killum","Brad Daugherty","Mitchell Wiggins","Bob Warlick","Sam Jones","Delaney Rudd","Eric Piatkowski","Daniel Santiago","Luke Babbitt","Don Otten","Neil Johnston","Larry Siegfried","Frankie Baumholtz","Dick Schnittker","Mark Price","Aubrey Davis","Danny Ainge","Essie Hollis","George Senesky","Donyell Marshall","Trevor Booker","Harold Jamison","Bob Harris","Jake Carter","Bill Closs","Kenny Thomas","Frank Gates","John Hargis","Terry Davis","Justin Anderson","Rod Derline","Luke Ridnour","Marvin Williams","Chuck Mencel","Bill Hanzlik","Tom Black","Mike D'Antoni","Moe Radovich","Carlos Boozer","Robert Horry","Rory White","John Drew","Jamario Moon","Bud Stallworth","Travis Grant","Jimmy Oliver","Jeff Martin","Jim Barnes","Ron Moore","Tom Patterson","James Anderson","Ronnie Brewer","Paul Silas","Malik Monk","Corliss Williamson","Bill Stricker","Isaac Austin","Darrell Brown","Pete Verhoeven","Gerald Madkins","Orlando Johnson","Josh Akognon","Phil Jordon","Artis Gilmore","Jonathan Isaac","Will Perdue","Clemon Johnson","Frankie King","Tony Mitchell","Jumaine Jones","Donnell Harvey","Wayne Cooper","Greg Minor","Tree Rollins","Jordan McRae","Mike Glenn","Darrell Lockhart","Charlie Ward","Dale Davis","Al Thornton","Red Rocha","Brett Szabo","Raef LaFrentz","Barry Yates","Nick Collison","Loren Meyer","Dave Gunther","Kevin Kunnert","Matt Fish","Dean Oliver","Kyle Korver","Ryan Bowen","Kirk Hinrich","Steve Hayes","Gary Freeman","Dale Wilkinson","Andy Toolson","Keita Bates-Diop","Brian Cardinal","Rex Morgan","Meyers Leonard","Gene Vance","Ed Dahler","Lew Hitch","Archie Dees","Keon Clark","Dave Scholz","Kim Hughes","Dan Godfread","Fran Curran","Johnny Orr","Jack Turner","Larry Bird","Tommy Kron","Steve Green","Darrell Elston","Earl Gardner","Ward Williams","Ralph Johnson","Brad Miller","Scott Skiles","Scott Hastings","Willie Cauley-Stein","Otto Schnellbacher","Ron Baker","Dick Knostman","Steve Henson","Semi Ojeleye","Paul Shirley","Bob Brannum","Butch Beard","Greg Smith","Blackie Towery","Wah Wah Jones","Clarence Glover","Ralph Davis","Joe Fulks","Jack Coleman","John Oldham","Johnny Cox","Jack Tingle","Larry Johnson","Virgil Vaughn","Frank Ramsey","Adrian Smith","Darius Miller","Dan Swartz","Tex Ritter","Reggie Hanson","Ervin Johnson","Bob Hopkins","Elvin Hayes","Mel McGaha","P.J. Brown","Nikita Wilson","Mark Davis","Joe Dumars","Harvey Marlatt","Nate Huffman","Matt Costello","Paul Griffin","Phil Martin","Whitey Skoog","Doug Bolstorff","Arnie Johnson","Jeff Nordgaard","Vern Mikkelsen","Randy Breuer","Clint Wager","Steven Hill","John Brown","OG Anunoby","Scott Sims","Don Anielak","Chris Carr","Norm Stewart","Win Wilfong","Joe Kleine","Tyronn Lue","Kim Anderson","Otto Porter","Anthony Tolliver","Johnny O'Bryant","Clarence Weatherspoon","Larry Smith","Sam Lacey","Terry Catledge","Spencer Haywood","Al Jefferson","Erick Dampier","Dwayne Whitfield","Slick Watts","John Stroud","George Johnson","Kenny Payne","Mike Green","Jonathan Bender","Travis Outlaw","Michael Phelps","Jim Ware","Josh Huestis","Jack Cotton","Ed Kalafat","Ray Kuka","Larry Krystkowiak","Kenny Williams","Belus Smawley","Mike Evans","Dave Henderson","Walt Bellamy","Tom Burleson","Kent Bazemore","Jerrod Mustaf","M.L. Carr","Blue Edwards","Harthorne Wingo","Chris King","Brian Rowsom","Mel Gibson","David Thompson","Jamie Watson","Les Jepsen","Phil Jackson","Glenn Hansen","Alex Stivrins","Tom Kropp","Matt Bonner","Alex Kirk","Chick Halbert","Jimmer Fredette","Tyler Lydon","George Carter","Maurice Martin","Rick Carlisle","John Schweitz","Lou Spicer","Dave Sorenson","Bob Brown","John McCullough","Don Grate","Evan Eschmeyer","Kevin Martin","Bob Priddy","Cecil Hankins","Claude Overton","Ken Corley","Mel Counts","Dave Gambee","Kyle Singler","Josh Davis","Joe Colone","Sam Bowie","Herschel Baltimore","Tom McMillen","Bob Weiss","John Barr","Alize Johnson","Cozell McQueen","Mikki Moore","Garland O'Shields","Ray Allen","Raymond Felton","Mike Gibson","Clifford Ray","Ray Ellefson","Mike Miller","Jared Reiner","Todd Mundt","Marcus Haislip","Popeye Jones","Dan King","Bob Hogsett","Andrae Patterson","Gene Wiley","LaBradford Smith","Tom Barker","Adrian Caldwell","Wesley Johnson","Bob Burrow","Craig Ehlo","Jim Spruill","Bob Carpenter","Kenrich Williams","John Barber","Grady Lewis","Carlton McKinney","Chris Andersen","Mike Harris","Howie Shannon","Price Brookfield","Terry Teagle","Zelmo Beaty","Jack Maddox","Shawn Bradley","Ariel Maughan","Johnny Newman","Ralph Sampson","Linton Townes","Bryant Stith","Jim Palmer","Jerome Kersey","Erick Green","Byron Beck","Gene Conley","Mark Hendrickson","John Greig","Bernie Fryer","Red Morrison","Joe Harris","John Stroeder","Jacob Wiley","Paul Cloyd","Greg Stiemsma","Travis Diener","Tony Bennett","Logan Vander Velden","Wayne Kreklow","Frank Schade","Henry Ellenson","Mel Peterson","Tamar Slay","Bob Wilson","Bimbo Coles","Ron Williams","Rod Thorn","Floyd Volker","Kenny Sailors","Vern Gardner"]],"container":"<table class=\"cell-border nowrap\">\n  <thead>\n    <tr>\n      <th>State(s)<\/th>\n      <th>Area<\/th>\n      <th>Players<\/th>\n      <th>Most Games<\/th>\n      <th>Most WS<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"dom":"tpl","columnDefs":[{"className":"dt-right","targets":2},{"name":"State(s)","targets":0},{"name":"Area","targets":1},{"name":"Players","targets":2},{"name":"Most Games","targets":3},{"name":"Most WS","targets":4}],"order":[],"autoWidth":false,"orderClasses":false}},"evals":[],"jsHooks":[]}</script>

In the table above, we look at the metro areas that have produced the most NBA players. All cities/counties with at least one player that also played at least one regular season game are included. The “Most Games” and “Most WS” columns denote the players with the most regular season games and career Win Shares, respectively. The results are not surprising, with the most populous cities producing the most NBA players. The New York City metro area—which is made up of counties from New York, New Jersey, and Pennsylvania—has put nearly 450 players into the NBA. This is 200 more than either Los Angeles or Chicago, which have produced the second and third most pros. New York, Los Angeles, and Chicago are also the three most populous CBSAs as of the 2010 Census. Pittsburgh is the highest ranked city that is currently without an NBA team, last hosting the ABA’s Condors in 1972. Only two cities in the top 25—Riverside, California and Columbus, Ohio—have never been home to a major professional basketball franchise (NBA, BAA, or ABA).

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-4-1.png" width="816" style="display: block; margin: auto;" />

Next we will look at how the impact of some of the major cities on the NBA has changed throughout the league’s history. This is done by breaking down the percent of all players in the league that call each city home for every season (i.e., for each season, divide the number of players in the league from that city by the total number of players in the NBA that appeared in at least one game). The results for the top 15 cities are plotted, along with LOESS smoothers in blue to help cut out some of the noise.

Immediately noticeable from the graph is the decline in influence of New York City on the NBA. The metro started off accounting for about 20% of all league players for most of the 1950s, a greater percentage than any other city in any era. That influence has declined every year since, dropping to about 10% to 15% in the 1960s and 1970s to just over 5% in the 2010s. Despite that continuous decline, they still led the league in total players nearly every year until this last decade when Los Angeles took the lead. Los Angeles has slowly risen in percent of league players and has had the most players in the NBA every season since 2009 (except for 2013 when New York retook the lead for that single season). Other risers include Atlanta and Dallas, although both cities also had large population growth during this time. Decliners include St. Louis and Pittsburgh which each had a higher proportion of players in 1950s and 1960s but have had weaker numbers compared to other major cities every decade since.

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-5-1.png" width="816" style="display: block; margin: auto;" />

The general decrease in percentage of players by city is the result of the spread of basketball internationally. A few large U.S. metros no longer have a monopoly in producing talent like they did in the 1950s. The number of NBA players with a non-U.S. hometown has increased nearly every season since the 1980s. There were only three players international players in the BAA’s inaugural season in 1947: Norm Baker of Victoria, British Columbia, Canada and both Hank Biasatti and Gino Sovran of Windsor, Ontario, Canada. All three had careers that lasted just that one season, and there would be no players with confirmed international hometowns in the NBA from 1948 to 1978. The international surge started with the 1979 season, seeing the debuts of Lars Hansen out of Coquitlam, British Columbia and Mychal Thompson out of The Bahamas. As of the 2019 season, international players made up about 20% of the players.

## Per Capita Rates

Earlier we saw that the areas that produced the most players are also the areas with the largest populations. We can control for this by scaling the counts from each city by population, giving per capita rates. The simplest way of doing this is by dividing the total number of players from each city by their respective populations and then multiplying by 100,000 to give the number of NBA players per 100,000 people. This is only a rough estimate because populations are not constant over time. Cities grow and shrink, doing so at different rates. Better estimates can be obtained if we take advantage of the fact that there is a Census every ten years. We obtain Census numbers for U.S. counties from 1950 to 2010. There are some issues with counties changing borders, but these effects will be ignored for simplicity. Players will be assigned to the closest Census of their debut season: the 1946-47 to 1954-55 seasons will use the 1950 Census, the 1955-56 to 1964-65 seasons will use the 1960 Census, and so on. The 2014-15 to 2018-19 seasons will use the 2010 Census because the 2020 Census does not yet exist.

For each census, the number of players that made their NBA debut are divided by the population and then multiplied by 100,000. For each area, the mean of these numbers for all seven Censuses is taken, resulting in the average number of NBA players debuting per 100,000 people every 10 years. We start off by looking at the cities with the highest average debuts per 100,000. Note that cities are filtered to those that have produced at least four players, removing inflated rates from cities that have tiny populations but have produced few players. The “Earliest” column shows the first season in which the city had a player debut in the NBA; the “Latest” column shows the most recent season.

<div class="datatables html-widget html-fill-item" id="htmlwidget-2" style="width:100%;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-2">{"x":{"filter":"none","vertical":false,"caption":"<caption style=\"caption-side: bottom; text-align: center;\">* Per 100,000<\/caption>","data":[["Washington, IN","Desha County, AR","Kinston, NC","Jasper, IN","Washington, NC","Muncie, IN","Warsaw, IN","Racine, WI","Macon, GA","Jackson, MS","London, KY","Cleveland, TN","Niles, MI","Flint, MI","Meridian, MS","Monroe, LA","Owensboro, KY","Indianapolis, IN","Elkhart, IN","Lexington, KY","Baton Rouge, LA","Fort Wayne, IN","Boulder, CO","Memphis, TN","Ames, IA","Terre Haute, IN","Las Vegas, NV","Springfield, OH","Ocala, FL","Saginaw, MI","Toledo, OH","Dayton, OH","Trenton, NJ","Louisville, KY","Carbondale, IL","Canton, OH","Chicago, IL","Rocky Mount, NC","Wheeling, WV","Altoona, PA","Washington, DC","South Bend, IN","Ogden, UT","Philadelphia, PA","Richmond, VA","Akron, OH","New York, NY","Montgomery, AL","Springfield, IL","Clarksville, TN","Birmingham, AL","Winston, NC","Wilmington, NC","Charleston, WV","San Francisco, CA","Los Angeles, CA","Detroit, MI","Cincinnati, OH","Evansville, IN","Lansing, MI","Columbus, OH","Little Rock, AR","Santa Maria, CA","Atlanta, GA","Lake Charles, LA","Milwaukee, WI","Wichita, KS","Savannah, GA","Provo, UT","Pittsburgh, PA","Oklahoma City, OK","Durham, NC","Hagerstown, MD","Beaumont, TX","Roanoke, VA","Cape Coral, FL","Peoria, IL","New Orleans, LA","Minneapolis, MN","Bakersfield, CA","Shreveport, LA","Kansas City, MO","Harrisburg, PA","Portland, OR","Raleigh, NC","Columbus, GA","Norwich, CT","Pensacola, FL","Fresno, CA","Colorado Springs, CO","Lakeland, FL","Longview, TX","St. Louis, MO","Myrtle Beach, SC","Houston, TX","Baltimore, MD","Omaha, NE","Gulfport, MS","Nashville, TN","Riverside, CA","Rockford, IL","Dallas, TX","Columbia, SC","Hartford, CT","Bridgeport, CT","Seattle, WA","Charlotte, NC","Buffalo, NY","Rochester, NY","San Jose, CA","Tulsa, OK","Scranton, PA","Greensboro, NC","Huntington, WV","Augusta, GA","Davenport, IA","Duluth, MN","Des Moines, IA","Cleveland, OH","Salt Lake City, UT","Phoenix, AZ","Virginia Beach, VA","Mobile, AL","Fayetteville, NC","Syracuse, NY","Jacksonville, FL","Grand Rapids, MI","Denver, CO","Orlando, FL","Killeen, TX","San Diego, CA","San Antonio, TX","Providence, RI","Boston, MA","Sacramento, CA","Spokane, WA","New Haven, CT","Albany, NY","Greenville, SC","Madison, WI","Miami, FL","Youngstown, OH","Allentown, PA","Deltona, FL","Austin, TX","Tampa, FL","Knoxville, TN","Worcester, MA","Poughkeepsie, NY","Springfield, MA","Tucson, AZ"],[28119.57142857143,18513.28571428571,56095.57142857143,46618.28571428572,40640.42857142857,116442.1428571429,56823.71428571428,164944.1428571429,194406.8571428571,451449.2857142857,121181.4285714286,78222.57142857143,154480.2857142857,404636.5714285714,101329.1428571429,177244.1428571429,98180.14285714286,1366490.714285714,141672.7142857143,314494.7142857143,575838,308537.7142857143,179322.5714285714,997841.4285714285,94150.14285714286,188235.5714285714,711453.2857142857,140153.5714285714,152338.2857142857,202031.8571428571,624333.1428571428,747061.2857142857,307300.2857142857,960582.4285714285,119003.2857142857,381015.2857142857,7922823.714285715,127148.2857142857,173621.1428571429,133648,3620490.714285714,288668.2857142857,342485.4285714286,5196522.428571428,818979.7142857143,639236.4285714285,16591164.71428571,284509.8571428572,179553.7142857143,176150.5714285714,859702.4285714285,445189.4285714286,143455.4285714286,305598.1428571428,3327224,9348780.571428571,4128906.285714286,1752326.285714286,270298.5714285714,447350.2857142857,1343391.571428571,479801.4285714286,289007.1428571428,2758944,164142.8571428571,1368955.714285714,477670.4285714286,244083.5714285714,248351.1428571429,2573475.714285714,856095.7142857143,355169.7142857143,179270.8571428571,348903.8571428572,248212.8571428571,254740,395471,1145525.285714286,2320912.285714286,471042.4285714286,336763.1428571428,1511445.142857143,439809.8571428572,1393018.285714286,526017.4285714285,267856.7142857143,226774.7142857143,296149,566783,338977,337058.7142857143,216383.1428571429,2452989.571428571,177218,3196465.285714286,2175193.142857143,652714.2857142857,282412.2857142857,1011668,2004466.142857143,272068.1428571428,3423554.285714286,496812.5714285714,1010019.285714286,769275.5714285715,2216872.857142857,1303583.142857143,1211876,950497.4285714285,1210378.285714286,681335.7142857143,593878.4285714285,503034.5714285714,349294,392992,363097.4285714286,296657.1428571428,443449.4285714286,2090017.285714286,656462.4285714285,1917113.571428571,1266410.857142857,362227.1428571428,321653.4285714286,611566.8571428572,806375,717916.4285714285,1480785.571428571,987971.7142857143,232589.5714285714,1888097.285714286,1252721,1419700,3948246.142857143,1200264.857142857,368161.8571428572,743298.2857142857,759452.1428571428,560317.8571428572,421141.1428571428,3182370.285714286,610029.8571428572,645471.4285714285,304853.4285714286,764882,1603309,603815,758624.5714285715,493759.2857142857,632867.5714285715,540125],[2.940651462175181,2.891844997108155,1.457403531892533,1.377523269920788,1.290102389615672,1.037902886627006,0.9078537505408957,0.9076522732331824,0.8570076353618747,0.824754946020704,0.8089856743361545,0.7847243176679976,0.7009251522535436,0.6886234958425614,0.6778466234775037,0.676658675056489,0.6091798547151909,0.6023782067163492,0.5986342799350769,0.5925382939087172,0.5873715704665311,0.5847516625989202,0.5583621803628692,0.5490403534222177,0.5411979834722632,0.5350953494730353,0.5193999659139227,0.5156815945399064,0.4965342376293291,0.4768233146573881,0.4743890999781669,0.4733066658592115,0.4728736945957001,0.4713903632938083,0.4692716270809119,0.4675217184012223,0.4437256848220942,0.4417762946040287,0.4389181427188382,0.4340507564807986,0.4145281136633797,0.4086500476614604,0.408268806159614,0.4075959302380658,0.4072485458603702,0.4032165428737268,0.4003913349764503,0.3991572706774138,0.3960071632994571,0.3878198595664468,0.3802759155601463,0.3662159837450517,0.3612856786114366,0.3575403985587371,0.3550435883786365,0.3513423024437424,0.348261575922115,0.3427840055371224,0.3350267791719992,0.3302850640933663,0.3215827961930769,0.3196746744689847,0.3157789245995894,0.3149593410334315,0.3068140833669132,0.2979564390730055,0.2947960939227579,0.2920129875438343,0.2904086692369214,0.2889479040581991,0.2885854848193815,0.2883031641315212,0.2850429769697547,0.2819627853980647,0.2813317122961825,0.2804029017063902,0.2788117001277235,0.2753090247777205,0.2728883553579697,0.2691380999691021,0.268739513927815,0.2679950039145779,0.2669297942340279,0.266826890779254,0.2650581688236943,0.2626387700235435,0.2619414428094542,0.2611592891715179,0.2603679944441937,0.2601488209206042,0.257402580985727,0.257291969417863,0.2566751914830314,0.2532143262059802,0.2514617329088573,0.2505117708435107,0.2503497241058594,0.2450726544099419,0.2436006438319322,0.2408825034941564,0.2280471490793085,0.2253764229848843,0.224325624913399,0.2239539577309534,0.2229869069049218,0.2199214149541195,0.2197690842005854,0.2161671087333234,0.2157692556761471,0.2104751674046395,0.2095892071285872,0.2052534068671599,0.2046789404563801,0.2045060206764567,0.1994049024060455,0.1944721507200365,0.1912300296608462,0.1879088477238593,0.1858954657245965,0.1783141042156451,0.1778771343775058,0.1766732013682191,0.1708548069401019,0.170145727202586,0.1653982755410192,0.1635429715990677,0.1631794794892366,0.1541104203153701,0.1498190071730428,0.1489383601720345,0.1449551473840121,0.1438934327863796,0.1364930187278888,0.1339207807769349,0.1296379231761359,0.1283335627819677,0.1265587363815443,0.1251408930365424,0.1224891710375908,0.1208213114315153,0.118646669821111,0.1170198197906721,0.1149491420739476,0.1131360403258639,0.1113070379726989,0.1068847076573941,0.09939426204576898,0.09719416415267143,0.09611567178629327,0.09134802763446224,0.08429777201971204],[6,4,6,4,4,8,4,10,12,27,6,4,7,21,5,9,4,55,5,12,26,10,5,44,4,7,15,5,5,7,20,25,10,32,4,13,239,4,6,4,118,8,5,149,26,17,444,9,5,6,24,12,4,8,74,243,104,40,6,11,30,12,6,82,4,30,10,5,8,53,20,7,4,7,5,4,8,23,40,9,7,28,8,31,14,5,4,6,13,4,9,4,43,4,62,43,12,6,17,34,4,69,9,16,12,40,25,18,14,16,12,9,8,5,7,5,4,5,27,8,21,19,5,5,7,10,9,17,17,4,23,15,13,39,14,4,7,7,5,4,32,5,5,4,5,16,4,5,4,4,4],[1949,1977,1978,1948,1983,1950,1960,1947,1950,1962,1947,1950,1948,1973,1985,1965,1955,1947,1947,1948,1950,1949,1947,1969,1972,1950,1949,1957,1978,1980,1947,1948,1947,1950,1959,1961,1947,1979,1949,1981,1951,1948,1947,1947,1959,1947,1947,1976,1949,1977,1966,1956,1981,1949,1947,1947,1947,1949,1953,1947,1947,1962,1963,1963,1981,1949,1954,1950,1981,1947,1953,1947,1976,1954,1952,1967,1979,1950,1947,1969,1977,1948,1949,1961,1973,1971,1947,1956,1960,1947,1978,1971,1947,1980,1950,1950,1961,1991,1950,1947,1950,1949,1975,1949,1947,1947,1977,1948,1953,1953,1986,1947,1967,1950,1990,1963,1947,1950,1947,1947,1948,1978,1987,1972,1952,1964,1955,1957,1976,1999,1966,1949,1947,1947,1977,1985,1973,1965,1971,1960,1966,1947,1947,1990,1964,1963,1963,1947,1972,1948,1983],[2014,1984,2017,1977,2018,1999,2017,2018,2006,2009,1959,2003,2008,2019,2015,2006,1989,2019,1991,2012,2019,2018,2007,2019,2015,1997,2019,2001,1993,2013,2018,2015,2018,2019,2012,2014,2019,2016,1963,1998,2019,2017,2005,2019,2019,2016,2019,2015,2005,2017,2018,2019,2018,1999,2018,2019,2019,2019,1997,2017,2019,2019,2012,2019,2018,2019,2002,2017,2019,2016,2019,2018,2019,2004,2014,2003,2018,2019,2019,2018,2019,2019,2001,2019,2019,1990,2017,2019,2012,2012,2018,1998,2018,2008,2019,2019,2019,2014,2013,2018,2017,2019,2018,2018,2018,2019,2018,2018,2018,2015,2019,1996,2019,2011,2018,2017,1981,1991,2019,2008,2019,2017,2011,2019,2018,2019,2016,2018,2019,2018,2018,2017,2019,2019,2018,2015,2006,2019,1999,2014,2018,2016,2016,2008,2018,2019,1990,2002,2017,2003,2015]],"container":"<table class=\"cell-border nowrap\">\n  <thead>\n    <tr>\n      <th>Area<\/th>\n      <th>Avg Population<\/th>\n      <th>Avg Debuts Per Census*<\/th>\n      <th>Total<\/th>\n      <th>Earliest<\/th>\n      <th>Latest<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"dom":"tpl","columnDefs":[{"targets":2,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":1,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 0, 3, \",\", \".\", null);\n  }"},{"className":"dt-right","targets":[1,2,3,4,5]},{"name":"Area","targets":0},{"name":"Avg Population","targets":1},{"name":"Avg Debuts Per Census*","targets":2},{"name":"Total","targets":3},{"name":"Earliest","targets":4},{"name":"Latest","targets":5}],"order":[],"autoWidth":false,"orderClasses":false}},"evals":["options.columnDefs.0.render","options.columnDefs.1.render"],"jsHooks":[]}</script>

Washington, Indiana finishes atop the list, putting 6 players into the NBA with an average population of only 28,120 from 1950 to 2010. This results in an average of nearly 3 players per 100,000 residents every 10 years. This result is slightly less impressive when we look into the players from
the city:

<table class="table" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>
<span id="tab:unnamed-chunk-8"></span>Table 1: (#tab:unnamed-chunk-8)Players from Washington, Indiana
</caption>
<thead>
<tr>
<th style="text-align:left;">
Player
</th>
<th style="text-align:right;">
From
</th>
<th style="text-align:right;">
To
</th>
<th style="text-align:left;">
City
</th>
<th style="text-align:left;">
State
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
Leo Klier
</td>
<td style="text-align:right;">
1949
</td>
<td style="text-align:right;">
1950
</td>
<td style="text-align:left;">
Washington
</td>
<td style="text-align:left;">
IN
</td>
</tr>
<tr>
<td style="text-align:left;">
Jim Riffey
</td>
<td style="text-align:right;">
1951
</td>
<td style="text-align:right;">
1951
</td>
<td style="text-align:left;">
Washington
</td>
<td style="text-align:left;">
IN
</td>
</tr>
<tr>
<td style="text-align:left;">
Craig Neal
</td>
<td style="text-align:right;">
1989
</td>
<td style="text-align:right;">
1991
</td>
<td style="text-align:left;">
Washington
</td>
<td style="text-align:left;">
IN
</td>
</tr>
<tr>
<td style="text-align:left;">
Luke Zeller
</td>
<td style="text-align:right;">
2013
</td>
<td style="text-align:right;">
2013
</td>
<td style="text-align:left;">
Washington
</td>
<td style="text-align:left;">
IN
</td>
</tr>
<tr>
<td style="text-align:left;">
Tyler Zeller
</td>
<td style="text-align:right;">
2013
</td>
<td style="text-align:right;">
2019
</td>
<td style="text-align:left;">
Washington
</td>
<td style="text-align:left;">
IN
</td>
</tr>
<tr>
<td style="text-align:left;">
Cody Zeller
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:right;">
2019
</td>
<td style="text-align:left;">
Washington
</td>
<td style="text-align:left;">
IN
</td>
</tr>
</tbody>
</table>

The Zeller brothers—Luke, Tyler, and Cody—make up half of all the NBA pros from Washington. Two others, Leo Klier and Jim Riffey, were BAAers with short careers. All six went to Washington High School, but the Zeller brothers each ended up at different colleges. The same applies to the next area on the list: Desha County, Arkansas.

<table class="table" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>
<span id="tab:unnamed-chunk-9"></span>Table 3: (#tab:unnamed-chunk-9)Players from Desha County, Arkansas
</caption>
<thead>
<tr>
<th style="text-align:left;">
Player
</th>
<th style="text-align:right;">
From
</th>
<th style="text-align:right;">
To
</th>
<th style="text-align:left;">
City
</th>
<th style="text-align:left;">
State
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
Caldwell Jones
</td>
<td style="text-align:right;">
1977
</td>
<td style="text-align:right;">
1990
</td>
<td style="text-align:left;">
McGehee
</td>
<td style="text-align:left;">
AR
</td>
</tr>
<tr>
<td style="text-align:left;">
Wil Jones
</td>
<td style="text-align:right;">
1977
</td>
<td style="text-align:right;">
1978
</td>
<td style="text-align:left;">
McGehee
</td>
<td style="text-align:left;">
AR
</td>
</tr>
<tr>
<td style="text-align:left;">
Major Jones
</td>
<td style="text-align:right;">
1980
</td>
<td style="text-align:right;">
1985
</td>
<td style="text-align:left;">
McGehee
</td>
<td style="text-align:left;">
AR
</td>
</tr>
<tr>
<td style="text-align:left;">
Charles Jones
</td>
<td style="text-align:right;">
1984
</td>
<td style="text-align:right;">
1998
</td>
<td style="text-align:left;">
McGehee
</td>
<td style="text-align:left;">
AR
</td>
</tr>
</tbody>
</table>

Brothers Wil, Caldwell, Major, and Charles Jones were all born in McGehee, graduated high school at Desha Central, played college basketball at Albany State in Georgia, and finally drafted into the NBA. The siblings make up the NBA’s only pros out of Desha County. The list gets more interesting with Kinston, North Carolina.

<table class="table" style="width: auto !important; margin-left: auto; margin-right: auto;">
<caption>
<span id="tab:unnamed-chunk-10"></span>Table 5: (#tab:unnamed-chunk-10)Players from Kinston, North Carolina
</caption>
<thead>
<tr>
<th style="text-align:left;">
Player
</th>
<th style="text-align:right;">
From
</th>
<th style="text-align:right;">
To
</th>
<th style="text-align:left;">
City
</th>
<th style="text-align:left;">
State
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
Cedric Maxwell
</td>
<td style="text-align:right;">
1978
</td>
<td style="text-align:right;">
1988
</td>
<td style="text-align:left;">
Kinston
</td>
<td style="text-align:left;">
NC
</td>
</tr>
<tr>
<td style="text-align:left;">
Charles Shackleford
</td>
<td style="text-align:right;">
1989
</td>
<td style="text-align:right;">
1999
</td>
<td style="text-align:left;">
Kinston
</td>
<td style="text-align:left;">
NC
</td>
</tr>
<tr>
<td style="text-align:left;">
Tony Dawson
</td>
<td style="text-align:right;">
1991
</td>
<td style="text-align:right;">
1995
</td>
<td style="text-align:left;">
Kinston
</td>
<td style="text-align:left;">
NC
</td>
</tr>
<tr>
<td style="text-align:left;">
Jerry Stackhouse
</td>
<td style="text-align:right;">
1996
</td>
<td style="text-align:right;">
2013
</td>
<td style="text-align:left;">
Kinston
</td>
<td style="text-align:left;">
NC
</td>
</tr>
<tr>
<td style="text-align:left;">
Reggie Bullock
</td>
<td style="text-align:right;">
2014
</td>
<td style="text-align:right;">
2019
</td>
<td style="text-align:left;">
Kinston
</td>
<td style="text-align:left;">
NC
</td>
</tr>
<tr>
<td style="text-align:left;">
Brandon Ingram
</td>
<td style="text-align:right;">
2017
</td>
<td style="text-align:right;">
2019
</td>
<td style="text-align:left;">
Kinston
</td>
<td style="text-align:left;">
NC
</td>
</tr>
</tbody>
</table>

[Kinston](http://www.espn.com/espn/feature/story/_/id/22467698/how-kinston-north-carolina-became-greatest-producer-nba-talent-america), with a population of close to 60,000, has produced six NBA players since 1978. This group does include one pair of brothers in Tony Dawson and Jerry Stackhouse. Dawson played two seasons in the NBA, appearing in four games in 1991 and two games in 1995. The rest have had mostly substantial careers. Cedric Maxwell won two championships with the Celtics, including the Finals MVP award in 1981. Charles Shackleford logged 303 games over 6 seasons for 4 different teams. Jerry Stackhouse was a 2 time All-Star over a 18 year career. Reggie Bullock and Brandon Ingram are still active NBA players as of the 2020 NBA season. One more Kinston product, Herbert Hill, was drafted but never played a game. All players attended Kinston High School (Stackhouse later transfered to basketall factory Oak Hill Academy). Mitchell Wiggins, the father of the 2014 NBA draft’s number one pick Andrew Wiggins, is from Grifton, North Carolina and played six seasons in the league all while battling substance abuse issues. Grifton can be grouped into either the Greenville Metropolitan area or the Kinston Micropolitan area depending on the exact coordinates in the city. Our data groups Grifton into Greenville, but the city could very well have been included with Kinston, highlighting a weakness with our dataset.

The list of areas with the highest per capita rates is dominated by cities and counties with small populations. We look at areas with average populations of at least 250,000 since 1950:

<div class="datatables html-widget html-fill-item" id="htmlwidget-3" style="width:100%;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-3">{"x":{"filter":"none","vertical":false,"caption":"<caption style=\"caption-side: bottom; text-align: center;\">* Per 100,000<\/caption>","data":[["Jackson, MS","Flint, MI","Indianapolis, IN","Lexington, KY","Baton Rouge, LA","Fort Wayne, IN","Memphis, TN","Las Vegas, NV","Toledo, OH","Dayton, OH","Trenton, NJ","Louisville, KY","Canton, OH","Chicago, IL","Washington, DC","South Bend, IN","Ogden, UT","Philadelphia, PA","Richmond, VA","Akron, OH","New York, NY","Montgomery, AL","Birmingham, AL","Winston, NC","Charleston, WV","San Francisco, CA","Los Angeles, CA","Detroit, MI","Cincinnati, OH","Evansville, IN","Lansing, MI","Columbus, OH","Little Rock, AR","Santa Maria, CA","Atlanta, GA","Milwaukee, WI","Wichita, KS","Pittsburgh, PA","Oklahoma City, OK","Durham, NC","Beaumont, TX","Cape Coral, FL","Peoria, IL","New Orleans, LA","Minneapolis, MN","Bakersfield, CA","Shreveport, LA","Kansas City, MO","Harrisburg, PA","Portland, OR","Raleigh, NC","Columbus, GA","Pensacola, FL","Fresno, CA","Colorado Springs, CO","Lakeland, FL","St. Louis, MO","Houston, TX","Baltimore, MD","Omaha, NE","Gulfport, MS","Nashville, TN","Riverside, CA","Rockford, IL","Dallas, TX","Columbia, SC","Hartford, CT","Bridgeport, CT","Seattle, WA","Charlotte, NC","Buffalo, NY","Rochester, NY","Ann Arbor, MI","San Jose, CA","Tulsa, OK","Scranton, PA","Greensboro, NC","Huntington, WV","Augusta, GA","Davenport, IA","Visalia, CA","Duluth, MN","Des Moines, IA","Cleveland, OH","Binghamton, NY","Salt Lake City, UT","Phoenix, AZ","Virginia Beach, VA","Mobile, AL","Fayetteville, NC","Syracuse, NY","Jacksonville, FL","Grand Rapids, MI","Denver, CO","Orlando, FL","San Diego, CA","San Antonio, TX","Providence, RI","Boston, MA","Sacramento, CA","Spokane, WA","Lancaster, PA","New Haven, CT","Albany, NY","Greenville, SC","Madison, WI","Miami, FL","Youngstown, OH","Allentown, PA","Deltona, FL","Hickory, NC","Austin, TX","North Port, FL","Erie, PA","Huntsville, AL","Tampa, FL","Stockton, CA","Knoxville, TN","Worcester, MA","Chattanooga, TN","Poughkeepsie, NY","Springfield, MA","Tucson, AZ","Modesto, CA","Asheville, NC","Boise City, ID","Lafayette, LA","Charleston, SC","Reading, PA","Vallejo, CA","Oxnard, CA","Kingsport, TN","El Paso, TX","Corpus Christi, TX","Albuquerque, NM","Palm Bay, FL","Salinas, CA","Springfield, MO","Santa Rosa, CA","Manchester, NH","McAllen, TX","Portland, ME","Urban Honolulu, HI","Utica, NY","York, PA"],[451449.2857142857,404636.5714285714,1366490.714285714,314494.7142857143,575838,308537.7142857143,997841.4285714285,711453.2857142857,624333.1428571428,747061.2857142857,307300.2857142857,960582.4285714285,381015.2857142857,7922823.714285715,3620490.714285714,288668.2857142857,342485.4285714286,5196522.428571428,818979.7142857143,639236.4285714285,16591164.71428571,284509.8571428572,859702.4285714285,445189.4285714286,305598.1428571428,3327224,9348780.571428571,4128906.285714286,1752326.285714286,270298.5714285714,447350.2857142857,1343391.571428571,479801.4285714286,289007.1428571428,2758944,1368955.714285714,477670.4285714286,2573475.714285714,856095.7142857143,355169.7142857143,348903.8571428572,254740,395471,1145525.285714286,2320912.285714286,471042.4285714286,336763.1428571428,1511445.142857143,439809.8571428572,1393018.285714286,526017.4285714285,267856.7142857143,296149,566783,338977,337058.7142857143,2452989.571428571,3196465.285714286,2175193.142857143,652714.2857142857,282412.2857142857,1011668,2004466.142857143,272068.1428571428,3423554.285714286,496812.5714285714,1010019.285714286,769275.5714285715,2216872.857142857,1303583.142857143,1211876,950497.4285714285,250931.4285714286,1210378.285714286,681335.7142857143,593878.4285714285,503034.5714285714,349294,392992,363097.4285714286,267692.5714285714,296657.1428571428,443449.4285714286,2090017.285714286,252236.7142857143,656462.4285714285,1917113.571428571,1266410.857142857,362227.1428571428,321653.4285714286,611566.8571428572,806375,717916.4285714285,1480785.571428571,987971.7142857143,1888097.285714286,1252721,1419700,3948246.142857143,1200264.857142857,368161.8571428572,372577.1428571428,743298.2857142857,759452.1428571428,560317.8571428572,421141.1428571428,3182370.285714286,610029.8571428572,645471.4285714285,304853.4285714286,264843.2857142857,764882,365648.2857142857,264355,255250.8571428571,1603309,402545.8571428572,603815,758624.5714285715,409927.8571428572,493759.2857142857,632867.5714285715,540125,296700.4285714286,295297.2857142857,311635.8571428572,341522,426253,323092.5714285714,256125.8571428571,494988.5714285714,262210.2857142857,491800.4285714286,316381.5714285714,518418.2857142857,293805.2857142857,291691.8571428572,272320,298008.5714285714,279047.4285714286,361984.4285714286,391904,701537.7142857143,313115.5714285714,311848],[0.824754946020704,0.6886234958425614,0.6023782067163492,0.5925382939087172,0.5873715704665311,0.5847516625989202,0.5490403534222177,0.5193999659139227,0.4743890999781669,0.4733066658592115,0.4728736945957001,0.4713903632938083,0.4675217184012223,0.4437256848220942,0.4145281136633797,0.4086500476614604,0.408268806159614,0.4075959302380658,0.4072485458603702,0.4032165428737268,0.4003913349764503,0.3991572706774138,0.3802759155601463,0.3662159837450517,0.3575403985587371,0.3550435883786365,0.3513423024437424,0.348261575922115,0.3427840055371224,0.3350267791719992,0.3302850640933663,0.3215827961930769,0.3196746744689847,0.3157789245995894,0.3149593410334315,0.2979564390730055,0.2947960939227579,0.2889479040581991,0.2885854848193815,0.2883031641315212,0.2819627853980647,0.2804029017063902,0.2788117001277235,0.2753090247777205,0.2728883553579697,0.2691380999691021,0.268739513927815,0.2679950039145779,0.2669297942340279,0.266826890779254,0.2650581688236943,0.2626387700235435,0.2611592891715179,0.2603679944441937,0.2601488209206042,0.257402580985727,0.2566751914830314,0.2514617329088573,0.2505117708435107,0.2503497241058594,0.2450726544099419,0.2436006438319322,0.2408825034941564,0.2280471490793085,0.2253764229848843,0.224325624913399,0.2239539577309534,0.2229869069049218,0.2199214149541195,0.2197690842005854,0.2161671087333234,0.2157692556761471,0.2105803119119656,0.2104751674046395,0.2095892071285872,0.2052534068671599,0.2046789404563801,0.2045060206764567,0.1994049024060455,0.1944721507200365,0.1926592859466615,0.1912300296608462,0.1879088477238593,0.1858954657245965,0.1802757373292715,0.1783141042156451,0.1778771343775058,0.1766732013682191,0.1708548069401019,0.170145727202586,0.1653982755410192,0.1635429715990677,0.1631794794892366,0.1541104203153701,0.1498190071730428,0.1449551473840121,0.1438934327863796,0.1364930187278888,0.1339207807769349,0.1296379231761359,0.1283335627819677,0.1277910653582051,0.1265587363815443,0.1251408930365424,0.1224891710375908,0.1208213114315153,0.118646669821111,0.1170198197906721,0.1149491420739476,0.1131360403258639,0.1116766582897283,0.1113070379726989,0.1102296261223163,0.1080479226767394,0.1075448487400934,0.1068847076573941,0.09979453936494372,0.09939426204576898,0.09719416415267143,0.09644706671328401,0.09611567178629327,0.09134802763446224,0.08429777201971204,0.08149463572867542,0.08000671862540584,0.07475908883622526,0.07460409472034284,0.07353452710310253,0.07295519332673932,0.07076966870789321,0.06570096674726034,0.05924658487873112,0.05051707453586128,0.04082869179155483,0.03915777116316006,0.03580576945524386,0.03441868053234685,0.03271198017392306,0.0295233804506803,0,0,0,0,0,0],[27,21,55,12,26,10,44,15,20,25,10,32,13,239,118,8,5,149,26,17,444,9,24,12,8,74,243,104,40,6,11,30,12,6,82,30,10,53,20,7,7,4,8,23,40,9,7,28,8,31,14,5,6,13,4,9,43,62,43,12,6,17,34,4,69,9,16,12,40,25,18,14,3,16,12,9,8,5,7,5,3,4,5,27,3,8,21,19,5,5,7,10,9,17,17,23,15,13,39,14,4,3,7,7,5,4,32,5,5,4,2,5,3,2,2,16,3,4,5,3,4,4,4,2,2,1,2,3,2,2,3,1,2,1,2,1,1,1,1,0,0,0,0,0,0],[1962,1973,1947,1948,1950,1949,1969,1949,1947,1948,1947,1950,1961,1947,1951,1948,1947,1947,1959,1947,1947,1976,1966,1956,1949,1947,1947,1947,1949,1953,1947,1947,1962,1963,1963,1949,1954,1947,1953,1947,1954,1967,1979,1950,1947,1969,1977,1948,1949,1961,1973,1971,1956,1960,1947,1978,1947,1950,1950,1961,1991,1950,1947,1950,1949,1975,1949,1947,1947,1977,1948,1953,1950,1953,1986,1947,1967,1950,1990,1963,1948,1947,1950,1947,1950,1947,1948,1978,1987,1972,1952,1964,1955,1957,1976,1966,1949,1947,1947,1977,1985,1950,1973,1965,1971,1960,1966,1947,1947,1990,1966,1964,1972,1955,1982,1963,1973,1963,1947,1978,1972,1948,1983,1977,1987,1971,1991,1998,1995,2002,1975,1967,1975,1990,2000,1989,2013,2009,2013,null,null,null,null,null,null],[2009,2019,2019,2012,2019,2018,2019,2019,2018,2015,2018,2019,2014,2019,2019,2017,2005,2019,2019,2016,2019,2015,2018,2019,1999,2018,2019,2019,2019,1997,2017,2019,2019,2012,2019,2019,2002,2016,2019,2018,2004,2003,2018,2019,2019,2018,2019,2019,2001,2019,2019,1990,2019,2012,2012,2018,2018,2019,2019,2019,2014,2013,2018,2017,2019,2018,2018,2018,2019,2018,2018,2018,1986,2015,2019,1996,2019,2011,2018,2017,2001,1981,1991,2019,2012,2008,2019,2017,2011,2019,2018,2019,2016,2018,2019,2018,2017,2019,2019,2018,2015,2016,2006,2019,1999,2014,2018,2016,2016,2008,1987,2018,2018,1979,1991,2019,2014,1990,2002,1998,2017,2003,2015,2006,2006,1971,1992,2013,2019,2018,2015,1967,2000,1990,2001,1989,2013,2009,2013,null,null,null,null,null,null]],"container":"<table class=\"cell-border nowrap\">\n  <thead>\n    <tr>\n      <th>City<\/th>\n      <th>Avg Population<\/th>\n      <th>Avg Debuts Per Census*<\/th>\n      <th>Total<\/th>\n      <th>Earliest<\/th>\n      <th>Latest<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"dom":"tpl","columnDefs":[{"targets":2,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 2, 3, \",\", \".\", null);\n  }"},{"targets":1,"render":"function(data, type, row, meta) {\n    return type !== 'display' ? data : DTWidget.formatRound(data, 0, 3, \",\", \".\", null);\n  }"},{"className":"dt-right","targets":[1,2,3,4,5]},{"name":"City","targets":0},{"name":"Avg Population","targets":1},{"name":"Avg Debuts Per Census*","targets":2},{"name":"Total","targets":3},{"name":"Earliest","targets":4},{"name":"Latest","targets":5}],"order":[],"autoWidth":false,"orderClasses":false}},"evals":["options.columnDefs.0.render","options.columnDefs.1.render"],"jsHooks":[]}</script>

Jackson, Mississippi has the highest rate among these larger areas, producing 27 NBA players with an average population of about 450,000. The most well-known of these 27 include Lindsey Hunter, Monta Ellis, and Mo Williams. Indianapolis, Indiana is the leading city among populations of at least a million, putting Hall of Famers Oscar Robertson, George McGinnis, and Louie Dampier (though more for his ABA contributions) into the league. One note about this top ten of larger cities is the prevalence of southern and midwest cities.

Some other findings:

- Haskell County, Kansas is the least-populous area to have ever produced an NBA talent. The county put Otto Schnellbacher into the NBA in 1949 despite an average population of 3,647 (and of only 2,606 back in 1950). Burke County, North Dakota, average population 4,040, provides a more recent example with Les Jepsen in 1991.

- Honolulu, Hawaii is the largest metro to have never produced an NBA talent. Even with an average population of over 700,000 since 1950 (and almost a million in 2010), no NBA player has called Honolulu home. The state of Hawaii itself has only produced a single pro—two-time All-Star Red Rocha—whose career spanned 1948 to 1957. Cedric Ceballos, the only other player to have been born in Hawaii, grew up in Los Angeles.

- Maine and Vermont are the only states to not be the homes of any NBA players. Jeff Turner and Duncan Robinson were both born in Maine, but grew up in Florida and New Hampshire, respectively. A number of NBA players attended Pittsfield’s Maine Central Institute, but it a boarding school that attracts athletes. Bruce Brown attended Saxtons River’s Vermont Academy, but he grew up around the Boston area.

## Geographical Distribution

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-13-1.png" width="816" style="display: block; margin: auto;" />

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-15-1.png" width="816" style="display: block; margin: auto;" />

All areas that have produced at least one NBA player are plotted in the maps above. The first plot shows the entire history of the league. The second plot shows results by the decade that players debuted, giving a sense of the changing geographic distribution of hometowns. Notice the concentration of talent in the Mid-Atlantic (mostly the New York area) and eastern part of the Midwest in the 1940s and 1950s. Talent started arriving in the NBA from the South in large numbers beginning with the 1970s. California has become a bigger contributor over time. The less dense Moutain, Southwest, and western Midwest states have continued to stay relatively quiet throughout the NBA’s history.

## Hometown Heroes

<div class="datatables html-widget html-fill-item" id="htmlwidget-4" style="width:100%;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-4">{"x":{"filter":"none","vertical":false,"data":[[2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,2020,1968,1955,1950,1947,1947,1957,1962,1971,1949,1953,1978,1984,1960,2008,1963,1947,1949,1957,1972,1985,1950,1950,1979,1951,1963,1973],["Atlanta Hawks","Boston Celtics","Brooklyn Nets","Charlotte Hornets","Chicago Bulls","Cleveland Cavaliers","Dallas Mavericks","Denver Nuggets","Detroit Pistons","Golden State Warriors","Houston Rockets","Indiana Pacers","Los Angeles Clippers","Los Angeles Lakers","Memphis Grizzlies","Miami Heat","Milwaukee Bucks","Minnesota Timberwolves","New Orleans Pelicans","New York Knicks","Oklahoma City Thunder","Orlando Magic","Philadelphia 76ers","Phoenix Suns","Portland Trail Blazers","Sacramento Kings","San Antonio Spurs","Utah Jazz","Washington Wizards","Atlanta Hawks","Baltimore Bullets (1948-55)","Chicago Stags","Cleveland Rebels","Detroit Falcons","Detroit Pistons","Golden State Warriors","Houston Rockets","Indianapolis Jets","Indianapolis Olympians","Los Angeles Clippers","Los Angeles Clippers","Los Angeles Lakers","Oklahoma City Thunder","Philadelphia 76ers","Pittsburgh Ironmen","Providence Steam Rollers","Sacramento Kings","Sacramento Kings","Sacramento Kings","Sheboygan Red Skins","St. Louis Bombers","Utah Jazz","Washington Capitols","Washington Wizards","Washington Wizards"],["Atlanta Hawks","Boston Celtics","Brooklyn Nets","Charlotte Hornets","Chicago Bulls","Cleveland Cavaliers","Dallas Mavericks","Denver Nuggets","Detroit Pistons","Golden State Warriors","Houston Rockets","Indiana Pacers","Los Angeles Clippers","Los Angeles Lakers","Memphis Grizzlies","Miami Heat","Milwaukee Bucks","Minnesota Timberwolves","New Orleans Pelicans","New York Knicks","Oklahoma City Thunder","Orlando Magic","Philadelphia 76ers","Phoenix Suns","Portland Trail Blazers","Sacramento Kings","San Antonio Spurs","Utah Jazz","Washington Wizards","St. Louis Hawks","Baltimore Bullets","Chicago Stags","Cleveland Rebels","Detroit Falcons","Fort Wayne Pistons","Philadelphia Warriors","San Diego Rockets","Indianapolis Jets","Indianapolis Olympians","Buffalo Braves","San Diego Clippers","Minneapolis Lakers","Seattle SuperSonics","Syracuse Nationals","Pittsburgh Ironmen","Providence Steam Rollers","Rochester Royals","Cincinnati Royals","Kansas City Kings","Sheboygan Red Skins","St. Louis Bombers","New Orleans Jazz","Washington Capitols","Chicago Zephyrs","Baltimore Bullets"],[15,8,46,2,32,4,10,5,34,17,10,9,30,36,6,6,3,4,4,86,1,2,23,4,6,3,3,2,17,5,1,8,4,2,2,22,1,1,4,1,2,7,3,2,11,5,2,6,3,1,4,1,1,6,1],["Josh Smith","Dana Barros","Albert King","Jeff McInnis","Dave Corzine","Jawad Williams","Deron Williams","Chauncey Billups","John Long","Joe Ellis","Dwight Jones","Jerry Sichting","Darrick Martin","Michael Cooper","Lorenzen Wright","Udonis Haslem","Jeff Webb","Tyus Jones","Elfrid Payton","Carl Braun","Daniel Orton","Chucky Atkins","Aaron McKie","Channing Frye","Damon Stoudamire","Matt Barnes","Devin Brown","Fred Roberts","Larry Wright","Ed Macauley","Paul Gordon","Joe Graboski","Mel Riebe","Art Stolkey","Curly Armstrong","Paul Arizin","Art Williams","Jim Springer","Leo Barnhorst","Mike Macaluso","Bill Walton","Tony Jaros","Steve Hawes","Larry Costello","Michael Bytzura","Ernie Calverley","Al Masino","Jerry Lucas","Larry Drew","Walt Lautenbach","Giff Roux","Aaron James","Earl Lloyd","Nick Mantis","Gene Shue"],["Josh Smith","Dana Barros","Kenny Anderson","Todd Fuller","Derrick Rose","Jawad Williams","Deron Williams","Chauncey Billups","Terry Tyler","Phil Smith","Clyde Drexler","George Hill","Marques Johnson","Byron Scott","Lorenzen Wright","Udonis Haslem","Steve Novak","Tyus Jones","Elfrid Payton","Carl Braun","Daniel Orton","Chucky Atkins","Wilt Chamberlain","Channing Frye","Damon Stoudamire","Michael Stewart","Devin Brown","Fred Roberts","Larry Wright","Ed Macauley","Paul Gordon","Mickey Rottner","Mel Riebe","Art Stolkey","Curly Armstrong","Paul Arizin","Art Williams","Jim Springer","Leo Barnhorst","Mike Macaluso","Bill Walton","Don Carlson","Steve Hawes","Larry Costello","Stan Noszka","Earl Shannon","Al Masino, Frank Reddout","Jerry Lucas","Larry Drew","Walt Lautenbach","Ed Macauley","Aaron James","Earl Lloyd","Joe Graboski, Jeff Slade","Gene Shue"]],"container":"<table class=\"cell-border nowrap\">\n  <thead>\n    <tr>\n      <th>Last Season<\/th>\n      <th>Franchise<\/th>\n      <th>Team<\/th>\n      <th># of Players<\/th>\n      <th>Most Games<\/th>\n      <th>Most WS<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"dom":"tpl","columnDefs":[{"className":"dt-right","targets":[0,3]},{"name":"Last Season","targets":0},{"name":"Franchise","targets":1},{"name":"Team","targets":2},{"name":"# of Players","targets":3},{"name":"Most Games","targets":4},{"name":"Most WS","targets":5}],"order":[],"autoWidth":false,"orderClasses":false}},"evals":[],"jsHooks":[]}</script>

We can also look at all players that had the opportunity to play for their hometown teams. There were 534 instances of this in the NBA’s history given our dataset. Note that this can apply to players multiple times; a Los Angeles native can have played for both the Clippers and Lakers. The definitions of home using CBSAs are still used, so Cleveland does not qualify as LeBron James’ hometown because Cleveland and Akron are defined as different metropolitan areas. The results for all U.S.-based teams are presented in the table above, along with some defunct franchises. Every active team has had at least one player who grew up in the city end up playing for them. Unsurprsingly, the two New York teams, the New York Knicks and Brooklyn Nets, have had the most hometown players. The Knicks have 86 and the Nets have 46.

Michael Cooper appeared in 873 games for his hometown Los Angeles Lakers, more than any other player for their hometown team. Miami’s Udonis Haslem played 854 for the Heat and Inglewood’s Byron Scott played 846 for the Lakers. Hall of Famer Paul Arizin has had one of the most impressive careers for a hometown team, spending his entire NBA life with the Philadelphia Warriors and leading them to an NBA title in 1956. Philadelphia’s Wilt Chamberlain played for two different franchises in his hometown—the Warriors from 1960 to 1962 and the 76ers from 1965 to 1968—winning the title in 1967.

While not on the table above, there have been four Canadians that have suited up for the Toronto Raptors, three of which are from the Toronto area. Of the three, Cory Joseph has played the most games and has the most Win Shares.
