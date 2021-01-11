# MTA Subway Turnstile Analysis

The use case for this project is to address a client's desire to fill their event space at an annual fundraiser gala and maximize contributions. They deploy street teams to subway entrances to collect email addresses. Those individuals are then sent a a free invitation to the gala.

> The challenge is to use MTA subway data to identify optimal subway station positions for the street team.

<br/>

**Approach:**

1. Analyze/clean data
2. Identify Top 10 stations by volume
3. Identify target days and times for each station

<br/>

**Data used:**

We used data from the [MTA Data Feeds](http://web.mta.info/developers/developer-data-terms.html#data)

| Data | Field Descriptions | Usage
| --------------- | -------------- | ----------- |
| [Turnstile Data](http://web.mta.info/developers/turnstile.html) | [Descriptions](http://web.mta.info/developers/resources/nyct/turnstile/ts_Field_Description.txt) | Data analysis
| [Station Entrances](http://web.mta.info/developers/data/nyct/subway/StationEntrances.csv) | [Descriptions](http://web.mta.info/developers/resources/nyct/subway/StationEntranceDefinitions.csv) | Reference for mapping entrance locations

<br/>

**Features used:**

*Main features*

| Feature | Usage
| --------------- | --------------
| C/A, UNIT, SCP | Concatenated to create unique turnstile ID
| STATION | Station names
| DATE, TIME | Converted to datetime
| ENTRIES, EXITS | Net values added to analyze total traffic

<br/>

- C/A - Control Area
- Unit - Remote unit for a station
- SCP - Turnstile device
- Station - Station name. These are not unique for some subsequent stops on the same street or avenue
- Date/Time - Values as strings
- Entries/Exits - Represented as incremental values from the last reported value

<br/>

*Data Cleaning features*

| Feature | Usage
| --------------- | --------------
| LINENAME | Concatenated to stations with multiple spread out locations
| DIVISION | Filtered only values for subway stations
| DESC | Removed duplicate records with "RECOVER AUD" value

<br/>

- Linename - Line serviced by specific record
- Division - Old representation of NYC lines
- Desc - Differentiates the way records were received, either through the usual 4-hour audit or a recovery process

<br/>

**Tools Used:**

- Seaborn
- Matplotlib

<br/>
This project could possibly be of use to those looking for the peak days/times of the most populous NYC subway stations.
