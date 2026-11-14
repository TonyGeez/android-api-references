Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

# CloudMediaProviderContract

```
class CloudMediaProviderContract
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.provider.CloudMediaProviderContract](https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#) |

Defines the contract between a cloud media provider and the OS.

To create a cloud media provider, extend `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider`, which provides a foundational implementation of this contract.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.AlbumColumns` Constants related to an album item, including `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` column names |
| | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.Capabilities` Information about what capabilities a CloudMediaProvider can support. |
| | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaCategoryColumns` MediaCategory represents a broader structure that a `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaSetColumns` or another `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaCategoryColumns` belongs to. |
| | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaCollectionInfo` Constants related to a media collection |
| | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaColumns` Constants related to a media item, including `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` column names |
| | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaSetColumns` MediaSet represents a cohesive collection of related unique media items, sharing a common meaningful context or theme. |
| | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.SearchSuggestionColumns` Represents a search suggestion provided by the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider`. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_ALBUM_ID:kotlin.String` Limits the query results to only media items matching the given album id. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_LOOPING_PLAYBACK_ENABLED:kotlin.String` Indicates whether to enable looping playback of media items. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_MEDIA_COLLECTION_ID:kotlin.String` `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaCollectionInfo#MEDIA_COLLECTION_ID:kotlin.String` on which the media or album query occurred. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_SIZE:kotlin.String` The maximum number of query results that should be included in a batch when syncing metadata with cloud provider. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_TOKEN:kotlin.String` Opaque pagination token to retrieve the next page (cursor) from a media or album query. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PREVIEW_THUMBNAIL:kotlin.String` Forces the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onOpenPreview(kotlin.String,%20android.graphics.Point,%20android.os.Bundle,%20android.os.CancellationSignal)` file descriptor to return a thumbnail image. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_SORT_ORDER:kotlin.String` Extra used to specify the sorting behavior when querying from `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_SURFACE_CONTROLLER_AUDIO_MUTE_ENABLED:kotlin.String` Indicates whether to mute audio during preview of media items. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_SYNC_GENERATION:kotlin.String` Generation number to fetch the latest media or album metadata changes from the media collection. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#MANAGE_CLOUD_MEDIA_PROVIDERS_PERMISSION:kotlin.String` Permission required to protect `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider` instances. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#MEDIA_CATEGORY_TYPE_PEOPLE_AND_PETS:kotlin.String` Represents media category related to faces of people and pets. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#MEDIA_CATEGORY_TYPE_USER_ALBUMS:kotlin.String` Represents media category related to a user's custom albums. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#PROVIDER_INTERFACE:kotlin.String` `https://developer.android.com/reference/kotlin/android/content/Intent.html#` action used to identify `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider` instances. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#SEARCH_SUGGESTION_ALBUM:kotlin.String` Suggestion based on user albums. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#SEARCH_SUGGESTION_DATE:kotlin.String` Suggestion based on the date photos were taken. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#SEARCH_SUGGESTION_FACE:kotlin.String` Suggestion based on faces detected in photos. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#SEARCH_SUGGESTION_LOCATION:kotlin.String` Suggestion based on location data associated with photos. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#SEARCH_SUGGESTION_TEXT:kotlin.String` Represents a generic text search suggestion. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#SORT_ORDER_DESC_DATE_TAKEN:kotlin.Int` Sort items in descending order by the `DATE_TAKEN_MILLIS`. |

## Constants

### EXTRA_ALBUM_ID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
static val EXTRA_ALBUM_ID: String
```

Limits the query results to only media items matching the given album id.

If the provider handled the album filter, they must also add the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_ALBUM_ID:kotlin.String` key to the array of `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String` as part of the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` `https://developer.android.com/reference/kotlin/android/os/Bundle.html#`.

 Value: "android.provider.extra.ALBUM_ID"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryMedia(android.os.Bundle)`

### EXTRA_LOOPING_PLAYBACK_ENABLED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
static val EXTRA_LOOPING_PLAYBACK_ENABLED: String
```

Indicates whether to enable looping playback of media items.

In case this is not present, the default value should be false.

 Value: "android.provider.extra.LOOPING_PLAYBACK_ENABLED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onCreateCloudMediaSurfaceController(android.os.Bundle,%20android.provider.CloudMediaProvider.CloudMediaSurfaceStateChangedCallback)`
- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider.CloudMediaSurfaceController#onConfigChange(android.os.Bundle)`

### EXTRA_MEDIA_COLLECTION_ID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
static val EXTRA_MEDIA_COLLECTION_ID: String
```

`https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaCollectionInfo#MEDIA_COLLECTION_ID:kotlin.String` on which the media or album query occurred.

