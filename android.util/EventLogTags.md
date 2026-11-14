# EventLogTags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EventLogTags

Kotlin| [Java](https://developer.android.com/reference/android/util/EventLogTags "View this page in Java") 
| --- | --- |

```
open class EventLogTags
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.EventLogTags](https://developer.android.com/reference/kotlin/android/util/EventLogTags#) |

| **This class was deprecated in API level 9.**
|
| This class is no longer functional. Use [android.util.EventLog](https://developer.android.com/reference/kotlin/android/util/EventLog) instead.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------|
| open | [Description](https://developer.android.com/reference/kotlin/android/util/EventLogTags.Description) <br /> |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EventLogTags](https://developer.android.com/reference/kotlin/android/util/EventLogTags#EventLogTags())`()` <br /> |
| [EventLogTags](https://developer.android.com/reference/kotlin/android/util/EventLogTags#EventLogTags(java.io.BufferedReader))`(`input:` ` [BufferedReader](https://developer.android.com/reference/kotlin/java/io/BufferedReader.html#)!`)` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [EventLogTags.Description](https://developer.android.com/reference/kotlin/android/util/EventLogTags.Description)! | [get](https://developer.android.com/reference/kotlin/android/util/EventLogTags#get(kotlin.Int))`(`tag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [EventLogTags.Description](https://developer.android.com/reference/kotlin/android/util/EventLogTags.Description)! | [get](https://developer.android.com/reference/kotlin/android/util/EventLogTags#get(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### EventLogTags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EventLogTags()
```  

### EventLogTags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EventLogTags(input: BufferedReader!)
```

## Public methods

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(tag: Int): EventLogTags.Description!
```

**Deprecated:** *Deprecated in Java.* 

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(name: String!): EventLogTags.Description!
```

**Deprecated:** *Deprecated in Java.*
