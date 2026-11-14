# RenderScript

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RenderScript

Kotlin| [Java](https://developer.android.com/reference/android/renderscript/RenderScript "View this page in Java") 
| --- | --- |

```
open class RenderScript
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.renderscript.RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#) |

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
| | [ContextType](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.ContextType) ContextType specifies the specific type of context to be created. |
| | [Priority](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.Priority) RenderScript worker thread priority enumeration. |
| open | [RSErrorHandler](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.RSErrorHandler) The runtime error handler base class. |
| --- | --- |
| open | [RSMessageHandler](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.RSMessageHandler) The base class from which an application should derive in order to receive RS messages from scripts. |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CREATE_FLAG_LOW_LATENCY](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#CREATE_FLAG_LOW_LATENCY:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CREATE_FLAG_LOW_POWER](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#CREATE_FLAG_LOW_POWER:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CREATE_FLAG_NONE](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#CREATE_FLAG_NONE:kotlin.Int) <br /> |
| --- | --- |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [contextDump](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#contextDump())`()` Print the currently available debugging information about the state of the RS context to the log. |
| openstatic [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#)! | [create](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#create(android.content.Context))`(`ctx:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` calls create(ctx, ContextType.NORMAL, CREATE_FLAG_NONE) See documentation for @create for details |
| openstatic [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#)! | [create](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#create(android.content.Context,%20android.renderscript.RenderScript.ContextType))`(`ctx:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `ct:` ` [RenderScript.ContextType](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.ContextType)!`)` calls create(ctx, ct, CREATE_FLAG_NONE) See documentation for @create for details |
| --- | --- |
| openstatic [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#)! | [create](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#create(android.content.Context,%20android.renderscript.RenderScript.ContextType,%20kotlin.Int))`(`ctx:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `ct:` ` [RenderScript.ContextType](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.ContextType)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets or creates a RenderScript context of the specified type. |
| openstatic [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#)! | [createMultiContext](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#createMultiContext(android.content.Context,%20android.renderscript.RenderScript.ContextType,%20kotlin.Int,%20kotlin.Int))`(`ctx:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `ct:` ` [RenderScript.ContextType](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.ContextType)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `API_number:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a RenderScript context. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#destroy())`()` Destroys this RenderScript context. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finish](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#finish())`()` Wait for any pending asynchronous opeations (such as copies to a RS allocation or RS script executions) to complete. |
| [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | [getApplicationContext](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#getApplicationContext())`()` Gets the application context associated with the RenderScript context. |
| open [RenderScript.RSErrorHandler](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.RSErrorHandler)! | [getErrorHandler](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#getErrorHandler())`()` <br /> |
| --- | --- |
| open [RenderScript.RSMessageHandler](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.RSMessageHandler)! | [getMessageHandler](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#getMessageHandler())`()` <br /> |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMinorVersion](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#getMinorVersion())`()` Returns an identifier that can be used to identify a particular minor version of RS. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseAllContexts](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#releaseAllContexts())`()` Releases all the process contexts. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendMessage](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#sendMessage(kotlin.Int,%20kotlin.IntArray))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Place a message into the message queue to be sent back to the message handler once all previous commands have been executed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorHandler](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#setErrorHandler(android.renderscript.RenderScript.RSErrorHandler))`(`msg:` ` [RenderScript.RSErrorHandler](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.RSErrorHandler)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMessageHandler](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#setMessageHandler(android.renderscript.RenderScript.RSMessageHandler))`(`msg:` ` [RenderScript.RSMessageHandler](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.RSMessageHandler)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPriority](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#setPriority(android.renderscript.RenderScript.Priority))`(`p:` ` [RenderScript.Priority](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.Priority)!`)` Change the priority of the worker threads for this context. |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#finalize())`()` <br /> |

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
| `ctx` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context. |

| Return ||
|----------------------------------------------------------------------------------------------------|--------------|
| [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#)! | RenderScript |

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
| `ctx` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context. |
| `ct` | [RenderScript.ContextType](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.ContextType)!:The type of context to be created. |

| Return ||
|----------------------------------------------------------------------------------------------------|--------------|
| [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#)! | RenderScript |

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
| `ctx` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context. |
| `ct` | [RenderScript.ContextType](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.ContextType)!:The type of context to be created. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The OR of the CREATE_FLAG_\* options desired |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------|--------------|
| [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#)! | RenderScript |

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
| `ctx` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context. |

| Return ||
|----------------------------------------------------------------------------------------------------|--------------|
| [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript#)! | RenderScript |

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
| [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | The application context. |

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
| `p` | [RenderScript.Priority](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript.Priority)!:New priority to be set. |

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
