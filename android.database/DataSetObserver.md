# DataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataSetObserver

Kotlin| [Java](../android/database/DataSetObserver.md) 
| --- | --- |

```
abstract class DataSetObserver
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.database.DataSetObserver](../android/database/DataSetObserver.md) |

| Known Direct Subclasses [AlphabetIndexer](../android/widget/AlphabetIndexer.md) |--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------| | [AlphabetIndexer](../android/widget/AlphabetIndexer.md) | A helper class for adapters that implement the SectionIndexer interface. | |
| --- | --- | --- | --- | --- | --- | --- |

Receives call backs when a data set has been changed, or made invalid. The typically data sets that are observed are [Cursor](../android/database/Cursor.md) s or [android.widget.Adapter](../android/widget/Adapter.md) s. DataSetObserver must be implemented by objects which are added to a DataSetObservable.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------|---|
| [DataSetObserver](../android/database/DataSetObserver.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onChanged](../android/database/DataSetObserver.md))`()` This method is called when the entire data set has changed, most likely through a call to [Cursor.requery()](../android/database/Cursor.md))on a [Cursor](../android/database/Cursor.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInvalidated](../android/database/DataSetObserver.md))`()` This method is called when the entire data becomes invalid, most likely through a call to [Cursor.deactivate()](../android/database/Cursor.md))or android. |

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

This method is called when the entire data set has changed, most likely through a call to [Cursor.requery()](../android/database/Cursor.md))on a [Cursor](../android/database/Cursor.md). 

### onInvalidated

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onInvalidated(): Unit
```

This method is called when the entire data becomes invalid, most likely through a call to [Cursor.deactivate()](../android/database/Cursor.md))or android.database.Cursor#close() on a [Cursor](../android/database/Cursor.md).
