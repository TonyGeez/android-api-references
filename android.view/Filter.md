# LayoutInflater.Filter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Filter

Kotlin| [Java](../android/view/LayoutInflater.Filter.md) 
| --- | --- |

```
interface Filter
```

| [android.view.LayoutInflater.Filter](../android/view/LayoutInflater.Filter.md) |

| Known Direct Subclasses [RemoteViews](../android.widget/RemoteViews.md) |------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------| | [RemoteViews](../android.widget/RemoteViews.md) | A class that describes a view hierarchy that can be displayed in another process. | |
| --- | --- | --- | --- | --- | --- | --- |

Hook to allow clients of the LayoutInflater to restrict the set of Views that are allowed to be inflated.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLoadClass](../android/view/LayoutInflater.Filter.md))`(`clazz:` ` [Class](../java.lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Hook to allow clients of the LayoutInflater to restrict the set of Views that are allowed to be inflated. |

## Public methods

### onLoadClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onLoadClass(clazz: Class<Any!>!): Boolean
```

Hook to allow clients of the LayoutInflater to restrict the set of Views that are allowed to be inflated.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `clazz` | [Class](../java.lang/Class.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:The class object for the View that is about to be inflated |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this class is allowed to be inflated, or false otherwise |
