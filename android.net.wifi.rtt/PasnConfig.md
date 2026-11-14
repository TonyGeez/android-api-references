Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PasnConfig

```
class PasnConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.rtt.PasnConfig](PasnConfig.md) |

Pre-association security negotiation (PASN) configuration.

PASN configuration in IEEE 802.11az focuses on securing the ranging process before a device fully associates with a Wi-Fi network. IEEE 802.11az supports various based AKMs as in `AKM_*` for PASN and cipher as in `CIPHER_*`. Password is also another input to some base AKMs.

Once PASN is initiated, the AP and the client device exchange messages to authenticate each other and establish security keys. This process ensures that only authorized devices can participate in ranging.

After successful PASN authentication, ranging operations are performed using the established secure channel. This protects the ranging measurements from eavesdropping and tampering.

The keys derived during the PASN process are used to protect the LTFs exchanged during ranging. This ensures that the LTFs are encrypted and authenticated, preventing unauthorized access and manipulation.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig.Builder` Builder for `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#` |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#AKM_FILS_EAP_SHA256:kotlin.Int` Fast Initial Link Setup (FILS) with Extensible Authentication Protocol (EAP) and SHA-256. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#AKM_FILS_EAP_SHA384:kotlin.Int` Fast Initial Link Setup (FILS) with Extensible Authentication Protocol (EAP) and SHA-384. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#AKM_FT_EAP_SHA256:kotlin.Int` Fast BSS Transition (FT) with Extensible Authentication Protocol (EAP) and SHA-256. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#AKM_FT_EAP_SHA384:kotlin.Int` Fast BSS Transition (FT) with Extensible Authentication Protocol (EAP) and SHA-384. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#AKM_FT_PSK_SHA256:kotlin.Int` Fast BSS Transition (FT) with Pre-Shared Key (PSK) and SHA-256. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#AKM_FT_PSK_SHA384:kotlin.Int` Fast BSS Transition (FT) with Pre-Shared Key (PSK) and SHA-384. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#AKM_NONE:kotlin.Int` No authentication and key management. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#AKM_PASN:kotlin.Int` Pre-association security negotiation (PASN). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#AKM_SAE:kotlin.Int` Simultaneous authentication of equals (SAE). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#CIPHER_CCMP_128:kotlin.Int` Counter Mode with Cipher Block Chaining Message Authentication Code Protocol (CCMP) with 128-bit key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#CIPHER_CCMP_256:kotlin.Int` Counter Mode with Cipher Block Chaining Message Authentication Code Protocol (CCMP) with 256-bit key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#CIPHER_GCMP_128:kotlin.Int` Galois/Counter Mode Protocol (GCMP) with 128-bit key. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#CIPHER_GCMP_256:kotlin.Int` Galois/Counter Mode Protocol (GCMP) with 256-bit key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#CIPHER_NONE:kotlin.Int` No encryption. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#getBaseAkms()()` Return base AKMs (Authentication and Key Management). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#getCiphers()()` Return pairwise ciphers. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#getPasnComebackCookie()()` Get PASN comeback cookie. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#getPassword()()` Get password used by base AKM. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#getPmk()()` Get the PMK (pairwise master key). |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#getProximityDetectionSeekerDeviceIdentityKey()()` Get the Seeker device identity key. |
| [WifiSsid](../android.net.wifi/WifiSsid.md)? | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#getWifiSsid()()` Get Wifi SSID which is used to retrieve saved network profile if `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#getPassword()` is null. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#hashCode()()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PasnConfig](PasnConfig.md)!\> | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### AKM_FILS_EAP_SHA256

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AKM_FILS_EAP_SHA256: Int
```

Fast Initial Link Setup (FILS) with Extensible Authentication Protocol (EAP) and SHA-256.

 Value: 64

### AKM_FILS_EAP_SHA384

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AKM_FILS_EAP_SHA384: Int
```

Fast Initial Link Setup (FILS) with Extensible Authentication Protocol (EAP) and SHA-384.

 Value: 128

