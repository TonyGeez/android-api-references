# StackWalker

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StackWalker

```
class StackWalker
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.StackWalker](StackWalker.md) |

A stack walker.

The [walk](StackWalker.md))method opens a sequential stream of [StackFrame](../java/lang/StackWalker.StackFrame.md) s for the current thread and then applies the given function to walk the`StackFrame`stream. The stream reports stack frame elements in order, from the top most frame that represents the execution point at which the stack was generated to the bottom most frame. The`StackFrame`stream is closed when the`walk`method returns. If an attempt is made to reuse the closed stream,`IllegalStateException`will be thrown.

The [*stack walking options*](../java/lang/StackWalker.Option.md) of a`StackWalker`determines the information of [StackFrame](../java/lang/StackWalker.StackFrame.md) objects to be returned. By default, stack frames of the reflection API and implementation classes are [hidden](../java/lang/StackWalker.Option.md) and`StackFrame`s have the class name and method name available but not the [Class reference](../java/lang/StackWalker.StackFrame.md)).

`StackWalker`is thread-safe. Multiple threads can share a single`StackWalker`object to traverse its own stack. A permission check is performed when a`StackWalker`is created, according to the options it requests. No further permission check is done at stack walking time.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Option](../java/lang/StackWalker.Option.md) Stack walker option to configure the [stack frame](../java/lang/StackWalker.StackFrame.md) information obtained by a`StackWalker`. |
| abstract | [StackFrame](../java/lang/StackWalker.StackFrame.md) A`StackFrame`object represents a method invocation returned by [StackWalker](StackWalker.md). |

| Public methods ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](StackWalker.md))`(`action:` ` [Consumer](../java.util.function/Consumer.md)<in` ` [StackWalker.StackFrame](../java/lang/StackWalker.StackFrame.md)!>!`)` Performs the given action on each element of`StackFrame`stream of the current thread, traversing from the top frame of the stack, which is the method calling this`forEach`method. |
| [Class](Class.md)\<\*\>! | [getCallerClass](StackWalker.md))`()` Gets the`Class`object of the caller who invoked the method that invoked`getCallerClass`. |
| static [StackWalker](StackWalker.md)! | [getInstance](StackWalker.md))`()` Returns a`StackWalker`instance. |
| --- | --- |
| static [StackWalker](StackWalker.md)! | [getInstance](StackWalker.md))`(`option:` ` [StackWalker.Option](../java/lang/StackWalker.Option.md)!`)` Returns a`StackWalker`instance with the given option specifying the stack frame information it can access. |
| static [StackWalker](StackWalker.md)! | [getInstance](StackWalker.md))`(`options:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [StackWalker.Option](../java/lang/StackWalker.Option.md)!>!`)` Returns a`StackWalker`instance with the given`options`specifying the stack frame information it can access. |
| static [StackWalker](StackWalker.md)! | [getInstance](StackWalker.md))`(`options:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [StackWalker.Option](../java/lang/StackWalker.Option.md)!>!`, `estimateDepth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a`StackWalker`instance with the given`options`specifying the stack frame information it can access. |
| --- | --- |
| T | [walk](StackWalker.md))`(`function:` ` [Function](../java.util.function/Function.md)<in` ` [Stream](../java.util.stream/Stream.md)< [StackWalker.StackFrame](../java/lang/StackWalker.StackFrame.md)!>!,` `out` `T>!`)` Applies the given function to the stream of`StackFrame`s for the current thread, traversing from the top frame of the stack, which is the method calling this`walk`method. |

## Public methods

### forEach

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forEach(action: Consumer<in StackWalker.StackFrame!>!): Unit
```

Performs the given action on each element of`StackFrame`stream of the current thread, traversing from the top frame of the stack, which is the method calling this`forEach`method.

This method is equivalent to calling
`walk(s -> { s.forEach(action); return null; });`

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](../java.util.function/Consumer.md)\<in [StackWalker.StackFrame](../java/lang/StackWalker.StackFrame.md)!\>!:an action to be performed on each`StackFrame`of the stack of the current thread |

### getCallerClass

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCallerClass(): Class<*>!
```

Gets the`Class`object of the caller who invoked the method that invoked`getCallerClass`.

This method filters [frames](../java/lang/StackWalker.Option.md), [java.lang.invoke.MethodHandle](../java.lang.invoke/MethodHandle.md), and [hidden frames](../java/lang/StackWalker.Option.md) regardless of the [SHOW_REFLECT_FRAMES](../java/lang/StackWalker.Option.md) and [SHOW_HIDDEN_FRAMES](../java/lang/StackWalker.Option.md) options this`StackWalker`has been configured with.

This method should be called when a caller frame is present. If it is called from the bottom most frame on the stack,`IllegalCallerException`will be thrown.

This method throws`UnsupportedOperationException`if this`StackWalker`is not configured with the [RETAIN_CLASS_REFERENCE](../java/lang/StackWalker.Option.md) option.

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| [Class](Class.md)<*>! | `Class`object of the caller's caller invoking this method. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if this`StackWalker`is not configured with [Option.RETAIN_CLASS_REFERENCE](../java/lang/StackWalker.Option.md). |
| `java.lang.IllegalCallerException` | if there is no caller frame, i.e. when this`getCallerClass`method is called from a method which is the last frame on the stack. |

### getInstance

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(): StackWalker!
```

