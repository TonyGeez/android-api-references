Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResourcesProvider

```
open class ResourcesProvider : AutoCloseable, Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.res.loader.ResourcesProvider](ResourcesProvider.md) |

Provides methods to load resources data from APKs (`.apk`) and resources tables (eg. `resources.arsc`) for use with ResourcesLoader.

## Summary

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | close Frees internal data structures. |
| open static [ResourcesProvider](ResourcesProvider.md) | empty Creates an empty ResourcesProvider with no resource data. |
| open static [ResourcesProvider](ResourcesProvider.md) | loadFromApk Creates a ResourcesProvider from an APK (`.apk`) file descriptor. |
| --- | --- |
| open static [ResourcesProvider](ResourcesProvider.md) | loadFromApk Creates a ResourcesProvider from an APK (`.apk`) file descriptor. |
| open static [ResourcesProvider](ResourcesProvider.md) | loadFromDirectory Creates a ResourcesProvider from a directory path. |
| open static [ResourcesProvider](ResourcesProvider.md) | loadFromSplit Read from a split installed alongside the application, which may not have been loaded initially because the application requested isolated split loading. |
| --- | --- |
| open static [ResourcesProvider](ResourcesProvider.md) | loadFromTable Creates a ResourcesProvider from a resources table (`.arsc`) file descriptor. |
| open static [ResourcesProvider](ResourcesProvider.md) | loadOverlay Creates a ResourcesProvider instance from the specified overlay information. |

## Public methods

### close

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Frees internal data structures. Closed providers can no longer be added to ResourcesLoader.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.IllegalStateException` | if provider is currently used by a ResourcesLoader |
| --- | --- |

### empty

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun empty(assetsProvider: AssetsProvider): ResourcesProvider
```

Creates an empty ResourcesProvider with no resource data. This is useful for loading file-based assets not associated with resource identifiers.

| Parameters ||
|---|---|
| `assetsProvider` | [AssetsProvider](AssetsProvider.md): the assets provider that implements the loading of file-based resources. This value cannot be `null`. |

| Return ||
|---|---|
| ResourcesProvider | This value cannot be `null`. |

### loadFromApk

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun loadFromApk(fileDescriptor: ParcelFileDescriptor): ResourcesProvider
```

Creates a ResourcesProvider from an APK (`.apk`) file descriptor.

The file descriptor is duplicated and the original may be closed by the application at any time without affecting the ResourcesProvider.

| Parameters ||
|---|---|
| `fileDescriptor` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md): the file descriptor of the APK to load. This value cannot be `null`. |

| Return ||
|---|---|
| ResourcesProvider | This value cannot be `null`. |

**See Also**

- open
- memfd_create

### loadFromApk

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun loadFromApk(
    fileDescriptor: ParcelFileDescriptor, 
    assetsProvider: AssetsProvider?
): ResourcesProvider
```

Creates a ResourcesProvider from an APK (`.apk`) file descriptor.

The file descriptor is duplicated and the original may be closed by the application at any time without affecting the ResourcesProvider.

The assets provider can override the loading of files within the APK and can provide entirely new files that do not exist in the APK.

| Parameters ||
|---|---|
| `fileDescriptor` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md): the file descriptor of the APK to load. This value cannot be `null`. |
| `assetsProvider` | [AssetsProvider](AssetsProvider.md)?: the assets provider that overrides the loading of file-based resources. This value may be `null`. |

| Return ||
|---|---|
| ResourcesProvider | This value cannot be `null`. |

**See Also**

- open
- memfd_create

### loadFromDirectory

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun loadFromDirectory(
    path: String, 
    assetsProvider: AssetsProvider?
): ResourcesProvider
```

Creates a ResourcesProvider from a directory path. File-based resources will be resolved within the directory as if the directory is an APK.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the path of the directory to treat as an APK. This value cannot be `null`. |
| `assetsProvider` | [AssetsProvider](AssetsProvider.md)?: the assets provider that overrides the loading of file-based resources. This value may be `null`. |

| Return ||
|---|---|
| ResourcesProvider | This value cannot be `null`. |

### loadFromSplit

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun loadFromSplit(
    context: Context, 
    splitName: String
): ResourcesProvider
```

Read from a split installed alongside the application, which may not have been loaded initially because the application requested isolated split loading.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): a context of the package that contains the split. This value cannot be `null`. |
| `splitName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of the split to load. This value cannot be `null`. |

| Return ||
|---|---|
| ResourcesProvider | This value cannot be `null`. |

### loadFromTable

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun loadFromTable(
    fileDescriptor: ParcelFileDescriptor, 
    assetsProvider: AssetsProvider?
): ResourcesProvider
```

Creates a ResourcesProvider from a resources table (`.arsc`) file descriptor.

The file descriptor is duplicated and the original may be closed by the application at any time without affecting the ResourcesProvider.

The resources table format is not an archive format and therefore cannot asset files within itself. The assets provider can instead provide files that are potentially referenced by path in the resources table.

| Parameters ||
|---|---|
| `fileDescriptor` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md): the file descriptor of the resources table to load. This value cannot be `null`. |
| `assetsProvider` | [AssetsProvider](AssetsProvider.md)?: the assets provider that implements the loading of file-based resources. This value may be `null`. |

| Return ||
|---|---|
| ResourcesProvider | This value cannot be `null`. |

**See Also**

- open
- memfd_create

### loadOverlay

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun loadOverlay(overlayInfo: OverlayInfo): ResourcesProvider
```

Creates a ResourcesProvider instance from the specified overlay information.

In order to enable the registered overlays, an application can create a ResourcesProvider instance according to the specified `https://developer.android.com/reference/kotlin/android/content/om/OverlayInfo.html#` instance and put them into a ResourcesLoader instance. The application calls addLoaders to load the overlays.

| Parameters ||
|---|---|
| `overlayInfo` | [OverlayInfo](../android.content.om/OverlayInfo.md): is the information about the specified overlay. This value cannot be `null`. |

| Return ||
|---|---|
| ResourcesProvider | the resources provider instance for the `overlayInfo` This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | when the files can't be loaded. |

**See Also**

- getOverlayInfosForTarget
