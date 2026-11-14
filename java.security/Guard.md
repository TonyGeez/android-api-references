# Guard

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Guard

```
interface Guard
```

| [java.security.Guard](../java/security/Guard.md) |

| Known Direct Subclasses [Permission](../java/security/Permission.md) |---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------| | [Permission](../java/security/Permission.md) | Android doesn't support [SecurityManager](../java/lang/SecurityManager.md). | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AllPermission](../java/security/AllPermission.md), [AuthPermission](../javax/security/auth/AuthPermission.md), [BasicPermission](../java/security/BasicPermission.md), [FilePermission](../java/io/FilePermission.md), [LinkPermission](../java/nio/file/LinkPermission.md), [LoggingPermission](../java/util/logging/LoggingPermission.md), [NetPermission](../java/net/NetPermission.md), [PrivateCredentialPermission](../javax/security/auth/PrivateCredentialPermission.md), [PropertyPermission](../java/util/PropertyPermission.md), [ReflectPermission](../java/lang/reflect/ReflectPermission.md), [RuntimePermission](../java/lang/RuntimePermission.md), [SQLPermission](../java/sql/SQLPermission.md), and 5 others. |-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------| | [AllPermission](../java/security/AllPermission.md) | Android doesn't support [SecurityManager](../java/lang/SecurityManager.md). | | [AuthPermission](../javax/security/auth/AuthPermission.md) | Legacy security code; do not use. | | [BasicPermission](../java/security/BasicPermission.md) | Android doesn't support [SecurityManager](../java/lang/SecurityManager.md). | | [FilePermission](../java/io/FilePermission.md) | Legacy security code; do not use. | | [LinkPermission](../java/nio/file/LinkPermission.md) | The`Permission`class for link creation operations. | | [LoggingPermission](../java/util/logging/LoggingPermission.md) | Legacy security code; do not use. | | [NetPermission](../java/net/NetPermission.md) | Legacy security code; do not use. | | [PrivateCredentialPermission](../javax/security/auth/PrivateCredentialPermission.md) | Legacy security code; do not use. | | [PropertyPermission](../java/util/PropertyPermission.md) | Legacy security code; do not use. | | [ReflectPermission](../java/lang/reflect/ReflectPermission.md) | Legacy security code; do not use. | | [RuntimePermission](../java/lang/RuntimePermission.md) | Legacy security code; do not use. | | [SQLPermission](../java/sql/SQLPermission.md) | Legacy security code; do not use. | | [SSLPermission](../javax/net/ssl/SSLPermission.md) | Legacy security code; do not use. | | [SecurityPermission](../java/security/SecurityPermission.md) | Legacy security code; do not use. | | [SerializablePermission](../java/io/SerializablePermission.md) | This legacy security is not supported on Android. | | [SocketPermission](../java/net/SocketPermission.md) | Legacy security code; do not use. | | [UnresolvedPermission](../java/security/UnresolvedPermission.md) | Legacy security code; do not use. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This interface represents a guard, which is an object that is used to protect access to another object.

This interface contains a single method,`checkGuard`, with a single`object`argument.`checkGuard`is invoked (by the GuardedObject`getObject`method) to determine whether or not to allow access to the object.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkGuard](../java/security/Guard.md))`(`object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Determines whether or not to allow access to the guarded object`object`. |

## Public methods

### checkGuard

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun checkGuard(object: Any!): Unit
```

Determines whether or not to allow access to the guarded object`object`. Returns silently if access is allowed. Otherwise, throws a SecurityException.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------|
| `object` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object being protected by the guard. |

| Exceptions ||
|-------------------------------|----------------------|
| `java.lang.SecurityException` | if access is denied. |
