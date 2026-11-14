# PBEKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PBEKeySpec

```
open class PBEKeySpec : KeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.spec.PBEKeySpec](../javax/crypto/spec/PBEKeySpec.md) |

A user-chosen password that can be used with password-based encryption (*PBE*).

The password can be viewed as some kind of raw key material, from which the encryption mechanism that uses it derives a cryptographic key.

Different PBE mechanisms may consume different bits of each password character. For example, the PBE mechanism defined in [PKCS #5](http://www.ietf.org/rfc/rfc2898.txt) looks at only the low order 8 bits of each character, whereas PKCS #12 looks at all 16 bits of each character.

You convert the password characters to a PBE key by creating an instance of the appropriate secret-key factory. For example, a secret-key factory for PKCS #5 will construct a PBE key from only the low order 8 bits of each password character, whereas a secret-key factory for PKCS #12 will take all 16 bits of each character.

Also note that this class stores passwords as char arrays instead of`String`objects (which would seem more logical), because the String class is immutable and there is no way to overwrite its internal value when the password stored in it is no longer needed. Hence, this class requests the password as a char array, so it can be overwritten when done.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PBEKeySpec](../javax/crypto/spec/PBEKeySpec.md))`(`password:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Constructor that takes a password. |
| [PBEKeySpec](../javax/crypto/spec/PBEKeySpec.md))`(`password:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `salt:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `iterationCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor that takes a password, salt, iteration count for generating PBEKey of fixed-key-size PBE ciphers. |
| [PBEKeySpec](../javax/crypto/spec/PBEKeySpec.md))`(`password:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `salt:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `iterationCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `keyLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor that takes a password, salt, iteration count, and to-be-derived key length for generating PBEKey of variable-key-size PBE ciphers. |

| Public methods ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearPassword](../javax/crypto/spec/PBEKeySpec.md))`()` Clears the internal copy of the password. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIterationCount](../javax/crypto/spec/PBEKeySpec.md))`()` Returns the iteration count or 0 if not specified. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getKeyLength](../javax/crypto/spec/PBEKeySpec.md))`()` Returns the to-be-derived key length or 0 if not specified. |
| --- | --- |
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [getPassword](../javax/crypto/spec/PBEKeySpec.md))`()` Returns a copy of the password. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getSalt](../javax/crypto/spec/PBEKeySpec.md))`()` Returns a copy of the salt or null if not specified. |

## Public constructors

### PBEKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PBEKeySpec(password: CharArray!)
```

Constructor that takes a password. An empty char\[\] is used if null is specified.

Note:`password`is cloned before it is stored in the new`PBEKeySpec`object.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------|
| `password` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the password. |

### PBEKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PBEKeySpec(
    password: CharArray!, 
    salt: ByteArray!, 
    iterationCount: Int)
```

Constructor that takes a password, salt, iteration count for generating PBEKey of fixed-key-size PBE ciphers. An empty char\[\] is used if null is specified for`password`.

Note: the`password`and`salt`are cloned before they are stored in the new`PBEKeySpec`object.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------|
| `password` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the password. |
| `salt` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the salt. |
| `iterationCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the iteration count. |
| --- | --- |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`salt`is null. |
| `java.lang.IllegalArgumentException` | if`salt`is empty, i.e. 0-length, or`iterationCount`is not positive. |

### PBEKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PBEKeySpec(
    password: CharArray!, 
    salt: ByteArray!, 
    iterationCount: Int, 
    keyLength: Int)
```

Constructor that takes a password, salt, iteration count, and to-be-derived key length for generating PBEKey of variable-key-size PBE ciphers. An empty char\[\] is used if null is specified for`password`.

Note: the`password`and`salt`are cloned before they are stored in the new`PBEKeySpec`object.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------|
| `password` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the password. |
| `salt` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the salt. |
| `iterationCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the iteration count. |
| --- | --- |
| `keyLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the to-be-derived key length. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`salt`is null. |
| `java.lang.IllegalArgumentException` | if`salt`is empty, i.e. 0-length,`iterationCount`or`keyLength`is not positive. |

## Public methods

### clearPassword

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clearPassword(): Unit
```

Clears the internal copy of the password. 

### getIterationCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIterationCount(): Int
```

Returns the iteration count or 0 if not specified.

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the iteration count. |

### getKeyLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKeyLength(): Int
```

Returns the to-be-derived key length or 0 if not specified.

Note: this is used to indicate the preference on key length for variable-key-size ciphers. The actual key size depends on each provider's implementation.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the to-be-derived key length. |

### getPassword

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPassword(): CharArray!
```

Returns a copy of the password.

Note: this method returns a copy of the password. It is the caller's responsibility to zero out the password information after it is no longer needed.

| Return ||
|------------------------------------------------------------------------------------------|---------------|
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | the password. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------|
| `java.lang.IllegalStateException` | if password has been cleared by calling`clearPassword`method. |

### getSalt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSalt(): ByteArray!
```

Returns a copy of the salt or null if not specified.

Note: this method should return a copy of the salt. It is the caller's responsibility to zero out the salt information after it is no longer needed.

| Return ||
|------------------------------------------------------------------------------------------|-----------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the salt. |
