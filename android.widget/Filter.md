# Filter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Filter

Kotlin| [Java](https://developer.android.com/reference/android/widget/Filter "View this page in Java") 

```
abstract class Filter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.widget.Filter](https://developer.android.com/reference/kotlin/android/widget/Filter#) |

A filter constrains data with a filtering pattern.

Filters are usually created by [android.widget.Filterable](https://developer.android.com/reference/kotlin/android/widget/Filterable) classes.

Filtering operations performed by calling [filter(java.lang.CharSequence)](https://developer.android.com/reference/kotlin/android/widget/Filter#filter(kotlin.CharSequence))or [filter(java.lang.CharSequence,android.widget.Filter.FilterListener)](https://developer.android.com/reference/kotlin/android/widget/Filter#filter(kotlin.CharSequence,%20android.widget.Filter.FilterListener))are performed asynchronously. When these methods are called, a filtering request is posted in a request queue and processed later. Any call to one of these methods will cancel any previous non-executed filtering request.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [FilterListener](https://developer.android.com/reference/kotlin/android/widget/Filter.FilterListener) Listener used to receive a notification upon completion of a filtering operation. |
| open | [FilterResults](https://developer.android.com/reference/kotlin/android/widget/Filter.FilterResults) Holds the results of a filtering operation. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------|---|
| [Filter](https://developer.android.com/reference/kotlin/android/widget/Filter#Filter())`()` Creates a new asynchronous filter. |

| Public methods ||
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [convertResultToString](https://developer.android.com/reference/kotlin/android/widget/Filter#convertResultToString(kotlin.Any))`(`resultValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Converts a value from the filtered set into a CharSequence. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [filter](https://developer.android.com/reference/kotlin/android/widget/Filter#filter(kotlin.CharSequence))`(`constraint:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Starts an asynchronous filtering operation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [filter](https://developer.android.com/reference/kotlin/android/widget/Filter#filter(kotlin.CharSequence,%20android.widget.Filter.FilterListener))`(`constraint:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `listener:` ` [Filter.FilterListener](https://developer.android.com/reference/kotlin/android/widget/Filter.FilterListener)!`)` Starts an asynchronous filtering operation. |

| Protected methods ||
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Filter.FilterResults](https://developer.android.com/reference/kotlin/android/widget/Filter.FilterResults)! | [performFiltering](https://developer.android.com/reference/kotlin/android/widget/Filter#performFiltering(kotlin.CharSequence))`(`constraint:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Invoked in a worker thread to filter the data according to the constraint. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [publishResults](https://developer.android.com/reference/kotlin/android/widget/Filter#publishResults(kotlin.CharSequence,%20android.widget.Filter.FilterResults))`(`constraint:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `results:` ` [Filter.FilterResults](https://developer.android.com/reference/kotlin/android/widget/Filter.FilterResults)!`)` Invoked in the UI thread to publish the filtering results in the user interface. |

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

- [#filter(CharSequence, android.widget.Filter.FilterListener)](https://developer.android.com/reference/kotlin/android/widget/Filter#filter(kotlin.CharSequence,%20android.widget.Filter.FilterListener)) 

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
| `listener` | [Filter.FilterListener](https://developer.android.com/reference/kotlin/android/widget/Filter.FilterListener)!:a listener notified upon completion of the operation |

**See Also**

- [#filter(CharSequence)](https://developer.android.com/reference/kotlin/android/widget/Filter#filter(kotlin.CharSequence))
- [#performFiltering(CharSequence)](https://developer.android.com/reference/kotlin/android/widget/Filter#performFiltering(kotlin.CharSequence))
- [#publishResults(CharSequence, android.widget.Filter.FilterResults)](https://developer.android.com/reference/kotlin/android/widget/Filter#publishResults(kotlin.CharSequence,%20android.widget.Filter.FilterResults))

## Protected methods

### performFiltering

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun performFiltering(constraint: CharSequence!): Filter.FilterResults!
```

Invoked in a worker thread to filter the data according to the constraint. Subclasses must implement this method to perform the filtering operation. Results computed by the filtering operation must be returned as a [android.widget.Filter.FilterResults](https://developer.android.com/reference/kotlin/android/widget/Filter.FilterResults) that will then be published in the UI thread through [publishResults(java.lang.CharSequence,android.widget.Filter.FilterResults)](https://developer.android.com/reference/kotlin/android/widget/Filter#publishResults(kotlin.CharSequence,%20android.widget.Filter.FilterResults)).

**Contract:**When the constraint is null, the original data must be restored.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `constraint` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the constraint used to filter the data |

| Return ||
|-------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [Filter.FilterResults](https://developer.android.com/reference/kotlin/android/widget/Filter.FilterResults)! | the results of the filtering operation |

**See Also**

- [#filter(CharSequence, android.widget.Filter.FilterListener)](https://developer.android.com/reference/kotlin/android/widget/Filter#filter(kotlin.CharSequence,%20android.widget.Filter.FilterListener))
- [#publishResults(CharSequence, android.widget.Filter.FilterResults)](https://developer.android.com/reference/kotlin/android/widget/Filter#publishResults(kotlin.CharSequence,%20android.widget.Filter.FilterResults))
- [android.widget.Filter.FilterResults](https://developer.android.com/reference/kotlin/android/widget/Filter.FilterResults) 

### publishResults

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun publishResults(
    constraint: CharSequence!, 
    results: Filter.FilterResults!
): Unit
```

Invoked in the UI thread to publish the filtering results in the user interface. Subclasses must implement this method to display the results computed in [performFiltering](https://developer.android.com/reference/kotlin/android/widget/Filter#performFiltering(kotlin.CharSequence)).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `constraint` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the constraint used to filter the data |
| `results` | [Filter.FilterResults](https://developer.android.com/reference/kotlin/android/widget/Filter.FilterResults)!:the results of the filtering operation |

**See Also**

- [#filter(CharSequence, android.widget.Filter.FilterListener)](https://developer.android.com/reference/kotlin/android/widget/Filter#filter(kotlin.CharSequence,%20android.widget.Filter.FilterListener))
- [#performFiltering(CharSequence)](https://developer.android.com/reference/kotlin/android/widget/Filter#performFiltering(kotlin.CharSequence))
- [android.widget.Filter.FilterResults](https://developer.android.com/reference/kotlin/android/widget/Filter.FilterResults)
