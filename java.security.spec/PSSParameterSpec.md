# PSSParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PSSParameterSpec

```
open class PSSParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.PSSParameterSpec](../java/security/spec/PSSParameterSpec.md) |

This class specifies a parameter spec for RSASSA-PSS signature scheme, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard.

Its ASN.1 definition in PKCS#1 standard is described below: 

```kotlin
RSASSA-PSS-params ::= SEQUENCE {
    hashAlgorithm      [0] HashAlgorithm      DEFAULT sha1,
    maskGenAlgorithm   [1] MaskGenAlgorithm   DEFAULT mgf1SHA1,
    saltLength         [2] INTEGER            DEFAULT 20,
    trailerField       [3] TrailerField       DEFAULT trailerFieldBC(1)
  }
  
```
where 

```kotlin
HashAlgorithm ::= AlgorithmIdentifier {
    {OAEP-PSSDigestAlgorithms}
  }
  MaskGenAlgorithm ::= AlgorithmIdentifier { {PKCS1MGFAlgorithms} }
  TrailerField ::= INTEGER { trailerFieldBC(1) }
 
  OAEP-PSSDigestAlgorithms    ALGORITHM-IDENTIFIER ::= {
    { OID id-sha1       PARAMETERS NULL }|
    { OID id-sha224     PARAMETERS NULL }|
    { OID id-sha256     PARAMETERS NULL }|
    { OID id-sha384     PARAMETERS NULL }|
    { OID id-sha512     PARAMETERS NULL }|
    { OID id-sha512-224 PARAMETERS NULL }|
    { OID id-sha512-256 PARAMETERS NULL },
    ...  -- Allows for future expansion --
  }
  PKCS1MGFAlgorithms    ALGORITHM-IDENTIFIER ::= {
    { OID id-mgf1 PARAMETERS HashAlgorithm },
    ...  -- Allows for future expansion --
  }
  
```

Note: the PSSParameterSpec.DEFAULT uses the following: message digest -- "SHA-1" mask generation function (mgf) -- "MGF1" parameters for mgf -- MGF1ParameterSpec.SHA1 SaltLength -- 20 TrailerField -- 1

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRAILER_FIELD_BC](../java/security/spec/PSSParameterSpec.md) The`TrailerFieldBC`constant as defined in PKCS#1 |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PSSParameterSpec](../java/security/spec/PSSParameterSpec.md))`(`saltLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new`PSSParameterSpec`using the specified salt length and other default values as defined in PKCS#1. |
| [PSSParameterSpec](../java/security/spec/PSSParameterSpec.md))`(`mdName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mgfName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mgfSpec:` ` [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!`, `saltLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `trailerField:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new`PSSParameterSpec`as defined in the PKCS #1 standard using the specified message digest, mask generation function, parameters for mask generation function, salt length, and trailer field values. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDigestAlgorithm](../java/security/spec/PSSParameterSpec.md))`()` Returns the message digest algorithm name. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMGFAlgorithm](../java/security/spec/PSSParameterSpec.md))`()` Returns the mask generation function algorithm name. |
| open [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)! | [getMGFParameters](../java/security/spec/PSSParameterSpec.md))`()` Returns the parameters for the mask generation function. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSaltLength](../java/security/spec/PSSParameterSpec.md))`()` Returns the salt length in bytes. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTrailerField](../java/security/spec/PSSParameterSpec.md))`()` Returns the value for the trailer field. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/security/spec/PSSParameterSpec.md))`()` <br /> |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [PSSParameterSpec](../java/security/spec/PSSParameterSpec.md)! | [DEFAULT](../java/security/spec/PSSParameterSpec.md) The PSS parameter set with all default values |

## Constants

### TRAILER_FIELD_BC

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRAILER_FIELD_BC: Int
```

The`TrailerFieldBC`constant as defined in PKCS#1 

 Value: 1

## Public constructors

### PSSParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PSSParameterSpec(saltLen: Int)
```

Creates a new`PSSParameterSpec`using the specified salt length and other default values as defined in PKCS#1.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `saltLen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length of salt in bytes to be used in PKCS#1 PSS encoding |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if`saltLen`is less than 0 |

### PSSParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PSSParameterSpec(
    mdName: String!, 
    mgfName: String!, 
    mgfSpec: AlgorithmParameterSpec!, 
    saltLen: Int, 
    trailerField: Int)
```

Creates a new`PSSParameterSpec`as defined in the PKCS #1 standard using the specified message digest, mask generation function, parameters for mask generation function, salt length, and trailer field values.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mdName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm name of the hash function |
| `mgfName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm name of the mask generation function |
| `mgfSpec` | [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!:the parameters for the mask generation function. If null is specified, null will be returned by getMGFParameters(). |
| --- | --- |
| `saltLen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length of salt |
| `trailerField` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value of the trailer field |

| Exceptions ||
|--------------------------------------|-------------------------------------------|
| `java.lang.NullPointerException` | if`mdName`, or`mgfName`is null |
| `java.lang.IllegalArgumentException` | if`saltLen`or`trailerField`is less than 0 |

## Public methods

### getDigestAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDigestAlgorithm(): String!
```

Returns the message digest algorithm name.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the message digest algorithm name |

### getMGFAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMGFAlgorithm(): String!
```

Returns the mask generation function algorithm name.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the mask generation function algorithm name |

### getMGFParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMGFParameters(): AlgorithmParameterSpec!
```

Returns the parameters for the mask generation function.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)! | the parameters for the mask generation function |

### getSaltLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSaltLength(): Int
```

Returns the salt length in bytes.

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the salt length |

### getTrailerField

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTrailerField(): Int
```

Returns the value for the trailer field.

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value for the trailer field |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Properties

### DEFAULT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT: PSSParameterSpec!
```

The PSS parameter set with all default values
