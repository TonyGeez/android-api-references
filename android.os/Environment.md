# Environment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Environment

Kotlin| [Java](../android/os/Environment.md) 
| --- | --- |

```
open class Environment
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.Environment](../android/os/Environment.md) |

Provides access to environment variables.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_BAD_REMOVAL](../android/os/Environment.md) Storage state if the media was removed before it was unmounted. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_CHECKING](../android/os/Environment.md) Storage state if the media is present and being disk-checked. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_EJECTING](../android/os/Environment.md) Storage state if the media is in the process of being ejected. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_MOUNTED](../android/os/Environment.md) Storage state if the media is present and mounted at its mount point with read/write access. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_MOUNTED_READ_ONLY](../android/os/Environment.md) Storage state if the media is present and mounted at its mount point with read-only access. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_NOFS](../android/os/Environment.md) Storage state if the media is present but is blank or is using an unsupported filesystem. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_REMOVED](../android/os/Environment.md) Storage state if the media is not present. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_SHARED](../android/os/Environment.md) Storage state if the media is present not mounted, and shared via USB mass storage. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_UNKNOWN](../android/os/Environment.md) Unknown storage state, such as when a path isn't backed by known storage media. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_UNMOUNTABLE](../android/os/Environment.md) Storage state if the media is present but cannot be mounted. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_UNMOUNTED](../android/os/Environment.md) Storage state if the media is present but not mounted. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------|---|
| [Environment](../android/os/Environment.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [File](../java/io/File.md)! | [getDataDirectory](../android/os/Environment.md))`()` Return the user data directory. |
| openstatic [File](../java/io/File.md)! | [getDownloadCacheDirectory](../android/os/Environment.md))`()` Return the download/cache content directory. |
| openstatic [File](../java/io/File.md)! | [getExternalStorageDirectory](../android/os/Environment.md))`()` Return the primary shared/external storage directory. |
| --- | --- |
| openstatic [File](../java/io/File.md)! | [getExternalStoragePublicDirectory](../android/os/Environment.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get a top-level shared/external storage directory for placing files of a particular type. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getExternalStorageState](../android/os/Environment.md))`()` Returns the current state of the primary shared/external storage media. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getExternalStorageState](../android/os/Environment.md))`(`path:` ` [File](../java/io/File.md)!`)` Returns the current state of the shared/external storage media at the given path. |
| --- | --- |
| openstatic [File](../java/io/File.md) | [getRootDirectory](../android/os/Environment.md))`()` Return root of the "system" partition holding the core Android OS. |
| openstatic [File](../java/io/File.md) | [getStorageDirectory](../android/os/Environment.md))`()` Return root directory where all external storage devices will be mounted. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getStorageState](../android/os/Environment.md))`(`path:` ` [File](../java/io/File.md)!`)` <br /> |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExternalStorageEmulated](../android/os/Environment.md))`()` Returns whether the primary shared/external storage media is emulated. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExternalStorageEmulated](../android/os/Environment.md))`(`path:` ` [File](../java/io/File.md)`)` Returns whether the shared/external storage media at the given path is emulated. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExternalStorageLegacy](../android/os/Environment.md))`()` Returns whether the shared/external storage media is a legacy view that includes files not owned by the app. |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExternalStorageLegacy](../android/os/Environment.md))`(`path:` ` [File](../java/io/File.md)`)` Returns whether the shared/external storage media is a legacy view that includes files not owned by the app. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExternalStorageManager](../android/os/Environment.md))`()` Returns whether the calling app has All Files Access on the primary shared/external storage media. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExternalStorageManager](../android/os/Environment.md))`(`path:` ` [File](../java/io/File.md)`)` Returns whether the calling app has All Files Access at the given`path` |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExternalStorageRemovable](../android/os/Environment.md))`()` Returns whether the primary shared/external storage media is physically removable. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExternalStorageRemovable](../android/os/Environment.md))`(`path:` ` [File](../java/io/File.md)`)` Returns whether the shared/external storage media at the given path is physically removable. |

| Properties ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_ALARMS](../android/os/Environment.md) Standard directory in which to place any audio files that should be in the list of alarms that the user can select (not as regular music). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_AUDIOBOOKS](../android/os/Environment.md) Standard directory in which to place any audio files that should be in the list of audiobooks that the user can select (not as regular music). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_DCIM](../android/os/Environment.md) The traditional location for pictures and videos when mounting the device as a camera. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_DOCUMENTS](../android/os/Environment.md) Standard directory in which to place documents that have been created by the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_DOWNLOADS](../android/os/Environment.md) Standard directory in which to place files that have been downloaded by the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_MOVIES](../android/os/Environment.md) Standard directory in which to place movies that are available to the user. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_MUSIC](../android/os/Environment.md) Standard directory in which to place any audio files that should be in the regular list of music for the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_NOTIFICATIONS](../android/os/Environment.md) Standard directory in which to place any audio files that should be in the list of notifications that the user can select (not as regular music). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_PICTURES](../android/os/Environment.md) Standard directory in which to place pictures that are available to the user. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_PODCASTS](../android/os/Environment.md) Standard directory in which to place any audio files that should be in the list of podcasts that the user can select (not as regular music). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DIRECTORY_RECORDINGS](../android/os/Environment.md) Standard directory in which to place any audio files that should be in the list of voice recordings recorded by voice recorder apps that the user can select (not as regular music). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_RINGTONES](../android/os/Environment.md) Standard directory in which to place any audio files that should be in the list of ringtones that the user can select (not as regular music). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_SCREENSHOTS](../android/os/Environment.md) Standard directory in which to place screenshots that have been taken by the user. |

## Constants

### MEDIA_BAD_REMOVAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_BAD_REMOVAL: String
```

