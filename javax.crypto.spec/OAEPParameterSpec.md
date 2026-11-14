# OAEPParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OAEPParameterSpec

```
open class OAEPParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.spec.OAEPParameterSpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/OAEPParameterSpec#) |

This class specifies the set of parameters used with OAEP Padding, as defined in the [PKCS #1](http://www.ietf.org/rfc/rfc3447.txt) standard. Its ASN.1 definition in PKCS#1 standard is described below: 

```kotlin
RSAES-OAEP-params ::= SEQUENCE {
    hashAlgorithm      [0] OAEP-PSSDigestAlgorithms     DEFAULT sha1,
    maskGenAlgorithm   [1] PKCS1MGFAlgorithms  DEFAULT mgf1SHA1,
    pSourceAlgorithm   [2] PKCS1PSourceAlgorithms  DEFAULT pSpecifiedEmpty
  }
  
```
where 

```kotlin
OAEP-PSSDigestAlgorithms    ALGORITHM-IDENTIFIER ::= {
    { OID id-sha1 PARAMETERS NULL   }|
    { OID id-sha256 PARAMETERS NULL }|
    { OID id-sha384 PARAMETERS NULL }|
    { OID id-sha512 PARAMETERS NULL },
    ...  -- Allows for future expansion --
  }
  PKCS1MGFAlgorithms    ALGORITHM-IDENTIFIER ::= {
    { OID id-mgf1 PARAMETERS OAEP-PSSDigestAlgorithms },
    ...  -- Allows for future expansion --
  }
  PKCS1PSourceAlgorithms    ALGORITHM-IDENTIFIER ::= {
    { OID id-pSpecified PARAMETERS OCTET STRING },
    ...  -- Allows for future expansion --
  }
  
```

<br />

Note: the OAEPParameterSpec.DEFAULT uses the following: message digest -- "SHA-1" mask generation function (mgf) -- "MGF1" parameters for mgf -- MGF1ParameterSpec.SHA1 source of encoding input -- PSource.PSpecified.DEFAULT

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OAEPParameterSpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/OAEPParameterSpec#OAEPParameterSpec(kotlin.String,%20kotlin.String,%20java.security.spec.AlgorithmParameterSpec,%20javax.crypto.spec.PSource))`(`mdName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mgfName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mgfSpec:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)!`, `pSrc:` ` [PSource](https://developer.android.com/reference/kotlin/javax/crypto/spec/PSource)!`)` Constructs a parameter set for OAEP padding as defined in the PKCS #1 standard using the specified message digest algorithm`mdName`, mask generation function algorithm`mgfName`, parameters for the mask generation function`mgfSpec`, and source of the encoding input P`pSrc`. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDigestAlgorithm](https://developer.android.com/reference/kotlin/javax/crypto/spec/OAEPParameterSpec#getDigestAlgorithm())`()` Returns the message digest algorithm name. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMGFAlgorithm](https://developer.android.com/reference/kotlin/javax/crypto/spec/OAEPParameterSpec#getMGFAlgorithm())`()` Returns the mask generation function algorithm name. |
| open [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)! | [getMGFParameters](https://developer.android.com/reference/kotlin/javax/crypto/spec/OAEPParameterSpec#getMGFParameters())`()` Returns the parameters for the mask generation function. |
| --- | --- |
| open [PSource](https://developer.android.com/reference/kotlin/javax/crypto/spec/PSource)! | [getPSource](https://developer.android.com/reference/kotlin/javax/crypto/spec/OAEPParameterSpec#getPSource())`()` Returns the source of encoding input P. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [OAEPParameterSpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/OAEPParameterSpec#)! | [DEFAULT](https://developer.android.com/reference/kotlin/javax/crypto/spec/OAEPParameterSpec#DEFAULT:javax.crypto.spec.OAEPParameterSpec) The OAEP parameter set with all default values. |

## Public constructors

### OAEPParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OAEPParameterSpec(
    mdName: String!, 
    mgfName: String!, 
    mgfSpec: AlgorithmParameterSpec!, 
    pSrc: PSource!)
```

Constructs a parameter set for OAEP padding as defined in the PKCS #1 standard using the specified message digest algorithm`mdName`, mask generation function algorithm`mgfName`, parameters for the mask generation function`mgfSpec`, and source of the encoding input P`pSrc`.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mdName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm name for the message digest. |
| `mgfName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm name for the mask generation function. |
| `mgfSpec` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)!:the parameters for the mask generation function. If null is specified, null will be returned by getMGFParameters(). |
| --- | --- |
| `pSrc` | [PSource](https://developer.android.com/reference/kotlin/javax/crypto/spec/PSource)!:the source of the encoding input P. |

| Exceptions ||
|----------------------------------|----------------------------------------|
| `java.lang.NullPointerException` | if`mdName`,`mgfName`, or`pSrc`is null. |

## Public methods

### getDigestAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDigestAlgorithm(): String!
```

Returns the message digest algorithm name.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the message digest algorithm name. |

### getMGFAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMGFAlgorithm(): String!
```

Returns the mask generation function algorithm name.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the mask generation function algorithm name. |

### getMGFParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMGFParameters(): AlgorithmParameterSpec!
```

Returns the parameters for the mask generation function.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)! | the parameters for the mask generation function. |

### getPSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPSource(): PSource!
```

Returns the source of encoding input P.

| Return ||
|--------------------------------------------------------------------------------------|---------------------------------|
| [PSource](https://developer.android.com/reference/kotlin/javax/crypto/spec/PSource)! | the source of encoding input P. |

## Properties

### DEFAULT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT: OAEPParameterSpec!
```

The OAEP parameter set with all default values.
