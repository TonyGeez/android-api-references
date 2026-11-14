# DebugUtils

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DebugUtils

Kotlin| [Java](../android/util/DebugUtils.md) 
| --- | --- |

```
open class DebugUtils
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.DebugUtils](../android/util/DebugUtils.md) |

Various utilities for debugging and logging.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isObjectSelected](../android/util/DebugUtils.md))`(`object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Filters objects against the`ANDROID_OBJECT_FILTER`environment variable. |

## Public methods

### isObjectSelected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isObjectSelected(object: Any!): Boolean
```

Filters objects against the`ANDROID_OBJECT_FILTER`environment variable. This environment variable can filter objects based on their class name and attribute values.

Here is the syntax for`ANDROID_OBJECT_FILTER`:

`ClassName@attribute1=value1@attribute2=value2...`

Examples:

- Select TextView instances:`TextView`
- Select TextView instances of text "Loading" and bottom offset of 22:`TextView@text=Loading.*@bottom=22`

The class name and the values are regular expressions.

This class is useful for debugging and logging purpose: 

```kotlin
if (DEBUG) {
    if (DebugUtils.isObjectSelected(childView) && LOGV_ENABLED) {
      Log.v(TAG, "Object " + childView + " logged!");
    }
  }
  
```

**NOTE**: This method is very expensive as it relies heavily on regular expressions and reflection. Calls to this method should always be stripped out of the release binaries and avoided as much as possible in debug mode.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `object` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:any object to match against the ANDROID_OBJECT_FILTER environement variable |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if object is selected by the ANDROID_OBJECT_FILTER environment variable, false otherwise |
