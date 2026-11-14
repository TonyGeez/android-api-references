# Telephony.BaseMmsColumns

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseMmsColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/Telephony.BaseMmsColumns "View this page in Java") 
| --- | --- |

```
interface BaseMmsColumns : BaseColumns
```

| [android.provider.Telephony.BaseMmsColumns](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#) |

| Known Direct Subclasses [Telephony.Mms](https://developer.android.com/reference/kotlin/android/provider/Telephony.Mms), [Telephony.Mms.Draft](https://developer.android.com/reference/kotlin/android/provider/Telephony.Mms.Draft), [Telephony.Mms.Inbox](https://developer.android.com/reference/kotlin/android/provider/Telephony.Mms.Inbox), [Telephony.Mms.Outbox](https://developer.android.com/reference/kotlin/android/provider/Telephony.Mms.Outbox), [Telephony.Mms.Sent](https://developer.android.com/reference/kotlin/android/provider/Telephony.Mms.Sent) |--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------| | [Telephony.Mms](https://developer.android.com/reference/kotlin/android/provider/Telephony.Mms) | Contains all MMS messages. | | [Telephony.Mms.Draft](https://developer.android.com/reference/kotlin/android/provider/Telephony.Mms.Draft) | Contains all MMS messages in the MMS app drafts folder. | | [Telephony.Mms.Inbox](https://developer.android.com/reference/kotlin/android/provider/Telephony.Mms.Inbox) | Contains all MMS messages in the MMS app inbox. | | [Telephony.Mms.Outbox](https://developer.android.com/reference/kotlin/android/provider/Telephony.Mms.Outbox) | Contains all MMS messages in the MMS app outbox. | | [Telephony.Mms.Sent](https://developer.android.com/reference/kotlin/android/provider/Telephony.Mms.Sent) | Contains all MMS messages in the MMS app sent folder. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base columns for tables that contain MMSs.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTENT_CLASS](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#CONTENT_CLASS:kotlin.String) The`content-class`of the message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTENT_LOCATION](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#CONTENT_LOCATION:kotlin.String) The`Content-Location`of the message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#CONTENT_TYPE:kotlin.String) The`Content-Type`of the message. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CREATOR](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#CREATOR:kotlin.String) The identity of the sender of a sent message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATE](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#DATE:kotlin.String) The date the message was received. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATE_SENT](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#DATE_SENT:kotlin.String) The date the message was sent. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DELIVERY_REPORT](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#DELIVERY_REPORT:kotlin.String) The`delivery-report`of the message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DELIVERY_TIME](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#DELIVERY_TIME:kotlin.String) The`delivery-time`of the message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXPIRY](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#EXPIRY:kotlin.String) The expiry time of the message. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LOCKED](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#LOCKED:kotlin.String) Is the message locked? |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MESSAGE_BOX](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#MESSAGE_BOX:kotlin.String) The box which the message belongs to, e. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MESSAGE_BOX_ALL](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#MESSAGE_BOX_ALL:kotlin.Int) Message box: all messages. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MESSAGE_BOX_DRAFTS](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#MESSAGE_BOX_DRAFTS:kotlin.Int) Message box: drafts. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MESSAGE_BOX_FAILED](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#MESSAGE_BOX_FAILED:kotlin.Int) Message box: failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MESSAGE_BOX_INBOX](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#MESSAGE_BOX_INBOX:kotlin.Int) Message box: inbox. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MESSAGE_BOX_OUTBOX](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#MESSAGE_BOX_OUTBOX:kotlin.Int) Message box: outbox. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MESSAGE_BOX_SENT](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#MESSAGE_BOX_SENT:kotlin.Int) Message box: sent messages. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MESSAGE_CLASS](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#MESSAGE_CLASS:kotlin.String) The class of the message. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MESSAGE_ID](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#MESSAGE_ID:kotlin.String) The`Message-ID`of the message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MESSAGE_SIZE](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#MESSAGE_SIZE:kotlin.String) The size of the message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MESSAGE_TYPE](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#MESSAGE_TYPE:kotlin.String) The type of the message defined by MMS spec. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MMS_VERSION](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#MMS_VERSION:kotlin.String) The version of the specification that this message conforms to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PRIORITY](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#PRIORITY:kotlin.String) The priority of the message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [READ](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#READ:kotlin.String) Has the message been read? |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [READ_REPORT](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#READ_REPORT:kotlin.String) The`read-report`of the message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [READ_STATUS](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#READ_STATUS:kotlin.String) The`read-status`of the message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REPORT_ALLOWED](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#REPORT_ALLOWED:kotlin.String) Is read report allowed? |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RESPONSE_STATUS](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#RESPONSE_STATUS:kotlin.String) The`response-status`of the message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RESPONSE_TEXT](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#RESPONSE_TEXT:kotlin.String) The`response-text`of the message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RETRIEVE_STATUS](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#RETRIEVE_STATUS:kotlin.String) The`retrieve-status`of the message. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RETRIEVE_TEXT](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#RETRIEVE_TEXT:kotlin.String) The`retrieve-text`of the message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RETRIEVE_TEXT_CHARSET](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#RETRIEVE_TEXT_CHARSET:kotlin.String) The character set of the retrieve-text. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SEEN](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#SEEN:kotlin.String) Has the message been seen by the user? The "seen" flag determines whether we need to show a new message notification. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STATUS](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#STATUS:kotlin.String) The`status`of the message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUBJECT](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#SUBJECT:kotlin.String) The subject of the message, if present. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUBJECT_CHARSET](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#SUBJECT_CHARSET:kotlin.String) The character set of the subject, if present. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUBSCRIPTION_ID](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#SUBSCRIPTION_ID:kotlin.String) The subscription to which the message belongs to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TEXT_ONLY](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#TEXT_ONLY:kotlin.String) Does the message have only a text part (can also have a subject) with no picture, slideshow, sound, etc. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [THREAD_ID](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#THREAD_ID:kotlin.String) The thread ID of the message. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TRANSACTION_ID](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#TRANSACTION_ID:kotlin.String) The`transaction-id`of the message. |

| Inherited constants ||
|---|---|
| From class [BaseColumns](https://developer.android.com/reference/kotlin/android/provider/BaseColumns) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_COUNT](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_COUNT:kotlin.String) <br /> The count of rows in a directory. Type: INTEGER <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_ID](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String) <br /> The unique ID for a row. Type: INTEGER (long) <br /> | ||

## Constants

### CONTENT_CLASS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CLASS: String
```

The`content-class`of the message.

Type: INTEGER 

 Value: "ct_cls"

### CONTENT_LOCATION

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_LOCATION: String
```

The`Content-Location`of the message.

Type: TEXT 

 Value: "ct_l"

### CONTENT_TYPE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE: String
```

The`Content-Type`of the message.

Type: TEXT 

 Value: "ct_t"

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

### DELIVERY_REPORT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DELIVERY_REPORT: String
```

The`delivery-report`of the message.

Type: INTEGER 

 Value: "d_rpt"

### DELIVERY_TIME

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DELIVERY_TIME: String
```

The`delivery-time`of the message.

Type: INTEGER 

 Value: "d_tm"

### EXPIRY

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXPIRY: String
```

The expiry time of the message.

Type: INTEGER (long) 

 Value: "exp"

### LOCKED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCKED: String
```

Is the message locked?

Type: INTEGER (boolean) 

 Value: "locked"

### MESSAGE_BOX

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_BOX: String
```

The box which the message belongs to, e.g. [MESSAGE_BOX_INBOX](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns#MESSAGE_BOX_INBOX:kotlin.Int).

Type: INTEGER 

 Value: "msg_box"

### MESSAGE_BOX_ALL

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_BOX_ALL: Int
```

Message box: all messages. 

 Value: 0

### MESSAGE_BOX_DRAFTS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_BOX_DRAFTS: Int
```

Message box: drafts. 

 Value: 3

### MESSAGE_BOX_FAILED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_BOX_FAILED: Int
```

Message box: failed. 

 Value: 5

### MESSAGE_BOX_INBOX

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_BOX_INBOX: Int
```

Message box: inbox. 

 Value: 1

### MESSAGE_BOX_OUTBOX

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_BOX_OUTBOX: Int
```

Message box: outbox. 

 Value: 4

### MESSAGE_BOX_SENT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_BOX_SENT: Int
```

Message box: sent messages. 

 Value: 2

### MESSAGE_CLASS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_CLASS: String
```

The class of the message.

Type: TEXT 

 Value: "m_cls"

### MESSAGE_ID

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_ID: String
```

The`Message-ID`of the message.

Type: TEXT 

 Value: "m_id"

### MESSAGE_SIZE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_SIZE: String
```

The size of the message.

Type: INTEGER 

 Value: "m_size"

### MESSAGE_TYPE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MESSAGE_TYPE: String
```

The type of the message defined by MMS spec.

Type: INTEGER 

 Value: "m_type"

### MMS_VERSION

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MMS_VERSION: String
```

The version of the specification that this message conforms to.

Type: INTEGER 

 Value: "v"

### PRIORITY

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIORITY: String
```

The priority of the message.

Type: INTEGER 

 Value: "pri"

### READ

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val READ: String
```

Has the message been read?

Type: INTEGER (boolean) 

 Value: "read"

### READ_REPORT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val READ_REPORT: String
```

The`read-report`of the message.

Type: INTEGER (boolean) 

 Value: "rr"

### READ_STATUS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val READ_STATUS: String
```

The`read-status`of the message.

Type: INTEGER 

 Value: "read_status"

### REPORT_ALLOWED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPORT_ALLOWED: String
```

Is read report allowed?

Type: INTEGER (boolean) 

 Value: "rpt_a"

### RESPONSE_STATUS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_STATUS: String
```

The`response-status`of the message.

Type: INTEGER 

 Value: "resp_st"

### RESPONSE_TEXT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_TEXT: String
```

The`response-text`of the message.

Type: TEXT 

 Value: "resp_txt"

### RETRIEVE_STATUS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RETRIEVE_STATUS: String
```

The`retrieve-status`of the message.

Type: INTEGER 

 Value: "retr_st"

### RETRIEVE_TEXT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RETRIEVE_TEXT: String
```

The`retrieve-text`of the message.

Type: TEXT 

 Value: "retr_txt"

### RETRIEVE_TEXT_CHARSET

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RETRIEVE_TEXT_CHARSET: String
```

The character set of the retrieve-text.

Type: INTEGER 

 Value: "retr_txt_cs"

### SEEN

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEEN: String
```

Has the message been seen by the user? The "seen" flag determines whether we need to show a new message notification.

Type: INTEGER (boolean) 

 Value: "seen"

### STATUS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS: String
```

The`status`of the message.

Type: INTEGER 

 Value: "st"

### SUBJECT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBJECT: String
```

The subject of the message, if present.

Type: TEXT 

 Value: "sub"

### SUBJECT_CHARSET

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBJECT_CHARSET: String
```

The character set of the subject, if present.

Type: INTEGER 

 Value: "sub_cs"

### SUBSCRIPTION_ID

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBSCRIPTION_ID: String
```

The subscription to which the message belongs to. Its value will be \< 0 if the sub id cannot be determined.

Type: INTEGER (long) 

 Value: "sub_id"

### TEXT_ONLY

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TEXT_ONLY: String
```

Does the message have only a text part (can also have a subject) with no picture, slideshow, sound, etc. parts?

Type: INTEGER (boolean) 

 Value: "text_only"

### THREAD_ID

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val THREAD_ID: String
```

The thread ID of the message.

Type: INTEGER (long) 

 Value: "thread_id"

### TRANSACTION_ID

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSACTION_ID: String
```

The`transaction-id`of the message.

Type: TEXT 

 Value: "tr_id"
