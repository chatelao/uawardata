# Ukraine War Data

## What you will find here
In this repository you will find the data we use on [www.uawardata.com](https://www.uawardata.com). You can use this data for free, but please note the citation (see below).

## How to cite
If you want to use this data, please quote us. You have two options:
* Henry Schlottman (https://twitter.com/HN_Schlottman)
* uawardata.com (https://www.uawardata.com)

## The data
All data is stored in the folder [`/data`](./data) as a [csv](./data/csv) and [geojson](./data/geojson). How they are structured:

### Units
Files:
* `units_all.geojson` and `units_all.csv`: All data points
* `units_current.geojson`and `units_current.csv`: Only the most current day

The **Unit**-files contains the units and where approximately their headquarters might be. Each unit in turn consists of different battalions (more about this later). The columns/properties of the files:

| Property | Type | Description |
|----------|------|-------------|
|date|*str*|At which date a unit was there (`%Y-%m-%d`)|
|lat|*float*|Latitude, only in CSV|
|lng|*float*|Longitude, only in CSV|
|icon|*str*|Nato symbol (MIL-STD-2525C).|
|type|*str*|Type of units (eg *Mechanized Infantry*)|
|strength|*str*|Strength of units (eg *Battalion*)|
|strength_in_btg_number|*number*|Approx. Strength in Batallion Tactical Groups|
|strength_in_btg_text|*text*|Approx. Strength in Batallion Tactical Groups (could be `< 1`)|
|unit|*str*|Name of the unit|
|unitnumber|*number*|Name of the unit as a number|
|subordinate_to|*str*|Subordinates to which unit|

### BTGs
Files:
* `btgs_all.geojson` and `btgs_all.csv`: All data points
* `btgs_current.geojson`and `btgs_current.csv`: Only the most current day

The **BTGs**-files contains the position of each individual unit (brigades, divisions, etc.). This file is the most accurate representation of the military presence.

| Property | Type | Description |
|----------|------|-------------|
|date|*str*|At which date a unit was there (`%Y-%m-%d`)|
|lat|*float*|Latitude, only in CSV|
|lng|*float*|Longitude, only in CSV|
|unit|*str*|Name of the unit|
|type_of_btg|*enum*|Type of unit. One of these: `motor_rifle`, `vdv` (Russian Airborne Forces), `tank`|

## Methodology
The data is collected by Henry Schlottman, a former U.S. Army analyst. Using known troop positions before the war began, pictures of (destroyed) Russian war equipment, information from prisoners, and other public data, he is able to record the approximate position of each unit. Despite all the information, the data remain approximations.

## Credits
Made by [Henry Schlottman](https://twitter.com/HN_Schlottman) and [Simon Huwiler](https://twitter.com/simon_huwiler)