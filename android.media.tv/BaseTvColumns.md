# TvContract.BaseTvColumns

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseTvColumns

Kotlin| [Java](../android/media/tv/TvContract.BaseTvColumns.md) 
| --- | --- |

```
interface BaseTvColumns : BaseColumns
```

| [android.media.tv.TvContract.BaseTvColumns](../android/media/tv/TvContract.BaseTvColumns.md) |

| Known Direct Subclasses [TvContract.Channels](../android/media/tv/TvContract.Channels.md), [TvContract.PreviewPrograms](../android/media/tv/TvContract.PreviewPrograms.md), [TvContract.Programs](../android/media/tv/TvContract.Programs.md), [TvContract.RecordedPrograms](../android/media/tv/TvContract.RecordedPrograms.md), [TvContract.WatchNextPrograms](../android/media/tv/TvContract.WatchNextPrograms.md) |------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------| | [TvContract.Channels](../android/media/tv/TvContract.Channels.md) | Column definitions for the TV channels table. | | [TvContract.PreviewPrograms](../android/media/tv/TvContract.PreviewPrograms.md) | Column definitions for the preview TV programs table. | | [TvContract.Programs](../android/media/tv/TvContract.Programs.md) | Column definitions for the TV programs table. | | [TvContract.RecordedPrograms](../android/media/tv/TvContract.RecordedPrograms.md) | Column definitions for the recorded TV programs table. | | [TvContract.WatchNextPrograms](../android/media/tv/TvContract.WatchNextPrograms.md) | Column definitions for the "watch next" TV programs table. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Common base for the tables of TV channels/programs.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COLUMN_PACKAGE_NAME](../android/media/tv/TvContract.BaseTvColumns.md) The name of the package that owns the current row. |

| Inherited constants ||
|---|---|
| From class [BaseColumns](../android/provider/BaseColumns.md) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_COUNT](../android/provider/BaseColumns.md) <br /> The count of rows in a directory. Type: INTEGER <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_ID](../android/provider/BaseColumns.md) <br /> The unique ID for a row. Type: INTEGER (long) <br /> | ||

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
