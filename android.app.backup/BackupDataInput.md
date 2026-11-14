Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BackupDataInput

```
open class BackupDataInput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.backup.BackupDataInput](https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInput#) |

Provides the structured interface through which a `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent` reads information from the backup data set, via its `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent#onRestore(android.app.backup.BackupDataInput,%20kotlin.Int,%20android.os.ParcelFileDescriptor)` method. The data is presented as a set of "entities," each representing one named record as previously stored by the agent's android.app.backup.BackupAgent#onBackup(ParcelFileDescriptor,android.app.backup.BackupDataOutput,ParcelFileDescriptor) implementation. An entity is composed of a descriptive header plus a byte array that holds the raw data saved in the remote backup.

The agent must consume every entity in the data stream, otherwise the restored state of the application will be incomplete.

### Example

A typical android.app.backup.BackupAgent#onRestore(android.app.backup.BackupDataInput,int,ParcelFileDescriptor) implementation might be structured something like this:

```kotlin
public void onRestore(BackupDataInput data, int appVersionCode,
                        ParcelFileDescriptor newState) {
      while (data.readNextHeader()) {
          String key = data.getKey();
          int dataSize = data.getDataSize();
 
          if (key.equals(MY_BACKUP_KEY_ONE)) {
              // process this kind of record here
              byte[] buffer = new byte[dataSize];
              data.readEntityData(buffer, 0, dataSize); // reads the entire entity at once
 
              // now 'buffer' holds the raw data and can be processed however
              // the agent wishes
              processBackupKeyOne(buffer);
          } else if (key.equals(MY_BACKUP_KEY_TO_IGNORE) {
              // a key we recognize but wish to discard
              data.skipEntityData();
          } // ... etc.
     }
  }
```

## Summary

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInput#getDataSize()()` Report the size in bytes of the data associated with the current entity in the restore stream. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInput#getKey()()` Report the key associated with the current entity in the restore stream |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInput#readEntityData(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(data: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, size: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Read a record's raw data from the restore stream. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInput#readNextHeader()()` Extract the next entity header from the restore stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInput#skipEntityData()()` Consume the current entity's data without extracting it into a buffer for further processing. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInput#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Public methods

### getDataSize

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDataSize(): Int
```

Report the size in bytes of the data associated with the current entity in the restore stream.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The size of the record's raw data, in bytes |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the next record header has not yet been read |

### getKey

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getKey(): String!
```

Report the key associated with the current entity in the restore stream

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the current entity's key string |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the next record header has not yet been read |

### readEntityData

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readEntityData(
    data: ByteArray!, 
    offset: Int, 
    size: Int
): Int
```

Read a record's raw data from the restore stream. The record's header must first have been processed by the `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInput#readNextHeader()` method. Multiple calls to this method may be made in order to process the data in chunks; not all of it must be read in a single call. Once all of the raw data for the current entity has been read, further calls to this method will simply return zero.

| Parameters ||
|---|---|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: An allocated byte array of at least 'size' bytes |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Offset within the 'data' array at which the data will be placed when read from the stream |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of bytes to read in this pass |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of bytes of data read. Once all of the data for this entity has been read, further calls to this method will return zero. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an error occurred when trying to read the restore data stream |

### readNextHeader

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readNextHeader(): Boolean
```

Extract the next entity header from the restore stream. After this method return success, the `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInput#getKey()` and `https://developer.android.com/reference/kotlin/android/app/backup/BackupDataInput#getDataSize()` methods can be used to inspect the entity that is now available for processing.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` when there is an entity ready for consumption from the restore stream, `false` if the restore stream has been fully consumed. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an error occurred while reading the restore stream |

### skipEntityData

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun skipEntityData(): Unit
```

Consume the current entity's data without extracting it into a buffer for further processing. This allows a `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent` to efficiently discard obsolete or otherwise uninteresting records during the restore operation.

| Exceptions ||
|---|---|
| `java.io.IOException` | if an error occurred when trying to read the restore data stream |

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
