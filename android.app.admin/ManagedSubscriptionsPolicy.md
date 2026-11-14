# ManagedSubscriptionsPolicy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ManagedSubscriptionsPolicy

Kotlin| [Java](https://developer.android.com/reference/android/app/admin/ManagedSubscriptionsPolicy "View this page in Java") 

```
class ManagedSubscriptionsPolicy : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.admin.ManagedSubscriptionsPolicy](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy#) |

A policy class that describes how managed SIM subscriptions should behave on the device.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ALL_MANAGED_SUBSCRIPTIONS](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy#TYPE_ALL_MANAGED_SUBSCRIPTIONS:kotlin.Int) Represents policy to have only managed subscriptions on the device, any existing and future subscriptions on the device are exclusively associated with the managed profile. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ALL_PERSONAL_SUBSCRIPTIONS](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy#TYPE_ALL_PERSONAL_SUBSCRIPTIONS:kotlin.Int) Represents default policy to not have any managed subscriptions on the device. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ManagedSubscriptionsPolicy](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy#ManagedSubscriptionsPolicy(kotlin.Int))`(`policyType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPolicyType](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy#getPolicyType())`()` Returns the type of managed subscriptions policy, or [TYPE_ALL_PERSONAL_SUBSCRIPTIONS](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy#TYPE_ALL_PERSONAL_SUBSCRIPTIONS:kotlin.Int) if no policy has been set. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ManagedSubscriptionsPolicy](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### TYPE_ALL_MANAGED_SUBSCRIPTIONS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ALL_MANAGED_SUBSCRIPTIONS: Int
```

Represents policy to have only managed subscriptions on the device, any existing and future subscriptions on the device are exclusively associated with the managed profile.

When a subscription is associated with the managed profile, incoming/outgoing calls and text message using that subscription would only work via apps on managed profile. Also, Call logs and messages would be accessible only from the managed profile. 

 Value: 1

### TYPE_ALL_PERSONAL_SUBSCRIPTIONS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ALL_PERSONAL_SUBSCRIPTIONS: Int
```

Represents default policy to not have any managed subscriptions on the device. 

 Value: 0

## Public constructors

### ManagedSubscriptionsPolicy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ManagedSubscriptionsPolicy(policyType: Int)
```

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `policyType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.app.admin.ManagedSubscriptionsPolicy#TYPE_ALL_PERSONAL_SUBSCRIPTIONS](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy#TYPE_ALL_PERSONAL_SUBSCRIPTIONS:kotlin.Int), or [android.app.admin.ManagedSubscriptionsPolicy#TYPE_ALL_MANAGED_SUBSCRIPTIONS](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy#TYPE_ALL_MANAGED_SUBSCRIPTIONS:kotlin.Int) |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getPolicyType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPolicyType(): Int
```

Returns the type of managed subscriptions policy, or [TYPE_ALL_PERSONAL_SUBSCRIPTIONS](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy#TYPE_ALL_PERSONAL_SUBSCRIPTIONS:kotlin.Int) if no policy has been set.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The policy type. Value is [android.app.admin.ManagedSubscriptionsPolicy#TYPE_ALL_PERSONAL_SUBSCRIPTIONS](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy#TYPE_ALL_PERSONAL_SUBSCRIPTIONS:kotlin.Int), or [android.app.admin.ManagedSubscriptionsPolicy#TYPE_ALL_MANAGED_SUBSCRIPTIONS](https://developer.android.com/reference/kotlin/android/app/admin/ManagedSubscriptionsPolicy#TYPE_ALL_MANAGED_SUBSCRIPTIONS:kotlin.Int) |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ManagedSubscriptionsPolicy!>
```
