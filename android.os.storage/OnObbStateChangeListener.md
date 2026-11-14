# OnObbStateChangeListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnObbStateChangeListener

Kotlin| [Java](../android/os/storage/OnObbStateChangeListener.md) 
| --- | --- |

```
abstract class OnObbStateChangeListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.storage.OnObbStateChangeListener](../android/os/storage/OnObbStateChangeListener.md) |

Used for receiving notifications from [StorageManager](../android/os/storage/StorageManager.md) about OBB file states.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ALREADY_MOUNTED](../android/os/storage/OnObbStateChangeListener.md) The OBB has already been mounted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_COULD_NOT_MOUNT](../android/os/storage/OnObbStateChangeListener.md) The OBB could not be mounted by the system. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_COULD_NOT_UNMOUNT](../android/os/storage/OnObbStateChangeListener.md) The OBB could not be unmounted. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INTERNAL](../android/os/storage/OnObbStateChangeListener.md) There was an internal system error encountered while trying to mount the OBB. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NOT_MOUNTED](../android/os/storage/OnObbStateChangeListener.md) A call was made to unmount the OBB when it was not mounted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PERMISSION_DENIED](../android/os/storage/OnObbStateChangeListener.md) The current application does not have permission to use this OBB. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MOUNTED](../android/os/storage/OnObbStateChangeListener.md) The OBB container is now mounted and ready for use. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNMOUNTED](../android/os/storage/OnObbStateChangeListener.md) The OBB container is now unmounted and not usable. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OnObbStateChangeListener](../android/os/storage/OnObbStateChangeListener.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onObbStateChange](../android/os/storage/OnObbStateChangeListener.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when an OBB has changed states. |

## Constants

### ERROR_ALREADY_MOUNTED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_ALREADY_MOUNTED: Int
```

The OBB has already been mounted. Returned in status messages from calls made via [StorageManager](../android/os/storage/StorageManager.md) 

 Value: 24

### ERROR_COULD_NOT_MOUNT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_COULD_NOT_MOUNT: Int
```

The OBB could not be mounted by the system. Returned in status messages from calls made via [StorageManager](../android/os/storage/StorageManager.md) 

 Value: 21

### ERROR_COULD_NOT_UNMOUNT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_COULD_NOT_UNMOUNT: Int
```

The OBB could not be unmounted. This most likely indicates that a file is in use on the OBB. Returned in status messages from calls made via [StorageManager](../android/os/storage/StorageManager.md) 

 Value: 22

### ERROR_INTERNAL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INTERNAL: Int
```

There was an internal system error encountered while trying to mount the OBB. Returned in status messages from calls made via [StorageManager](../android/os/storage/StorageManager.md) 

 Value: 20

### ERROR_NOT_MOUNTED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_NOT_MOUNTED: Int
```

A call was made to unmount the OBB when it was not mounted. Returned in status messages from calls made via [StorageManager](../android/os/storage/StorageManager.md) 

 Value: 23

### ERROR_PERMISSION_DENIED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_PERMISSION_DENIED: Int
```

The current application does not have permission to use this OBB. This could be because the OBB indicates it's owned by a different package or some other error. Returned in status messages from calls made via [StorageManager](../android/os/storage/StorageManager.md) 

 Value: 25

### MOUNTED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MOUNTED: Int
```

The OBB container is now mounted and ready for use. Returned in status messages from calls made via [StorageManager](../android/os/storage/StorageManager.md) 

 Value: 1

### UNMOUNTED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNMOUNTED: Int
```

The OBB container is now unmounted and not usable. Returned in status messages from calls made via [StorageManager](../android/os/storage/StorageManager.md) 

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
