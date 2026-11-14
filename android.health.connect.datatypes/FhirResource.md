# FhirResource

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

# FhirResource

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/datatypes/FhirResource "View this page in Java") 

```
class FhirResource : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.health.connect.datatypes.FhirResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#) |

A class to capture the FHIR resource data. This is the class used for all supported FHIR resource types, which is a subset of the resource list on [the official FHIR website](https://build.fhir.org/resourcelist.html). The list of supported types will likely expand in future releases.

FHIR stands for the [Fast Healthcare Interoperability Resources](https://hl7.org/fhir/) standard.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource.Builder) Builder class for [FhirResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#). |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_ALLERGY_INTOLERANCE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_ALLERGY_INTOLERANCE:kotlin.Int) FHIR resource type for [AllergyIntolerance](https://www.hl7.org/fhir/allergyintolerance.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_CONDITION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_CONDITION:kotlin.Int) FHIR resource type for a [FHIR Condition](https://www.hl7.org/fhir/condition.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_ENCOUNTER](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_ENCOUNTER:kotlin.Int) FHIR resource type for a [FHIR Encounter](https://www.hl7.org/fhir/encounter.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_IMMUNIZATION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_IMMUNIZATION:kotlin.Int) FHIR resource type for [Immunization](https://www.hl7.org/fhir/immunization.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_LOCATION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_LOCATION:kotlin.Int) FHIR resource type for a [FHIR Location](https://www.hl7.org/fhir/location.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_MEDICATION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_MEDICATION:kotlin.Int) FHIR resource type for a [FHIR Medication](https://www.hl7.org/fhir/medication.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_MEDICATION_REQUEST](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_MEDICATION_REQUEST:kotlin.Int) FHIR resource type for a [FHIR MedicationRequest](https://www.hl7.org/fhir/medicationrequest.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_MEDICATION_STATEMENT](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_MEDICATION_STATEMENT:kotlin.Int) FHIR resource type for a [FHIR MedicationStatement](https://www.hl7.org/fhir/medicationstatement.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_OBSERVATION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_OBSERVATION:kotlin.Int) FHIR resource type for a [FHIR Observation](https://www.hl7.org/fhir/observation.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_ORGANIZATION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_ORGANIZATION:kotlin.Int) FHIR resource type for a [FHIR Organization](https://www.hl7.org/fhir/organization.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_PATIENT](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_PATIENT:kotlin.Int) FHIR resource type for a [FHIR Patient](https://www.hl7.org/fhir/patient.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_PRACTITIONER](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_PRACTITIONER:kotlin.Int) FHIR resource type for a [FHIR Practitioner](https://www.hl7.org/fhir/practitioner.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_PRACTITIONER_ROLE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_PRACTITIONER_ROLE:kotlin.Int) FHIR resource type for a [FHIR PractitionerRole](https://www.hl7.org/fhir/practitionerrole.html). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FHIR_RESOURCE_TYPE_PROCEDURE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_PROCEDURE:kotlin.Int) FHIR resource type for a [FHIR Procedure](https://www.hl7.org/fhir/procedure.html). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getData](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#getData())`()` Returns the FHIR resource data in JSON representation. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getId](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#getId())`()` Returns the FHIR resource ID. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#getType())`()` Returns the FHIR resource type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [FhirResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#CREATOR:android.os.Parcelable.Creator) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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

Returns the FHIR resource ID. This is extracted from the "id" field in`data`. This is NOT a unique identifier among all [FhirResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#) s.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
fun getType(): Int
```

Returns the FHIR resource type. This is extracted from the "resourceType" field in [getData](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#getData()).

The list of supported types is a subset of the resource list on [the official FHIR website](https://build.fhir.org/resourcelist.html). For a list of supported types, see the [FhirResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#) constants, such as [FHIR_RESOURCE_TYPE_IMMUNIZATION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_IMMUNIZATION:kotlin.Int). Clients should be aware that this list is non exhaustive and may increase in future releases when additional types will need to be handled.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_IMMUNIZATION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_IMMUNIZATION:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_ALLERGY_INTOLERANCE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_ALLERGY_INTOLERANCE:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_OBSERVATION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_OBSERVATION:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_CONDITION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_CONDITION:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PROCEDURE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_PROCEDURE:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_MEDICATION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_MEDICATION:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_MEDICATION_REQUEST](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_MEDICATION_REQUEST:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_MEDICATION_STATEMENT](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_MEDICATION_STATEMENT:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PATIENT](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_PATIENT:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PRACTITIONER](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_PRACTITIONER:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PRACTITIONER_ROLE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_PRACTITIONER_ROLE:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_ENCOUNTER](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_ENCOUNTER:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_LOCATION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_LOCATION:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_ORGANIZATION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_ORGANIZATION:kotlin.Int), or android.health.connect.datatypes.FhirResource.FHIR_RESOURCE_TYPE_DEVICE |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val CREATOR: Parcelable.Creator<FhirResource!>
```
