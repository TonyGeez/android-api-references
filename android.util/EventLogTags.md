# EventLogTags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EventLogTags

Kotlin| [Java](EventLogTags.md) 
| --- | --- |

```
open class EventLogTags
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.EventLogTags](EventLogTags.md) |

| **This class was deprecated in API level 9.**
|
| This class is no longer functional. Use [android.util.EventLog](EventLog.md) instead.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------|
| open | [Description](../android/util/EventLogTags.Description.md) <br /> |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EventLogTags](EventLogTags.md))`()` <br /> |
| [EventLogTags](EventLogTags.md))`(`input:` ` [BufferedReader](../java.io/BufferedReader.md)!`)` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [EventLogTags.Description](../android/util/EventLogTags.Description.md)! | [get](EventLogTags.md))`(`tag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [EventLogTags.Description](../android/util/EventLogTags.Description.md)! | [get](EventLogTags.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

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
