# Food Allergies - Food Allergies FHIR Implementation Guide v0.1.0-test

* [**Table of Contents**](toc.md)
* [**Artifacts Summary**](artifacts.md)
* **Food Allergies**

## ValueSet: Food Allergies 

| | |
| :--- | :--- |
| *Official URL*:http://example.com/fhir/example/ValueSet/FoodAllergyVS | *Version*:0.1.0-test |
| Active as of 2026-04-20 | *Computable Name*:FoodAllergyVS |

 
Main Food allergies. 

 **References** 

* [Food Allergy](StructureDefinition-FoodAllergy.md)

### Logical Definition (CLD)

 

### Expansion

-------

 Explanation of the columns that may appear on this page: 

| | |
| :--- | :--- |
| Level | A few code lists that FHIR defines are hierarchical - each code is assigned a level. In this scheme, some codes are under other codes, and imply that the code they are under also applies |
| System | The source of the definition of the code (when the value set draws in codes defined elsewhere) |
| Code | The code (used as the code in the resource instance) |
| Display | The display (used in the*display*element of a[Coding](http://hl7.org/fhir/R4/datatypes.html#Coding)). If there is no display, implementers should not simply display the code, but map the concept into their application |
| Definition | An explanation of the meaning of the concept |
| Comments | Additional notes about how to use the code |



## Resource Content

```json
{
  "resourceType" : "ValueSet",
  "id" : "FoodAllergyVS",
  "url" : "http://example.com/fhir/example/ValueSet/FoodAllergyVS",
  "version" : "0.1.0-test",
  "name" : "FoodAllergyVS",
  "title" : "Food Allergies",
  "status" : "active",
  "date" : "2026-04-20T22:37:21+00:00",
  "publisher" : "fnovillo",
  "contact" : [{
    "telecom" : [{
      "system" : "url",
      "value" : "mailto:fnovper@gmail.com"
    }]
  }],
  "description" : "Main Food allergies.",
  "jurisdiction" : [{
    "coding" : [{
      "system" : "http://unstats.un.org/unsd/methods/m49/m49.htm",
      "code" : "001"
    }]
  }],
  "compose" : {
    "include" : [{
      "system" : "http://snomed.info/sct",
      "concept" : [{
        "code" : "91935009",
        "display" : "Allergy to peanut"
      },
      {
        "code" : "48821000119104",
        "display" : "Allergy to tree nut"
      },
      {
        "code" : "782555009",
        "display" : "Allergy to cow's milk protein"
      },
      {
        "code" : "213020009",
        "display" : "Allergy to egg protein"
      },
      {
        "code" : "417532002",
        "display" : "Allergy to fish"
      },
      {
        "code" : "300913006",
        "display" : "Allergy to shellfish"
      },
      {
        "code" : "782594005",
        "display" : "Allergy to soy protein"
      },
      {
        "code" : "260167008",
        "display" : "Sesame seed"
      },
      {
        "code" : "21191000122102",
        "display" : "Allergy to mustard"
      },
      {
        "code" : "712843002",
        "display" : "Allergy to celery"
      },
      {
        "code" : "782575000",
        "display" : "Allergy to lupine seed"
      }]
    }]
  }
}

```
