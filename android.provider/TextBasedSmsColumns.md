# Telephony.TextBasedSmsColumns

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextBasedSmsColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/Telephony.TextBasedSmsColumns "View this page in Java") 

```
interface TextBasedSmsColumns
```

| [android.provider.Telephony.TextBasedSmsColumns](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#) |

| Known Direct Subclasses [Telephony.Sms](https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms), [Telephony.Sms.Conversations](https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms.Conversations), [Telephony.Sms.Draft](https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms.Draft), [Telephony.Sms.Inbox](https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms.Inbox), [Telephony.Sms.Outbox](https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms.Outbox), [Telephony.Sms.Sent](https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms.Sent) |----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------| | [Telephony.Sms](https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms) | Contains all text-based SMS messages. | | [Telephony.Sms.Conversations](https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms.Conversations) | Contains a view of SMS conversations (also referred to as threads). | | [Telephony.Sms.Draft](https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms.Draft) | Contains all draft text-based SMS messages in the SMS app. | | [Telephony.Sms.Inbox](https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms.Inbox) | Contains all text-based SMS messages in the SMS app inbox. | | [Telephony.Sms.Outbox](https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms.Outbox) | Contains all pending outgoing text-based SMS messages. | | [Telephony.Sms.Sent](https://developer.android.com/reference/kotlin/android/provider/Telephony.Sms.Sent) | Contains all sent text-based SMS messages in the SMS app. | |

Base columns for tables that contain text-based SMSs.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ADDRESS](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#ADDRESS:kotlin.String) The address of the other party. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [BODY](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#BODY:kotlin.String) The body of the message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CREATOR](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#CREATOR:kotlin.String) The identity of the sender of a sent message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATE](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#DATE:kotlin.String) The date the message was received. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATE_SENT](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#DATE_SENT:kotlin.String) The date the message was sent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ERROR_CODE](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#ERROR_CODE:kotlin.String) Error code associated with sending or receiving this message |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LOCKED](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#LOCKED:kotlin.String) Is the message locked? |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MESSAGE_TYPE_ALL](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#MESSAGE_TYPE_ALL:kotlin.Int) Message type: all messages. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MESSAGE_TYPE_DRAFT](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#MESSAGE_TYPE_DRAFT:kotlin.Int) Message type: drafts. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MESSAGE_TYPE_FAILED](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#MESSAGE_TYPE_FAILED:kotlin.Int) Message type: failed outgoing message. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MESSAGE_TYPE_INBOX](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#MESSAGE_TYPE_INBOX:kotlin.Int) Message type: inbox. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MESSAGE_TYPE_OUTBOX](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#MESSAGE_TYPE_OUTBOX:kotlin.Int) Message type: outbox. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MESSAGE_TYPE_QUEUED](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#MESSAGE_TYPE_QUEUED:kotlin.Int) Message type: queued to send later. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MESSAGE_TYPE_SENT](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#MESSAGE_TYPE_SENT:kotlin.Int) Message type: sent messages. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PERSON](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#PERSON:kotlin.String) The ID of the sender of the conversation, if present. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROTOCOL](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#PROTOCOL:kotlin.String) The protocol identifier code. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [READ](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#READ:kotlin.String) Has the message been read? |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REPLY_PATH_PRESENT](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#REPLY_PATH_PRESENT:kotlin.String) Is the`TP-Reply-Path`flag set? |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SEEN](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#SEEN:kotlin.String) Has the message been seen by the user? The "seen" flag determines whether we need to show a notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SERVICE_CENTER](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#SERVICE_CENTER:kotlin.String) The service center (SC) through which to send the message, if present. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STATUS](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#STATUS:kotlin.String) `TP-Status`value for the message, or -1 if no status has been received. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_COMPLETE](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#STATUS_COMPLETE:kotlin.Int) TP-Status: complete. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_FAILED](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#STATUS_FAILED:kotlin.Int) TP-Status: failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_NONE](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#STATUS_NONE:kotlin.Int) TP-Status: no status received. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_PENDING](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#STATUS_PENDING:kotlin.Int) TP-Status: pending. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUBJECT](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#SUBJECT:kotlin.String) The subject of the message, if present. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUBSCRIPTION_ID](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#SUBSCRIPTION_ID:kotlin.String) The subscription to which the message belongs to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [THREAD_ID](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#THREAD_ID:kotlin.String) The thread ID of the message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns#TYPE:kotlin.String) The type of message. |

## Constants

### ADDRESS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADDRESS: String
```

The address of the other party.

Type: TEXT 

 Value: "address"

### BODY

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BODY: String
```

The body of the message.

Type: TEXT 

 Value: "body"

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: String
```

The identity of the sender of a sent message. It is usually the package name of the app which sends the message.

**Note:**This column is read-only. It is set by the provider and can not be changed by apps.

Type: TEXT 

 Value: "creator"

### DATE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATE: String
```

The date the message was received.

Type: INTEGER (long) 

 Value: "date"

### DATE_SENT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATE_SENT: String
```

The date the message was sent.

Type: INTEGER (long) 

 Value: "date_sent"

### ERROR_CODE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CODE: String
```

Error code associated with sending or receiving this message

Type: INTEGER 

 Value: "error_code"

### LOCKED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCKED: String
```

Is the message locked?

Type: INTEGER (boolean) 

 Value: "locked"

### MESSAGE_TYPE_ALL

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_TYPE_ALL: Int
```

Message type: all messages. 

 Value: 0

### MESSAGE_TYPE_DRAFT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_TYPE_DRAFT: Int
```

Message type: drafts. 

 Value: 3

### MESSAGE_TYPE_FAILED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_TYPE_FAILED: Int
```

Message type: failed outgoing message. 

 Value: 5

### MESSAGE_TYPE_INBOX

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_TYPE_INBOX: Int
```

Message type: inbox. 

 Value: 1

### MESSAGE_TYPE_OUTBOX

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_TYPE_OUTBOX: Int
```

Message type: outbox. 

 Value: 4

### MESSAGE_TYPE_QUEUED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_TYPE_QUEUED: Int
```

Message type: queued to send later. 

 Value: 6

### MESSAGE_TYPE_SENT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_TYPE_SENT: Int
```

Message type: sent messages. 

 Value: 2

### PERSON

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERSON: String
```

The ID of the sender of the conversation, if present.

Type: INTEGER (reference to item in`content://contacts/people`) 

 Value: "person"

### PROTOCOL

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROTOCOL: String
```

The protocol identifier code.

Type: INTEGER 

 Value: "protocol"

### READ

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val READ: String
```

Has the message been read?

Type: INTEGER (boolean) 

 Value: "read"

### REPLY_PATH_PRESENT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPLY_PATH_PRESENT: String
```

Is the`TP-Reply-Path`flag set?

Type: BOOLEAN 

 Value: "reply_path_present"

### SEEN

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEEN: String
```

Has the message been seen by the user? The "seen" flag determines whether we need to show a notification.

Type: INTEGER (boolean) 

 Value: "seen"

### SERVICE_CENTER

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_CENTER: String
```

The service center (SC) through which to send the message, if present.

Type: TEXT 

 Value: "service_center"

### STATUS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS: String
```

`TP-Status`value for the message, or -1 if no status has been received.

Type: INTEGER 

 Value: "status"

### STATUS_COMPLETE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_COMPLETE: Int
```

TP-Status: complete. 

 Value: 0

### STATUS_FAILED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_FAILED: Int
```

TP-Status: failed. 

 Value: 64

### STATUS_NONE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_NONE: Int
```

TP-Status: no status received. 

 Value: -1

### STATUS_PENDING

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_PENDING: Int
```

TP-Status: pending. 

 Value: 32

### SUBJECT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBJECT: String
```

The subject of the message, if present.

Type: TEXT 

 Value: "subject"

### SUBSCRIPTION_ID

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBSCRIPTION_ID: String
```

The subscription to which the message belongs to. Its value will be \< 0 if the sub id cannot be determined.

Type: INTEGER (long) 

 Value: "sub_id"

### THREAD_ID

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val THREAD_ID: String
```

The thread ID of the message.

Type: INTEGER 

 Value: "thread_id"

### TYPE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE: String
```

The type of message.

Type: INTEGER 

 Value: "type"
