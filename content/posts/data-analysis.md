+++
title = 'data'
date = 2024-09-29T00:06:17+10:00
draft = true
status = ['incomplete']
+++

A post about how I got into data and data analysis.

It all comes back to a dataset that I found on the ACT Government's data portal about bicycle accidents: https://www.data.act.gov.au/Justice-Safety-and-Emergency/Cyclist-Crashes/n2kg-qkwj/about_data



From there, I downloadeed a CSV, and tried a number of different things over the next few months and years.

First, I imported it into Excel, and played around with some basic summary statistics.

Then, I imported it into R with RStudio and did some more summary statistics and charts. Then, I found a similar dataset for road vehicle accidents and noticed that some of the crash ids were the same and had similar features, so joined the datasets together to do more interesting analyses.

I realised the dataset had GPS coordinates, so I spent hours trying to work out how to import a CSV into GQIS and display the points on a map. I also found other related datasets, and started trying to do spatial joins to group the original dataset around other geographies.

Then I started to get interested in reproducible analysis using RMarkdown, so I re-factored my original R code to use a literate programming approach and to document the analytical environment with the renv package.

Then, I decided to set up a postgresql server on my laptop and import the dataset into there - with SQL and with R's interface with postgresql. I was able to undertake some rudimentary analysis with SQL, which was recorded as SQL statements in code chunks in R Notebooks. After a few configuration tribulations, I was able to connect RStudio to that database and execute those SQL statements from the R Notebook directly through DBI and ODBC connections. I was also able to import the data into R direct from my local postgresql server.

I now learned a bit more about coordinate reference systems and switched from the stock standard geographic CRS to a projected CRS that was more appropriate for grouping data points within boundaries.

This was about the time I discovered the PostGIS extension to SQL. After doing the tutorial, it was time to do some rudimentary spatial analysis in SQL and then to connect postgresql with PostGIS up to QGIS and to bring the data in that way. A few extra layers made a pretty enough map.

Finally, it was time for the data to change - not just adding some new rows but also updating errors in the data in existing rows. Now it was time to experience ETL (export, transform, load) and understand what it is like to work with a data pipeline ... A series of bash and SQL scripts later and the data was being downloaded, upserted into the postgresql server, re-generating the geographic data types and indexes. I even toyed with setting it up on a cron job, before realising the data had only changed 

And, I've now discovered that while the dataset hasn't updated since 2021, there's an API available. There's also an R package specifically for accessing data through the software package used to serve the data. And, in the interim, I've learned about git, and I've explored flexdashboards and quarto has been released.

It all started with one little dataset ...