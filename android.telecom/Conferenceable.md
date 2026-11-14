# Conferenceable

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Conferenceable

Kotlin| [Java](Conferenceable.md) 
| --- | --- |

```
abstract class Conferenceable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telecom.Conferenceable](Conferenceable.md) |

| Known Direct Subclasses [Conference](Conference.md), [Connection](Connection.md) |-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Conference](Conference.md) | Represents a conference call which can contain any number of [Connection](Connection.md) objects. | | [Connection](Connection.md) | Represents a phone call or connection to a remote endpoint that carries voice and/or video traffic. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface used to identify entities with which another entity can participate in a conference call with. The [ConnectionService](ConnectionService.md) implementation will only recognize [Conferenceable](Conferenceable.md) s which are [Connection](Connection.md) s or [Conference](Conference.md) s.

## Summary
