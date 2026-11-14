Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PackagePolicy

```
class PackagePolicy : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.admin.PackagePolicy](https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#) |

A generic class that defines which APK packages are in scope for some device policy.

The packages can be defined using either an allowlist or a blocklist. In allowlist mode, it could optionally include all system packages that meet the specific criteria of the device policy in question.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PACKAGE_POLICY_ALLOWLIST:kotlin.Int` PackagePolicy type indicator for `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#` |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PACKAGE_POLICY_ALLOWLIST_AND_SYSTEM:kotlin.Int` PackagePolicy type indicator for `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#` |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PACKAGE_POLICY_BLOCKLIST:kotlin.Int` PackagePolicy type indicator for `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#` |
| --- | --- |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PackagePolicy(kotlin.Int)(policyType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create the package policy |
| `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PackagePolicy(kotlin.Int,%20kotlin.collections.MutableSet)(policyType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, packageNames: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` Create the package policy |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#getPackageNames()()` Returns the list of packages to use as an allow/deny list based on policy type |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#getPolicyType()()` Returns the current policy type |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#hashCode()()` Returns a hash code value for the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PackagePolicy](https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#)!\> | `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### PACKAGE_POLICY_ALLOWLIST

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PACKAGE_POLICY_ALLOWLIST: Int
```

PackagePolicy type indicator for `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#`

This constant indicates that all packages are denied except for the packages returned by `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#getPackageNames()`, which acts as an allowlist.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PACKAGE_POLICY_BLOCKLIST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PACKAGE_POLICY_ALLOWLIST_AND_SYSTEM:kotlin.Int`

### PACKAGE_POLICY_ALLOWLIST_AND_SYSTEM

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PACKAGE_POLICY_ALLOWLIST_AND_SYSTEM: Int
```

PackagePolicy type indicator for `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#`

This constant indicates system packages are allowed in addition to the packages returned by `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#getPackageNames()`, which acts as an allowlist.

Functions that accept `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#` will further clarify how this policy is interpreted.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PACKAGE_POLICY_BLOCKLIST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PACKAGE_POLICY_ALLOWLIST:kotlin.Int`

### PACKAGE_POLICY_BLOCKLIST

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PACKAGE_POLICY_BLOCKLIST: Int
```

PackagePolicy type indicator for `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#`

This constant indicates that all packages are allowed except for the packages returned by `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#getPackageNames()`, which acts as a denylist.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PACKAGE_POLICY_ALLOWLIST_AND_SYSTEM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PACKAGE_POLICY_ALLOWLIST:kotlin.Int`

## Public constructors

### PackagePolicy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PackagePolicy(policyType: Int)
```

Create the package policy

| Parameters ||
|---|---|
| `policyType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): indicates how to interpret this policy. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PACKAGE_POLICY_BLOCKLIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PACKAGE_POLICY_ALLOWLIST_AND_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PACKAGE_POLICY_ALLOWLIST:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PackagePolicy(kotlin.Int,%20kotlin.collections.MutableSet)`

### PackagePolicy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PackagePolicy(
    policyType: Int, 
    packageNames: MutableSet<String!>)
```

Create the package policy

| Parameters ||
|---|---|
| `policyType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): indicates how to interpret this policy. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PACKAGE_POLICY_BLOCKLIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PACKAGE_POLICY_ALLOWLIST_AND_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PACKAGE_POLICY_ALLOWLIST:kotlin.Int` |
| `packageNames` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: allowlist or a denylist, based on policyType. This value cannot be `null`. |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getPackageNames

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPackageNames(): MutableSet<String!>
```

Returns the list of packages to use as an allow/deny list based on policy type

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

### getPolicyType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPolicyType(): Int
```

Returns the current policy type

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PACKAGE_POLICY_BLOCKLIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PACKAGE_POLICY_ALLOWLIST_AND_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/admin/PackagePolicy#PACKAGE_POLICY_ALLOWLIST:kotlin.Int` |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

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
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<PackagePolicy!>
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#`
