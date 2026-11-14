# SubjectDomainCombiner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SubjectDomainCombiner

```
open class SubjectDomainCombiner : DomainCombiner
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.security.auth.SubjectDomainCombiner](../javax/security/auth/SubjectDomainCombiner.md) |

Legacy security code; do not use.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SubjectDomainCombiner](../javax/security/auth/SubjectDomainCombiner.md))`(`subject:` ` [Subject](../javax/security/auth/Subject.md)!`)` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ProtectionDomain](../java/security/ProtectionDomain.md)!\>! | [combine](../javax/security/auth/SubjectDomainCombiner.md))`(`currentDomains:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ProtectionDomain](../java/security/ProtectionDomain.md)!>!`, `assignedDomains:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ProtectionDomain](../java/security/ProtectionDomain.md)!>!`)` <br /> |
| open [Subject](../javax/security/auth/Subject.md)! | [getSubject](../javax/security/auth/SubjectDomainCombiner.md))`()` <br /> |

## Public constructors

### SubjectDomainCombiner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SubjectDomainCombiner(subject: Subject!)
```

## Public methods

### combine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun combine(
    currentDomains: Array<ProtectionDomain!>!, 
    assignedDomains: Array<ProtectionDomain!>!
): Array<ProtectionDomain!>!
```  

### getSubject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSubject(): Subject!
```
