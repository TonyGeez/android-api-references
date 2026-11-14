# KeyStoreSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyStoreSpi

```
abstract class KeyStoreSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.KeyStoreSpi](KeyStoreSpi.md) |

This class defines the*Service Provider Interface* (**SPI** ) for the`KeyStore`class. All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a keystore for a particular keystore type.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------|---|
| [KeyStoreSpi](KeyStoreSpi.md))`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Enumeration](../java.util/Enumeration.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [engineAliases](KeyStoreSpi.md))`()` Lists all the alias names of this keystore. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [engineContainsAlias](KeyStoreSpi.md))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Checks if the given alias exists in this keystore. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineDeleteEntry](KeyStoreSpi.md))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Deletes the entry identified by the given alias from this keystore. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [engineEntryInstanceOf](KeyStoreSpi.md))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `entryClass:` ` [Class](../java.lang/Class.md)<out` ` [KeyStore.Entry](../java/security/KeyStore.Entry.md)!>!`)` Determines if the keystore`Entry`for the specified`alias`is an instance or subclass of the specified`entryClass`. |
| abstract [Certificate](../java.security.cert/Certificate.md)! | [engineGetCertificate](KeyStoreSpi.md))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the certificate associated with the given alias. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [engineGetCertificateAlias](KeyStoreSpi.md))`(`cert:` ` [Certificate](../java.security.cert/Certificate.md)!`)` Returns the (alias) name of the first keystore entry whose certificate matches the given certificate. |
| --- | --- |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](../java.security.cert/Certificate.md)!\>! | [engineGetCertificateChain](KeyStoreSpi.md))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the certificate chain associated with the given alias. |
| abstract [Date](../java.util/Date.md)! | [engineGetCreationDate](KeyStoreSpi.md))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the creation date of the entry identified by the given alias. |
| open [KeyStore.Entry](../java/security/KeyStore.Entry.md)! | [engineGetEntry](KeyStoreSpi.md))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `protParam:` ` [KeyStore.ProtectionParameter](../java/security/KeyStore.ProtectionParameter.md)!`)` Gets a`KeyStore.Entry`for the specified alias with the specified protection parameter. |
| --- | --- |
| abstract [Key](Key.md)! | [engineGetKey](KeyStoreSpi.md))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `password:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Returns the key associated with the given alias, using the given password to recover it. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [engineIsCertificateEntry](KeyStoreSpi.md))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns true if the entry identified by the given alias was created by a call to`setCertificateEntry`, or created by a call to`setEntry`with a`TrustedCertificateEntry`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [engineIsKeyEntry](KeyStoreSpi.md))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns true if the entry identified by the given alias was created by a call to`setKeyEntry`, or created by a call to`setEntry`with a`PrivateKeyEntry`or a`SecretKeyEntry`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineLoad](KeyStoreSpi.md))`(`stream:` ` [InputStream](../java.io/InputStream.md)!`, `password:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Loads the keystore from the given input stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineLoad](KeyStoreSpi.md))`(`param:` ` [KeyStore.LoadStoreParameter](../java/security/KeyStore.LoadStoreParameter.md)!`)` Loads the keystore using the given`KeyStore.LoadStoreParameter`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [engineProbe](KeyStoreSpi.md))`(`stream:` ` [InputStream](../java.io/InputStream.md)!`)` Probes the specified input stream to determine whether it contains a keystore that is supported by this implementation, or not. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineSetCertificateEntry](KeyStoreSpi.md))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cert:` ` [Certificate](../java.security.cert/Certificate.md)!`)` Assigns the given certificate to the given alias. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineSetEntry](KeyStoreSpi.md))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `entry:` ` [KeyStore.Entry](../java/security/KeyStore.Entry.md)!`, `protParam:` ` [KeyStore.ProtectionParameter](../java/security/KeyStore.ProtectionParameter.md)!`)` Saves a`KeyStore.Entry`under the specified alias. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineSetKeyEntry](KeyStoreSpi.md))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `key:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `chain:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](../java.security.cert/Certificate.md)!>!`)` Assigns the given key (that has already been protected) to the given alias. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineSetKeyEntry](KeyStoreSpi.md))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `key:` ` [Key](Key.md)!`, `password:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `chain:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](../java.security.cert/Certificate.md)!>!`)` Assigns the given key to the given alias, protecting it with the given password. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [engineSize](KeyStoreSpi.md))`()` Retrieves the number of entries in this keystore. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineStore](KeyStoreSpi.md))`(`stream:` ` [OutputStream](../java.io/OutputStream.md)!`, `password:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Stores this keystore to the given output stream, and protects its integrity with the given password. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineStore](KeyStoreSpi.md))`(`param:` ` [KeyStore.LoadStoreParameter](../java/security/KeyStore.LoadStoreParameter.md)!`)` Stores this keystore using the given`KeyStore.LoadStoreParmeter`. |

