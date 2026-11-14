# LoaderManager

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LoaderManager

Kotlin| [Java](https://developer.android.com/reference/android/app/LoaderManager "View this page in Java") 
| --- | --- |

```
abstract class LoaderManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager#) |

| **This class was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.loader.app.LoaderManager

Interface associated with an [Activity](https://developer.android.com/reference/kotlin/android/app/Activity) or [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment) for managing one or more [android.content.Loader](https://developer.android.com/reference/kotlin/android/content/Loader.html#) instances associated with it. This helps an application manage longer-running operations in conjunction with the Activity or Fragment lifecycle; the most common use of this is with a [android.content.CursorLoader](https://developer.android.com/reference/kotlin/android/content/CursorLoader.html#), however applications are free to write their own loaders for loading other types of data. While the LoaderManager API was introduced in [android.os.Build.VERSION_CODES#HONEYCOMB](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int), a version of the API at is also available for use on older platforms through androidx.fragment.app.FragmentActivity. See the blog post [Fragments For All](http://android-developers.blogspot.com/2011/03/fragments-for-all.html) for more details.

As an example, here is the full implementation of a [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment) that displays a [android.widget.ListView](https://developer.android.com/reference/kotlin/android/widget/ListView.html#) containing the results of a query against the contacts content provider. It uses a [android.content.CursorLoader](https://developer.android.com/reference/kotlin/android/content/CursorLoader.html#) to manage the query on the provider.
|
| ### Developer Guides
|
| For more information about using loaders, read the [Loaders](https://developer.android.com/guide/topics/fundamentals/loaders.html) developer guide.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [LoaderCallbacks](https://developer.android.com/reference/kotlin/android/app/LoaderManager.LoaderCallbacks) Callback interface for a client to interact with the manager. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------|---|
| [LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager#LoaderManager())`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroyLoader](https://developer.android.com/reference/kotlin/android/app/LoaderManager#destroyLoader(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Stops and removes the loader with the given ID. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/app/LoaderManager#dump(kotlin.String,%20java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!`, `writer:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Print the LoaderManager's state into the given stream. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [enableDebugLogging](https://developer.android.com/reference/kotlin/android/app/LoaderManager#enableDebugLogging(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Control whether the framework's internal loader manager debugging logs are turned on. |
| --- | --- |
| abstract [Loader](https://developer.android.com/reference/kotlin/android/content/Loader.html#)\<D\>! | [getLoader](https://developer.android.com/reference/kotlin/android/app/LoaderManager#getLoader(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the Loader with the given id or null if no matching Loader is found. |
| abstract [Loader](https://developer.android.com/reference/kotlin/android/content/Loader.html#)\<D\>! | [initLoader](https://developer.android.com/reference/kotlin/android/app/LoaderManager#initLoader(kotlin.Int,%20android.os.Bundle,%20android.app.LoaderManager.LoaderCallbacks))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `args:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`, `callback:` ` [LoaderManager.LoaderCallbacks](https://developer.android.com/reference/kotlin/android/app/LoaderManager.LoaderCallbacks)<D>!`)` Ensures a loader is initialized and active. |
| abstract [Loader](https://developer.android.com/reference/kotlin/android/content/Loader.html#)\<D\>! | [restartLoader](https://developer.android.com/reference/kotlin/android/app/LoaderManager#restartLoader(kotlin.Int,%20android.os.Bundle,%20android.app.LoaderManager.LoaderCallbacks))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `args:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`, `callback:` ` [LoaderManager.LoaderCallbacks](https://developer.android.com/reference/kotlin/android/app/LoaderManager.LoaderCallbacks)<D>!`)` Starts a new or restarts an existing [android.content.Loader](https://developer.android.com/reference/kotlin/android/content/Loader.html#) in this manager, registers the callbacks to it, and (if the activity/fragment is currently started) starts loading it. |
| --- | --- |

## Public constructors

### LoaderManager

```
LoaderManager()
```

## Public methods

### destroyLoader

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun destroyLoader(id: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Stops and removes the loader with the given ID. If this loader had previously reported data to the client through [LoaderCallbacks.onLoadFinished(Loader, Object)](https://developer.android.com/reference/kotlin/android/app/LoaderManager.LoaderCallbacks#onLoadFinished(android.content.Loader,%20android.app.LoaderManager.LoaderCallbacks.D)), a call will be made to [LoaderCallbacks.onLoaderReset(Loader)](https://developer.android.com/reference/kotlin/android/app/LoaderManager.LoaderCallbacks#onLoaderReset(android.content.Loader)). 

### dump

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun dump(
    prefix: String!, 
    fd: FileDescriptor!, 
    writer: PrintWriter!, 
    args: Array<String!>!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Print the LoaderManager's state into the given stream.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Text to print at the front of each line. |
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!:The raw file descriptor that the dump is being sent to. |
| `writer` | [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!:A PrintWriter to which the dump is to be set. |
| --- | --- |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Additional arguments to the dump request. |

### enableDebugLogging

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun enableDebugLogging(enabled: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Control whether the framework's internal loader manager debugging logs are turned on. If enabled, you will see output in logcat as the framework performs loader operations. 

### getLoader

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <D : Any!> getLoader(id: Int): Loader<D>!
```

**Deprecated:** *Deprecated in Java.*

Return the Loader with the given id or null if no matching Loader is found. 

### initLoader

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <D : Any!> initLoader(
    id: Int, 
    args: Bundle!, 
    callback: LoaderManager.LoaderCallbacks<D>!
): Loader<D>!
```

**Deprecated:** *Deprecated in Java.*

Ensures a loader is initialized and active. If the loader doesn't already exist, one is created and (if the activity/fragment is currently started) starts the loader. Otherwise the last created loader is re-used.

In either case, the given callback is associated with the loader, and will be called as the loader state changes. If at the point of call the caller is in its started state, and the requested loader already exists and has generated its data, then callback [LoaderCallbacks.onLoadFinished](https://developer.android.com/reference/kotlin/android/app/LoaderManager.LoaderCallbacks#onLoadFinished(android.content.Loader,%20android.app.LoaderManager.LoaderCallbacks.D))will be called immediately (inside of this function), so you must be prepared for this to happen.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A unique identifier for this loader. Can be whatever you want. Identifiers are scoped to a particular LoaderManager instance. |
| `args` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:Optional arguments to supply to the loader at construction. If a loader already exists (a new one does not need to be created), this parameter will be ignored and the last arguments continue to be used. |
| `callback` | [LoaderManager.LoaderCallbacks](https://developer.android.com/reference/kotlin/android/app/LoaderManager.LoaderCallbacks)\<D\>!:Interface the LoaderManager will call to report about changes in the state of the loader. Required. |
| --- | --- |

### restartLoader

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <D : Any!> restartLoader(
    id: Int, 
    args: Bundle!, 
    callback: LoaderManager.LoaderCallbacks<D>!
): Loader<D>!
```

**Deprecated:** *Deprecated in Java.*

Starts a new or restarts an existing [android.content.Loader](https://developer.android.com/reference/kotlin/android/content/Loader.html#) in this manager, registers the callbacks to it, and (if the activity/fragment is currently started) starts loading it. If a loader with the same id has previously been started it will automatically be destroyed when the new loader completes its work. The callback will be delivered before the old loader is destroyed.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A unique identifier for this loader. Can be whatever you want. Identifiers are scoped to a particular LoaderManager instance. |
| `args` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:Optional arguments to supply to the loader at construction. |
| `callback` | [LoaderManager.LoaderCallbacks](https://developer.android.com/reference/kotlin/android/app/LoaderManager.LoaderCallbacks)\<D\>!:Interface the LoaderManager will call to report about changes in the state of the loader. Required. |
| --- | --- |
