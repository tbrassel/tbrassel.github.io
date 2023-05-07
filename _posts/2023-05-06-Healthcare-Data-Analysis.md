---
layout: post
title: Healthcare Data Analysis with R and SQL (in progress)
subtitle: Meaningful insights with interactive graphs
---

# Building a SQL Database
To build the database with the provided .csv files I created a SQLite database with the DBI() package and RStudio. I then used RMarkdown's inline SQL engine and the kable() package to implement and display SQLite database queries in neatly formatted PDF LaTex tables. I then saved the file outputs as CSV files. 

### Load required R packages
```R
library(readr) # Read file inputs
library(DBI) # Database connection
library(kableExtra) # Table formatting
library(ggplot2) # Graphing
library(plotly) # Make interactive graphs
library(magrittr) # Pipes %>%
library(dplyr) # Data manipulation
```

### Read both .csv tables into R with R tidyverse functions. 
```R
Attribution <- read_delim("data/AttributionData.csv", delim = "|")
Encounter <- read_delim("data/EncounterData.csv", delim = "|")
Person <- read_delim("data/PersonData.csv", delim = "|", skip_empty_rows = TRUE)
Person <- Person[-(nrow(Person)),]
```

### Create a new SQLite database file path
```R
network_db_file <- "data/network_db.sqlite"
```

### Make a SQLite database at the file path location 'conversations_db_file'
```R
con <- dbConnect(RSQLite::SQLite(), network_db_file)
```

### Write the 'Attribution' table to the database
```R
dbWriteTable(con, "Attribution", Attribution[,], overwrite = TRUE, row.names = FALSE)
```
