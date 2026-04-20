# Food Allergy - Food Allergies FHIR Implementation Guide v0.1.0-test

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Food Allergy**

## Resource Profile: Food Allergy 

| | |
| :--- | :--- |
| *Official URL*:http://example.com/fhir/example/StructureDefinition/FoodAllergy | *Version*:0.1.0-test |
| Active as of 2026-04-20 | *Computable Name*:FoodAllergy |

 
Food Allergy profile 

**Usages:**

* Examples for this Profile: [AllergyIntolerance/MyPeanutAllergy](AllergyIntolerance-MyPeanutAllergy.md)

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/xxexample.fhir.food-Allergy|current/StructureDefinition/FoodAllergy)

### Formal Views of Profile Content

 [Description of Profiles, Differentials, Snapshots and how the different presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-FoodAllergy.csv), [Excel](StructureDefinition-FoodAllergy.xlsx), [Schematron](StructureDefinition-FoodAllergy.sch) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "FoodAllergy",
  "url" : "http://example.com/fhir/example/StructureDefinition/FoodAllergy",
  "version" : "0.1.0-test",
  "name" : "FoodAllergy",
  "title" : "Food Allergy",
  "status" : "active",
  "date" : "2026-04-20T22:37:21+00:00",
  "publisher" : "fnovillo",
  "contact" : [{
    "telecom" : [{
      "system" : "url",
      "value" : "mailto:fnovper@gmail.com"
    }]
  }],
  "description" : "Food Allergy profile",
  "jurisdiction" : [{
    "coding" : [{
      "system" : "http://unstats.un.org/unsd/methods/m49/m49.htm",
      "code" : "001"
    }]
  }],
  "fhirVersion" : "4.0.1",
  "mapping" : [{
    "identity" : "rim",
    "uri" : "http://hl7.org/v3",
    "name" : "RIM Mapping"
  },
  {
    "identity" : "w5",
    "uri" : "http://hl7.org/fhir/fivews",
    "name" : "FiveWs Pattern Mapping"
  },
  {
    "identity" : "v2",
    "uri" : "http://hl7.org/v2",
    "name" : "HL7 v2 Mapping"
  }],
  "kind" : "resource",
  "abstract" : false,
  "type" : "AllergyIntolerance",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/AllergyIntolerance",
  "derivation" : "constraint",
  "differential" : {
    "element" : [{
      "id" : "AllergyIntolerance",
      "path" : "AllergyIntolerance"
    },
    {
      "id" : "AllergyIntolerance.clinicalStatus",
      "path" : "AllergyIntolerance.clinicalStatus",
      "min" : 1,
      "mustSupport" : true
    },
    {
      "id" : "AllergyIntolerance.verificationStatus",
      "path" : "AllergyIntolerance.verificationStatus",
      "min" : 1,
      "mustSupport" : true
    },
    {
      "id" : "AllergyIntolerance.code",
      "path" : "AllergyIntolerance.code",
      "min" : 1,
      "mustSupport" : true,
      "binding" : {
        "strength" : "extensible",
        "valueSet" : "http://example.com/fhir/example/ValueSet/FoodAllergyVS"
      }
    },
    {
      "id" : "AllergyIntolerance.patient",
      "path" : "AllergyIntolerance.patient",
      "mustSupport" : true
    },
    {
      "id" : "AllergyIntolerance.recordedDate",
      "path" : "AllergyIntolerance.recordedDate",
      "mustSupport" : true
    },
    {
      "id" : "AllergyIntolerance.recorder",
      "path" : "AllergyIntolerance.recorder",
      "mustSupport" : true
    },
    {
      "id" : "AllergyIntolerance.asserter",
      "path" : "AllergyIntolerance.asserter",
      "mustSupport" : true
    },
    {
      "id" : "AllergyIntolerance.reaction",
      "path" : "AllergyIntolerance.reaction",
      "mustSupport" : true
    },
    {
      "id" : "AllergyIntolerance.reaction.extension",
      "path" : "AllergyIntolerance.reaction.extension",
      "slicing" : {
        "discriminator" : [{
          "type" : "value",
          "path" : "url"
        }],
        "ordered" : false,
        "rules" : "open"
      }
    },
    {
      "id" : "AllergyIntolerance.reaction.extension:certainty",
      "path" : "AllergyIntolerance.reaction.extension",
      "sliceName" : "certainty",
      "min" : 0,
      "max" : "1",
      "type" : [{
        "code" : "Extension",
        "profile" : ["http://hl7.org/fhir/StructureDefinition/allergyintolerance-certainty"]
      }],
      "mustSupport" : true
    },
    {
      "id" : "AllergyIntolerance.reaction.manifestation",
      "path" : "AllergyIntolerance.reaction.manifestation",
      "mustSupport" : true
    },
    {
      "id" : "AllergyIntolerance.reaction.exposureRoute",
      "path" : "AllergyIntolerance.reaction.exposureRoute",
      "mustSupport" : true
    },
    {
      "id" : "AllergyIntolerance.reaction.note",
      "path" : "AllergyIntolerance.reaction.note",
      "mustSupport" : true
    }]
  }
}

```
