# LayoutInflater.Filter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Filter

Kotlin| [Java](https://developer.android.com/reference/android/view/LayoutInflater.Filter "View this page in Java") 

```
interface Filter
```

| [android.view.LayoutInflater.Filter](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Filter#) |

| Known Direct Subclasses [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#) |------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------| | [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#) | A class that describes a view hierarchy that can be displayed in another process. | |

Hook to allow clients of the LayoutInflater to restrict the set of Views that are allowed to be inflated.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLoadClass](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Filter#onLoadClass(java.lang.Class))`(`clazz:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Hook to allow clients of the LayoutInflater to restrict the set of Views that are allowed to be inflated. |

## Public methods

### onLoadClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onLoadClass(clazz: Class<Any!>!): Boolean
```

Hook to allow clients of the LayoutInflater to restrict the set of Views that are allowed to be inflated.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `clazz` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:The class object for the View that is about to be inflated |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this class is allowed to be inflated, or false otherwise |
