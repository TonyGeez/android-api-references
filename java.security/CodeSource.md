# CodeSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CodeSource

```
open class CodeSource : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.CodeSource](https://developer.android.com/reference/kotlin/java/security/CodeSource#) |

Legacy security code; do not use.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CodeSource](https://developer.android.com/reference/kotlin/java/security/CodeSource#CodeSource(java.net.URL,%20kotlin.Array))`(`url:` ` [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)!`, `certs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!>!`)` <br /> |
| [CodeSource](https://developer.android.com/reference/kotlin/java/security/CodeSource#CodeSource(java.net.URL,%20kotlin.Array))`(`url:` ` [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)!`, `signers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CodeSigner](https://developer.android.com/reference/kotlin/java/security/CodeSigner)!>!`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!\>! | [getCertificates](https://developer.android.com/reference/kotlin/java/security/CodeSource#getCertificates())`()` <br /> |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CodeSigner](https://developer.android.com/reference/kotlin/java/security/CodeSigner)!\>! | [getCodeSigners](https://developer.android.com/reference/kotlin/java/security/CodeSource#getCodeSigners())`()` <br /> |
| [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)! | [getLocation](https://developer.android.com/reference/kotlin/java/security/CodeSource#getLocation())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](https://developer.android.com/reference/kotlin/java/security/CodeSource#implies(java.security.CodeSource))`(`codesource:` ` [CodeSource](https://developer.android.com/reference/kotlin/java/security/CodeSource#)!`)` <br /> |

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
