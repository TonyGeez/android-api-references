Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptC

Kotlin | [Java](https://developer.android.com/reference/android/renderscript/ScriptC "View this page in Java")
| --- | --- |

```
open class ScriptC : Script
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj) |||
| | ↳ | [android.renderscript.Script](https://developer.android.com/reference/kotlin/android/renderscript/Script) ||
| | | ↳ | [android.renderscript.ScriptC](https://developer.android.com/reference/kotlin/android/renderscript/ScriptC#) |
| --- | --- | --- | --- |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

The superclass for all user-defined scripts. This is only intended to be used by the generated derived classes.

## Summary

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/renderscript/ScriptC#ScriptC(android.renderscript.RenderScript,%20android.content.res.Resources,%20kotlin.Int)(rs: https://developer.android.com/reference/kotlin/android/renderscript/RenderScript!, resources: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#!, resourceID: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Only intended for use by the generated derived classes. |
| `https://developer.android.com/reference/kotlin/android/renderscript/ScriptC#ScriptC(android.renderscript.RenderScript,%20kotlin.String,%20kotlin.ByteArray,%20kotlin.ByteArray)(rs: https://developer.android.com/reference/kotlin/android/renderscript/RenderScript!, resName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, bitcode32: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, bitcode64: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Only intended for use by the generated derived classes. |
| `https://developer.android.com/reference/kotlin/android/renderscript/ScriptC#ScriptC(kotlin.Int,%20android.renderscript.RenderScript)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, rs: https://developer.android.com/reference/kotlin/android/renderscript/RenderScript!)` Only intended for use by the generated derived classes. |
| `https://developer.android.com/reference/kotlin/android/renderscript/ScriptC#ScriptC(kotlin.Long,%20android.renderscript.RenderScript)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, rs: https://developer.android.com/reference/kotlin/android/renderscript/RenderScript!)` Only intended for use by the generated derived classes. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/renderscript/Script` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#bindAllocation(android.renderscript.Allocation,%20kotlin.Int)(va: https://developer.android.com/reference/kotlin/android/renderscript/Allocation!, slot: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Only intended for use by generated reflected code. <br /> | | `https://developer.android.com/reference/kotlin/android/renderscript/Script.FieldID!` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#createFieldID(kotlin.Int,%20android.renderscript.Element)(slot: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, e: https://developer.android.com/reference/kotlin/android/renderscript/Element!)` Only to be used by generated reflected classes. <br /> | | `https://developer.android.com/reference/kotlin/android/renderscript/Script.InvokeID!` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#createInvokeID(kotlin.Int)(slot: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Only to be used by generated reflected classes. <br /> | | `https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID!` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#createKernelID(kotlin.Int,%20kotlin.Int,%20android.renderscript.Element,%20android.renderscript.Element)(slot: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, sig: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, ein: https://developer.android.com/reference/kotlin/android/renderscript/Element!, eout: https://developer.android.com/reference/kotlin/android/renderscript/Element!)` Only to be used by generated reflected classes. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#forEach(kotlin.Int,%20android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.FieldPacker)(slot: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, ain: https://developer.android.com/reference/kotlin/android/renderscript/Allocation!, aout: https://developer.android.com/reference/kotlin/android/renderscript/Allocation!, v: https://developer.android.com/reference/kotlin/android/renderscript/FieldPacker!)` Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#forEach(kotlin.Int,%20android.renderscript.Allocation,%20android.renderscript.Allocation,%20android.renderscript.FieldPacker,%20android.renderscript.Script.LaunchOptions)(slot: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, ain: https://developer.android.com/reference/kotlin/android/renderscript/Allocation!, aout: https://developer.android.com/reference/kotlin/android/renderscript/Allocation!, v: https://developer.android.com/reference/kotlin/android/renderscript/FieldPacker!, sc: https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions!)` Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#forEach(kotlin.Int,%20kotlin.Array,%20android.renderscript.Allocation,%20android.renderscript.FieldPacker)(slot: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, ains: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/renderscript/Allocation!>!, aout: https://developer.android.com/reference/kotlin/android/renderscript/Allocation!, v: https://developer.android.com/reference/kotlin/android/renderscript/FieldPacker!)` Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#forEach(kotlin.Int,%20kotlin.Array,%20android.renderscript.Allocation,%20android.renderscript.FieldPacker,%20android.renderscript.Script.LaunchOptions)(slot: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, ains: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/renderscript/Allocation!>!, aout: https://developer.android.com/reference/kotlin/android/renderscript/Allocation!, v: https://developer.android.com/reference/kotlin/android/renderscript/FieldPacker!, sc: https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions!)` Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#getVarB(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#getVarD(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#getVarF(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#getVarI(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#getVarJ(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#getVarV(kotlin.Int,%20android.renderscript.FieldPacker)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, v: https://developer.android.com/reference/kotlin/android/renderscript/FieldPacker!)` Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#invoke(kotlin.Int)(slot: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#invoke(kotlin.Int,%20android.renderscript.FieldPacker)(slot: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, v: https://developer.android.com/reference/kotlin/android/renderscript/FieldPacker!)` Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#reduce(kotlin.Int,%20kotlin.Array,%20android.renderscript.Allocation,%20android.renderscript.Script.LaunchOptions)(slot: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, ains: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/renderscript/Allocation!>!, aout: https://developer.android.com/reference/kotlin/android/renderscript/Allocation!, sc: https://developer.android.com/reference/kotlin/android/renderscript/Script.LaunchOptions!)` Only intended for use by generated reflected code. (General reduction) <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#setTimeZone(kotlin.String)(timeZone: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#setVar(kotlin.Int,%20android.renderscript.BaseObj)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, o: https://developer.android.com/reference/kotlin/android/renderscript/BaseObj!)` Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#setVar(kotlin.Int,%20android.renderscript.FieldPacker)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, v: https://developer.android.com/reference/kotlin/android/renderscript/FieldPacker!)` Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#setVar(kotlin.Int,%20android.renderscript.FieldPacker,%20android.renderscript.Element,%20kotlin.IntArray)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, v: https://developer.android.com/reference/kotlin/android/renderscript/FieldPacker!, e: https://developer.android.com/reference/kotlin/android/renderscript/Element!, dims: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!)` Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#setVar(kotlin.Int,%20kotlin.Boolean)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#setVar(kotlin.Int,%20kotlin.Double)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#setVar(kotlin.Int,%20kotlin.Float)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#setVar(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Only intended for use by generated reflected code. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/Script#setVar(kotlin.Int,%20kotlin.Long)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Only intended for use by generated reflected code. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/renderscript/BaseObj` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#destroy()()` Frees any native resources associated with this object. The primary use is to force immediate cleanup of resources when it is believed the GC will not respond quickly enough. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compare the current BaseObj with another BaseObj for equality. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup. The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded. The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition. The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates. After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded. The `finalize` method is never invoked more than once by a Java virtual machine for any given object. Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#getName()()` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#hashCode()()` Calculates the hash code value for a BaseObj. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#setName(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` setName assigns a name to an object. This object can later be looked up by this name. <br /> | ||

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
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!: |
| `resources` | [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)!: |
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
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!: |

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
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!: |

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
| `rs` | [RenderScript](https://developer.android.com/reference/kotlin/android/renderscript/RenderScript)!: |
