# Map data of "Driving Licence: City 3D" (მართვის მოწმობა: ქალაქი 3D)

This is the map data the game ships, offered under the Open Database License as section 4.6 of that licence asks of a
work made from OpenStreetMap: the database derived from OpenStreetMap, whole, in the form the game reads it.

**Contains information from OpenStreetMap, which is made available here under the Open Database License (ODbL) 1.0.**
Map data © OpenStreetMap contributors: https://www.openstreetmap.org/copyright

## Source

- OpenStreetMap, Geofabrik's Georgia extract: https://download.geofabrik.de/europe/georgia-latest.osm.pbf, data up to
  2026-09-13 (file of 101,758,587 bytes, Last-Modified 2026-09-13 23:39 GMT, downloaded 2026-09-14).
- Clipped to the city of Rustavi (OSM relation 1997305) and the eight category B city exam routes' corridors.

## How it was made

- The road network (lanes, junctions, traffic lights, connections, crossings, signs, markings) by SUMO's `netconvert`
  from the OSM extract, then converted to the game's own JSON. Where OSM maps no sign, the sign is placed by the
  traffic law's rules; such entries are marked `derived`.
- Trees and parked cars are placed by rule on the areas OSM maps (rows along streets, the market's car parks); their
  positions are the game's, not surveyed.
- The eight routes follow the exam routes as drawn over the OSM network.

## Files

| File | What it holds |
|---|---|
| `data/city_world.json` | The city's drivable network: lanes, connections, traffic lights, roundabouts, signs, crossings, separations, markings, points of interest |
| `data/routes.json` | The index of the eight routes |
| `data/routes/rustavi-1.json` … `rustavi-8.json` | Each exam route: its path over the network, its manoeuvres, checkpoints, limits and junctions |
| `data/trees.json` | Trees placed along the streets |
| `data/parked_cars.json` | Parked cars placed on the mapped car parks and aisles |
| `data/monuments.json`, `data/landmarks.json` | Where the city's monuments, islands and landmarks stand |

## Licence

The data in this repository is licensed under the Open Database License 1.0,
https://opendatacommons.org/licenses/odbl/1-0/ . Its individual contents are under the Database Contents License,
https://opendatacommons.org/licenses/dbcl/1-0/ , as OpenStreetMap's are. Anyone may copy, change and use it, on the
same terms, with the attribution above.