Providers must set this token as part of the `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` returned from the cursors on query. This allows the OS to verify that the returned results match the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaCollectionInfo#MEDIA_COLLECTION_ID:kotlin.String` queried via `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onGetMediaCollectionInfo(android.os.Bundle)`. If the collection differs, the OS will ignore the result and may try again.

 Value: "android.provider.extra.MEDIA_COLLECTION_ID"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryMedia(android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryDeletedMedia(android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryAlbums(android.os.Bundle)`

### EXTRA_PAGE_SIZE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 8](https://developer.android.com/sdkExtensions)

```
static val EXTRA_PAGE_SIZE: String
```

The maximum number of query results that should be included in a batch when syncing metadata with cloud provider. This extra can be passed as a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` parameter to the media or album query methods. It is optional for the provider to honor this extra and return results at max page size.

 Value: "android.provider.extra.PAGE_SIZE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryMedia(android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryAlbums(android.os.Bundle)`

### EXTRA_PAGE_TOKEN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
static val EXTRA_PAGE_TOKEN: String
```

Opaque pagination token to retrieve the next page (cursor) from a media or album query.

Providers can optionally set this token as part of the `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` `https://developer.android.com/reference/kotlin/android/os/Bundle.html#`. If a token is set, the OS can pass it as a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` parameter when querying for media or albums to fetch subsequent pages. The provider can keep returning pagination tokens until the last page at which point it should not set a token on the `https://developer.android.com/reference/kotlin/android/database/Cursor.html#`.

If the provider handled the page token as part of the query, they must add the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_PAGE_TOKEN:kotlin.String` key to the array of `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String` as part of the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` `https://developer.android.com/reference/kotlin/android/os/Bundle.html#`.

 Value: "android.provider.extra.PAGE_TOKEN"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryMedia(android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryAlbums(android.os.Bundle)`

### EXTRA_PREVIEW_THUMBNAIL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
static val EXTRA_PREVIEW_THUMBNAIL: String
```

Forces the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onOpenPreview(kotlin.String,%20android.graphics.Point,%20android.os.Bundle,%20android.os.CancellationSignal)` file descriptor to return a thumbnail image. This is only useful for videos where the OS can either request a video or image for preview. If false or not specified, CloudMediaProvider#onOpenPreview should return the media item's file descriptor instead.

 Value: "android.provider.extra.PREVIEW_THUMBNAIL"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onOpenPreview(kotlin.String,%20android.graphics.Point,%20android.os.Bundle,%20android.os.CancellationSignal)`

### EXTRA_SORT_ORDER

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 16](https://developer.android.com/sdkExtensions)

```
static val EXTRA_SORT_ORDER: String
```

Extra used to specify the sorting behavior when querying from `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider`. The value associated with this extra should be one of the integer constants defined in the SortOrders.

Type: INTEGER

 Value: "android.provider.extra.SORT_ORDER"

**See Also**

### EXTRA_SURFACE_CONTROLLER_AUDIO_MUTE_ENABLED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
static val EXTRA_SURFACE_CONTROLLER_AUDIO_MUTE_ENABLED: String
```

Indicates whether to mute audio during preview of media items.

 Value: "android.provider.extra.SURFACE_CONTROLLER_AUDIO_MUTE_ENABLED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onCreateCloudMediaSurfaceController(android.os.Bundle,%20android.provider.CloudMediaProvider.CloudMediaSurfaceStateChangedCallback)`
- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider.CloudMediaSurfaceController#onConfigChange(android.os.Bundle)`

### EXTRA_SYNC_GENERATION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
static val EXTRA_SYNC_GENERATION: String
```

Generation number to fetch the latest media or album metadata changes from the media collection.

The provider should associate a monotonically increasing sync generation to each media item change (insertion/deletion/update). This is useful to quickly identify exactly which media items have changed since a previous point in time.

Providers should also associate a separate monotonically increasing sync generation for album changes (insertion/deletion/update). This album sync generation, should record both changes to the album metadata itself and changes to the media items contained in the album. E.g. a direct change to an album's `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.AlbumColumns#DISPLAY_NAME:kotlin.String` will increase the album sync generation, likewise adding a photo to that album should also increase the sync generation.

Note that multiple media (or album) items can share a sync generation as long as the entire change appears atomic from the perspective of the query APIs. E.g. each item in a batch photo sync from the cloud can have the same sync generation if they were all synced atomically into the collection from the perspective of an external observer.

This extra can be passed as a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` parameter to the media or album query methods and the provider should only return items with a sync generation that is strictly greater than the one provided in the filter.

If the provider supports this filter, it must support the respective `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onGetMediaCollectionInfo(android.os.Bundle)` methods to return the `count` and `max generation` for media or albums.

If the provider handled the generation, they must add the `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract#EXTRA_SYNC_GENERATION:kotlin.String` key to the array of `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#EXTRA_HONORED_ARGS:kotlin.String` as part of the returned `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setExtras(android.os.Bundle)` `https://developer.android.com/reference/kotlin/android/os/Bundle.html#`.

 Value: "android.provider.extra.SYNC_GENERATION"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaCollectionInfo#LAST_MEDIA_SYNC_GENERATION:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryMedia(android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider#onQueryAlbums(android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#GENERATION_MODIFIED:kotlin.String`

### MANAGE_CLOUD_MEDIA_PROVIDERS_PERMISSION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
static val MANAGE_CLOUD_MEDIA_PROVIDERS_PERMISSION: String
```

Permission required to protect `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider` instances. Providers should require this in the `permission` attribute in their `<provider>` tag. The OS will not connect to a provider without this protection.

 Value: "com.android.providers.media.permission.MANAGE_CLOUD_MEDIA_PROVIDERS"

### MEDIA_CATEGORY_TYPE_PEOPLE_AND_PETS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 16](https://developer.android.com/sdkExtensions)

```
static val MEDIA_CATEGORY_TYPE_PEOPLE_AND_PETS: String
```

Represents media category related to faces of people and pets.

 Value: "com.android.providers.media.MEDIA_CATEGORY_TYPE_PEOPLE_AND_PETS"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaCategoryColumns#MEDIA_CATEGORY_TYPE:kotlin.String`

### MEDIA_CATEGORY_TYPE_USER_ALBUMS

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 19](https://developer.android.com/sdkExtensions)

```
static val MEDIA_CATEGORY_TYPE_USER_ALBUMS: String
```

Represents media category related to a user's custom albums.

 Value: "com.android.providers.media.MEDIA_CATEGORY_TYPE_USER_ALBUMS"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.MediaCategoryColumns#MEDIA_CATEGORY_TYPE:kotlin.String`

### PROVIDER_INTERFACE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
static val PROVIDER_INTERFACE: String
```

`https://developer.android.com/reference/kotlin/android/content/Intent.html#` action used to identify `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider` instances. This is used in the `<intent-filter>` of the `<provider>`.

 Value: "android.content.action.CLOUD_MEDIA_PROVIDER"

### SEARCH_SUGGESTION_ALBUM

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 16](https://developer.android.com/sdkExtensions)

```
static val SEARCH_SUGGESTION_ALBUM: String
```

Suggestion based on user albums.

 Value: "com.android.providers.media.SEARCH_SUGGESTION_ALBUM"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.SearchSuggestionColumns#TYPE:kotlin.String`

### SEARCH_SUGGESTION_DATE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 16](https://developer.android.com/sdkExtensions)

```
static val SEARCH_SUGGESTION_DATE: String
```

Suggestion based on the date photos were taken.

 Value: "com.android.providers.media.SEARCH_SUGGESTION_DATE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.SearchSuggestionColumns#TYPE:kotlin.String`

### SEARCH_SUGGESTION_FACE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 16](https://developer.android.com/sdkExtensions)

```
static val SEARCH_SUGGESTION_FACE: String
```

Suggestion based on faces detected in photos.

 Value: "com.android.providers.media.SEARCH_SUGGESTION_FACE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.SearchSuggestionColumns#TYPE:kotlin.String`

### SEARCH_SUGGESTION_LOCATION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 16](https://developer.android.com/sdkExtensions)

```
static val SEARCH_SUGGESTION_LOCATION: String
```

Suggestion based on location data associated with photos.

 Value: "com.android.providers.media.SEARCH_SUGGESTION_LOCATION"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.SearchSuggestionColumns#TYPE:kotlin.String`

### SEARCH_SUGGESTION_TEXT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 16](https://developer.android.com/sdkExtensions)

```
static val SEARCH_SUGGESTION_TEXT: String
```

Represents a generic text search suggestion. This can be treated as a default when the type of search suggestions is unknown.

 Value: "com.android.providers.media.SEARCH_SUGGESTION_TEXT"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract.SearchSuggestionColumns#TYPE:kotlin.String`

### SORT_ORDER_DESC_DATE_TAKEN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 16](https://developer.android.com/sdkExtensions)

```
static val SORT_ORDER_DESC_DATE_TAKEN: Int
```

Sort items in descending order by the `DATE_TAKEN_MILLIS`.

This means the most recently taken photos or videos will appear first.

Type: INTEGER

 Value: 1
