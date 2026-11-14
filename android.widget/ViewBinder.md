# SimpleCursorTreeAdapter.ViewBinder

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewBinder

Kotlin| [Java](../android/widget/SimpleCursorTreeAdapter.ViewBinder.md) 
| --- | --- |

```
interface ViewBinder
```

| [android.widget.SimpleCursorTreeAdapter.ViewBinder](../android/widget/SimpleCursorTreeAdapter.ViewBinder.md) |

This class can be used by external clients of SimpleCursorTreeAdapter to bind values from the Cursor to views. You should use this class to bind values from the Cursor to views that are not directly supported by SimpleCursorTreeAdapter or to change the way binding occurs for views supported by SimpleCursorTreeAdapter.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setViewValue](../android/widget/SimpleCursorTreeAdapter.ViewBinder.md))`(`view:` ` [View](../android.view/View.md)!`, `cursor:` ` [Cursor](../android.database/Cursor.md)!`, `columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Binds the Cursor column defined by the specified index to the specified view. |

## Public methods

### setViewValue

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setViewValue(
    view: View!, 
    cursor: Cursor!, 
    columnIndex: Int
): Boolean
```

Binds the Cursor column defined by the specified index to the specified view. When binding is handled by this ViewBinder, this method must return true. If this method returns false, SimpleCursorTreeAdapter will attempts to handle the binding on its own.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android.view/View.md)!:the view to bind the data to |
| `cursor` | [Cursor](../android.database/Cursor.md)!:the cursor to get the data from |
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the column at which the data can be found in the cursor |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the data was bound to the view, false otherwise |
