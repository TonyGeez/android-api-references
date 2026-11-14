# SubjectDomainCombiner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SubjectDomainCombiner

```
open class SubjectDomainCombiner : DomainCombiner
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.security.auth.SubjectDomainCombiner](https://developer.android.com/reference/kotlin/javax/security/auth/SubjectDomainCombiner#) |

Legacy security code; do not use.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SubjectDomainCombiner](https://developer.android.com/reference/kotlin/javax/security/auth/SubjectDomainCombiner#SubjectDomainCombiner(javax.security.auth.Subject))`(`subject:` ` [Subject](https://developer.android.com/reference/kotlin/javax/security/auth/Subject)!`)` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ProtectionDomain](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain.html#)!\>! | [combine](https://developer.android.com/reference/kotlin/javax/security/auth/SubjectDomainCombiner#combine(kotlin.Array,%20kotlin.Array))`(`currentDomains:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ProtectionDomain](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain.html#)!>!`, `assignedDomains:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ProtectionDomain](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain.html#)!>!`)` <br /> |
| open [Subject](https://developer.android.com/reference/kotlin/javax/security/auth/Subject)! | [getSubject](https://developer.android.com/reference/kotlin/javax/security/auth/SubjectDomainCombiner#getSubject())`()` <br /> |

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
