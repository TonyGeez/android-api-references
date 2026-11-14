# CalendarContract.ExtendedPropertiesColumns

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExtendedPropertiesColumns

Kotlin| [Java](../android/provider/CalendarContract.ExtendedPropertiesColumns.md) 
| --- | --- |

```
protected interface ExtendedPropertiesColumns
```

| [android.provider.CalendarContract.ExtendedPropertiesColumns](../android/provider/CalendarContract.ExtendedPropertiesColumns.md) |

| Known Direct Subclasses [CalendarContract.ExtendedProperties](../android/provider/CalendarContract.ExtendedProperties.md) |--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------| | [CalendarContract.ExtendedProperties](../android/provider/CalendarContract.ExtendedProperties.md) | Fields for accessing the Extended Properties. | |
| --- | --- | --- | --- | --- | --- | --- |

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EVENT_ID](../android/provider/CalendarContract.ExtendedPropertiesColumns.md) The event the extended property belongs to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NAME](../android/provider/CalendarContract.ExtendedPropertiesColumns.md) The name of the extended property. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [VALUE](../android/provider/CalendarContract.ExtendedPropertiesColumns.md) The value of the extended property. |
| --- | --- |

## Constants

### EVENT_ID

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_ID: String
```

The event the extended property belongs to. Column name.

Type: INTEGER (foreign key to the Events table) 

 Value: "event_id"

### NAME

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAME: String
```

The name of the extended property. This is a uri of the form {scheme}#{local-name} convention. Column name.

Type: TEXT 

 Value: "name"

### VALUE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VALUE: String
```

The value of the extended property. Column name.

Type: TEXT 

 Value: "value"
