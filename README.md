# Danish municipalities geoJSON
This is meant to be used in [Elastic Map Services](https://maps.elastic.co/) or other similar services

To use this map with private IP-ranges, see [this repository](https://github.com/magnuslarsen/CustomMaxmindDatabase)

## Update map properties
lau_1 is fixed. Do not change this.
Rest can be changed as pleased.

To update the geoJSON map, run the following:
```
./apply_csv.rb
```

## Helpful links
https://en.wikipedia.org/wiki/List_of_municipalities_of_Denmark

## Source
geoJSON map forked from [dagi](https://github.com/Neogeografen/dagi): \
Geodatastyrelsen & Danske Kommuner - FOT data set - 2014-02-13 -Scale 1:500.000
