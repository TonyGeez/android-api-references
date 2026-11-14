# Environment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Environment

Kotlin| [Java](https://developer.android.com/reference/android/os/Environment "View this page in Java") 

```
open class Environment
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.Environment](https://developer.android.com/reference/kotlin/android/os/Environment#) |

Provides access to environment variables.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_BAD_REMOVAL](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_BAD_REMOVAL:kotlin.String) Storage state if the media was removed before it was unmounted. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_CHECKING](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_CHECKING:kotlin.String) Storage state if the media is present and being disk-checked. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_EJECTING](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_EJECTING:kotlin.String) Storage state if the media is in the process of being ejected. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_MOUNTED](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_MOUNTED:kotlin.String) Storage state if the media is present and mounted at its mount point with read/write access. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_MOUNTED_READ_ONLY](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_MOUNTED_READ_ONLY:kotlin.String) Storage state if the media is present and mounted at its mount point with read-only access. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_NOFS](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_NOFS:kotlin.String) Storage state if the media is present but is blank or is using an unsupported filesystem. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_REMOVED](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_REMOVED:kotlin.String) Storage state if the media is not present. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_SHARED](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_SHARED:kotlin.String) Storage state if the media is present not mounted, and shared via USB mass storage. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_UNKNOWN](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_UNKNOWN:kotlin.String) Unknown storage state, such as when a path isn't backed by known storage media. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_UNMOUNTABLE](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_UNMOUNTABLE:kotlin.String) Storage state if the media is present but cannot be mounted. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MEDIA_UNMOUNTED](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_UNMOUNTED:kotlin.String) Storage state if the media is present but not mounted. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------|---|
| [Environment](https://developer.android.com/reference/kotlin/android/os/Environment#Environment())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [File](https://developer.android.com/reference/kotlin/java/io/File.html#)! | [getDataDirectory](https://developer.android.com/reference/kotlin/android/os/Environment#getDataDirectory())`()` Return the user data directory. |
| openstatic [File](https://developer.android.com/reference/kotlin/java/io/File.html#)! | [getDownloadCacheDirectory](https://developer.android.com/reference/kotlin/android/os/Environment#getDownloadCacheDirectory())`()` Return the download/cache content directory. |
| openstatic [File](https://developer.android.com/reference/kotlin/java/io/File.html#)! | [getExternalStorageDirectory](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageDirectory())`()` Return the primary shared/external storage directory. |
| openstatic [File](https://developer.android.com/reference/kotlin/java/io/File.html#)! | [getExternalStoragePublicDirectory](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStoragePublicDirectory(kotlin.String))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get a top-level shared/external storage directory for placing files of a particular type. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getExternalStorageState](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageState())`()` Returns the current state of the primary shared/external storage media. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getExternalStorageState](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageState(java.io.File))`(`path:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`)` Returns the current state of the shared/external storage media at the given path. |
| openstatic [File](https://developer.android.com/reference/kotlin/java/io/File.html#) | [getRootDirectory](https://developer.android.com/reference/kotlin/android/os/Environment#getRootDirectory())`()` Return root of the "system" partition holding the core Android OS. |
| openstatic [File](https://developer.android.com/reference/kotlin/java/io/File.html#) | [getStorageDirectory](https://developer.android.com/reference/kotlin/android/os/Environment#getStorageDirectory())`()` Return root directory where all external storage devices will be mounted. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getStorageState](https://developer.android.com/reference/kotlin/android/os/Environment#getStorageState(java.io.File))`(`path:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`)` <br /> |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExternalStorageEmulated](https://developer.android.com/reference/kotlin/android/os/Environment#isExternalStorageEmulated())`()` Returns whether the primary shared/external storage media is emulated. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExternalStorageEmulated](https://developer.android.com/reference/kotlin/android/os/Environment#isExternalStorageEmulated(java.io.File))`(`path:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)`)` Returns whether the shared/external storage media at the given path is emulated. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExternalStorageLegacy](https://developer.android.com/reference/kotlin/android/os/Environment#isExternalStorageLegacy())`()` Returns whether the shared/external storage media is a legacy view that includes files not owned by the app. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExternalStorageLegacy](https://developer.android.com/reference/kotlin/android/os/Environment#isExternalStorageLegacy(java.io.File))`(`path:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)`)` Returns whether the shared/external storage media is a legacy view that includes files not owned by the app. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExternalStorageManager](https://developer.android.com/reference/kotlin/android/os/Environment#isExternalStorageManager())`()` Returns whether the calling app has All Files Access on the primary shared/external storage media. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExternalStorageManager](https://developer.android.com/reference/kotlin/android/os/Environment#isExternalStorageManager(java.io.File))`(`path:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)`)` Returns whether the calling app has All Files Access at the given`path` |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExternalStorageRemovable](https://developer.android.com/reference/kotlin/android/os/Environment#isExternalStorageRemovable())`()` Returns whether the primary shared/external storage media is physically removable. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExternalStorageRemovable](https://developer.android.com/reference/kotlin/android/os/Environment#isExternalStorageRemovable(java.io.File))`(`path:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)`)` Returns whether the shared/external storage media at the given path is physically removable. |

| Properties ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_ALARMS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_ALARMS:kotlin.String) Standard directory in which to place any audio files that should be in the list of alarms that the user can select (not as regular music). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_AUDIOBOOKS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_AUDIOBOOKS:kotlin.String) Standard directory in which to place any audio files that should be in the list of audiobooks that the user can select (not as regular music). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_DCIM](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_DCIM:kotlin.String) The traditional location for pictures and videos when mounting the device as a camera. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_DOCUMENTS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_DOCUMENTS:kotlin.String) Standard directory in which to place documents that have been created by the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_DOWNLOADS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_DOWNLOADS:kotlin.String) Standard directory in which to place files that have been downloaded by the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_MOVIES](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_MOVIES:kotlin.String) Standard directory in which to place movies that are available to the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_MUSIC](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_MUSIC:kotlin.String) Standard directory in which to place any audio files that should be in the regular list of music for the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_NOTIFICATIONS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_NOTIFICATIONS:kotlin.String) Standard directory in which to place any audio files that should be in the list of notifications that the user can select (not as regular music). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_PICTURES](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_PICTURES:kotlin.String) Standard directory in which to place pictures that are available to the user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_PODCASTS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_PODCASTS:kotlin.String) Standard directory in which to place any audio files that should be in the list of podcasts that the user can select (not as regular music). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DIRECTORY_RECORDINGS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_RECORDINGS:kotlin.String) Standard directory in which to place any audio files that should be in the list of voice recordings recorded by voice recorder apps that the user can select (not as regular music). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_RINGTONES](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_RINGTONES:kotlin.String) Standard directory in which to place any audio files that should be in the list of ringtones that the user can select (not as regular music). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DIRECTORY_SCREENSHOTS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_SCREENSHOTS:kotlin.String) Standard directory in which to place screenshots that have been taken by the user. |

## Constants

### MEDIA_BAD_REMOVAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_BAD_REMOVAL: String
```

Storage state if the media was removed before it was unmounted. 

 Value: "bad_removal"

**See Also**

- [#getExternalStorageState(File)](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageState(java.io.File)) 

### MEDIA_CHECKING

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_CHECKING: String
```

Storage state if the media is present and being disk-checked. 

 Value: "checking"

**See Also**

- [#getExternalStorageState(File)](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageState(java.io.File)) 

### MEDIA_EJECTING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_EJECTING: String
```

Storage state if the media is in the process of being ejected. 

 Value: "ejecting"

**See Also**

- [#getExternalStorageState(File)](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageState(java.io.File)) 

### MEDIA_MOUNTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_MOUNTED: String
```

Storage state if the media is present and mounted at its mount point with read/write access. 

 Value: "mounted"

**See Also**

- [#getExternalStorageState(File)](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageState(java.io.File)) 

### MEDIA_MOUNTED_READ_ONLY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_MOUNTED_READ_ONLY: String
```

Storage state if the media is present and mounted at its mount point with read-only access. 

 Value: "mounted_ro"

**See Also**

- [#getExternalStorageState(File)](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageState(java.io.File)) 

### MEDIA_NOFS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_NOFS: String
```

Storage state if the media is present but is blank or is using an unsupported filesystem. 

 Value: "nofs"

**See Also**

- [#getExternalStorageState(File)](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageState(java.io.File)) 

### MEDIA_REMOVED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_REMOVED: String
```

Storage state if the media is not present. 

 Value: "removed"

**See Also**

- [#getExternalStorageState(File)](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageState(java.io.File)) 

### MEDIA_SHARED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_SHARED: String
```

Storage state if the media is present not mounted, and shared via USB mass storage. 

 Value: "shared"

**See Also**

- [#getExternalStorageState(File)](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageState(java.io.File)) 

### MEDIA_UNKNOWN

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_UNKNOWN: String
```

Unknown storage state, such as when a path isn't backed by known storage media. 

 Value: "unknown"

**See Also**

- [#getExternalStorageState(File)](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageState(java.io.File)) 

### MEDIA_UNMOUNTABLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_UNMOUNTABLE: String
```

Storage state if the media is present but cannot be mounted. Typically this happens if the file system on the media is corrupted. 

 Value: "unmountable"

**See Also**

- [#getExternalStorageState(File)](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageState(java.io.File)) 

### MEDIA_UNMOUNTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEDIA_UNMOUNTED: String
```

Storage state if the media is present but not mounted. 

 Value: "unmounted"

**See Also**

- [#getExternalStorageState(File)](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageState(java.io.File))

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

Return the primary shared/external storage directory. This directory may not currently be accessible if it has been mounted by the user on their computer, has been removed from the device, or some other problem has happened. You can determine its current state with [getExternalStorageState()](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageState()).

*Note: don't be confused by the word "external" here. This directory can better be thought as media/shared storage. It is a filesystem that can hold a relatively large amount of data and that is shared across all applications (does not enforce permissions). Traditionally this is an SD card, but it may also be implemented as built-in storage in a device that is distinct from the protected internal storage and can be mounted as a filesystem on a computer.*

On devices with multiple users (as described by [UserManager](https://developer.android.com/reference/kotlin/android/os/UserManager)), each user has their own isolated shared storage. Applications only have access to the shared storage for the user they're running as.

In devices with multiple shared/external storage directories, this directory represents the primary storage that the user will interact with. Access to secondary storage is available through [Context.getExternalFilesDirs(String)](https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalFilesDirs(kotlin.String)), [Context.getExternalCacheDirs()](https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalCacheDirs()), and [Context.getExternalMediaDirs()](https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalMediaDirs()).

Applications should not directly use this top-level directory, in order to avoid polluting the user's root namespace. Any files that are private to the application should be placed in a directory returned by [Context.getExternalFilesDir](https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalFilesDir(kotlin.String)), which the system will take care of deleting if the application is uninstalled. Other shared files should be placed in one of the directories returned by [getExternalStoragePublicDirectory](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStoragePublicDirectory(kotlin.String)).

Writing to this path requires the [android.Manifest.permission#WRITE_EXTERNAL_STORAGE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String) permission, and starting in [android.os.Build.VERSION_CODES#KITKAT](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#KITKAT:kotlin.Int), read access requires the [android.Manifest.permission#READ_EXTERNAL_STORAGE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String) permission, which is automatically granted if you hold the write permission.

Starting in [android.os.Build.VERSION_CODES#KITKAT](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#KITKAT:kotlin.Int), if your application only needs to store internal data, consider using [Context.getExternalFilesDir(String)](https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalFilesDir(kotlin.String)), [Context.getExternalCacheDir()](https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalCacheDir()), or [Context.getExternalMediaDirs()](https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalMediaDirs()), which require no permissions to read or write.

This path may change between platform versions, so applications should only persist relative paths.

Here is an example of typical code to monitor the state of external storage:

<br />

Note that alternatives such as [Context.getExternalFilesDir(String)](https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalFilesDir(kotlin.String))or [MediaStore](https://developer.android.com/reference/kotlin/android/provider/MediaStore.html#) offer better performance. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageState()>
- <https://developer.android.com/reference/kotlin/android/os/Environment#isExternalStorageRemovable()> 

### getExternalStoragePublicDirectory

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getExternalStoragePublicDirectory(type: String!): File!
```

Get a top-level shared/external storage directory for placing files of a particular type. This is where the user will typically place and manage their own files, so you should be careful about what you put here to ensure you don't erase their files or get in the way of their own organization.

On devices with multiple users (as described by [UserManager](https://developer.android.com/reference/kotlin/android/os/UserManager)), each user has their own isolated shared storage. Applications only have access to the shared storage for the user they're running as.

Here is an example of typical code to manipulate a picture on the public shared storage:

Note that alternatives such as [Context.getExternalFilesDir(String)](https://developer.android.com/reference/kotlin/android/content/Context.html#getExternalFilesDir(kotlin.String))or [MediaStore](https://developer.android.com/reference/kotlin/android/provider/MediaStore.html#) offer better performance.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The type of storage directory to return. Should be one of [DIRECTORY_MUSIC](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_MUSIC:kotlin.String), [DIRECTORY_PODCASTS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_PODCASTS:kotlin.String), [DIRECTORY_RINGTONES](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_RINGTONES:kotlin.String), [DIRECTORY_ALARMS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_ALARMS:kotlin.String), [DIRECTORY_NOTIFICATIONS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_NOTIFICATIONS:kotlin.String), [DIRECTORY_PICTURES](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_PICTURES:kotlin.String), [DIRECTORY_MOVIES](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_MOVIES:kotlin.String), [DIRECTORY_DOWNLOADS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_DOWNLOADS:kotlin.String), [DIRECTORY_DCIM](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_DCIM:kotlin.String), or [DIRECTORY_DOCUMENTS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_DOCUMENTS:kotlin.String). May not be null. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [File](https://developer.android.com/reference/kotlin/java/io/File.html#)! | Returns the File path for the directory. Note that this directory may not yet exist, so you must make sure it exists before using it such as with [File.mkdirs()](https://developer.android.com/reference/kotlin/java/io/File.html#mkdirs()). |

### getExternalStorageState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getExternalStorageState(): String!
```

Returns the current state of the primary shared/external storage media.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | one of [MEDIA_UNKNOWN](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_UNKNOWN:kotlin.String), [MEDIA_REMOVED](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_REMOVED:kotlin.String), [MEDIA_UNMOUNTED](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_UNMOUNTED:kotlin.String), [MEDIA_CHECKING](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_CHECKING:kotlin.String), [MEDIA_NOFS](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_NOFS:kotlin.String), [MEDIA_MOUNTED](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_MOUNTED:kotlin.String), [MEDIA_MOUNTED_READ_ONLY](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_MOUNTED_READ_ONLY:kotlin.String), [MEDIA_SHARED](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_SHARED:kotlin.String), [MEDIA_BAD_REMOVAL](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_BAD_REMOVAL:kotlin.String), or [MEDIA_UNMOUNTABLE](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_UNMOUNTABLE:kotlin.String). |

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
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | one of [MEDIA_UNKNOWN](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_UNKNOWN:kotlin.String), [MEDIA_REMOVED](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_REMOVED:kotlin.String), [MEDIA_UNMOUNTED](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_UNMOUNTED:kotlin.String), [MEDIA_CHECKING](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_CHECKING:kotlin.String), [MEDIA_NOFS](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_NOFS:kotlin.String), [MEDIA_MOUNTED](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_MOUNTED:kotlin.String), [MEDIA_MOUNTED_READ_ONLY](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_MOUNTED_READ_ONLY:kotlin.String), [MEDIA_SHARED](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_SHARED:kotlin.String), [MEDIA_BAD_REMOVAL](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_BAD_REMOVAL:kotlin.String), or [MEDIA_UNMOUNTABLE](https://developer.android.com/reference/kotlin/android/os/Environment#MEDIA_UNMOUNTABLE:kotlin.String). |

### getRootDirectory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getRootDirectory(): File
```

Return root of the "system" partition holding the core Android OS. Always present and mounted read-only.

| Return ||
|---------------------------------------------------------------------------|-----------------------------|
| [File](https://developer.android.com/reference/kotlin/java/io/File.html#) | This value cannot be`null`. |

### getStorageDirectory

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getStorageDirectory(): File
```

Return root directory where all external storage devices will be mounted. For example, [getExternalStorageDirectory()](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageDirectory())will appear under this location.

| Return ||
|---------------------------------------------------------------------------|-----------------------------|
| [File](https://developer.android.com/reference/kotlin/java/io/File.html#) | This value cannot be`null`. |

### getStorageState

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getStorageState(path: File!): String!
```

**Deprecated:** *use [getExternalStorageState(java.io.File)](https://developer.android.com/reference/kotlin/android/os/Environment#getExternalStorageState(java.io.File))* 

### isExternalStorageEmulated

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isExternalStorageEmulated(): Boolean
```

Returns whether the primary shared/external storage media is emulated.

The contents of emulated storage devices are backed by a private user data partition, which means there is little benefit to apps storing data here instead of the private directories returned by [Context.getFilesDir()](https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()), etc.

This returns true when emulated storage is backed by either internal storage or an adopted storage device. 
**See Also**

- [android.app.admin.DevicePolicyManager#setStorageEncryption(android.content.ComponentName,
* boolean)](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#setStorageEncryption(android.content.ComponentName,%20kotlin.Boolean)) 

### isExternalStorageEmulated

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isExternalStorageEmulated(path: File): Boolean
```

Returns whether the shared/external storage media at the given path is emulated.

The contents of emulated storage devices are backed by a private user data partition, which means there is little benefit to apps storing data here instead of the private directories returned by [Context.getFilesDir()](https://developer.android.com/reference/kotlin/android/content/Context.html#getFilesDir()), etc.

This returns true when emulated storage is backed by either internal storage or an adopted storage device.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `path` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#):This value cannot be`null`. |

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

Non-legacy apps can continue to discover and read media belonging to other apps via [android.provider.MediaStore](https://developer.android.com/reference/kotlin/android/provider/MediaStore.html#). 

### isExternalStorageLegacy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isExternalStorageLegacy(path: File): Boolean
```

Returns whether the shared/external storage media is a legacy view that includes files not owned by the app.

This value may be different from the value requested by`requestLegacyExternalStorage`in the app's manifest, since an app may inherit its legacy state based on when it was first installed, target sdk and other factors.

Non-legacy apps can continue to discover and read media belonging to other apps via [android.provider.MediaStore](https://developer.android.com/reference/kotlin/android/provider/MediaStore.html#).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `path` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#):This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | if the path is not a valid storage device. |

### isExternalStorageManager

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isExternalStorageManager(): Boolean
```

Returns whether the calling app has All Files Access on the primary shared/external storage media.

Declaring the permission [android.Manifest.permission#MANAGE_EXTERNAL_STORAGE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String) isn't enough to gain the access.

To request access, use [android.provider.Settings#ACTION_MANAGE_APP_ALL_FILES_ACCESS_PERMISSION](https://developer.android.com/reference/kotlin/android/provider/Settings.html#ACTION_MANAGE_APP_ALL_FILES_ACCESS_PERMISSION:kotlin.String). 

### isExternalStorageManager

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isExternalStorageManager(path: File): Boolean
```

Returns whether the calling app has All Files Access at the given`path`

Declaring the permission [android.Manifest.permission#MANAGE_EXTERNAL_STORAGE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String) isn't enough to gain the access.

To request access, use [android.provider.Settings#ACTION_MANAGE_APP_ALL_FILES_ACCESS_PERMISSION](https://developer.android.com/reference/kotlin/android/provider/Settings.html#ACTION_MANAGE_APP_ALL_FILES_ACCESS_PERMISSION:kotlin.String).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `path` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#):This value cannot be`null`. |

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
| `path` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#):This value cannot be`null`. |

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

Standard directory in which to place any audio files that should be in the list of alarms that the user can select (not as regular music). This may be combined with [DIRECTORY_MUSIC](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_MUSIC:kotlin.String), [DIRECTORY_AUDIOBOOKS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_AUDIOBOOKS:kotlin.String), [DIRECTORY_PODCASTS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_PODCASTS:kotlin.String), [DIRECTORY_NOTIFICATIONS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_NOTIFICATIONS:kotlin.String), [DIRECTORY_RINGTONES](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_RINGTONES:kotlin.String), and [DIRECTORY_RECORDINGS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_RECORDINGS:kotlin.String) as a series of directories to categorize a particular audio file as more than one type. 

### DIRECTORY_AUDIOBOOKS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var DIRECTORY_AUDIOBOOKS: String!
```

Standard directory in which to place any audio files that should be in the list of audiobooks that the user can select (not as regular music). This may be combined with [DIRECTORY_MUSIC](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_MUSIC:kotlin.String), [DIRECTORY_PODCASTS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_PODCASTS:kotlin.String), [DIRECTORY_NOTIFICATIONS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_NOTIFICATIONS:kotlin.String), [DIRECTORY_ALARMS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_ALARMS:kotlin.String), [DIRECTORY_RINGTONES](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_RINGTONES:kotlin.String), and [DIRECTORY_RECORDINGS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_RECORDINGS:kotlin.String) as a series of directories to categorize a particular audio file as more than one type. 

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

Standard directory in which to place any audio files that should be in the regular list of music for the user. This may be combined with [DIRECTORY_AUDIOBOOKS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_AUDIOBOOKS:kotlin.String), [DIRECTORY_PODCASTS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_PODCASTS:kotlin.String), [DIRECTORY_NOTIFICATIONS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_NOTIFICATIONS:kotlin.String), [DIRECTORY_ALARMS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_ALARMS:kotlin.String), [DIRECTORY_RINGTONES](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_RINGTONES:kotlin.String), and [DIRECTORY_RECORDINGS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_RECORDINGS:kotlin.String) as a series of directories to categorize a particular audio file as more than one type. 

### DIRECTORY_NOTIFICATIONS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var DIRECTORY_NOTIFICATIONS: String!
```

Standard directory in which to place any audio files that should be in the list of notifications that the user can select (not as regular music). This may be combined with [DIRECTORY_MUSIC](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_MUSIC:kotlin.String), [DIRECTORY_AUDIOBOOKS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_AUDIOBOOKS:kotlin.String), [DIRECTORY_PODCASTS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_PODCASTS:kotlin.String), [DIRECTORY_ALARMS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_ALARMS:kotlin.String), [DIRECTORY_RINGTONES](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_RINGTONES:kotlin.String), and [DIRECTORY_RECORDINGS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_RECORDINGS:kotlin.String) as a series of directories to categorize a particular audio file as more than one type. 

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

Standard directory in which to place any audio files that should be in the list of podcasts that the user can select (not as regular music). This may be combined with [DIRECTORY_MUSIC](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_MUSIC:kotlin.String), [DIRECTORY_AUDIOBOOKS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_AUDIOBOOKS:kotlin.String), [DIRECTORY_NOTIFICATIONS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_NOTIFICATIONS:kotlin.String), [DIRECTORY_ALARMS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_ALARMS:kotlin.String), [DIRECTORY_RINGTONES](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_RINGTONES:kotlin.String), and [DIRECTORY_RECORDINGS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_RECORDINGS:kotlin.String) as a series of directories to categorize a particular audio file as more than one type. 

### DIRECTORY_RECORDINGS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var DIRECTORY_RECORDINGS: String
```

Standard directory in which to place any audio files that should be in the list of voice recordings recorded by voice recorder apps that the user can select (not as regular music). This may be combined with [DIRECTORY_MUSIC](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_MUSIC:kotlin.String), [DIRECTORY_AUDIOBOOKS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_AUDIOBOOKS:kotlin.String), [DIRECTORY_PODCASTS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_PODCASTS:kotlin.String), [DIRECTORY_NOTIFICATIONS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_NOTIFICATIONS:kotlin.String), [DIRECTORY_ALARMS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_ALARMS:kotlin.String), and [DIRECTORY_RINGTONES](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_RINGTONES:kotlin.String) as a series of directories to categorize a particular audio file as more than one type. 

### DIRECTORY_RINGTONES

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var DIRECTORY_RINGTONES: String!
```

Standard directory in which to place any audio files that should be in the list of ringtones that the user can select (not as regular music). This may be combined with [DIRECTORY_MUSIC](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_MUSIC:kotlin.String), [DIRECTORY_AUDIOBOOKS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_AUDIOBOOKS:kotlin.String), [DIRECTORY_PODCASTS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_PODCASTS:kotlin.String), [DIRECTORY_NOTIFICATIONS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_NOTIFICATIONS:kotlin.String), [DIRECTORY_ALARMS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_ALARMS:kotlin.String), and [DIRECTORY_RECORDINGS](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_RECORDINGS:kotlin.String) as a series of directories to categorize a particular audio file as more than one type. 

### DIRECTORY_SCREENSHOTS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var DIRECTORY_SCREENSHOTS: String!
```

Standard directory in which to place screenshots that have been taken by the user. Typically used as a secondary directory under [DIRECTORY_PICTURES](https://developer.android.com/reference/kotlin/android/os/Environment#DIRECTORY_PICTURES:kotlin.String).
