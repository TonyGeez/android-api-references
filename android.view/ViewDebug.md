# ViewDebug

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewDebug

Kotlin| [Java](../android/view/ViewDebug.md) 
| --- | --- |

```
open class ViewDebug
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.ViewDebug](../android/view/ViewDebug.md) |

Various debugging/tracing tools related to [View](../android/view/View.md) and the view hierarchy.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [CapturedViewProperty](../android/view/ViewDebug.CapturedViewProperty.md) This annotation can be used to mark fields and methods to be dumped when the view is captured. |
| | [ExportedProperty](../android/view/ViewDebug.ExportedProperty.md) This annotation can be used to mark fields and methods to be dumped by the view server. |
| | [FlagToString](../android/view/ViewDebug.FlagToString.md) Defines a mapping from a flag to a String. |
| --- | --- |
| | [HierarchyTraceType](../android/view/ViewDebug.HierarchyTraceType.md) <br /> |
| | [IntToString](../android/view/ViewDebug.IntToString.md) Defines a mapping from an int value to a String. |
| | [RecyclerTraceType](../android/view/ViewDebug.RecyclerTraceType.md) <br /> |
| --- | --- |

| Constants ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [TRACE_HIERARCHY](../android/view/ViewDebug.md) <br /> |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [TRACE_RECYCLER](../android/view/ViewDebug.md) <br /> |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------|---|
| [ViewDebug](../android/view/ViewDebug.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dumpCapturedView](../android/view/ViewDebug.md))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `view:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Dump view info for id based instrument test generation (and possibly further data analysis). |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startHierarchyTracing](../android/view/ViewDebug.md))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `view:` ` [View](../android/view/View.md)!`)` <br /> |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startRecyclerTracing](../android/view/ViewDebug.md))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `view:` ` [View](../android/view/View.md)!`)` <br /> |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopHierarchyTracing](../android/view/ViewDebug.md))`()` <br /> |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopRecyclerTracing](../android/view/ViewDebug.md))`()` <br /> |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [trace](../android/view/ViewDebug.md))`(`view:` ` [View](../android/view/View.md)!`, `type:` ` [ViewDebug.HierarchyTraceType](../android/view/ViewDebug.HierarchyTraceType.md)!`)` <br /> |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [trace](../android/view/ViewDebug.md))`(`view:` ` [View](../android/view/View.md)!`, `type:` ` [ViewDebug.RecyclerTraceType](../android/view/ViewDebug.RecyclerTraceType.md)!`, `vararg` `parameters:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

## Constants

### TRACE_HIERARCHY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACE_HIERARCHY: Boolean
```

**Deprecated:** *This flag is now unused* 

 Value: false

### TRACE_RECYCLER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACE_RECYCLER: Boolean
```

**Deprecated:** *This flag is now unused* 

 Value: false

## Public constructors

### ViewDebug

```
ViewDebug()
```

## Public methods

### dumpCapturedView

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dumpCapturedView(
    tag: String!, 
    view: Any!
): Unit
```

Dump view info for id based instrument test generation (and possibly further data analysis). The results are dumped to the log.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:for log |
| `view` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:for dump |

### startHierarchyTracing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun startHierarchyTracing(
    prefix: String!, 
    view: View!
): Unit
```

**Deprecated:** *This method is now unused and invoking it is a no-op* 

### startRecyclerTracing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun startRecyclerTracing(
    prefix: String!, 
    view: View!
): Unit
```

**Deprecated:** *This method is now unused and invoking it is a no-op* 

### stopHierarchyTracing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun stopHierarchyTracing(): Unit
```

**Deprecated:** *This method is now unused and invoking it is a no-op* 

### stopRecyclerTracing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun stopRecyclerTracing(): Unit
```

**Deprecated:** *This method is now unused and invoking it is a no-op* 

### trace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun trace(
    view: View!, 
    type: ViewDebug.HierarchyTraceType!
): Unit
```

**Deprecated:** *This method is now unused and invoking it is a no-op* 

### trace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun trace(
    view: View!, 
    type: ViewDebug.RecyclerTraceType!, 
    vararg parameters: Int
): Unit
```

**Deprecated:** *This method is now unused and invoking it is a no-op*
