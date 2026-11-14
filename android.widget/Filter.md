# Filter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Filter

Kotlin| [Java](../android/widget/Filter.md) 
| --- | --- |

```
abstract class Filter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.Filter](../android/widget/Filter.md) |

A filter constrains data with a filtering pattern.

Filters are usually created by [android.widget.Filterable](../android/widget/Filterable.md) classes.

Filtering operations performed by calling [filter(java.lang.CharSequence)](../android/widget/Filter.md))or [filter(java.lang.CharSequence,android.widget.Filter.FilterListener)](../android/widget/Filter.md))are performed asynchronously. When these methods are called, a filtering request is posted in a request queue and processed later. Any call to one of these methods will cancel any previous non-executed filtering request.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [FilterListener](../android/widget/Filter.FilterListener.md) Listener used to receive a notification upon completion of a filtering operation. |
| open | [FilterResults](../android/widget/Filter.FilterResults.md) Holds the results of a filtering operation. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------|---|
| [Filter](../android/widget/Filter.md))`()` Creates a new asynchronous filter. |

| Public methods ||
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [convertResultToString](../android/widget/Filter.md))`(`resultValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Converts a value from the filtered set into a CharSequence. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [filter](../android/widget/Filter.md))`(`constraint:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Starts an asynchronous filtering operation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [filter](../android/widget/Filter.md))`(`constraint:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `listener:` ` [Filter.FilterListener](../android/widget/Filter.FilterListener.md)!`)` Starts an asynchronous filtering operation. |
| --- | --- |

| Protected methods ||
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Filter.FilterResults](../android/widget/Filter.FilterResults.md)! | [performFiltering](../android/widget/Filter.md))`(`constraint:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Invoked in a worker thread to filter the data according to the constraint. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [publishResults](../android/widget/Filter.md))`(`constraint:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `results:` ` [Filter.FilterResults](../android/widget/Filter.FilterResults.md)!`)` Invoked in the UI thread to publish the filtering results in the user interface. |

## Public constructors

### Filter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Filter()
```

Creates a new asynchronous filter.

## Public methods

### convertResultToString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun convertResultToString(resultValue: Any!): CharSequence!
```

Converts a value from the filtered set into a CharSequence. Subclasses should override this method to convert their results. The default implementation returns an empty String for null values or the default String representation of the value.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------|
| `resultValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the value to convert to a CharSequence |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | a CharSequence representing the value |

### filter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun filter(constraint: CharSequence!): Unit
```

Starts an asynchronous filtering operation. Calling this method cancels all previous non-executed filtering requests and posts a new filtering request that will be executed later.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `constraint` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the constraint used to filter the data |

**See Also**

- [#filter(CharSequence, android.widget.Filter.FilterListener)](../android/widget/Filter.md)) 

### filter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun filter(
    constraint: CharSequence!, 
    listener: Filter.FilterListener!
): Unit
```

Starts an asynchronous filtering operation. Calling this method cancels all previous non-executed filtering requests and posts a new filtering request that will be executed later.

Upon completion, the listener is notified.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `constraint` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the constraint used to filter the data |
| `listener` | [Filter.FilterListener](../android/widget/Filter.FilterListener.md)!:a listener notified upon completion of the operation |

**See Also**

- [#filter(CharSequence)](../android/widget/Filter.md))
- [#performFiltering(CharSequence)](../android/widget/Filter.md))
- [#publishResults(CharSequence, android.widget.Filter.FilterResults)](../android/widget/Filter.md))

## Protected methods

### performFiltering

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun performFiltering(constraint: CharSequence!): Filter.FilterResults!
```

Invoked in a worker thread to filter the data according to the constraint. Subclasses must implement this method to perform the filtering operation. Results computed by the filtering operation must be returned as a [android.widget.Filter.FilterResults](../android/widget/Filter.FilterResults.md) that will then be published in the UI thread through [publishResults(java.lang.CharSequence,android.widget.Filter.FilterResults)](../android/widget/Filter.md)).

**Contract:**When the constraint is null, the original data must be restored.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `constraint` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the constraint used to filter the data |

| Return ||
|-------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [Filter.FilterResults](../android/widget/Filter.FilterResults.md)! | the results of the filtering operation |

**See Also**

- [#filter(CharSequence, android.widget.Filter.FilterListener)](../android/widget/Filter.md))
- [#publishResults(CharSequence, android.widget.Filter.FilterResults)](../android/widget/Filter.md))
- [android.widget.Filter.FilterResults](../android/widget/Filter.FilterResults.md) 

### publishResults

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun publishResults(
    constraint: CharSequence!, 
    results: Filter.FilterResults!
): Unit
```

Invoked in the UI thread to publish the filtering results in the user interface. Subclasses must implement this method to display the results computed in [performFiltering](../android/widget/Filter.md)).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `constraint` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the constraint used to filter the data |
| `results` | [Filter.FilterResults](../android/widget/Filter.FilterResults.md)!:the results of the filtering operation |

**See Also**

- [#filter(CharSequence, android.widget.Filter.FilterListener)](../android/widget/Filter.md))
- [#performFiltering(CharSequence)](../android/widget/Filter.md))
- [android.widget.Filter.FilterResults](../android/widget/Filter.FilterResults.md)
