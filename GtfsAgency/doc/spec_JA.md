<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
エンティティGtfsAgency  
================<!-- /10-Header -->  
<!-- 15-License -->  
[オープンライセンス](https://github.com/smart-data-models//dataModel.UrbanMobility/blob/master/GtfsAgency/LICENSE.md)  
[ドキュメント自動生成](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
グローバルな説明**GTFS機関**。  
バージョン: 0.0.2  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## プロパティ一覧  

<sup><sub>[*] 属性にタイプがない場合、複数のタイプまたは異なるフォーマット/パターンを持つ可能性があるためです</sub></sup>。  
- `addressCountry[string]`: 国のことです。例えば、スペイン  . Model: [https://schema.org/addressCountry](https://schema.org/addressCountry)- `addressLocality[string]`: ストリートアドレスがある地域、地域内の  . Model: [https://schema.org/addressLocality](https://schema.org/addressLocality)- `addressRegion[string]`: ロケールがある地域、国内にある地域  . Model: [https://schema.org/addressRegion](https://schema.org/addressRegion)- `agencyName[string]`: GTFSの`agency_name`と同じ。  . Model: [https://schema.org/Text](https://schema.org/Text)- `alternateName[string]`: この項目の別称  - `dataProvider[string]`: 調和されたデータエンティティの提供者を識別する一連の文字。  - `dateCreated[string]`: エンティティの作成タイムスタンプ。これは通常、ストレージプラットフォームによって割り当てられる。  - `dateModified[string]`: エンティティの最終更新のタイムスタンプ。これは通常、ストレージプラットフォームによって割り当てられる。  - `description[string]`: このアイテムの説明  - `entitySource[string]`: Entity データの元のソースを URL として示す一連の文字。これは、この Entity を生成するために使用されたオリジナルの GTFS フィードの URL を指すものとする。  . Model: [https://schema.org/URL](https://schema.org/URL)- `id[*]`: エンティティの一意な識別子  - `language[string]`: GTFSの `agency_language` と同じです。GTFS](https://developers.google.com/transit/gtfs/reference/#agencytxt)を参照。  . Model: [https://schema.org/Text](https://schema.org/Text)- `name[string]`: このアイテムの名称です。  - `owner[array]`: 所有者の一意のIDを参照するJSONエンコードされた文字列を含むリストです。  - `page[string]`: GTFSの `stop_url` と同じ。  . Model: [http://schema.org/URL](http://schema.org/URL)- `phone[string]`: GFTSの`agency_phone`と同じ。  . Model: [https://schema.org/Text](https://schema.org/Text)- `postOfficeBoxNumber[string]`: 私書箱の住所の場合は、郵便番号。例：03578  . Model: [https://schema.org/postOfficeBoxNumber](https://schema.org/postOfficeBoxNumber)- `postalCode[string]`: 郵便番号です。例：24004  . Model: [https://schema.org/https://schema.org/postalCode](https://schema.org/https://schema.org/postalCode)- `seeAlso[*]`: 項目に関する追加リソースを指すURIのリスト。  - `source[string]`: エンティティデータの元のソースをURLで示す一連の文字。ソースプロバイダの完全修飾ドメイン名、またはソースオブジェクトのURLであることが推奨されます。  - `streetAddress[string]`: ストリートアドレス  . Model: [https://schema.org/streetAddress](https://schema.org/streetAddress)- `timezone[string]`: GTFSの `agency_timezone` と同じです。GTFS](https://developers.google.com/transit/gtfs/reference/#agencytxt)を参照。  . Model: [https://schema.org/Text](https://schema.org/Text)- `type[string]`: NGSI Entity Type。GtfsAgencyである必要があります。Enum:'GtfsAgency' です。  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
必要なプロパティ  
- `agencyName`  - `id`  - `source`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-RequiredProperties -->  
参照[https://developers.google.com/transit/gtfs/reference/#agencytxt](https://developers.google.com/transit/gtfs/reference/#agencytxt)  
<!-- /40-RequiredProperties -->  
<!-- 50-DataModelHeader -->  
## プロパティのデータモデル記述  
アルファベット順に並びます（クリックで詳細へ）  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
GtfsAgency:    
  description: 'GTFS Agency'    
  properties:    
    addressCountry:    
      description: 'The country. For example, Spain'    
      type: string    
      x-ngsi:    
        model: https://schema.org/addressCountry    
        type: Property    
    addressLocality:    
      description: 'The locality in which the street address is, and which is in the region'    
      type: string    
      x-ngsi:    
        model: https://schema.org/addressLocality    
        type: Property    
    addressRegion:    
      description: 'The region in which the locality is, and which is in the country'    
      type: string    
      x-ngsi:    
        model: https://schema.org/addressRegion    
        type: Property    
    agencyName:    
      description: 'Same as GTFS `agency_name`'    
      type: string    
      x-ngsi:    
        model: https://schema.org/Text    
        type: Property    
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
    entitySource:    
      description: 'A sequence of characters giving the original source of the Entity data as a URL. It shall point to the URL of the original GTFS feed used to generate this Entity'    
      format: uri    
      type: string    
      x-ngsi:    
        model: https://schema.org/URL    
        type: Property    
    id:    
      anyOf: &gtfsagency_-_properties_-_owner_-_items_-_anyof    
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
    language:    
      description: "Same as GTFS `agency_language`. See [GTFS](https://developers.google.com/transit/gtfs/reference/#agencytxt)"    
      type: string    
      x-ngsi:    
        model: https://schema.org/Text    
        type: Property    
    name:    
      description: 'The name of this item.'    
      type: string    
      x-ngsi:    
        type: Property    
    owner:    
      description: 'A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)'    
      items:    
        anyOf: *gtfsagency_-_properties_-_owner_-_items_-_anyof    
        description: 'Property. Unique identifier of the entity'    
      type: array    
      x-ngsi:    
        type: Property    
    page:    
      description: 'Same as GTFS `stop_url`'    
      format: uri    
      type: string    
      x-ngsi:    
        model: http://schema.org/URL    
        type: Property    
    phone:    
      description: 'Same as GFTS `agency_phone`'    
      type: string    
      x-ngsi:    
        model: https://schema.org/Text    
        type: Property    
    postOfficeBoxNumber:    
      description: 'The post office box number for PO box addresses. For example, 03578'    
      type: string    
      x-ngsi:    
        model: https://schema.org/postOfficeBoxNumber    
        type: Property    
    postalCode:    
      description: 'The postal code. For example, 24004'    
      type: string    
      x-ngsi:    
        model: https://schema.org/https://schema.org/postalCode    
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
    streetAddress:    
      description: 'The street address'    
      type: string    
      x-ngsi:    
        model: https://schema.org/streetAddress    
        type: Property    
    timezone:    
      description: "Same as GTFS `agency_timezone`. See [GTFS](https://developers.google.com/transit/gtfs/reference/#agencytxt)"    
      type: string    
      x-ngsi:    
        model: https://schema.org/Text    
        type: Property    
    type:    
      description: 'NGSI Entity Type: It has to be GtfsAgency. Enum:''GtfsAgency'''    
      enum:    
        - GtfsAgency    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - agencyName    
    - source    
  type: object    
  x-derived-from: ""    
  x-disclaimer: 'Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2022 Contributors to Smart Data Models Program'    
  x-license-url: https://github.com/smart-data-models/dataModel.UrbanMobility/blob/master/GtfsAgency/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModels.UrbanMobility/GtfsAgency/schema.json    
  x-model-tags: ""    
  x-version: 0.0.2    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## ペイロードの例  
#### GtfsAgency NGSI-v2 key-value の例。  
ここでは、GtfsAgencyをJSON-LD形式でkey-valuesにした例を示します。これは、`options=keyValues`を使用した場合にNGSI-v2と互換性があり、個々のエンティティのコンテキストデータを返します。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:GtfsAgency:Malaga_EMT",  
  "type": "GtfsAgency",  
  "agencyName": "Empresa Malagueña de Transportes",  
  "page": "http://www.emtmalaga.es/",  
  "timezone": "Europe/Madrid",  
  "language": "ES",  
  "source": "http://datosabiertos.malaga.eu/dataset/lineas-y-horarios-bus-google-transit/resource/24e86888-b91e-45bf-a48c-09855832fd52"  
}  
```  
</details>  
#### GtfsAgency NGSI-v2 正規化例  
GtfsAgency を JSON-LD 形式で正規化した例を示します。これはオプションを使用しない場合，NGSI-v2と互換性があり，個々のエンティティのコンテキストデータを返します。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:GtfsAgency:Malaga_EMT",  
  "type": "GtfsAgency",  
  "agencyName": {  
    "value": "Empresa Malague\u00f1a de Transportes"  
  },  
  "language": {  
    "value": "ES"  
  },  
  "page": {  
    "value": "http://www.emtmalaga.es/"  
  },  
  "source": {  
    "value": "http://datosabiertos.malaga.eu/dataset/lineas-y-horarios-bus-google-transit/resource/24e86888-b91e-45bf-a48c-09855832fd52"  
  },  
  "timezone": {  
    "value": "Europe/Madrid"  
  }  
}  
```  
</details>  
#### GtfsAgency NGSI-LD キー値例  
ここでは、GtfsAgencyをJSON-LD形式でkey-valuesとして表した例を示します。これは、`options=keyValues`を使用した場合にNGSI-LDと互換性があり、個々のエンティティのコンテキストデータを返します。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:GtfsAgency:Malaga_EMT",  
    "type": "GtfsAgency",  
    "agencyName": {  
        "type": "Property",  
        "value": "Empresa Malague\u00f1a de Transportes"  
    },  
    "language": {  
        "type": "Property",  
        "value": "ES"  
    },  
    "page": {  
        "type": "Property",  
        "value": "http://www.emtmalaga.es/"  
    },  
    "source": {  
        "type": "Property",  
        "value": "http://datosabiertos.malaga.eu/dataset/lineas-y-horarios-bus-google-transit/resource/24e86888-b91e-45bf-a48c-09855832fd52"  
    },  
    "timezone": {  
        "type": "Property",  
        "value": "Europe/Madrid"  
    },  
    "@context": [  
        "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context.jsonld",  
        "https://raw.githubusercontent.com/smart-data-models/dataModel.UrbanMobility/master/context.jsonld"  
    ]  
}  
```  
</details>  
#### GtfsAgency NGSI-LD 正規化例  
GtfsAgencyをJSON-LD形式で正規化した例です。これはオプションを使用しない場合のNGSI-LDと互換性があり，個々のエンティティのコンテキストデータを返します。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:GtfsAgency:Malaga_EMT",  
    "type": "GtfsAgency",  
    "agencyName": "Empresa Malague\u00f1a de Transportes",  
    "language": "ES",  
    "page": "http://www.emtmalaga.es/",  
    "source": "http://datosabiertos.malaga.eu/dataset/lineas-y-horarios-bus-google-transit/resource/24e86888-b91e-45bf-a48c-09855832fd52",  
    "timezone": "Europe/Madrid",  
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
マグニチュード単位の扱いについては、[FAQ 10](https://smartdatamodels.org/index.php/faqs/)を参照してください。  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
