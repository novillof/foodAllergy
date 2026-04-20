# Food Allergy Logical Model - Food Allergies FHIR Implementation Guide v0.1.0-test

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Food Allergy Logical Model**

## Logical Model: Food Allergy Logical Model 

| | |
| :--- | :--- |
| *Official URL*:http://example.com/fhir/example/StructureDefinition/FoodAllergyModel | *Version*:0.1.0-test |
| Active as of 2026-04-20 | *Computable Name*:FoodAllergyModel |

 
Food Allergy information model 

**Usages:**

* This Logical Model is not used by any profiles in this Implementation Guide

You can also check for [usages in the FHIR IG Statistics](https://packages2.fhir.org/xig/xxexample.fhir.food-Allergy|current/StructureDefinition/FoodAllergyModel)

### Formal Views of Profile Content

 [Description of Profiles, Differentials, Snapshots and how the different presentations work](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#structure-definitions). 

 

Other representations of profile: [CSV](StructureDefinition-FoodAllergyModel.csv), [Excel](StructureDefinition-FoodAllergyModel.xlsx) 



## Resource Content

```json
{
  "resourceType" : "StructureDefinition",
  "id" : "FoodAllergyModel",
  "url" : "http://example.com/fhir/example/StructureDefinition/FoodAllergyModel",
  "version" : "0.1.0-test",
  "name" : "FoodAllergyModel",
  "title" : "Food Allergy Logical Model",
  "status" : "active",
  "date" : "2026-04-20T22:37:21+00:00",
  "publisher" : "fnovillo",
  "contact" : [{
    "telecom" : [{
      "system" : "url",
      "value" : "mailto:fnovper@gmail.com"
    }]
  }],
  "description" : "Food Allergy information model",
  "jurisdiction" : [{
    "coding" : [{
      "system" : "http://unstats.un.org/unsd/methods/m49/m49.htm",
      "code" : "001"
    }]
  }],
  "fhirVersion" : "4.0.1",
  "kind" : "logical",
  "abstract" : false,
  "type" : "http://example.com/fhir/example/StructureDefinition/FoodAllergyModel",
  "baseDefinition" : "http://hl7.org/fhir/StructureDefinition/Base",
  "derivation" : "specialization",
  "differential" : {
    "element" : [{
      "id" : "FoodAllergyModel",
      "path" : "FoodAllergyModel",
      "short" : "Food Allergy Logical Model",
      "definition" : "Food Allergy information model"
    },
    {
      "id" : "FoodAllergyModel.patient",
      "path" : "FoodAllergyModel.patient",
      "short" : "The person that has the allergy",
      "definition" : "The person that has the allergy",
      "min" : 1,
      "max" : "1",
      "type" : [{
        "code" : "Reference"
      }]
    },
    {
      "id" : "FoodAllergyModel.allergen",
      "path" : "FoodAllergyModel.allergen",
      "short" : "The substance that the person is allergic to",
      "definition" : "The substance - from a lst of substances - that the person is allergic to. It is possible to use free text but for the products indicated, a code must be used",
      "min" : 1,
      "max" : "1",
      "type" : [{
        "code" : "CodeableConcept"
      }]
    },
    {
      "id" : "FoodAllergyModel.clinicalStatus",
      "path" : "FoodAllergyModel.clinicalStatus",
      "short" : "The status of the allergy - if it is active or resolved",
      "definition" : "The status of the allergy - if it is active or resolved",
      "min" : 1,
      "max" : "1",
      "type" : [{
        "code" : "CodeableConcept"
      }]
    },
    {
      "id" : "FoodAllergyModel.verificationStatus",
      "path" : "FoodAllergyModel.verificationStatus",
      "short" : "The verification status of the allergy - if it is confirmed or suspected or refuted",
      "definition" : "The verification status of the allergy - if it is confirmed or suspected or refuted",
      "min" : 1,
      "max" : "1",
      "type" : [{
        "code" : "CodeableConcept"
      }]
    },
    {
      "id" : "FoodAllergyModel.recordedDate",
      "path" : "FoodAllergyModel.recordedDate",
      "short" : "When the allergy was reported",
      "definition" : "When the allergy was reported",
      "min" : 0,
      "max" : "1",
      "type" : [{
        "code" : "dateTime"
      }]
    },
    {
      "id" : "FoodAllergyModel.recorder",
      "path" : "FoodAllergyModel.recorder",
      "short" : "Who recorded the allergy",
      "definition" : "Who recorded the allergy",
      "min" : 0,
      "max" : "1",
      "type" : [{
        "code" : "Reference"
      }]
    },
    {
      "id" : "FoodAllergyModel.asserter",
      "path" : "FoodAllergyModel.asserter",
      "short" : "Who asserted the allergy",
      "definition" : " who asserted or provided the allergy information e.g. the patient, a relative, a care giver...",
      "min" : 0,
      "max" : "1",
      "type" : [{
        "code" : "Reference"
      }]
    },
    {
      "id" : "FoodAllergyModel.reactions",
      "path" : "FoodAllergyModel.reactions",
      "short" : "known past reactions to the allergen",
      "definition" : "known past reactions to the allergen",
      "min" : 0,
      "max" : "1",
      "type" : [{
        "code" : "BackboneElement"
      }]
    },
    {
      "id" : "FoodAllergyModel.reactions.manifestation",
      "path" : "FoodAllergyModel.reactions.manifestation",
      "short" : "How the reaction manifested itself",
      "definition" : "How the reaction manifested itself, e.g. rash, breathing difficulty...",
      "min" : 0,
      "max" : "1",
      "type" : [{
        "code" : "CodeableConcept"
      }]
    },
    {
      "id" : "FoodAllergyModel.reactions.certitude",
      "path" : "FoodAllergyModel.reactions.certitude",
      "short" : "How certain we are that the cause of the reaction was the allergen indicated",
      "definition" : "How certain we are that the cause of the reaction was the allergen indicated",
      "min" : 0,
      "max" : "1",
      "type" : [{
        "code" : "CodeableConcept"
      }]
    },
    {
      "id" : "FoodAllergyModel.reactions.exposure",
      "path" : "FoodAllergyModel.reactions.exposure",
      "short" : "The exposure route to the substance",
      "definition" : "The exposure route to the substance",
      "min" : 0,
      "max" : "1",
      "type" : [{
        "code" : "CodeableConcept"
      }]
    },
    {
      "id" : "FoodAllergyModel.reactions.note",
      "path" : "FoodAllergyModel.reactions.note",
      "short" : "Additional text note about the allergic reaction",
      "definition" : "Additional text note about the allergic reaction",
      "min" : 0,
      "max" : "1",
      "type" : [{
        "code" : "string"
      }]
    }]
  }
}

```
