# LoaderManager.LoaderCallbacks

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LoaderCallbacks

Kotlin| [Java](https://developer.android.com/reference/android/app/LoaderManager.LoaderCallbacks "View this page in Java") 

```
interface LoaderCallbacks<D : Any!>
```

| [android.app.LoaderManager.LoaderCallbacks](https://developer.android.com/reference/kotlin/android/app/LoaderManager.LoaderCallbacks#) |

| **This interface was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.loader.app.LoaderManager.LoaderCallbacks

Callback interface for a client to interact with the manager.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Loader](https://developer.android.com/reference/kotlin/android/content/Loader.html#)\<D\>! | [onCreateLoader](https://developer.android.com/reference/kotlin/android/app/LoaderManager.LoaderCallbacks#onCreateLoader(kotlin.Int,%20android.os.Bundle))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `args:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Instantiate and return a new Loader for the given ID. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLoadFinished](https://developer.android.com/reference/kotlin/android/app/LoaderManager.LoaderCallbacks#onLoadFinished(android.content.Loader,%20android.app.LoaderManager.LoaderCallbacks.D))`(`loader:` ` [Loader](https://developer.android.com/reference/kotlin/android/content/Loader.html#)<D>!`, `data:` `D`)` Called when a previously created loader has finished its load. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLoaderReset](https://developer.android.com/reference/kotlin/android/app/LoaderManager.LoaderCallbacks#onLoaderReset(android.content.Loader))`(`loader:` ` [Loader](https://developer.android.com/reference/kotlin/android/content/Loader.html#)<D>!`)` Called when a previously created loader is being reset, and thus making its data unavailable. |

## Public methods

### onCreateLoader

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCreateLoader(
    id: Int, 
    args: Bundle!
): Loader<D>!
```

**Deprecated:** *Deprecated in Java.*

Instantiate and return a new Loader for the given ID.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID whose loader is to be created. |
| `args` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:Any arguments supplied by the caller. |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Loader](https://developer.android.com/reference/kotlin/android/content/Loader.html#)<D>! | Return a new Loader instance that is ready to start loading. |

### onLoadFinished

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onLoadFinished(
    loader: Loader<D>!, 
    data: D
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when a previously created loader has finished its load. Note that normally an application is*not* allowed to commit fragment transactions while in this call, since it can happen after an activity's state is saved. See [FragmentManager.openTransaction()](https://developer.android.com/reference/kotlin/android/app/FragmentManager#beginTransaction())for further discussion on this.

This function is guaranteed to be called prior to the release of the last data that was supplied for this Loader. At this point you should remove all use of the old data (since it will be released soon), but should not do your own release of the data since its Loader owns it and will take care of that. The Loader will take care of management of its data so you don't have to. In particular:

- The Loader will monitor for changes to the data, and report them to you through new calls here. You should not monitor the data yourself. For example, if the data is a [android.database.Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) and you place it in a [android.widget.CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter.html#), use the [android.widget.CursorAdapter#CursorAdapter(android.content.Context, * android.database.Cursor, int)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter.html#CursorAdapter(android.content.Context,%20android.database.Cursor,%20kotlin.Int))constructor*without* passing in either [android.widget.CursorAdapter#FLAG_AUTO_REQUERY](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter.html#FLAG_AUTO_REQUERY:kotlin.Int) or [android.widget.CursorAdapter#FLAG_REGISTER_CONTENT_OBSERVER](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter.html#FLAG_REGISTER_CONTENT_OBSERVER:kotlin.Int)(that is, use 0 for the flags argument). This prevents the CursorAdapter from doing its own observing of the Cursor, which is not needed since when a change happens you will get a new Cursor throw another call here.

- The Loader will release the data once it knows the application is no longer using it. For example, if the data is a [android.database.Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) from a [android.content.CursorLoader](https://developer.android.com/reference/kotlin/android/content/CursorLoader.html#), you should not call close() on it yourself. If the Cursor is being placed in a [android.widget.CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter.html#), you should use the [android.widget.CursorAdapter#swapCursor(android.database.Cursor)](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter.html#swapCursor(android.database.Cursor))method so that the old Cursor is not closed.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `loader` | [Loader](https://developer.android.com/reference/kotlin/android/content/Loader.html#)\<D\>!:The Loader that has finished. |
| `data` | D:The data generated by the Loader. |

### onLoaderReset

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onLoaderReset(loader: Loader<D>!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when a previously created loader is being reset, and thus making its data unavailable. The application should at this point remove any references it has to the Loader's data.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------|
| `loader` | [Loader](https://developer.android.com/reference/kotlin/android/content/Loader.html#)\<D\>!:The Loader that is being reset. |