### AKM_FT_EAP_SHA256

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AKM_FT_EAP_SHA256: Int
```

Fast BSS Transition (FT) with Extensible Authentication Protocol (EAP) and SHA-256.

 Value: 4

### AKM_FT_EAP_SHA384

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AKM_FT_EAP_SHA384: Int
```

Fast BSS Transition (FT) with Extensible Authentication Protocol (EAP) and SHA-384.

 Value: 16

### AKM_FT_PSK_SHA256

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AKM_FT_PSK_SHA256: Int
```

Fast BSS Transition (FT) with Pre-Shared Key (PSK) and SHA-256.

 Value: 8

### AKM_FT_PSK_SHA384

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AKM_FT_PSK_SHA384: Int
```

Fast BSS Transition (FT) with Pre-Shared Key (PSK) and SHA-384.

 Value: 32

### AKM_NONE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AKM_NONE: Int
```

No authentication and key management.

 Value: 0

### AKM_PASN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AKM_PASN: Int
```

Pre-association security negotiation (PASN).

 Value: 1

### AKM_SAE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AKM_SAE: Int
```

Simultaneous authentication of equals (SAE).

 Value: 2

### CIPHER_CCMP_128

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CIPHER_CCMP_128: Int
```

Counter Mode with Cipher Block Chaining Message Authentication Code Protocol (CCMP) with 128-bit key.

 Value: 1

### CIPHER_CCMP_256

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CIPHER_CCMP_256: Int
```

Counter Mode with Cipher Block Chaining Message Authentication Code Protocol (CCMP) with 256-bit key.

 Value: 2

### CIPHER_GCMP_128

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CIPHER_GCMP_128: Int
```

Galois/Counter Mode Protocol (GCMP) with 128-bit key.

 Value: 4

### CIPHER_GCMP_256

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CIPHER_GCMP_256: Int
```

Galois/Counter Mode Protocol (GCMP) with 256-bit key.

 Value: 8

### CIPHER_NONE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CIPHER_NONE: Int
```

No encryption.

 Value: 0

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### getBaseAkms

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBaseAkms(): Int
```

Return base AKMs (Authentication and Key Management).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#AKM_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#AKM_PASN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#AKM_SAE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#AKM_FT_EAP_SHA256:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#AKM_FT_PSK_SHA256:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#AKM_FT_EAP_SHA384:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#AKM_FT_PSK_SHA384:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#AKM_FILS_EAP_SHA256:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#AKM_FILS_EAP_SHA384:kotlin.Int` |

### getCiphers

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCiphers(): Int
```

Return pairwise ciphers.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#CIPHER_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#CIPHER_CCMP_128:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#CIPHER_CCMP_256:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#CIPHER_GCMP_128:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#CIPHER_GCMP_256:kotlin.Int` |

### getPasnComebackCookie

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPasnComebackCookie(): ByteArray?
```

Get PASN comeback cookie. See `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig.Builder#setPasnComebackCookie(kotlin.ByteArray)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | This value may be `null`. |

### getPassword

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPassword(): String?
```

Get password used by base AKM. If null, password is retrieved from the saved network profile for the PASN authentication. See `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#getWifiSsid()` on retrieving saved network profile.

### getPmk

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPmk(): ByteArray?
```

Get the PMK (pairwise master key). See `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig.Builder#setPmk(kotlin.ByteArray)`. see `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig.Builder`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | This value may be `null`. |

### getProximityDetectionSeekerDeviceIdentityKey

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProximityDetectionSeekerDeviceIdentityKey(): ByteArray?
```

Get the Seeker device identity key. See `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig.Builder#setProximityDetectionSeekerDeviceIdentityKey(kotlin.ByteArray)`. see `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig.Builder`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | This value may be `null`. |

### getWifiSsid

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWifiSsid(): WifiSsid?
```

Get Wifi SSID which is used to retrieve saved network profile if `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/PasnConfig#getPassword()` is null. If Wifi SSID and password are not set and there is no saved profile corresponding to the responder, unauthenticated PASN will be used if `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingRequest#getSecurityMode()` allows. See `SECURITY_MODE_*` for more details.

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

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
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<PasnConfig!>
```
