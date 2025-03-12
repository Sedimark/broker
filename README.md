## Context
The [context](https://sedimark.github.io/broker/jsonld-contexts/sedimark-compound.jsonld) define all
the already discussed property for types :
- [Asset](https://sedimark.github.io/broker/jsonld-contexts/sedimark-asset.jsonld)
- [DataAsset](https://sedimark.github.io/broker/jsonld-contexts/sedimark-data-asset.jsonld)
- [AIModelAsset](https://sedimark.github.io/broker/jsonld-contexts/sedimark-ai-model-asset.jsonld)
- [ServiceAsset](https://sedimark.github.io/broker/jsonld-contexts/sedimark-service-asset.jsonld)

## Calling the broker with the context
You can use the "Link" header to define the context of your request when calling the NGSILD-Broker.
```
<https://sedimark.github.io/broker/jsonld-contexts/sedimark-compound.jsonld>; rel="http://www.w3.org/ns/json-ld#context"; type="application/ld+json"
```

## creation of assets
An example of asset creation for a broker deployed on "localhost:8080" would be the following :

POST "localhost:8080/ngsi-ld/v1/entities"

body : [example here](https://sedimark.github.io/broker/payload-example/asset.jsonld)

## fetching of asset by id
GET "localhost:8080/ngsi-ld/v1/entities/{id}"

[response example](https://sedimark.github.io/broker/payload-example/asset.jsonld)

##  fetching of a list of assets
GET "localhost:8080/ngsi-ld/v1/entities?type=Asset"

### temporal entities
If your properties are changing through time, you can add an observedAt value inside the properties to mark the point that they represent in times.

Then you can use the temporal endpoints to fetch the temporal representation.
https://stellio.readthedocs.io/en/latest/API_walkthrough.html#get-temporal-evolution-of-attributes

## additionnal resource https://ngsild.org/

