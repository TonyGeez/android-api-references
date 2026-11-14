Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MutableCallSite

```
open class MutableCallSite : CallSite
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.lang.invoke.CallSite](../java/lang/invoke/CallSite.md) ||
| | ↳ | [java.lang.invoke.MutableCallSite](../java/lang/invoke/MutableCallSite.md) |

A `MutableCallSite` is a `https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite` whose target variable behaves like an ordinary field. An `invokedynamic` instruction linked to a `MutableCallSite` delegates all calls to the site's current target. The [dynamic invoker](../java/lang/invoke/CallSite.md)) of a mutable call site also delegates each call to the site's current target.

Here is an example of a mutable call site which introduces a state variable into a method handle chain.

```kotlin
<code>MutableCallSite name = new MutableCallSite(MethodType.methodType(String.class));
 MethodHandle MH_name = name.dynamicInvoker();
 MethodType MT_str1 = MethodType.methodType(String.class);
 MethodHandle MH_upcase = MethodHandles.lookup()
     .findVirtual(String.class, "toUpperCase", MT_str1);
 MethodHandle worker1 = MethodHandles.filterReturnValue(MH_name, MH_upcase);
 name.setTarget(MethodHandles.constant(String.class, "Rocky"));
 assertEquals("ROCKY", (String) worker1.invokeExact());
 name.setTarget(MethodHandles.constant(String.class, "Fred"));
 assertEquals("FRED", (String) worker1.invokeExact());
// (mutation can be continued indefinitely)
  </code>
```

The same call site may be used in several places at once.

```kotlin
<code>MethodType MT_str2 = MethodType.methodType(String.class, String.class);
 MethodHandle MH_cat = lookup().findVirtual(String.class,
   "concat", methodType(String.class, String.class));
 MethodHandle MH_dear = MethodHandles.insertArguments(MH_cat, 1, ", dear?");
 MethodHandle worker2 = MethodHandles.filterReturnValue(MH_name, MH_dear);
 assertEquals("Fred, dear?", (String) worker2.invokeExact());
 name.setTarget(MethodHandles.constant(String.class, "Wilma"));
 assertEquals("WILMA", (String) worker1.invokeExact());
 assertEquals("Wilma, dear?", (String) worker2.invokeExact());
  </code>
```

*Non-synchronization of target values:* A write to a mutable call site's target does not force other threads to become aware of the updated value. Threads which do not perform suitable synchronization actions relative to the updated call site may cache the old target value and delay their use of the new target value indefinitely. (This is a normal consequence of the Java Memory Model as applied to object fields.)

For target values which will be frequently updated, consider using a [volatile call site](../java/lang/invoke/VolatileCallSite.md) instead.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/invoke/MutableCallSite#MutableCallSite(java.lang.invoke.MethodHandle)(target: https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle!)` Creates a call site object with an initial target method handle. |
| `https://developer.android.com/reference/kotlin/java/lang/invoke/MutableCallSite#MutableCallSite(java.lang.invoke.MethodType)(type: https://developer.android.com/reference/kotlin/java/lang/invoke/MethodType!)` Creates a blank call site object with the given method type. |

| Public methods ||
|---|---|
| [MethodHandle](../java/lang/invoke/MethodHandle.md)! | `https://developer.android.com/reference/kotlin/java/lang/invoke/MutableCallSite#dynamicInvoker()()` Produces a method handle equivalent to an invokedynamic instruction which has been linked to this call site. |
| [MethodHandle](../java/lang/invoke/MethodHandle.md)! | `https://developer.android.com/reference/kotlin/java/lang/invoke/MutableCallSite#getTarget()()` Returns the target method of the call site, which behaves like a normal field of the `MutableCallSite`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/invoke/MutableCallSite#setTarget(java.lang.invoke.MethodHandle)(newTarget: https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle!)` Updates the target method of this call site, as a normal variable. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite` |---|---| | `https://developer.android.com/reference/kotlin/java/lang/invoke/MethodType!` | `https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#type()()` Returns the type of this call site's target. Although targets may change, any call site's type is permanent, and can never change to an unequal type. The `setTarget` method enforces this invariant by refusing any new target that does not have the previous target's type. <br /> | ||

## Public constructors

### MutableCallSite

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MutableCallSite(target: MethodHandle!)
```

Creates a call site object with an initial target method handle. The type of the call site is permanently set to the initial target's type.

| Parameters ||
|---|---|
| `target` | [MethodHandle](../java/lang/invoke/MethodHandle.md)!: the method handle that will be the initial target of the call site |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the proposed target is null |

### MutableCallSite

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MutableCallSite(type: MethodType!)
```

Creates a blank call site object with the given method type. The initial target is set to a method handle of the given type which will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` if called.

The type of the call site is permanently set to the given type.

Before this `CallSite` object is returned from a bootstrap method, or invoked in some other manner, it is usually provided with a more useful target method, via a call to `https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#setTarget(java.lang.invoke.MethodHandle)`.

| Parameters ||
|---|---|
| `type` | [MethodType](../java/lang/invoke/MethodType.md)!: the method type that this call site will have |

| Exceptions ||
|---|---|
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
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle!` | a method handle which always invokes this call site's current target |

### getTarget

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTarget(): MethodHandle!
```

Returns the target method of the call site, which behaves like a normal field of the `MutableCallSite`.

The interactions of `getTarget` with memory are the same as of a read from an ordinary variable, such as an array element or a non-volatile, non-final field.

In particular, the current thread may choose to reuse the result of a previous read of the target from memory, and may fail to see a recent update to the target by another thread.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle!` | the linkage state of this call site, a method handle which can change over time |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/invoke/MutableCallSite#setTarget(java.lang.invoke.MethodHandle)`

### setTarget

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTarget(newTarget: MethodHandle!): Unit
```

Updates the target method of this call site, as a normal variable. The type of the new target must agree with the type of the old target.

The interactions with memory are the same as of a write to an ordinary variable, such as an array element or a non-volatile, non-final field.

In particular, unrelated threads may fail to see the updated target until they perform a read from memory. Stronger guarantees can be created by putting appropriate operations into the bootstrap method and/or the target methods used at any given call site.

| Parameters ||
|---|---|
| `newTarget` | [MethodHandle](../java/lang/invoke/MethodHandle.md)!: the new target |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the proposed new target is null |
| `java.lang.invoke.WrongMethodTypeException` | if the proposed new target has a method type that differs from the previous target |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/invoke/MutableCallSite#getTarget()`
