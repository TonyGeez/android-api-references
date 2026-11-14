Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IpSecAlgorithm

```
class IpSecAlgorithm : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.IpSecAlgorithm](https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#) |

This class represents a single algorithm that can be used by an `https://developer.android.com/reference/kotlin/android/net/IpSecTransform`.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_AES_CMAC:kotlin.String` AES-CMAC Authentication/Integrity Algorithm. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_AES_XCBC:kotlin.String` AES-XCBC Authentication/Integrity Algorithm. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_CRYPT_AES_GCM:kotlin.String` AES-GCM Authentication/Integrity + Encryption/Ciphering Algorithm. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_CRYPT_CHACHA20_POLY1305:kotlin.String` ChaCha20-Poly1305 Authentication/Integrity + Encryption/Ciphering Algorithm. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_HMAC_MD5:kotlin.String` MD5 HMAC Authentication/Integrity Algorithm. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_HMAC_SHA1:kotlin.String` SHA1 HMAC Authentication/Integrity Algorithm. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_HMAC_SHA256:kotlin.String` SHA256 HMAC Authentication/Integrity Algorithm. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_HMAC_SHA384:kotlin.String` SHA384 HMAC Authentication/Integrity Algorithm. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_HMAC_SHA512:kotlin.String` SHA512 HMAC Authentication/Integrity Algorithm. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#CRYPT_AES_CBC:kotlin.String` AES-CBC Encryption/Ciphering Algorithm. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#CRYPT_AES_CTR:kotlin.String` AES-CTR Encryption/Ciphering Algorithm. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#IpSecAlgorithm(kotlin.String,%20kotlin.ByteArray)(algorithm: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)` Creates an IpSecAlgorithm of one of the supported types. |
| `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#IpSecAlgorithm(kotlin.String,%20kotlin.ByteArray,%20kotlin.Int)(algorithm: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html, truncLenBits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates an IpSecAlgorithm of one of the supported types. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#describeContents()()` Parcelable Implementation |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#getKey()()` Get the key for this algorithm |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#getName()()` Get the algorithm name |
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#getSupportedAlgorithms()()` Returns supported IPsec algorithms for the current device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#getTruncationLengthBits()()` Get the truncation length of this algorithm, in bits |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#writeToParcel(android.os.Parcel,%20kotlin.Int)(out: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Write to parcel |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [IpSecAlgorithm](https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#)!\> | `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#CREATOR:android.os.Parcelable.Creator` Parcelable Creator |

## Constants

### AUTH_AES_CMAC

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTH_AES_CMAC: String
```

AES-CMAC Authentication/Integrity Algorithm.

Keys for this algorithm must be 128 bits in length.

The only valid truncation length is 96 bits.

This algorithm may be available on the device. Caller MUST check if it is supported before using it by calling `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#getSupportedAlgorithms()` and checking if this algorithm is included in the returned algorithm set. The returned algorithm set will not change unless the device is rebooted. `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown if this algorithm is requested on an unsupported device.

 Value: "cmac(aes)"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#getSupportedAlgorithms()`

### AUTH_AES_XCBC

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTH_AES_XCBC: String
```

AES-XCBC Authentication/Integrity Algorithm.

Keys for this algorithm must be 128 bits in length.

The only valid truncation length is 96 bits.

This algorithm may be available on the device. Caller MUST check if it is supported before using it by calling `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#getSupportedAlgorithms()` and checking if this algorithm is included in the returned algorithm set. The returned algorithm set will not change unless the device is rebooted. `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown if this algorithm is requested on an unsupported device.

 Value: "xcbc(aes)"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#getSupportedAlgorithms()`

### AUTH_CRYPT_AES_GCM

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTH_CRYPT_AES_GCM: String
```

AES-GCM Authentication/Integrity + Encryption/Ciphering Algorithm.

Valid lengths for keying material are {160, 224, 288}.

As per [RFC4106 (Section 8.1)](https://tools.ietf.org/html/rfc4106#section-8.1), keying material consists of a 128, 192, or 256 bit AES key followed by a 32-bit salt. RFC compliance requires that the salt must be unique per invocation with the same key.

Valid ICV (truncation) lengths are {64, 96, 128}.

 Value: "rfc4106(gcm(aes))"

### AUTH_CRYPT_CHACHA20_POLY1305

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTH_CRYPT_CHACHA20_POLY1305: String
```

ChaCha20-Poly1305 Authentication/Integrity + Encryption/Ciphering Algorithm.

Keys for this algorithm must be 288 bits in length.

