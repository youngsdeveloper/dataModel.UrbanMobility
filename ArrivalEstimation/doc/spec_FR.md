<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entité : ArrivalEstimation  
==========================<!-- /10-Header -->  
<!-- 15-License -->  
[Licence ouverte] (https://github.com/smart-data-models//dataModel.UrbanMobility/blob/master/ArrivalEstimation/LICENSE.md)  
[document généré automatiquement] (https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Description globale : **Estimation de l'arrivée**  
version : 0.0.3  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## Liste des propriétés  

<sup><sub>[*] S'il n'y a pas de type dans un attribut, c'est parce qu'il pourrait avoir plusieurs types ou différents formats/modèles</sub></sup>.  
- `alternateName[string]`: Un nom alternatif pour cet élément  - `dataProvider[string]`: Une séquence de caractères identifiant le fournisseur de l'entité de données harmonisées.  - `dateCreated[string]`: Horodatage de la création de l'entité. Celui-ci sera généralement attribué par la plateforme de stockage.  - `dateModified[string]`: Horodatage de la dernière modification de l'entité. Il sera généralement attribué par la plateforme de stockage.  - `description[string]`: Une description de cet article  - `hasStop[array]`: Il doit pointer vers une entité de type GtfsStop.  - `hasTrip[*]`: Voyage associé à cette Entité. Il doit pointer vers une Entité de type GtfsTrip  . Model: [https://schema.org/URL](https://schema.org/URL)- `headSign[string]`: Il doit contenir le texte qui figure sur un panneau indiquant aux passagers la destination du voyage.  . Model: [https://schema.org/Text.](https://schema.org/Text.)- `id[*]`: Identifiant unique de l'entité  - `name[string]`: Le nom de cet élément.  - `owner[array]`: Une liste contenant une séquence de caractères codée en JSON référençant les identifiants uniques du ou des propriétaires.  - `remainingDistance[number]`: Il contient la distance restante (en mètres) d'arrivée pour le trajet se dirigeant vers l'arrêt concerné  . Model: [https://schema.org/Number](https://schema.org/Number)- `remainingTime[string]`: Il contient l'heure d'arrivée restante du voyage à destination de l'arrêt concerné. Le temps restant est codé sous la forme d'une durée ISO8601. Ex. `PT8M5S`.  - `seeAlso[*]`: liste d'uri pointant vers des ressources supplémentaires sur l'élément  - `source[string]`: Une séquence de caractères donnant la source originale des données de l'entité sous forme d'URL. Il est recommandé d'utiliser le nom de domaine entièrement qualifié du fournisseur source ou l'URL de l'objet source.  - `type[string]`: Type d'entité NGSI : Il doit s'agir de ArrivalEstimation. Enum : 'ArrivalEstimation' (estimation d'arrivée)  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Propriétés requises  
- `hasStop`  - `hasTrip`  - `headSign`  - `id`  - `remainingTime`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-RequiredProperties -->  
Ce type d'entité saisit l'heure d'arrivée estimée d'un véhicule de transport public atteignant un arrêt particulier, alors que le véhicule dessert un itinéraire particulier.  
<!-- /40-RequiredProperties -->  
<!-- 50-DataModelHeader -->  
## Description des propriétés du modèle de données  
Classés par ordre alphabétique (cliquez pour plus de détails)  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
ArrivalEstimation:    
  description: 'Arrival Estimation'    
  properties:    
    alternateName:    
      description: 'An alternative name for this item'    
      type: string    
      x-ngsi:    
        type: Property    
    dataProvider:    
      description: 'A sequence of characters identifying the provider of the harmonised data entity.'    
      type: string    
      x-ngsi:    
        type: Property    
    dateCreated:    
      description: 'Entity creation timestamp. This will usually be allocated by the storage platform.'    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    dateModified:    
      description: 'Timestamp of the last modification of the entity. This will usually be allocated by the storage platform.'    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    description:    
      description: 'A description of this item'    
      type: string    
      x-ngsi:    
        type: Property    
    hasStop:    
      description: 'It shall point to an Entity of Type GtfsStop'    
      items:    
        anyOf:    
          - description: 'Property. Identifier format of any NGSI entity'    
            maxLength: 256    
            minLength: 1    
            pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
            type: string    
          - description: 'Property. Identifier format of any NGSI entity'    
            format: uri    
            type: string    
      type: array    
      x-ngsi:    
        type: Relationship    
    hasTrip:    
      anyOf:    
        - description: 'Property. Identifier format of any NGSI entity'    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
        - description: 'Property. Identifier format of any NGSI entity'    
          format: uri    
          type: string    
      description: 'Trip associated to this Entity. It shall point to an Entity of Type GtfsTrip'    
      x-ngsi:    
        model: https://schema.org/URL    
        type: Relationship    
    headSign:    
      description: 'It shall contain the text that appears on a sign that identifies the trip''s destination to passengers'    
      type: string    
      x-ngsi:    
        model: https://schema.org/Text.    
        type: Property    
    id:    
      anyOf: &arrivalestimation_-_properties_-_owner_-_items_-_anyof    
        - description: 'Property. Identifier format of any NGSI entity'    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
        - description: 'Property. Identifier format of any NGSI entity'    
          format: uri    
          type: string    
      description: 'Unique identifier of the entity'    
      x-ngsi:    
        type: Property    
    name:    
      description: 'The name of this item.'    
      type: string    
      x-ngsi:    
        type: Property    
    owner:    
      description: 'A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)'    
      items:    
        anyOf: *arrivalestimation_-_properties_-_owner_-_items_-_anyof    
        description: 'Property. Unique identifier of the entity'    
      type: array    
      x-ngsi:    
        type: Property    
    remainingDistance:    
      description: 'It shall contain the remaining distance (in meters) of arrival for the trip heading to the concerned stop'    
      minimum: 0    
      type: number    
      x-ngsi:    
        model: https://schema.org/Number    
        type: Property    
        units: Meters    
    remainingTime:    
      description: 'It shall contain the remaining time of arrival for the trip heading to the concerned stop. Remaining time shall be encoded as a ISO8601 duration. Ex. `PT8M5S`.'    
      pattern: ^P(?=\w*\d)(?:\d+Y|Y)?(?:\d+M|M)?(?:\d+W|W)?(?:\d+D|D)?(?:T(?:\d+H|H)?(?:\d+M|M)?(?:\d+(?:\?.\d{1,2})?S|S)?)?$    
      type: string    
      x-ngsi:    
        type: Property    
    seeAlso:    
      description: 'list of uri pointing to additional resources about the item'    
      oneOf:    
        - items:    
            format: uri    
            type: string    
          minItems: 1    
          type: array    
        - format: uri    
          type: string    
      x-ngsi:    
        type: Property    
    source:    
      description: 'A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object.'    
      type: string    
      x-ngsi:    
        type: Property    
    type:    
      description: 'NGSI Entity Type: It has to be ArrivalEstimation. Enum:''ArrivalEstimation'''    
      enum:    
        - ArrivalEstimation    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - hasStop    
    - hasTrip    
    - remainingTime    
    - headSign    
  type: object    
  x-derived-from: ""    
  x-disclaimer: 'Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2022 Contributors to Smart Data Models Program'    
  x-license-url: https://github.com/smart-data-models/dataModel.UrbanMobility/blob/master/ArrivalEstimation/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.UrbanMobility/ArrivalEstimation/schema.json    
  x-model-tags: ""    
  x-version: 0.0.3    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## Exemples de charges utiles  
#### ArrivéeEstimation Valeurs-clés NGSI-v2 Exemple  
Voici un exemple d'une ArrivalEstimation au format JSON-LD sous forme de valeurs-clés. Ceci est compatible avec NGSI-v2 lorsqu'on utilise `options=keyValues` et renvoie les données contextuelles d'une entité individuelle.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:ArrivalEstimation:L5C1_Stop74_1",  
  "type": "ArrivalEstimation",  
  "hasStop": ["urn:ngsi-ld:GtfsStop:tus:74"],  
  "hasTrip": "urn:ngsi-ld:GtfsTrip:tus:5C1",  
  "remainingTime": "PT8M5S",  
  "remainingDistance": 1200,  
  "headSign": "Plaza Italia"  
}  
```  
</details>  
#### ArrivéeEstimation NGSI-v2 normalisée Exemple  
Voici un exemple d'ArrivalEstimation au format JSON-LD tel que normalisé. Ce format est compatible avec la NGSI-v2 lorsqu'il n'utilise pas d'options et renvoie les données contextuelles d'une entité individuelle.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:ArrivalEstimation:L5C1_Stop74_1",  
  "type": "ArrivalEstimation",  
  "hasTrip": {  
    "type": "Relationship",  
    "value": "urn:ngsi-ld:GtfsTrip:tus:5C1"  
  },  
  "headSign": {  
    "value": "Plaza Italia"  
  },  
  "remainingTime": {  
    "value": "PT8M5S"  
  },  
  "hasStop": {  
    "type": "Relationship",  
    "value": "urn:ngsi-ld:GtfsStop:tus:74"  
  },  
  "remainingDistance": {  
    "value": 1200  
  }  
}  
```  
</details>  
#### ArrivéeEstimation Valeurs-clés NGSI-LD Exemple  
Voici un exemple d'une ArrivalEstimation au format JSON-LD sous forme de valeurs-clés. Ceci est compatible avec NGSI-LD lorsque l'on utilise `options=keyValues` et renvoie les données contextuelles d'une entité individuelle.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:ArrivalEstimation:L5C1_Stop74_1",  
    "type": "ArrivalEstimation",  
    "hasStop": {  
        "type": "Relationship",  
        "object": "urn:ngsi-ld:GtfsStop:tus:74"  
    },  
    "hasTrip": {  
        "type": "Relationship",  
        "object": "urn:ngsi-ld:GtfsTrip:tus:5C1"  
    },  
    "headSign": {  
        "type": "Property",  
        "value": "Plaza Italia"  
    },  
    "remainingDistance": {  
        "type": "Property",  
        "value": 1200  
    },  
    "remainingTime": {  
        "type": "Property",  
        "value": "PT8M5S"  
    },  
    "@context": [  
        "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context.jsonld",  
        "https://raw.githubusercontent.com/smart-data-models/dataModel.UrbanMobility/master/context.jsonld"  
    ]  
}  
```  
</details>  
#### ArrivéeEstimation NGSI-LD normalisée Exemple  
Voici un exemple d'ArrivalEstimation au format JSON-LD tel que normalisé. Ce format est compatible avec NGSI-LD lorsqu'il n'utilise pas d'options et renvoie les données contextuelles d'une entité individuelle.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:ArrivalEstimation:L5C1_Stop74_1",  
    "type": "ArrivalEstimation",  
    "hasStop": "urn:ngsi-ld:GtfsStop:tus:74",  
    "hasTrip": "urn:ngsi-ld:GtfsTrip:tus:5C1",  
    "headSign": "Plaza Italia",  
    "remainingDistance": 1200,  
    "remainingTime": "PT8M5S",  
    "@context": [  
        "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context.jsonld",  
        "https://raw.githubusercontent.com/smart-data-models/dataModel.UrbanMobility/master/context.jsonld"  
    ]  
}  
```  
</details><!-- /80-Examples -->  
<!-- 90-FooterNotes -->  
<!-- /90-FooterNotes -->  
<!-- 95-Units -->  
Voir [FAQ 10](https://smartdatamodels.org/index.php/faqs/) pour obtenir une réponse sur la façon de traiter les unités de magnitude.  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
