# RenderScript

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RenderScript

Kotlin| [Java](RenderScript.md) 
| --- | --- |

```
open class RenderScript
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.renderscript.RenderScript](RenderScript.md) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

This class provides access to a RenderScript context, which controls RenderScript initialization, resource management, and teardown. An instance of the RenderScript class must be created before any other RS objects can be created.
|
| ### Developer Guides
|
| For more information about creating an application that uses RenderScript, read the [RenderScript](https://developer.android.com/guide/topics/renderscript/index.html) developer guide.

<br />

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [ContextType](../android/renderscript/RenderScript.ContextType.md) ContextType specifies the specific type of context to be created. |
| | [Priority](../android/renderscript/RenderScript.Priority.md) RenderScript worker thread priority enumeration. |
| open | [RSErrorHandler](../android/renderscript/RenderScript.RSErrorHandler.md) The runtime error handler base class. |
| --- | --- |
| open | [RSMessageHandler](../android/renderscript/RenderScript.RSMessageHandler.md) The base class from which an application should derive in order to receive RS messages from scripts. |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CREATE_FLAG_LOW_LATENCY](RenderScript.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CREATE_FLAG_LOW_POWER](RenderScript.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CREATE_FLAG_NONE](RenderScript.md) <br /> |
| --- | --- |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [contextDump](RenderScript.md))`()` Print the currently available debugging information about the state of the RS context to the log. |
| openstatic [RenderScript](RenderScript.md)! | [create](RenderScript.md))`(`ctx:` ` [Context](../android.content/Context.md)!`)` calls create(ctx, ContextType.NORMAL, CREATE_FLAG_NONE) See documentation for @create for details |
| openstatic [RenderScript](RenderScript.md)! | [create](RenderScript.md))`(`ctx:` ` [Context](../android.content/Context.md)!`, `ct:` ` [RenderScript.ContextType](../android/renderscript/RenderScript.ContextType.md)!`)` calls create(ctx, ct, CREATE_FLAG_NONE) See documentation for @create for details |
| --- | --- |
| openstatic [RenderScript](RenderScript.md)! | [create](RenderScript.md))`(`ctx:` ` [Context](../android.content/Context.md)!`, `ct:` ` [RenderScript.ContextType](../android/renderscript/RenderScript.ContextType.md)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets or creates a RenderScript context of the specified type. |
| openstatic [RenderScript](RenderScript.md)! | [createMultiContext](RenderScript.md))`(`ctx:` ` [Context](../android.content/Context.md)!`, `ct:` ` [RenderScript.ContextType](../android/renderscript/RenderScript.ContextType.md)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `API_number:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a RenderScript context. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](RenderScript.md))`()` Destroys this RenderScript context. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finish](RenderScript.md))`()` Wait for any pending asynchronous opeations (such as copies to a RS allocation or RS script executions) to complete. |
| [Context](../android.content/Context.md)! | [getApplicationContext](RenderScript.md))`()` Gets the application context associated with the RenderScript context. |
| open [RenderScript.RSErrorHandler](../android/renderscript/RenderScript.RSErrorHandler.md)! | [getErrorHandler](RenderScript.md))`()` <br /> |
| --- | --- |
| open [RenderScript.RSMessageHandler](../android/renderscript/RenderScript.RSMessageHandler.md)! | [getMessageHandler](RenderScript.md))`()` <br /> |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMinorVersion](RenderScript.md))`()` Returns an identifier that can be used to identify a particular minor version of RS. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseAllContexts](RenderScript.md))`()` Releases all the process contexts. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendMessage](RenderScript.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Place a message into the message queue to be sent back to the message handler once all previous commands have been executed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](RenderScript.md))`(`msg:` ` [RenderScript.RSErrorHandler](../android/renderscript/RenderScript.RSErrorHandler.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMessageHandler](RenderScript.md))`(`msg:` ` [RenderScript.RSMessageHandler](../android/renderscript/RenderScript.RSMessageHandler.md)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPriority](RenderScript.md))`(`p:` ` [RenderScript.Priority](../android/renderscript/RenderScript.Priority.md)!`)` Change the priority of the worker threads for this context. |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](RenderScript.md))`()` <br /> |

## Constants

### CREATE_FLAG_LOW_LATENCY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATE_FLAG_LOW_LATENCY: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 2

### CREATE_FLAG_LOW_POWER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATE_FLAG_LOW_POWER: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 4

### CREATE_FLAG_NONE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATE_FLAG_NONE: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 0

## Public methods

### contextDump

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contextDump(): Unit
```

**Deprecated:** *Deprecated in Java.*

Print the currently available debugging information about the state of the RS context to the log. 

### create

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(ctx: Context!): RenderScript!
```

