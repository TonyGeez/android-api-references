# PSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PSource

```
open class PSource
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.spec.PSource](PSource.md) |

| Known Direct Subclasses [PSource.PSpecified](../javax/crypto/spec/PSource.PSpecified.md) |-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------| | [PSource.PSpecified](../javax/crypto/spec/PSource.PSpecified.md) | This class is used to explicitly specify the value for encoding input P in OAEP Padding. | |
| --- | --- | --- | --- | --- | --- | --- |

This class specifies the source for encoding input P in OAEP Padding, as defined in the [PKCS #1](http://www.ietf.org/rfc/rfc3447.txt) standard. 

```kotlin
PKCS1PSourceAlgorithms    ALGORITHM-IDENTIFIER ::= {
    { OID id-pSpecified PARAMETERS OCTET STRING },
    ...  -- Allows for future expansion --
  }
  
```

<br />

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [PSpecified](../javax/crypto/spec/PSource.PSpecified.md) This class is used to explicitly specify the value for encoding input P in OAEP Padding. |

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PSource](PSource.md))`(`pSrcName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a source of the encoding input P for OAEP padding as defined in the PKCS #1 standard using the specified PSource algorithm. |

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](PSource.md))`()` Returns the PSource algorithm name. |

## Protected constructors

### PSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected PSource(pSrcName: String!)
```

Constructs a source of the encoding input P for OAEP padding as defined in the PKCS #1 standard using the specified PSource algorithm.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `pSrcName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm for the source of the encoding input P. |

| Exceptions ||
|----------------------------------|----------------------|
| `java.lang.NullPointerException` | if`pSrcName`is null. |

## Public methods

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAlgorithm(): String!
```

Returns the PSource algorithm name.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the PSource algorithm name. |
