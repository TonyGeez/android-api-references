# java.security

# java.security

## Interfaces

| [AlgorithmConstraints](AlgorithmConstraints.md) | This interface specifies constraints for cryptographic algorithms, keys (key sizes), and other algorithm parameters. |
| --- | --- |
| [Certificate](Certificate.md) | This is an interface of abstract methods for managing a variety of identity certificates. |
| [DomainCombiner](DomainCombiner.md) | Legacy security code; do not use. |
| [Guard](Guard.md) | This interface represents a guard, which is an object that is used to protect access to another object. |
| --- | --- |
| [Key](Key.md) | The Key interface is the top-level interface for all keys. |
| [Entry](../java/security/KeyStore.Entry.md) | A marker interface for`KeyStore`entry types. |
| [LoadStoreParameter](../java/security/KeyStore.LoadStoreParameter.md) | A marker interface for`KeyStore` [load](KeyStore.md))and [store](KeyStore.md))parameters. |
| --- | --- |
| [ProtectionParameter](../java/security/KeyStore.ProtectionParameter.md) | A marker interface for keystore protection parameters. |
| [Parameters](../java/security/Policy.Parameters.md) | <br /> |
| [Principal](Principal.md) | This interface represents the abstract notion of a principal, which can be used to represent any entity, such as an individual, a corporation, and a login id. |
| --- | --- |
| [PrivateKey](PrivateKey.md) | A private key. |
| [PrivilegedAction](PrivilegedAction.md) | Android doesn't support [SecurityManager](../java.lang/SecurityManager.md). |
| [PrivilegedExceptionAction](PrivilegedExceptionAction.md) | Android doesn't support [SecurityManager](../java.lang/SecurityManager.md). |
| --- | --- |
| [PublicKey](PublicKey.md) | A public key. |
| [SecureRandomParameters](SecureRandomParameters.md) | A marker interface for parameters used in various`SecureRandom`methods. |

## Classes

