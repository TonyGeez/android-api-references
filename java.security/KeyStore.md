Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyStore

```
open class KeyStore
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore#) |

This class represents a storage facility for cryptographic keys and certificates.

A `KeyStore` manages different types of entries. Each type of entry implements the `KeyStore.Entry` interface. Three basic `KeyStore.Entry` implementations are provided:

- **KeyStore.PrivateKeyEntry**

 This type of entry holds a cryptographic `PrivateKey`, which is optionally stored in a protected format to prevent unauthorized access. It is also accompanied by a certificate chain for the corresponding public key.

 Private keys and certificate chains are used by a given entity for self-authentication. Applications for this authentication include software distribution organizations which sign JAR files as part of releasing and/or licensing software.
- **KeyStore.SecretKeyEntry**

 This type of entry holds a cryptographic `SecretKey`, which is optionally stored in a protected format to prevent unauthorized access.
- **KeyStore.TrustedCertificateEntry**

 This type of entry contains a single public key `Certificate` belonging to another party. It is called a *trusted certificate* because the keystore owner trusts that the public key in the certificate indeed belongs to the identity identified by the *subject* (owner) of the certificate.

 This type of entry can be used to authenticate other parties.

Each entry in a keystore is identified by an "alias" string. In the case of private keys and their associated certificate chains, these strings distinguish among the different ways in which the entity may authenticate itself. For example, the entity may authenticate itself using different certificate authorities, or using different public key algorithms.

Whether aliases are case sensitive is implementation dependent. In order to avoid problems, it is recommended not to use aliases in a KeyStore that only differ in case.

Whether keystores are persistent, and the mechanisms used by the keystore if it is persistent, are not specified here. This allows use of a variety of techniques for protecting sensitive (e.g., private or secret) keys. Smart cards or other integrated cryptographic engines (SafeKeyper) are one option, and simpler mechanisms such as files may also be used (in a variety of formats).

Typical ways to request a KeyStore object include specifying an existing keystore file, relying on the default type and providing a specific keystore type.

- To specify an existing keystore file:

  ```kotlin
  // get keystore password
       char[] password = getPassword();
   
       // probe the keystore file and load the keystore entries
       KeyStore ks = KeyStore.getInstance(new File("keyStoreName"), password);
   
  ```
 The system will probe the specified file to determine its keystore type and return a keystore implementation with its entries already loaded. When this approach is used there is no need to call the keystore's `https://developer.android.com/reference/kotlin/java/security/KeyStore#load(java.io.InputStream,%20kotlin.CharArray)` method.
- To rely on the default type:

  ```kotlin
  KeyStore ks = KeyStore.getInstance(KeyStore.getDefaultType());
    
  ```
 The system will return a keystore implementation for the default type.
- To provide a specific keystore type:

  ```kotlin
  KeyStore ks = KeyStore.getInstance("JKS");
    
  ```
 The system will return the most preferred implementation of the specified keystore type available in the environment.

Before a keystore can be accessed, it must be `https://developer.android.com/reference/kotlin/java/security/KeyStore#load(java.io.InputStream,%20kotlin.CharArray)`.

```kotlin
KeyStore ks = KeyStore.getInstance(KeyStore.getDefaultType());
 
     // get user password and file input stream
     char[] password = getPassword();
 
     try (FileInputStream fis = new FileInputStream("keyStoreName")) {
         ks.load(fis, password);
     }
  
```
To create an empty keystore using the above `load` method, pass `null` as the `InputStream` argument.

Once the keystore has been loaded, it is possible to read existing entries from the keystore, or to write new entries into the keystore:

```kotlin
KeyStore.ProtectionParameter protParam =
         new KeyStore.PasswordProtection(password);
 
     // get my private key
     KeyStore.PrivateKeyEntry pkEntry = (KeyStore.PrivateKeyEntry)
         ks.getEntry("privateKeyAlias", protParam);
     PrivateKey myPrivateKey = pkEntry.getPrivateKey();
 
     // save my secret key
     javax.crypto.SecretKey mySecretKey;
     KeyStore.SecretKeyEntry skEntry =
         new KeyStore.SecretKeyEntry(mySecretKey);
     ks.setEntry("secretKeyAlias", skEntry, protParam);
 
     // store away the keystore
     try (FileOutputStream fos = new FileOutputStream("newKeyStoreName")) {
         ks.store(fos, password);
     }
  
```
Note that although the same password may be used to load the keystore, to protect the private key entry, to protect the secret key entry, and to store the keystore (as is shown in the sample code above), different passwords or other protection parameters may also be used.

