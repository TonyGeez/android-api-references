# NamedParameterSpec

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NamedParameterSpec

```
open class NamedParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.spec.NamedParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec#) |

| Known Direct Subclasses [ECGenParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/ECGenParameterSpec) |------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------| | [ECGenParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/ECGenParameterSpec) | This immutable class specifies the set of parameters used for generating elliptic curve (EC) domain parameters. | |

This class is used to specify any algorithm parameters that are determined by a standard name. This class also holds constants for standard parameter set names. The names of these constants exactly match the corresponding parameter set name. For example, NamedParameterSpec.X25519 represents the parameter set identified by the string "X25519". These strings are defined in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#parameterspec-names).

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NamedParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec#NamedParameterSpec(kotlin.String))`(`stdName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Creates a parameter specification using a standard (or predefined) name`stdName`. |

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec#getName())`()` Returns the standard name that determines the algorithm parameters. |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [NamedParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec#)! | [ED25519](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec#ED25519:java.security.spec.NamedParameterSpec) The Ed25519 parameters |
| static [NamedParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec#)! | [ED448](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec#ED448:java.security.spec.NamedParameterSpec) The Ed448 parameters |
| static [NamedParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec#)! | [X25519](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec#X25519:java.security.spec.NamedParameterSpec) The X25519 parameters |
| static [NamedParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec#)! | [X448](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec#X448:java.security.spec.NamedParameterSpec) The X448 parameters |

## Public constructors

### NamedParameterSpec

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NamedParameterSpec(stdName: String)
```

Creates a parameter specification using a standard (or predefined) name`stdName`. For the list of supported names, please consult the documentation of the provider whose implementation will be used.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stdName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the standard name of the algorithm parameters. See the ParameterSpec Names section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#parameterspec-names) for information about standard names. |

| Exceptions ||
|----------------------------------|---------------------|
| `java.lang.NullPointerException` | if`stdName`is null. |

## Public methods

### getName

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(): String
```

Returns the standard name that determines the algorithm parameters.

| Return ||
|----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the standard name. |

## Properties

### ED25519

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ED25519: NamedParameterSpec!
```

The Ed25519 parameters 

### ED448

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ED448: NamedParameterSpec!
```

The Ed448 parameters 

### X25519

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val X25519: NamedParameterSpec!
```

The X25519 parameters 

### X448

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val X448: NamedParameterSpec!
```

The X448 parameters
