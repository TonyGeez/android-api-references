Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PasspointConfiguration

Kotlin | [Java](../android/net/wifi/hotspot2/PasspointConfiguration.md)
| --- | --- |

```
class PasspointConfiguration : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.hotspot2.PasspointConfiguration](../android/net/wifi/hotspot2/PasspointConfiguration.md) |

Class representing Passpoint configuration. This contains configurations specified in PerProviderSubscription (PPS) Management Object (MO) tree. For more info, refer to Hotspot 2.0 PPS MO defined in section 9.1 of the Hotspot 2.0 Release 2 Technical Specification.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#PasspointConfiguration()()` Constructor for creating PasspointConfiguration with default values. |
| `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#PasspointConfiguration(android.net.wifi.hotspot2.PasspointConfiguration)(source: https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#!)` Copy constructor. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Credential](../android/net/wifi/hotspot2/pps/Credential.md)! | `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#getCredential()()` Get the credential information. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#getDecoratedIdentityPrefix()()` Get the decorated identity prefix. |
| [HomeSp](../android/net/wifi/hotspot2/pps/HomeSp.md)! | `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#getHomeSp()()` Get the Home SP (Service Provider) information. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#getSubscriptionExpirationTimeMillis()()` Utility method to get the time this subscription will expire. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#getUniqueId()()` Get a unique identifier for a PasspointConfiguration object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#isOsuProvisioned()()` Indicates if the Passpoint Configuration was provisioned by a subscription (OSU) server, which means that it's an R2 (or R3) profile. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#setCredential(android.net.wifi.hotspot2.pps.Credential)(credential: https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential!)` Set the credential information. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#setDecoratedIdentityPrefix(kotlin.String)(decoratedIdentityPrefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Set a prefix for a decorated identity as per RFC 7542. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#setHomeSp(android.net.wifi.hotspot2.pps.HomeSp)(homeSp: https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp!)` Set the Home SP (Service Provider) information. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#setSubscriptionExpirationTimeInMillis(kotlin.Long)(subscriptionExpirationTimeInMillis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Utility method to set the time this subscription will expire. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PasspointConfiguration](../android/net/wifi/hotspot2/PasspointConfiguration.md)!\> | `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/PasspointConfiguration#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### PasspointConfiguration

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PasspointConfiguration()
```

Constructor for creating PasspointConfiguration with default values.

### PasspointConfiguration

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PasspointConfiguration(source: PasspointConfiguration!)
```

Copy constructor.

| Parameters ||
|---|---|
| `source` | [PasspointConfiguration](../android/net/wifi/hotspot2/PasspointConfiguration.md)!: The source to copy from |

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### getCredential

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCredential(): Credential!
```

Get the credential information.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/Credential!` | credential information |

### getDecoratedIdentityPrefix

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDecoratedIdentityPrefix(): String?
```

Get the decorated identity prefix.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The decorated identity prefix. This value may be `null`. |

### getHomeSp

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHomeSp(): HomeSp!
```

Get the Home SP (Service Provider) information.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp!` | Home SP information |

### getSubscriptionExpirationTimeMillis

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSubscriptionExpirationTimeMillis(): Long
```

Utility method to get the time this subscription will expire. It is in the format of number of milliseconds since January 1, 1970, 00:00:00 GMT. 
Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The time this subscription will expire, or Long.MIN_VALUE to indicate unset value. Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |

### getUniqueId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUniqueId(): String
```

Get a unique identifier for a PasspointConfiguration object. The identifier depends on the subscription ID, the configuration that identify the service provider under the HomeSp subtree, and the credential configuration under the Credential subtree. The method throws an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` if the configuration under HomeSp subtree or the configuration under Credential subtree are not initialized.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | A unique identifier. This value cannot be `null`. |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### isOsuProvisioned

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isOsuProvisioned(): Boolean
```

Indicates if the Passpoint Configuration was provisioned by a subscription (OSU) server, which means that it's an R2 (or R3) profile.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the Passpoint Configuration was provisioned by a subscription server. |

### setCredential

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCredential(credential: Credential!): Unit
```

Set the credential information.

| Parameters ||
|---|---|
| `credential` | [Credential](../android/net/wifi/hotspot2/pps/Credential.md)!: The credential information to set to |

### setDecoratedIdentityPrefix

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDecoratedIdentityPrefix(decoratedIdentityPrefix: String?): Unit
```

Set a prefix for a decorated identity as per RFC 7542. This prefix must contain a list of realms (could be a list of 1) delimited by a '!' character. e.g. homerealm.example.org! or proxyrealm.example.net!homerealm.example.org! A prefix of "homerealm.example.org!" will generate a decorated identity that looks like: homerealm.example.org!user@otherrealm.example.net Calling with a null parameter will clear the decorated prefix. Note: Caller must verify that the device supports this feature by calling `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#isDecoratedIdentitySupported()`

| Parameters ||
|---|---|
| `decoratedIdentityPrefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The prefix to add to the outer/anonymous identity. This value may be `null`. |

### setHomeSp

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setHomeSp(homeSp: HomeSp!): Unit
```

Set the Home SP (Service Provider) information.

| Parameters ||
|---|---|
| `homeSp` | [HomeSp](../android/net/wifi/hotspot2/pps/HomeSp.md)!: The Home SP information to set to |

### setSubscriptionExpirationTimeInMillis

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setSubscriptionExpirationTimeInMillis(subscriptionExpirationTimeInMillis: Long): Unit
```

Utility method to set the time this subscription will expire. The framework will not attempt to auto-connect to networks using expired subscriptions.

| Parameters ||
|---|---|
| `subscriptionExpirationTimeInMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The expiration time in the format of number of milliseconds since January 1, 1970, 00:00:00 GMT, or `https://developer.android.com/reference/kotlin/java/lang/Long.html#MIN_VALUE:kotlin.Long` to unset. Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<PasspointConfiguration!>
```
