# TvContract

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TvContract

Kotlin| [Java](TvContract.md) 
| --- | --- |

```
class TvContract
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.tv.TvContract](TvContract.md) |

The contract between the TV provider and applications. Contains definitions for the supported URIs and columns.

### Overview

<br />

TvContract defines a basic database of TV content metadata such as channel and program information. The information is stored in [Channels](../android/media/tv/TvContract.Channels.md) and [Programs](../android/media/tv/TvContract.Programs.md) tables.

- A row in the [Channels](../android/media/tv/TvContract.Channels.md) table represents information about a TV channel. The data format can vary greatly from standard to standard or according to service provider, thus the columns here are mostly comprised of basic entities that are usually seen to users regardless of standard such as channel number and name.
- A row in the [Programs](../android/media/tv/TvContract.Programs.md) table represents a set of data describing a TV program such as program title and start time.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [BaseTvColumns](../android/media/tv/TvContract.BaseTvColumns.md) Common base for the tables of TV channels/programs. |
| | [Channels](../android/media/tv/TvContract.Channels.md) Column definitions for the TV channels table. |
| | [PreviewPrograms](../android/media/tv/TvContract.PreviewPrograms.md) Column definitions for the preview TV programs table. |
| --- | --- |
| | [Programs](../android/media/tv/TvContract.Programs.md) Column definitions for the TV programs table. |
| | [RecordedPrograms](../android/media/tv/TvContract.RecordedPrograms.md) Column definitions for the recorded TV programs table. |
| | [WatchNextPrograms](../android/media/tv/TvContract.WatchNextPrograms.md) Column definitions for the "watch next" TV programs table. |
| --- | --- |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_INITIALIZE_PROGRAMS](TvContract.md) Broadcast Action: sent to the target TV input after it is first installed to notify the input to initialize its channels and programs to the system content provider. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_PREVIEW_PROGRAM_ADDED_TO_WATCH_NEXT](TvContract.md) Broadcast Action: sent by the system to tell the target TV input that one of its existing preview programs is added to the watch next programs table by user. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_PREVIEW_PROGRAM_BROWSABLE_DISABLED](TvContract.md) Broadcast Action: sent by the system to tell the target TV input that one of its preview program's browsable state is disabled, i. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_REQUEST_CHANNEL_BROWSABLE](TvContract.md) Activity Action: sent by an application telling the system to make the given channel browsable with user interaction. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_WATCH_NEXT_PROGRAM_BROWSABLE_DISABLED](TvContract.md) Broadcast Action: sent by the system to tell the target TV input that one of its "watch next" program's browsable state is disabled, i. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AUTHORITY](TvContract.md) The authority for the TV provider. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CHANNEL_ID](TvContract.md) The key for a bundle parameter containing a channel ID as a long integer |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PREVIEW_PROGRAM_ID](TvContract.md) The key for a bundle parameter containing a program ID as a long integer. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_WATCH_NEXT_PROGRAM_ID](TvContract.md) The key for a bundle parameter containing a watch next program ID as a long integer. |
| --- | --- |

| Public methods ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Uri](../android.net/Uri.md)! | [buildChannelLogoUri](TvContract.md))`(`channelUri:` ` [Uri](../android.net/Uri.md)!`)` Builds a URI that points to a channel logo. |
| static [Uri](../android.net/Uri.md)! | [buildChannelLogoUri](TvContract.md))`(`channelId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Builds a URI that points to a channel logo. |
| static [Uri](../android.net/Uri.md)! | [buildChannelUri](TvContract.md))`(`channelId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Builds a URI that points to a specific channel. |
| --- | --- |
| static [Uri](../android.net/Uri.md)! | [buildChannelUriForPassthroughInput](TvContract.md))`(`inputId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Build a special channel URI intended to be used with pass-through inputs. |
| static [Uri](../android.net/Uri.md)! | [buildChannelsUriForInput](TvContract.md))`(`inputId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Builds a URI that points to all channels from a given TV input. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [buildInputId](TvContract.md))`(`name:` ` [ComponentName](../android.content/ComponentName.md)!`)` Builds an ID that uniquely identifies a TV input service. |
| --- | --- |
| static [Uri](../android.net/Uri.md)! | [buildPreviewProgramUri](TvContract.md))`(`previewProgramId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Builds a URI that points to a specific preview program. |
| static [Uri](../android.net/Uri.md)! | [buildPreviewProgramsUriForChannel](TvContract.md))`(`channelUri:` ` [Uri](../android.net/Uri.md)!`)` Builds a URI that points to all preview programs on a given channel. |
| static [Uri](../android.net/Uri.md)! | [buildPreviewProgramsUriForChannel](TvContract.md))`(`channelId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Builds a URI that points to all preview programs on a given channel. |
| --- | --- |
| static [Uri](../android.net/Uri.md)! | [buildProgramUri](TvContract.md))`(`programId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Builds a URI that points to a specific program. |
| static [Uri](../android.net/Uri.md)! | [buildProgramsUriForChannel](TvContract.md))`(`channelUri:` ` [Uri](../android.net/Uri.md)!`)` Builds a URI that points to all programs on a given channel. |
| static [Uri](../android.net/Uri.md)! | [buildProgramsUriForChannel](TvContract.md))`(`channelUri:` ` [Uri](../android.net/Uri.md)!`, `startTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `endTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Builds a URI that points to programs on a specific channel whose schedules overlap with the given time frame. |
| --- | --- |
| static [Uri](../android.net/Uri.md)! | [buildProgramsUriForChannel](TvContract.md))`(`channelId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Builds a URI that points to all programs on a given channel. |
| static [Uri](../android.net/Uri.md)! | [buildProgramsUriForChannel](TvContract.md))`(`channelId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `startTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `endTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Builds a URI that points to programs on a specific channel whose schedules overlap with the given time frame. |
| static [Uri](../android.net/Uri.md)! | [buildRecordedProgramUri](TvContract.md))`(`recordedProgramId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Builds a URI that points to a specific recorded program. |
| --- | --- |
| static [Uri](../android.net/Uri.md)! | [buildWatchNextProgramUri](TvContract.md))`(`watchNextProgramId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Builds a URI that points to a specific watch next program. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChannelUri](TvContract.md))`(`uri:` ` [Uri](../android.net/Uri.md)`)` <br /> |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChannelUriForPassthroughInput](TvContract.md))`(`uri:` ` [Uri](../android.net/Uri.md)`)` <br /> |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChannelUriForTunerInput](TvContract.md))`(`uri:` ` [Uri](../android.net/Uri.md)`)` <br /> |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProgramUri](TvContract.md))`(`uri:` ` [Uri](../android.net/Uri.md)`)` <br /> |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRecordedProgramUri](TvContract.md))`(`uri:` ` [Uri](../android.net/Uri.md)`)` <br /> |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestChannelBrowsable](TvContract.md))`(`context:` ` [Context](../android.content/Context.md)!`, `channelId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Requests to make a channel browsable. |

