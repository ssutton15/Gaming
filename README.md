# Gaming
#mc_database.ipynb is a notebook of 5 parts built to create a csv/excel/googlesheets doc of the Marvel Champions Cards.  
#This assumes you have used jupyter notebooks a little bit already.  

#Initial Setup  
#First you will need a folder for the JSON files (I imported 34 files).  
#Download and add all of the JSON files you want to your folder such as ant.json, cap.json, etc (for antman and captain america packs, respectively).  
#The link to the JSONs is here: https://github.com/zzorba/marvelsdb-json-data/tree/master/pack

#Part 1 - Single JSON Example  
#This part is an example just pulling in cap.json  

#Part 2 - Multiple JSON Files into single DF
#This part uses 'glob' to read all the json files in the specified directory and add them to a file_list.
#I then loop through that list of files and add them to a single dataframe.
#There are many columns I wish to remove. Initially, I have 1323 rows and 52 columns.
#I start by combining the 4 resources into new column, then list out columns to remove, and a desired reordering of the remaining columns.
#I clean up the dataframe and remove some NaN rows leaving 1103 rows and 17 columns.

#Part 3 - Export the DF to a csv
#This should put a csv file in the current directory. I gave it the full path name to be sure.

#Part 4 - Extra Information
#An Alphabetical list of Heros
#A list of the card sets in the dataframe. These represent the various packs/expansions. But some are redundant.
#For instance, mts_campaign is mad titans shadow expansion. This set comes with spectrum and adam warlock.
#But the sets listed include 'mts_campaign', 'spectrum', and 'warlock'.

#Part 5 - Sunburst Plots
#These do not show on github.
#If you download and run this notebook you can generate 2 INTERACTIVE sunburst plots.
#The first shows heros, and if you drill down you see their specific 15ish cards that must be included when deckbuilding that hero.
#The second shows a list of allies based on their aspect [basic, leadership, protection, justice, aggression].
#'Hero' is also considered an aspect for this purpose as it is a specific category of card.
