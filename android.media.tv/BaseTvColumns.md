# TvContract.BaseTvColumns

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseTvColumns

Kotlin| [Java](https://developer.android.com/reference/android/media/tv/TvContract.BaseTvColumns "View this page in Java") 
| --- | --- |

```
interface BaseTvColumns : BaseColumns
```

| [android.media.tv.TvContract.BaseTvColumns](https://developer.android.com/reference/kotlin/android/media/tv/TvContract.BaseTvColumns#) |

| Known Direct Subclasses [TvContract.Channels](https://developer.android.com/reference/kotlin/android/media/tv/TvContract.Channels), [TvContract.PreviewPrograms](https://developer.android.com/reference/kotlin/android/media/tv/TvContract.PreviewPrograms), [TvContract.Programs](https://developer.android.com/reference/kotlin/android/media/tv/TvContract.Programs), [TvContract.RecordedPrograms](https://developer.android.com/reference/kotlin/android/media/tv/TvContract.RecordedPrograms), [TvContract.WatchNextPrograms](https://developer.android.com/reference/kotlin/android/media/tv/TvContract.WatchNextPrograms) |------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------| | [TvContract.Channels](https://developer.android.com/reference/kotlin/android/media/tv/TvContract.Channels) | Column definitions for the TV channels table. | | [TvContract.PreviewPrograms](https://developer.android.com/reference/kotlin/android/media/tv/TvContract.PreviewPrograms) | Column definitions for the preview TV programs table. | | [TvContract.Programs](https://developer.android.com/reference/kotlin/android/media/tv/TvContract.Programs) | Column definitions for the TV programs table. | | [TvContract.RecordedPrograms](https://developer.android.com/reference/kotlin/android/media/tv/TvContract.RecordedPrograms) | Column definitions for the recorded TV programs table. | | [TvContract.WatchNextPrograms](https://developer.android.com/reference/kotlin/android/media/tv/TvContract.WatchNextPrograms) | Column definitions for the "watch next" TV programs table. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Common base for the tables of TV channels/programs.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_PACKAGE_NAME](https://developer.android.com/reference/kotlin/android/media/tv/TvContract.BaseTvColumns#COLUMN_PACKAGE_NAME:kotlin.String) The name of the package that owns the current row. |

| Inherited constants ||
|---|---|
| From class [BaseColumns](https://developer.android.com/reference/kotlin/android/provider/BaseColumns.html#) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_COUNT](https://developer.android.com/reference/kotlin/android/provider/BaseColumns.html#_COUNT:kotlin.String) <br /> The count of rows in a directory. Type: INTEGER <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_ID](https://developer.android.com/reference/kotlin/android/provider/BaseColumns.html#_ID:kotlin.String) <br /> The unique ID for a row. Type: INTEGER (long) <br /> | ||

## Constants

### COLUMN_PACKAGE_NAME

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COLUMN_PACKAGE_NAME: String
```

The name of the package that owns the current row.

The TV provider fills in this column with the name of the package that provides the initial data of the row. If the package is later uninstalled, the rows it owns are automatically removed from the tables.

Type: TEXT 

 Value: "package_name"
