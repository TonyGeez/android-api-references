# Permission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Permission

```
abstract class Permission : Guard, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.Permission](Permission.md) |

| Known Direct Subclasses [AllPermission](AllPermission.md), [BasicPermission](BasicPermission.md), [FilePermission](../java.io/FilePermission.md), [PrivateCredentialPermission](../javax.security.auth/PrivateCredentialPermission.md), [SocketPermission](../java.net/SocketPermission.md), [UnresolvedPermission](UnresolvedPermission.md) |-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------| | [AllPermission](AllPermission.md) | Android doesn't support [SecurityManager](../java.lang/SecurityManager.md). | | [BasicPermission](BasicPermission.md) | Android doesn't support [SecurityManager](../java.lang/SecurityManager.md). | | [FilePermission](../java.io/FilePermission.md) | Legacy security code; do not use. | | [PrivateCredentialPermission](../javax.security.auth/PrivateCredentialPermission.md) | Legacy security code; do not use. | | [SocketPermission](../java.net/SocketPermission.md) | Legacy security code; do not use. | | [UnresolvedPermission](UnresolvedPermission.md) | Legacy security code; do not use. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AuthPermission](../javax.security.auth/AuthPermission.md), [LinkPermission](../java.nio.file/LinkPermission.md), [LoggingPermission](../java.util.logging/LoggingPermission.md), [NetPermission](../java.net/NetPermission.md), [PropertyPermission](../java.util/PropertyPermission.md), [ReflectPermission](../java.lang.reflect/ReflectPermission.md), [RuntimePermission](../java.lang/RuntimePermission.md), [SQLPermission](../java.sql/SQLPermission.md), [SSLPermission](../javax.net.ssl/SSLPermission.md), [SecurityPermission](SecurityPermission.md), [SerializablePermission](../java.io/SerializablePermission.md) |---------------------------------------------------------------------------------------------------------------|----------------------------------------------------| | [AuthPermission](../javax.security.auth/AuthPermission.md) | Legacy security code; do not use. | | [LinkPermission](../java.nio.file/LinkPermission.md) | The`Permission`class for link creation operations. | | [LoggingPermission](../java.util.logging/LoggingPermission.md) | Legacy security code; do not use. | | [NetPermission](../java.net/NetPermission.md) | Legacy security code; do not use. | | [PropertyPermission](../java.util/PropertyPermission.md) | Legacy security code; do not use. | | [ReflectPermission](../java.lang.reflect/ReflectPermission.md) | Legacy security code; do not use. | | [RuntimePermission](../java.lang/RuntimePermission.md) | Legacy security code; do not use. | | [SQLPermission](../java.sql/SQLPermission.md) | Legacy security code; do not use. | | [SSLPermission](../javax.net.ssl/SSLPermission.md) | Legacy security code; do not use. | | [SecurityPermission](SecurityPermission.md) | Legacy security code; do not use. | | [SerializablePermission](../java.io/SerializablePermission.md) | This legacy security is not supported on Android. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Android doesn't support [SecurityManager](../java.lang/SecurityManager.md). Do not use this class.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Permission](Permission.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkGuard](Permission.md))`(`object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getActions](Permission.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](Permission.md))`()` <br /> |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](Permission.md))`(`permission:` ` [Permission](Permission.md)!`)` <br /> |
| open [PermissionCollection](PermissionCollection.md)! | [newPermissionCollection](Permission.md))`()` <br /> |

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
