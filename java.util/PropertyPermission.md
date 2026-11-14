Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PropertyPermission

```
class PropertyPermission : BasicPermission
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.security.Permission](../java.security/Permission.md) |||
| | ↳ | [java.security.BasicPermission](../java.security/BasicPermission.md) ||
| | | ↳ | [java.util.PropertyPermission](PropertyPermission.md) |
| --- | --- | --- | --- |

Legacy security code; do not use.

## Summary

| Public constructors ||
|---|---|
| PropertyPermission <br /> |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/security/Permission.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | checkGuard Determines whether or not to allow access to the guarded object `object`. Returns silently if access is allowed. Otherwise, throws a SecurityException. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getName <br /> | | `https://developer.android.com/reference/kotlin/java/security/PermissionCollection.html#!` | newPermissionCollection <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/security/BasicPermission.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getActions <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | implies <br /> | ||

## Public constructors

### PropertyPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PropertyPermission(
    name: String!, 
    actions: String!)
```