Storage state if the media was removed before it was unmounted. 

 Value: "bad_removal"

**See Also**

- [#getExternalStorageState(File)](../android/os/Environment.md)) 

### MEDIA_CHECKING

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_CHECKING: String
```

Storage state if the media is present and being disk-checked. 

 Value: "checking"

**See Also**

- [#getExternalStorageState(File)](../android/os/Environment.md)) 

### MEDIA_EJECTING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_EJECTING: String
```

Storage state if the media is in the process of being ejected. 

 Value: "ejecting"

**See Also**

- [#getExternalStorageState(File)](../android/os/Environment.md)) 

### MEDIA_MOUNTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_MOUNTED: String
```

Storage state if the media is present and mounted at its mount point with read/write access. 

 Value: "mounted"

**See Also**

- [#getExternalStorageState(File)](../android/os/Environment.md)) 

### MEDIA_MOUNTED_READ_ONLY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_MOUNTED_READ_ONLY: String
```

Storage state if the media is present and mounted at its mount point with read-only access. 

 Value: "mounted_ro"

**See Also**

- [#getExternalStorageState(File)](../android/os/Environment.md)) 

### MEDIA_NOFS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_NOFS: String
```

Storage state if the media is present but is blank or is using an unsupported filesystem. 

 Value: "nofs"

**See Also**

- [#getExternalStorageState(File)](../android/os/Environment.md)) 

### MEDIA_REMOVED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_REMOVED: String
```

Storage state if the media is not present. 

 Value: "removed"

**See Also**

- [#getExternalStorageState(File)](../android/os/Environment.md)) 

### MEDIA_SHARED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_SHARED: String
```

Storage state if the media is present not mounted, and shared via USB mass storage. 

 Value: "shared"

**See Also**

- [#getExternalStorageState(File)](../android/os/Environment.md)) 

### MEDIA_UNKNOWN

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_UNKNOWN: String
```

Unknown storage state, such as when a path isn't backed by known storage media. 

 Value: "unknown"

**See Also**

- [#getExternalStorageState(File)](../android/os/Environment.md)) 

### MEDIA_UNMOUNTABLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_UNMOUNTABLE: String
```

Storage state if the media is present but cannot be mounted. Typically this happens if the file system on the media is corrupted. 

 Value: "unmountable"

**See Also**

- [#getExternalStorageState(File)](../android/os/Environment.md)) 

### MEDIA_UNMOUNTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_UNMOUNTED: String
```

Storage state if the media is present but not mounted. 

 Value: "unmounted"

**See Also**

- [#getExternalStorageState(File)](../android/os/Environment.md))

## Public constructors

### Environment

```
Environment()
```

## Public methods

### getDataDirectory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDataDirectory(): File!
```

Return the user data directory. 

### getDownloadCacheDirectory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDownloadCacheDirectory(): File!
```

Return the download/cache content directory. 

### getExternalStorageDirectory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getExternalStorageDirectory(): File!
```

Return the primary shared/external storage directory. This directory may not currently be accessible if it has been mounted by the user on their computer, has been removed from the device, or some other problem has happened. You can determine its current state with [getExternalStorageState()](../android/os/Environment.md)).

*Note: don't be confused by the word "external" here. This directory can better be thought as media/shared storage. It is a filesystem that can hold a relatively large amount of data and that is shared across all applications (does not enforce permissions). Traditionally this is an SD card, but it may also be implemented as built-in storage in a device that is distinct from the protected internal storage and can be mounted as a filesystem on a computer.*

On devices with multiple users (as described by [UserManager](../android/os/UserManager.md)), each user has their own isolated shared storage. Applications only have access to the shared storage for the user they're running as.

In devices with multiple shared/external storage directories, this directory represents the primary storage that the user will interact with. Access to secondary storage is available through [Context.getExternalFilesDirs(String)](../android/content/Context.md)), [Context.getExternalCacheDirs()](../android/content/Context.md)), and [Context.getExternalMediaDirs()](../android/content/Context.md)).

Applications should not directly use this top-level directory, in order to avoid polluting the user's root namespace. Any files that are private to the application should be placed in a directory returned by [Context.getExternalFilesDir](../android/content/Context.md)), which the system will take care of deleting if the application is uninstalled. Other shared files should be placed in one of the directories returned by [getExternalStoragePublicDirectory](../android/os/Environment.md)).

Writing to this path requires the [android.Manifest.permission#WRITE_EXTERNAL_STORAGE](../android/Manifest.permission.md) permission, and starting in [android.os.Build.VERSION_CODES#KITKAT](../android/os/Build.VERSION_CODES.md), read access requires the [android.Manifest.permission#READ_EXTERNAL_STORAGE](../android/Manifest.permission.md) permission, which is automatically granted if you hold the write permission.

Starting in [android.os.Build.VERSION_CODES#KITKAT](../android/os/Build.VERSION_CODES.md), if your application only needs to store internal data, consider using [Context.getExternalFilesDir(String)](../android/content/Context.md)), [Context.getExternalCacheDir()](../android/content/Context.md)), or [Context.getExternalMediaDirs()](../android/content/Context.md)), which require no permissions to read or write.

This path may change between platform versions, so applications should only persist relative paths.

Here is an example of typical code to monitor the state of external storage:

<br />

Note that alternatives such as [Context.getExternalFilesDir(String)](../android/content/Context.md))or [MediaStore](../android/provider/MediaStore.md) offer better performance. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageState()>
- <https://developer.android.com/reference/kotlin/android/os/Environment#isExternalStorageRemovable()> 

### getExternalStoragePublicDirectory

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getExternalStoragePublicDirectory(type: String!): File!
```

Get a top-level shared/external storage directory for placing files of a particular type. This is where the user will typically place and manage their own files, so you should be careful about what you put here to ensure you don't erase their files or get in the way of their own organization.

On devices with multiple users (as described by [UserManager](../android/os/UserManager.md)), each user has their own isolated shared storage. Applications only have access to the shared storage for the user they're running as.

Here is an example of typical code to manipulate a picture on the public shared storage:

Note that alternatives such as [Context.getExternalFilesDir(String)](../android/content/Context.md))or [MediaStore](../android/provider/MediaStore.md) offer better performance.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The type of storage directory to return. Should be one of [DIRECTORY_MUSIC](../android/os/Environment.md), [DIRECTORY_PODCASTS](../android/os/Environment.md), [DIRECTORY_RINGTONES](../android/os/Environment.md), [DIRECTORY_ALARMS](../android/os/Environment.md), [DIRECTORY_NOTIFICATIONS](../android/os/Environment.md), [DIRECTORY_PICTURES](../android/os/Environment.md), [DIRECTORY_MOVIES](../android/os/Environment.md), [DIRECTORY_DOWNLOADS](../android/os/Environment.md), [DIRECTORY_DCIM](../android/os/Environment.md), or [DIRECTORY_DOCUMENTS](../android/os/Environment.md). May not be null. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [File](../java/io/File.md)! | Returns the File path for the directory. Note that this directory may not yet exist, so you must make sure it exists before using it such as with [File.mkdirs()](../java/io/File.md)). |

### getExternalStorageState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getExternalStorageState(): String!
```

Returns the current state of the primary shared/external storage media.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | one of [MEDIA_UNKNOWN](../android/os/Environment.md), [MEDIA_REMOVED](../android/os/Environment.md), [MEDIA_UNMOUNTED](../android/os/Environment.md), [MEDIA_CHECKING](../android/os/Environment.md), [MEDIA_NOFS](../android/os/Environment.md), [MEDIA_MOUNTED](../android/os/Environment.md), [MEDIA_MOUNTED_READ_ONLY](../android/os/Environment.md), [MEDIA_SHARED](../android/os/Environment.md), [MEDIA_BAD_REMOVAL](../android/os/Environment.md), or [MEDIA_UNMOUNTABLE](../android/os/Environment.md). |

**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageDirectory()> 

### getExternalStorageState

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getExternalStorageState(path: File!): String!
```

Returns the current state of the shared/external storage media at the given path.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | one of [MEDIA_UNKNOWN](../android/os/Environment.md), [MEDIA_REMOVED](../android/os/Environment.md), [MEDIA_UNMOUNTED](../android/os/Environment.md), [MEDIA_CHECKING](../android/os/Environment.md), [MEDIA_NOFS](../android/os/Environment.md), [MEDIA_MOUNTED](../android/os/Environment.md), [MEDIA_MOUNTED_READ_ONLY](../android/os/Environment.md), [MEDIA_SHARED](../android/os/Environment.md), [MEDIA_BAD_REMOVAL](../android/os/Environment.md), or [MEDIA_UNMOUNTABLE](../android/os/Environment.md). |

### getRootDirectory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getRootDirectory(): File
```

Return root of the "system" partition holding the core Android OS. Always present and mounted read-only.

| Return ||
|---------------------------------------------------------------------------|-----------------------------|
| [File](../java/io/File.md) | This value cannot be`null`. |

### getStorageDirectory

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getStorageDirectory(): File
```

Return root directory where all external storage devices will be mounted. For example, [getExternalStorageDirectory()](../android/os/Environment.md))will appear under this location.

| Return ||
|---------------------------------------------------------------------------|-----------------------------|
| [File](../java/io/File.md) | This value cannot be`null`. |

### getStorageState

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getStorageState(path: File!): String!
```

**Deprecated:** *use [getExternalStorageState(java.io.File)](../android/os/Environment.md))* 

### isExternalStorageEmulated

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isExternalStorageEmulated(): Boolean
```

Returns whether the primary shared/external storage media is emulated.

The contents of emulated storage devices are backed by a private user data partition, which means there is little benefit to apps storing data here instead of the private directories returned by [Context.getFilesDir()](../android/content/Context.md)), etc.

This returns true when emulated storage is backed by either internal storage or an adopted storage device. 
**See Also**

- [android.app.admin.DevicePolicyManager#setStorageEncryption(android.content.ComponentName,
* boolean)](../android/app/admin/DevicePolicyManager.md)) 

