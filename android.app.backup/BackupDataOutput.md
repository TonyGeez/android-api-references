Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BackupDataOutput

```
open class BackupDataOutput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.backup.BackupDataOutput](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput#) |

Provides the structured interface through which a `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent` commits information to the backup data set, via its `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#onBackup(android.os.ParcelFileDescriptor,%20android.app.backup.BackupDataOutput,%20android.os.ParcelFileDescriptor)` method. Data written for backup is presented as a set of "entities," key/value pairs in which each binary data record "value" is named with a string "key."

To commit a data record to the backup transport, the agent's `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#onBackup(android.os.ParcelFileDescriptor,%20android.app.backup.BackupDataOutput,%20android.os.ParcelFileDescriptor)` method first writes an "entity header" that supplies the key string for the record and the total size of the binary value for the record. After the header has been written, the agent then writes the binary entity value itself. The entity value can be written in multiple chunks if desired, as long as the total count of bytes written matches what was supplied to `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput#writeEntityHeader(kotlin.String,%20kotlin.Int)`.

Entity key strings are considered to be unique within a given application's backup data set. If a backup agent writes a new entity under an existing key string, its value will replace any previous value in the transport's remote data store. You can remove a record entirely from the remote data set by writing a new entity header using the existing record's key, but supplying a negative `dataSize` parameter. When you do so, the agent does not need to call `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput#writeEntityData(kotlin.ByteArray,%20kotlin.Int)`.

### Example

Here is an example illustrating a way to back up the value of a String variable called `mStringToBackUp`:

```kotlin
static final String MY_STRING_KEY = "storedstring";
 
  public void <code><a docref="android.app.backup.BackupAgent$onBackup(android.os.ParcelFileDescriptor, android.app.backup.BackupDataOutput, android.os.ParcelFileDescriptor)">onBackup(ParcelFileDescriptor oldState, BackupDataOutput data, ParcelFileDescriptor newState)</a></code>throws IOException {
      ...
      byte[] stringBytes = mStringToBackUp.getBytes();
      data.writeEntityHeader(MY_STRING_KEY, stringBytes.length);
      data.writeEntityData(stringBytes, stringBytes.length);
      ...
  }
```

## Summary

| Public methods ||
|---|---|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput#getQuota()()` Returns the quota in bytes for the application's current backup operation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput#getTransportFlags()()` Returns flags with additional information about the backup transport. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput#writeEntityData(kotlin.ByteArray,%20kotlin.Int)(data: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, size: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Write a chunk of data under the current entity to the backup transport. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput#writeEntityHeader(kotlin.String,%20kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, dataSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Mark the beginning of one record in the backup data stream. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Public methods

### getQuota

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getQuota(): Long
```

Returns the quota in bytes for the application's current backup operation. The value can vary for each operation.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/backup/FullBackupDataOutput#getQuota()`

### getTransportFlags

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTransportFlags(): Int
```

Returns flags with additional information about the backup transport. For supported flags see `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent`
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/backup/FullBackupDataOutput#getTransportFlags()`

### writeEntityData

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeEntityData(
    data: ByteArray!, 
    size: Int
): Int
```

Write a chunk of data under the current entity to the backup transport.

| Parameters ||
|---|---|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: A raw data buffer to send |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of bytes to be sent in this chunk |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of bytes written |

| Exceptions ||
|---|---|
| `java.io.IOException` | if the write failed |

### writeEntityHeader

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeEntityHeader(
    key: String!, 
    dataSize: Int
): Int
```

Mark the beginning of one record in the backup data stream. This must be called before `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataOutput#writeEntityData(kotlin.ByteArray,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A string key that uniquely identifies the data record within the application. Keys whose first character is \\uFF00 or higher are not valid. |
| `dataSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The size in bytes of this record's data. Passing a dataSize of -1 indicates that the record under this key should be deleted. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of bytes written to the backup stream |

| Exceptions ||
|---|---|
| `java.io.IOException` | if the write failed |

## Protected methods

### finalize

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |
