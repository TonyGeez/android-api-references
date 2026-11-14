# ClientInfoStatus

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClientInfoStatus

```
class ClientInfoStatus
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.sql.ClientInfoStatus](https://developer.android.com/reference/kotlin/java/sql/ClientInfoStatus#)\> ||
| | ↳ | [java.sql.ClientInfoStatus](https://developer.android.com/reference/kotlin/java/sql/ClientInfoStatus#) |

| Known Direct Subclasses [ClientInfoStatus.REASON_UNKNOWN](https://developer.android.com/reference/kotlin/java/sql/ClientInfoStatus#ENUM_VALUE:REASON_UNKNOWN), [ClientInfoStatus.REASON_UNKNOWN_PROPERTY](https://developer.android.com/reference/kotlin/java/sql/ClientInfoStatus#ENUM_VALUE:REASON_UNKNOWN_PROPERTY), [ClientInfoStatus.REASON_VALUE_INVALID](https://developer.android.com/reference/kotlin/java/sql/ClientInfoStatus#ENUM_VALUE:REASON_VALUE_INVALID), [ClientInfoStatus.REASON_VALUE_TRUNCATED](https://developer.android.com/reference/kotlin/java/sql/ClientInfoStatus#ENUM_VALUE:REASON_VALUE_TRUNCATED) |---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------| | [ClientInfoStatus.REASON_UNKNOWN](https://developer.android.com/reference/kotlin/java/sql/ClientInfoStatus#ENUM_VALUE:REASON_UNKNOWN) | The client info property could not be set for some unknown reason | | [ClientInfoStatus.REASON_UNKNOWN_PROPERTY](https://developer.android.com/reference/kotlin/java/sql/ClientInfoStatus#ENUM_VALUE:REASON_UNKNOWN_PROPERTY) | The client info property name specified was not a recognized property name. | | [ClientInfoStatus.REASON_VALUE_INVALID](https://developer.android.com/reference/kotlin/java/sql/ClientInfoStatus#ENUM_VALUE:REASON_VALUE_INVALID) | The value specified for the client info property was not valid. | | [ClientInfoStatus.REASON_VALUE_TRUNCATED](https://developer.android.com/reference/kotlin/java/sql/ClientInfoStatus#ENUM_VALUE:REASON_VALUE_TRUNCATED) | The value specified for the client info property was too large. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Enumeration for status of the reason that a property could not be set via a call to`Connection.setClientInfo`

## Summary

| Enum values ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [REASON_UNKNOWN](https://developer.android.com/reference/kotlin/java/sql/ClientInfoStatus#ENUM_VALUE:REASON_UNKNOWN) The client info property could not be set for some unknown reason |
| [REASON_UNKNOWN_PROPERTY](https://developer.android.com/reference/kotlin/java/sql/ClientInfoStatus#ENUM_VALUE:REASON_UNKNOWN_PROPERTY) The client info property name specified was not a recognized property name. |
| [REASON_VALUE_INVALID](https://developer.android.com/reference/kotlin/java/sql/ClientInfoStatus#ENUM_VALUE:REASON_VALUE_INVALID) The value specified for the client info property was not valid. |
| [REASON_VALUE_TRUNCATED](https://developer.android.com/reference/kotlin/java/sql/ClientInfoStatus#ENUM_VALUE:REASON_VALUE_TRUNCATED) The value specified for the client info property was too large. |

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
