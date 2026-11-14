# CodeSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CodeSource

```
open class CodeSource : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.CodeSource](CodeSource.md) |

Legacy security code; do not use.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CodeSource](CodeSource.md))`(`url:` ` [URL](../java.net/URL.md)!`, `certs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](../java.security.cert/Certificate.md)!>!`)` <br /> |
| [CodeSource](CodeSource.md))`(`url:` ` [URL](../java.net/URL.md)!`, `signers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CodeSigner](CodeSigner.md)!>!`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](../java.security.cert/Certificate.md)!\>! | [getCertificates](CodeSource.md))`()` <br /> |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CodeSigner](CodeSigner.md)!\>! | [getCodeSigners](CodeSource.md))`()` <br /> |
| [URL](../java.net/URL.md)! | [getLocation](CodeSource.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](CodeSource.md))`(`codesource:` ` [CodeSource](CodeSource.md)!`)` <br /> |

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
