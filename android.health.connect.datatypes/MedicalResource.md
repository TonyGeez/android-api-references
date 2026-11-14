# MedicalResource

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

# MedicalResource

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/datatypes/MedicalResource "View this page in Java") 

```
class MedicalResource : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.health.connect.datatypes.MedicalResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#) |

A class to capture the user's medical data. This is the class used for all medical resource types.

The data representation follows the [Fast Healthcare Interoperability Resources (FHIR)](https://hl7.org/fhir/) standard.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource.Builder) Builder class for [MedicalResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#). |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDICAL_RESOURCE_TYPE_ALLERGIES_INTOLERANCES](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_ALLERGIES_INTOLERANCES:kotlin.Int) Medical resource type labelling data as allergies or intolerances. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDICAL_RESOURCE_TYPE_CONDITIONS](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_CONDITIONS:kotlin.Int) Medical resource type labelling data as medical conditions (clinical condition, problem, diagnosis etc). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDICAL_RESOURCE_TYPE_LABORATORY_RESULTS](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_LABORATORY_RESULTS:kotlin.Int) Medical resource type labelling data as results (Laboratory or pathology). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDICAL_RESOURCE_TYPE_MEDICATIONS](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_MEDICATIONS:kotlin.Int) Medical resource type labelling data as medication related. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDICAL_RESOURCE_TYPE_PERSONAL_DETAILS](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_PERSONAL_DETAILS:kotlin.Int) Medical resource type labelling data as related to personal details, including demographic information such as name, date of birth, and contact details such as address or telephone numbers. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDICAL_RESOURCE_TYPE_PRACTITIONER_DETAILS](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_PRACTITIONER_DETAILS:kotlin.Int) Medical resource type labelling data as related to practitioners. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDICAL_RESOURCE_TYPE_PREGNANCY](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_PREGNANCY:kotlin.Int) Medical resource type labelling data as to do with pregnancy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDICAL_RESOURCE_TYPE_PROCEDURES](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_PROCEDURES:kotlin.Int) Medical resource type labelling data as procedures (actions taken on or for a patient). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDICAL_RESOURCE_TYPE_SOCIAL_HISTORY](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_SOCIAL_HISTORY:kotlin.Int) Medical resource type labelling data as social history. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDICAL_RESOURCE_TYPE_VACCINES](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_VACCINES:kotlin.Int) Medical resource type labelling data as vaccines. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDICAL_RESOURCE_TYPE_VISITS](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_VISITS:kotlin.Int) Medical resource type labelling data as related to an encounter with a practitioner. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEDICAL_RESOURCE_TYPE_VITAL_SIGNS](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_VITAL_SIGNS:kotlin.Int) Medical resource type labelling data as vital signs. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getDataSourceId](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#getDataSourceId())`()` Returns the unique [MedicalDataSource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource) ID of where the data comes from. |
| [FhirResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource) | [getFhirResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#getFhirResource())`()` Returns the enclosed [FhirResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource) object. |
| [FhirVersion](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirVersion) | [getFhirVersion](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#getFhirVersion())`()` Returns the FHIR version being used for`mFhirResource` |
| [MedicalResourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId.html#) | [getId](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#getId())`()` Returns the ID of this [MedicalResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#) as [MedicalResourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId.html#). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#getType())`()` Returns the medical resource type, assigned by the Android Health Platform at insertion time. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [MedicalResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### MEDICAL_RESOURCE_TYPE_ALLERGIES_INTOLERANCES

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val MEDICAL_RESOURCE_TYPE_ALLERGIES_INTOLERANCES: Int
```

Medical resource type labelling data as allergies or intolerances. 

 Value: 2

### MEDICAL_RESOURCE_TYPE_CONDITIONS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val MEDICAL_RESOURCE_TYPE_CONDITIONS: Int
```

Medical resource type labelling data as medical conditions (clinical condition, problem, diagnosis etc). 

 Value: 7

### MEDICAL_RESOURCE_TYPE_LABORATORY_RESULTS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val MEDICAL_RESOURCE_TYPE_LABORATORY_RESULTS: Int
```

Medical resource type labelling data as results (Laboratory or pathology). 

 Value: 6

### MEDICAL_RESOURCE_TYPE_MEDICATIONS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val MEDICAL_RESOURCE_TYPE_MEDICATIONS: Int
```

Medical resource type labelling data as medication related. 

 Value: 9

### MEDICAL_RESOURCE_TYPE_PERSONAL_DETAILS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val MEDICAL_RESOURCE_TYPE_PERSONAL_DETAILS: Int
```

Medical resource type labelling data as related to personal details, including demographic information such as name, date of birth, and contact details such as address or telephone numbers. 

 Value: 10

### MEDICAL_RESOURCE_TYPE_PRACTITIONER_DETAILS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val MEDICAL_RESOURCE_TYPE_PRACTITIONER_DETAILS: Int
```

Medical resource type labelling data as related to practitioners. This is information about the doctors, nurses, masseurs, physios, etc who have been involved with the user. 

 Value: 11

### MEDICAL_RESOURCE_TYPE_PREGNANCY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val MEDICAL_RESOURCE_TYPE_PREGNANCY: Int
```

