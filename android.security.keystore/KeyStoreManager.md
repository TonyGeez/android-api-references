# KeyStoreManager

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyStoreManager

Kotlin| [Java](https://developer.android.com/reference/android/security/keystore/KeyStoreManager "View this page in Java") 

```
class KeyStoreManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.security.keystore.KeyStoreManager](https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager#) |

This class provides methods for interacting with keys stored within the [Android Keystore](https://developer.android.com/reference/kotlin/privacy-and-security/keystore).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODULE_HASH](https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager#MODULE_HASH:kotlin.Int) When passed into getSupplementaryAttestationInfo, getSupplementaryAttestationInfo returns the DER-encoded structure corresponding to the \`Modules\` schema described in the KeyMint HAL's KeyCreationResult. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!\> | [getGrantedCertificateChainFromId](https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager#getGrantedCertificateChainFromId(kotlin.Long))`(`id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a [List](https://developer.android.com/reference/kotlin/java/util/List.html#) of [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#) instances representing the certificate chain for the key that was previously shared with the app under the provided`id`. |
| [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#) | [getGrantedKeyFromId](https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager#getGrantedKeyFromId(kotlin.Long))`(`id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the key with the specified`id`that was previously shared with the app. |
| [KeyPair](https://developer.android.com/reference/kotlin/java/security/KeyPair.html#) | [getGrantedKeyPairFromId](https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager#getGrantedKeyPairFromId(kotlin.Long))`(`id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a [KeyPair](https://developer.android.com/reference/kotlin/java/security/KeyPair.html#) containing the public and private key associated with the key that was previously shared with the app under the provided`id`. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getSupplementaryAttestationInfo](https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager#getSupplementaryAttestationInfo(kotlin.Int))`(`tag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns tag-specific data required to interpret a tag's attested value. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [grantKeyAccess](https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager#grantKeyAccess(kotlin.String,%20kotlin.Int))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Grants access to the key owned by the calling app stored under the specified`alias`to another app on the device with the provided`uid`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [revokeKeyAccess](https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager#revokeKeyAccess(kotlin.String,%20kotlin.Int))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Revokes access to the key in the app's namespace stored under the specified`alias`that was previously granted to another app on the device with the provided`uid`. |

## Constants

### MODULE_HASH

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODULE_HASH: Int
```

When passed into getSupplementaryAttestationInfo, getSupplementaryAttestationInfo returns the DER-encoded structure corresponding to the \`Modules\` schema described in the KeyMint HAL's KeyCreationResult.aidl. The SHA-256 hash of this encoded structure is what's included with the tag in attestations. To ensure the returned encoded structure is the one attested to, clients should verify its SHA-256 hash matches the one in the attestation. Note that the returned structure can vary between boots. 

 Value: -1879047468

## Public methods

### getGrantedCertificateChainFromId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGrantedCertificateChainFromId(id: Long): MutableList<X509Certificate!>
```

Returns a [List](https://developer.android.com/reference/kotlin/java/util/List.html#) of [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#) instances representing the certificate chain for the key that was previously shared with the app under the provided`id`.

If a [java.security.PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#) has not been granted to the caller with the specified`id`, then an [UnrecoverableKeyException](https://developer.android.com/reference/kotlin/java/security/UnrecoverableKeyException.html#) is thrown.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the ID of the asymmetric key that was shared with the app |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!> | a List of X509Certificates with the certificate at index 0 corresponding to the private key shared with the app This value cannot be`null`. |

| Exceptions ||
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.UnrecoverableKeyException` | if the specified key cannot be recovered |
| `android.security.keystore.KeyPermanentlyInvalidatedException` | if the specified key was authorized to only be used if the user has been authenticated and a change has been made to the users lockscreen or biometric enrollment that permanently invalidates the key |

**See Also**

- [#grantKeyAccess(String, int)](https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager#grantKeyAccess(kotlin.String,%20kotlin.Int)) 

### getGrantedKeyFromId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGrantedKeyFromId(id: Long): Key
```

Returns the key with the specified`id`that was previously shared with the app.

This method can return instances of both [javax.crypto.SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey.html#) and . If a key with the provide`id`has not been granted to the caller, then an [UnrecoverableKeyException](https://developer.android.com/reference/kotlin/java/security/UnrecoverableKeyException.html#) is thrown.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------|
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the ID of the key that was shared with the app |

| Return ||
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#) | the [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#) that was shared with the app This value cannot be`null`. |

| Exceptions ||
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.UnrecoverableKeyException` | if the specified key cannot be recovered |
| `android.security.keystore.KeyPermanentlyInvalidatedException` | if the specified key was authorized to only be used if the user has been authenticated and a change has been made to the users lockscreen or biometric enrollment that permanently invalidates the key |

**See Also**

- [#grantKeyAccess(String, int)](https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager#grantKeyAccess(kotlin.String,%20kotlin.Int)) 

### getGrantedKeyPairFromId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGrantedKeyPairFromId(id: Long): KeyPair
```

Returns a [KeyPair](https://developer.android.com/reference/kotlin/java/security/KeyPair.html#) containing the public and private key associated with the key that was previously shared with the app under the provided`id`.

If a [java.security.PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#) has not been granted to the caller with the specified`id`, then an [UnrecoverableKeyException](https://developer.android.com/reference/kotlin/java/security/UnrecoverableKeyException.html#) is thrown.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the ID of the private key that was shared with the app |

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [KeyPair](https://developer.android.com/reference/kotlin/java/security/KeyPair.html#) | a KeyPair containing the public and private key shared with the app This value cannot be`null`. |

| Exceptions ||
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.UnrecoverableKeyException` | if the specified key cannot be recovered |
| `android.security.keystore.KeyPermanentlyInvalidatedException` | if the specified key was authorized to only be used if the user has been authenticated and a change has been made to the users lockscreen or biometric enrollment that permanently invalidates the key |

### getSupplementaryAttestationInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSupplementaryAttestationInfo(tag: Int): ByteArray
```

Returns tag-specific data required to interpret a tag's attested value. When performing key attestation, the obtained attestation certificate contains a list of tags and their corresponding attested values. For some tags, additional information about the attested value can be queried via this API. See individual tags for specifics.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):tag for which info is being requested Value is [android.security.keystore.KeyStoreManager#MODULE_HASH](https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager#MODULE_HASH:kotlin.Int) |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | tag-specific info This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|----------------------------------------|
| `android.security.KeyStoreException` | if the requested info is not available |

### grantKeyAccess

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun grantKeyAccess(
    alias: String, 
    uid: Int
): Long
```

Grants access to the key owned by the calling app stored under the specified`alias`to another app on the device with the provided`uid`.

This method supports granting access to instances of both [javax.crypto.SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey.html#) and [java.security.PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#). The resulting ID will persist across reboots and can be used by the grantee app for the life of the key or until access is revoked with [revokeKeyAccess(java.lang.String,int)](https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager#revokeKeyAccess(kotlin.String,%20kotlin.Int)).

If the provided`alias`does not correspond to a key in the Android KeyStore, then an [UnrecoverableKeyException](https://developer.android.com/reference/kotlin/java/security/UnrecoverableKeyException.html#) is thrown.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the alias of the key to be granted to another app This value cannot be`null`. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the uid of the app to which the key should be granted |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the ID of the granted key; this can be shared with the specified app, and that app can use [getGrantedKeyFromId(long)](https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager#getGrantedKeyFromId(kotlin.Long))to access the key |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------|
| `java.security.UnrecoverableKeyException` | if the specified key cannot be recovered |
| `android.security.KeyStoreException` | if an error is encountered when attempting to grant access to the key |

**See Also**

- [#getGrantedKeyFromId(long)](https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager#getGrantedKeyFromId(kotlin.Long)) 

### revokeKeyAccess

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun revokeKeyAccess(
    alias: String, 
    uid: Int
): Unit
```

Revokes access to the key in the app's namespace stored under the specified`alias`that was previously granted to another app on the device with the provided`uid`.

If the provided`alias`does not correspond to a key in the Android KeyStore, then an [UnrecoverableKeyException](https://developer.android.com/reference/kotlin/java/security/UnrecoverableKeyException.html#) is thrown.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the alias of the key to be revoked from another app This value cannot be`null`. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the uid of the app from which the key access should be revoked |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------|
| `java.security.UnrecoverableKeyException` | if the specified key cannot be recovered |
| `android.security.KeyStoreException` | if an error is encountered when attempting to revoke access to the key |
