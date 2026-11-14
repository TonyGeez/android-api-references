# MGF1ParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MGF1ParameterSpec

```
open class MGF1ParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.spec.MGF1ParameterSpec](MGF1ParameterSpec.md) |

This class specifies the set of parameters used with mask generation function MGF1 in OAEP Padding and RSASSA-PSS signature scheme, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard.

Its ASN.1 definition in PKCS#1 standard is described below: 

```kotlin
PKCS1MGFAlgorithms    ALGORITHM-IDENTIFIER ::= {
    { OID id-mgf1 PARAMETERS HashAlgorithm },
    ...  -- Allows for future expansion --
  }
  
```
where 

```kotlin
HashAlgorithm ::= AlgorithmIdentifier {
    {OAEP-PSSDigestAlgorithms}
  }
 
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
  
```

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MGF1ParameterSpec](MGF1ParameterSpec.md))`(`mdName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a parameter set for mask generation function MGF1 as defined in the PKCS #1 standard. |

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDigestAlgorithm](MGF1ParameterSpec.md))`()` Returns the algorithm name of the message digest used by the mask generation function. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](MGF1ParameterSpec.md))`()` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [MGF1ParameterSpec](MGF1ParameterSpec.md)! | [SHA1](MGF1ParameterSpec.md) The MGF1ParameterSpec which uses "SHA-1" message digest |
| static [MGF1ParameterSpec](MGF1ParameterSpec.md)! | [SHA224](MGF1ParameterSpec.md) The MGF1ParameterSpec which uses "SHA-224" message digest |
| static [MGF1ParameterSpec](MGF1ParameterSpec.md)! | [SHA256](MGF1ParameterSpec.md) The MGF1ParameterSpec which uses "SHA-256" message digest |
| --- | --- |
| static [MGF1ParameterSpec](MGF1ParameterSpec.md)! | [SHA384](MGF1ParameterSpec.md) The MGF1ParameterSpec which uses "SHA-384" message digest |
| static [MGF1ParameterSpec](MGF1ParameterSpec.md)! | [SHA3_224](MGF1ParameterSpec.md) The MGF1ParameterSpec which uses SHA3-224 message digest |
| static [MGF1ParameterSpec](MGF1ParameterSpec.md)! | [SHA3_256](MGF1ParameterSpec.md) The MGF1ParameterSpec which uses SHA3-256 message digest |
| --- | --- |
| static [MGF1ParameterSpec](MGF1ParameterSpec.md)! | [SHA3_384](MGF1ParameterSpec.md) The MGF1ParameterSpec which uses SHA3-384 message digest |
| static [MGF1ParameterSpec](MGF1ParameterSpec.md)! | [SHA3_512](MGF1ParameterSpec.md) The MGF1ParameterSpec which uses SHA3-512 message digest |
| static [MGF1ParameterSpec](MGF1ParameterSpec.md)! | [SHA512](MGF1ParameterSpec.md) The MGF1ParameterSpec which uses SHA-512 message digest |
| --- | --- |
| static [MGF1ParameterSpec](MGF1ParameterSpec.md)! | [SHA512_224](MGF1ParameterSpec.md) The MGF1ParameterSpec which uses SHA-512/224 message digest |
| static [MGF1ParameterSpec](MGF1ParameterSpec.md)! | [SHA512_256](MGF1ParameterSpec.md) The MGF1ParameterSpec which uses SHA-512/256 message digest |

## Public constructors

### MGF1ParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MGF1ParameterSpec(mdName: String!)
```

Constructs a parameter set for mask generation function MGF1 as defined in the PKCS #1 standard.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mdName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm name for the message digest used in this mask generation function MGF1. |

| Exceptions ||
|----------------------------------|--------------------|
| `java.lang.NullPointerException` | if`mdName`is null. |

## Public methods

### getDigestAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDigestAlgorithm(): String!
```

Returns the algorithm name of the message digest used by the mask generation function.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the algorithm name of the message digest. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Properties

### SHA1

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHA1: MGF1ParameterSpec!
```

The MGF1ParameterSpec which uses "SHA-1" message digest 

### SHA224

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHA224: MGF1ParameterSpec!
```

The MGF1ParameterSpec which uses "SHA-224" message digest 

### SHA256

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHA256: MGF1ParameterSpec!
```

The MGF1ParameterSpec which uses "SHA-256" message digest 

### SHA384

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHA384: MGF1ParameterSpec!
```

The MGF1ParameterSpec which uses "SHA-384" message digest 

### SHA3_224

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHA3_224: MGF1ParameterSpec!
```

The MGF1ParameterSpec which uses SHA3-224 message digest 

### SHA3_256

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHA3_256: MGF1ParameterSpec!
```

The MGF1ParameterSpec which uses SHA3-256 message digest 

### SHA3_384

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHA3_384: MGF1ParameterSpec!
```

The MGF1ParameterSpec which uses SHA3-384 message digest 

### SHA3_512

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHA3_512: MGF1ParameterSpec!
```

The MGF1ParameterSpec which uses SHA3-512 message digest 

### SHA512

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHA512: MGF1ParameterSpec!
```

The MGF1ParameterSpec which uses SHA-512 message digest 

### SHA512_224

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHA512_224: MGF1ParameterSpec!
```

The MGF1ParameterSpec which uses SHA-512/224 message digest 

### SHA512_256

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHA512_256: MGF1ParameterSpec!
```

The MGF1ParameterSpec which uses SHA-512/256 message digest
