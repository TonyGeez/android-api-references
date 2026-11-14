# Loader.OnLoadCompleteListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnLoadCompleteListener

Kotlin | [Java](../android/content/Loader.OnLoadCompleteListener.md) 
| --- | --- |

```
interface OnLoadCompleteListener<D : Any!>
```

| [android.content.Loader.OnLoadCompleteListener](../android/content/Loader.OnLoadCompleteListener.md) |

| **This interface was deprecated in API level 28.**
|
| Use androidx.loader.content.Loader.OnLoadCompleteListener

Interface that is implemented to discover when a Loader has finished loading its data. You do not normally need to implement this yourself; it is used in the implementation of [android.app.LoaderManager](../android/app/LoaderManager.md) to find out when a Loader it is managing has completed so that this can be reported to its client. This interface should only be used if a Loader is not being used in conjunction with LoaderManager.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLoadComplete](../android/content/Loader.OnLoadCompleteListener.md))`(`loader:` ` [Loader](../android/content/Loader.md)<D>!`, `data:` `D`)` Called on the thread that created the Loader when the load is complete. |

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
| `loader` | [Loader](../android/content/Loader.md)\<D\>!: the loader that completed the load |
| `data` | D: the result of the load |
