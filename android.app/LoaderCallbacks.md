# LoaderManager.LoaderCallbacks

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LoaderCallbacks

Kotlin| [Java](../android/app/LoaderManager.LoaderCallbacks.md) 
| --- | --- |

```
interface LoaderCallbacks<D : Any!>
```

| [android.app.LoaderManager.LoaderCallbacks](../android/app/LoaderManager.LoaderCallbacks.md) |

| **This interface was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.loader.app.LoaderManager.LoaderCallbacks

Callback interface for a client to interact with the manager.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Loader](../android.content/Loader.md)\<D\>! | [onCreateLoader](../android/app/LoaderManager.LoaderCallbacks.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `args:` ` [Bundle](../android.os/Bundle.md)!`)` Instantiate and return a new Loader for the given ID. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLoadFinished](../android/app/LoaderManager.LoaderCallbacks.md))`(`loader:` ` [Loader](../android.content/Loader.md)<D>!`, `data:` `D`)` Called when a previously created loader has finished its load. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLoaderReset](../android/app/LoaderManager.LoaderCallbacks.md))`(`loader:` ` [Loader](../android.content/Loader.md)<D>!`)` Called when a previously created loader is being reset, and thus making its data unavailable. |
| --- | --- |

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
| `args` | [Bundle](../android.os/Bundle.md)!:Any arguments supplied by the caller. |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Loader](../android.content/Loader.md)<D>! | Return a new Loader instance that is ready to start loading. |

### onLoadFinished

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onLoadFinished(
    loader: Loader<D>!, 
    data: D
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when a previously created loader has finished its load. Note that normally an application is*not* allowed to commit fragment transactions while in this call, since it can happen after an activity's state is saved. See [FragmentManager.openTransaction()](FragmentManager.md))for further discussion on this.

This function is guaranteed to be called prior to the release of the last data that was supplied for this Loader. At this point you should remove all use of the old data (since it will be released soon), but should not do your own release of the data since its Loader owns it and will take care of that. The Loader will take care of management of its data so you don't have to. In particular:

- The Loader will monitor for changes to the data, and report them to you through new calls here. You should not monitor the data yourself. For example, if the data is a [android.database.Cursor](../android.database/Cursor.md) and you place it in a [android.widget.CursorAdapter](../android.widget/CursorAdapter.md), use the [android.widget.CursorAdapter#CursorAdapter(android.content.Context, * android.database.Cursor, int)](../android.widget/CursorAdapter.md))constructor*without* passing in either [android.widget.CursorAdapter#FLAG_AUTO_REQUERY](../android.widget/CursorAdapter.md) or [android.widget.CursorAdapter#FLAG_REGISTER_CONTENT_OBSERVER](../android.widget/CursorAdapter.md)(that is, use 0 for the flags argument). This prevents the CursorAdapter from doing its own observing of the Cursor, which is not needed since when a change happens you will get a new Cursor throw another call here.

- The Loader will release the data once it knows the application is no longer using it. For example, if the data is a [android.database.Cursor](../android.database/Cursor.md) from a [android.content.CursorLoader](../android.content/CursorLoader.md), you should not call close() on it yourself. If the Cursor is being placed in a [android.widget.CursorAdapter](../android.widget/CursorAdapter.md), you should use the [android.widget.CursorAdapter#swapCursor(android.database.Cursor)](../android.widget/CursorAdapter.md))method so that the old Cursor is not closed.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `loader` | [Loader](../android.content/Loader.md)\<D\>!:The Loader that has finished. |
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
| `loader` | [Loader](../android.content/Loader.md)\<D\>!:The Loader that is being reset. |
