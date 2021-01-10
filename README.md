# MTA Subway Turnstile Analysis

The use case for this project is to address a client's desire to fill their event space at an annual fundraiser gala and maximize contributions. They deploy street teams to subway entrances to collect email addresses. Those individuals are then sent a a free invitation to the gala.

> The challenge is to use MTA subway data to identify optimal subway station positions for the street team.

 <br/>

**Approach:**

1. Analyze/clean data
2. Identify Top 10 stations by volume
3. Identify target days and times for each station
 <br/>
 <br/>


**Data used:**

We used data from the [MTA Data Feeds](http://web.mta.info/developers/developer-data-terms.html#data)

| Data | Field Descriptions | Usage
| --------------- | -------------- | ----------- |
| [Turnstile Data](http://web.mta.info/developers/turnstile.html) | [Descriptions](http://web.mta.info/developers/resources/nyct/turnstile/ts_Field_Description.txt) | Data analysis
| [Station Entrances](http://web.mta.info/developers/data/nyct/subway/StationEntrances.csv) | [Descriptions](http://web.mta.info/developers/resources/nyct/subway/StationEntranceDefinitions.csv) | Reference for mapping entrance locations

 <br/>

**Tools Used:**

- Seaborn
- Matplotlib

 <br/>


This project could possibly be of use to those looking for the peak days/times of the most populous NYC subway stations.
