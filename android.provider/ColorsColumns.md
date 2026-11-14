# CalendarContract.ColorsColumns

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ColorsColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/CalendarContract.ColorsColumns "View this page in Java") 
| --- | --- |

```
protected interface ColorsColumns : SyncStateContract.Columns
```

| [android.provider.CalendarContract.ColorsColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ColorsColumns#) |

| Known Direct Subclasses [CalendarContract.Colors](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Colors) |--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------| | [CalendarContract.Colors](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Colors) | Fields for accessing colors available for a given account. | |
| --- | --- | --- | --- | --- | --- | --- |

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLOR](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ColorsColumns#COLOR:kotlin.String) The color as an 8-bit ARGB integer value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLOR_KEY](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ColorsColumns#COLOR_KEY:kotlin.String) The key used to reference this color. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLOR_TYPE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ColorsColumns#COLOR_TYPE:kotlin.String) The type of color, which describes how it should be used. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CALENDAR](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ColorsColumns#TYPE_CALENDAR:kotlin.Int) This indicateds a color that can be used for calendars. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_EVENT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ColorsColumns#TYPE_EVENT:kotlin.Int) This indicates a color that can be used for events. |

| Inherited constants ||
|---|---|
| From class [Columns](https://developer.android.com/reference/kotlin/android/provider/SyncStateContract.Columns) |----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACCOUNT_NAME](https://developer.android.com/reference/kotlin/android/provider/SyncStateContract.Columns#ACCOUNT_NAME:kotlin.String) <br /> A reference to the name of the account to which this data belongs Type: STRING <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACCOUNT_TYPE](https://developer.android.com/reference/kotlin/android/provider/SyncStateContract.Columns#ACCOUNT_TYPE:kotlin.String) <br /> A reference to the type of the account to which this data belongs Type: STRING <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA](https://developer.android.com/reference/kotlin/android/provider/SyncStateContract.Columns#DATA:kotlin.String) <br /> The sync data associated with this account. Type: NONE <br /> | ||
| From class [BaseColumns](https://developer.android.com/reference/kotlin/android/provider/BaseColumns) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_COUNT](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_COUNT:kotlin.String) <br /> The count of rows in a directory. Type: INTEGER <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_ID](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String) <br /> The unique ID for a row. Type: INTEGER (long) <br /> | ||

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

The key used to reference this color. This can be any non-empty string, but must be unique for a given [ACCOUNT_TYPE](https://developer.android.com/reference/kotlin/android/provider/SyncStateContract.Columns#ACCOUNT_TYPE:kotlin.String) and [ACCOUNT_NAME](https://developer.android.com/reference/kotlin/android/provider/SyncStateContract.Columns#ACCOUNT_NAME:kotlin.String). Column name.

Type: TEXT 

 Value: "color_index"

### COLOR_TYPE

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLOR_TYPE: String
```

The type of color, which describes how it should be used. Valid types are [TYPE_CALENDAR](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ColorsColumns#TYPE_CALENDAR:kotlin.Int) and [TYPE_EVENT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ColorsColumns#TYPE_EVENT:kotlin.Int). Column name.

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