**Deprecated:** *Deprecated in Java.*

calls create(ctx, ContextType.NORMAL, CREATE_FLAG_NONE) See documentation for @create for details

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `ctx` | [Context](../android.content/Context.md)!:The context. |

| Return ||
|----------------------------------------------------------------------------------------------------|--------------|
| [RenderScript](RenderScript.md)! | RenderScript |

### create

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    ctx: Context!, 
    ct: RenderScript.ContextType!
): RenderScript!
```

**Deprecated:** *Deprecated in Java.*

calls create(ctx, ct, CREATE_FLAG_NONE) See documentation for @create for details

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ctx` | [Context](../android.content/Context.md)!:The context. |
| `ct` | [RenderScript.ContextType](../android/renderscript/RenderScript.ContextType.md)!:The type of context to be created. |

| Return ||
|----------------------------------------------------------------------------------------------------|--------------|
| [RenderScript](RenderScript.md)! | RenderScript |

### create

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    ctx: Context!, 
    ct: RenderScript.ContextType!, 
    flags: Int
): RenderScript!
```

**Deprecated:** *Deprecated in Java.*

Gets or creates a RenderScript context of the specified type. The returned context will be cached for future reuse within the process. When an application is finished using RenderScript it should call releaseAllContexts() A process context is a context designed for easy creation and lifecycle management. Multiple calls to this function will return the same object provided they are called with the same options. This allows it to be used any time a RenderScript context is needed. Prior to API 23 this always created a new context.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ctx` | [Context](../android.content/Context.md)!:The context. |
| `ct` | [RenderScript.ContextType](../android/renderscript/RenderScript.ContextType.md)!:The type of context to be created. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The OR of the CREATE_FLAG_\* options desired |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------|--------------|
| [RenderScript](RenderScript.md)! | RenderScript |

### createMultiContext

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createMultiContext(
    ctx: Context!, 
    ct: RenderScript.ContextType!, 
    flags: Int, 
    API_number: Int
): RenderScript!
```

**Deprecated:** *Deprecated in Java.*

Create a RenderScript context. This is an advanced function intended for applications which need to create more than one RenderScript context to be used at the same time. If you need a single context please use create()

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `ctx` | [Context](../android.content/Context.md)!:The context. |

| Return ||
|----------------------------------------------------------------------------------------------------|--------------|
| [RenderScript](RenderScript.md)! | RenderScript |

### destroy

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun destroy(): Unit
```

**Deprecated:** *Deprecated in Java.*

Destroys this RenderScript context. Once this function is called, using this context or any objects belonging to this context is illegal. API 23+, this function is a NOP if the context was created with create(). Please use releaseAllContexts() to clean up contexts created with the create function. 

### finish

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun finish(): Unit
```

**Deprecated:** *Deprecated in Java.*

Wait for any pending asynchronous opeations (such as copies to a RS allocation or RS script executions) to complete. 

### getApplicationContext

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getApplicationContext(): Context!
```

**Deprecated:** *Deprecated in Java.*

Gets the application context associated with the RenderScript context.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [Context](../android.content/Context.md)! | The application context. |

### getErrorHandler

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorHandler(): RenderScript.RSErrorHandler!
```

**Deprecated:** *Deprecated in Java.* 

### getMessageHandler

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMessageHandler(): RenderScript.RSMessageHandler!
```

**Deprecated:** *Deprecated in Java.* 

### getMinorVersion

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMinorVersion(): Long
```

**Deprecated:** *Deprecated in Java.*

Returns an identifier that can be used to identify a particular minor version of RS.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The minor RenderScript version number |

### releaseAllContexts

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun releaseAllContexts(): Unit
```

**Deprecated:** *Deprecated in Java.*

Releases all the process contexts. This is the same as calling .destroy() on each unique context retreived with create(...). If no contexts have been created this function does nothing. Typically you call this when your application is losing focus and will not be using a context for some time. This has no effect on a context created with createMultiContext() 

### sendMessage

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sendMessage(
    id: Int, 
    data: IntArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Place a message into the message queue to be sent back to the message handler once all previous commands have been executed.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `data` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: |

### setErrorHandler

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setErrorHandler(msg: RenderScript.RSErrorHandler!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### setMessageHandler

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMessageHandler(msg: RenderScript.RSMessageHandler!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### setPriority

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPriority(p: RenderScript.Priority!): Unit
```

**Deprecated:** *Deprecated in Java.*

Change the priority of the worker threads for this context.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------|
| `p` | [RenderScript.Priority](../android/renderscript/RenderScript.Priority.md)!:New priority to be set. |

## Protected methods

### finalize

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

**Deprecated:** *Deprecated in Java.*

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
