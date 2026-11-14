# Loader.OnLoadCanceledListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnLoadCanceledListener

Kotlin| [Java](https://developer.android.com/reference/android/content/Loader.OnLoadCanceledListener "View this page in Java") 

```
interface OnLoadCanceledListener<D : Any!>
```

| [android.content.Loader.OnLoadCanceledListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCanceledListener#) |

| **This interface was deprecated in API level 28.**
|
| Use androidx.loader.content.Loader.OnLoadCanceledListener

Interface that is implemented to discover when a Loader has been canceled before it finished loading its data. You do not normally need to implement this yourself; it is used in the implementation of [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) to find out when a Loader it is managing has been canceled so that it can schedule the next Loader. This interface should only be used if a Loader is not being used in conjunction with LoaderManager.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLoadCanceled](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCanceledListener#onLoadCanceled(android.content.Loader))`(`loader:` ` [Loader](https://developer.android.com/reference/kotlin/android/content/Loader)<D>!`)` Called on the thread that created the Loader when the load is canceled. |

## Public methods

### onLoadCanceled

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onLoadCanceled(loader: Loader<D>!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called on the thread that created the Loader when the load is canceled.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------|
| `loader` | [Loader](https://developer.android.com/reference/kotlin/android/content/Loader)\<D\>!:the loader that canceled the load |
