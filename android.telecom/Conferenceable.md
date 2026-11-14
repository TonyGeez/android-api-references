# Conferenceable

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Conferenceable

Kotlin| [Java](https://developer.android.com/reference/android/telecom/Conferenceable "View this page in Java") 
| --- | --- |

```
abstract class Conferenceable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telecom.Conferenceable](https://developer.android.com/reference/kotlin/android/telecom/Conferenceable#) |

| Known Direct Subclasses [Conference](https://developer.android.com/reference/kotlin/android/telecom/Conference), [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection) |-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Conference](https://developer.android.com/reference/kotlin/android/telecom/Conference) | Represents a conference call which can contain any number of [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection) objects. | | [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection) | Represents a phone call or connection to a remote endpoint that carries voice and/or video traffic. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface used to identify entities with which another entity can participate in a conference call with. The [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) implementation will only recognize [Conferenceable](https://developer.android.com/reference/kotlin/android/telecom/Conferenceable#) s which are [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection) s or [Conference](https://developer.android.com/reference/kotlin/android/telecom/Conference) s.

## Summary
