# CallSite

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CallSite

```
abstract class CallSite
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.invoke.CallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#) |

| Known Direct Subclasses [ConstantCallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/ConstantCallSite), [MutableCallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/MutableCallSite), [VolatileCallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/VolatileCallSite) |------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ConstantCallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/ConstantCallSite) | A`ConstantCallSite`is a [CallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#) whose target is permanent, and can never be changed. | | [MutableCallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/MutableCallSite) | A`MutableCallSite`is a [CallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#) whose target variable behaves like an ordinary field. | | [VolatileCallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/VolatileCallSite) | A`VolatileCallSite`is a [CallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#) whose target acts like a volatile variable. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A`CallSite`is a holder for a variable [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle), which is called its`target`. An`invokedynamic`instruction linked to a`CallSite`delegates all calls to the site's current target. A`CallSite`may be associated with several`invokedynamic`instructions, or it may be "free floating", associated with none. In any case, it may be invoked through an associated method handle called its [dynamic invoker](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#dynamicInvoker()).

`CallSite`is an abstract class which does not allow direct subclassing by users. It has three immediate, concrete subclasses that may be either instantiated or subclassed.

- If a mutable target is not required, an`invokedynamic`instruction may be permanently bound by means of a [constant call site](https://developer.android.com/reference/kotlin/java/lang/invoke/ConstantCallSite).
- If a mutable target is required which has volatile variable semantics, because updates to the target must be immediately and reliably witnessed by other threads, a [volatile call site](https://developer.android.com/reference/kotlin/java/lang/invoke/VolatileCallSite) may be used.
- Otherwise, if a mutable target is required, a [mutable call site](https://developer.android.com/reference/kotlin/java/lang/invoke/MutableCallSite) may be used.

A non-constant call site may be*relinked* by changing its target. The new target must have the same [type](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle#type())as the previous target. Thus, though a call site can be relinked to a series of successive targets, it cannot change its type.

Here is a sample use of call sites and bootstrap methods which links every dynamic call site to print its arguments: 

```kotlin
<code>static void test() throws Throwable {
   // THE FOLLOWING LINE IS PSEUDOCODE FOR A JVM INSTRUCTION
   InvokeDynamic[#bootstrapDynamic].baz("baz arg", 2, 3.14);
 }
 private static void printArgs(Object... args) {
 System.out.println(java.util.Arrays.deepToString(args));
 }
 private static final MethodHandle printArgs;
 static {
 MethodHandles.Lookup lookup = MethodHandles.lookup();
 Class thisClass = lookup.lookupClass();  // (who am I?)
 printArgs = lookup.findStatic(thisClass,
     "printArgs", MethodType.methodType(void.class, Object[].class));
 }
 private static CallSite bootstrapDynamic(MethodHandles.Lookup caller, String name, MethodType type) {
 // ignore caller and name, but match the type:
 return new ConstantCallSite(printArgs.asType(type));
 }
 </code>
```

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle)! | [dynamicInvoker](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#dynamicInvoker())`()` Produces a method handle equivalent to an invokedynamic instruction which has been linked to this call site. |
| abstract [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle)! | [getTarget](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#getTarget())`()` Returns the target method of the call site, according to the behavior defined by this call site's specific class. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTarget](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#setTarget(java.lang.invoke.MethodHandle))`(`newTarget:` ` [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle)!`)` Updates the target method of this call site, according to the behavior defined by this call site's specific class. |
| --- | --- |
| open [MethodType](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodType)! | [type](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#type())`()` Returns the type of this call site's target. |

## Public methods

### dynamicInvoker

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun dynamicInvoker(): MethodHandle!
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
| [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle)! | a method handle which always invokes this call site's current target |

### getTarget

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTarget(): MethodHandle!
```

Returns the target method of the call site, according to the behavior defined by this call site's specific class. The immediate subclasses of`CallSite`document the class-specific behaviors of this method.

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle)! | the current linkage state of the call site, its target method handle |

**See Also**

- [java.lang.invoke.ConstantCallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/ConstantCallSite)
- [java.lang.invoke.VolatileCallSite](https://developer.android.com/reference/kotlin/java/lang/invoke/VolatileCallSite)
- [#setTarget](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#setTarget(java.lang.invoke.MethodHandle))
- [java.lang.invoke.ConstantCallSite#getTarget](https://developer.android.com/reference/kotlin/java/lang/invoke/ConstantCallSite#getTarget())
- [java.lang.invoke.MutableCallSite#getTarget](https://developer.android.com/reference/kotlin/java/lang/invoke/MutableCallSite#getTarget())
- [java.lang.invoke.VolatileCallSite#getTarget](https://developer.android.com/reference/kotlin/java/lang/invoke/VolatileCallSite#getTarget()) 

### setTarget

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTarget(newTarget: MethodHandle!): Unit
```

Updates the target method of this call site, according to the behavior defined by this call site's specific class. The immediate subclasses of`CallSite`document the class-specific behaviors of this method.

The type of the new target must be [equal to](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodType#equals(kotlin.Any))the type of the old target.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------|
| `newTarget` | [MethodHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle)!:the new target |

| Exceptions ||
|---------------------------------------------|------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the proposed new target is null |
| `java.lang.invoke.WrongMethodTypeException` | if the proposed new target has a method type that differs from the previous target |

**See Also**

- [java.lang.invoke.CallSite#getTarget](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#getTarget())
- [java.lang.invoke.ConstantCallSite#setTarget](https://developer.android.com/reference/kotlin/java/lang/invoke/ConstantCallSite#setTarget(java.lang.invoke.MethodHandle))
- [java.lang.invoke.MutableCallSite#setTarget](https://developer.android.com/reference/kotlin/java/lang/invoke/MutableCallSite#setTarget(java.lang.invoke.MethodHandle))
- [java.lang.invoke.VolatileCallSite#setTarget](https://developer.android.com/reference/kotlin/java/lang/invoke/VolatileCallSite#setTarget(java.lang.invoke.MethodHandle)) 

### type

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun type(): MethodType!
```

Returns the type of this call site's target. Although targets may change, any call site's type is permanent, and can never change to an unequal type. The`setTarget`method enforces this invariant by refusing any new target that does not have the previous target's type.

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [MethodType](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodType)! | the type of the current target, which is also the type of any future target |