## Constants

### ACTION_INITIALIZE_PROGRAMS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_INITIALIZE_PROGRAMS: String
```

Broadcast Action: sent to the target TV input after it is first installed to notify the input to initialize its channels and programs to the system content provider.

Note that this intent is sent only on devices with [android.content.pm.PackageManager#FEATURE_LEANBACK](../android.content.pm/PackageManager.md) enabled. Besides that, in order to receive this intent, the target TV input must:

- Declare a broadcast receiver for this intent in its`AndroidManifest.xml`.
- Declare appropriate permissions to write channel and program data in its`AndroidManifest.xml`.

 Value: "android.media.tv.action.INITIALIZE_PROGRAMS"

### ACTION_PREVIEW_PROGRAM_ADDED_TO_WATCH_NEXT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_PREVIEW_PROGRAM_ADDED_TO_WATCH_NEXT: String
```

Broadcast Action: sent by the system to tell the target TV input that one of its existing preview programs is added to the watch next programs table by user.

The intent must contain the following bundle parameters:

- [EXTRA_PREVIEW_PROGRAM_ID](TvContract.md): the ID of the existing preview program.
- [EXTRA_WATCH_NEXT_PROGRAM_ID](TvContract.md): the ID of the new watch next program.

 Value: "android.media.tv.action.PREVIEW_PROGRAM_ADDED_TO_WATCH_NEXT"

### ACTION_PREVIEW_PROGRAM_BROWSABLE_DISABLED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_PREVIEW_PROGRAM_BROWSABLE_DISABLED: String
```

Broadcast Action: sent by the system to tell the target TV input that one of its preview program's browsable state is disabled, i.e., it will no longer be shown to users, which, for example, might be a result of users' interaction with UI. The input is expected to delete the preview program from the content provider.

The intent must contain the following bundle parameter:

- [EXTRA_PREVIEW_PROGRAM_ID](TvContract.md): the disabled preview program ID.

 Value: "android.media.tv.action.PREVIEW_PROGRAM_BROWSABLE_DISABLED"

### ACTION_REQUEST_CHANNEL_BROWSABLE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_REQUEST_CHANNEL_BROWSABLE: String
```

