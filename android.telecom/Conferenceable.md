# Conferenceable

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Conferenceable

Kotlin| [Java](../android/telecom/Conferenceable.md) 
| --- | --- |

```
abstract class Conferenceable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telecom.Conferenceable](../android/telecom/Conferenceable.md) |

| Known Direct Subclasses [Conference](../android/telecom/Conference.md), [Connection](../android/telecom/Connection.md) |-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Conference](../android/telecom/Conference.md) | Represents a conference call which can contain any number of [Connection](../android/telecom/Connection.md) objects. | | [Connection](../android/telecom/Connection.md) | Represents a phone call or connection to a remote endpoint that carries voice and/or video traffic. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface used to identify entities with which another entity can participate in a conference call with. The [ConnectionService](../android/telecom/ConnectionService.md) implementation will only recognize [Conferenceable](../android/telecom/Conferenceable.md) s which are [Connection](../android/telecom/Connection.md) s or [Conference](../android/telecom/Conference.md) s.

## Summary