Medical resource type labelling data as to do with pregnancy. 

 Value: 3

### MEDICAL_RESOURCE_TYPE_PROCEDURES

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val MEDICAL_RESOURCE_TYPE_PROCEDURES: Int
```

Medical resource type labelling data as procedures (actions taken on or for a patient). 

 Value: 8

### MEDICAL_RESOURCE_TYPE_SOCIAL_HISTORY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val MEDICAL_RESOURCE_TYPE_SOCIAL_HISTORY: Int
```

Medical resource type labelling data as social history. 

 Value: 4

### MEDICAL_RESOURCE_TYPE_VACCINES

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val MEDICAL_RESOURCE_TYPE_VACCINES: Int
```

Medical resource type labelling data as vaccines. 

 Value: 1

### MEDICAL_RESOURCE_TYPE_VISITS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val MEDICAL_RESOURCE_TYPE_VISITS: Int
```

Medical resource type labelling data as related to an encounter with a practitioner. This includes visits to healthcare providers and remote encounters such as telephone and videoconference appointments, and information about the time, location and organization who is being met. 

 Value: 12

### MEDICAL_RESOURCE_TYPE_VITAL_SIGNS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
static val MEDICAL_RESOURCE_TYPE_VITAL_SIGNS: Int
```

Medical resource type labelling data as vital signs. 

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

### getFhirResource

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
fun getFhirResource(): FhirResource
```

Returns the enclosed [FhirResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource) object.

| Return ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------|
| [FhirResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource) | This value cannot be`null`. |

### getFhirVersion

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
fun getFhirVersion(): FhirVersion
```

Returns the FHIR version being used for`mFhirResource`

| Return ||
|------------------------------------------------------------------------------------------------------------|-----------------------------|
| [FhirVersion](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirVersion) | This value cannot be`null`. |

### getId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
fun getId(): MedicalResourceId
```

Returns the ID of this [MedicalResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#) as [MedicalResourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId.html#).

| Return ||
|--------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MedicalResourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId.html#) | This value cannot be`null`. |

### getType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions) 

```
fun getType(): Int
```

Returns the medical resource type, assigned by the Android Health Platform at insertion time.

For a list of supported types, see the [MedicalResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#) type constants, such as [MEDICAL_RESOURCE_TYPE_VACCINES](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_VACCINES:kotlin.Int). Clients should be aware that this list is non exhaustive and may increase in future releases when additional types will need to be handled.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.health.connect.datatypes.MedicalResource#MEDICAL_RESOURCE_TYPE_ALLERGIES_INTOLERANCES](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_ALLERGIES_INTOLERANCES:kotlin.Int), [android.health.connect.datatypes.MedicalResource#MEDICAL_RESOURCE_TYPE_CONDITIONS](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_CONDITIONS:kotlin.Int), [android.health.connect.datatypes.MedicalResource#MEDICAL_RESOURCE_TYPE_LABORATORY_RESULTS](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_LABORATORY_RESULTS:kotlin.Int), [android.health.connect.datatypes.MedicalResource#MEDICAL_RESOURCE_TYPE_MEDICATIONS](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_MEDICATIONS:kotlin.Int), [android.health.connect.datatypes.MedicalResource#MEDICAL_RESOURCE_TYPE_PERSONAL_DETAILS](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_PERSONAL_DETAILS:kotlin.Int), [android.health.connect.datatypes.MedicalResource#MEDICAL_RESOURCE_TYPE_PRACTITIONER_DETAILS](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_PRACTITIONER_DETAILS:kotlin.Int), [android.health.connect.datatypes.MedicalResource#MEDICAL_RESOURCE_TYPE_PREGNANCY](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_PREGNANCY:kotlin.Int), [android.health.connect.datatypes.MedicalResource#MEDICAL_RESOURCE_TYPE_PROCEDURES](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_PROCEDURES:kotlin.Int), [android.health.connect.datatypes.MedicalResource#MEDICAL_RESOURCE_TYPE_SOCIAL_HISTORY](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_SOCIAL_HISTORY:kotlin.Int), [android.health.connect.datatypes.MedicalResource#MEDICAL_RESOURCE_TYPE_VACCINES](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_VACCINES:kotlin.Int), [android.health.connect.datatypes.MedicalResource#MEDICAL_RESOURCE_TYPE_VISITS](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_VISITS:kotlin.Int), [android.health.connect.datatypes.MedicalResource#MEDICAL_RESOURCE_TYPE_VITAL_SIGNS](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource#MEDICAL_RESOURCE_TYPE_VITAL_SIGNS:kotlin.Int), or android.health.connect.datatypes.MedicalResource.MEDICAL_RESOURCE_TYPE_DEVICES |

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
static val CREATOR: Parcelable.Creator<MedicalResource!>
```