Activity Action: sent by an application telling the system to make the given channel browsable with user interaction. The system may show UI to ask user to approve the channel. This is only relevant to channels with [Channels.TYPE_PREVIEW](../android/media/tv/TvContract.Channels.md) type. Use android.app.Activity#startActivityForResult to get the result of the request.

The intent must contain the following bundle parameters:

- [EXTRA_CHANNEL_ID](TvContract.md): ID for the [Channels.TYPE_PREVIEW](../android/media/tv/TvContract.Channels.md) channel as a long integer.

 Value: "android.media.tv.action.REQUEST_CHANNEL_BROWSABLE"

### ACTION_WATCH_NEXT_PROGRAM_BROWSABLE_DISABLED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_WATCH_NEXT_PROGRAM_BROWSABLE_DISABLED: String
```

Broadcast Action: sent by the system to tell the target TV input that one of its "watch next" program's browsable state is disabled, i.e., it will no longer be shown to users, which, for example, might be a result of users' interaction with UI. The input is expected to delete the "watch next" program from the content provider.

The intent must contain the following bundle parameter:

- [EXTRA_WATCH_NEXT_PROGRAM_ID](TvContract.md): the disabled "watch next" program ID.

 Value: "android.media.tv.action.WATCH_NEXT_PROGRAM_BROWSABLE_DISABLED"

### AUTHORITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUTHORITY: String
```

The authority for the TV provider. 

 Value: "android.media.tv"

### EXTRA_CHANNEL_ID

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_CHANNEL_ID: String
```

The key for a bundle parameter containing a channel ID as a long integer 

 Value: "android.media.tv.extra.CHANNEL_ID"

### EXTRA_PREVIEW_PROGRAM_ID

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PREVIEW_PROGRAM_ID: String
```

The key for a bundle parameter containing a program ID as a long integer. 

 Value: "android.media.tv.extra.PREVIEW_PROGRAM_ID"

### EXTRA_WATCH_NEXT_PROGRAM_ID

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_WATCH_NEXT_PROGRAM_ID: String
```

The key for a bundle parameter containing a watch next program ID as a long integer. 

 Value: "android.media.tv.extra.WATCH_NEXT_PROGRAM_ID"

## Public methods

### buildChannelLogoUri

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun buildChannelLogoUri(channelUri: Uri!): Uri!
```

Builds a URI that points to a channel logo. See [Channels.Logo](../android/media/tv/TvContract.Channels.Logo.md).

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| `channelUri` | [Uri](../android.net/Uri.md)!:The URI of the channel whose logo is pointed to. |

### buildChannelLogoUri

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun buildChannelLogoUri(channelId: Long): Uri!
```

Builds a URI that points to a channel logo. See [Channels.Logo](../android/media/tv/TvContract.Channels.Logo.md).

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------|
| `channelId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The ID of the channel whose logo is pointed to. |

### buildChannelUri

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun buildChannelUri(channelId: Long): Uri!
```

Builds a URI that points to a specific channel.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------|
| `channelId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The ID of the channel to point to. |

### buildChannelUriForPassthroughInput

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun buildChannelUriForPassthroughInput(inputId: String!): Uri!
```

Build a special channel URI intended to be used with pass-through inputs. (e.g. HDMI)

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `inputId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The ID of the pass-through input to build a channels URI for. |

**See Also**

