# OnObbStateChangeListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnObbStateChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/os/storage/OnObbStateChangeListener "View this page in Java") 
| --- | --- |

```
abstract class OnObbStateChangeListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.storage.OnObbStateChangeListener](https://developer.android.com/reference/kotlin/android/os/storage/OnObbStateChangeListener#) |

Used for receiving notifications from [StorageManager](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager) about OBB file states.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ALREADY_MOUNTED](https://developer.android.com/reference/kotlin/android/os/storage/OnObbStateChangeListener#ERROR_ALREADY_MOUNTED:kotlin.Int) The OBB has already been mounted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_COULD_NOT_MOUNT](https://developer.android.com/reference/kotlin/android/os/storage/OnObbStateChangeListener#ERROR_COULD_NOT_MOUNT:kotlin.Int) The OBB could not be mounted by the system. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_COULD_NOT_UNMOUNT](https://developer.android.com/reference/kotlin/android/os/storage/OnObbStateChangeListener#ERROR_COULD_NOT_UNMOUNT:kotlin.Int) The OBB could not be unmounted. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INTERNAL](https://developer.android.com/reference/kotlin/android/os/storage/OnObbStateChangeListener#ERROR_INTERNAL:kotlin.Int) There was an internal system error encountered while trying to mount the OBB. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NOT_MOUNTED](https://developer.android.com/reference/kotlin/android/os/storage/OnObbStateChangeListener#ERROR_NOT_MOUNTED:kotlin.Int) A call was made to unmount the OBB when it was not mounted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PERMISSION_DENIED](https://developer.android.com/reference/kotlin/android/os/storage/OnObbStateChangeListener#ERROR_PERMISSION_DENIED:kotlin.Int) The current application does not have permission to use this OBB. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MOUNTED](https://developer.android.com/reference/kotlin/android/os/storage/OnObbStateChangeListener#MOUNTED:kotlin.Int) The OBB container is now mounted and ready for use. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNMOUNTED](https://developer.android.com/reference/kotlin/android/os/storage/OnObbStateChangeListener#UNMOUNTED:kotlin.Int) The OBB container is now unmounted and not usable. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OnObbStateChangeListener](https://developer.android.com/reference/kotlin/android/os/storage/OnObbStateChangeListener#OnObbStateChangeListener())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onObbStateChange](https://developer.android.com/reference/kotlin/android/os/storage/OnObbStateChangeListener#onObbStateChange(kotlin.String,%20kotlin.Int))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when an OBB has changed states. |

## Constants

### ERROR_ALREADY_MOUNTED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_ALREADY_MOUNTED: Int
```

The OBB has already been mounted. Returned in status messages from calls made via [StorageManager](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager) 

 Value: 24

### ERROR_COULD_NOT_MOUNT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_COULD_NOT_MOUNT: Int
```

The OBB could not be mounted by the system. Returned in status messages from calls made via [StorageManager](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager) 

 Value: 21

### ERROR_COULD_NOT_UNMOUNT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_COULD_NOT_UNMOUNT: Int
```

The OBB could not be unmounted. This most likely indicates that a file is in use on the OBB. Returned in status messages from calls made via [StorageManager](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager) 

 Value: 22

### ERROR_INTERNAL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INTERNAL: Int
```

There was an internal system error encountered while trying to mount the OBB. Returned in status messages from calls made via [StorageManager](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager) 

 Value: 20

### ERROR_NOT_MOUNTED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_NOT_MOUNTED: Int
```

A call was made to unmount the OBB when it was not mounted. Returned in status messages from calls made via [StorageManager](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager) 

 Value: 23

### ERROR_PERMISSION_DENIED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_PERMISSION_DENIED: Int
```

The current application does not have permission to use this OBB. This could be because the OBB indicates it's owned by a different package or some other error. Returned in status messages from calls made via [StorageManager](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager) 

 Value: 25

### MOUNTED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MOUNTED: Int
```

The OBB container is now mounted and ready for use. Returned in status messages from calls made via [StorageManager](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager) 

 Value: 1

### UNMOUNTED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNMOUNTED: Int
```

The OBB container is now unmounted and not usable. Returned in status messages from calls made via [StorageManager](https://developer.android.com/reference/kotlin/android/os/storage/StorageManager) 

 Value: 2

## Public constructors

### OnObbStateChangeListener

```
OnObbStateChangeListener()
```

## Public methods

### onObbStateChange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onObbStateChange(
    path: String!, 
    state: Int
): Unit
```

Called when an OBB has changed states.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:path to the OBB file the state change has happened on |
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the current state of the OBB |
