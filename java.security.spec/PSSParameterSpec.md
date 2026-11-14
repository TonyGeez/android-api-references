# PSSParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PSSParameterSpec

```
open class PSSParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.spec.PSSParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/PSSParameterSpec#) |

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
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRAILER_FIELD_BC](https://developer.android.com/reference/kotlin/java/security/spec/PSSParameterSpec#TRAILER_FIELD_BC:kotlin.Int) The`TrailerFieldBC`constant as defined in PKCS#1 |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PSSParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/PSSParameterSpec#PSSParameterSpec(kotlin.Int))`(`saltLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new`PSSParameterSpec`using the specified salt length and other default values as defined in PKCS#1. |
| [PSSParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/PSSParameterSpec#PSSParameterSpec(kotlin.String,%20kotlin.String,%20java.security.spec.AlgorithmParameterSpec,%20kotlin.Int,%20kotlin.Int))`(`mdName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mgfName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mgfSpec:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!`, `saltLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `trailerField:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new`PSSParameterSpec`as defined in the PKCS #1 standard using the specified message digest, mask generation function, parameters for mask generation function, salt length, and trailer field values. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDigestAlgorithm](https://developer.android.com/reference/kotlin/java/security/spec/PSSParameterSpec#getDigestAlgorithm())`()` Returns the message digest algorithm name. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMGFAlgorithm](https://developer.android.com/reference/kotlin/java/security/spec/PSSParameterSpec#getMGFAlgorithm())`()` Returns the mask generation function algorithm name. |
| open [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)! | [getMGFParameters](https://developer.android.com/reference/kotlin/java/security/spec/PSSParameterSpec#getMGFParameters())`()` Returns the parameters for the mask generation function. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSaltLength](https://developer.android.com/reference/kotlin/java/security/spec/PSSParameterSpec#getSaltLength())`()` Returns the salt length in bytes. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTrailerField](https://developer.android.com/reference/kotlin/java/security/spec/PSSParameterSpec#getTrailerField())`()` Returns the value for the trailer field. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/security/spec/PSSParameterSpec#toString())`()` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [PSSParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/PSSParameterSpec#)! | [DEFAULT](https://developer.android.com/reference/kotlin/java/security/spec/PSSParameterSpec#DEFAULT:java.security.spec.PSSParameterSpec) The PSS parameter set with all default values |

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
| `mgfSpec` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!:the parameters for the mask generation function. If null is specified, null will be returned by getMGFParameters(). |
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
| [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)! | the parameters for the mask generation function |

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
