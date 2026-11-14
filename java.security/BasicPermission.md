# BasicPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BasicPermission

```
abstract class BasicPermission : Permission, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.security.Permission](https://developer.android.com/reference/kotlin/java/security/Permission) ||
| | ↳ | [java.security.BasicPermission](https://developer.android.com/reference/kotlin/java/security/BasicPermission#) |

| Known Direct Subclasses [AuthPermission](https://developer.android.com/reference/kotlin/javax/security/auth/AuthPermission.html#), [LinkPermission](https://developer.android.com/reference/kotlin/java/nio/file/LinkPermission.html#), [LoggingPermission](https://developer.android.com/reference/kotlin/java/util/logging/LoggingPermission.html#), [NetPermission](https://developer.android.com/reference/kotlin/java/net/NetPermission.html#), [PropertyPermission](https://developer.android.com/reference/kotlin/java/util/PropertyPermission.html#), [ReflectPermission](https://developer.android.com/reference/kotlin/java/lang/reflect/ReflectPermission.html#), [RuntimePermission](https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#), [SQLPermission](https://developer.android.com/reference/kotlin/java/sql/SQLPermission.html#), [SSLPermission](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLPermission.html#), [SecurityPermission](https://developer.android.com/reference/kotlin/java/security/SecurityPermission), [SerializablePermission](https://developer.android.com/reference/kotlin/java/io/SerializablePermission.html#) |---------------------------------------------------------------------------------------------------------------|----------------------------------------------------| | [AuthPermission](https://developer.android.com/reference/kotlin/javax/security/auth/AuthPermission.html#) | Legacy security code; do not use. | | [LinkPermission](https://developer.android.com/reference/kotlin/java/nio/file/LinkPermission.html#) | The`Permission`class for link creation operations. | | [LoggingPermission](https://developer.android.com/reference/kotlin/java/util/logging/LoggingPermission.html#) | Legacy security code; do not use. | | [NetPermission](https://developer.android.com/reference/kotlin/java/net/NetPermission.html#) | Legacy security code; do not use. | | [PropertyPermission](https://developer.android.com/reference/kotlin/java/util/PropertyPermission.html#) | Legacy security code; do not use. | | [ReflectPermission](https://developer.android.com/reference/kotlin/java/lang/reflect/ReflectPermission.html#) | Legacy security code; do not use. | | [RuntimePermission](https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#) | Legacy security code; do not use. | | [SQLPermission](https://developer.android.com/reference/kotlin/java/sql/SQLPermission.html#) | Legacy security code; do not use. | | [SSLPermission](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLPermission.html#) | Legacy security code; do not use. | | [SecurityPermission](https://developer.android.com/reference/kotlin/java/security/SecurityPermission) | Legacy security code; do not use. | | [SerializablePermission](https://developer.android.com/reference/kotlin/java/io/SerializablePermission.html#) | This legacy security is not supported on Android. | |

Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). Do not use this class.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BasicPermission](https://developer.android.com/reference/kotlin/java/security/BasicPermission#BasicPermission(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [BasicPermission](https://developer.android.com/reference/kotlin/java/security/BasicPermission#BasicPermission(kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actions:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getActions](https://developer.android.com/reference/kotlin/java/security/BasicPermission#getActions())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](https://developer.android.com/reference/kotlin/java/security/BasicPermission#implies(java.security.Permission))`(`p:` ` [Permission](https://developer.android.com/reference/kotlin/java/security/Permission)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Permission](https://developer.android.com/reference/kotlin/java/security/Permission) |------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkGuard](https://developer.android.com/reference/kotlin/java/security/Permission#checkGuard(kotlin.Any))`(`object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/java/security/Permission#getName())`()` <br /> | | [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection)! | [newPermissionCollection](https://developer.android.com/reference/kotlin/java/security/Permission#newPermissionCollection())`()` <br /> | ||

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
