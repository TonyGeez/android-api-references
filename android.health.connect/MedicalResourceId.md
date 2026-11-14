# MedicalResourceId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

# MedicalResourceId

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/MedicalResourceId "View this page in Java") 

```
class MedicalResourceId : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.health.connect.MedicalResourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#) |

A class to represent a unique identifier of a medical resource.

This class contains a set of properties that together represent a unique identifier of a medical resource.

The medical resource data representation follows the [Fast Healthcare Interoperability Resources (FHIR)](https://hl7.org/fhir/) standard.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MedicalResourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#MedicalResourceId(kotlin.String,%20kotlin.Int,%20kotlin.String))`(`dataSourceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `fhirResourceType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fhirResourceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructs a new [MedicalResourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#) instance. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| static [MedicalResourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#) | [fromFhirReference](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#fromFhirReference(kotlin.String,%20kotlin.String))`(`dataSourceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `fhirReference:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Creates a [MedicalResourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#) instance from`dataSourceId`and`fhirReference`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getDataSourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#getDataSourceId())`()` Returns the unique [MedicalDataSource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource) ID of where the data comes from. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getFhirResourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#getFhirResourceId())`()` Returns the FHIR resource ID. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFhirResourceType](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#getFhirResourceType())`()` Returns the FHIR resource type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [MedicalResourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### MedicalResourceId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
MedicalResourceId(
    dataSourceId: String, 
    fhirResourceType: Int, 
    fhirResourceId: String)
```

Constructs a new [MedicalResourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#) instance.

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataSourceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The unique identifier of the existing [MedicalDataSource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource), representing where the data comes from. This value cannot be`null`. |
| `fhirResourceType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The FHIR resource type. This is the "resourceType" field from a JSON representation of FHIR resource data. Value is [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_IMMUNIZATION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_IMMUNIZATION:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_ALLERGY_INTOLERANCE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_ALLERGY_INTOLERANCE:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_OBSERVATION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_OBSERVATION:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_CONDITION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_CONDITION:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PROCEDURE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_PROCEDURE:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_MEDICATION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_MEDICATION:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_MEDICATION_REQUEST](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_MEDICATION_REQUEST:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_MEDICATION_STATEMENT](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_MEDICATION_STATEMENT:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PATIENT](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_PATIENT:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PRACTITIONER](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_PRACTITIONER:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PRACTITIONER_ROLE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_PRACTITIONER_ROLE:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_ENCOUNTER](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_ENCOUNTER:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_LOCATION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_LOCATION:kotlin.Int), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_ORGANIZATION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource#FHIR_RESOURCE_TYPE_ORGANIZATION:kotlin.Int), or android.health.connect.datatypes.FhirResource.FHIR_RESOURCE_TYPE_DEVICE |
| `fhirResourceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The FHIR resource ID. This is the "id" field from a JSON representation of FHIR resource data. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the provided`dataSourceId`is not a valid ID, or`fhirResourceType`is not a valid supported type. |

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

### fromFhirReference

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static fun fromFhirReference(
    dataSourceId: String, 
    fhirReference: String
): MedicalResourceId
```

Creates a [MedicalResourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#) instance from`dataSourceId`and`fhirReference`.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataSourceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The unique identifier of the existing [MedicalDataSource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource), representing where the data comes from. This value cannot be`null`. |
| `fhirReference` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The FHIR reference string typically extracted from the "reference" field in one FHIR resource (source), pointing to another FHIR resource (target) within the same data source, for example "Patient/034AB16". This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MedicalResourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId#) | This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the provided`dataSourceId`is not a valid ID, the referenced resource type is not a valid [FhirResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource) type supported by Health Connect, or`fhirReference`does not match with the pattern of`$fhir_resource_type/$fhir_resource_id`, where the FHIR resource type should align with the resource list in [the official FHIR website](https://build.fhir.org/resourcelist.html), and the FHIR resource ID should also follow the pattern described in [the official FHIR datatypes](https://build.fhir.org/datatypes.html#id). |

### getDataSourceId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
fun getDataSourceId(): String
```

Returns the unique [MedicalDataSource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource) ID of where the data comes from.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getFhirResourceId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
fun getFhirResourceId(): String
```

Returns the FHIR resource ID.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getFhirResourceType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
fun getFhirResourceType(): Int
```

Returns the FHIR resource type.

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
static val CREATOR: Parcelable.Creator<MedicalResourceId!>
```
