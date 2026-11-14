# ViewDebug

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewDebug

Kotlin| [Java](https://developer.android.com/reference/android/view/ViewDebug "View this page in Java") 
| --- | --- |

```
open class ViewDebug
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.ViewDebug](https://developer.android.com/reference/kotlin/android/view/ViewDebug#) |

Various debugging/tracing tools related to [View](https://developer.android.com/reference/kotlin/android/view/View) and the view hierarchy.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [CapturedViewProperty](https://developer.android.com/reference/kotlin/android/view/ViewDebug.CapturedViewProperty) This annotation can be used to mark fields and methods to be dumped when the view is captured. |
| | [ExportedProperty](https://developer.android.com/reference/kotlin/android/view/ViewDebug.ExportedProperty) This annotation can be used to mark fields and methods to be dumped by the view server. |
| | [FlagToString](https://developer.android.com/reference/kotlin/android/view/ViewDebug.FlagToString) Defines a mapping from a flag to a String. |
| --- | --- |
| | [HierarchyTraceType](https://developer.android.com/reference/kotlin/android/view/ViewDebug.HierarchyTraceType) <br /> |
| | [IntToString](https://developer.android.com/reference/kotlin/android/view/ViewDebug.IntToString) Defines a mapping from an int value to a String. |
| | [RecyclerTraceType](https://developer.android.com/reference/kotlin/android/view/ViewDebug.RecyclerTraceType) <br /> |
| --- | --- |

| Constants ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [TRACE_HIERARCHY](https://developer.android.com/reference/kotlin/android/view/ViewDebug#TRACE_HIERARCHY:kotlin.Boolean) <br /> |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [TRACE_RECYCLER](https://developer.android.com/reference/kotlin/android/view/ViewDebug#TRACE_RECYCLER:kotlin.Boolean) <br /> |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------|---|
| [ViewDebug](https://developer.android.com/reference/kotlin/android/view/ViewDebug#ViewDebug())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dumpCapturedView](https://developer.android.com/reference/kotlin/android/view/ViewDebug#dumpCapturedView(kotlin.String,%20kotlin.Any))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `view:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Dump view info for id based instrument test generation (and possibly further data analysis). |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startHierarchyTracing](https://developer.android.com/reference/kotlin/android/view/ViewDebug#startHierarchyTracing(kotlin.String,%20android.view.View))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`)` <br /> |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startRecyclerTracing](https://developer.android.com/reference/kotlin/android/view/ViewDebug#startRecyclerTracing(kotlin.String,%20android.view.View))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`)` <br /> |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopHierarchyTracing](https://developer.android.com/reference/kotlin/android/view/ViewDebug#stopHierarchyTracing())`()` <br /> |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopRecyclerTracing](https://developer.android.com/reference/kotlin/android/view/ViewDebug#stopRecyclerTracing())`()` <br /> |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [trace](https://developer.android.com/reference/kotlin/android/view/ViewDebug#trace(android.view.View,%20android.view.ViewDebug.HierarchyTraceType))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `type:` ` [ViewDebug.HierarchyTraceType](https://developer.android.com/reference/kotlin/android/view/ViewDebug.HierarchyTraceType)!`)` <br /> |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [trace](https://developer.android.com/reference/kotlin/android/view/ViewDebug#trace(android.view.View,%20android.view.ViewDebug.RecyclerTraceType,%20kotlin.Int))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `type:` ` [ViewDebug.RecyclerTraceType](https://developer.android.com/reference/kotlin/android/view/ViewDebug.RecyclerTraceType)!`, `vararg` `parameters:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

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
