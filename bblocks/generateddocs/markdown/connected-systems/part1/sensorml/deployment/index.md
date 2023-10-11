
# SensorML Deployment (Schema)

`ogc.connected-systems.part1.sensorml.deployment` *v0.1*

A Deployment Feature in SensorML format

[*Status*](http://www.opengis.net/def/status): Invalid

## Examples

### SensorML deployment
#### json
```json
{
  "type": "Deployment",
  "id": "iv3f2kcq27gfi",
  "definition": "http://www.w3.org/ns/ssn/Deployment",
  "uniqueId": "urn:x-saildrone:mission:2025",
  "label": "Saildrone - 2017 Arctic Mission",
  "description": "In July 2017, three saildrones were launched from Dutch Harbor, Alaska, in partnership with NOAA Research...",
  "classifiers": [
    {
      "definition": "https://schema.org/DefinedRegion",
      "label": "Region",
      "value": "Arctic"
    }
  ],
  "contacts": [
    {
      "role": "http://sensorml.com/ont/swe/property/Operator",
      "organisationName": "Saildrone, Inc.",
      "contactInfo": {
        "website": "https://www.saildrone.com/",
        "address": {
          "deliveryPoint": "1050 W. Tower Ave.",
          "city": "Alameda",
          "postalCode": "94501",
          "administrativeArea": "CA",
          "country": "USA"
        }
      }
    },
    {
      "role": "http://sensorml.com/ont/swe/property/DataProvider",
      "organisationName": "NOAA Pacific Marine Environmental Laboratory (PMEL)",
      "contactInfo": {
        "website": "https://www.pmel.noaa.gov"
      }
    }
  ],
  "validTime": [
    "2017-07-17T00:00:00Z",
    "2017-09-29T00:00:00Z"
  ],
  "location": {
    "type": "Polygon",
    "coordinates": [[
      [-173.70, 53.76],
      [-173.70, 75.03],
      [-155.07, 75.03],
      [-155.07, 53.76],
      [-173.70, 53.76]
    ]]
  },
  "members": [
    {
      "href": "https://data.example.org/api/systems/2f35ofoms2l6?f=sml",
      "uid": "urn:x-saildrone:platforms:SD-1001",
      "title": "Saildrone SD-1001"
    },
    {
      "href": "https://data.example.org/api/systems/2f35ofoms2l8?f=sml",
      "uid": "urn:x-saildrone:platforms:SD-1002",
      "title": "Saildrone SD-1002"
    },
    {
      "type": "PhysicalSystem",
      "name": "Saildrone SD-1003",
      "uniqueId": "urn:x-saildrone:platforms:SD-1003",
      "typeOf": {
        "href": "https://data.example.org/api/systems/2f35ofoms2l9?f=sml"
      },
      "components": [
        {
          "name": "air_temp_sensor",
          "href": "https://data.example.org/api/systems/41548?f=sml",
          "uid": "urn:x-saildrone:sensors:temp01",
          "title": "Air Temperature Sensor"
        },
        {
          "name": "water_temp_sensor",
          "href": "https://data.example.org/api/systems/36584?f=sml",
          "uid": "urn:x-saildrone:sensors:temp02",
          "title": "Water Temperature Sensor"
        },
        {
          "name": "wind_sensor",
          "href": "https://data.example.org/api/systems/47752?f=sml",
          "uid": "urn:x-saildrone:sensors:wind01",
          "title": "Wind Speed and Direction Sensor"
        }
      ]
    }
  ],
  "links": [
    {
      "href" : "https://data.example.org/api/deployments/iv3f2kcq27gfi?f=sml",
      "rel" : "self",
      "type" : "application/sml+json",
      "title" : "this document"
    }, {
      "href" : "https://data.example.org/api/deployments/iv3f2kcq27gfi?f=json",
      "rel" : "alternate",
      "type" : "application/geo+json",
      "title" : "this resource as GeoJSON"
    }
  ]
}
```

## Schema

```yaml
$schema: http://json-schema.org/draft-07/schema#
allOf:
- $ref: ../../../../../../api/part1/openapi/schemas/sensorml/sensormlDefs.json#/definitions/Deployment
- properties:
    definition:
      const: http://www.w3.org/ns/ssn/Deployment
    links:
      description: Links to related resources
      $ref: ../../../../../../api/part1/openapi/schemas/common/links.json
  required:
  - definition

```

Links to the schema:

* YAML version: [schema.yaml](https://ogcincubator.github.io/ogcapi-connected-systems/bblocks/annotated-schemas/connected-systems/part1/sensorml/deployment/schema.json)
* JSON version: [schema.json](https://ogcincubator.github.io/ogcapi-connected-systems/bblocks/annotated-schemas/connected-systems/part1/sensorml/deployment/schema.yaml)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/ogcincubator/ogcapi-connected-systems](https://github.com/ogcincubator/ogcapi-connected-systems)
* Path: `bblocks/_sources/part1/sensorml/deployment`
