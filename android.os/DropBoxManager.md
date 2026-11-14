# DropBoxManager

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DropBoxManager

Kotlin| [Java](DropBoxManager.md) 
| --- | --- |

```
open class DropBoxManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.DropBoxManager](DropBoxManager.md) |

Enqueues chunks of data (from various sources -- application crashes, kernel log records, etc.). The queue is size bounded and will drop old data if the enqueued data exceeds the maximum size. You can think of this as a persistent, system-wide, blob-oriented "logcat".

DropBoxManager entries are not sent anywhere directly, but other system services and debugging tools may scan and upload entries for processing.

## Summary

| Nested classes ||
|------|-------------------------------------------------------------------------------------------------------------------------------------|
| open | [Entry](../android/os/DropBoxManager.Entry.md) A single entry retrieved from the drop box. |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_DROPBOX_ENTRY_ADDED](DropBoxManager.md) Broadcast Action: This is broadcast when a new entry is added in the dropbox. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DROPPED_COUNT](DropBoxManager.md) Extra for [android.os.DropBoxManager#ACTION_DROPBOX_ENTRY_ADDED](DropBoxManager.md): integer value containing number of broadcasts dropped due to rate limiting on this [android.os.DropBoxManager#EXTRA_TAG](DropBoxManager.md) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_TAG](DropBoxManager.md) Extra for [android.os.DropBoxManager#ACTION_DROPBOX_ENTRY_ADDED](DropBoxManager.md): string containing the dropbox tag. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_TIME](DropBoxManager.md) Extra for [android.os.DropBoxManager#ACTION_DROPBOX_ENTRY_ADDED](DropBoxManager.md): long integer value containing time (in milliseconds since January 1, 1970 00:00:00 UTC) when the entry was created. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IS_EMPTY](DropBoxManager.md) Flag value: Entry's content was deleted to save space. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IS_GZIPPED](DropBoxManager.md) Flag value: Content can be decompressed with java. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IS_TEXT](DropBoxManager.md) Flag value: Content is human-readable UTF-8 text (can be combined with IS_GZIPPED). |

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DropBoxManager](DropBoxManager.md))`()` Create an instance for testing. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addData](DropBoxManager.md))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Stores binary data, which may be ignored or discarded as with [addText](DropBoxManager.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFile](DropBoxManager.md))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `file:` ` [File](../java.io/File.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Stores the contents of a file, which may be ignored or discarded as with [addText](DropBoxManager.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addText](DropBoxManager.md))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Stores human-readable text. |
| --- | --- |
| open [DropBoxManager.Entry](../android/os/DropBoxManager.Entry.md)? | [getNextEntry](DropBoxManager.md))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `msec:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Gets the next entry from the drop box*after*the specified time. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTagEnabled](DropBoxManager.md))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Checks any denylists (set in system settings) to see whether a certain tag is allowed. |

## Constants

### ACTION_DROPBOX_ENTRY_ADDED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_DROPBOX_ENTRY_ADDED: String
```

