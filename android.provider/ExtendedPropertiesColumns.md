# CalendarContract.ExtendedPropertiesColumns

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExtendedPropertiesColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/CalendarContract.ExtendedPropertiesColumns "View this page in Java") 
| --- | --- |

```
protected interface ExtendedPropertiesColumns
```

| [android.provider.CalendarContract.ExtendedPropertiesColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ExtendedPropertiesColumns#) |

| Known Direct Subclasses [CalendarContract.ExtendedProperties](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ExtendedProperties) |--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------| | [CalendarContract.ExtendedProperties](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ExtendedProperties) | Fields for accessing the Extended Properties. | |
| --- | --- | --- | --- | --- | --- | --- |

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EVENT_ID](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ExtendedPropertiesColumns#EVENT_ID:kotlin.String) The event the extended property belongs to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NAME](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ExtendedPropertiesColumns#NAME:kotlin.String) The name of the extended property. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [VALUE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ExtendedPropertiesColumns#VALUE:kotlin.String) The value of the extended property. |
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