### isExternalStorageEmulated

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isExternalStorageEmulated(path: File): Boolean
```

Returns whether the shared/external storage media at the given path is emulated.

The contents of emulated storage devices are backed by a private user data partition, which means there is little benefit to apps storing data here instead of the private directories returned by [Context.getFilesDir()](../android/content/Context.md)), etc.

This returns true when emulated storage is backed by either internal storage or an adopted storage device.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `path` | [File](../java/io/File.md):This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | if the path is not a valid storage device. |

### isExternalStorageLegacy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isExternalStorageLegacy(): Boolean
```

Returns whether the shared/external storage media is a legacy view that includes files not owned by the app.

This value may be different from the value requested by`requestLegacyExternalStorage`in the app's manifest, since an app may inherit its legacy state based on when it was first installed, target sdk and other factors.

Non-legacy apps can continue to discover and read media belonging to other apps via [android.provider.MediaStore](../android/provider/MediaStore.md). 

### isExternalStorageLegacy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isExternalStorageLegacy(path: File): Boolean
```

Returns whether the shared/external storage media is a legacy view that includes files not owned by the app.

This value may be different from the value requested by`requestLegacyExternalStorage`in the app's manifest, since an app may inherit its legacy state based on when it was first installed, target sdk and other factors.

Non-legacy apps can continue to discover and read media belonging to other apps via [android.provider.MediaStore](../android/provider/MediaStore.md).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `path` | [File](../java/io/File.md):This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | if the path is not a valid storage device. |

### isExternalStorageManager

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isExternalStorageManager(): Boolean
```

