# CalendarContract.ColorsColumns

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ColorsColumns

Kotlin| [Java](../android/provider/CalendarContract.ColorsColumns.md) 
| --- | --- |

```
protected interface ColorsColumns : SyncStateContract.Columns
```

| [android.provider.CalendarContract.ColorsColumns](../android/provider/CalendarContract.ColorsColumns.md) |

| Known Direct Subclasses [CalendarContract.Colors](../android/provider/CalendarContract.Colors.md) |--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------| | [CalendarContract.Colors](../android/provider/CalendarContract.Colors.md) | Fields for accessing colors available for a given account. | |
| --- | --- | --- | --- | --- | --- | --- |

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLOR](../android/provider/CalendarContract.ColorsColumns.md) The color as an 8-bit ARGB integer value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLOR_KEY](../android/provider/CalendarContract.ColorsColumns.md) The key used to reference this color. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLOR_TYPE](../android/provider/CalendarContract.ColorsColumns.md) The type of color, which describes how it should be used. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CALENDAR](../android/provider/CalendarContract.ColorsColumns.md) This indicateds a color that can be used for calendars. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_EVENT](../android/provider/CalendarContract.ColorsColumns.md) This indicates a color that can be used for events. |

| Inherited constants ||
|---|---|
| From class [Columns](../android/provider/SyncStateContract.Columns.md) |----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACCOUNT_NAME](../android/provider/SyncStateContract.Columns.md) <br /> A reference to the name of the account to which this data belongs Type: STRING <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACCOUNT_TYPE](../android/provider/SyncStateContract.Columns.md) <br /> A reference to the type of the account to which this data belongs Type: STRING <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA](../android/provider/SyncStateContract.Columns.md) <br /> The sync data associated with this account. Type: NONE <br /> | ||
| From class [BaseColumns](../android/provider/BaseColumns.md) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_COUNT](../android/provider/BaseColumns.md) <br /> The count of rows in a directory. Type: INTEGER <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_ID](../android/provider/BaseColumns.md) <br /> The unique ID for a row. Type: INTEGER (long) <br /> | ||

## Constants

### COLOR

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR: String
```

The color as an 8-bit ARGB integer value. Colors should specify alpha as fully opaque (eg 0xFF993322) as the alpha may be ignored or modified for display. It is reccomended that colors be usable with light (near white) text. Apps should not depend on that assumption, however. Column name.

Type: INTEGER (NOT NULL) 

 Value: "color"

### COLOR_KEY

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_KEY: String
```

The key used to reference this color. This can be any non-empty string, but must be unique for a given [ACCOUNT_TYPE](../android/provider/SyncStateContract.Columns.md) and [ACCOUNT_NAME](../android/provider/SyncStateContract.Columns.md). Column name.

Type: TEXT 

 Value: "color_index"

### COLOR_TYPE

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_TYPE: String
```

The type of color, which describes how it should be used. Valid types are [TYPE_CALENDAR](../android/provider/CalendarContract.ColorsColumns.md) and [TYPE_EVENT](../android/provider/CalendarContract.ColorsColumns.md). Column name.

Type: INTEGER (NOT NULL) 

 Value: "color_type"

### TYPE_CALENDAR

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CALENDAR: Int
```

This indicateds a color that can be used for calendars. 

 Value: 0

### TYPE_EVENT

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_EVENT: Int
```

This indicates a color that can be used for events. 

 Value: 1
