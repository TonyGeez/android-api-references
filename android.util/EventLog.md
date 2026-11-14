# EventLog

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EventLog

Kotlin| [Java](https://developer.android.com/reference/android/util/EventLog "View this page in Java") 
| --- | --- |

```
open class EventLog
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.EventLog](https://developer.android.com/reference/kotlin/android/util/EventLog#) |

Access to the system diagnostic event record. System diagnostic events are used to record certain system-level events (such as garbage collection, activity manager state, system watchdogs, and other low level activity), which may be automatically collected and analyzed during system development.

This is**not** the main "logcat" debugging log ([android.util.Log](https://developer.android.com/reference/kotlin/android/util/Log))! These diagnostic events are for system integrators, not application authors.

Events use integer tag codes corresponding to /system/etc/event-log-tags. They carry a payload of one or more int, long, or String values. The event-log-tags file defines the payload contents for each type code.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------|
| | [Event](https://developer.android.com/reference/kotlin/android/util/EventLog.Event) A previously logged event read from the logs. |

| Public methods ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTagCode](https://developer.android.com/reference/kotlin/android/util/EventLog#getTagCode(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get the event type tag code associated with an event name. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTagName](https://developer.android.com/reference/kotlin/android/util/EventLog#getTagName(kotlin.Int))`(`tag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the name associated with an event type tag code. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readEvents](https://developer.android.com/reference/kotlin/android/util/EventLog#readEvents(kotlin.IntArray,%20kotlin.collections.MutableCollection))`(`tags:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `output:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [EventLog.Event](https://developer.android.com/reference/kotlin/android/util/EventLog.Event)!>!`)` Read events from the log, filtered by type. |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [writeEvent](https://developer.android.com/reference/kotlin/android/util/EventLog#writeEvent(kotlin.Int,%20kotlin.Float))`(`tag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Record an event log message. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [writeEvent](https://developer.android.com/reference/kotlin/android/util/EventLog#writeEvent(kotlin.Int,%20kotlin.Int))`(`tag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Record an event log message. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [writeEvent](https://developer.android.com/reference/kotlin/android/util/EventLog#writeEvent(kotlin.Int,%20kotlin.Any))`(`tag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `vararg` `list:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Record an event log message. |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [writeEvent](https://developer.android.com/reference/kotlin/android/util/EventLog#writeEvent(kotlin.Int,%20kotlin.String))`(`tag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Record an event log message. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [writeEvent](https://developer.android.com/reference/kotlin/android/util/EventLog#writeEvent(kotlin.Int,%20kotlin.Long))`(`tag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Record an event log message. |

## Public methods

### getTagCode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTagCode(name: String!): Int
```

Get the event type tag code associated with an event name.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:of event to look up |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the tag code, or -1 if no tag has that name |

### getTagName

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTagName(tag: Int): String!
```

Get the name associated with an event type tag code.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------|
| `tag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code to look up |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the tag, or null if no tag has that number |

### readEvents

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun readEvents(
    tags: IntArray!, 
    output: MutableCollection<EventLog.Event!>!
): Unit
```

Read events from the log, filtered by type.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tags` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:to search for |
| `output` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [EventLog.Event](https://developer.android.com/reference/kotlin/android/util/EventLog.Event)!\>!:container to add events into |

| Exceptions ||
|-----------------------|----------------------------------------|
| `java.io.IOException` | if something goes wrong reading events |

### writeEvent

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun writeEvent(
    tag: Int, 
    value: Float
): Int
```

Record an event log message.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------|
| `tag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The event type tag code |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):A value to log |

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of bytes written |

### writeEvent

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun writeEvent(
    tag: Int, 
    value: Int
): Int
```

Record an event log message.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------|
| `tag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The event type tag code |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A value to log |

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of bytes written |

### writeEvent

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun writeEvent(
    tag: Int, 
    vararg list: Any!
): Int
```

Record an event log message.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------|
| `tag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The event type tag code |
| `list` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:A list of values to log |

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of bytes written |

### writeEvent

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun writeEvent(
    tag: Int, 
    str: String!
): Int
```

Record an event log message.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------|
| `tag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The event type tag code |
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A value to log |

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of bytes written |

### writeEvent

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun writeEvent(
    tag: Int, 
    value: Long
): Int
```

Record an event log message.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------|
| `tag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The event type tag code |
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):A value to log |

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of bytes written |
