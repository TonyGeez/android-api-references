# RowIdLifetime

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RowIdLifetime

```
class RowIdLifetime
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.sql.RowIdLifetime](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime#)\> ||
| | ↳ | [java.sql.RowIdLifetime](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime#) |

| Known Direct Subclasses [RowIdLifetime.ROWID_UNSUPPORTED](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime#ENUM_VALUE:ROWID_UNSUPPORTED), [RowIdLifetime.ROWID_VALID_FOREVER](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime#ENUM_VALUE:ROWID_VALID_FOREVER), [RowIdLifetime.ROWID_VALID_OTHER](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime#ENUM_VALUE:ROWID_VALID_OTHER), [RowIdLifetime.ROWID_VALID_SESSION](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime#ENUM_VALUE:ROWID_VALID_SESSION), [RowIdLifetime.ROWID_VALID_TRANSACTION](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime#ENUM_VALUE:ROWID_VALID_TRANSACTION) |---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RowIdLifetime.ROWID_UNSUPPORTED](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime#ENUM_VALUE:ROWID_UNSUPPORTED) | Indicates that this data source does not support the ROWID type. | | [RowIdLifetime.ROWID_VALID_FOREVER](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime#ENUM_VALUE:ROWID_VALID_FOREVER) | Indicates that the lifetime of a RowId from this data source is, effectively, unlimited. | | [RowIdLifetime.ROWID_VALID_OTHER](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime#ENUM_VALUE:ROWID_VALID_OTHER) | Indicates that the lifetime of a RowId from this data source is indeterminate; but not one of ROWID_VALID_TRANSACTION, ROWID_VALID_SESSION, or, ROWID_VALID_FOREVER. | | [RowIdLifetime.ROWID_VALID_SESSION](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime#ENUM_VALUE:ROWID_VALID_SESSION) | Indicates that the lifetime of a RowId from this data source is at least the containing session. | | [RowIdLifetime.ROWID_VALID_TRANSACTION](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime#ENUM_VALUE:ROWID_VALID_TRANSACTION) | Indicates that the lifetime of a RowId from this data source is at least the containing transaction. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Enumeration for RowId life-time values.

## Summary

| Enum values ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ROWID_UNSUPPORTED](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime#ENUM_VALUE:ROWID_UNSUPPORTED) Indicates that this data source does not support the ROWID type. |
| [ROWID_VALID_FOREVER](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime#ENUM_VALUE:ROWID_VALID_FOREVER) Indicates that the lifetime of a RowId from this data source is, effectively, unlimited. |
| [ROWID_VALID_OTHER](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime#ENUM_VALUE:ROWID_VALID_OTHER) Indicates that the lifetime of a RowId from this data source is indeterminate; but not one of ROWID_VALID_TRANSACTION, ROWID_VALID_SESSION, or, ROWID_VALID_FOREVER. |
| [ROWID_VALID_SESSION](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime#ENUM_VALUE:ROWID_VALID_SESSION) Indicates that the lifetime of a RowId from this data source is at least the containing session. |
| [ROWID_VALID_TRANSACTION](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime#ENUM_VALUE:ROWID_VALID_TRANSACTION) Indicates that the lifetime of a RowId from this data source is at least the containing transaction. |

## Enum values

### ROWID_UNSUPPORTED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val ROWID_UNSUPPORTED : RowIdLifetime
```

Indicates that this data source does not support the ROWID type. 

### ROWID_VALID_FOREVER

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val ROWID_VALID_FOREVER : RowIdLifetime
```

Indicates that the lifetime of a RowId from this data source is, effectively, unlimited. 

### ROWID_VALID_OTHER

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val ROWID_VALID_OTHER : RowIdLifetime
```

Indicates that the lifetime of a RowId from this data source is indeterminate; but not one of ROWID_VALID_TRANSACTION, ROWID_VALID_SESSION, or, ROWID_VALID_FOREVER. 

### ROWID_VALID_SESSION

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val ROWID_VALID_SESSION : RowIdLifetime
```

Indicates that the lifetime of a RowId from this data source is at least the containing session. 

### ROWID_VALID_TRANSACTION

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val ROWID_VALID_TRANSACTION : RowIdLifetime
```

Indicates that the lifetime of a RowId from this data source is at least the containing transaction.