| [AccessControlContext](AccessControlContext.md) | Android doesn't support [SecurityManager](../java.lang/SecurityManager.md). |
| --- | --- |
| [AccessController](AccessController.md) | Android doesn't support [SecurityManager](../java.lang/SecurityManager.md). |
| [AlgorithmParameterGenerator](AlgorithmParameterGenerator.md) | The`AlgorithmParameterGenerator`class is used to generate a set of parameters to be used with a certain algorithm. |
| [AlgorithmParameterGeneratorSpi](AlgorithmParameterGeneratorSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`AlgorithmParameterGenerator`class, which is used to generate a set of parameters to be used with a certain algorithm. |
| --- | --- |
| [AlgorithmParameters](AlgorithmParameters.md) | This class is used as an opaque representation of cryptographic parameters. |
| [AlgorithmParametersSpi](AlgorithmParametersSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`AlgorithmParameters`class, which is used to manage algorithm parameters. |
| [AllPermission](AllPermission.md) | Android doesn't support [SecurityManager](../java.lang/SecurityManager.md). |
| --- | --- |
| [AuthProvider](AuthProvider.md) | Legacy security code; do not use. |
| [BasicPermission](BasicPermission.md) | Android doesn't support [SecurityManager](../java.lang/SecurityManager.md). |
| [CodeSigner](CodeSigner.md) | This class encapsulates information about a code signer. |
| --- | --- |
| [CodeSource](CodeSource.md) | Legacy security code; do not use. |
| [DigestInputStream](DigestInputStream.md) | A transparent stream that updates the associated message digest using the bits going through the stream. |
| [DigestOutputStream](DigestOutputStream.md) | A transparent stream that updates the associated message digest using the bits going through the stream. |
| --- | --- |
| [DomainLoadStoreParameter](DomainLoadStoreParameter.md) | Configuration data that specifies the keystores in a keystore domain. |
| [DrbgParameters](DrbgParameters.md) | This class specifies the parameters used by a DRBG (Deterministic Random Bit Generator). |
| [GuardedObject](GuardedObject.md) | A GuardedObject is an object that is used to protect access to another object. |
| --- | --- |
| [Identity](Identity.md) | This class represents identities: real-world objects such as people, companies or organizations whose identities can be authenticated using their public keys. |
| [IdentityScope](IdentityScope.md) | This class represents a scope for identities. |
| [KeyFactory](KeyFactory.md) | Key factories are used to convert*keys* (opaque cryptographic keys of type`Key`) into*key specifications*(transparent representations of the underlying key material), and vice versa. |
| --- | --- |
| [KeyFactorySpi](KeyFactorySpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`KeyFactory`class. |
| [KeyPair](KeyPair.md) | This class is a simple holder for a key pair (a public key and a private key). |
| [KeyPairGenerator](KeyPairGenerator.md) | The KeyPairGenerator class is used to generate pairs of public and private keys. |
| --- | --- |
| [KeyPairGeneratorSpi](KeyPairGeneratorSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`KeyPairGenerator`class, which is used to generate pairs of public and private keys. |
| [KeyRep](KeyRep.md) | Standardized representation for serialized Key objects. |
| [KeyStore](KeyStore.md) | This class represents a storage facility for cryptographic keys and certificates. |
| --- | --- |
| [KeyStoreSpi](KeyStoreSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`KeyStore`class. |
| [MessageDigest](MessageDigest.md) | This MessageDigest class provides applications the functionality of a message digest algorithm, such as SHA-1 or SHA-256. |
| [MessageDigestSpi](MessageDigestSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`MessageDigest`class, which provides the functionality of a message digest algorithm, such as MD5 or SHA. |
| --- | --- |
| [Permission](Permission.md) | Android doesn't support [SecurityManager](../java.lang/SecurityManager.md). |
| [PermissionCollection](PermissionCollection.md) | Android doesn't support [SecurityManager](../java.lang/SecurityManager.md). |
| [Permissions](Permissions.md) | Android doesn't support [SecurityManager](../java.lang/SecurityManager.md). |
| --- | --- |
| [PKCS12Attribute](PKCS12Attribute.md) | An attribute associated with a PKCS12 keystore entry. |
| [Policy](Policy.md) | Android doesn't support [SecurityManager](../java.lang/SecurityManager.md). |
| [PolicySpi](PolicySpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`Policy`class. |
| --- | --- |
| [ProtectionDomain](ProtectionDomain.md) | Legacy security code; do not use. |
| [Provider](Provider.md) | This class represents a "provider" for the Java Security API, where a provider implements some or all parts of Java Security. |
| [SecureClassLoader](SecureClassLoader.md) | This class extends ClassLoader with additional support for defining classes with an associated code source and permissions which are retrieved by the system policy by default. |
| --- | --- |
| [SecureRandom](SecureRandom.md) | This class provides a cryptographically strong random number generator (RNG). |
| [SecureRandomSpi](SecureRandomSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the [SecureRandom](SecureRandom.md) class. |
| [Security](Security.md) | This class centralizes all security properties and common security methods. |
| --- | --- |
| [SecurityPermission](SecurityPermission.md) | Legacy security code; do not use. |
| [Signature](Signature.md) | The Signature class is used to provide applications the functionality of a digital signature algorithm. |
| [SignatureSpi](SignatureSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`Signature`class, which is used to provide the functionality of a digital signature algorithm. |
| --- | --- |
| [SignedObject](SignedObject.md) | SignedObject is a class for the purpose of creating authentic runtime objects whose integrity cannot be compromised without being detected. |
| [Signer](Signer.md) | This class is used to represent an Identity that can also digitally sign data. |
| [Timestamp](Timestamp.md) | This class encapsulates information about a signed timestamp. |
| --- | --- |
| [UnresolvedPermission](UnresolvedPermission.md) | Legacy security code; do not use. |

## Exceptions

| [AccessControlException](AccessControlException.md) | This exception is thrown by the AccessController to indicate that a requested access (to a critical system resource such as the file system or the network) is denied. |
| --- | --- |
| [DigestException](DigestException.md) | This is the generic Message Digest exception. |
| [GeneralSecurityException](GeneralSecurityException.md) | The`GeneralSecurityException`class is a generic security exception class that provides type safety for all the security-related exception classes that extend from it. |
| [InvalidAlgorithmParameterException](InvalidAlgorithmParameterException.md) | This is the exception for invalid or inappropriate algorithm parameters. |
| --- | --- |
| [InvalidKeyException](InvalidKeyException.md) | This is the exception for invalid Keys (invalid encoding, wrong length, uninitialized, etc). |
| [InvalidParameterException](InvalidParameterException.md) | This exception, designed for use by the JCA/JCE engine classes, is thrown when an invalid parameter is passed to a method. |
| [KeyException](KeyException.md) | This is the basic key exception. |
| --- | --- |
| [KeyManagementException](KeyManagementException.md) | This is the general key management exception for all operations dealing with key management. |
| [KeyStoreException](KeyStoreException.md) | This is the generic KeyStore exception. |
| [NoSuchAlgorithmException](NoSuchAlgorithmException.md) | This exception is thrown when a particular cryptographic algorithm is requested but is not available in the environment. |
| --- | --- |
| [NoSuchProviderException](NoSuchProviderException.md) | This exception is thrown when a particular security provider is requested but is not available in the environment. |
| [PrivilegedActionException](PrivilegedActionException.md) | Legacy security code; do not use. |
| [ProviderException](ProviderException.md) | A runtime exception for Provider exceptions (such as misconfiguration errors or unrecoverable internal errors), which may be subclassed by Providers to throw specialized, provider-specific runtime errors. |
| --- | --- |
| [SignatureException](SignatureException.md) | This is the generic Signature exception. |
| [UnrecoverableEntryException](UnrecoverableEntryException.md) | This exception is thrown if an entry in the keystore cannot be recovered. |
| [UnrecoverableKeyException](UnrecoverableKeyException.md) | This exception is thrown if a key in the keystore cannot be recovered. |
| --- | --- |

## Enums

| [CryptoPrimitive](CryptoPrimitive.md) | An enumeration of cryptographic primitives. |
| --- | --- |
