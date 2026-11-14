# DomainCombiner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DomainCombiner

```
interface DomainCombiner
```

| [java.security.DomainCombiner](https://developer.android.com/reference/kotlin/java/security/DomainCombiner#) |

| Known Direct Subclasses [SubjectDomainCombiner](https://developer.android.com/reference/kotlin/javax/security/auth/SubjectDomainCombiner.html#) |-------------------------------------------------------------------------------------------------------------------------|-----------------------------------| | [SubjectDomainCombiner](https://developer.android.com/reference/kotlin/javax/security/auth/SubjectDomainCombiner.html#) | Legacy security code; do not use. | |

Legacy security code; do not use.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ProtectionDomain](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain)!\>! | [combine](https://developer.android.com/reference/kotlin/java/security/DomainCombiner#combine(kotlin.Array,%20kotlin.Array))`(`currentDomains:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ProtectionDomain](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain)!>!`, `assignedDomains:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ProtectionDomain](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain)!>!`)` <br /> |

## Public methods

### combine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun combine(
    currentDomains: Array<ProtectionDomain!>!, 
    assignedDomains: Array<ProtectionDomain!>!
): Array<ProtectionDomain!>!
```
