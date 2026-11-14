Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UserData

Kotlin | [Java](https://developer.android.com/reference/android/service/autofill/UserData "View this page in Java")

```
class UserData : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.service.autofill.UserData](https://developer.android.com/reference/kotlin/android/service/autofill/UserData#) |

Defines the user data used for [field classification](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#FieldClassification).

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/service/autofill/UserData.Builder` A builder for `https://developer.android.com/reference/kotlin/android/service/autofill/UserData#` objects. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/autofill/UserData#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/service/autofill/UserData#getFieldClassificationAlgorithm()()` Gets the name of the default algorithm that is used to calculate `https://developer.android.com/reference/kotlin/android/service/autofill/FieldClassification.Match#getScore()` match scores}. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/service/autofill/UserData#getFieldClassificationAlgorithmForCategory(kotlin.String)(categoryId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Gets the name of the algorithm corresponding to the specific autofill category that is used to calculate `https://developer.android.com/reference/kotlin/android/service/autofill/FieldClassification.Match#getScore()` |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/service/autofill/UserData#getId()()` Gets the id. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/autofill/UserData#getMaxCategoryCount()()` Gets the maximum number of unique category ids that can be passed to the builder's constructor and `https://developer.android.com/reference/kotlin/android/service/autofill/UserData.Builder#add(kotlin.String,%20kotlin.String)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/autofill/UserData#getMaxFieldClassificationIdsSize()()` Gets the maximum number of ids that can be passed to `https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.Builder#setFieldClassificationIds(android.view.autofill.AutofillId)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/autofill/UserData#getMaxUserDataSize()()` Gets the maximum number of values that can be added to a `https://developer.android.com/reference/kotlin/android/service/autofill/UserData#`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/autofill/UserData#getMaxValueLength()()` Gets the maximum length of values passed to the builder's constructor or or `https://developer.android.com/reference/kotlin/android/service/autofill/UserData.Builder#add(kotlin.String,%20kotlin.String)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/autofill/UserData#getMinValueLength()()` Gets the minimum length of values passed to the builder's constructor or or `https://developer.android.com/reference/kotlin/android/service/autofill/UserData.Builder#add(kotlin.String,%20kotlin.String)`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/service/autofill/UserData#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/service/autofill/UserData#writeToParcel(android.os.Parcel,%20kotlin.Int)(parcel: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [UserData](https://developer.android.com/reference/kotlin/android/service/autofill/UserData#)!\> | `https://developer.android.com/reference/kotlin/android/service/autofill/UserData#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getFieldClassificationAlgorithm

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFieldClassificationAlgorithm(): String?
```

Gets the name of the default algorithm that is used to calculate `https://developer.android.com/reference/kotlin/android/service/autofill/FieldClassification.Match#getScore()` match scores}.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### getFieldClassificationAlgorithmForCategory

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFieldClassificationAlgorithmForCategory(categoryId: String): String?
```

Gets the name of the algorithm corresponding to the specific autofill category that is used to calculate `https://developer.android.com/reference/kotlin/android/service/autofill/FieldClassification.Match#getScore()`

| Parameters ||
|---|---|
| `categoryId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): autofill field category. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | String name of algorithm, null if none found. |

### getId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getId(): String!
```

Gets the id.

### getMaxCategoryCount

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getMaxCategoryCount(): Int
```

Gets the maximum number of unique category ids that can be passed to the builder's constructor and `https://developer.android.com/reference/kotlin/android/service/autofill/UserData.Builder#add(kotlin.String,%20kotlin.String)`.

### getMaxFieldClassificationIdsSize

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getMaxFieldClassificationIdsSize(): Int
```

Gets the maximum number of ids that can be passed to `https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.Builder#setFieldClassificationIds(android.view.autofill.AutofillId)`.

### getMaxUserDataSize

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getMaxUserDataSize(): Int
```

Gets the maximum number of values that can be added to a `https://developer.android.com/reference/kotlin/android/service/autofill/UserData#`.

### getMaxValueLength

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getMaxValueLength(): Int
```

Gets the maximum length of values passed to the builder's constructor or or `https://developer.android.com/reference/kotlin/android/service/autofill/UserData.Builder#add(kotlin.String,%20kotlin.String)`.

### getMinValueLength

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getMinValueLength(): Int
```

Gets the minimum length of values passed to the builder's constructor or or `https://developer.android.com/reference/kotlin/android/service/autofill/UserData.Builder#add(kotlin.String,%20kotlin.String)`.

### toString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<UserData!>
```
