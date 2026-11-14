# DomainCombiner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DomainCombiner

```
interface DomainCombiner
```

| [java.security.DomainCombiner](DomainCombiner.md) |

| Known Direct Subclasses [SubjectDomainCombiner](../javax.security.auth/SubjectDomainCombiner.md) |-------------------------------------------------------------------------------------------------------------------------|-----------------------------------| | [SubjectDomainCombiner](../javax.security.auth/SubjectDomainCombiner.md) | Legacy security code; do not use. | |
| --- | --- | --- | --- | --- | --- | --- |

Legacy security code; do not use.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ProtectionDomain](ProtectionDomain.md)!\>! | [combine](DomainCombiner.md))`(`currentDomains:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ProtectionDomain](ProtectionDomain.md)!>!`, `assignedDomains:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ProtectionDomain](ProtectionDomain.md)!>!`)` <br /> |

## Public methods

### combine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun combine(
    currentDomains: Array<ProtectionDomain!>!, 
    assignedDomains: Array<ProtectionDomain!>!
): Array<ProtectionDomain!>!
```