Broadcast Action: This is broadcast when a new entry is added in the dropbox. For apps targeting 35 and later, For apps targeting Android versions lower than 35, you must hold [android.Manifest.permission#READ_LOGS](../android/Manifest.permission.md). This broadcast can be rate limited for low priority entries

This is a protected intent that can only be sent by the system. 

 Value: "android.intent.action.DROPBOX_ENTRY_ADDED"

### EXTRA_DROPPED_COUNT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_DROPPED_COUNT: String
```

Extra for [android.os.DropBoxManager#ACTION_DROPBOX_ENTRY_ADDED](DropBoxManager.md): integer value containing number of broadcasts dropped due to rate limiting on this [android.os.DropBoxManager#EXTRA_TAG](DropBoxManager.md) 

 Value: "android.os.extra.DROPPED_COUNT"

### EXTRA_TAG

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_TAG: String
```

Extra for [android.os.DropBoxManager#ACTION_DROPBOX_ENTRY_ADDED](DropBoxManager.md): string containing the dropbox tag. 

 Value: "tag"

### EXTRA_TIME

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_TIME: String
```

Extra for [android.os.DropBoxManager#ACTION_DROPBOX_ENTRY_ADDED](DropBoxManager.md): long integer value containing time (in milliseconds since January 1, 1970 00:00:00 UTC) when the entry was created. 

 Value: "time"

### IS_EMPTY

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IS_EMPTY: Int
```

Flag value: Entry's content was deleted to save space. 

 Value: 1

### IS_GZIPPED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IS_GZIPPED: Int
```

Flag value: Content can be decompressed with java.util.zip.GZIPOutputStream. 

 Value: 4

### IS_TEXT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IS_TEXT: Int
```

Flag value: Content is human-readable UTF-8 text (can be combined with IS_GZIPPED). 

 Value: 2

## Protected constructors

### DropBoxManager

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected DropBoxManager()
```

Create an instance for testing. All methods will fail unless overridden with an appropriate mock implementation. To obtain a functional instance, use android.content.Context#getSystemService.

## Public methods

### addData

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addData(
    tag: String, 
    data: ByteArray?, 
    flags: Int
): Unit
```

Stores binary data, which may be ignored or discarded as with [addText](DropBoxManager.md)).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):describing the type of entry being stored This value cannot be`null`. |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:value to store This value may be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):describing the data Value is either`0`or a combination of [android.os.DropBoxManager#IS_EMPTY](DropBoxManager.md), [android.os.DropBoxManager#IS_TEXT](DropBoxManager.md), and [android.os.DropBoxManager#IS_GZIPPED](DropBoxManager.md) |
| --- | --- |

### addFile

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addFile(
    tag: String, 
    file: File, 
    flags: Int
): Unit
```

Stores the contents of a file, which may be ignored or discarded as with [addText](DropBoxManager.md)).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):describing the type of entry being stored This value cannot be`null`. |
| `file` | [File](../java.io/File.md):to read from This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):describing the data Value is either`0`or a combination of [android.os.DropBoxManager#IS_EMPTY](DropBoxManager.md), [android.os.DropBoxManager#IS_TEXT](DropBoxManager.md), and [android.os.DropBoxManager#IS_GZIPPED](DropBoxManager.md) |
| --- | --- |

| Exceptions ||
|-----------------------|-----------------------------|
| `java.io.IOException` | if the file can't be opened |

### addText

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addText(
    tag: String, 
    data: String
): Unit
```

Stores human-readable text. The data may be discarded eventually (or even immediately) if space is limited, or ignored entirely if the tag has been blocked (see [isTagEnabled](DropBoxManager.md))).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):describing the type of entry being stored This value cannot be`null`. |
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):value to store This value cannot be`null`. |

### getNextEntry

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNextEntry(
    tag: String!, 
    msec: Long
): DropBoxManager.Entry?
```

Gets the next entry from the drop box*after* the specified time. You must always call android.os.DropBoxManager.Entry#close() on the return value![android.Manifest.permission#READ_LOGS](../android/Manifest.permission.md) permission is required for apps targeting Android versions lower than 35. 
Requires [android.Manifest.permission#READ_DROPBOX_DATA](../android/Manifest.permission.md) and [android.Manifest.permission#PACKAGE_USAGE_STATS](../android/Manifest.permission.md)

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:of entry to look for, null for all tags |
| `msec` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):time of the last entry seen |

| Return ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [DropBoxManager.Entry](../android/os/DropBoxManager.Entry.md)? | the next entry, or null if there are no more entries |

### isTagEnabled

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isTagEnabled(tag: String!): Boolean
```

Checks any denylists (set in system settings) to see whether a certain tag is allowed. Entries with disabled tags will be dropped immediately, so you can save the work of actually constructing and sending the data.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:that would be used in [addText](DropBoxManager.md))or [addFile](DropBoxManager.md)) |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether events with that tag would be accepted |
