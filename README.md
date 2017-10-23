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
          "outputData": {"type": "..."}
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
          "inputData":{"type":"..."}
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
          "inputData":{"type":"..."}
      },
      {
          "@type": ["Event"],
          "name": "feedback",
          "outputData": {"type": "..."}
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
          "outputData": {"type": "..."}
      },
      {
          "@type": ["Event"],
          "name": "prescription",
          "outputData": {"type": "..."}
      },
      {
          "@type": ["Event"],
          "name": "advice",
          "outputData": {"type": "..."}
      }
  ]
}
```
