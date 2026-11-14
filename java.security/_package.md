# java.security

# java.security

## Interfaces

| [AlgorithmConstraints](../java/security/AlgorithmConstraints.md) | This interface specifies constraints for cryptographic algorithms, keys (key sizes), and other algorithm parameters. |
| --- | --- |
| [Certificate](../java/security/Certificate.md) | This is an interface of abstract methods for managing a variety of identity certificates. |
| [DomainCombiner](../java/security/DomainCombiner.md) | Legacy security code; do not use. |
| [Guard](../java/security/Guard.md) | This interface represents a guard, which is an object that is used to protect access to another object. |
| --- | --- |
| [Key](../java/security/Key.md) | The Key interface is the top-level interface for all keys. |
| [Entry](../java/security/KeyStore.Entry.md) | A marker interface for`KeyStore`entry types. |
| [LoadStoreParameter](../java/security/KeyStore.LoadStoreParameter.md) | A marker interface for`KeyStore` [load](../java/security/KeyStore.md))and [store](../java/security/KeyStore.md))parameters. |
| --- | --- |
| [ProtectionParameter](../java/security/KeyStore.ProtectionParameter.md) | A marker interface for keystore protection parameters. |
| [Parameters](../java/security/Policy.Parameters.md) | <br /> |
| [Principal](../java/security/Principal.md) | This interface represents the abstract notion of a principal, which can be used to represent any entity, such as an individual, a corporation, and a login id. |
| --- | --- |
| [PrivateKey](../java/security/PrivateKey.md) | A private key. |
| [PrivilegedAction](../java/security/PrivilegedAction.md) | Android doesn't support [SecurityManager](../java/lang/SecurityManager.md). |
| [PrivilegedExceptionAction](../java/security/PrivilegedExceptionAction.md) | Android doesn't support [SecurityManager](../java/lang/SecurityManager.md). |
| --- | --- |
| [PublicKey](../java/security/PublicKey.md) | A public key. |
| [SecureRandomParameters](../java/security/SecureRandomParameters.md) | A marker interface for parameters used in various`SecureRandom`methods. |

## Classes