## Public constructors

### KeyStoreSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyStoreSpi()
```

## Public methods

### engineAliases

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineAliases(): Enumeration<String!>!
```

Lists all the alias names of this keystore.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| [Enumeration](../java.util/Enumeration.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | enumeration of the alias names |

### engineContainsAlias

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineContainsAlias(alias: String!): Boolean
```

Checks if the given alias exists in this keystore.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the alias name |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the alias exists, false otherwise |

### engineDeleteEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineDeleteEntry(alias: String!): Unit
```

Deletes the entry identified by the given alias from this keystore.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the alias name |

| Exceptions ||
|-----------------------------------|---------------------------------|
| `java.security.KeyStoreException` | if the entry cannot be removed. |

### engineEntryInstanceOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun engineEntryInstanceOf(
    alias: String!, 
    entryClass: Class<out KeyStore.Entry!>!
): Boolean
```

Determines if the keystore`Entry`for the specified`alias`is an instance or subclass of the specified`entryClass`.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the alias name |
| `entryClass` | [Class](../java.lang/Class.md)\<out [KeyStore.Entry](../java/security/KeyStore.Entry.md)!\>!:the entry class |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the keystore`Entry`for the specified`alias`is an instance or subclass of the specified`entryClass`, false otherwise |

### engineGetCertificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineGetCertificate(alias: String!): Certificate!
```

Returns the certificate associated with the given alias.

If the given alias name identifies an entry created by a call to`setCertificateEntry`, or created by a call to`setEntry`with a`TrustedCertificateEntry`, then the trusted certificate contained in that entry is returned.

If the given alias name identifies an entry created by a call to`setKeyEntry`, or created by a call to`setEntry`with a`PrivateKeyEntry`, then the first element of the certificate chain in that entry (if a chain exists) is returned.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the alias name |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Certificate](../java.security.cert/Certificate.md)! | the certificate, or null if the given alias does not exist or does not contain a certificate. |

### engineGetCertificateAlias

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineGetCertificateAlias(cert: Certificate!): String!
```

Returns the (alias) name of the first keystore entry whose certificate matches the given certificate.

This method attempts to match the given certificate with each keystore entry. If the entry being considered was created by a call to`setCertificateEntry`, or created by a call to`setEntry`with a`TrustedCertificateEntry`, then the given certificate is compared to that entry's certificate.

If the entry being considered was created by a call to`setKeyEntry`, or created by a call to`setEntry`with a`PrivateKeyEntry`, then the given certificate is compared to the first element of that entry's certificate chain.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------|
| `cert` | [Certificate](../java.security.cert/Certificate.md)!:the certificate to match with. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the alias name of the first entry with matching certificate, or null if no such entry exists in this keystore. |

### engineGetCertificateChain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineGetCertificateChain(alias: String!): Array<Certificate!>!
```

Returns the certificate chain associated with the given alias. The certificate chain must have been associated with the alias by a call to`setKeyEntry`, or by a call to`setEntry`with a`PrivateKeyEntry`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the alias name |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](../java.security.cert/Certificate.md)!>! | the certificate chain (ordered with the user's certificate first and the root certificate authority last), or null if the given alias does not exist or does not contain a certificate chain |

### engineGetCreationDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineGetCreationDate(alias: String!): Date!
```

Returns the creation date of the entry identified by the given alias.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the alias name |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Date](../java.util/Date.md)! | the creation date of this entry, or null if the given alias does not exist |

### engineGetEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun engineGetEntry(
    alias: String!, 
    protParam: KeyStore.ProtectionParameter!
): KeyStore.Entry!
```

Gets a`KeyStore.Entry`for the specified alias with the specified protection parameter.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:get the`KeyStore.Entry`for this alias |
| `protParam` | [KeyStore.ProtectionParameter](../java/security/KeyStore.ProtectionParameter.md)!:the`ProtectionParameter`used to protect the`Entry`, which may be`null` |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [KeyStore.Entry](../java/security/KeyStore.Entry.md)! | the`KeyStore.Entry`for the specified alias, or`null`if there is no such entry |

| Exceptions ||
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.KeyStoreException` | if the operation failed |
| `java.security.NoSuchAlgorithmException` | if the algorithm for recovering the entry cannot be found |
| `java.security.UnrecoverableEntryException` | if the specified`protParam`were insufficient or invalid |
| --- | --- |
| `java.security.UnrecoverableKeyException` | if the entry is a`PrivateKeyEntry`or`SecretKeyEntry`and the specified`protParam`does not contain the information needed to recover the key (e.g. wrong password) |

### engineGetKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineGetKey(
    alias: String!, 
    password: CharArray!
): Key!
```

Returns the key associated with the given alias, using the given password to recover it. The key must have been associated with the alias by a call to`setKeyEntry`, or by a call to`setEntry`with a`PrivateKeyEntry`or`SecretKeyEntry`.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the alias name |
| `password` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the password for recovering the key |

| Return ||
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Key](Key.md)! | the requested key, or null if the given alias does not exist or does not identify a key-related entry. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if the algorithm for recovering the key cannot be found |
| `java.security.UnrecoverableKeyException` | if the key cannot be recovered (e.g., the given password is wrong). |

### engineIsCertificateEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineIsCertificateEntry(alias: String!): Boolean
```

Returns true if the entry identified by the given alias was created by a call to`setCertificateEntry`, or created by a call to`setEntry`with a`TrustedCertificateEntry`.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the alias for the keystore entry to be checked |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the entry identified by the given alias contains a trusted certificate, false otherwise. |

### engineIsKeyEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineIsKeyEntry(alias: String!): Boolean
```

Returns true if the entry identified by the given alias was created by a call to`setKeyEntry`, or created by a call to`setEntry`with a`PrivateKeyEntry`or a`SecretKeyEntry`.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the alias for the keystore entry to be checked |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the entry identified by the given alias is a key-related, false otherwise. |

### engineLoad

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineLoad(
    stream: InputStream!, 
    password: CharArray!
): Unit
```

Loads the keystore from the given input stream.

A password may be given to unlock the keystore (e.g. the keystore resides on a hardware token device), or to check the integrity of the keystore data. If a password is not given for integrity checking, then integrity checking is not performed.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stream` | [InputStream](../java.io/InputStream.md)!:the input stream from which the keystore is loaded, or`null` |
| `password` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the password used to check the integrity of the keystore, the password used to unlock the keystore, or`null` |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if there is an I/O or format problem with the keystore data, if a password is required but not given, or if the given password was incorrect. If the error is due to a wrong password, the [cause](../java.lang/Throwable.md))of the`IOException`should be an`UnrecoverableKeyException` |
| `java.security.NoSuchAlgorithmException` | if the algorithm used to check the integrity of the keystore cannot be found |
| `java.security.cert.CertificateException` | if any of the certificates in the keystore could not be loaded |
| --- | --- |

### engineLoad

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun engineLoad(param: KeyStore.LoadStoreParameter!): Unit
```

Loads the keystore using the given`KeyStore.LoadStoreParameter`.

Note that if this KeyStore has already been loaded, it is reinitialized and loaded again from the given parameter.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `param` | [KeyStore.LoadStoreParameter](../java/security/KeyStore.LoadStoreParameter.md)!:the`KeyStore.LoadStoreParameter`that specifies how to load the keystore, which may be`null` |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the given`KeyStore.LoadStoreParameter`input is not recognized |
| `java.io.IOException` | if there is an I/O or format problem with the keystore data. If the error is due to an incorrect`ProtectionParameter`(e.g. wrong password) the [cause](../java.lang/Throwable.md))of the`IOException`should be an`UnrecoverableKeyException` |
| `java.security.NoSuchAlgorithmException` | if the algorithm used to check the integrity of the keystore cannot be found |
| --- | --- |
| `java.security.cert.CertificateException` | if any of the certificates in the keystore could not be loaded |

### engineProbe

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun engineProbe(stream: InputStream!): Boolean
```

Probes the specified input stream to determine whether it contains a keystore that is supported by this implementation, or not.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------|
| `stream` | [InputStream](../java.io/InputStream.md)!:the keystore data to be probed |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the keystore data is supported, otherwise false |

| Exceptions ||
|----------------------------------|----------------------------------------------------|
| `java.io.IOException` | if there is an I/O problem with the keystore data. |
| `java.lang.NullPointerException` | if stream is`null`. |

### engineSetCertificateEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineSetCertificateEntry(
    alias: String!, 
    cert: Certificate!
): Unit
```

Assigns the given certificate to the given alias.

If the given alias identifies an existing entry created by a call to`setCertificateEntry`, or created by a call to`setEntry`with a`TrustedCertificateEntry`, the trusted certificate in the existing entry is overridden by the given certificate.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the alias name |
| `cert` | [Certificate](../java.security.cert/Certificate.md)!:the certificate |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.KeyStoreException` | if the given alias already exists and does not identify an entry containing a trusted certificate, or this operation fails for some other reason. |

### engineSetEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun engineSetEntry(
    alias: String!, 
    entry: KeyStore.Entry!, 
    protParam: KeyStore.ProtectionParameter!
): Unit
```

Saves a`KeyStore.Entry`under the specified alias. The specified protection parameter is used to protect the`Entry`.

If an entry already exists for the specified alias, it is overridden.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:save the`KeyStore.Entry`under this alias |
| `entry` | [KeyStore.Entry](../java/security/KeyStore.Entry.md)!:the`Entry`to save |
| `protParam` | [KeyStore.ProtectionParameter](../java/security/KeyStore.ProtectionParameter.md)!:the`ProtectionParameter`used to protect the`Entry`, which may be`null` |
| --- | --- |

| Exceptions ||
|-----------------------------------|-------------------------|
| `java.security.KeyStoreException` | if this operation fails |

### engineSetKeyEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineSetKeyEntry(
    alias: String!, 
    key: ByteArray!, 
    chain: Array<Certificate!>!
): Unit
```

Assigns the given key (that has already been protected) to the given alias.

If the protected key is of type`java.security.PrivateKey`, it must be accompanied by a certificate chain certifying the corresponding public key.

If the given alias already exists, the keystore information associated with it is overridden by the given key (and possibly certificate chain).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the alias name |
| `key` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the key (in protected format) to be associated with the alias |
| `chain` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](../java.security.cert/Certificate.md)!\>!:the certificate chain for the corresponding public key (only useful if the protected key is of type`java.security.PrivateKey`). |
| --- | --- |

| Exceptions ||
|-----------------------------------|--------------------------|
| `java.security.KeyStoreException` | if this operation fails. |

### engineSetKeyEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineSetKeyEntry(
    alias: String!, 
    key: Key!, 
    password: CharArray!, 
    chain: Array<Certificate!>!
): Unit
```

Assigns the given key to the given alias, protecting it with the given password.

If the given key is of type`java.security.PrivateKey`, it must be accompanied by a certificate chain certifying the corresponding public key.

If the given alias already exists, the keystore information associated with it is overridden by the given key (and possibly certificate chain).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the alias name |
| `key` | [Key](Key.md)!:the key to be associated with the alias |
| `password` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the password to protect the key |
| --- | --- |
| `chain` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](../java.security.cert/Certificate.md)!\>!:the certificate chain for the corresponding public key (only required if the given key is of type`java.security.PrivateKey`). |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------|
| `java.security.KeyStoreException` | if the given key cannot be protected, or this operation fails for some other reason |

### engineSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineSize(): Int
```

Retrieves the number of entries in this keystore.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of entries in this keystore |

### engineStore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineStore(
    stream: OutputStream!, 
    password: CharArray!
): Unit
```

Stores this keystore to the given output stream, and protects its integrity with the given password.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `stream` | [OutputStream](../java.io/OutputStream.md)!:the output stream to which this keystore is written. |
| `password` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the password to generate the keystore integrity check |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------|
| `java.io.IOException` | if there was an I/O problem with data |
| `java.security.NoSuchAlgorithmException` | if the appropriate data integrity algorithm could not be found |
| `java.security.cert.CertificateException` | if any of the certificates included in the keystore data could not be stored |
| --- | --- |

### engineStore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun engineStore(param: KeyStore.LoadStoreParameter!): Unit
```

Stores this keystore using the given`KeyStore.LoadStoreParmeter`.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `param` | [KeyStore.LoadStoreParameter](../java/security/KeyStore.LoadStoreParameter.md)!:the`KeyStore.LoadStoreParmeter`that specifies how to store the keystore, which may be`null` |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the given`KeyStore.LoadStoreParmeter`input is not recognized |
| `java.io.IOException` | if there was an I/O problem with data |
| `java.security.NoSuchAlgorithmException` | if the appropriate data integrity algorithm could not be found |
| --- | --- |
| `java.security.cert.CertificateException` | if any of the certificates included in the keystore data could not be stored |
