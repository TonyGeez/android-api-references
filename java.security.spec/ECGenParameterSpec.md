Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ECGenParameterSpec

```
open class ECGenParameterSpec : NamedParameterSpec, AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.spec.NamedParameterSpec](NamedParameterSpec.md) ||
| | ↳ | [java.security.spec.ECGenParameterSpec](ECGenParameterSpec.md) |

This immutable class specifies the set of parameters used for generating elliptic curve (EC) domain parameters.

## Summary

| Public constructors ||
|---|---|
| ECGenParameterSpec Creates a parameter specification for EC parameter generation using a standard (or predefined) name `stdName` in order to generate the corresponding (precomputed) elliptic curve domain parameters. |

| Public methods ||
|---|---|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getName Returns the standard or predefined name of the to-be-generated EC domain parameters. |

| Inherited properties ||
|---|---|
| From class NamedParameterSpec |---|---| | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec!` | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec#ED25519:java.security.spec.NamedParameterSpec` The Ed25519 parameters <br /> | | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec!` | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec#ED448:java.security.spec.NamedParameterSpec` The Ed448 parameters <br /> | | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec!` | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec#ML_DSA_65:java.security.spec.NamedParameterSpec` The ML-DSA-65 parameters <br /> | | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec!` | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec#ML_DSA_87:java.security.spec.NamedParameterSpec` The ML-DSA-87 parameters <br /> | | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec!` | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec#X25519:java.security.spec.NamedParameterSpec` The X25519 parameters <br /> | | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec!` | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec#X448:java.security.spec.NamedParameterSpec` The X448 parameters <br /> | ||

## Public constructors

### ECGenParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ECGenParameterSpec(stdName: String!)
```

Creates a parameter specification for EC parameter generation using a standard (or predefined) name `stdName` in order to generate the corresponding (precomputed) elliptic curve domain parameters. For the list of supported names, please consult the documentation of the provider whose implementation will be used.

| Parameters ||
|---|---|
| `stdName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the standard name of the to-be-generated EC domain parameters. See the ParameterSpec Names section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#parameterspec-names) for information about standard names. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `stdName` is null. |

## Public methods

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getName(): String
```

Returns the standard or predefined name of the to-be-generated EC domain parameters.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the standard or predefined name. |
