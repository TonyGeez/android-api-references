Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PropertyPermission

```
class PropertyPermission : BasicPermission
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [java.security.Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#) |||
| | ↳ | [java.security.BasicPermission](https://developer.android.com/reference/kotlin/java/security/BasicPermission.html#) ||
| | | ↳ | [java.util.PropertyPermission](https://developer.android.com/reference/kotlin/java/util/PropertyPermission#) |

Legacy security code; do not use.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/PropertyPermission#PropertyPermission(kotlin.String,%20kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, actions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/security/Permission.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/security/Permission.html#checkGuard(kotlin.Any)(object: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Determines whether or not to allow access to the guarded object `object`. Returns silently if access is allowed. Otherwise, throws a SecurityException. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/java/security/Permission.html#getName()()` <br /> | | `https://developer.android.com/reference/kotlin/java/security/PermissionCollection.html#!` | `https://developer.android.com/reference/kotlin/java/security/Permission.html#newPermissionCollection()()` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/security/BasicPermission.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/java/security/BasicPermission.html#getActions()()` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/security/BasicPermission.html#implies(java.security.Permission)(p: https://developer.android.com/reference/kotlin/java/security/Permission.html#!)` <br /> | ||

## Public constructors

### PropertyPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PropertyPermission(
    name: String!, 
    actions: String!)
```
