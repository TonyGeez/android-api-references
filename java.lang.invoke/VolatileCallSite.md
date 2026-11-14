# VolatileCallSite

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VolatileCallSite

```
open class VolatileCallSite : CallSite
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.lang.invoke.CallSite](CallSite.md) ||
| | ↳ | [java.lang.invoke.VolatileCallSite](VolatileCallSite.md) |

A`VolatileCallSite`is a [CallSite](CallSite.md) whose target acts like a volatile variable. An`invokedynamic`instruction linked to a`VolatileCallSite`sees updates to its call site target immediately, even if the update occurs in another thread. There may be a performance penalty for such tight coupling between threads.

In other respects, a`VolatileCallSite`is interchangeable with`MutableCallSite`.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [VolatileCallSite](VolatileCallSite.md))`(`target:` ` [MethodHandle](MethodHandle.md)!`)` Creates a call site with a volatile binding to its target. |
| [VolatileCallSite](VolatileCallSite.md))`(`type:` ` [MethodType](MethodType.md)!`)` Creates a call site with a volatile binding to its target. |

| Public methods ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | [dynamicInvoker](VolatileCallSite.md))`()` Produces a method handle equivalent to an invokedynamic instruction which has been linked to this call site. |
| [MethodHandle](MethodHandle.md)! | [getTarget](VolatileCallSite.md))`()` Returns the target method of the call site, which behaves like a`volatile`field of the`VolatileCallSite`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTarget](VolatileCallSite.md))`(`newTarget:` ` [MethodHandle](MethodHandle.md)!`)` Updates the target method of this call site, as a volatile variable. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [CallSite](CallSite.md) |-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MethodType](MethodType.md)! | [type](CallSite.md))`()` <br /> Returns the type of this call site's target. Although targets may change, any call site's type is permanent, and can never change to an unequal type. The`setTarget`method enforces this invariant by refusing any new target that does not have the previous target's type. <br /> | ||

## Public constructors

### VolatileCallSite

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
VolatileCallSite(target: MethodHandle!)
```

Creates a call site with a volatile binding to its target. The target is set to the given value.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [MethodHandle](MethodHandle.md)!:the method handle that will be the initial target of the call site |

| Exceptions ||
|----------------------------------|--------------------------------|
| `java.lang.NullPointerException` | if the proposed target is null |

### VolatileCallSite

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
VolatileCallSite(type: MethodType!)
```

Creates a call site with a volatile binding to its target. The initial target is set to a method handle of the given type which will throw an`IllegalStateException`if called.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [MethodType](MethodType.md)!:the method type that this call site will have |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.NullPointerException` | if the proposed type is null |

## Public methods

### dynamicInvoker

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun dynamicInvoker(): MethodHandle!
```

Produces a method handle equivalent to an invokedynamic instruction which has been linked to this call site.

This method is equivalent to the following code: 

```kotlin
<code>MethodHandle getTarget, invoker, result;
  getTarget = MethodHandles.publicLookup().bind(this, "getTarget", MethodType.methodType(MethodHandle.class));
  invoker = MethodHandles.exactInvoker(this.type());
  result = MethodHandles.foldArguments(invoker, getTarget)
  </code>
```

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle which always invokes this call site's current target |

### getTarget

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTarget(): MethodHandle!
```

Returns the target method of the call site, which behaves like a`volatile`field of the`VolatileCallSite`.

The interactions of`getTarget`with memory are the same as of a read from a`volatile`field.

In particular, the current thread is required to issue a fresh read of the target from memory, and must not fail to see a recent update to the target by another thread.

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | the linkage state of this call site, a method handle which can change over time |

**See Also**

- [#setTarget](VolatileCallSite.md)) 

### setTarget

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTarget(newTarget: MethodHandle!): Unit
```

Updates the target method of this call site, as a volatile variable. The type of the new target must agree with the type of the old target.

The interactions with memory are the same as of a write to a volatile field. In particular, any threads is guaranteed to see the updated target the next time it calls`getTarget`.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------|
| `newTarget` | [MethodHandle](MethodHandle.md)!:the new target |

| Exceptions ||
|---------------------------------------------|------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the proposed new target is null |
| `java.lang.invoke.WrongMethodTypeException` | if the proposed new target has a method type that differs from the previous target |

**See Also**

- [#getTarget](VolatileCallSite.md))
