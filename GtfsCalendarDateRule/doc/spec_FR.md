<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entité : GtfsCalendarDateRule  
=============================<!-- /10-Header -->  
<!-- 15-License -->  
[Licence ouverte] (https://github.com/smart-data-models//dataModel.UrbanMobility/blob/master/GtfsCalendarDateRule/LICENSE.md)  
[document généré automatiquement] (https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Description globale : **Règle de la date du calendrier **GTFS  
version : 0.0.2  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## Liste des propriétés  

<sup><sub>[*] S'il n'y a pas de type dans un attribut, c'est parce qu'il pourrait avoir plusieurs types ou différents formats/modèles</sub></sup>.  
- `alternateName[string]`: Un nom alternatif pour cet élément  - `appliesOn[string]`:  Date (au format AAAA-MM-JJ) à laquelle cette règle s'applique. Elle est obtenue à partir du champ GTFS `date`.  . Model: [https://schema.org/Date](https://schema.org/Date)- `dataProvider[string]`: Une séquence de caractères identifiant le fournisseur de l'entité de données harmonisées.  - `dateCreated[string]`: Horodatage de la création de l'entité. Celui-ci sera généralement attribué par la plateforme de stockage.  - `dateModified[string]`: Horodatage de la dernière modification de l'entité. Il sera généralement attribué par la plateforme de stockage.  - `description[string]`: Une description de cet article  - `exceptionType[string]`: Identique au champ `exception_type` de GTFS. Enum : "1, 2  . Model: [https://schema.org/Text](https://schema.org/Text)- `hasService[string]`: Service auquel s'applique cette règle. Dérivé de `service_id`.  . Model: [https://schema.org/URL](https://schema.org/URL)- `id[*]`: Identifiant unique de l'entité  - `name[string]`: Le nom de cet élément.  - `owner[array]`: Une liste contenant une séquence de caractères codée en JSON référençant les identifiants uniques du ou des propriétaires.  - `seeAlso[*]`: liste d'uri pointant vers des ressources supplémentaires sur l'article  - `source[string]`: Une séquence de caractères donnant la source originale des données de l'entité sous forme d'URL. Il est recommandé d'utiliser le nom de domaine entièrement qualifié du fournisseur source ou l'URL de l'objet source.  - `type[string]`: Type d'entité NGSI : Il doit être GtfsCalendarDateRule. Enum : "GtfsCalendarDateRule" (en anglais)  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Propriétés requises  
- `appliesOn`  - `exceptionType`  - `hasService`  - `id`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-RequiredProperties -->  
Voir [https://developers.google.com/transit/gtfs/reference/#calendar_datestxt](https://developers.google.com/transit/gtfs/reference/#calendar_datestxt)  
<!-- /40-RequiredProperties -->  
<!-- 50-DataModelHeader -->  
## Description des propriétés du modèle de données  
Classés par ordre alphabétique (cliquez pour plus de détails)  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
GtfsCalendarDateRule:    
  description: 'GTFS Calendar Date Rule'    
  properties:    
    alternateName:    
      description: 'An alternative name for this item'    
      type: string    
      x-ngsi:    
        type: Property    
    appliesOn:    
      description: ' Date (in YYYY-MM-DD format) this rule applies to. It shall be obtained from the GTFS `date` field'    
      format: date    
      type: string    
      x-ngsi:    
        model: https://schema.org/Date    
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
    exceptionType:    
      description: 'Same as GTFS `exception_type` field. Enum:''1, 2'''    
      enum:    
        - 1    
        - 2    
      type: string    
      x-ngsi:    
        model: https://schema.org/Text    
        type: Property    
    hasService:    
      anyOf:    
        - description: 'Property. Identifier format of any NGSI entity'    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
        - description: 'Property. Identifier format of any NGSI entity'    
          format: uri    
          type: string    
      description: 'Service to which this rule applies to. Derived from `service_id`'    
      type: string    
      x-ngsi:    
        model: https://schema.org/URL    
        type: Relationship    
    id:    
      anyOf: &gtfscalendardaterule_-_properties_-_owner_-_items_-_anyof    
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
        anyOf: *gtfscalendardaterule_-_properties_-_owner_-_items_-_anyof    
        description: 'Property. Unique identifier of the entity'    
      type: array    
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
      description: 'NGSI Entity Type: It has to be GtfsCalendarDateRule. Enum:''GtfsCalendarDateRule'''    
      enum:    
        - GtfsCalendarDateRule    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - hasService    
    - appliesOn    
    - exceptionType    
  type: object    
  x-derived-from: ""    
  x-disclaimer: 'Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2022 Contributors to Smart Data Models Program'    
  x-license-url: https://github.com/smart-data-models/dataModel.UrbanMobility/blob/master/GtfsCalendarDateRule/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.UrbanMobility/GtfsCalendarDateRule/schema.json    
  x-model-tags: ""    
  x-version: 0.0.2    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## Exemples de charges utiles  
#### GtfsCalendarDateRule Valeurs-clés NGSI-v2 Exemple  
Voici un exemple de GtfsCalendarDateRule au format JSON-LD en tant que valeurs-clés. Ceci est compatible avec NGSI-v2 en utilisant `options=keyValues` et renvoie les données contextuelles d'une entité individuelle.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:CalendarDateRule:Malaga:Rule67",  
  "type": "GtfsCalendarDateRule",  
  "name": "Rule Fair Area",  
  "hasService": "urn:ngsi-ld:Gtfservice:Malaga:FairArea_1",  
  "appliesOn": "2018-03-19",  
  "exceptionType": "1"  
}  
```  
</details>  
#### GtfsCalendarDateRule NGSI-v2 normalisée Exemple  
Voici un exemple de GtfsCalendarDateRule au format JSON-LD tel que normalisé. Cette règle est compatible avec la NGSI-v2 lorsqu'elle n'utilise pas d'options et renvoie les données contextuelles d'une entité individuelle.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:CalendarDateRule:Malaga:Rule67",  
  "type": "GtfsCalendarDateRule",  
  "name": {  
    "value": "Rule Fair Area"  
  },  
  "exceptionType": {  
    "value": "1"  
  },  
  "hasService": {  
    "type": "Relationship",  
    "value": "urn:ngsi-ld:GtfsService:Malaga:FairArea_1"  
  },  
  "appliesOn": {  
    "value": "2018-03-19"  
  }  
}  
```  
</details>  
#### GtfsCalendarDateRule Valeurs clés NGSI-LD Exemple  
Voici un exemple de GtfsCalendarDateRule au format JSON-LD en tant que valeurs-clés. Ceci est compatible avec NGSI-LD lorsque l'on utilise `options=keyValues` et renvoie les données contextuelles d'une entité individuelle.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:CalendarDateRule:Malaga:Rule67",  
    "type": "GtfsCalendarDateRule",  
    "appliesOn": {  
        "type": "Property",  
        "value": "2018-03-19"  
    },  
    "exceptionType": {  
        "type": "Property",  
        "value": "1"  
    },  
    "hasService": {  
        "type": "Relationship",  
        "object": "urn:ngsi-ld:GtfsService:Malaga:FairArea_1"  
    },  
    "name": {  
        "type": "Property",  
        "value": "Rule Fair Area"  
    },  
    "@context": [  
        "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context.jsonld",  
        "https://raw.githubusercontent.com/smart-data-models/dataModel.UrbanMobility/master/context.jsonld"  
    ]  
}  
```  
</details>  
#### GtfsCalendarDateRule NGSI-LD normalisé Exemple  
Voici un exemple de GtfsCalendarDateRule au format JSON-LD tel que normalisé. Ceci est compatible avec NGSI-LD lorsqu'on n'utilise pas d'options et renvoie les données contextuelles d'une entité individuelle.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:CalendarDateRule:Malaga:Rule67",  
    "type": "GtfsCalendarDateRule",  
    "appliesOn": "2018-03-19",  
    "exceptionType": "1",  
    "hasService": "urn:ngsi-ld:GtfsService:Malaga:FairArea_1",  
    "name": "Rule Fair Area",  
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
