# Danish municipalities geoJSON
This is meant to be used in [Elastic Map Services](https://maps.elastic.co/) or other similar services

To use this map with private IP-ranges, see [this repository](https://github.com/magnuslarsen/CustomMaxmindDatabase)

## Update map properties
`lau_1` and `postal_code` are fixed. Do not change these. \
Rest can be changed as pleased.

To update a geoJSON map, do the following:

1. Change directory to either `municipalities` or `postal_codes`
2. Update `data.csv`
3. Apply the changes with this command:
```
./apply_csv.rb
```

# Kibana configuration
Simply add this to your `kibana.yml` file:
```
map.regionmap:
  layers:
  - name: "Municipalities of Denmark"
    url: "https://raw.githubusercontent.com/magnuslarsen/geoJSON-Danish-municipalities/master/municipalities/municipalities.geojson"
    attribution: "Geodatastyrelsen & Danske Kommuner"
    fields:
    - name: "label_en"
      description: "Municipality name (in English)"
    - name: "label_dk"
      description: "Municipality name (in Danish)"
    - name: "lau_1"
      description: "LAU-1 code"

  - name: "Postal codes of Denmark"
    url: "https://raw.githubusercontent.com/magnuslarsen/geoJSON-Danish-municipalities/master/postal_codes/postal_codes.geojson"
    attribution: "Geodatastyrelsen & Danske Kommuner"
    fields:
    - name: "label_en"
      description: "Postal name (in English)"
    - name: "label_dk"
      description: "Postal name (in Danish)"
    - name: "postal_code"
      description: "Postal code"
```

## Helpful links
https://en.wikipedia.org/wiki/List_of_municipalities_of_Denmark

## Source
geoJSON map forked from [dagi](https://github.com/Neogeografen/dagi): \
Geodatastyrelsen & Danske Kommuner - FOT data set - 2014-02-13 - Scale 1:500.000