Android provides the following `KeyStore` types:

| Algorithm | Supported API Levels |
|---|---|
| AndroidCAStore | 14+ |
| AndroidKeyStore | 18+ |
| BCPKCS12 | 1-8 |
| BKS | 1+ |
| BouncyCastle | 1+ |
| PKCS12 | 1+ |
| PKCS12-DEF | 1-8 |

These types are described in the [KeyStore section](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#KeyStore) of the Java Cryptography Architecture Standard Algorithm Name Documentation.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/java/security/KeyStore.Builder` A description of a to-be-instantiated KeyStore object. |
| open | `https://developer.android.com/reference/kotlin/java/security/KeyStore.CallbackHandlerProtection` A ProtectionParameter encapsulating a CallbackHandler. |
| abstract | `https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry` A marker interface for `KeyStore` entry types. |
| abstract | `https://developer.android.com/reference/kotlin/java/security/KeyStore.LoadStoreParameter` A marker interface for `KeyStore` `https://developer.android.com/reference/kotlin/java/security/KeyStore#load(java.security.KeyStore.LoadStoreParameter)` and `https://developer.android.com/reference/kotlin/java/security/KeyStore#store(java.security.KeyStore.LoadStoreParameter)` parameters. |
| open | `https://developer.android.com/reference/kotlin/java/security/KeyStore.PasswordProtection` A password-based implementation of `ProtectionParameter`. |
| | `https://developer.android.com/reference/kotlin/java/security/KeyStore.PrivateKeyEntry` A `KeyStore` entry that holds a `PrivateKey` and corresponding certificate chain. |
| abstract | `https://developer.android.com/reference/kotlin/java/security/KeyStore.ProtectionParameter` A marker interface for keystore protection parameters. |
| | `https://developer.android.com/reference/kotlin/java/security/KeyStore.SecretKeyEntry` A `KeyStore` entry that holds a `SecretKey`. |
| | `https://developer.android.com/reference/kotlin/java/security/KeyStore.TrustedCertificateEntry` A `KeyStore` entry that holds a trusted `Certificate`. |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/KeyStore#KeyStore(java.security.KeyStoreSpi,%20java.security.Provider,%20kotlin.String)(keyStoreSpi: https://developer.android.com/reference/kotlin/java/security/KeyStoreSpi!, provider: https://developer.android.com/reference/kotlin/java/security/Provider!, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a KeyStore object of the given type, and encapsulates the given provider implementation (SPI object) in it. |

| Public methods ||
|---|---|
| [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/security/KeyStore#aliases()()` Lists all the alias names of this keystore. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/security/KeyStore#containsAlias(kotlin.String)(alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Checks if the given alias exists in this keystore. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/KeyStore#deleteEntry(kotlin.String)(alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Deletes the entry identified by the given alias from this keystore. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/security/KeyStore#entryInstanceOf(kotlin.String,%20java.lang.Class)(alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, entryClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<out https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry!>!)` Determines if the keystore `Entry` for the specified `alias` is an instance or subclass of the specified `entryClass`. |
| [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)! | `https://developer.android.com/reference/kotlin/java/security/KeyStore#getCertificate(kotlin.String)(alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the certificate associated with the given alias. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/security/KeyStore#getCertificateAlias(java.security.cert.Certificate)(cert: https://developer.android.com/reference/kotlin/java/security/cert/Certificate!)` Returns the (alias) name of the first keystore entry whose certificate matches the given certificate. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!\>! | `https://developer.android.com/reference/kotlin/java/security/KeyStore#getCertificateChain(kotlin.String)(alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the certificate chain associated with the given alias. |
| [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | `https://developer.android.com/reference/kotlin/java/security/KeyStore#getCreationDate(kotlin.String)(alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the creation date of the entry identified by the given alias. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/security/KeyStore#getDefaultType()()` Returns the default keystore type as specified by the `keystore.type` security property, or the string "jks" (acronym for "Java keystore") if no such property exists. |
| [KeyStore.Entry](https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry)! | `https://developer.android.com/reference/kotlin/java/security/KeyStore#getEntry(kotlin.String,%20java.security.KeyStore.ProtectionParameter)(alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, protParam: https://developer.android.com/reference/kotlin/java/security/KeyStore.ProtectionParameter!)` Gets a keystore `Entry` for the specified alias with the specified protection parameter. |
| static [KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore#)! | `https://developer.android.com/reference/kotlin/java/security/KeyStore#getInstance(java.io.File,%20kotlin.CharArray)(file: https://developer.android.com/reference/kotlin/java/io/File.html#!, password: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!)` Returns a loaded keystore object of the appropriate keystore type. |
| static [KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore#)! | `https://developer.android.com/reference/kotlin/java/security/KeyStore#getInstance(java.io.File,%20java.security.KeyStore.LoadStoreParameter)(file: https://developer.android.com/reference/kotlin/java/io/File.html#!, param: https://developer.android.com/reference/kotlin/java/security/KeyStore.LoadStoreParameter!)` Returns a loaded keystore object of the appropriate keystore type. |
| open static [KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore#)! | `https://developer.android.com/reference/kotlin/java/security/KeyStore#getInstance(kotlin.String)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns a keystore object of the specified type. |
| open static [KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore#)! | `https://developer.android.com/reference/kotlin/java/security/KeyStore#getInstance(kotlin.String,%20kotlin.String)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, provider: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns a keystore object of the specified type. |
| open static [KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore#)! | `https://developer.android.com/reference/kotlin/java/security/KeyStore#getInstance(kotlin.String,%20java.security.Provider)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, provider: https://developer.android.com/reference/kotlin/java/security/Provider!)` Returns a keystore object of the specified type. |
| [Key](https://developer.android.com/reference/kotlin/java/security/Key)! | `https://developer.android.com/reference/kotlin/java/security/KeyStore#getKey(kotlin.String,%20kotlin.CharArray)(alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, password: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!)` Returns the key associated with the given alias, using the given password to recover it. |
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)! | `https://developer.android.com/reference/kotlin/java/security/KeyStore#getProvider()()` Returns the provider of this keystore. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/security/KeyStore#getType()()` Returns the type of this keystore. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/security/KeyStore#isCertificateEntry(kotlin.String)(alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns true if the entry identified by the given alias was created by a call to `setCertificateEntry`, or created by a call to `setEntry` with a `TrustedCertificateEntry`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/security/KeyStore#isKeyEntry(kotlin.String)(alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns true if the entry identified by the given alias was created by a call to `setKeyEntry`, or created by a call to `setEntry` with a `PrivateKeyEntry` or a `SecretKeyEntry`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/KeyStore#load(java.io.InputStream,%20kotlin.CharArray)(stream: https://developer.android.com/reference/kotlin/java/io/InputStream.html#!, password: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!)` Loads this KeyStore from the given input stream. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/KeyStore#load(java.security.KeyStore.LoadStoreParameter)(param: https://developer.android.com/reference/kotlin/java/security/KeyStore.LoadStoreParameter!)` Loads this keystore using the given `LoadStoreParameter`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/KeyStore#setCertificateEntry(kotlin.String,%20java.security.cert.Certificate)(alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, cert: https://developer.android.com/reference/kotlin/java/security/cert/Certificate!)` Assigns the given trusted certificate to the given alias. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/KeyStore#setEntry(kotlin.String,%20java.security.KeyStore.Entry,%20java.security.KeyStore.ProtectionParameter)(alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, entry: https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry!, protParam: https://developer.android.com/reference/kotlin/java/security/KeyStore.ProtectionParameter!)` Saves a keystore `Entry` under the specified alias. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/KeyStore#setKeyEntry(kotlin.String,%20kotlin.ByteArray,%20kotlin.Array)(alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, chain: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/security/cert/Certificate!>!)` Assigns the given key (that has already been protected) to the given alias. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/KeyStore#setKeyEntry(kotlin.String,%20java.security.Key,%20kotlin.CharArray,%20kotlin.Array)(alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, key: https://developer.android.com/reference/kotlin/java/security/Key!, password: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, chain: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/security/cert/Certificate!>!)` Assigns the given key to the given alias, protecting it with the given password. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/security/KeyStore#size()()` Retrieves the number of entries in this keystore. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/KeyStore#store(java.io.OutputStream,%20kotlin.CharArray)(stream: https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!, password: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!)` Stores this keystore to the given output stream, and protects its integrity with the given password. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/KeyStore#store(java.security.KeyStore.LoadStoreParameter)(param: https://developer.android.com/reference/kotlin/java/security/KeyStore.LoadStoreParameter!)` Stores this keystore using the given `LoadStoreParameter`. |

## Protected constructors

### KeyStore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected KeyStore(
    keyStoreSpi: KeyStoreSpi!, 
    provider: Provider!, 
    type: String!)
```

Creates a KeyStore object of the given type, and encapsulates the given provider implementation (SPI object) in it.

| Parameters ||
|---|---|
| `keyStoreSpi` | [KeyStoreSpi](https://developer.android.com/reference/kotlin/java/security/KeyStoreSpi)!: the provider implementation. |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!: the provider. |
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the keystore type. |

## Public methods

### aliases

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun aliases(): Enumeration<String!>!
```

Lists all the alias names of this keystore.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Enumeration.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | enumeration of the alias names |

| Exceptions ||
|---|---|
| `java.security.KeyStoreException` | if the keystore has not been initialized (loaded). |

### containsAlias

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun containsAlias(alias: String!): Boolean
```

Checks if the given alias exists in this keystore.

| Parameters ||
|---|---|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the alias name |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the alias exists, false otherwise |

| Exceptions ||
|---|---|
| `java.security.KeyStoreException` | if the keystore has not been initialized (loaded). |

### deleteEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun deleteEntry(alias: String!): Unit
```

Deletes the entry identified by the given alias from this keystore.

| Parameters ||
|---|---|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the alias name |

| Exceptions ||
|---|---|
| `java.security.KeyStoreException` | if the keystore has not been initialized, or if the entry cannot be removed. |

### entryInstanceOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun entryInstanceOf(
    alias: String!, 
    entryClass: Class<out KeyStore.Entry!>!
): Boolean
```

Determines if the keystore `Entry` for the specified `alias` is an instance or subclass of the specified `entryClass`.

| Parameters ||
|---|---|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the alias name |
| `entryClass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<out [KeyStore.Entry](https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry)!\>!: the entry class |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the keystore `Entry` for the specified `alias` is an instance or subclass of the specified `entryClass`, false otherwise |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `alias` or `entryClass` is `null` |
| `java.security.KeyStoreException` | if the keystore has not been initialized (loaded) |

### getCertificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCertificate(alias: String!): Certificate!
```

Returns the certificate associated with the given alias.

If the given alias name identifies an entry created by a call to `setCertificateEntry`, or created by a call to `setEntry` with a `TrustedCertificateEntry`, then the trusted certificate contained in that entry is returned.

If the given alias name identifies an entry created by a call to `setKeyEntry`, or created by a call to `setEntry` with a `PrivateKeyEntry`, then the first element of the certificate chain in that entry is returned.

| Parameters ||
|---|---|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the alias name |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/cert/Certificate!` | the certificate, or null if the given alias does not exist or does not contain a certificate. |

| Exceptions ||
|---|---|
| `java.security.KeyStoreException` | if the keystore has not been initialized (loaded). |

### getCertificateAlias

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCertificateAlias(cert: Certificate!): String!
```

Returns the (alias) name of the first keystore entry whose certificate matches the given certificate.

This method attempts to match the given certificate with each keystore entry. If the entry being considered was created by a call to `setCertificateEntry`, or created by a call to `setEntry` with a `TrustedCertificateEntry`, then the given certificate is compared to that entry's certificate.

If the entry being considered was created by a call to `setKeyEntry`, or created by a call to `setEntry` with a `PrivateKeyEntry`, then the given certificate is compared to the first element of that entry's certificate chain.

| Parameters ||
|---|---|
| `cert` | [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!: the certificate to match with. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the alias name of the first entry with a matching certificate, or null if no such entry exists in this keystore. |

| Exceptions ||
|---|---|
| `java.security.KeyStoreException` | if the keystore has not been initialized (loaded). |

### getCertificateChain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCertificateChain(alias: String!): Array<Certificate!>!
```

Returns the certificate chain associated with the given alias. The certificate chain must have been associated with the alias by a call to `setKeyEntry`, or by a call to `setEntry` with a `PrivateKeyEntry`.

| Parameters ||
|---|---|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the alias name |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/security/cert/Certificate!>!` | the certificate chain (ordered with the user's certificate first followed by zero or more certificate authorities), or null if the given alias does not exist or does not contain a certificate chain |

| Exceptions ||
|---|---|
| `java.security.KeyStoreException` | if the keystore has not been initialized (loaded). |

### getCreationDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCreationDate(alias: String!): Date!
```

Returns the creation date of the entry identified by the given alias.

| Parameters ||
|---|---|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the alias name |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Date.html#!` | the creation date of this entry, or null if the given alias does not exist |

| Exceptions ||
|---|---|
| `java.security.KeyStoreException` | if the keystore has not been initialized (loaded). |

### getDefaultType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDefaultType(): String!
```

Returns the default keystore type as specified by the `keystore.type` security property, or the string "jks" (acronym for "Java keystore") if no such property exists.

The default keystore type can be used by applications that do not want to use a hard-coded keystore type when calling one of the `getInstance` methods, and want to provide a default keystore type in case a user does not specify its own.

The default keystore type can be changed by setting the value of the `keystore.type` security property to the desired keystore type.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the default keystore type as specified by the `keystore.type` security property, or the string "jks" if no such property exists. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/Security`

### getEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEntry(
    alias: String!, 
    protParam: KeyStore.ProtectionParameter!
): KeyStore.Entry!
```

Gets a keystore `Entry` for the specified alias with the specified protection parameter.

| Parameters ||
|---|---|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: get the keystore `Entry` for this alias |
| `protParam` | [KeyStore.ProtectionParameter](https://developer.android.com/reference/kotlin/java/security/KeyStore.ProtectionParameter)!: the `ProtectionParameter` used to protect the `Entry`, which may be `null` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry!` | the keystore `Entry` for the specified alias, or `null` if there is no such entry |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `alias` is `null` |
| `java.security.KeyStoreException` | if the keystore has not been initialized (loaded). |
| `java.security.NoSuchAlgorithmException` | if the algorithm for recovering the entry cannot be found |
| `java.security.UnrecoverableEntryException` | if the specified `protParam` were insufficient or invalid |
| `java.security.UnrecoverableKeyException` | if the entry is a `PrivateKeyEntry` or `SecretKeyEntry` and the specified `protParam` does not contain the information needed to recover the key (e.g. wrong password) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/KeyStore#setEntry(kotlin.String,%20java.security.KeyStore.Entry,%20java.security.KeyStore.ProtectionParameter)`

### getInstance

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(
    file: File!, 
    password: CharArray!
): KeyStore!
```

Returns a loaded keystore object of the appropriate keystore type. First the keystore type is determined by probing the specified file. Then a keystore object is instantiated and loaded using the data from that file.

A password may be given to unlock the keystore (e.g. the keystore resides on a hardware token device), or to check the integrity of the keystore data. If a password is not given for integrity checking, then integrity checking is not performed.

This method traverses the list of registered security [providers](https://developer.android.com/reference/kotlin/java/security/Provider), starting with the most preferred Provider. For each `https://developer.android.com/reference/kotlin/java/security/KeyStoreSpi` implementation supported by a Provider, it invokes the `https://developer.android.com/reference/kotlin/java/security/KeyStoreSpi#engineProbe(java.io.InputStream)` method to determine if it supports the specified keystore. A new KeyStore object is returned that encapsulates the KeyStoreSpi implementation from the first Provider that supports the specified file.

Note that the list of registered providers may be retrieved via the `https://developer.android.com/reference/kotlin/java/security/Security#getProviders()` method.

| Parameters ||
|---|---|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!: the keystore file |
| `password` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the keystore password, which may be `null` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/KeyStore#!` | a keystore object loaded with keystore data |

| Exceptions ||
|---|---|
| `java.io.IOException` | if there is an I/O or format problem with the keystore data, if a password is required but not given, or if the given password was incorrect. If the error is due to a wrong password, the `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause()` of the `IOException` should be an `UnrecoverableKeyException`. |
| `java.lang.IllegalArgumentException` | if file does not exist or does not refer to a normal file. |
| `java.lang.NullPointerException` | if file is `null`. |
| `java.lang.SecurityException` | if a security manager exists and its java.lang.SecurityManager#checkRead method denies read access to the specified file. |
| `java.security.KeyStoreException` | if no Provider supports a KeyStoreSpi implementation for the specified keystore file. |
| `java.security.NoSuchAlgorithmException` | if the algorithm used to check the integrity of the keystore cannot be found. |
| `java.security.cert.CertificateException` | if any of the certificates in the keystore could not be loaded. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/Provider`

### getInstance

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(
    file: File!, 
    param: KeyStore.LoadStoreParameter!
): KeyStore!
```

Returns a loaded keystore object of the appropriate keystore type. First the keystore type is determined by probing the specified file. Then a keystore object is instantiated and loaded using the data from that file. A `LoadStoreParameter` may be supplied which specifies how to unlock the keystore data or perform an integrity check.

This method traverses the list of registered security [providers](https://developer.android.com/reference/kotlin/java/security/Provider), starting with the most preferred Provider. For each `https://developer.android.com/reference/kotlin/java/security/KeyStoreSpi` implementation supported by a Provider, it invokes the `https://developer.android.com/reference/kotlin/java/security/KeyStoreSpi#engineProbe(java.io.InputStream)` method to determine if it supports the specified keystore. A new KeyStore object is returned that encapsulates the KeyStoreSpi implementation from the first Provider that supports the specified file.

Note that the list of registered providers may be retrieved via the `https://developer.android.com/reference/kotlin/java/security/Security#getProviders()` method.

| Parameters ||
|---|---|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!: the keystore file |
| `param` | [KeyStore.LoadStoreParameter](https://developer.android.com/reference/kotlin/java/security/KeyStore.LoadStoreParameter)!: the `LoadStoreParameter` that specifies how to load the keystore, which may be `null` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/KeyStore#!` | a keystore object loaded with keystore data |

| Exceptions ||
|---|---|
| `java.io.IOException` | if there is an I/O or format problem with the keystore data. If the error is due to an incorrect `ProtectionParameter` (e.g. wrong password) the `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause()` of the `IOException` should be an `UnrecoverableKeyException`. |
| `java.lang.IllegalArgumentException` | if file does not exist or does not refer to a normal file, or if param is not recognized. |
| `java.lang.NullPointerException` | if file is `null`. |
| `java.lang.SecurityException` | if a security manager exists and its java.lang.SecurityManager#checkRead method denies read access to the specified file. |
| `java.security.KeyStoreException` | if no Provider supports a KeyStoreSpi implementation for the specified keystore file. |
| `java.security.NoSuchAlgorithmException` | if the algorithm used to check the integrity of the keystore cannot be found. |
| `java.security.cert.CertificateException` | if any of the certificates in the keystore could not be loaded. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/Provider`

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(type: String!): KeyStore!
```

Returns a keystore object of the specified type.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new KeyStore object encapsulating the KeyStoreSpi implementation from the first Provider that supports the specified type is returned.

Note that the list of registered providers may be retrieved via the `https://developer.android.com/reference/kotlin/java/security/Security#getProviders()` method.

| Parameters ||
|---|---|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the type of keystore. See the KeyStore section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#keystore-types) for information about standard keystore types. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/KeyStore#!` | a keystore object of the specified type |

| Exceptions ||
|---|---|
| `java.security.KeyStoreException` | if no Provider supports a KeyStoreSpi implementation for the specified type. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/Provider`

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(
    type: String!, 
    provider: String!
): KeyStore!
```

Returns a keystore object of the specified type.

A new KeyStore object encapsulating the KeyStoreSpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the `https://developer.android.com/reference/kotlin/java/security/Security#getProviders()` method.

| Parameters ||
|---|---|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the type of keystore. See the KeyStore section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#keystore-types) for information about standard keystore types. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the provider. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/KeyStore#!` | a keystore object of the specified type |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the provider name is null or empty. |
| `java.security.KeyStoreException` | if a KeyStoreSpi implementation for the specified type is not available from the specified provider. |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/Provider`

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(
    type: String!, 
    provider: Provider!
): KeyStore!
```

Returns a keystore object of the specified type.

A new KeyStore object encapsulating the KeyStoreSpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

| Parameters ||
|---|---|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the type of keystore. See the KeyStore section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#keystore-types) for information about standard keystore types. |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!: the provider. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/KeyStore#!` | a keystore object of the specified type |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the specified provider is `null` |
| `java.lang.NullPointerException` | if `type` is `null` |
| `java.security.KeyStoreException` | if `KeyStoreSpi` implementation for the specified type is not available from the specified `Provider` object |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/Provider`

### getKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKey(
    alias: String!, 
    password: CharArray!
): Key!
```

Returns the key associated with the given alias, using the given password to recover it. The key must have been associated with the alias by a call to `setKeyEntry`, or by a call to `setEntry` with a `PrivateKeyEntry` or `SecretKeyEntry`.

| Parameters ||
|---|---|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the alias name |
| `password` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the password for recovering the key |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/Key!` | the requested key, or null if the given alias does not exist or does not identify a key-related entry. |

| Exceptions ||
|---|---|
| `java.security.KeyStoreException` | if the keystore has not been initialized (loaded). |
| `java.security.NoSuchAlgorithmException` | if the algorithm for recovering the key cannot be found |
| `java.security.UnrecoverableKeyException` | if the key cannot be recovered (e.g., the given password is wrong). |

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProvider(): Provider!
```

Returns the provider of this keystore.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/Provider!` | the provider of this keystore. |

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(): String!
```

Returns the type of this keystore.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the type of this keystore. |

### isCertificateEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isCertificateEntry(alias: String!): Boolean
```

Returns true if the entry identified by the given alias was created by a call to `setCertificateEntry`, or created by a call to `setEntry` with a `TrustedCertificateEntry`.

| Parameters ||
|---|---|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the alias for the keystore entry to be checked |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the entry identified by the given alias contains a trusted certificate, false otherwise. |

| Exceptions ||
|---|---|
| `java.security.KeyStoreException` | if the keystore has not been initialized (loaded). |

### isKeyEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isKeyEntry(alias: String!): Boolean
```

Returns true if the entry identified by the given alias was created by a call to `setKeyEntry`, or created by a call to `setEntry` with a `PrivateKeyEntry` or a `SecretKeyEntry`.

| Parameters ||
|---|---|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the alias for the keystore entry to be checked |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the entry identified by the given alias is a key-related entry, false otherwise. |

| Exceptions ||
|---|---|
| `java.security.KeyStoreException` | if the keystore has not been initialized (loaded). |

### load

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun load(
    stream: InputStream!, 
    password: CharArray!
): Unit
```

Loads this KeyStore from the given input stream.

A password may be given to unlock the keystore (e.g. the keystore resides on a hardware token device), or to check the integrity of the keystore data. If a password is not given for integrity checking, then integrity checking is not performed.

In order to create an empty keystore, or if the keystore cannot be initialized from a stream, pass `null` as the `stream` argument.

Note that if this keystore has already been loaded, it is reinitialized and loaded again from the given input stream.

| Parameters ||
|---|---|
| `stream` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!: the input stream from which the keystore is loaded, or `null` |
| `password` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the password used to check the integrity of the keystore, the password used to unlock the keystore, or `null` |

| Exceptions ||
|---|---|
| `java.io.IOException` | if there is an I/O or format problem with the keystore data, if a password is required but not given, or if the given password was incorrect. If the error is due to a wrong password, the `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause()` of the `IOException` should be an `UnrecoverableKeyException` |
| `java.security.NoSuchAlgorithmException` | if the algorithm used to check the integrity of the keystore cannot be found |
| `java.security.cert.CertificateException` | if any of the certificates in the keystore could not be loaded |

### load

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun load(param: KeyStore.LoadStoreParameter!): Unit
```

Loads this keystore using the given `LoadStoreParameter`.

Note that if this KeyStore has already been loaded, it is reinitialized and loaded again from the given parameter.

| Parameters ||
|---|---|
| `param` | [KeyStore.LoadStoreParameter](https://developer.android.com/reference/kotlin/java/security/KeyStore.LoadStoreParameter)!: the `LoadStoreParameter` that specifies how to load the keystore, which may be `null` |

| Exceptions ||
|---|---|
| `java.io.IOException` | if there is an I/O or format problem with the keystore data. If the error is due to an incorrect `ProtectionParameter` (e.g. wrong password) the `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause()` of the `IOException` should be an `UnrecoverableKeyException` |
| `java.lang.IllegalArgumentException` | if the given `LoadStoreParameter` input is not recognized |
| `java.security.NoSuchAlgorithmException` | if the algorithm used to check the integrity of the keystore cannot be found |
| `java.security.cert.CertificateException` | if any of the certificates in the keystore could not be loaded |

### setCertificateEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCertificateEntry(
    alias: String!, 
    cert: Certificate!
): Unit
```

Assigns the given trusted certificate to the given alias.

If the given alias identifies an existing entry created by a call to `setCertificateEntry`, or created by a call to `setEntry` with a `TrustedCertificateEntry`, the trusted certificate in the existing entry is overridden by the given certificate.

| Parameters ||
|---|---|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the alias name |
| `cert` | [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!: the certificate |

| Exceptions ||
|---|---|
| `java.security.KeyStoreException` | if the keystore has not been initialized, or the given alias already exists and does not identify an entry containing a trusted certificate, or this operation fails for some other reason. |

### setEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setEntry(
    alias: String!, 
    entry: KeyStore.Entry!, 
    protParam: KeyStore.ProtectionParameter!
): Unit
```

Saves a keystore `Entry` under the specified alias. The protection parameter is used to protect the `Entry`.

If an entry already exists for the specified alias, it is overridden.

| Parameters ||
|---|---|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: save the keystore `Entry` under this alias |
| `entry` | [KeyStore.Entry](https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry)!: the `Entry` to save |
| `protParam` | [KeyStore.ProtectionParameter](https://developer.android.com/reference/kotlin/java/security/KeyStore.ProtectionParameter)!: the `ProtectionParameter` used to protect the `Entry`, which may be `null` |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `alias` or `entry` is `null` |
| `java.security.KeyStoreException` | if the keystore has not been initialized (loaded), or if this operation fails for some other reason |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/KeyStore#getEntry(kotlin.String,%20java.security.KeyStore.ProtectionParameter)`

### setKeyEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setKeyEntry(
    alias: String!, 
    key: ByteArray!, 
    chain: Array<Certificate!>!
): Unit
```

Assigns the given key (that has already been protected) to the given alias.

If the protected key is of type `java.security.PrivateKey`, it must be accompanied by a certificate chain certifying the corresponding public key. If the underlying keystore implementation is of type `jks`, `key` must be encoded as an `EncryptedPrivateKeyInfo` as defined in the PKCS #8 standard.

If the given alias already exists, the keystore information associated with it is overridden by the given key (and possibly certificate chain).

| Parameters ||
|---|---|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the alias name |
| `key` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the key (in protected format) to be associated with the alias |
| `chain` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!\>!: the certificate chain for the corresponding public key (only useful if the protected key is of type `java.security.PrivateKey`). |

| Exceptions ||
|---|---|
| `java.security.KeyStoreException` | if the keystore has not been initialized (loaded), or if this operation fails for some other reason. |

### setKeyEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setKeyEntry(
    alias: String!, 
    key: Key!, 
    password: CharArray!, 
    chain: Array<Certificate!>!
): Unit
```

Assigns the given key to the given alias, protecting it with the given password.

If the given key is of type `java.security.PrivateKey`, it must be accompanied by a certificate chain certifying the corresponding public key.

If the given alias already exists, the keystore information associated with it is overridden by the given key (and possibly certificate chain).

| Parameters ||
|---|---|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the alias name |
| `key` | [Key](https://developer.android.com/reference/kotlin/java/security/Key)!: the key to be associated with the alias |
| `password` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the password to protect the key |
| `chain` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!\>!: the certificate chain for the corresponding public key (only required if the given key is of type `java.security.PrivateKey`). |

| Exceptions ||
|---|---|
| `java.security.KeyStoreException` | if the keystore has not been initialized (loaded), the given key cannot be protected, or this operation fails for some other reason |

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun size(): Int
```

Retrieves the number of entries in this keystore.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of entries in this keystore |

| Exceptions ||
|---|---|
| `java.security.KeyStoreException` | if the keystore has not been initialized (loaded). |

### store

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun store(
    stream: OutputStream!, 
    password: CharArray!
): Unit
```

Stores this keystore to the given output stream, and protects its integrity with the given password.

| Parameters ||
|---|---|
| `stream` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!: the output stream to which this keystore is written. |
| `password` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the password to generate the keystore integrity check |

| Exceptions ||
|---|---|
| `java.io.IOException` | if there was an I/O problem with data |
| `java.security.KeyStoreException` | if the keystore has not been initialized (loaded). |
| `java.security.NoSuchAlgorithmException` | if the appropriate data integrity algorithm could not be found |
| `java.security.cert.CertificateException` | if any of the certificates included in the keystore data could not be stored |

### store

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun store(param: KeyStore.LoadStoreParameter!): Unit
```

Stores this keystore using the given `LoadStoreParameter`.

| Parameters ||
|---|---|
| `param` | [KeyStore.LoadStoreParameter](https://developer.android.com/reference/kotlin/java/security/KeyStore.LoadStoreParameter)!: the `LoadStoreParameter` that specifies how to store the keystore, which may be `null` |

| Exceptions ||
|---|---|
| `java.io.IOException` | if there was an I/O problem with data |
| `java.lang.IllegalArgumentException` | if the given `LoadStoreParameter` input is not recognized |
| `java.security.KeyStoreException` | if the keystore has not been initialized (loaded) |
| `java.security.NoSuchAlgorithmException` | if the appropriate data integrity algorithm could not be found |
| `java.security.cert.CertificateException` | if any of the certificates included in the keystore data could not be stored |
