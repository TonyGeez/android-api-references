# java.security

# java.security

## Interfaces

| [AlgorithmConstraints](https://developer.android.com/reference/kotlin/java/security/AlgorithmConstraints) | This interface specifies constraints for cryptographic algorithms, keys (key sizes), and other algorithm parameters. |
| --- | --- |
| [Certificate](https://developer.android.com/reference/kotlin/java/security/Certificate) | This is an interface of abstract methods for managing a variety of identity certificates. |
| [DomainCombiner](https://developer.android.com/reference/kotlin/java/security/DomainCombiner) | Legacy security code; do not use. |
| [Guard](https://developer.android.com/reference/kotlin/java/security/Guard) | This interface represents a guard, which is an object that is used to protect access to another object. |
| --- | --- |
| [Key](https://developer.android.com/reference/kotlin/java/security/Key) | The Key interface is the top-level interface for all keys. |
| [Entry](https://developer.android.com/reference/kotlin/java/security/KeyStore.Entry) | A marker interface for`KeyStore`entry types. |
| [LoadStoreParameter](https://developer.android.com/reference/kotlin/java/security/KeyStore.LoadStoreParameter) | A marker interface for`KeyStore` [load](https://developer.android.com/reference/kotlin/java/security/KeyStore#load(java.security.KeyStore.LoadStoreParameter))and [store](https://developer.android.com/reference/kotlin/java/security/KeyStore#store(java.security.KeyStore.LoadStoreParameter))parameters. |
| --- | --- |
| [ProtectionParameter](https://developer.android.com/reference/kotlin/java/security/KeyStore.ProtectionParameter) | A marker interface for keystore protection parameters. |
| [Parameters](https://developer.android.com/reference/kotlin/java/security/Policy.Parameters) | <br /> |
| [Principal](https://developer.android.com/reference/kotlin/java/security/Principal) | This interface represents the abstract notion of a principal, which can be used to represent any entity, such as an individual, a corporation, and a login id. |
| --- | --- |
| [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey) | A private key. |
| [PrivilegedAction](https://developer.android.com/reference/kotlin/java/security/PrivilegedAction) | Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). |
| [PrivilegedExceptionAction](https://developer.android.com/reference/kotlin/java/security/PrivilegedExceptionAction) | Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). |
| --- | --- |
| [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey) | A public key. |
| [SecureRandomParameters](https://developer.android.com/reference/kotlin/java/security/SecureRandomParameters) | A marker interface for parameters used in various`SecureRandom`methods. |

## Classes

| [AccessControlContext](https://developer.android.com/reference/kotlin/java/security/AccessControlContext) | Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). |
| --- | --- |
| [AccessController](https://developer.android.com/reference/kotlin/java/security/AccessController) | Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). |
| [AlgorithmParameterGenerator](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGenerator) | The`AlgorithmParameterGenerator`class is used to generate a set of parameters to be used with a certain algorithm. |
| [AlgorithmParameterGeneratorSpi](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameterGeneratorSpi) | This class defines the*Service Provider Interface* (**SPI** ) for the`AlgorithmParameterGenerator`class, which is used to generate a set of parameters to be used with a certain algorithm. |
| --- | --- |
| [AlgorithmParameters](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameters) | This class is used as an opaque representation of cryptographic parameters. |
| [AlgorithmParametersSpi](https://developer.android.com/reference/kotlin/java/security/AlgorithmParametersSpi) | This class defines the*Service Provider Interface* (**SPI** ) for the`AlgorithmParameters`class, which is used to manage algorithm parameters. |
| [AllPermission](https://developer.android.com/reference/kotlin/java/security/AllPermission) | Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). |
| --- | --- |
| [AuthProvider](https://developer.android.com/reference/kotlin/java/security/AuthProvider) | Legacy security code; do not use. |
| [BasicPermission](https://developer.android.com/reference/kotlin/java/security/BasicPermission) | Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). |
| [CodeSigner](https://developer.android.com/reference/kotlin/java/security/CodeSigner) | This class encapsulates information about a code signer. |
| --- | --- |
| [CodeSource](https://developer.android.com/reference/kotlin/java/security/CodeSource) | Legacy security code; do not use. |
| [DigestInputStream](https://developer.android.com/reference/kotlin/java/security/DigestInputStream) | A transparent stream that updates the associated message digest using the bits going through the stream. |
| [DigestOutputStream](https://developer.android.com/reference/kotlin/java/security/DigestOutputStream) | A transparent stream that updates the associated message digest using the bits going through the stream. |
| --- | --- |
| [DomainLoadStoreParameter](https://developer.android.com/reference/kotlin/java/security/DomainLoadStoreParameter) | Configuration data that specifies the keystores in a keystore domain. |
| [DrbgParameters](https://developer.android.com/reference/kotlin/java/security/DrbgParameters) | This class specifies the parameters used by a DRBG (Deterministic Random Bit Generator). |
| [GuardedObject](https://developer.android.com/reference/kotlin/java/security/GuardedObject) | A GuardedObject is an object that is used to protect access to another object. |
| --- | --- |
| [Identity](https://developer.android.com/reference/kotlin/java/security/Identity) | This class represents identities: real-world objects such as people, companies or organizations whose identities can be authenticated using their public keys. |
| [IdentityScope](https://developer.android.com/reference/kotlin/java/security/IdentityScope) | This class represents a scope for identities. |
| [KeyFactory](https://developer.android.com/reference/kotlin/java/security/KeyFactory) | Key factories are used to convert*keys* (opaque cryptographic keys of type`Key`) into*key specifications*(transparent representations of the underlying key material), and vice versa. |
| --- | --- |
| [KeyFactorySpi](https://developer.android.com/reference/kotlin/java/security/KeyFactorySpi) | This class defines the*Service Provider Interface* (**SPI** ) for the`KeyFactory`class. |
| [KeyPair](https://developer.android.com/reference/kotlin/java/security/KeyPair) | This class is a simple holder for a key pair (a public key and a private key). |
| [KeyPairGenerator](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator) | The KeyPairGenerator class is used to generate pairs of public and private keys. |
| --- | --- |
| [KeyPairGeneratorSpi](https://developer.android.com/reference/kotlin/java/security/KeyPairGeneratorSpi) | This class defines the*Service Provider Interface* (**SPI** ) for the`KeyPairGenerator`class, which is used to generate pairs of public and private keys. |
| [KeyRep](https://developer.android.com/reference/kotlin/java/security/KeyRep) | Standardized representation for serialized Key objects. |
| [KeyStore](https://developer.android.com/reference/kotlin/java/security/KeyStore) | This class represents a storage facility for cryptographic keys and certificates. |
| --- | --- |
| [KeyStoreSpi](https://developer.android.com/reference/kotlin/java/security/KeyStoreSpi) | This class defines the*Service Provider Interface* (**SPI** ) for the`KeyStore`class. |
| [MessageDigest](https://developer.android.com/reference/kotlin/java/security/MessageDigest) | This MessageDigest class provides applications the functionality of a message digest algorithm, such as SHA-1 or SHA-256. |
| [MessageDigestSpi](https://developer.android.com/reference/kotlin/java/security/MessageDigestSpi) | This class defines the*Service Provider Interface* (**SPI** ) for the`MessageDigest`class, which provides the functionality of a message digest algorithm, such as MD5 or SHA. |
| --- | --- |
| [Permission](https://developer.android.com/reference/kotlin/java/security/Permission) | Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). |
| [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection) | Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). |
| [Permissions](https://developer.android.com/reference/kotlin/java/security/Permissions) | Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). |
| --- | --- |
| [PKCS12Attribute](https://developer.android.com/reference/kotlin/java/security/PKCS12Attribute) | An attribute associated with a PKCS12 keystore entry. |
| [Policy](https://developer.android.com/reference/kotlin/java/security/Policy) | Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). |
| [PolicySpi](https://developer.android.com/reference/kotlin/java/security/PolicySpi) | This class defines the*Service Provider Interface* (**SPI** ) for the`Policy`class. |
| --- | --- |
| [ProtectionDomain](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain) | Legacy security code; do not use. |
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider) | This class represents a "provider" for the Java Security API, where a provider implements some or all parts of Java Security. |
| [SecureClassLoader](https://developer.android.com/reference/kotlin/java/security/SecureClassLoader) | This class extends ClassLoader with additional support for defining classes with an associated code source and permissions which are retrieved by the system policy by default. |
| --- | --- |
| [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom) | This class provides a cryptographically strong random number generator (RNG). |
| [SecureRandomSpi](https://developer.android.com/reference/kotlin/java/security/SecureRandomSpi) | This class defines the*Service Provider Interface* (**SPI** ) for the [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom) class. |
| [Security](https://developer.android.com/reference/kotlin/java/security/Security) | This class centralizes all security properties and common security methods. |
| --- | --- |
| [SecurityPermission](https://developer.android.com/reference/kotlin/java/security/SecurityPermission) | Legacy security code; do not use. |
| [Signature](https://developer.android.com/reference/kotlin/java/security/Signature) | The Signature class is used to provide applications the functionality of a digital signature algorithm. |
| [SignatureSpi](https://developer.android.com/reference/kotlin/java/security/SignatureSpi) | This class defines the*Service Provider Interface* (**SPI** ) for the`Signature`class, which is used to provide the functionality of a digital signature algorithm. |
| --- | --- |
| [SignedObject](https://developer.android.com/reference/kotlin/java/security/SignedObject) | SignedObject is a class for the purpose of creating authentic runtime objects whose integrity cannot be compromised without being detected. |
| [Signer](https://developer.android.com/reference/kotlin/java/security/Signer) | This class is used to represent an Identity that can also digitally sign data. |
| [Timestamp](https://developer.android.com/reference/kotlin/java/security/Timestamp) | This class encapsulates information about a signed timestamp. |
| --- | --- |
| [UnresolvedPermission](https://developer.android.com/reference/kotlin/java/security/UnresolvedPermission) | Legacy security code; do not use. |

## Exceptions

| [AccessControlException](https://developer.android.com/reference/kotlin/java/security/AccessControlException) | This exception is thrown by the AccessController to indicate that a requested access (to a critical system resource such as the file system or the network) is denied. |
| --- | --- |
| [DigestException](https://developer.android.com/reference/kotlin/java/security/DigestException) | This is the generic Message Digest exception. |
| [GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException) | The`GeneralSecurityException`class is a generic security exception class that provides type safety for all the security-related exception classes that extend from it. |
| [InvalidAlgorithmParameterException](https://developer.android.com/reference/kotlin/java/security/InvalidAlgorithmParameterException) | This is the exception for invalid or inappropriate algorithm parameters. |
| --- | --- |
| [InvalidKeyException](https://developer.android.com/reference/kotlin/java/security/InvalidKeyException) | This is the exception for invalid Keys (invalid encoding, wrong length, uninitialized, etc). |
| [InvalidParameterException](https://developer.android.com/reference/kotlin/java/security/InvalidParameterException) | This exception, designed for use by the JCA/JCE engine classes, is thrown when an invalid parameter is passed to a method. |
| [KeyException](https://developer.android.com/reference/kotlin/java/security/KeyException) | This is the basic key exception. |
| --- | --- |
| [KeyManagementException](https://developer.android.com/reference/kotlin/java/security/KeyManagementException) | This is the general key management exception for all operations dealing with key management. |
| [KeyStoreException](https://developer.android.com/reference/kotlin/java/security/KeyStoreException) | This is the generic KeyStore exception. |
| [NoSuchAlgorithmException](https://developer.android.com/reference/kotlin/java/security/NoSuchAlgorithmException) | This exception is thrown when a particular cryptographic algorithm is requested but is not available in the environment. |
| --- | --- |
| [NoSuchProviderException](https://developer.android.com/reference/kotlin/java/security/NoSuchProviderException) | This exception is thrown when a particular security provider is requested but is not available in the environment. |
| [PrivilegedActionException](https://developer.android.com/reference/kotlin/java/security/PrivilegedActionException) | Legacy security code; do not use. |
| [ProviderException](https://developer.android.com/reference/kotlin/java/security/ProviderException) | A runtime exception for Provider exceptions (such as misconfiguration errors or unrecoverable internal errors), which may be subclassed by Providers to throw specialized, provider-specific runtime errors. |
| --- | --- |
| [SignatureException](https://developer.android.com/reference/kotlin/java/security/SignatureException) | This is the generic Signature exception. |
| [UnrecoverableEntryException](https://developer.android.com/reference/kotlin/java/security/UnrecoverableEntryException) | This exception is thrown if an entry in the keystore cannot be recovered. |
| [UnrecoverableKeyException](https://developer.android.com/reference/kotlin/java/security/UnrecoverableKeyException) | This exception is thrown if a key in the keystore cannot be recovered. |
| --- | --- |

## Enums

| [CryptoPrimitive](https://developer.android.com/reference/kotlin/java/security/CryptoPrimitive) | An enumeration of cryptographic primitives. |
| --- | --- |
