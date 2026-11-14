# SigningInfo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SigningInfo

Kotlin| [Java](../android/content/pm/SigningInfo.md) 
| --- | --- |

```
class SigningInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.SigningInfo](../android/content/pm/SigningInfo.md) |

Information pertaining to the signing certificates used to sign a package.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VERSION_JAR](../android/content/pm/SigningInfo.md) JAR signing (v1 scheme). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VERSION_SIGNING_BLOCK_V2](../android/content/pm/SigningInfo.md) APK signature scheme v2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VERSION_SIGNING_BLOCK_V3](../android/content/pm/SigningInfo.md) APK signature scheme v3. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VERSION_SIGNING_BLOCK_V4](../android/content/pm/SigningInfo.md) APK signature scheme v4. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SigningInfo](../android/content/pm/SigningInfo.md))`()` <br /> |
| [SigningInfo](../android/content/pm/SigningInfo.md))`(`orig:` ` [SigningInfo](../android/content/pm/SigningInfo.md)!`)` <br /> |
| [SigningInfo](../android/content/pm/SigningInfo.md))`(`schemeVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `apkContentsSigners:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Signature](../android/content/pm/Signature.md)!>?`, `publicKeys:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [PublicKey](../java/security/PublicKey.md)!>?`, `signingCertificateHistory:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Signature](../android/content/pm/Signature.md)!>?`)` Creates a new instance of information used to sign the APK. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/content/pm/SigningInfo.md))`()` <br /> |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Signature](../android/content/pm/Signature.md)!\>! | [getApkContentsSigners](../android/content/pm/SigningInfo.md))`()` Returns the signing certificates used to sign the APK contents of this application. |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [PublicKey](../java/security/PublicKey.md)!\> | [getPublicKeys](../android/content/pm/SigningInfo.md))`()` Returns the public keys for the signing certificates. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSchemeVersion](../android/content/pm/SigningInfo.md))`()` Returns the version of signing schema used to sign the APK. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Signature](../android/content/pm/Signature.md)!\>! | [getSigningCertificateHistory](../android/content/pm/SigningInfo.md))`()` Returns the signing certificates this package has proven it is authorized to use. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMultipleSigners](../android/content/pm/SigningInfo.md))`()` Although relatively uncommon, packages may be signed by more than one signer, in which case their identity is viewed as being the set of all signers, not just any one. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasPastSigningCertificates](../android/content/pm/SigningInfo.md))`()` APK Signature Scheme v3 enables packages to provide a proof-of-rotation record that the platform verifies, and uses, to allow the use of new signing certificates. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [signersMatchExactly](../android/content/pm/SigningInfo.md))`(`other:` ` [SigningInfo](../android/content/pm/SigningInfo.md)`)` Returns true if the signing certificates in this and other match exactly. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/content/pm/SigningInfo.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `parcelableFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SigningInfo](../android/content/pm/SigningInfo.md)!\> | [CREATOR](../android/content/pm/SigningInfo.md) <br /> |

## Constants

### VERSION_JAR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VERSION_JAR: Int
```

JAR signing (v1 scheme). See https://source.android.com/docs/security/features/apksigning#v1. 

 Value: 1

### VERSION_SIGNING_BLOCK_V2

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VERSION_SIGNING_BLOCK_V2: Int
```

APK signature scheme v2. See https://source.android.com/docs/security/features/apksigning/v2. 

 Value: 2

### VERSION_SIGNING_BLOCK_V3

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VERSION_SIGNING_BLOCK_V3: Int
```

APK signature scheme v3. See https://source.android.com/docs/security/features/apksigning/v3. 

 Value: 3

### VERSION_SIGNING_BLOCK_V4

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VERSION_SIGNING_BLOCK_V4: Int
```

APK signature scheme v4. See https://source.android.com/docs/security/features/apksigning/v4. 

 Value: 4

## Public constructors

### SigningInfo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SigningInfo()
```  

### SigningInfo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SigningInfo(orig: SigningInfo!)
```  

### SigningInfo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SigningInfo(
    schemeVersion: Int, 
    apkContentsSigners: MutableCollection<Signature!>?, 
    publicKeys: MutableCollection<PublicKey!>?, 
    signingCertificateHistory: MutableCollection<Signature!>?)
```

Creates a new instance of information used to sign the APK.

