Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptC

Kotlin | [Java](ScriptC.md)
| --- | --- |

```
open class ScriptC : Script
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](BaseObj.md) |||
| | ↳ | [android.renderscript.Script](Script.md) ||
| | | ↳ | [android.renderscript.ScriptC](ScriptC.md) |
| --- | --- | --- | --- |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

The superclass for all user-defined scripts. This is only intended to be used by the generated derived classes.

## Summary

| Protected constructors ||
|---|---|
| ScriptC Only intended for use by the generated derived classes. |
| ScriptC Only intended for use by the generated derived classes. |
| ScriptC Only intended for use by the generated derived classes. |
| ScriptC Only intended for use by the generated derived classes. |

| Inherited functions ||
|---|---|
| From class Script |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | bindAllocation Only intended for use by generated reflected code. <br /> | | `https://developer.android.com/reference/kotlin/android/renderscript/Script.FieldID!` | createFieldID Only to be used by generated reflected classes. <br /> | | `https://developer.android.com/reference/kotlin/android/renderscript/Script.InvokeID!` | createInvokeID Only to be used by generated reflected classes. <br /> | | `https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID!` | createKernelID Only to be used by generated reflected classes. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | forEach Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | forEach Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | forEach Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | forEach Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getVarB <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | getVarD <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | getVarF <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getVarI <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | getVarJ <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | getVarV Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | invoke Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | invoke Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | reduce Only intended for use by generated reflected code. (General reduction) <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setTimeZone <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setVar Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setVar Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setVar Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setVar Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setVar Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setVar Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setVar Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setVar Only intended for use by generated reflected code. <br /> | ||
| From class BaseObj |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | destroy Frees any native resources associated with this object. The primary use is to force immediate cleanup of resources when it is believed the GC will not respond quickly enough. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | equals Compare the current BaseObj with another BaseObj for equality. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | finalize Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup. The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded. The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition. The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates. After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded. The `finalize` method is never invoked more than once by a Java virtual machine for any given object. Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getName <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | hashCode Calculates the hash code value for a BaseObj. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setName setName assigns a name to an object. This object can later be looked up by this name. <br /> | ||

## Protected constructors

### ScriptC

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected ScriptC(
    rs: RenderScript!, 
    resources: Resources!, 
    resourceID: Int)
```

Only intended for use by the generated derived classes.

| Parameters ||
|---|---|
| `rs` | [RenderScript](RenderScript.md)!: |
| `resources` | [Resources](../android.content.res/Resources.md)!: |
| `resourceID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| --- | --- |

### ScriptC

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected ScriptC(
    rs: RenderScript!, 
    resName: String!, 
    bitcode32: ByteArray!, 
    bitcode64: ByteArray!)
```

Only intended for use by the generated derived classes.

| Parameters ||
|---|---|
| `rs` | [RenderScript](RenderScript.md)!: |

### ScriptC

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected ScriptC(
    id: Int, 
    rs: RenderScript!)
```

Only intended for use by the generated derived classes.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `rs` | [RenderScript](RenderScript.md)!: |

### ScriptC

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected ScriptC(
    id: Long, 
    rs: RenderScript!)
```

Only intended for use by the generated derived classes.

| Parameters ||
|---|---|
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): |
| `rs` | [RenderScript](RenderScript.md)!: |
