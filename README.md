shapefile bug
===

## What's the problem?

The `avg_temp` field for the Wyoming feature is `null` in the shapefile. When converted to geojson via `shp2json`, this value becomes `0`.

## How to test

```
npm start
```

This will output `us-states.geojson` which will have a value of `0` for Wyoming's `avg_temp`, instead of `null`.

```json
{
  "type": "Feature",
  "properties": {
    "name": "Wyoming",
    "fid": "WY",
    "avg_temp": 0
  }
}
```
