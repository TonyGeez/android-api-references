# CodeSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CodeSource

```
open class CodeSource : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.CodeSource](../java/security/CodeSource.md) |

Legacy security code; do not use.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CodeSource](../java/security/CodeSource.md))`(`url:` ` [URL](../java/net/URL.md)!`, `certs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](../java/security/cert/Certificate.md)!>!`)` <br /> |
| [CodeSource](../java/security/CodeSource.md))`(`url:` ` [URL](../java/net/URL.md)!`, `signers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CodeSigner](../java/security/CodeSigner.md)!>!`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](../java/security/cert/Certificate.md)!\>! | [getCertificates](../java/security/CodeSource.md))`()` <br /> |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CodeSigner](../java/security/CodeSigner.md)!\>! | [getCodeSigners](../java/security/CodeSource.md))`()` <br /> |
| [URL](../java/net/URL.md)! | [getLocation](../java/security/CodeSource.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](../java/security/CodeSource.md))`(`codesource:` ` [CodeSource](../java/security/CodeSource.md)!`)` <br /> |

## Public constructors

### CodeSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CodeSource(
    url: URL!, 
    certs: Array<Certificate!>!)
```  

### CodeSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CodeSource(
    url: URL!, 
    signers: Array<CodeSigner!>!)
```

## Public methods

### getCertificates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCertificates(): Array<Certificate!>!
```  

### getCodeSigners

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCodeSigners(): Array<CodeSigner!>!
```  

### getLocation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocation(): URL!
```  

### implies

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun implies(codesource: CodeSource!): Boolean
```
