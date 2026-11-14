# ScriptGroup

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptGroup

Kotlin| [Java](https://developer.android.com/reference/android/renderscript/ScriptGroup "View this page in Java") 
| --- | --- |

```
class ScriptGroup : BaseObj
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj) ||
| | ↳ | [android.renderscript.ScriptGroup](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup#) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

A group of kernels that are executed together with one execution call as if they were a single kernel

In addition to kernels, a script group may contain invocable functions as well. A script group may take inputs and generate outputs, which are consumed and produced by its member kernels. Inside a script group, outputs from one kernel can be passed to another kernel as inputs. The API disallows cyclic dependencies among kernels in a script group, effectively making it a directed acyclic graph (DAG) of kernels.

Grouping kernels together allows for more efficient execution. For example, runtime and compiler optimization can be applied to reduce computation and communication overhead, and to make better use of the CPU and the GPU.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Binding](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup.Binding) Represents a binding of a value to a global variable in a kernel or invocable function. |
| | [Builder](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup.Builder) Helper class to build a ScriptGroup. |
| | [Builder2](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup.Builder2) The builder class for creating script groups |
| --- | --- |
| | [Closure](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup.Closure) An opaque class for closures |
| | [Future](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup.Future) An opaque class for futures |
| | [Input](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup.Input) An opaque class for script group inputs |
| --- | --- |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup#destroy())`()` Destroy this ScriptGroup and all Closures in it |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup#execute())`()` Execute the ScriptGroup. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [execute](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup#execute(kotlin.Any))`(`vararg` `inputs:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Executes a script group |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInput](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup#setInput(android.renderscript.Script.KernelID,%20android.renderscript.Allocation))`(`s:` ` [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)!`, `a:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Sets an input of the ScriptGroup. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOutput](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup#setOutput(android.renderscript.Script.KernelID,%20android.renderscript.Allocation))`(`s:` ` [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)!`, `a:` ` [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!`)` Sets an output of the ScriptGroup. |

| Inherited functions ||
|---|---|
| From class [BaseObj](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compare the current BaseObj with another BaseObj for equality. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#finalize())`()` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#getName())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#hashCode())`()` <br /> Calculates the hash code value for a BaseObj. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setName](https://developer.android.com/reference/kotlin/android/renderscript/BaseObj#setName(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> setName assigns a name to an object. This object can later be looked up by this name. <br /> | ||

## Public methods

### destroy

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun destroy(): Unit
```

**Deprecated:** *Deprecated in Java.*

Destroy this ScriptGroup and all Closures in it 

### execute

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun execute(): Unit
```

**Deprecated:** *Use #execute instead.*

Execute the ScriptGroup. This will run all the kernels in the ScriptGroup. No internal connection results will be visible after execution of the ScriptGroup. 

### execute

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun execute(vararg inputs: Any!): Array<Any!>!
```

**Deprecated:** *Deprecated in Java.*

Executes a script group

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inputs` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:Values for inputs to the script group, in the order as the inputs are added via [Builder2.addInput](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup.Builder2#addInput()). |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | Outputs of the script group as an array of objects, in the order as futures are passed to [Builder2.create](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup.Builder2#create(kotlin.String,%20android.renderscript.ScriptGroup.Future)). |

### setInput

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInput(
    s: Script.KernelID!, 
    a: Allocation!
): Unit
```

**Deprecated:** *Set arguments to [execute(java.lang.Object...)](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup#execute(kotlin.Any))instead.*

Sets an input of the ScriptGroup. This specifies an Allocation to be used for kernels that require an input Allocation provided from outside of the ScriptGroup.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)!:The ID of the kernel where the allocation should be connected. |
| `a` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The allocation to connect. |

### setOutput

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOutput(
    s: Script.KernelID!, 
    a: Allocation!
): Unit
```

**Deprecated:** *Use return value of [execute(java.lang.Object...)](https://developer.android.com/reference/kotlin/android/renderscript/ScriptGroup#execute(kotlin.Any))instead.*

Sets an output of the ScriptGroup. This specifies an Allocation to be used for the kernels that require an output Allocation visible after the ScriptGroup is executed.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [Script.KernelID](https://developer.android.com/reference/kotlin/android/renderscript/Script.KernelID)!:The ID of the kernel where the allocation should be connected. |
| `a` | [Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation)!:The allocation to connect. |
