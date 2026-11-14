# ConstantCallSite

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConstantCallSite

```
open class ConstantCallSite : CallSite
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.lang.invoke.CallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite) ||
| | ↳ | [java.lang.invoke.ConstantCallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/ConstantCallSite#) |

A`ConstantCallSite`is a [CallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite) whose target is permanent, and can never be changed. An`invokedynamic`instruction linked to a`ConstantCallSite`is permanently bound to the call site's target.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ConstantCallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/ConstantCallSite#ConstantCallSite(java.lang.invoke.MethodHandle))`(`target:` ` [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle)!`)` Creates a call site with a permanent target. |

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ConstantCallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/ConstantCallSite#ConstantCallSite(java.lang.invoke.MethodType,%20java.lang.invoke.MethodHandle))`(`targetType:` ` [MethodType](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodType)!`, `createTargetHook:` ` [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle)!`)` Creates a call site with a permanent target, possibly bound to the call site itself. |

| Public methods ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle)! | [dynamicInvoker](https://developer.android.com/reference/kotlin/java/lang/invoke/ConstantCallSite#dynamicInvoker())`()` Returns this call site's permanent target. |
| [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle)! | [getTarget](https://developer.android.com/reference/kotlin/java/lang/invoke/ConstantCallSite#getTarget())`()` Returns the target method of the call site, which behaves like a`final`field of the`ConstantCallSite`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTarget](https://developer.android.com/reference/kotlin/java/lang/invoke/ConstantCallSite#setTarget(java.lang.invoke.MethodHandle))`(`ignore:` ` [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle)!`)` Always throws an [UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#). |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [CallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite) |-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MethodType](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodType)! | [type](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#type())`()` <br /> Returns the type of this call site's target. Although targets may change, any call site's type is permanent, and can never change to an unequal type. The`setTarget`method enforces this invariant by refusing any new target that does not have the previous target's type. <br /> | ||

## Public constructors

### ConstantCallSite

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConstantCallSite(target: MethodHandle!)
```

Creates a call site with a permanent target.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle)!:the target to be permanently associated with this call site |

| Exceptions ||
|----------------------------------|--------------------------------|
| `java.lang.NullPointerException` | if the proposed target is null |

## Protected constructors

### ConstantCallSite

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected ConstantCallSite(
    targetType: MethodType!, 
    createTargetHook: MethodHandle!)
```

Creates a call site with a permanent target, possibly bound to the call site itself.

During construction of the call site, the`createTargetHook`is invoked to produce the actual target, as if by a call of the form`(MethodHandle) createTargetHook.invoke(this)`.

Note that user code cannot perform such an action directly in a subclass constructor, since the target must be fixed before the`ConstantCallSite`constructor returns.

The hook is said to bind the call site to a target method handle, and a typical action would be`someTarget.bindTo(this)`. However, the hook is free to take any action whatever, including ignoring the call site and returning a constant target.

The result returned by the hook must be a method handle of exactly the same type as the call site.

While the hook is being called, the new`ConstantCallSite`object is in a partially constructed state. In this state, a call to`getTarget`, or any other attempt to use the target, will result in an`IllegalStateException`. It is legal at all times to obtain the call site's type using the`type`method.

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `targetType` | [MethodType](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodType)!:the type of the method handle to be permanently associated with this call site |
| `createTargetHook` | [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle)!:a method handle to invoke (on the call site) to produce the call site's target |

| Exceptions ||
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.invoke.WrongMethodTypeException` | if the hook cannot be invoked on the required arguments, or if the target returned by the hook is not of the given`targetType` |
| `java.lang.NullPointerException` | if the hook returns a null value |
| `java.lang.ClassCastException` | if the hook returns something other than a`MethodHandle` |
| --- | --- |
| `java.lang.Throwable` | anything else thrown by the hook function |

## Public methods

### dynamicInvoker

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun dynamicInvoker(): MethodHandle!
```

Returns this call site's permanent target. Since that target will never change, this is a correct implementation of [CallSite.dynamicInvoker](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#dynamicInvoker()).

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle)! | the immutable linkage state of this call site, a constant method handle |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------|
| `java.lang.IllegalStateException` | if the`ConstantCallSite`constructor has not completed |

### getTarget

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTarget(): MethodHandle!
```

Returns the target method of the call site, which behaves like a`final`field of the`ConstantCallSite`. That is, the target is always the original value passed to the constructor call which created this instance.

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle)! | the immutable linkage state of this call site, a constant method handle |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------|
| `java.lang.IllegalStateException` | if the`ConstantCallSite`constructor has not completed |

### setTarget

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTarget(ignore: MethodHandle!): Unit
```

Always throws an [UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#). This kind of call site cannot change its target.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newTarget` | the new target |
| `ignore` | [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle)!:a new target proposed for the call site, which is ignored |

| Exceptions ||
|---------------------------------------------|------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the proposed new target is null |
| `java.lang.invoke.WrongMethodTypeException` | if the proposed new target has a method type that differs from the previous target |
| `java.lang.UnsupportedOperationException` | because this kind of call site cannot change its target |
| --- | --- |
