# BasicPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BasicPermission

```
abstract class BasicPermission : Permission, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.Permission](../java/security/Permission.md) ||
| | ↳ | [java.security.BasicPermission](../java/security/BasicPermission.md) |

| Known Direct Subclasses [AuthPermission](../javax/security/auth/AuthPermission.md), [LinkPermission](../java/nio/file/LinkPermission.md), [LoggingPermission](../java/util/logging/LoggingPermission.md), [NetPermission](../java/net/NetPermission.md), [PropertyPermission](../java/util/PropertyPermission.md), [ReflectPermission](../java/lang/reflect/ReflectPermission.md), [RuntimePermission](../java/lang/RuntimePermission.md), [SQLPermission](../java/sql/SQLPermission.md), [SSLPermission](../javax/net/ssl/SSLPermission.md), [SecurityPermission](../java/security/SecurityPermission.md), [SerializablePermission](../java/io/SerializablePermission.md) |---------------------------------------------------------------------------------------------------------------|----------------------------------------------------| | [AuthPermission](../javax/security/auth/AuthPermission.md) | Legacy security code; do not use. | | [LinkPermission](../java/nio/file/LinkPermission.md) | The`Permission`class for link creation operations. | | [LoggingPermission](../java/util/logging/LoggingPermission.md) | Legacy security code; do not use. | | [NetPermission](../java/net/NetPermission.md) | Legacy security code; do not use. | | [PropertyPermission](../java/util/PropertyPermission.md) | Legacy security code; do not use. | | [ReflectPermission](../java/lang/reflect/ReflectPermission.md) | Legacy security code; do not use. | | [RuntimePermission](../java/lang/RuntimePermission.md) | Legacy security code; do not use. | | [SQLPermission](../java/sql/SQLPermission.md) | Legacy security code; do not use. | | [SSLPermission](../javax/net/ssl/SSLPermission.md) | Legacy security code; do not use. | | [SecurityPermission](../java/security/SecurityPermission.md) | Legacy security code; do not use. | | [SerializablePermission](../java/io/SerializablePermission.md) | This legacy security is not supported on Android. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Android doesn't support [SecurityManager](../java/lang/SecurityManager.md). Do not use this class.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BasicPermission](../java/security/BasicPermission.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [BasicPermission](../java/security/BasicPermission.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actions:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getActions](../java/security/BasicPermission.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](../java/security/BasicPermission.md))`(`p:` ` [Permission](../java/security/Permission.md)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Permission](../java/security/Permission.md) |------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkGuard](../java/security/Permission.md))`(`object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../java/security/Permission.md))`()` <br /> | | [PermissionCollection](../java/security/PermissionCollection.md)! | [newPermissionCollection](../java/security/Permission.md))`()` <br /> | ||

## Public constructors

### BasicPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BasicPermission(name: String!)
```  

### BasicPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BasicPermission(
    name: String!, 
    actions: String!)
```

## Public methods

### getActions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActions(): String!
```  

### implies

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun implies(p: Permission!): Boolean
```