Returns a`StackWalker`instance.

This`StackWalker`is configured to skip all [hidden frames](../java/lang/StackWalker.Option.md) and no [class reference](../java/lang/StackWalker.Option.md) is retained.

| Return ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [StackWalker](StackWalker.md)! | a`StackWalker`configured to skip all [hidden frames](../java/lang/StackWalker.Option.md) and no [class reference](../java/lang/StackWalker.Option.md) is retained. |

### getInstance

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(option: StackWalker.Option!): StackWalker!
```

Returns a`StackWalker`instance with the given option specifying the stack frame information it can access.

If a security manager is present and the given`option`is [Option.RETAIN_CLASS_REFERENCE](../java/lang/StackWalker.Option.md), it calls its java.lang.SecurityManager#checkPermission method for`RuntimePermission("getStackWalkerWithClassReference")`.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `option` | [StackWalker.Option](../java/lang/StackWalker.Option.md)!: [stack walking option](../java/lang/StackWalker.Option.md) |

| Return ||
|---------------------------------------------------------------------------------------|------------------------------------------------|
| [StackWalker](StackWalker.md)! | a`StackWalker`configured with the given option |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkPermission`method denies access. |

### getInstance

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(options: MutableSet<StackWalker.Option!>!): StackWalker!
```

Returns a`StackWalker`instance with the given`options`specifying the stack frame information it can access. If the given`options`is empty, this`StackWalker`is configured to skip all [hidden frames](../java/lang/StackWalker.Option.md) and no [class reference](../java/lang/StackWalker.Option.md) is retained.

If a security manager is present and the given`options`contains [Option.RETAIN_CLASS_REFERENCE](../java/lang/StackWalker.Option.md), it calls its java.lang.SecurityManager#checkPermission method for`RuntimePermission("getStackWalkerWithClassReference")`.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `options` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [StackWalker.Option](../java/lang/StackWalker.Option.md)!\>!: [stack walking option](../java/lang/StackWalker.Option.md) |

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------|
| [StackWalker](StackWalker.md)! | a`StackWalker`configured with the given options |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkPermission`method denies access. |

### getInstance

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    options: MutableSet<StackWalker.Option!>!, 
    estimateDepth: Int
): StackWalker!
```

Returns a`StackWalker`instance with the given`options`specifying the stack frame information it can access. If the given`options`is empty, this`StackWalker`is configured to skip all [hidden frames](../java/lang/StackWalker.Option.md) and no [class reference](../java/lang/StackWalker.Option.md) is retained.

If a security manager is present and the given`options`contains [Option.RETAIN_CLASS_REFERENCE](../java/lang/StackWalker.Option.md), it calls its java.lang.SecurityManager#checkPermission method for`RuntimePermission("getStackWalkerWithClassReference")`.

The`estimateDepth`specifies the estimate number of stack frames this`StackWalker`will traverse that the`StackWalker`could use as a hint for the buffer size.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `options` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [StackWalker.Option](../java/lang/StackWalker.Option.md)!\>!: [stack walking options](../java/lang/StackWalker.Option.md) |
| `estimateDepth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Estimate number of stack frames to be traversed. |

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------|
| [StackWalker](StackWalker.md)! | a`StackWalker`configured with the given options |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`estimateDepth <= 0` |
| `java.lang.SecurityException` | if a security manager exists and its`checkPermission`method denies access. |

### walk

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <T : Any!> walk(function: Function<in Stream<StackWalker.StackFrame!>!, out T>!): T
```

Applies the given function to the stream of`StackFrame`s for the current thread, traversing from the top frame of the stack, which is the method calling this`walk`method.

The`StackFrame`stream will be closed when this method returns. When a closed`Stream<StackFrame>`object is reused,`IllegalStateException`will be thrown.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `function` | [Function](../java.util.function/Function.md)\<in [Stream](../java.util.stream/Stream.md)\< [StackWalker.StackFrame](../java/lang/StackWalker.StackFrame.md)!\>!,outT\>!:a function that takes a stream of [stack frames](../java/lang/StackWalker.StackFrame.md) and returns a result. |
| `<T>` | The type of the result of applying the function to the stream of [stack frame](../java/lang/StackWalker.StackFrame.md). |

| Return ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| T | the result of applying the function to the stream of [stack frame](../java/lang/StackWalker.StackFrame.md). |
