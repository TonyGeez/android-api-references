# Permission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Permission

```
abstract class Permission : Guard, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.Permission](https://developer.android.com/reference/kotlin/java/security/Permission#) |

| Known Direct Subclasses [AllPermission](https://developer.android.com/reference/kotlin/java/security/AllPermission), [BasicPermission](https://developer.android.com/reference/kotlin/java/security/BasicPermission), [FilePermission](https://developer.android.com/reference/kotlin/java/io/FilePermission.html#), [PrivateCredentialPermission](https://developer.android.com/reference/kotlin/javax/security/auth/PrivateCredentialPermission.html#), [SocketPermission](https://developer.android.com/reference/kotlin/java/net/SocketPermission.html#), [UnresolvedPermission](https://developer.android.com/reference/kotlin/java/security/UnresolvedPermission) |-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------| | [AllPermission](https://developer.android.com/reference/kotlin/java/security/AllPermission) | Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). | | [BasicPermission](https://developer.android.com/reference/kotlin/java/security/BasicPermission) | Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). | | [FilePermission](https://developer.android.com/reference/kotlin/java/io/FilePermission.html#) | Legacy security code; do not use. | | [PrivateCredentialPermission](https://developer.android.com/reference/kotlin/javax/security/auth/PrivateCredentialPermission.html#) | Legacy security code; do not use. | | [SocketPermission](https://developer.android.com/reference/kotlin/java/net/SocketPermission.html#) | Legacy security code; do not use. | | [UnresolvedPermission](https://developer.android.com/reference/kotlin/java/security/UnresolvedPermission) | Legacy security code; do not use. | |

| Known Indirect Subclasses [AuthPermission](https://developer.android.com/reference/kotlin/javax/security/auth/AuthPermission.html#), [LinkPermission](https://developer.android.com/reference/kotlin/java/nio/file/LinkPermission.html#), [LoggingPermission](https://developer.android.com/reference/kotlin/java/util/logging/LoggingPermission.html#), [NetPermission](https://developer.android.com/reference/kotlin/java/net/NetPermission.html#), [PropertyPermission](https://developer.android.com/reference/kotlin/java/util/PropertyPermission.html#), [ReflectPermission](https://developer.android.com/reference/kotlin/java/lang/reflect/ReflectPermission.html#), [RuntimePermission](https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#), [SQLPermission](https://developer.android.com/reference/kotlin/java/sql/SQLPermission.html#), [SSLPermission](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLPermission.html#), [SecurityPermission](https://developer.android.com/reference/kotlin/java/security/SecurityPermission), [SerializablePermission](https://developer.android.com/reference/kotlin/java/io/SerializablePermission.html#) |---------------------------------------------------------------------------------------------------------------|----------------------------------------------------| | [AuthPermission](https://developer.android.com/reference/kotlin/javax/security/auth/AuthPermission.html#) | Legacy security code; do not use. | | [LinkPermission](https://developer.android.com/reference/kotlin/java/nio/file/LinkPermission.html#) | The`Permission`class for link creation operations. | | [LoggingPermission](https://developer.android.com/reference/kotlin/java/util/logging/LoggingPermission.html#) | Legacy security code; do not use. | | [NetPermission](https://developer.android.com/reference/kotlin/java/net/NetPermission.html#) | Legacy security code; do not use. | | [PropertyPermission](https://developer.android.com/reference/kotlin/java/util/PropertyPermission.html#) | Legacy security code; do not use. | | [ReflectPermission](https://developer.android.com/reference/kotlin/java/lang/reflect/ReflectPermission.html#) | Legacy security code; do not use. | | [RuntimePermission](https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#) | Legacy security code; do not use. | | [SQLPermission](https://developer.android.com/reference/kotlin/java/sql/SQLPermission.html#) | Legacy security code; do not use. | | [SSLPermission](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLPermission.html#) | Legacy security code; do not use. | | [SecurityPermission](https://developer.android.com/reference/kotlin/java/security/SecurityPermission) | Legacy security code; do not use. | | [SerializablePermission](https://developer.android.com/reference/kotlin/java/io/SerializablePermission.html#) | This legacy security is not supported on Android. | |

Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). Do not use this class.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Permission](https://developer.android.com/reference/kotlin/java/security/Permission#Permission(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkGuard](https://developer.android.com/reference/kotlin/java/security/Permission#checkGuard(kotlin.Any))`(`object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getActions](https://developer.android.com/reference/kotlin/java/security/Permission#getActions())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/java/security/Permission#getName())`()` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](https://developer.android.com/reference/kotlin/java/security/Permission#implies(java.security.Permission))`(`permission:` ` [Permission](https://developer.android.com/reference/kotlin/java/security/Permission#)!`)` <br /> |
| open [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection)! | [newPermissionCollection](https://developer.android.com/reference/kotlin/java/security/Permission#newPermissionCollection())`()` <br /> |

## Public constructors

### Permission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Permission(name: String!)
```

## Public methods

### checkGuard

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkGuard(object: Any!): Unit
```

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------|
| `object` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object being protected by the guard. |

### getActions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getActions(): String!
```  

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String!
```  

### implies

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun implies(permission: Permission!): Boolean
```  

### newPermissionCollection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newPermissionCollection(): PermissionCollection!
```
