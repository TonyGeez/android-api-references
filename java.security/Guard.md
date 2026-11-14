# Guard

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Guard

```
interface Guard
```

| [java.security.Guard](https://developer.android.com/reference/kotlin/java/security/Guard#) |

| Known Direct Subclasses [Permission](https://developer.android.com/reference/kotlin/java/security/Permission) |---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------| | [Permission](https://developer.android.com/reference/kotlin/java/security/Permission) | Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). | |

| Known Indirect Subclasses [AllPermission](https://developer.android.com/reference/kotlin/java/security/AllPermission), [AuthPermission](https://developer.android.com/reference/kotlin/javax/security/auth/AuthPermission.html#), [BasicPermission](https://developer.android.com/reference/kotlin/java/security/BasicPermission), [FilePermission](https://developer.android.com/reference/kotlin/java/io/FilePermission.html#), [LinkPermission](https://developer.android.com/reference/kotlin/java/nio/file/LinkPermission.html#), [LoggingPermission](https://developer.android.com/reference/kotlin/java/util/logging/LoggingPermission.html#), [NetPermission](https://developer.android.com/reference/kotlin/java/net/NetPermission.html#), [PrivateCredentialPermission](https://developer.android.com/reference/kotlin/javax/security/auth/PrivateCredentialPermission.html#), [PropertyPermission](https://developer.android.com/reference/kotlin/java/util/PropertyPermission.html#), [ReflectPermission](https://developer.android.com/reference/kotlin/java/lang/reflect/ReflectPermission.html#), [RuntimePermission](https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#), [SQLPermission](https://developer.android.com/reference/kotlin/java/sql/SQLPermission.html#), and 5 others. |-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------| | [AllPermission](https://developer.android.com/reference/kotlin/java/security/AllPermission) | Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). | | [AuthPermission](https://developer.android.com/reference/kotlin/javax/security/auth/AuthPermission.html#) | Legacy security code; do not use. | | [BasicPermission](https://developer.android.com/reference/kotlin/java/security/BasicPermission) | Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). | | [FilePermission](https://developer.android.com/reference/kotlin/java/io/FilePermission.html#) | Legacy security code; do not use. | | [LinkPermission](https://developer.android.com/reference/kotlin/java/nio/file/LinkPermission.html#) | The`Permission`class for link creation operations. | | [LoggingPermission](https://developer.android.com/reference/kotlin/java/util/logging/LoggingPermission.html#) | Legacy security code; do not use. | | [NetPermission](https://developer.android.com/reference/kotlin/java/net/NetPermission.html#) | Legacy security code; do not use. | | [PrivateCredentialPermission](https://developer.android.com/reference/kotlin/javax/security/auth/PrivateCredentialPermission.html#) | Legacy security code; do not use. | | [PropertyPermission](https://developer.android.com/reference/kotlin/java/util/PropertyPermission.html#) | Legacy security code; do not use. | | [ReflectPermission](https://developer.android.com/reference/kotlin/java/lang/reflect/ReflectPermission.html#) | Legacy security code; do not use. | | [RuntimePermission](https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#) | Legacy security code; do not use. | | [SQLPermission](https://developer.android.com/reference/kotlin/java/sql/SQLPermission.html#) | Legacy security code; do not use. | | [SSLPermission](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLPermission.html#) | Legacy security code; do not use. | | [SecurityPermission](https://developer.android.com/reference/kotlin/java/security/SecurityPermission) | Legacy security code; do not use. | | [SerializablePermission](https://developer.android.com/reference/kotlin/java/io/SerializablePermission.html#) | This legacy security is not supported on Android. | | [SocketPermission](https://developer.android.com/reference/kotlin/java/net/SocketPermission.html#) | Legacy security code; do not use. | | [UnresolvedPermission](https://developer.android.com/reference/kotlin/java/security/UnresolvedPermission) | Legacy security code; do not use. | |

This interface represents a guard, which is an object that is used to protect access to another object.

This interface contains a single method,`checkGuard`, with a single`object`argument.`checkGuard`is invoked (by the GuardedObject`getObject`method) to determine whether or not to allow access to the object.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkGuard](https://developer.android.com/reference/kotlin/java/security/Guard#checkGuard(kotlin.Any))`(`object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Determines whether or not to allow access to the guarded object`object`. |

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
