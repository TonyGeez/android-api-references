# ScriptGroup

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScriptGroup

Kotlin| [Java](ScriptGroup.md) 
| --- | --- |

```
class ScriptGroup : BaseObj
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.renderscript.BaseObj](BaseObj.md) ||
| | ↳ | [android.renderscript.ScriptGroup](ScriptGroup.md) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

A group of kernels that are executed together with one execution call as if they were a single kernel

In addition to kernels, a script group may contain invocable functions as well. A script group may take inputs and generate outputs, which are consumed and produced by its member kernels. Inside a script group, outputs from one kernel can be passed to another kernel as inputs. The API disallows cyclic dependencies among kernels in a script group, effectively making it a directed acyclic graph (DAG) of kernels.

Grouping kernels together allows for more efficient execution. For example, runtime and compiler optimization can be applied to reduce computation and communication overhead, and to make better use of the CPU and the GPU.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Binding](../android/renderscript/ScriptGroup.Binding.md) Represents a binding of a value to a global variable in a kernel or invocable function. |
| | [Builder](../android/renderscript/ScriptGroup.Builder.md) Helper class to build a ScriptGroup. |
| | [Builder2](../android/renderscript/ScriptGroup.Builder2.md) The builder class for creating script groups |
| --- | --- |
| | [Closure](../android/renderscript/ScriptGroup.Closure.md) An opaque class for closures |
| | [Future](../android/renderscript/ScriptGroup.Future.md) An opaque class for futures |
| | [Input](../android/renderscript/ScriptGroup.Input.md) An opaque class for script group inputs |
| --- | --- |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](ScriptGroup.md))`()` Destroy this ScriptGroup and all Closures in it |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](ScriptGroup.md))`()` Execute the ScriptGroup. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [execute](ScriptGroup.md))`(`vararg` `inputs:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Executes a script group |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInput](ScriptGroup.md))`(`s:` ` [Script.KernelID](../android/renderscript/Script.KernelID.md)!`, `a:` ` [Allocation](Allocation.md)!`)` Sets an input of the ScriptGroup. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOutput](ScriptGroup.md))`(`s:` ` [Script.KernelID](../android/renderscript/Script.KernelID.md)!`, `a:` ` [Allocation](Allocation.md)!`)` Sets an output of the ScriptGroup. |

| Inherited functions ||
|---|---|
| From class [BaseObj](BaseObj.md) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](BaseObj.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compare the current BaseObj with another BaseObj for equality. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](BaseObj.md))`()` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](BaseObj.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](BaseObj.md))`()` <br /> Calculates the hash code value for a BaseObj. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setName](BaseObj.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> setName assigns a name to an object. This object can later be looked up by this name. <br /> | ||

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
| `inputs` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:Values for inputs to the script group, in the order as the inputs are added via [Builder2.addInput](../android/renderscript/ScriptGroup.Builder2.md)). |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | Outputs of the script group as an array of objects, in the order as futures are passed to [Builder2.create](../android/renderscript/ScriptGroup.Builder2.md)). |

### setInput

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInput(
    s: Script.KernelID!, 
    a: Allocation!
): Unit
```

**Deprecated:** *Set arguments to [execute(java.lang.Object...)](ScriptGroup.md))instead.*

Sets an input of the ScriptGroup. This specifies an Allocation to be used for kernels that require an input Allocation provided from outside of the ScriptGroup.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [Script.KernelID](../android/renderscript/Script.KernelID.md)!:The ID of the kernel where the allocation should be connected. |
| `a` | [Allocation](Allocation.md)!:The allocation to connect. |

### setOutput

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOutput(
    s: Script.KernelID!, 
    a: Allocation!
): Unit
```

**Deprecated:** *Use return value of [execute(java.lang.Object...)](ScriptGroup.md))instead.*

Sets an output of the ScriptGroup. This specifies an Allocation to be used for the kernels that require an output Allocation visible after the ScriptGroup is executed.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [Script.KernelID](../android/renderscript/Script.KernelID.md)!:The ID of the kernel where the allocation should be connected. |
| `a` | [Allocation](Allocation.md)!:The allocation to connect. |
