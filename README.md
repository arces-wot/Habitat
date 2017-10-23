# Habitat
The SEPA has been adopted by the Habitat project (http://www.habitatproject.info/home)

# Habitat WoT Application
The Habitat application has been modelled following the WoT model: https://www.w3.org/TR/wot-thing-description/. The following Web Things have been identified:
## RID (RFID Reader) ##
```json
{
  "@context": ["http://w3c.github.io/wot/w3c-wot-td-context.jsonld",{"hbt":"http://www.habitatproject.info/ontology#"}],
  "@type": ["Thing"],
  "name": "RID",
  "interaction": [
      {
          "@type": ["Event"],
          "name": "position",
          "outputData": {
              "type": "object",
              "fields": [{"name": "tabletId","value": {"type": "string"}},
                         {"name": "eventId","value": {"type": "string"}},
                         {"name": "message", "value": {"type": "string"}}}
    ]}
      }
  ]
}
```
## Chair ##
```json
{
  "@context": ["http://w3c.github.io/wot/w3c-wot-td-context.jsonld",{"hbt":"http://www.habitatproject.info/ontology#"}],
  "@type": ["Thing"],
  "name": "Chair",
  "interaction": [
      {
          "@type": ["Event"],
          "name": "seated",
          "outputData": {"type": "string"}
      },
       {
          "@type": ["Event"],
          "name": "posture",
          "outputData": {"type": "string"}
      },
       {
          "@type": ["Event"],
          "name": "getUp",
          "outputData": {"type": "string"}
      }
  ]
}
```
## Radio ##
```json
{
  "@context": ["http://w3c.github.io/wot/w3c-wot-td-context.jsonld",{"hbt":"http://www.habitatproject.info/ontology#"}],
  "@type": ["Thing"],
  "name": "Radio",
  "interaction": [
      {
          "@type": ["Action"],
          "name": "showMessage",
          "inputData":{"type":"string"}
      },
      {
          "@type": ["Action"],
          "name": "showMessageWithFeedback",
          "inputData":{
              "type": "object",
              "fields": [{"name": "eventId","value": {"type": "string"}},
                         {"name": "message", "value": {"type": "string"}}}
    ]}
      },
      {
          "@type": ["Event"],
          "name": "feedback",
          "outputData": {
              "type": "object",
              "fields": [{"name": "tabletId","value": {"type": "string"}},
                         {"name": "eventId","value": {"type": "string"}},
                         {"name": "message", "value": {"type": "string"}}}
    ]}
      }
  ]
}
```
## Tablet ##
```json
{
  "@context": ["http://w3c.github.io/wot/w3c-wot-td-context.jsonld",{"hbt":"http://www.habitatproject.info/ontology#"}],
  "@type": ["Thing"],
  "name": "Tablet",
  "interaction": [
      {
          "@type": ["Action"],
          "name": "showMessage",
          "inputData":{"type":"string"}
      },
      {
          "@type": ["Action"],
          "name": "showMessageWithFeedback",
          "inputData":{
              "type": "object",
              "fields": [{"name": "eventId","value": {"type": "string"}},
                         {"name": "message", "value": {"type": "string"}}}
    ]}
      },
      {
          "@type": ["Event"],
          "name": "feedback",
          "outputData": {
              "type": "object",
              "fields": [{"name": "tabletId","value": {"type": "string"}},
                         {"name": "eventId","value": {"type": "string"}},
                         {"name": "message", "value": {"type": "string"}}}
    ]}
      }
  ]
}
```
## AI Module ##
```json
{
  "@context": ["http://w3c.github.io/wot/w3c-wot-td-context.jsonld",{"hbt":"http://www.habitatproject.info/ontology#"}],
  "@type": ["Thing"],
  "name": "AIModule",
  "interaction": [
      {
          "@type": ["Event"],
          "name": "alarm",
          "outputData": {
              "type": "object",
              "fields": [{"name": "id", "value": {"type": "string"}},
                         {"name": "type","value": {"type": "string"}},
                         {"name": "message", "value": {"type": "string"}},
                         {"name": "private","value": {"type": "boolean"}}
    ]}
      },
      {
          "@type": ["Event"],
          "name": "prescription",
          "outputData": {
              "type": "object",
              "fields": [{"name": "id", "value": {"type": "string"}},
                         {"name": "type","value": {"type": "string"}},
                         {"name": "message", "value": {"type": "string"}},
                         {"name": "private","value": {"type": "boolean"}}
    ]}
      },
      {
          "@type": ["Event"],
          "name": "advice",
          "outputData": {
              "type": "object",
              "fields": [{"name": "id", "value": {"type": "string"}},
                         {"name": "type","value": {"type": "string"}},
                         {"name": "message", "value": {"type": "string"}},
                         {"name": "private","value": {"type": "boolean"}}
    ]}
      }
  ]
}
```
