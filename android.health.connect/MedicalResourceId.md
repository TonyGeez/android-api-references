# MedicalResourceId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

# MedicalResourceId

Kotlin| [Java](MedicalResourceId.md) 
| --- | --- |

```
class MedicalResourceId : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.MedicalResourceId](MedicalResourceId.md) |

A class to represent a unique identifier of a medical resource.

This class contains a set of properties that together represent a unique identifier of a medical resource.

The medical resource data representation follows the [Fast Healthcare Interoperability Resources (FHIR)](https://hl7.org/fhir/) standard.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MedicalResourceId](MedicalResourceId.md))`(`dataSourceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `fhirResourceType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fhirResourceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructs a new [MedicalResourceId](MedicalResourceId.md) instance. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](MedicalResourceId.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](MedicalResourceId.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| static [MedicalResourceId](MedicalResourceId.md) | [fromFhirReference](MedicalResourceId.md))`(`dataSourceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `fhirReference:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Creates a [MedicalResourceId](MedicalResourceId.md) instance from`dataSourceId`and`fhirReference`. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getDataSourceId](MedicalResourceId.md))`()` Returns the unique [MedicalDataSource](../android.health.connect.datatypes/MedicalDataSource.md) ID of where the data comes from. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getFhirResourceId](MedicalResourceId.md))`()` Returns the FHIR resource ID. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFhirResourceType](MedicalResourceId.md))`()` Returns the FHIR resource type. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](MedicalResourceId.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](MedicalResourceId.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](MedicalResourceId.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [MedicalResourceId](MedicalResourceId.md)!\> | [CREATOR](MedicalResourceId.md) <br /> |

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

Constructs a new [MedicalResourceId](MedicalResourceId.md) instance.

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataSourceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The unique identifier of the existing [MedicalDataSource](../android.health.connect.datatypes/MedicalDataSource.md), representing where the data comes from. This value cannot be`null`. |
| `fhirResourceType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The FHIR resource type. This is the "resourceType" field from a JSON representation of FHIR resource data. Value is [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_IMMUNIZATION](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_ALLERGY_INTOLERANCE](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_OBSERVATION](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_CONDITION](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PROCEDURE](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_MEDICATION](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_MEDICATION_REQUEST](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_MEDICATION_STATEMENT](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PATIENT](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PRACTITIONER](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PRACTITIONER_ROLE](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_ENCOUNTER](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_LOCATION](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_ORGANIZATION](../android.health.connect.datatypes/FhirResource.md), or android.health.connect.datatypes.FhirResource.FHIR_RESOURCE_TYPE_DEVICE |
| `fhirResourceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The FHIR resource ID. This is the "id" field from a JSON representation of FHIR resource data. This value cannot be`null`. |
| --- | --- |

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

### fromFhirReference

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static fun fromFhirReference(
    dataSourceId: String, 
    fhirReference: String
): MedicalResourceId
```

Creates a [MedicalResourceId](MedicalResourceId.md) instance from`dataSourceId`and`fhirReference`.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataSourceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The unique identifier of the existing [MedicalDataSource](../android.health.connect.datatypes/MedicalDataSource.md), representing where the data comes from. This value cannot be`null`. |
| `fhirReference` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The FHIR reference string typically extracted from the "reference" field in one FHIR resource (source), pointing to another FHIR resource (target) within the same data source, for example "Patient/034AB16". This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MedicalResourceId](MedicalResourceId.md) | This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the provided`dataSourceId`is not a valid ID, the referenced resource type is not a valid [FhirResource](../android.health.connect.datatypes/FhirResource.md) type supported by Health Connect, or`fhirReference`does not match with the pattern of`$fhir_resource_type/$fhir_resource_id`, where the FHIR resource type should align with the resource list in [the official FHIR website](https://build.fhir.org/resourcelist.html), and the FHIR resource ID should also follow the pattern described in [the official FHIR datatypes](https://build.fhir.org/datatypes.html#id). |

### getDataSourceId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
fun getDataSourceId(): String
```

Returns the unique [MedicalDataSource](../android.health.connect.datatypes/MedicalDataSource.md) ID of where the data comes from.

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_IMMUNIZATION](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_ALLERGY_INTOLERANCE](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_OBSERVATION](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_CONDITION](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PROCEDURE](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_MEDICATION](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_MEDICATION_REQUEST](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_MEDICATION_STATEMENT](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PATIENT](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PRACTITIONER](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_PRACTITIONER_ROLE](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_ENCOUNTER](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_LOCATION](../android.health.connect.datatypes/FhirResource.md), [android.health.connect.datatypes.FhirResource#FHIR_RESOURCE_TYPE_ORGANIZATION](../android.health.connect.datatypes/FhirResource.md), or android.health.connect.datatypes.FhirResource.FHIR_RESOURCE_TYPE_DEVICE |

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
static val CREATOR: Parcelable.Creator<MedicalResourceId!>
```
