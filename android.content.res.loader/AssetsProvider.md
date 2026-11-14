Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AssetsProvider

Kotlin | [Java](AssetsProvider.md)
| --- | --- |

```
interface AssetsProvider
```

| [android.content.res.loader.AssetsProvider](AssetsProvider.md) |

Provides callbacks that allow for the value of a file-based resources or assets of a `https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesProvider` to be specified or overridden.

## Summary

| Public methods ||
|---|---|
| open [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)? | `https://developer.android.com/reference/kotlin/android/content/res/loader/AssetsProvider#loadAssetFd(kotlin.String,%20kotlin.Int)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, accessMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback that allows the value of a file-based resources or asset to be specified or overridden. |

## Public methods

### loadAssetFd

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadAssetFd(
    path: String, 
    accessMode: Int
): AssetFileDescriptor?
```

Callback that allows the value of a file-based resources or asset to be specified or overridden.

The system will take ownership of the file descriptor returned from this method, so `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#dup()` the file descriptor before returning if the system should not own it.

There are two situations in which this method will be called:

- AssetManager is queried for an InputStream of an asset using APIs like android.content.res.AssetManager#open and android.content.res.AssetManager#openXmlResourceParser.
- AssetManager is resolving the value of a file-based resource provided by the `https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesProvider` this instance is associated with.

If the value retrieved from this callback is null, AssetManager will attempt to find the file-based resource or asset within the APK provided by the ResourcesProvider this instance is associated with.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the asset path being loaded. This value cannot be `null`. |
| `accessMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the `https://developer.android.com/reference/kotlin/android/content/res/AssetManager.html#` access mode |

**See Also**
