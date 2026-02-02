# Water use case
This document describe how to access data from Sedimark water use case.

## Request examples
You can find the water use case [collection](https://raw.githubusercontent.com/Sedimark/broker/main/water_use_case.postman_collection)
and import it in tools like [postman](https://www.postman.com/) or [bruno](https://www.usebruno.com/downloads). 

You can also use the [open api specification](https://raw.githubusercontent.com/Sedimark/broker/main/water_use_case_open_api.yaml) as an example.

## Specific request
If you have a specific request. You can call the NGSI-LD URL accompanied by the following http headers :
- `NGSILD-Tenant=urn:ngsi-ld:tenant:sedimark`
- `LINK=<https://easy-global-market.github.io/ngsild-api-data-models/projects/jsonld-contexts/sedimark.jsonld>; rel="http://www.w3.org/ns/json-ld#context"; type="application/ld+json"`.

A [complete documentation of the available api](https://stellio.readthedocs.io/en/latest/) is available in stellio documentation.
Please note that provision endpoints are secured with open id connect. You can find [examples of authentication](https://stellio.readthedocs.io/en/latest/user/authentication_and_authorization.html#authenticate) in stellio documentation. 
