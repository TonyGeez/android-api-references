# javax.crypto

# javax.crypto

## Interfaces

| [SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey) | A secret (symmetric) key. |
| --- | --- |

## Classes

| [Cipher](https://developer.android.com/reference/kotlin/javax/crypto/Cipher) | This class provides the functionality of a cryptographic cipher for encryption and decryption. |
| --- | --- |
| [CipherInputStream](https://developer.android.com/reference/kotlin/javax/crypto/CipherInputStream) | A CipherInputStream is composed of an InputStream and a Cipher so that read() methods return data that are read in from the underlying InputStream but have been additionally processed by the Cipher. |
| [CipherOutputStream](https://developer.android.com/reference/kotlin/javax/crypto/CipherOutputStream) | A CipherOutputStream is composed of an OutputStream and a Cipher so that write() methods first process the data before writing them out to the underlying OutputStream. |
| [CipherSpi](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi) | This class defines the*Service Provider Interface* (**SPI** ) for the`Cipher`class. |
| --- | --- |
| [EncryptedPrivateKeyInfo](https://developer.android.com/reference/kotlin/javax/crypto/EncryptedPrivateKeyInfo) | This class implements the`EncryptedPrivateKeyInfo`type as defined in PKCS #8. |
| [ExemptionMechanism](https://developer.android.com/reference/kotlin/javax/crypto/ExemptionMechanism) | This class provides the functionality of an exemption mechanism, examples of which are*key recovery* ,*key weakening* , and*key escrow*. |
| [ExemptionMechanismSpi](https://developer.android.com/reference/kotlin/javax/crypto/ExemptionMechanismSpi) | This class defines the*Service Provider Interface* (**SPI** ) for the`ExemptionMechanism`class. |
| --- | --- |
| [KeyAgreement](https://developer.android.com/reference/kotlin/javax/crypto/KeyAgreement) | This class provides the functionality of a key agreement (or key exchange) protocol. |
| [KeyAgreementSpi](https://developer.android.com/reference/kotlin/javax/crypto/KeyAgreementSpi) | This class defines the*Service Provider Interface* (**SPI** ) for the`KeyAgreement`class. |
| [KeyGenerator](https://developer.android.com/reference/kotlin/javax/crypto/KeyGenerator) | This class provides the functionality of a secret (symmetric) key generator. |
| --- | --- |
| [KeyGeneratorSpi](https://developer.android.com/reference/kotlin/javax/crypto/KeyGeneratorSpi) | This class defines the*Service Provider Interface* (**SPI** ) for the`KeyGenerator`class. |
| [Mac](https://developer.android.com/reference/kotlin/javax/crypto/Mac) | This class provides the functionality of a "Message Authentication Code" (MAC) algorithm. |
| [MacSpi](https://developer.android.com/reference/kotlin/javax/crypto/MacSpi) | This class defines the*Service Provider Interface* (**SPI** ) for the`Mac`class. |
| --- | --- |
| [NullCipher](https://developer.android.com/reference/kotlin/javax/crypto/NullCipher) | The NullCipher class is a class that provides an "identity cipher" -- one that does not transform the plain text. |
| [SealedObject](https://developer.android.com/reference/kotlin/javax/crypto/SealedObject) | This class enables a programmer to create an object and protect its confidentiality with a cryptographic algorithm. |
| [SecretKeyFactory](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactory) | This class represents a factory for secret keys. |
| --- | --- |
| [SecretKeyFactorySpi](https://developer.android.com/reference/kotlin/javax/crypto/SecretKeyFactorySpi) | This class defines the*Service Provider Interface* (**SPI** ) for the`SecretKeyFactory`class. |

## Exceptions

| [AEADBadTagException](https://developer.android.com/reference/kotlin/javax/crypto/AEADBadTagException) | This exception is thrown when a [Cipher](https://developer.android.com/reference/kotlin/javax/crypto/Cipher) operating in an AEAD mode (such as GCM/CCM) is unable to verify the supplied authentication tag. |
| --- | --- |
| [BadPaddingException](https://developer.android.com/reference/kotlin/javax/crypto/BadPaddingException) | This exception is thrown when a particular padding mechanism is expected for the input data but the data is not padded properly. |
| [ExemptionMechanismException](https://developer.android.com/reference/kotlin/javax/crypto/ExemptionMechanismException) | This is the generic ExemptionMechanism exception. |
| [IllegalBlockSizeException](https://developer.android.com/reference/kotlin/javax/crypto/IllegalBlockSizeException) | This exception is thrown when the length of data provided to a block cipher is incorrect, i. |
| --- | --- |
| [NoSuchPaddingException](https://developer.android.com/reference/kotlin/javax/crypto/NoSuchPaddingException) | This exception is thrown when a particular padding mechanism is requested but is not available in the environment. |
| [ShortBufferException](https://developer.android.com/reference/kotlin/javax/crypto/ShortBufferException) | This exception is thrown when an output buffer provided by the user is too short to hold the operation result. |
