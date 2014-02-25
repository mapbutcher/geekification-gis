Geekification Of GIS
=====================

##Slide 1 - Grayson Perry

I have an admission to make - this presentation was inspired by a tranvestite potter from Essex.

Last year the english artist Grayson Perry gave a series of lectures for the BBC called the Reith lectures. In one of his lectures he explored the boundaries of what is and isn't art. 

Listening to Grayson Perry discuss egdes of the Art world made me consider the world I inhabit in the same way - It made we want to explore the boundaries of GIS.

## Slide 2 - The Edges are Blurred'

So, I'd like to spend the next 20 minutes or so exploring the boundaries where GIS and what could be considered 'broader IT' converge.

I think the quote from Vanessa Lawrence from the Ordnance Survey is very apt. At Geoplex we often operate where the edges are blurred and I'd like to share with you today some insight into some technology which is straying into the GIS domain - in effect highlighting what I'm calling the 'Geekification of GIS'.

## Slide 3 - Beating the Bounds

To help set the scene I'm going to begin by using a reference which Grayson Perry makes in his lecture - A reference to an Ancient English tradition

Beating the bounds was a custom where by younger members of the community were escorted around the boundaries of their villages to help share knowledge of where they lay. 

CLICK

At each village 'marker' the children were beaten. Essentially trying to embed a map by memory association. Children would be familiarised with the bounds of their village based upon a good old beating at the boundary

Rest assured I'll refrain from the beating today as we visit the markers around the boundaries of GIS

## Slide 4 - Markers

So as we beat the bounds this afternoon we're going to visit three markers: Search, Change and Maps Online. These markers represent three constants of GIS implementations.

At each marker I'll ask the questions:

What does our traditional view of the marker look like?
What is disrupting the marker?

....and finally

What might the future look like

## Slide 5 - Spatial databases are good for spatial data

It's quite ironic that Maps are meant to help us find things more easily. The current landscape of GIS applications and 'spatial data catalogues' tend to fail at providing useful search capabilities. They remind me of reading Where's Wally books to my kids.......frustrating.

Imagine if everything on our maps was searchable?


## Slide  - Matching expectations

Our traditional way of searching has focussed on searching the data sources that underpin our maps. But what if we think about it differently. What is we ask ourselves the question what's the best environment to put our data into to make it easier to search our data. Where would we look?

Our exacting nature means we believe our audiences want exact results

Most spatial search seems to begin by assuming the audient knows what they want to search for!

Are we using the right tool for the job?

## Slide 7 - Geo-Power

Furthermore

Being able to combine free text search with geo location is the crucial next step for our applications

Elasticsearch now includes support for spatial datatypes. Not only can we ask for information based upon an attribute of that information, but we can ask for information based upon where it exists.

Now you could argue - this is not really disruptive, we've been searching for things spatially for years, yes but our executions have not been targeting our audiences expectations.

## Slide 8 - I'll give you my 'geodatabase' when you pry it from my cold dead hands!

Well I know those in the old guard might be thinking to themselves....you'll not get rid of those spatial databases, but where those spatial databases live may well be challenged - how we manage databases and what we consider to be our storage options is changing. The release of Postresql & PostGIS in Amazon's RDS is a great step forward. 

The fact is that the future is no longer neatly locked into a single stack of technology.

The future involves more and more data! And as the volume of our data increases we need better ways to search it. 

We need to understand what tools best fit our requirements. We're backing search technology, not GIS technology when it comes to searching!

## Slide 9 - The Great Divide.

We work with alot of organisations which want to know what's changed, when and by who. However this sort of requirement has traditionally been met by big expensive solutions.

In my first job as a GIS Analyst we used to 'Merge and Post' overnight a long drawn out reconciliation of changes made across all the GIS editors in the organisation.

These version management solutions have remained the realm of those with deep pockets, and the rest of us have just cobbled along...until.

## Slide  - Please don't do this at home....

So what's changing?

Software engineers had been using this thing called version control for quite some time to manage source code. 

