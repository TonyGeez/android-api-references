Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiSsidPolicy

```
class WifiSsidPolicy : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.admin.WifiSsidPolicy](WifiSsidPolicy.md) |

Used to indicate the Wi-Fi SSID restriction policy the network must satisfy in order to be eligible for a connection.

If the policy type is a denylist, the device may not connect to networks on the denylist. If the policy type is an allowlist, the device may only connect to networks on the allowlist. Admin configured networks are not exempt from this restriction. This policy only prohibits connecting to a restricted network and does not affect adding a restricted network. If the current network is present in the denylist or not present in the allowlist, it will be disconnected.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/WifiSsidPolicy#WIFI_SSID_POLICY_TYPE_ALLOWLIST:kotlin.Int` SSID policy type indicator for WifiSsidPolicy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/WifiSsidPolicy#WIFI_SSID_POLICY_TYPE_DENYLIST:kotlin.Int` SSID policy type indicator for WifiSsidPolicy. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| WifiSsidPolicy Create the Wi-Fi SSID Policy. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Two instances of WifiSsidPolicy are considered equal if they have the same WifiSsidPolicyType and the same set of WifiSsids |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPolicyType Returns the policy type. |
| --- | --- |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [WifiSsid](../android.net.wifi/WifiSsid.md)!\> | getSsids Returns the set of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiSsid.html#` |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns the hash code value of WifiSsidPolicyType and WifiSsid set |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [WifiSsidPolicy](WifiSsidPolicy.md)!\> | `https://developer.android.com/reference/kotlin/android/app/admin/WifiSsidPolicy#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### WIFI_SSID_POLICY_TYPE_ALLOWLIST

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_SSID_POLICY_TYPE_ALLOWLIST: Int
```

SSID policy type indicator for WifiSsidPolicy.

When returned from getPolicyType, the constant indicates that the SSID policy type is an allowlist.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/WifiSsidPolicy#WIFI_SSID_POLICY_TYPE_DENYLIST:kotlin.Int`

### WIFI_SSID_POLICY_TYPE_DENYLIST

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_SSID_POLICY_TYPE_DENYLIST: Int
```

SSID policy type indicator for WifiSsidPolicy.

When returned from getPolicyType, the constant indicates that the SSID policy type is a denylist.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/WifiSsidPolicy#WIFI_SSID_POLICY_TYPE_ALLOWLIST:kotlin.Int`

## Public constructors

### WifiSsidPolicy

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
WifiSsidPolicy(
    policyType: Int, 
    ssids: MutableSet<WifiSsid!>)
```

Create the Wi-Fi SSID Policy.

| Parameters ||
|---|---|
| `policyType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): indicate whether the policy is an allowlist or a denylist. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/admin/WifiSsidPolicy#WIFI_SSID_POLICY_TYPE_ALLOWLIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/admin/WifiSsidPolicy#WIFI_SSID_POLICY_TYPE_DENYLIST:kotlin.Int` |
| `ssids` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [WifiSsid](../android.net.wifi/WifiSsid.md)!\>: set of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiSsid.html#` This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the input ssids set is empty or the policyType is invalid |

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Two instances of WifiSsidPolicy are considered equal if they have the same WifiSsidPolicyType and the same set of WifiSsids

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getPolicyType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPolicyType(): Int
```

Returns the policy type.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/admin/WifiSsidPolicy#WIFI_SSID_POLICY_TYPE_ALLOWLIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/admin/WifiSsidPolicy#WIFI_SSID_POLICY_TYPE_DENYLIST:kotlin.Int` |

### getSsids

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSsids(): MutableSet<WifiSsid!>
```

Returns the set of `https://developer.android.com/reference/kotlin/android/net/wifi/WifiSsid.html#`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/net/wifi/WifiSsid.html#!>` | This value cannot be `null`. |

### hashCode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns the hash code value of WifiSsidPolicyType and WifiSsid set

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### writeToParcel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<WifiSsidPolicy!>
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#`
