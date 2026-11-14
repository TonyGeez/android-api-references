# AdSelectionSignals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# AdSelectionSignals

Kotlin| [Java](AdSelectionSignals.md) 
| --- | --- |

```
class AdSelectionSignals : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.common.AdSelectionSignals](AdSelectionSignals.md) |

This class holds JSON that will be passed into a JavaScript function during ad selection. Its contents are not used by [FLEDGE](https://developer.android.com/design-for-safety/privacy-sandbox/fledge) platform code, but are merely validated and then passed to the appropriate JavaScript ad selection function.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](AdSelectionSignals.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](AdSelectionSignals.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this AdSelectionSignals to the specified object. |
| static [AdSelectionSignals](AdSelectionSignals.md) | [fromString](AdSelectionSignals.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Creates an AdSelectionSignals from a given JSON in String form. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](AdSelectionSignals.md))`()` Returns a hash code corresponding to the string representation of this class obtained by calling [toString()](AdSelectionSignals.md)). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](AdSelectionSignals.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](AdSelectionSignals.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AdSelectionSignals](AdSelectionSignals.md)!\> | [CREATOR](AdSelectionSignals.md) <br /> |
| static [AdSelectionSignals](AdSelectionSignals.md)! | [EMPTY](AdSelectionSignals.md) <br /> |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this AdSelectionSignals to the specified object. The result is true if and only if the argument is not null and is a AdSelectionSignals object with the same string form (obtained by calling [toString()](AdSelectionSignals.md))). Note that this method will not perform any JSON normalization so two AdSelectionSignals objects with the same JSON could be not equal if the String representations of the objects was not equal.

| Parameters ||
|-------|-------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | The object to compare this AdSelectionSignals against |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the given object represents an AdSelectionSignals equivalent to this AdSelectionSignals, false otherwise |

### fromString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
static fun fromString(source: String): AdSelectionSignals
```

Creates an AdSelectionSignals from a given JSON in String form.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):Any valid JSON string to create the AdSelectionSignals with. This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [AdSelectionSignals](AdSelectionSignals.md) | An AdSelectionSignals object wrapping the given String. This value cannot be`null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code corresponding to the string representation of this class obtained by calling [toString()](AdSelectionSignals.md)). Note that this method will not perform any JSON normalization so two AdSelectionSignals objects with the same JSON could have different hash codes if the underlying string representation was different.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The String form of the JSON wrapped by this class. This value cannot be`null`. |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
static val CREATOR: Parcelable.Creator<AdSelectionSignals!>
```  

### EMPTY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
static val EMPTY: AdSelectionSignals!
```
