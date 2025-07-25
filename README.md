**I. Introduction**
______________________
This dashboard automatically measures daily advertising performance using Google Sheets. It showcases skills in data import, cleaning, analysis, and visualization to produce an interactive and insightful report.

**II. Data Source**
______________________
Raw Data: (https://docs.google.com/spreadsheets/d/1h_yMbeEfiIKkV2YgRQuK_0E7nowEQUWamgJlBqsVX1M/edit?gid=0#gid=0)

**III. Project Objectives**
_______________________
- Automate daily ad performance tracking using Google Sheets

- Visualize key metrics: spend, messages, cost per message, engagement

- Highlight top efficient, inefficient, and high-spend campaigns

- Enable filtering by location and date

- Benchmark against CP Mess target

- Showcase skills in data processing and dashboard design

**IV. Requirements**
_______________________
- Google Sheets (no add-ons required)

- Functions: IMPORTRANGE, QUERY, IFERROR, SUMIFS, TEXTJOIN, IFS, REGEXMATCH

- Features: Pivot Tables, Slicer, Data Validation, Conditional Formatting, Charts

**V. Step-by-Step Guide**
_______________________
**1. Import Raw Data**
- Create a new Google Sheet
- In cell A1 enter:

 =IMPORTRANGE("https://docs.google.com/spreadsheets/d/1h_yMbeEfiIKkV2YgRQuK_0E7nowEQUWamgJlBqsVX1M/edit?gid=0#gid=0"; "Data Raw!A:S")

**2. Clean data**
- Add a new sheet and name it Clean Data
- In cell D1 enter:
=QUERY('Data Raw'!A:V,"Select * ")
- Create a new column named "Location" to filter the campaign by entering:
=ArrayFormula(iferror(IFS(REGEXMATCH(E2:E,"HEAD"), "HEAD", REGEXMATCH(E2:E,"Q7"), "Q7", REGEXMATCH(E2:E,"Q2"), "Q2"), "HEAD"))

**3. 
