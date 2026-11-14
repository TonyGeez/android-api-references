# AlgorithmConstraints

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AlgorithmConstraints

```
interface AlgorithmConstraints
```

| [java.security.AlgorithmConstraints](AlgorithmConstraints.md) |

This interface specifies constraints for cryptographic algorithms, keys (key sizes), and other algorithm parameters.

`AlgorithmConstraints`objects are immutable. An implementation of this interface should not provide methods that can change the state of an instance once it has been created.

Note that`AlgorithmConstraints`can be used to represent the restrictions described by the security properties`jdk.certpath.disabledAlgorithms`and`jdk.tls.disabledAlgorithms`, or could be used by a concrete`PKIXCertPathChecker`to check whether a specified certificate in the certification path contains the required algorithm constraints.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [permits](AlgorithmConstraints.md))`(`primitives:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [CryptoPrimitive](CryptoPrimitive.md)!>!`, `algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `parameters:` ` [AlgorithmParameters](AlgorithmParameters.md)!`)` Determines whether an algorithm is granted permission for the specified cryptographic primitives. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [permits](AlgorithmConstraints.md))`(`primitives:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [CryptoPrimitive](CryptoPrimitive.md)!>!`, `algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `key:` ` [Key](Key.md)!`, `parameters:` ` [AlgorithmParameters](AlgorithmParameters.md)!`)` Determines whether an algorithm and the corresponding key are granted permission for the specified cryptographic primitives. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [permits](AlgorithmConstraints.md))`(`primitives:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [CryptoPrimitive](CryptoPrimitive.md)!>!`, `key:` ` [Key](Key.md)!`)` Determines whether a key is granted permission for the specified cryptographic primitives. |
| --- | --- |

## Public methods

### permits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun permits(
    primitives: MutableSet<CryptoPrimitive!>!, 
    algorithm: String!, 
    parameters: AlgorithmParameters!
): Boolean
```

Determines whether an algorithm is granted permission for the specified cryptographic primitives.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `primitives` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [CryptoPrimitive](CryptoPrimitive.md)!\>!:a set of cryptographic primitives |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm name |
| `parameters` | [AlgorithmParameters](AlgorithmParameters.md)!:the algorithm parameters, or null if no additional parameters |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the algorithm is permitted and can be used for all of the specified cryptographic primitives |

| Exceptions ||
|--------------------------------------|---------------------------------------------|
| `java.lang.IllegalArgumentException` | if primitives or algorithm is null or empty |

### permits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun permits(
    primitives: MutableSet<CryptoPrimitive!>!, 
    algorithm: String!, 
    key: Key!, 
    parameters: AlgorithmParameters!
): Boolean
```

Determines whether an algorithm and the corresponding key are granted permission for the specified cryptographic primitives.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `primitives` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [CryptoPrimitive](CryptoPrimitive.md)!\>!:a set of cryptographic primitives |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm name |
| `key` | [Key](Key.md)!:the key |
| --- | --- |
| `parameters` | [AlgorithmParameters](AlgorithmParameters.md)!:the algorithm parameters, or null if no additional parameters |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the key and the algorithm can be used for all of the specified cryptographic primitives |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if primitives or algorithm is null or empty, or the key is null |

### permits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun permits(
    primitives: MutableSet<CryptoPrimitive!>!, 
    key: Key!
): Boolean
```

Determines whether a key is granted permission for the specified cryptographic primitives.

This method is usually used to check key size and key usage.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `primitives` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [CryptoPrimitive](CryptoPrimitive.md)!\>!:a set of cryptographic primitives |
| `key` | [Key](Key.md)!:the key |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the key can be used for all of the specified cryptographic primitives |

| Exceptions ||
|--------------------------------------|----------------------------------------------------|
| `java.lang.IllegalArgumentException` | if primitives is null or empty, or the key is null |
