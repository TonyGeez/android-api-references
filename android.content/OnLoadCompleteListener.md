# Loader.OnLoadCompleteListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnLoadCompleteListener

Kotlin | [Java](https://developer.android.com/reference/android/content/Loader.OnLoadCompleteListener "View this page in Java") 
| --- | --- |

```
interface OnLoadCompleteListener<D : Any!>
```

| [android.content.Loader.OnLoadCompleteListener](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCompleteListener#) |

| **This interface was deprecated in API level 28.**
|
| Use androidx.loader.content.Loader.OnLoadCompleteListener

Interface that is implemented to discover when a Loader has finished loading its data. You do not normally need to implement this yourself; it is used in the implementation of [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager.html#) to find out when a Loader it is managing has completed so that this can be reported to its client. This interface should only be used if a Loader is not being used in conjunction with LoaderManager.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLoadComplete](https://developer.android.com/reference/kotlin/android/content/Loader.OnLoadCompleteListener#onLoadComplete(android.content.Loader,%20android.content.Loader.OnLoadCompleteListener.D))`(`loader:` ` [Loader](https://developer.android.com/reference/kotlin/android/content/Loader)<D>!`, `data:` `D`)` Called on the thread that created the Loader when the load is complete. |

## Public methods

### onLoadComplete

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onLoadComplete(
    loader: Loader<D>!, 
    data: D
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called on the thread that created the Loader when the load is complete.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `loader` | [Loader](https://developer.android.com/reference/kotlin/android/content/Loader)\<D\>!: the loader that completed the load |
| `data` | D: the result of the load |