Multiple people could edit source code files at the same time and a system would track all these changes as well as provide ways to manage conflict resolution where conflicting changes occurred to the same file.

This sounds like something we could benefit from...

## Slide 11 - Map Diffing in GitHub

Over the last 5 years Git has emerged as the version control system of choice. 

Not only has it become popular amongst the IT world - it has become a growing platform for collaboration across non-it professionals. The City of Chicago for example has released a series of data openly via GitHub.

But how is this brave new world effecting our traditional world and how might it help us?

Well, companies like GitHub are now able to store and version control certain types of spatial data. In the example behind me you can see how you can visualise changes in geojson data committed to github.

## Slide 12 - Geogit

GeoJson and Github might be just the first step on our journey towards a brighter future where we can have manage change in our spatial data more easily and cost effectively.

I think one of the most exciting projects in this space is the GeoGit project being spearheaded by Boundless. 

Boundless have essentially created a branch of Git which allows you to commit a wider range of spatial data formats, such as Shapefile, PostGIS and SQL Server. Once committed into your GeoGit repository the data is tracked at the feature level. Any committed version can be differnced and exported. 

## Slide 13 - Crowded Space					

It's a crowded space out there in the mapping world. Ask Rohan :)

Surely everything has been done, we have static maps, dynamic maps, slippy maps, a million map API's, we have vector in the browser, we have temporal display, we have even have live twitter maps. Is there anything else left to do?

Does the crowd mean it can't be disrupted? Of course not, in my next example we'll see a disruption which is targetted towards combining together three factors which have been arguably absent until recently

These three factors are: Cost, Ease, Power

## Slide 14 - CartoDB

CartoDB has packaged the power of PostGIS into an interface where you can easily load spatial data and create powerful visualisations within a few clicks, and importantly they are doing so at a price point which disrupts the traditional model.

The map behind me shows the spread of the American Post Office network over a 10 second period...representing just under 400 years.

## Slide 15 - Incremental Innovation

One of the most disruptive features of CartoDB is arguably not it's most obvious.

The idea of creating map tiles is not exactly new. Ever since Google reinvented web mapping in 2005 we've been caching map tiles left, right and centre. But the accepted mantra during this period has been only cache what doesn't change - now whilst this is still true in many cases, it's no longer a universal truth. 

CartoDB, allows you to create map tiles on demand which are dynamic - what do I mean by dynamic? Well I can request a map, choosing what features are displayed and how they are displayed - all at runtime.

This is not new! I hear you cry - No you're right this is how all map servers essentially work - but what's new about it is that it works at scale, online and its affordable. This is essentially the evolution of online mapping

## Slide 16 What's next?

This one's far too hard to call! But I can't stand up here without putting my neck on the line so here goes...

1. I think we'll be revisiting our text books and trying to remember what raster analysis was all about, only this time we'll be able to do it online, in the browser - Like this excellent example from Mapbox which shows browser based dynamic hillshading.

2. With solutions like CartoDB finally the ultimate goodies in the spatial database toolbox are being let out - so I think we'll see spatial operators become a first class language.

3. The visualisation revolution will continue - our perception of who is qualified to make maps will continue to be challenged by people creating maps elsewhere. 

So before we conclude our journey around the boundaries of GIS, lets just briefly ask the question:

Why are the boundaries of GIS being blurred? Well I think there are two key reasons:


## Slide 17 - Digital Natives

The first reason is the ever increasing population of digitial natives. It is arguably the combination of digital natives with an entrepreneurial appetite which is leading to innovation in our industry and I for one think this is a really positive thing.


## Slide 16 - The Enabler

The second reason is the maturity of open source technology as an enabler - in each of the examples given this afternoon, open source has played a vital role. Elasticsearch wouldn't exist without Lucene, Github without Git and finally CartoDB without PostGIS and Mapnik. 

A closed proprietary eco-system is not devoid of innovation, but the geekification of GIS is flourishing under the influence of open source. 


