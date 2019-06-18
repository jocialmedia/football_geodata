# Football Geodata

As far as I know there is no up-to-date source for geodata of German football clubs. So I made one. If you find an error please leave me a message. If you find it useful please leave me a star.

## Files

- [football_geodata_ger_19-20_all.csv](data/football_geodata_ger_19-20_all.csv)
- [football_geodata_ger_19-20_all.geojson](data/football_geodata_ger_19-20_all.geojson)


## Stats

| League Identifier   | League                | Clubs    | Capacity       |
|---------------------|-----------------------|----------|----------------|
| germany_league_1    | Bundesliga            | 18       | 803.230        |
| germany_league_2    | 2. Bundesliga         | 18       | 485.887        |
| germany_league_3    | 3. Liga               | 18       | 407.886        |
| germany_league_4    | Regionalliga Nord     | 18       | 112.030        |
| germany_league_4    | Regionalliga Nordost  | 18       | 183.288        |
| germany_league_4    | Regionalliga West     | 19       | 204.392        |
| germany_league_4    | Regionalliga Südwest  | 18       | 172.235        |
| germany_league_4    | Regionalliga Bayern   | 18       | 139.840        |
|                     | **All**               | **147**  | **2.508.788**  |


## Data Schema 

Key                   | Description                                   | Origin/Source |
--------------------- | --------------------------------------------- |---------------|
id                    | Id in context of this file                    | -             |
season_2019-2020      | League identifier                             | Wikipedia     |
league                | Name of league                                | Wikipedia     |
club                  | Name of the club                              | Wikipedia     |
team_type             | First or second team of the club              | Own research  |
stadium               | Name of the stadium                           | Wikipedia     |
capacity              | Capacity of the stadium                       | Wikipedia     |
street                | Address of stadium                            | Own research  |
postcode              | Address of stadium                            | Own research  |
city                  | Address of stadium                            | Own research  |
federal_state         | Federal state the stadium is located in       | Own research  |
latitude              | Taken from the center of main pitch           | Own research  |
longitude             | Taken from the center of main pitch           | Own research  |
homepage              | Homepage of the club                          | Own research  | 
wikipedia_de          | Related Wikipedia page in German              | Own research  | 
wikipedia_en          | Related Wikipedia page in English             | Own research  | 
openstreetmap_object  | Stadium as object within OpenStreetMap        | Own research  | 


## Data Example

 ```
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "properties": {
        "id": "27",
        "club": "FC St. Pauli",
        "team_type": "1",
        "season_2019-2020": "germany_league_2",
        "league": "2. Bundesliga",
        "stadium": "Millerntor-Stadion",
        "capacity": "29.546",
        "address": "Harald-Stender-Platz 1, 20359 Hamburg",
        "federal_state": "HH",
        "homepage": "fcstpauli.com",
        "wikipedia_german": "https://de.wikipedia.org/wiki/FC_St._Pauli",
        "wikipedia_english": "https://en.wikipedia.org/wiki/FC_St._Pauli",
        "openstreetmap_object": "https://www.openstreetmap.org/way/381109520"
      },
      "geometry": { "type": "Point", "coordinates": [9.96773, 53.55458] }
    }
  ]
}
 ``` 


## Remarks

- The order is based on the position of the club at the end of season 2018/2019
- The informations about the stadiums used may be subject to change and will be updated as soon as I learn new details.
- The stadium of KFC Uerdingen is currently unfit for use so the club has to play in stadiums of other clubs like MSV Duisburg (Season 2018/2019) and Fortuna Düsseldorf (Season 2019/2020). This is why in this dataset the stadium information at id 10 and 47 are identical. 
- The second Team of the FC Bayern München, the TSV 1860 München and SV Türkgücü-Ataspor München use the same stadium. This is why in this dataset the stadium information at id 48, 56 and 146 are identical.


## Thank you to

- [OpenStreetMap](https://www.openstreetmap.org/about)
- [Python](https://www.python.org)
- [Wikipedia](https://en.wikipedia.org/wiki/Wikipedia:About)


## Reclaimer

The information given here is public. There is no commercial interest whatsoever. I can't and won't take any guarantee for the correctness of the data and any consequences that may result from using it.