| [AccessControlContext](../java/security/AccessControlContext.md) | Android doesn't support [SecurityManager](../java/lang/SecurityManager.md). |
| --- | --- |
| [AccessController](../java/security/AccessController.md) | Android doesn't support [SecurityManager](../java/lang/SecurityManager.md). |
| [AlgorithmParameterGenerator](../java/security/AlgorithmParameterGenerator.md) | The`AlgorithmParameterGenerator`class is used to generate a set of parameters to be used with a certain algorithm. |
| [AlgorithmParameterGeneratorSpi](../java/security/AlgorithmParameterGeneratorSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`AlgorithmParameterGenerator`class, which is used to generate a set of parameters to be used with a certain algorithm. |
| --- | --- |
| [AlgorithmParameters](../java/security/AlgorithmParameters.md) | This class is used as an opaque representation of cryptographic parameters. |
| [AlgorithmParametersSpi](../java/security/AlgorithmParametersSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`AlgorithmParameters`class, which is used to manage algorithm parameters. |
| [AllPermission](../java/security/AllPermission.md) | Android doesn't support [SecurityManager](../java/lang/SecurityManager.md). |
| --- | --- |
| [AuthProvider](../java/security/AuthProvider.md) | Legacy security code; do not use. |
| [BasicPermission](../java/security/BasicPermission.md) | Android doesn't support [SecurityManager](../java/lang/SecurityManager.md). |
| [CodeSigner](../java/security/CodeSigner.md) | This class encapsulates information about a code signer. |
| --- | --- |
| [CodeSource](../java/security/CodeSource.md) | Legacy security code; do not use. |
| [DigestInputStream](../java/security/DigestInputStream.md) | A transparent stream that updates the associated message digest using the bits going through the stream. |
| [DigestOutputStream](../java/security/DigestOutputStream.md) | A transparent stream that updates the associated message digest using the bits going through the stream. |
| --- | --- |
| [DomainLoadStoreParameter](../java/security/DomainLoadStoreParameter.md) | Configuration data that specifies the keystores in a keystore domain. |
| [DrbgParameters](../java/security/DrbgParameters.md) | This class specifies the parameters used by a DRBG (Deterministic Random Bit Generator). |
| [GuardedObject](../java/security/GuardedObject.md) | A GuardedObject is an object that is used to protect access to another object. |
| --- | --- |
| [Identity](../java/security/Identity.md) | This class represents identities: real-world objects such as people, companies or organizations whose identities can be authenticated using their public keys. |
| [IdentityScope](../java/security/IdentityScope.md) | This class represents a scope for identities. |
| [KeyFactory](../java/security/KeyFactory.md) | Key factories are used to convert*keys* (opaque cryptographic keys of type`Key`) into*key specifications*(transparent representations of the underlying key material), and vice versa. |
| --- | --- |
| [KeyFactorySpi](../java/security/KeyFactorySpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`KeyFactory`class. |
| [KeyPair](../java/security/KeyPair.md) | This class is a simple holder for a key pair (a public key and a private key). |
| [KeyPairGenerator](../java/security/KeyPairGenerator.md) | The KeyPairGenerator class is used to generate pairs of public and private keys. |
| --- | --- |
| [KeyPairGeneratorSpi](../java/security/KeyPairGeneratorSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`KeyPairGenerator`class, which is used to generate pairs of public and private keys. |
| [KeyRep](../java/security/KeyRep.md) | Standardized representation for serialized Key objects. |
| [KeyStore](../java/security/KeyStore.md) | This class represents a storage facility for cryptographic keys and certificates. |
| --- | --- |
| [KeyStoreSpi](../java/security/KeyStoreSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`KeyStore`class. |
| [MessageDigest](../java/security/MessageDigest.md) | This MessageDigest class provides applications the functionality of a message digest algorithm, such as SHA-1 or SHA-256. |
| [MessageDigestSpi](../java/security/MessageDigestSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`MessageDigest`class, which provides the functionality of a message digest algorithm, such as MD5 or SHA. |
| --- | --- |
| [Permission](../java/security/Permission.md) | Android doesn't support [SecurityManager](../java/lang/SecurityManager.md). |
| [PermissionCollection](../java/security/PermissionCollection.md) | Android doesn't support [SecurityManager](../java/lang/SecurityManager.md). |
| [Permissions](../java/security/Permissions.md) | Android doesn't support [SecurityManager](../java/lang/SecurityManager.md). |
| --- | --- |
| [PKCS12Attribute](../java/security/PKCS12Attribute.md) | An attribute associated with a PKCS12 keystore entry. |
| [Policy](../java/security/Policy.md) | Android doesn't support [SecurityManager](../java/lang/SecurityManager.md). |
| [PolicySpi](../java/security/PolicySpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`Policy`class. |
| --- | --- |
| [ProtectionDomain](../java/security/ProtectionDomain.md) | Legacy security code; do not use. |
| [Provider](../java/security/Provider.md) | This class represents a "provider" for the Java Security API, where a provider implements some or all parts of Java Security. |
| [SecureClassLoader](../java/security/SecureClassLoader.md) | This class extends ClassLoader with additional support for defining classes with an associated code source and permissions which are retrieved by the system policy by default. |
| --- | --- |
| [SecureRandom](../java/security/SecureRandom.md) | This class provides a cryptographically strong random number generator (RNG). |
| [SecureRandomSpi](../java/security/SecureRandomSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the [SecureRandom](../java/security/SecureRandom.md) class. |
| [Security](../java/security/Security.md) | This class centralizes all security properties and common security methods. |
| --- | --- |
| [SecurityPermission](../java/security/SecurityPermission.md) | Legacy security code; do not use. |
| [Signature](../java/security/Signature.md) | The Signature class is used to provide applications the functionality of a digital signature algorithm. |
| [SignatureSpi](../java/security/SignatureSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`Signature`class, which is used to provide the functionality of a digital signature algorithm. |
| --- | --- |
| [SignedObject](../java/security/SignedObject.md) | SignedObject is a class for the purpose of creating authentic runtime objects whose integrity cannot be compromised without being detected. |
| [Signer](../java/security/Signer.md) | This class is used to represent an Identity that can also digitally sign data. |
| [Timestamp](../java/security/Timestamp.md) | This class encapsulates information about a signed timestamp. |
| --- | --- |
| [UnresolvedPermission](../java/security/UnresolvedPermission.md) | Legacy security code; do not use. |

## Exceptions

| [AccessControlException](../java/security/AccessControlException.md) | This exception is thrown by the AccessController to indicate that a requested access (to a critical system resource such as the file system or the network) is denied. |
| --- | --- |
| [DigestException](../java/security/DigestException.md) | This is the generic Message Digest exception. |
| [GeneralSecurityException](../java/security/GeneralSecurityException.md) | The`GeneralSecurityException`class is a generic security exception class that provides type safety for all the security-related exception classes that extend from it. |
| [InvalidAlgorithmParameterException](../java/security/InvalidAlgorithmParameterException.md) | This is the exception for invalid or inappropriate algorithm parameters. |
| --- | --- |
| [InvalidKeyException](../java/security/InvalidKeyException.md) | This is the exception for invalid Keys (invalid encoding, wrong length, uninitialized, etc). |
| [InvalidParameterException](../java/security/InvalidParameterException.md) | This exception, designed for use by the JCA/JCE engine classes, is thrown when an invalid parameter is passed to a method. |
| [KeyException](../java/security/KeyException.md) | This is the basic key exception. |
| --- | --- |
| [KeyManagementException](../java/security/KeyManagementException.md) | This is the general key management exception for all operations dealing with key management. |
| [KeyStoreException](../java/security/KeyStoreException.md) | This is the generic KeyStore exception. |
| [NoSuchAlgorithmException](../java/security/NoSuchAlgorithmException.md) | This exception is thrown when a particular cryptographic algorithm is requested but is not available in the environment. |
| --- | --- |
| [NoSuchProviderException](../java/security/NoSuchProviderException.md) | This exception is thrown when a particular security provider is requested but is not available in the environment. |
| [PrivilegedActionException](../java/security/PrivilegedActionException.md) | Legacy security code; do not use. |
| [ProviderException](../java/security/ProviderException.md) | A runtime exception for Provider exceptions (such as misconfiguration errors or unrecoverable internal errors), which may be subclassed by Providers to throw specialized, provider-specific runtime errors. |
| --- | --- |
| [SignatureException](../java/security/SignatureException.md) | This is the generic Signature exception. |
| [UnrecoverableEntryException](../java/security/UnrecoverableEntryException.md) | This exception is thrown if an entry in the keystore cannot be recovered. |
| [UnrecoverableKeyException](../java/security/UnrecoverableKeyException.md) | This exception is thrown if a key in the keystore cannot be recovered. |
| --- | --- |

## Enums

| [CryptoPrimitive](../java/security/CryptoPrimitive.md) | An enumeration of cryptographic primitives. |
| --- | --- |