As per [RFC7634 (Section 2)](https://tools.ietf.org/html/rfc7634#section-2), keying material consists of a 256 bit key followed by a 32-bit salt. The salt is fixed per security association.

The only valid ICV (truncation) length is 128 bits.

This algorithm may be available on the device. Caller MUST check if it is supported before using it by calling `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#getSupportedAlgorithms()` and checking if this algorithm is included in the returned algorithm set. The returned algorithm set will not change unless the device is rebooted. `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown if this algorithm is requested on an unsupported device.

 Value: "rfc7539esp(chacha20,poly1305)"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#getSupportedAlgorithms()`

### AUTH_HMAC_MD5

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTH_HMAC_MD5: String
```

MD5 HMAC Authentication/Integrity Algorithm. **This algorithm is not recommended for use in new applications and is provided for legacy compatibility with 3gpp infrastructure.**

Keys for this algorithm must be 128 bits in length.

Valid truncation lengths are multiples of 8 bits from 96 to 128.

 Value: "hmac(md5)"

### AUTH_HMAC_SHA1

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTH_HMAC_SHA1: String
```

SHA1 HMAC Authentication/Integrity Algorithm. **This algorithm is not recommended for use in new applications and is provided for legacy compatibility with 3gpp infrastructure.**

Keys for this algorithm must be 160 bits in length.

Valid truncation lengths are multiples of 8 bits from 96 to 160.

 Value: "hmac(sha1)"

### AUTH_HMAC_SHA256

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTH_HMAC_SHA256: String
```

SHA256 HMAC Authentication/Integrity Algorithm.

Keys for this algorithm must be 256 bits in length.

Valid truncation lengths are multiples of 8 bits from 96 to 256.

 Value: "hmac(sha256)"

### AUTH_HMAC_SHA384

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTH_HMAC_SHA384: String
```

SHA384 HMAC Authentication/Integrity Algorithm.

Keys for this algorithm must be 384 bits in length.

Valid truncation lengths are multiples of 8 bits from 192 to 384.

 Value: "hmac(sha384)"

### AUTH_HMAC_SHA512

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTH_HMAC_SHA512: String
```

SHA512 HMAC Authentication/Integrity Algorithm.

Keys for this algorithm must be 512 bits in length.

Valid truncation lengths are multiples of 8 bits from 256 to 512.

 Value: "hmac(sha512)"

### CRYPT_AES_CBC

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CRYPT_AES_CBC: String
```

AES-CBC Encryption/Ciphering Algorithm.

Valid lengths for this key are {128, 192, 256}.

 Value: "cbc(aes)"

### CRYPT_AES_CTR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CRYPT_AES_CTR: String
```

AES-CTR Encryption/Ciphering Algorithm.

Valid lengths for keying material are {160, 224, 288}.

As per [RFC3686 (Section 5.1)](https://tools.ietf.org/html/rfc3686#section-5.1), keying material consists of a 128, 192, or 256 bit AES key followed by a 32-bit nonce. RFC compliance requires that the nonce must be unique per security association.

This algorithm may be available on the device. Caller MUST check if it is supported before using it by calling `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#getSupportedAlgorithms()` and checking if this algorithm is included in the returned algorithm set. The returned algorithm set will not change unless the device is rebooted. `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown if this algorithm is requested on an unsupported device.

 Value: "rfc3686(ctr(aes))"

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#getSupportedAlgorithms()`

## Public constructors

### IpSecAlgorithm

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
IpSecAlgorithm(
    algorithm: String, 
    key: ByteArray)
```

Creates an IpSecAlgorithm of one of the supported types. Supported algorithm names are defined as constants in this class.

For algorithms that produce an integrity check value, the truncation length is a required parameter. See `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#IpSecAlgorithm(kotlin.String,%20kotlin.ByteArray,%20kotlin.Int)`

| Parameters ||
|---|---|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name of the algorithm. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#CRYPT_AES_CBC:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#CRYPT_AES_CTR:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_HMAC_MD5:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_HMAC_SHA1:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_HMAC_SHA256:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_HMAC_SHA384:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_HMAC_SHA512:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_AES_XCBC:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_AES_CMAC:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_CRYPT_AES_GCM:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_CRYPT_CHACHA20_POLY1305:kotlin.String` |
| `key` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): key padded to a multiple of 8 bits. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if algorithm or key length is invalid. |

### IpSecAlgorithm

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
IpSecAlgorithm(
    algorithm: String, 
    key: ByteArray, 
    truncLenBits: Int)
```

Creates an IpSecAlgorithm of one of the supported types. Supported algorithm names are defined as constants in this class.

This constructor only supports algorithms that use a truncation length. i.e. Authentication and Authenticated Encryption algorithms.

| Parameters ||
|---|---|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name of the algorithm. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#CRYPT_AES_CBC:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#CRYPT_AES_CTR:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_HMAC_MD5:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_HMAC_SHA1:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_HMAC_SHA256:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_HMAC_SHA384:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_HMAC_SHA512:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_AES_XCBC:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_AES_CMAC:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_CRYPT_AES_GCM:kotlin.String` - `https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm#AUTH_CRYPT_CHACHA20_POLY1305:kotlin.String` |
| `key` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): key padded to a multiple of 8 bits. This value cannot be `null`. |
| `truncLenBits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of bits of output hash to use. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if algorithm, key length or truncation length is invalid. |

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Parcelable Implementation

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getKey

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKey(): ByteArray
```

Get the key for this algorithm

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | This value cannot be `null`. |

### getName

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): String
```

Get the algorithm name

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getSupportedAlgorithms

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getSupportedAlgorithms(): MutableSet<String!>
```

Returns supported IPsec algorithms for the current device.

Some algorithms may not be supported on old devices. Callers MUST check if an algorithm is supported before using it.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

### getTruncationLengthBits

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTruncationLengthBits(): Int
```

Get the truncation length of this algorithm, in bits

### toString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Write to parcel

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<IpSecAlgorithm!>
```

Parcelable Creator
