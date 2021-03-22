# plane-alert-db
This project contains several lists of 'interesting' aircraft, formatted as a CSV files. These files are designed to work with the excellent https://github.com/kx1t/docker-planefence and take the form 

- ICAO,Ident,Operator,Type,CMPG,$Tag,#$Tag2,Category

e.g 406C1B,G-CNWL,Cornwall Air Ambulance,Bell MD-900 Explorer,Civ,Air Ambo,Choppa,M\*A\*S\*H 

Add these characters to the column headers to control the behavior of PlaneAlert

- "$" \- Tweet this column as #hashtag
- "#" \- Don't show on the website (it will ignore this for the ICAO field, which is always shown)
- "#$"\- Don't show on the website, but tweet as a #hashtag

in the eample above the #hashtags would be 'Air Ambo' and 'Choppa', and Tag2 will not be shown on the PA website.


# Description of Categories	   

Think of categories like groups, with similar or related aircraft listed together. This allows you to easily select a subset of the list for your own use. The category names (and tags) come from my rather idiosyncratic sense of humour. If you have better suggestions I'm all ears.

- Aerobatic Teams	\- Red Arrows, Blue Angels etc
- As seen on TV	\- Companies and Brands
- Battle of Britiain Memorial Flight \- Historic British aircraft from WW2
- Bizjets	\- Fancy pants planes for fancy pants people
- Community \- Suggested by you. Aircraft start here and move other other categories
- Dictator Alert \- People of potentially questionable morals and values
- M\*A\*S\*H	\- Air Ambulance and Medical Flights
- Military Contractors \- Why do the dirty work when someone else can do it for you ?
- Nuclear \-	Nuclear Emergency  Support Team etc
- RAF	\- Aircraft of the Royal Air Force
- Royal Aircraft \- Aircraft used or owned by the UK Royal Family
- Royal Navy	\- Aircraft of the Royal Navy
- Sock Puppet	\- Someone Pretending to be something they are not
- Spotted	\- Aircraft spotted by my ADSB station. Aircraft start here and move other other categories
- UK National Police Air Service \- Your friendly neighbourhood flying bobby
- Under Observation \- 	Up to something dodgy, maybe
- USAF \- 	Aircraft of the United States Air Force
- Watch me fly \- 	Flying and Training Schools
- Who needs an Engine ?	\- Gliders etc
- Zoomies	\- Fast jets, fighters. Anything that moves fast.


# Current Content

- plane-alert-db.txt - The list of interesting aircaft, with tags and categories.
  - Bahrain Amiri Flight (Government Airline)
  - Qatar Amiri Flight.txt - A private VIP airline for the Qatari Royal Family
  - The Battle of Britain Memorial Flight
  - Government of Saudi Arabia Aircraft
  - United Kingdom National Police Aviation Service
  - RAF 32 Squadron and Helicopters operated by The Queen's Helicopter Flight.
  - US National Nuclear Security Administration
  - US Department of Energy
  - US Department of Justice
  - NASA
  - Random interesting aircaft e.g. AN124
- community-list.txt - Open list to add your suggestions to. These will be moved to the main list in time.
  
- archive - lists in out of date formats

  - military-contractors.txt - From refueing to operating fake flying cell phone towers, this list has it all.
  - royal-aircraft.txt - RAF 32 Squadron and Helicopters operated by The Queen's Helicopter Flight. HRH Queen Elizabeth II.
  - uk-NPAS.txt . Includes Helicopters and 4 Vulcanair P.68R aircraft.



# To do / Ideas

- Add more Military/Research/One-off Aircraft
- National Display Teams (e.g. Red Arrows, Blue Angels)
- Heads of State
- Drones and Spy Aircraft
- 'Covert' aircraft hiding their true purpose/ownership
- Old and Rare
- Aircraft with special history (e.g. Chinook Bravo November)
- Firefighting aircraft
- NASA Aircraft
- Input from non-english speaking countries
- film/tv/famous (Airwolf etc)

Any other idea's welcome.






