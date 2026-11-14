# ClientInfoStatus

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClientInfoStatus

```
class ClientInfoStatus
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.sql.ClientInfoStatus](ClientInfoStatus.md)\> ||
| | ↳ | [java.sql.ClientInfoStatus](ClientInfoStatus.md) |

| Known Direct Subclasses [ClientInfoStatus.REASON_UNKNOWN](ClientInfoStatus.md), [ClientInfoStatus.REASON_UNKNOWN_PROPERTY](ClientInfoStatus.md), [ClientInfoStatus.REASON_VALUE_INVALID](ClientInfoStatus.md), [ClientInfoStatus.REASON_VALUE_TRUNCATED](ClientInfoStatus.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------| | [ClientInfoStatus.REASON_UNKNOWN](ClientInfoStatus.md) | The client info property could not be set for some unknown reason | | [ClientInfoStatus.REASON_UNKNOWN_PROPERTY](ClientInfoStatus.md) | The client info property name specified was not a recognized property name. | | [ClientInfoStatus.REASON_VALUE_INVALID](ClientInfoStatus.md) | The value specified for the client info property was not valid. | | [ClientInfoStatus.REASON_VALUE_TRUNCATED](ClientInfoStatus.md) | The value specified for the client info property was too large. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Enumeration for status of the reason that a property could not be set via a call to`Connection.setClientInfo`

## Summary

| Enum values ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [REASON_UNKNOWN](ClientInfoStatus.md) The client info property could not be set for some unknown reason |
| [REASON_UNKNOWN_PROPERTY](ClientInfoStatus.md) The client info property name specified was not a recognized property name. |
| [REASON_VALUE_INVALID](ClientInfoStatus.md) The value specified for the client info property was not valid. |
| [REASON_VALUE_TRUNCATED](ClientInfoStatus.md) The value specified for the client info property was too large. |

## Enum values

### REASON_UNKNOWN

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val REASON_UNKNOWN : ClientInfoStatus
```

The client info property could not be set for some unknown reason 

### REASON_UNKNOWN_PROPERTY

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val REASON_UNKNOWN_PROPERTY : ClientInfoStatus
```

The client info property name specified was not a recognized property name. 

### REASON_VALUE_INVALID

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val REASON_VALUE_INVALID : ClientInfoStatus
```

The value specified for the client info property was not valid. 

### REASON_VALUE_TRUNCATED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val REASON_VALUE_TRUNCATED : ClientInfoStatus
```

The value specified for the client info property was too large.