- [android.media.tv.TvInputInfo#isPassthroughInput()](TvInputInfo.md)) 

### buildChannelsUriForInput

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun buildChannelsUriForInput(inputId: String?): Uri!
```

Builds a URI that points to all channels from a given TV input.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inputId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The ID of the TV input to build a channels URI for. If`null`, builds a URI for all the TV inputs. |

### buildInputId

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun buildInputId(name: ComponentName!): String!
```

Builds an ID that uniquely identifies a TV input service.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [ComponentName](../android.content/ComponentName.md)!:The [ComponentName](../android.content/ComponentName.md) of the TV input service to build ID for. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the ID for the given TV input service. |

### buildPreviewProgramUri

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun buildPreviewProgramUri(previewProgramId: Long): Uri!
```

Builds a URI that points to a specific preview program.

| Parameters ||
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| `previewProgramId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The ID of the preview program to point to. |

### buildPreviewProgramsUriForChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun buildPreviewProgramsUriForChannel(channelUri: Uri!): Uri!
```

Builds a URI that points to all preview programs on a given channel.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `channelUri` | [Uri](../android.net/Uri.md)!:The URI of the channel to return preview programs for. |

### buildPreviewProgramsUriForChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun buildPreviewProgramsUriForChannel(channelId: Long): Uri!
```

Builds a URI that points to all preview programs on a given channel.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------|
| `channelId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The ID of the channel to return preview programs for. |

### buildProgramUri

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun buildProgramUri(programId: Long): Uri!
```

Builds a URI that points to a specific program.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------|
| `programId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The ID of the program to point to. |

### buildProgramsUriForChannel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun buildProgramsUriForChannel(channelUri: Uri!): Uri!
```

Builds a URI that points to all programs on a given channel.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| `channelUri` | [Uri](../android.net/Uri.md)!:The URI of the channel to return programs for. |

### buildProgramsUriForChannel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun buildProgramsUriForChannel(
    channelUri: Uri!, 
    startTime: Long, 
    endTime: Long
): Uri!
```

Builds a URI that points to programs on a specific channel whose schedules overlap with the given time frame.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `channelUri` | [Uri](../android.net/Uri.md)!:The URI of the channel to return programs for. |
| `startTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The start time used to filter programs. The returned programs should have [Programs.COLUMN_END_TIME_UTC_MILLIS](../android/media/tv/TvContract.Programs.md) that is greater than this time. |
| `endTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The end time used to filter programs. The returned programs should have [Programs.COLUMN_START_TIME_UTC_MILLIS](../android/media/tv/TvContract.Programs.md) that is less than this time. |
| --- | --- |

### buildProgramsUriForChannel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun buildProgramsUriForChannel(channelId: Long): Uri!
```

Builds a URI that points to all programs on a given channel.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------|
| `channelId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The ID of the channel to return programs for. |

### buildProgramsUriForChannel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun buildProgramsUriForChannel(
    channelId: Long, 
    startTime: Long, 
    endTime: Long
): Uri!
```

Builds a URI that points to programs on a specific channel whose schedules overlap with the given time frame.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `channelId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The ID of the channel to return programs for. |
| `startTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The start time used to filter programs. The returned programs will have a [Programs.COLUMN_END_TIME_UTC_MILLIS](../android/media/tv/TvContract.Programs.md) that is greater than or equal to`startTime`. |
| `endTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The end time used to filter programs. The returned programs will have [Programs.COLUMN_START_TIME_UTC_MILLIS](../android/media/tv/TvContract.Programs.md) that is less than or equal to`endTime`. |
| --- | --- |

### buildRecordedProgramUri

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun buildRecordedProgramUri(recordedProgramId: Long): Uri!
```

Builds a URI that points to a specific recorded program.

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| `recordedProgramId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The ID of the recorded program to point to. |

### buildWatchNextProgramUri

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun buildWatchNextProgramUri(watchNextProgramId: Long): Uri!
```

Builds a URI that points to a specific watch next program.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| `watchNextProgramId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The ID of the watch next program to point to. |

### isChannelUri

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isChannelUri(uri: Uri): Boolean
```

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android.net/Uri.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`uri`is a channel URI. |

### isChannelUriForPassthroughInput

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isChannelUriForPassthroughInput(uri: Uri): Boolean
```

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android.net/Uri.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`uri`is a channel URI for a pass-through input. |

### isChannelUriForTunerInput

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isChannelUriForTunerInput(uri: Uri): Boolean
```

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android.net/Uri.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`uri`is a channel URI for a tuner input. |

### isProgramUri

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isProgramUri(uri: Uri): Boolean
```

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android.net/Uri.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`uri`is a program URI. |

### isRecordedProgramUri

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isRecordedProgramUri(uri: Uri): Boolean
```

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android.net/Uri.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`uri`is a recorded program URI. |

### requestChannelBrowsable

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun requestChannelBrowsable(
    context: Context!, 
    channelId: Long
): Unit
```

Requests to make a channel browsable.

Once called, the system will review the request and make the channel browsable based on its policy. The first request from a package is guaranteed to be approved. This is only relevant to channels with [Channels.TYPE_PREVIEW](../android/media/tv/TvContract.Channels.md) type.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:The context for accessing content provider. |
| `channelId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The channel ID to be browsable. |

**See Also**

- [android.media.tv.TvContract.Channels#COLUMN_BROWSABLE](../android/media/tv/TvContract.Channels.md)
