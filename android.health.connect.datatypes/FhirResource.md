# FhirResource

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

# FhirResource

Kotlin| [Java](FhirResource.md) 
| --- | --- |

```
class FhirResource : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.datatypes.FhirResource](FhirResource.md) |

A class to capture the FHIR resource data. This is the class used for all supported FHIR resource types, which is a subset of the resource list on [the official FHIR website](https://build.fhir.org/resourcelist.html). The list of supported types will likely expand in future releases.

FHIR stands for the [Fast Healthcare Interoperability Resources](https://hl7.org/fhir/) standard.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/health/connect/datatypes/FhirResource.Builder.md) Builder class for [FhirResource](FhirResource.md). |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_ALLERGY_INTOLERANCE](FhirResource.md) FHIR resource type for [AllergyIntolerance](https://www.hl7.org/fhir/allergyintolerance.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_CONDITION](FhirResource.md) FHIR resource type for a [FHIR Condition](https://www.hl7.org/fhir/condition.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_ENCOUNTER](FhirResource.md) FHIR resource type for a [FHIR Encounter](https://www.hl7.org/fhir/encounter.html). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_IMMUNIZATION](FhirResource.md) FHIR resource type for [Immunization](https://www.hl7.org/fhir/immunization.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_LOCATION](FhirResource.md) FHIR resource type for a [FHIR Location](https://www.hl7.org/fhir/location.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_MEDICATION](FhirResource.md) FHIR resource type for a [FHIR Medication](https://www.hl7.org/fhir/medication.html). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_MEDICATION_REQUEST](FhirResource.md) FHIR resource type for a [FHIR MedicationRequest](https://www.hl7.org/fhir/medicationrequest.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_MEDICATION_STATEMENT](FhirResource.md) FHIR resource type for a [FHIR MedicationStatement](https://www.hl7.org/fhir/medicationstatement.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_OBSERVATION](FhirResource.md) FHIR resource type for a [FHIR Observation](https://www.hl7.org/fhir/observation.html). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_ORGANIZATION](FhirResource.md) FHIR resource type for a [FHIR Organization](https://www.hl7.org/fhir/organization.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_PATIENT](FhirResource.md) FHIR resource type for a [FHIR Patient](https://www.hl7.org/fhir/patient.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_PRACTITIONER](FhirResource.md) FHIR resource type for a [FHIR Practitioner](https://www.hl7.org/fhir/practitioner.html). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_PRACTITIONER_ROLE](FhirResource.md) FHIR resource type for a [FHIR PractitionerRole](https://www.hl7.org/fhir/practitionerrole.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_PROCEDURE](FhirResource.md) FHIR resource type for a [FHIR Procedure](https://www.hl7.org/fhir/procedure.html). |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](FhirResource.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](FhirResource.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getData](FhirResource.md))`()` Returns the FHIR resource data in JSON representation. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getId](FhirResource.md))`()` Returns the FHIR resource ID. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](FhirResource.md))`()` Returns the FHIR resource type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](FhirResource.md))`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](FhirResource.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](FhirResource.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [FhirResource](FhirResource.md)!\> | [CREATOR](FhirResource.md) <br /> |

## Constants

### FHIR_RESOURCE_TYPE_ALLERGY_INTOLERANCE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val FHIR_RESOURCE_TYPE_ALLERGY_INTOLERANCE: Int
```

FHIR resource type for [AllergyIntolerance](https://www.hl7.org/fhir/allergyintolerance.html). 

 Value: 2

### FHIR_RESOURCE_TYPE_CONDITION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val FHIR_RESOURCE_TYPE_CONDITION: Int
```

FHIR resource type for a [FHIR Condition](https://www.hl7.org/fhir/condition.html). 

 Value: 4

### FHIR_RESOURCE_TYPE_ENCOUNTER

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val FHIR_RESOURCE_TYPE_ENCOUNTER: Int
```

FHIR resource type for a [FHIR Encounter](https://www.hl7.org/fhir/encounter.html). 

 Value: 12

### FHIR_RESOURCE_TYPE_IMMUNIZATION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val FHIR_RESOURCE_TYPE_IMMUNIZATION: Int
```

FHIR resource type for [Immunization](https://www.hl7.org/fhir/immunization.html). 

 Value: 1

### FHIR_RESOURCE_TYPE_LOCATION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val FHIR_RESOURCE_TYPE_LOCATION: Int
```

FHIR resource type for a [FHIR Location](https://www.hl7.org/fhir/location.html). 

 Value: 13

### FHIR_RESOURCE_TYPE_MEDICATION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val FHIR_RESOURCE_TYPE_MEDICATION: Int
```

FHIR resource type for a [FHIR Medication](https://www.hl7.org/fhir/medication.html). 

 Value: 6

### FHIR_RESOURCE_TYPE_MEDICATION_REQUEST

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val FHIR_RESOURCE_TYPE_MEDICATION_REQUEST: Int
```

FHIR resource type for a [FHIR MedicationRequest](https://www.hl7.org/fhir/medicationrequest.html). 

 Value: 7

### FHIR_RESOURCE_TYPE_MEDICATION_STATEMENT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val FHIR_RESOURCE_TYPE_MEDICATION_STATEMENT: Int
```

FHIR resource type for a [FHIR MedicationStatement](https://www.hl7.org/fhir/medicationstatement.html). 

 Value: 8

### FHIR_RESOURCE_TYPE_OBSERVATION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val FHIR_RESOURCE_TYPE_OBSERVATION: Int
```

FHIR resource type for a [FHIR Observation](https://www.hl7.org/fhir/observation.html). 

 Value: 3

### FHIR_RESOURCE_TYPE_ORGANIZATION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val FHIR_RESOURCE_TYPE_ORGANIZATION: Int
```

FHIR resource type for a [FHIR Organization](https://www.hl7.org/fhir/organization.html). 

 Value: 14

### FHIR_RESOURCE_TYPE_PATIENT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val FHIR_RESOURCE_TYPE_PATIENT: Int
```

FHIR resource type for a [FHIR Patient](https://www.hl7.org/fhir/patient.html). 

 Value: 9

### FHIR_RESOURCE_TYPE_PRACTITIONER

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val FHIR_RESOURCE_TYPE_PRACTITIONER: Int
```

FHIR resource type for a [FHIR Practitioner](https://www.hl7.org/fhir/practitioner.html). 

 Value: 10

### FHIR_RESOURCE_TYPE_PRACTITIONER_ROLE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val FHIR_RESOURCE_TYPE_PRACTITIONER_ROLE: Int
```

FHIR resource type for a [FHIR PractitionerRole](https://www.hl7.org/fhir/practitionerrole.html). 

 Value: 11

### FHIR_RESOURCE_TYPE_PROCEDURE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val FHIR_RESOURCE_TYPE_PROCEDURE: Int
```

FHIR resource type for a [FHIR Procedure](https://www.hl7.org/fhir/procedure.html). 

 Value: 5

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### equals

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getData

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
fun getData(): String
```

Returns the FHIR resource data in JSON representation.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
fun getId(): String
```

Returns the FHIR resource ID. This is extracted from the "id" field in`data`. This is NOT a unique identifier among all [FhirResource](FhirResource.md) s.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
fun getType(): Int
```

Returns the FHIR resource type. This is extracted from the "resourceType" field in [getData](FhirResource.md)).

The list of supported types is a subset of the resource list on [the official FHIR website](https://build.fhir.org/resourcelist.html). For a list of supported types, see the [FhirResource](FhirResource.md) constants, such as [FHIR_RESOURCE_TYPE_IMMUNIZATION](FhirResource.md). Clients should be aware that this list is non exhaustive and may increase in future releases when additional types will need to be handled.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_IMMUNIZATION](FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_ALLERGY_INTOLERANCE](FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_OBSERVATION](FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_CONDITION](FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PROCEDURE](FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_MEDICATION](FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_MEDICATION_REQUEST](FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_MEDICATION_STATEMENT](FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PATIENT](FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PRACTITIONER](FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PRACTITIONER_ROLE](FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_ENCOUNTER](FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_LOCATION](FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_ORGANIZATION](FhirResource.md), or android.health.connect.datatypes.FhirResource.FHIR_RESOURCE_TYPE_DEVICE |

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val CREATOR: Parcelable.Creator<FhirResource!>
```
