<!--
🚨 IMPORTANT NOTICE 🚨

This README is dynamically generated by the `update_readme.yml` action using the mustache template language and the chevron parser. To make changes, ONLY edit the `readme.mustache` file.

🚨 IMPORTANT NOTICE 🚨
-->

# plane-alert-db <!-- omit in toc -->

This project consists of lists of 'interesting' aircraft, formatted as CSV files. The list is designed to work with the excellent **<https://github.com/sdr-enthusiasts/docker-planefence>**.

> **Warning**
> Please only suggest/make any changes to the [plane-alert-db.csv](plane-alert-db.csv), [plane-alert-pia.csv](plane-alert-pia.csv), and [plane_images.csv](plane_images.csv) files on GitHub - all other files (except PIA) are generated from this file, and if you do not make your changes there, they will be overwritten and lost. Additionally, it is **not recommended** to edit the CSV files in Microsoft Excel, as Excel will attempt to "fix" some ICAO hexes and other fields. It's better to use a code editor such as VS Studio Code—you can access the web version of Code by pressing the period key . when viewing the file you wish to edit.

## TOC <!-- omit in toc -->

-   [Current Content](#current-content)
-   [Description of Categories](#description-of-categories)
-   [Planefence](#planefence)
-   [Contributing](#contributing)
-   [Disclaimer, excuses and dodges](#disclaimer-excuses-and-dodges)
-   [Data Sources](#data-sources)

## Current Content

There currently are about **15223** unique aircraft in **51** categories found in this repository. This [Dashboard](https://lookerstudio.google.com/reporting/94a654de-8cb5-4e7a-a3e5-e4ce25e47f37) contains details of the main list.
These aircraft are divided into four main databases:

-   [plane-alert-db.csv](plane-alert-db.csv) - A list of interesting aircraft with tags, categories and links. (15223)
-   [plane-alert-pia.csv](plane-alert-pia.csv): A list that contains PIA planes. (94)
-   [plane_images.csv](plane_images.csv): A accompanying list that contains aircraft images. (11925)

Based on these main databases, several derivative databases are created using a [GitHub action](https://github.com/sdr-enthusiasts/plane-alert-db/actions/workflows/create_db_derivatives.yaml):

-   [plane-alert-civ.csv](plane-alert-civ.csv) - Civilian Registered Aircraft, includes Historic and Distinctive. (4292)
-   [plane-alert-mil.csv](plane-alert-mil.csv) - Military Only. (8276)
-   [plane-alert-pol.csv](plane-alert-pol.csv) - Police Forces. (927)
-   [plane-alert-gov.csv](plane-alert-gov.csv) - Governments, Gov Agencies and Dictators. (1728)

A second version of each of the above lists contains up to 4 image links per aircraft. These lists are created in [GitHub action](https://github.com/sdr-enthusiasts/plane-alert-db/actions/workflows/create_db_derivatives.yaml) using the [plane_images.csv](plane_images.csv) database. **Please consider this experimental, do not come to rely on any of the image links**

-   [plane-alert-db-images.csv](plane-alert-db-images.csv)
-   [plane-alert-civ-images.csv](plane-alert-civ-images.csv)
-   [plane-alert-mil-images.csv](plane-alert-mil-images.csv)
-   [plane-alert-pol-images.csv](plane-alert-pol-images.csv)
-   [plane-alert-gov-images.csv](plane-alert-gov-images.csv)

Note, we used to create a seperate list, `plane-alert-twitter-blocked.csv`, for use with Planefence's Twitter posting functionality. This list would prevent certain aircraft from being posted to Twitter in an attempt to keep the posting bot account from being banned. Since Twitter has now made it all but impossible for users to make bots for free, we've stopped creating this list.

This [Dashboard](https://lookerstudio.google.com/reporting/46ff4328-09d3-4e65-ab5a-bd2ba27a18fd) contains details of the [main](https://github.com/sdr-enthusiasts/plane-alert-db/blob/main/plane-alert-db.csv) list.

## Description of Categories

Think of categories like groups, with similar or related aircraft listed together. This allows you to easily select a subset of the list for your own use. The category names (and tags) come from my rather idiosyncratic sense of humour. If you have better suggestions I'm all ears.

|**Category**|**Description**|**Count**|
|--------|-----------|----:|
|Aerial Firefighter|Firefighting Aircraft|351|
|Aerobatic Teams|Red Arrows, Blue Angels, etc.|78|
|Army Air Corps|UK Army Air Corps, mainly Helicopters|94|
|As Seen on TV|Companies and Brands|492|
|Big Hello|Large Helicopters (sic)|106|
|Bizjets|Fancy pants planes for fancy pants people|56|
|CAP|Civil Air Patrol.|14|
|Climate Crisis|Oil Companies, Large Business Jets - BBJs and ACJs|195|
|Coastguard|Coastguard, Customs and Border Patrols|447|
|Da Comrade|Russian or Soviet Aircraft|91|
|Dictator Alert|People of potentially questionable morals and values|326|
|Distinctive|Unique and/or special aircraft e.g. The AN-225 Myria, NASA aircraft, Testbeds|212|
|Dogs with Jobs|Aircraft with specific roles and/or modifications|211|
|Don't you know who I am?|Famous People. I was going to say notable, but I'll go with Famous|81|
|Flying Doctors|Air Ambulance and Medical Flights|810|
|Football|Actual, Aussie Rules or American. We don't discriminate.|23|
|GAF|Aircraft of the German Air Force|410|
|Gas Bags|Would you like to ride in my beautiful balloon?|14|
|Governments|Aircraft registered to Governments|263|
|Gunship|Brrrrrrrrrrrrrrrrrrrt|261|
|Hired Gun|Why do the dirty work when someone else can do it for you?|302|
|Historic|It's older than I am and most likely has a prop.|462|
|Jesus he Knows me|Aircraft owned and operated by religious organisations|24|
|Joe Cool|Cool Planes. Or at least I think they are cool.|241|
|Jump Johnny Jump|de Havilland Chipmunks. Air Cadets of a certain age will understand.|388|
|Nuclear|Nuclear Emergency Support Team etc.|19|
|Oligarch|I made this money all by myself.|41|
|Other Air Forces|Air Force aircraft that are not GAF, RAF, or USAF|2045|
|Other Navies|Navy Aircraft that are not Royal Navy Fleet Air Arm or United States Navy|200|
|Oxcart|Intelligence gathering aircraft|677|
|Perfectly Serviceable Aircraft|Why do you keep jumping out of a Perfectly Serviceable Aircraft aka Skydiving planes|45|
|PIA|Privacy ICAO Address....you can run, but you cannot hide.|15|
|Police Forces|Your friendly neighbourhood flying (insert local colloquialism here).|910|
|Ptolemy would be proud|Mapping and Aerial Survey aircraft.|233|
|Quango|NATO, United Nations, World Bank etc.|33|
|Radiohead|Very Very special aircraft. Think VC25.|5|
|RAF|Aircraft of the Royal Air Force|243|
|Royal Aircraft|Aircraft used or owned by the UK Royal Family|8|
|Royal Navy Fleet Air Arm|Aircraft of the Royal Navy Fleet Air Arm|97|
|Special Forces|The best of the best of the best. Sir.|172|
|Toy Soldiers|Armies from around the world.|907|
|UAV|It's not natural, I tell 'ya!|37|
|UK National Police Air Service|Your friendly neighbourhood flying bobby.|24|
|Ukraine|Aircraft from Ukraine|36|
|United States Marine Corps|Aircraft of the United States Marine Corps, Oorah!|245|
|United States Navy|United States Naval avaitors. Some say they are the best of the best.|520|
|USAF|Aircraft of the United States Air Force|2367|
|Vanity Plate|Distinctive registrations|78|
|Watch Me Fly|Flying and Training Schools|75|
|You came here in that thing?|Microlights, tiny planes and helis..think Yakima Super Breezy.|102|
|Zoomies|Fast jets, fighters. Anything that moves fast.|137|

## Planefence

The list takes the form:

| $ICAO  | $Registration | $Operator                | $Type                | $ICAO Type | #CMPG | $Tag 1           | $#Tag 2      | $#Tag 3    | Category        | $#Link                                               |
| ------ | ------------- | ------------------------ | -------------------- | ---------- | ----- | ---------------- | ------------ | ---------- | --------------- | ---------------------------------------------------- |
| 502C5C | YL-KSH        | Baltic Bees display team | Aero L-39C Albatross | L39        | Civ   | Do A Barrel Roll | Display Team | Aerobatics | Aerobatic Teams | <https://en.wikipedia.org/wiki/Baltic_Bees_Jet_Team> |

To use this list with Planefence, configure your `planefence.config` setup to include the following line:

```config
PF_ALERTLIST=https://raw.githubusercontent.com/sdr-enthusiasts/plane-alert-db/main/plane-alert-db.csv
```

If you want to add the list in addition to your local plane-alert-db.csv list, you can do the following:

```config
PF_ALERTLIST=plane-alert-db.csv,https://raw.githubusercontent.com/sdr-enthusiasts/plane-alert-db/main/plane-alert-gov.csv,https://raw.githubusercontent.com/sdr-enthusiasts/plane-alert-db/main/plane-alert-pol.csv
```

> **Note**
> The priority of use is first-to-last, so if you want your local list to be interpreted first, move it to the front of the list.

Add these characters to the column headers to control the behaviour of PlaneAlert

-   `$` - Tweet this column as #hashtag.
-   `#` - Don't show on the website (it will ignore this for the ICAO field, which is always shown).
-   `$#` - Don't show on the website; tweet as a #hashtag.

## Contributing

Feel free to [open an issue](https://github.com/sdr-enthusiasts/plane-alert-db/issues) if you have ideas on improving this repository or want to report a bug! All contributions are welcome 🚀. Please consult the [contribution guidelines](CONTRIBUTING.md) for more information. You can also check out the [TODOS](TODOS.md) page if you want to contribute to this repository but need some ideas.

> **Warning**
> As also [explained above](#current-content), this repository contains four main databases to which people can contribute. The other databases are created automatically using [GitHub action](https://github.com/sdr-enthusiasts/plane-alert-db/actions/workflows/create_db_derivatives.yaml). As a result, please only suggest/make any changes to these main databases. Changes made to all other CSV files will be overwritten and lost. Additionally, it is **not recommended** to edit the CSV files in Microsoft Excel, as Excel will attempt to "fix" some ICAO hexes and other fields. It's better to use a code editor such as VS Studio Code—you can access the web version of Code by pressing the period key . when viewing the file you wish to edit.

If you're creating a pull request with additions, please add them to the end of the file. We may sort the list periodically to group like planes together.

## Disclaimer, excuses and dodges

This is not intended to be a definitive list, especially when it comes to aircraft models. Where the same model of aircraft is made by several manufacturers I won't always have the correct one. If you thought it was a Beechcraft King Air 200 and actually it was a Textron Super King Air B200GT, I won't be losing any sleep. There are other data sources (see below) if you want absolute accuracy.

## Data Sources

This data has been gathered from far too many sources to mention, but some sites have been _really_ useful:

-   <https://github.com/iatacodes/whatisflying-db>
-   <https://github.com/The-CFR-Project/whatisflying-db>
-   <https://www.flightdb.net/index.php>
-   <http://www.rotorspot.nl/>
-   <http://www.dtvmovements.co.uk/>
-   <http://www.ads-b.nl/>
-   <https://www.live-military-mode-s.eu/>
-   <https://dictatoralert.org/>
-   <http://www.j-hangarspace.jp/>
-   <https://scramble.nl/>
-   <https://www.foxtrotcharlie.ovh/>
-   <https://www.planelogger.com/>
-   <https://www.jetphotos.com/>

## LICENSE

Copyright (C) 2022-2024 by SDR-Enthusiasts, Ramon F. Kolb (kx1t), and contributors.
A list of contributors can be found at <https://github.com/sdr-enthusiasts/plane-alert-db/graphs/contributors>

This Database is made available under the Open Database License: <http://opendatacommons.org/licenses/odbl/1.0/>
Any rights in individual contents of the database are licensed under the Database Contents License: <http://opendatacommons.org/licenses/dbcl/1.0/>
