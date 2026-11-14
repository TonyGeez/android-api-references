# GuardedObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GuardedObject

```
open class GuardedObject : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.GuardedObject](GuardedObject.md) |

A GuardedObject is an object that is used to protect access to another object.

A GuardedObject encapsulates a target object and a Guard object, such that access to the target object is possible only if the Guard object allows it. Once an object is encapsulated by a GuardedObject, access to that object is controlled by the`getObject`method, which invokes the`checkGuard`method on the Guard object that is guarding access. If access is not allowed, an exception is thrown.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GuardedObject](GuardedObject.md))`(`object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `guard:` ` [Guard](Guard.md)!`)` Constructs a GuardedObject using the specified object and guard. |

| Public methods ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getObject](GuardedObject.md))`()` Retrieves the guarded object, or throws an exception if access to the guarded object is denied by the guard. |

## Public constructors

### GuardedObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GuardedObject(
    object: Any!, 
    guard: Guard!)
```

Constructs a GuardedObject using the specified object and guard. If the Guard object is null, then no restrictions will be placed on who can access the object.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `object` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object to be guarded. |
| `guard` | [Guard](Guard.md)!:the Guard object that guards access to the object. |

## Public methods

### getObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getObject(): Any!
```

Retrieves the guarded object, or throws an exception if access to the guarded object is denied by the guard.

| Return ||
|-----------------------------------------------------------------------------|---------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the guarded object. |

| Exceptions ||
|-------------------------------|--------------------------------------------|
| `java.lang.SecurityException` | if access to the guarded object is denied. |
