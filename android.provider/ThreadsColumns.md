# Telephony.ThreadsColumns

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ThreadsColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/Telephony.ThreadsColumns "View this page in Java") 
| --- | --- |

```
interface ThreadsColumns : BaseColumns
```

| [android.provider.Telephony.ThreadsColumns](https://developer.android.com/reference/kotlin/android/provider/Telephony.ThreadsColumns#) |

| Known Direct Subclasses [Telephony.Threads](https://developer.android.com/reference/kotlin/android/provider/Telephony.Threads) |--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------| | [Telephony.Threads](https://developer.android.com/reference/kotlin/android/provider/Telephony.Threads) | Helper functions for the "threads" table used by MMS and SMS. | |
| --- | --- | --- | --- | --- | --- | --- |

Columns for the "threads" table used by MMS and SMS.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ARCHIVED](https://developer.android.com/reference/kotlin/android/provider/Telephony.ThreadsColumns#ARCHIVED:kotlin.String) If the thread is archived |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATE](https://developer.android.com/reference/kotlin/android/provider/Telephony.ThreadsColumns#DATE:kotlin.String) The date at which the thread was created. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ERROR](https://developer.android.com/reference/kotlin/android/provider/Telephony.ThreadsColumns#ERROR:kotlin.String) Indicates whether there is a transmission error in the thread. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [HAS_ATTACHMENT](https://developer.android.com/reference/kotlin/android/provider/Telephony.ThreadsColumns#HAS_ATTACHMENT:kotlin.String) Indicates whether this thread contains any attachments. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MESSAGE_COUNT](https://developer.android.com/reference/kotlin/android/provider/Telephony.ThreadsColumns#MESSAGE_COUNT:kotlin.String) The message count of the thread. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [READ](https://developer.android.com/reference/kotlin/android/provider/Telephony.ThreadsColumns#READ:kotlin.String) Indicates whether all messages of the thread have been read. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RECIPIENT_IDS](https://developer.android.com/reference/kotlin/android/provider/Telephony.ThreadsColumns#RECIPIENT_IDS:kotlin.String) A string encoding of the recipient IDs of the recipients of the message, in numerical order and separated by spaces. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SNIPPET](https://developer.android.com/reference/kotlin/android/provider/Telephony.ThreadsColumns#SNIPPET:kotlin.String) The snippet of the latest message in the thread. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SNIPPET_CHARSET](https://developer.android.com/reference/kotlin/android/provider/Telephony.ThreadsColumns#SNIPPET_CHARSET:kotlin.String) The charset of the snippet. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE](https://developer.android.com/reference/kotlin/android/provider/Telephony.ThreadsColumns#TYPE:kotlin.String) Type of the thread, either [Threads.COMMON_THREAD](https://developer.android.com/reference/kotlin/android/provider/Telephony.Threads#COMMON_THREAD:kotlin.Int) or [Threads.BROADCAST_THREAD](https://developer.android.com/reference/kotlin/android/provider/Telephony.Threads#BROADCAST_THREAD:kotlin.Int). |

| Inherited constants ||
|---|---|
| From class [BaseColumns](https://developer.android.com/reference/kotlin/android/provider/BaseColumns) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_COUNT](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_COUNT:kotlin.String) <br /> The count of rows in a directory. Type: INTEGER <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_ID](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String) <br /> The unique ID for a row. Type: INTEGER (long) <br /> | ||

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

Type of the thread, either [Threads.COMMON_THREAD](https://developer.android.com/reference/kotlin/android/provider/Telephony.Threads#COMMON_THREAD:kotlin.Int) or [Threads.BROADCAST_THREAD](https://developer.android.com/reference/kotlin/android/provider/Telephony.Threads#BROADCAST_THREAD:kotlin.Int).

Type: INTEGER 

 Value: "type"
