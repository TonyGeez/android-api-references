# DataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataSetObserver

Kotlin| [Java](https://developer.android.com/reference/android/database/DataSetObserver "View this page in Java") 

```
abstract class DataSetObserver
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.database.DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver#) |

| Known Direct Subclasses [AlphabetIndexer](https://developer.android.com/reference/kotlin/android/widget/AlphabetIndexer.html#) |--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------| | [AlphabetIndexer](https://developer.android.com/reference/kotlin/android/widget/AlphabetIndexer.html#) | A helper class for adapters that implement the SectionIndexer interface. | |

Receives call backs when a data set has been changed, or made invalid. The typically data sets that are observed are [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor) s or [android.widget.Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter.html#) s. DataSetObserver must be implemented by objects which are added to a DataSetObservable.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------|---|
| [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver#DataSetObserver())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onChanged](https://developer.android.com/reference/kotlin/android/database/DataSetObserver#onChanged())`()` This method is called when the entire data set has changed, most likely through a call to [Cursor.requery()](https://developer.android.com/reference/kotlin/android/database/Cursor#requery())on a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInvalidated](https://developer.android.com/reference/kotlin/android/database/DataSetObserver#onInvalidated())`()` This method is called when the entire data becomes invalid, most likely through a call to [Cursor.deactivate()](https://developer.android.com/reference/kotlin/android/database/Cursor#deactivate())or android. |

## Public constructors

### DataSetObserver

```
DataSetObserver()
```

## Public methods

### onChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onChanged(): Unit
```

This method is called when the entire data set has changed, most likely through a call to [Cursor.requery()](https://developer.android.com/reference/kotlin/android/database/Cursor#requery())on a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor). 

### onInvalidated

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onInvalidated(): Unit
```

This method is called when the entire data becomes invalid, most likely through a call to [Cursor.deactivate()](https://developer.android.com/reference/kotlin/android/database/Cursor#deactivate())or android.database.Cursor#close() on a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor).
