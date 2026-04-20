#  - Food Allergies FHIR Implementation Guide v0.1.0-test

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* ****

## AllergyIntolerance: 

Profile: [Food Allergy](StructureDefinition-FoodAllergy.md)

**clinicalStatus**: Active

**verificationStatus**: Unconfirmed

**code**: Allergy to peanut

**patient**: Paul Peters (Identifier: 8936584955)

**recordedDate**: 2021-07-28

**recorder**: Daniel Davis (Identifier: 8936584955)

**asserter**: Paul Peters (Identifier: 8936584955)



## Resource Content

```json
{
  "resourceType" : "AllergyIntolerance",
  "id" : "MyPeanutAllergy",
  "meta" : {
    "profile" : ["http://example.com/fhir/example/StructureDefinition/FoodAllergy"]
  },
  "clinicalStatus" : {
    "coding" : [{
      "system" : "http://terminology.hl7.org/CodeSystem/allergyintolerance-clinical",
      "code" : "active"
    }]
  },
  "verificationStatus" : {
    "coding" : [{
      "system" : "http://terminology.hl7.org/CodeSystem/allergyintolerance-verification",
      "code" : "unconfirmed"
    }]
  },
  "code" : {
    "coding" : [{
      "system" : "http://snomed.info/sct",
      "code" : "91935009",
      "display" : "Allergy to peanut"
    }]
  },
  "patient" : {
    "identifier" : {
      "value" : "8936584955"
    },
    "display" : "Paul Peters"
  },
  "recordedDate" : "2021-07-28",
  "recorder" : {
    "identifier" : {
      "value" : "8936584955"
    },
    "display" : "Daniel Davis"
  },
  "asserter" : {
    "identifier" : {
      "value" : "8936584955"
    },
    "display" : "Paul Peters"
  }
}

```
