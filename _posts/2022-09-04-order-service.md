---
title: FineTech Order Service AsyncAPI v1.0.0
date: 2022-09-04 10:00:00
categories: [sales,order,service]
tag: [api]
language_tabs:
  - http: Http
headingLevel: 3
toc_footers: []
includes: []
search: false
highlight_theme: darkula

---
The Order AsyncAPI subscibes on OrderPlacedEvent and publish OrderAsssessedEvent.
Base URLs:
Email: <a href="mailto:api@finelab.io">undefined</a> 
License: <a href="https://www.apache.org/licenses/LICENSE-2.0">Apache 2.0</a>

# Schemas

## OrderPlacedEvent

<a name="schemaorderplacedevent"></a>

```json
{
  "id": "string",
  "source": "string",
  "specversion": "string",
  "type": "string",
  "datacontenttype": "string",
  "dataschema": "string",
  "subject": "string",
  "time": "string",
  "data": {
    "number": "string",
    "quote": {},
    "person": {},
    "organization": {}
  },
  "data_base64": "string"
}

```

<h3 id="orderplacedevent-properties">Properties</h3>

*The OrderPlacedEvent contains Quote and Customer information and is based on CloudEvents Specification JSON Schema. https://raw.githubusercontent.com/cloudevents/spec/v1.0.1/spec.json*

|Name|Type|Required|Description|
|---|---|---|---|
|» id|string|true|No description|
|» source|string|true|No description|
|» specversion|string|true|No description|
|» type|string|true|No description|
|» datacontenttype|string|false|No description|
|» dataschema|string|false|No description|
|» subject|string|false|No description|
|» time|string|false|No description|
|» data|[Order](#schemaorder)|false|No description|
|»» number|string|false|No description|
|»» quote|object|false|No description|
|»» person|object|false|No description|
|»» organization|object|false|No description|
|» data_base64|string|false|No description|

## Order

<a name="schemaorder"></a>

```json
{
  "number": "string",
  "quote": {},
  "person": {},
  "organization": {}
}

```

<h3 id="order-properties">Properties</h3>

|Name|Type|Required|Description|
|---|---|---|---|
|» number|string|false|No description|
|» quote|object|false|No description|
|» person|object|false|No description|
|» organization|object|false|No description|

## OrderAssessedEvent

<a name="schemaorderassessedevent"></a>

```json
{
  "id": "string",
  "source": "string",
  "specversion": "string",
  "type": "string",
  "datacontenttype": "string",
  "dataschema": "string",
  "subject": "string",
  "time": "string",
  "data": {
    "status": "string",
    "order": {
      "number": "string",
      "quote": {},
      "person": {},
      "organization": {}
    }
  },
  "data_base64": "string"
}

```

<h3 id="orderassessedevent-properties">Properties</h3>

*The OrderAssessedEvent contains status for the assessment of the Quote and Customer information and is based on CloudEvents Specification JSON Schema. https://raw.githubusercontent.com/cloudevents/spec/v1.0.1/spec.json*

|Name|Type|Required|Description|
|---|---|---|---|
|» id|string|true|No description|
|» source|string|true|No description|
|» specversion|string|true|No description|
|» type|string|true|No description|
|» datacontenttype|string|false|No description|
|» dataschema|string|false|No description|
|» subject|string|false|No description|
|» time|string|false|No description|
|» data|[AssessedOrder](#schemaassessedorder)|false|No description|
|»» status|string|false|No description|
|»» order|[Order](#schemaorder)|false|No description|
|»»» number|string|false|No description|
|»»» quote|object|false|No description|
|»»» person|object|false|No description|
|»»» organization|object|false|No description|
|» data_base64|string|false|No description|

## AssessedOrder

<a name="schemaassessedorder"></a>

```json
{
  "status": "string",
  "order": {
    "number": "string",
    "quote": {},
    "person": {},
    "organization": {}
  }
}

```

<h3 id="assessedorder-properties">Properties</h3>

|Name|Type|Required|Description|
|---|---|---|---|
|» status|string|false|No description|
|» order|[Order](#schemaorder)|false|No description|
|»» number|string|false|No description|
|»» quote|object|false|No description|
|»» person|object|false|No description|
|»» organization|object|false|No description|

## OrderProcessedEvent

<a name="schemaorderprocessedevent"></a>

```json
{
  "id": "string",
  "source": "string",
  "specversion": "string",
  "type": "string",
  "datacontenttype": "string",
  "dataschema": "string",
  "subject": "string",
  "time": "string",
  "data": {
    "status": "string",
    "order": {
      "number": "string",
      "quote": {},
      "person": {},
      "organization": {}
    }
  },
  "data_base64": "string"
}

```

<h3 id="orderprocessedevent-properties">Properties</h3>

*The OrderProcessedEvent contains status for the order processing and referened to signatures It is based on CloudEvents Specification https://raw.githubusercontent.com/cloudevents/spec/v1.0.1/spec.json*

|Name|Type|Required|Description|
|---|---|---|---|
|» id|string|true|No description|
|» source|string|true|No description|
|» specversion|string|true|No description|
|» type|string|true|No description|
|» datacontenttype|string|false|No description|
|» dataschema|string|false|No description|
|» subject|string|false|No description|
|» time|string|false|No description|
|» data|[AssessedOrder](#schemaassessedorder)|false|No description|
|»» status|string|false|No description|
|»» order|[Order](#schemaorder)|false|No description|
|»»» number|string|false|No description|
|»»» quote|object|false|No description|
|»»» person|object|false|No description|
|»»» organization|object|false|No description|
|» data_base64|string|false|No description|

## ProcessedOrder

<a name="schemaprocessedorder"></a>

```json
{
  "status": "string",
  "order": {
    "number": "string",
    "quote": {},
    "person": {},
    "organization": {}
  },
  "signature_id": "string",
  "signature_url": "string"
}

```

<h3 id="processedorder-properties">Properties</h3>

|Name|Type|Required|Description|
|---|---|---|---|
|» status|string|false|No description|
|» order|[Order](#schemaorder)|false|No description|
|»» number|string|false|No description|
|»» quote|object|false|No description|
|»» person|object|false|No description|
|»» organization|object|false|No description|
|» signature_id|string|false|No description|
|» signature_url|string|false|No description|

