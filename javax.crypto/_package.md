# javax.crypto

# javax.crypto

## Interfaces

| [SecretKey](SecretKey.md) | A secret (symmetric) key. |
| --- | --- |

## Classes

| [Cipher](Cipher.md) | This class provides the functionality of a cryptographic cipher for encryption and decryption. |
| --- | --- |
| [CipherInputStream](CipherInputStream.md) | A CipherInputStream is composed of an InputStream and a Cipher so that read() methods return data that are read in from the underlying InputStream but have been additionally processed by the Cipher. |
| [CipherOutputStream](CipherOutputStream.md) | A CipherOutputStream is composed of an OutputStream and a Cipher so that write() methods first process the data before writing them out to the underlying OutputStream. |
| [CipherSpi](CipherSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`Cipher`class. |
| --- | --- |
| [EncryptedPrivateKeyInfo](EncryptedPrivateKeyInfo.md) | This class implements the`EncryptedPrivateKeyInfo`type as defined in PKCS #8. |
| [ExemptionMechanism](ExemptionMechanism.md) | This class provides the functionality of an exemption mechanism, examples of which are*key recovery* ,*key weakening* , and*key escrow*. |
| [ExemptionMechanismSpi](ExemptionMechanismSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`ExemptionMechanism`class. |
| --- | --- |
| [KeyAgreement](KeyAgreement.md) | This class provides the functionality of a key agreement (or key exchange) protocol. |
| [KeyAgreementSpi](KeyAgreementSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`KeyAgreement`class. |
| [KeyGenerator](KeyGenerator.md) | This class provides the functionality of a secret (symmetric) key generator. |
| --- | --- |
| [KeyGeneratorSpi](KeyGeneratorSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`KeyGenerator`class. |
| [Mac](Mac.md) | This class provides the functionality of a "Message Authentication Code" (MAC) algorithm. |
| [MacSpi](MacSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`Mac`class. |
| --- | --- |
| [NullCipher](NullCipher.md) | The NullCipher class is a class that provides an "identity cipher" -- one that does not transform the plain text. |
| [SealedObject](SealedObject.md) | This class enables a programmer to create an object and protect its confidentiality with a cryptographic algorithm. |
| [SecretKeyFactory](SecretKeyFactory.md) | This class represents a factory for secret keys. |
| --- | --- |
| [SecretKeyFactorySpi](SecretKeyFactorySpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`SecretKeyFactory`class. |

## Exceptions

| [AEADBadTagException](AEADBadTagException.md) | This exception is thrown when a [Cipher](Cipher.md) operating in an AEAD mode (such as GCM/CCM) is unable to verify the supplied authentication tag. |
| --- | --- |
| [BadPaddingException](BadPaddingException.md) | This exception is thrown when a particular padding mechanism is expected for the input data but the data is not padded properly. |
| [ExemptionMechanismException](ExemptionMechanismException.md) | This is the generic ExemptionMechanism exception. |
| [IllegalBlockSizeException](IllegalBlockSizeException.md) | This exception is thrown when the length of data provided to a block cipher is incorrect, i. |
| --- | --- |
| [NoSuchPaddingException](NoSuchPaddingException.md) | This exception is thrown when a particular padding mechanism is requested but is not available in the environment. |
| [ShortBufferException](ShortBufferException.md) | This exception is thrown when an output buffer provided by the user is too short to hold the operation result. |