| Parameters ||
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `schemeVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):version of signing schema. Value is android.content.pm.SigningDetails.SignatureSchemeVersion.UNKNOWN, android.content.pm.SigningDetails.SignatureSchemeVersion.JAR, android.content.pm.SigningDetails.SignatureSchemeVersion.SIGNING_BLOCK_V2, android.content.pm.SigningDetails.SignatureSchemeVersion.SIGNING_BLOCK_V3, or android.content.pm.SigningDetails.SignatureSchemeVersion.SIGNING_BLOCK_V4 |
| `apkContentsSigners` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Signature](../android/content/pm/Signature.md)!\>?:signing certificates. This value may be`null`. |
| `publicKeys` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [PublicKey](../java/security/PublicKey.md)!\>?:for the signing certificates. This value may be`null`. |
| --- | --- |
| `signingCertificateHistory` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Signature](../android/content/pm/Signature.md)!\>?:All signing certificates the package has proven it is authorized to use. This value may be`null`. |

**See Also**

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getApkContentsSigners

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getApkContentsSigners(): Array<Signature!>!
```

Returns the signing certificates used to sign the APK contents of this application. Not including any past signing certificates the package proved it is authorized to use. This method should not be used unless [hasMultipleSigners()](../android/content/pm/SigningInfo.md))returns true, indicating that [getSigningCertificateHistory()](../android/content/pm/SigningInfo.md))cannot be used, otherwise [getSigningCertificateHistory()](../android/content/pm/SigningInfo.md))should be preferred. 

### getPublicKeys

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPublicKeys(): MutableCollection<PublicKey!>
```

Returns the public keys for the signing certificates.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [PublicKey](../java/security/PublicKey.md)!> | This value cannot be`null`. |

### getSchemeVersion

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSchemeVersion(): Int
```

Returns the version of signing schema used to sign the APK.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is android.content.pm.SigningDetails.SignatureSchemeVersion.UNKNOWN, android.content.pm.SigningDetails.SignatureSchemeVersion.JAR, android.content.pm.SigningDetails.SignatureSchemeVersion.SIGNING_BLOCK_V2, android.content.pm.SigningDetails.SignatureSchemeVersion.SIGNING_BLOCK_V3, or android.content.pm.SigningDetails.SignatureSchemeVersion.SIGNING_BLOCK_V4 |

**See Also**

### getSigningCertificateHistory

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSigningCertificateHistory(): Array<Signature!>!
```

Returns the signing certificates this package has proven it is authorized to use. This includes both the signing certificate associated with the signer of the package and the past signing certificates it included as its proof of signing certificate rotation. Signing certificates are returned in the order of rotation with the original signing certificate at index 0, and the current signing certificate at the last index. This method is the preferred replacement for the`GET_SIGNATURES`flag used with [android.content.pm.PackageManager#getPackageInfo(java.lang.String,int)](../android/content/pm/PackageManager.md)). When determining if a package is signed by a desired certificate, the returned array should be checked to determine if it is one of the entries. This method returns null if the package is signed by multiple signing certificates, as opposed to being signed by one current signer and also providing the history of past signing certificates. [hasMultipleSigners()](../android/content/pm/SigningInfo.md))may be used to determine if this package is signed by multiple signers. Packages which are signed by multiple signers cannot change their signing certificates and their`Signature`array should be checked to make sure that every entry matches the looked-for signing certificates. 

### hasMultipleSigners

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasMultipleSigners(): Boolean
```

Although relatively uncommon, packages may be signed by more than one signer, in which case their identity is viewed as being the set of all signers, not just any one. 

### hasPastSigningCertificates

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasPastSigningCertificates(): Boolean
```

APK Signature Scheme v3 enables packages to provide a proof-of-rotation record that the platform verifies, and uses, to allow the use of new signing certificates. This is only available to packages that are not signed by multiple signers. In the event of a change to a new signing certificate, the package's past signing certificates are presented as well. Any check of a package's signing certificate should also include a search through its entire signing history, since it could change to a new signing certificate at any time. 

### signersMatchExactly

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun signersMatchExactly(other: SigningInfo): Boolean
```

Returns true if the signing certificates in this and other match exactly.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `other` | [SigningInfo](../android/content/pm/SigningInfo.md):This value cannot be`null`. |

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    parcelableFlags: Int
): Unit
```

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SigningInfo!>
```
