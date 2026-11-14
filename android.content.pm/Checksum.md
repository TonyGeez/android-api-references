# Checksum

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Checksum

Kotlin| [Java](https://developer.android.com/reference/android/content/pm/Checksum "View this page in Java") 
| --- | --- |

```
class Checksum : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.Checksum](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#) |

A typed checksum.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_PARTIAL_MERKLE_ROOT_1M_SHA256](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_PARTIAL_MERKLE_ROOT_1M_SHA256:kotlin.Int) Root SHA256 hash of a 1M Merkle tree computed over protected content. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_PARTIAL_MERKLE_ROOT_1M_SHA512](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_PARTIAL_MERKLE_ROOT_1M_SHA512:kotlin.Int) Root SHA512 hash of a 1M Merkle tree computed over protected content. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WHOLE_MD5](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_MD5:kotlin.Int) MD5 hash computed over all file bytes. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WHOLE_MERKLE_ROOT_4K_SHA256](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_MERKLE_ROOT_4K_SHA256:kotlin.Int) Root SHA256 hash of a 4K Merkle tree computed over all file bytes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WHOLE_SHA1](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_SHA1:kotlin.Int) SHA1 hash computed over all file bytes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WHOLE_SHA256](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_SHA256:kotlin.Int) SHA256 hash computed over all file bytes. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WHOLE_SHA512](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_SHA512:kotlin.Int) SHA512 hash computed over all file bytes. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Checksum](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#Checksum(kotlin.Int,%20kotlin.ByteArray))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Creates a new Checksum. |

| Public methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#getType())`()` Checksum type. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getValue](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#getValue())`()` Checksum value. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [Checksum](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### TYPE_PARTIAL_MERKLE_ROOT_1M_SHA256

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_PARTIAL_MERKLE_ROOT_1M_SHA256: Int
```

Root SHA256 hash of a 1M Merkle tree computed over protected content. Excludes signing block. [See APK Signature Scheme V2](https://source.android.com/security/apksigning/v2). 

 Value: 32

**See Also**

- [android.content.pm.PackageManager#requestChecksums](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#requestChecksums(kotlin.String,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.collections.MutableList,%20android.content.pm.PackageManager.OnChecksumsReadyListener)) 

### TYPE_PARTIAL_MERKLE_ROOT_1M_SHA512

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_PARTIAL_MERKLE_ROOT_1M_SHA512: Int
```

Root SHA512 hash of a 1M Merkle tree computed over protected content. Excludes signing block. [See APK Signature Scheme V2](https://source.android.com/security/apksigning/v2). 

 Value: 64

**See Also**

- [android.content.pm.PackageManager#requestChecksums](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#requestChecksums(kotlin.String,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.collections.MutableList,%20android.content.pm.PackageManager.OnChecksumsReadyListener)) 

### TYPE_WHOLE_MD5

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WHOLE_MD5: Int
```

**Deprecated:** *Not platform enforced. Cryptographically broken and unsuitable for further use. Use platform enforced digests e.g. [TYPE_WHOLE_MERKLE_ROOT_4K_SHA256](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_MERKLE_ROOT_4K_SHA256:kotlin.Int). Provided for completeness' sake and to support legacy usecases.*

MD5 hash computed over all file bytes. 

 Value: 2

**See Also**

- [android.content.pm.PackageManager#requestChecksums](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#requestChecksums(kotlin.String,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.collections.MutableList,%20android.content.pm.PackageManager.OnChecksumsReadyListener)) 

### TYPE_WHOLE_MERKLE_ROOT_4K_SHA256

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WHOLE_MERKLE_ROOT_4K_SHA256: Int
```

Root SHA256 hash of a 4K Merkle tree computed over all file bytes. [See APK Signature Scheme V4](https://source.android.com/security/apksigning/v4). [See fs-verity](https://www.kernel.org/doc/html/latest/filesystems/fsverity.html). Recommended for all new applications. Can be used by kernel to enforce authenticity and integrity of the APK. [See fs-verity for details](https://www.kernel.org/doc/html/latest/filesystems/fsverity.html) 

 Value: 1

**See Also**

- [android.content.pm.PackageManager#requestChecksums](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#requestChecksums(kotlin.String,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.collections.MutableList,%20android.content.pm.PackageManager.OnChecksumsReadyListener)) 

### TYPE_WHOLE_SHA1

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WHOLE_SHA1: Int
```

**Deprecated:** *Not platform enforced. Broken and should not be used. Use platform enforced digests e.g. [TYPE_WHOLE_MERKLE_ROOT_4K_SHA256](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_MERKLE_ROOT_4K_SHA256:kotlin.Int). Provided for completeness' sake and to support legacy usecases.*

SHA1 hash computed over all file bytes. 

 Value: 4

**See Also**

- [android.content.pm.PackageManager#requestChecksums](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#requestChecksums(kotlin.String,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.collections.MutableList,%20android.content.pm.PackageManager.OnChecksumsReadyListener)) 

### TYPE_WHOLE_SHA256

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WHOLE_SHA256: Int
```

**Deprecated:** *Not platform enforced. Use platform enforced digests e.g. [TYPE_WHOLE_MERKLE_ROOT_4K_SHA256](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_MERKLE_ROOT_4K_SHA256:kotlin.Int). Provided for completeness' sake and to support legacy usecases.*

SHA256 hash computed over all file bytes. 

 Value: 8

**See Also**

- [android.content.pm.PackageManager#requestChecksums](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#requestChecksums(kotlin.String,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.collections.MutableList,%20android.content.pm.PackageManager.OnChecksumsReadyListener)) 

### TYPE_WHOLE_SHA512

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WHOLE_SHA512: Int
```

**Deprecated:** *Not platform enforced. Use platform enforced digests e.g. [TYPE_WHOLE_MERKLE_ROOT_4K_SHA256](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_MERKLE_ROOT_4K_SHA256:kotlin.Int). Provided for completeness' sake and to support legacy usecases.*

SHA512 hash computed over all file bytes. 

 Value: 16

**See Also**

- [android.content.pm.PackageManager#requestChecksums](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#requestChecksums(kotlin.String,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.collections.MutableList,%20android.content.pm.PackageManager.OnChecksumsReadyListener))

## Public constructors

### Checksum

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Checksum(
    type: Int, 
    value: ByteArray)
```

Creates a new Checksum.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Checksum type. Value is [android.content.pm.Checksum#TYPE_WHOLE_MERKLE_ROOT_4K_SHA256](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_MERKLE_ROOT_4K_SHA256:kotlin.Int), [android.content.pm.Checksum#TYPE_WHOLE_MD5](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_MD5:kotlin.Int), [android.content.pm.Checksum#TYPE_WHOLE_SHA1](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_SHA1:kotlin.Int), [android.content.pm.Checksum#TYPE_WHOLE_SHA256](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_SHA256:kotlin.Int), [android.content.pm.Checksum#TYPE_WHOLE_SHA512](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_SHA512:kotlin.Int), [android.content.pm.Checksum#TYPE_PARTIAL_MERKLE_ROOT_1M_SHA256](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_PARTIAL_MERKLE_ROOT_1M_SHA256:kotlin.Int), or [android.content.pm.Checksum#TYPE_PARTIAL_MERKLE_ROOT_1M_SHA512](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_PARTIAL_MERKLE_ROOT_1M_SHA512:kotlin.Int) |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):Checksum value. This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Checksum type.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.content.pm.Checksum#TYPE_WHOLE_MERKLE_ROOT_4K_SHA256](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_MERKLE_ROOT_4K_SHA256:kotlin.Int), [android.content.pm.Checksum#TYPE_WHOLE_MD5](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_MD5:kotlin.Int), [android.content.pm.Checksum#TYPE_WHOLE_SHA1](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_SHA1:kotlin.Int), [android.content.pm.Checksum#TYPE_WHOLE_SHA256](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_SHA256:kotlin.Int), [android.content.pm.Checksum#TYPE_WHOLE_SHA512](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_SHA512:kotlin.Int), [android.content.pm.Checksum#TYPE_PARTIAL_MERKLE_ROOT_1M_SHA256](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_PARTIAL_MERKLE_ROOT_1M_SHA256:kotlin.Int), or [android.content.pm.Checksum#TYPE_PARTIAL_MERKLE_ROOT_1M_SHA512](https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_PARTIAL_MERKLE_ROOT_1M_SHA512:kotlin.Int) |

### getValue

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getValue(): ByteArray
```

Checksum value.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | This value cannot be`null`. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Checksum!>
```
