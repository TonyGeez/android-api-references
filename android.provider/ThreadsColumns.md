# Telephony.ThreadsColumns

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ThreadsColumns

Kotlin| [Java](../android/provider/Telephony.ThreadsColumns.md) 
| --- | --- |

```
interface ThreadsColumns : BaseColumns
```

| [android.provider.Telephony.ThreadsColumns](../android/provider/Telephony.ThreadsColumns.md) |

| Known Direct Subclasses [Telephony.Threads](../android/provider/Telephony.Threads.md) |--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------| | [Telephony.Threads](../android/provider/Telephony.Threads.md) | Helper functions for the "threads" table used by MMS and SMS. | |
| --- | --- | --- | --- | --- | --- | --- |

Columns for the "threads" table used by MMS and SMS.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ARCHIVED](../android/provider/Telephony.ThreadsColumns.md) If the thread is archived |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATE](../android/provider/Telephony.ThreadsColumns.md) The date at which the thread was created. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ERROR](../android/provider/Telephony.ThreadsColumns.md) Indicates whether there is a transmission error in the thread. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [HAS_ATTACHMENT](../android/provider/Telephony.ThreadsColumns.md) Indicates whether this thread contains any attachments. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MESSAGE_COUNT](../android/provider/Telephony.ThreadsColumns.md) The message count of the thread. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [READ](../android/provider/Telephony.ThreadsColumns.md) Indicates whether all messages of the thread have been read. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RECIPIENT_IDS](../android/provider/Telephony.ThreadsColumns.md) A string encoding of the recipient IDs of the recipients of the message, in numerical order and separated by spaces. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SNIPPET](../android/provider/Telephony.ThreadsColumns.md) The snippet of the latest message in the thread. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SNIPPET_CHARSET](../android/provider/Telephony.ThreadsColumns.md) The charset of the snippet. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE](../android/provider/Telephony.ThreadsColumns.md) Type of the thread, either [Threads.COMMON_THREAD](../android/provider/Telephony.Threads.md) or [Threads.BROADCAST_THREAD](../android/provider/Telephony.Threads.md). |

| Inherited constants ||
|---|---|
| From class [BaseColumns](BaseColumns.md) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_COUNT](BaseColumns.md) <br /> The count of rows in a directory. Type: INTEGER <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_ID](BaseColumns.md) <br /> The unique ID for a row. Type: INTEGER (long) <br /> | ||

## Constants

### ARCHIVED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ARCHIVED: String
```

If the thread is archived

Type: INTEGER (boolean) 

 Value: "archived"

### DATE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATE: String
```

The date at which the thread was created.

Type: INTEGER (long) 

 Value: "date"

### ERROR

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR: String
```

Indicates whether there is a transmission error in the thread.

Type: INTEGER 

 Value: "error"

### HAS_ATTACHMENT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HAS_ATTACHMENT: String
```

Indicates whether this thread contains any attachments.

Type: INTEGER 

 Value: "has_attachment"

### MESSAGE_COUNT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_COUNT: String
```

The message count of the thread.

Type: INTEGER 

 Value: "message_count"

### READ

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val READ: String
```

Indicates whether all messages of the thread have been read.

Type: INTEGER 

 Value: "read"

### RECIPIENT_IDS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RECIPIENT_IDS: String
```

A string encoding of the recipient IDs of the recipients of the message, in numerical order and separated by spaces.

Type: TEXT 

 Value: "recipient_ids"

### SNIPPET

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SNIPPET: String
```

The snippet of the latest message in the thread.

Type: TEXT 

 Value: "snippet"

### SNIPPET_CHARSET

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SNIPPET_CHARSET: String
```

The charset of the snippet.

Type: INTEGER 

 Value: "snippet_cs"

### TYPE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE: String
```

Type of the thread, either [Threads.COMMON_THREAD](../android/provider/Telephony.Threads.md) or [Threads.BROADCAST_THREAD](../android/provider/Telephony.Threads.md).

Type: INTEGER 

 Value: "type"