Returns whether the calling app has All Files Access on the primary shared/external storage media.

Declaring the permission [android.Manifest.permission#MANAGE_EXTERNAL_STORAGE](../android/Manifest.permission.md) isn't enough to gain the access.

To request access, use [android.provider.Settings#ACTION_MANAGE_APP_ALL_FILES_ACCESS_PERMISSION](../android/provider/Settings.md). 

### isExternalStorageManager

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isExternalStorageManager(path: File): Boolean
```

Returns whether the calling app has All Files Access at the given`path`

Declaring the permission [android.Manifest.permission#MANAGE_EXTERNAL_STORAGE](../android/Manifest.permission.md) isn't enough to gain the access.

To request access, use [android.provider.Settings#ACTION_MANAGE_APP_ALL_FILES_ACCESS_PERMISSION](../android/provider/Settings.md).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `path` | [File](../java/io/File.md):This value cannot be`null`. |

### isExternalStorageRemovable

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isExternalStorageRemovable(): Boolean
```

Returns whether the primary shared/external storage media is physically removable.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the storage device can be removed (such as an SD card), or false if the storage device is built in and cannot be physically removed. |

### isExternalStorageRemovable

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isExternalStorageRemovable(path: File): Boolean
```

Returns whether the shared/external storage media at the given path is physically removable.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `path` | [File](../java/io/File.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the storage device can be removed (such as an SD card), or false if the storage device is built in and cannot be physically removed. |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | if the path is not a valid storage device. |

## Properties

### DIRECTORY_ALARMS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var DIRECTORY_ALARMS: String!
```

Standard directory in which to place any audio files that should be in the list of alarms that the user can select (not as regular music). This may be combined with [DIRECTORY_MUSIC](../android/os/Environment.md), [DIRECTORY_AUDIOBOOKS](../android/os/Environment.md), [DIRECTORY_PODCASTS](../android/os/Environment.md), [DIRECTORY_NOTIFICATIONS](../android/os/Environment.md), [DIRECTORY_RINGTONES](../android/os/Environment.md), and [DIRECTORY_RECORDINGS](../android/os/Environment.md) as a series of directories to categorize a particular audio file as more than one type. 

### DIRECTORY_AUDIOBOOKS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var DIRECTORY_AUDIOBOOKS: String!
```

Standard directory in which to place any audio files that should be in the list of audiobooks that the user can select (not as regular music). This may be combined with [DIRECTORY_MUSIC](../android/os/Environment.md), [DIRECTORY_PODCASTS](../android/os/Environment.md), [DIRECTORY_NOTIFICATIONS](../android/os/Environment.md), [DIRECTORY_ALARMS](../android/os/Environment.md), [DIRECTORY_RINGTONES](../android/os/Environment.md), and [DIRECTORY_RECORDINGS](../android/os/Environment.md) as a series of directories to categorize a particular audio file as more than one type. 

### DIRECTORY_DCIM

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var DIRECTORY_DCIM: String!
```

The traditional location for pictures and videos when mounting the device as a camera. Note that this is primarily a convention for the top-level public directory, as this convention makes no sense elsewhere. 

### DIRECTORY_DOCUMENTS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var DIRECTORY_DOCUMENTS: String!
```

Standard directory in which to place documents that have been created by the user. 

### DIRECTORY_DOWNLOADS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var DIRECTORY_DOWNLOADS: String!
```

Standard directory in which to place files that have been downloaded by the user. Note that this is primarily a convention for the top-level public directory, you are free to download files anywhere in your own private directories. Also note that though the constant here is named DIRECTORY_DOWNLOADS (plural), the actual file name is non-plural for backwards compatibility reasons. 

### DIRECTORY_MOVIES

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var DIRECTORY_MOVIES: String!
```

Standard directory in which to place movies that are available to the user. Note that this is primarily a convention for the top-level public directory, as the media scanner will find and collect movies in any directory. 

### DIRECTORY_MUSIC

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var DIRECTORY_MUSIC: String!
```

Standard directory in which to place any audio files that should be in the regular list of music for the user. This may be combined with [DIRECTORY_AUDIOBOOKS](../android/os/Environment.md), [DIRECTORY_PODCASTS](../android/os/Environment.md), [DIRECTORY_NOTIFICATIONS](../android/os/Environment.md), [DIRECTORY_ALARMS](../android/os/Environment.md), [DIRECTORY_RINGTONES](../android/os/Environment.md), and [DIRECTORY_RECORDINGS](../android/os/Environment.md) as a series of directories to categorize a particular audio file as more than one type. 

### DIRECTORY_NOTIFICATIONS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var DIRECTORY_NOTIFICATIONS: String!
```

Standard directory in which to place any audio files that should be in the list of notifications that the user can select (not as regular music). This may be combined with [DIRECTORY_MUSIC](../android/os/Environment.md), [DIRECTORY_AUDIOBOOKS](../android/os/Environment.md), [DIRECTORY_PODCASTS](../android/os/Environment.md), [DIRECTORY_ALARMS](../android/os/Environment.md), [DIRECTORY_RINGTONES](../android/os/Environment.md), and [DIRECTORY_RECORDINGS](../android/os/Environment.md) as a series of directories to categorize a particular audio file as more than one type. 

### DIRECTORY_PICTURES

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var DIRECTORY_PICTURES: String!
```

Standard directory in which to place pictures that are available to the user. Note that this is primarily a convention for the top-level public directory, as the media scanner will find and collect pictures in any directory. 

### DIRECTORY_PODCASTS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var DIRECTORY_PODCASTS: String!
```

Standard directory in which to place any audio files that should be in the list of podcasts that the user can select (not as regular music). This may be combined with [DIRECTORY_MUSIC](../android/os/Environment.md), [DIRECTORY_AUDIOBOOKS](../android/os/Environment.md), [DIRECTORY_NOTIFICATIONS](../android/os/Environment.md), [DIRECTORY_ALARMS](../android/os/Environment.md), [DIRECTORY_RINGTONES](../android/os/Environment.md), and [DIRECTORY_RECORDINGS](../android/os/Environment.md) as a series of directories to categorize a particular audio file as more than one type. 

### DIRECTORY_RECORDINGS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var DIRECTORY_RECORDINGS: String
```

Standard directory in which to place any audio files that should be in the list of voice recordings recorded by voice recorder apps that the user can select (not as regular music). This may be combined with [DIRECTORY_MUSIC](../android/os/Environment.md), [DIRECTORY_AUDIOBOOKS](../android/os/Environment.md), [DIRECTORY_PODCASTS](../android/os/Environment.md), [DIRECTORY_NOTIFICATIONS](../android/os/Environment.md), [DIRECTORY_ALARMS](../android/os/Environment.md), and [DIRECTORY_RINGTONES](../android/os/Environment.md) as a series of directories to categorize a particular audio file as more than one type. 

### DIRECTORY_RINGTONES

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var DIRECTORY_RINGTONES: String!
```

Standard directory in which to place any audio files that should be in the list of ringtones that the user can select (not as regular music). This may be combined with [DIRECTORY_MUSIC](../android/os/Environment.md), [DIRECTORY_AUDIOBOOKS](../android/os/Environment.md), [DIRECTORY_PODCASTS](../android/os/Environment.md), [DIRECTORY_NOTIFICATIONS](../android/os/Environment.md), [DIRECTORY_ALARMS](../android/os/Environment.md), and [DIRECTORY_RECORDINGS](../android/os/Environment.md) as a series of directories to categorize a particular audio file as more than one type. 

### DIRECTORY_SCREENSHOTS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var DIRECTORY_SCREENSHOTS: String!
```

Standard directory in which to place screenshots that have been taken by the user. Typically used as a secondary directory under [DIRECTORY_PICTURES](../android/os/Environment.md).
