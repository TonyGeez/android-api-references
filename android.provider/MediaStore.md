Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaStore

```
class MediaStore
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.provider.MediaStore](https://developer.android.com/reference/kotlin/android/provider/MediaStore#) |

The contract between the media provider and applications. Contains definitions for the supported URIs and columns.

The media provider provides an indexed collection of common media types, such as `https://developer.android.com/reference/kotlin/android/provider/MediaStore.Audio`, `https://developer.android.com/reference/kotlin/android/provider/MediaStore.Video`, and `https://developer.android.com/reference/kotlin/android/provider/MediaStore.Images`, from any attached storage devices. Each collection is organized based on the primary MIME type of the underlying content; for example, `image/*` content is indexed under `https://developer.android.com/reference/kotlin/android/provider/MediaStore.Images`. The `https://developer.android.com/reference/kotlin/android/provider/MediaStore.Files` collection provides a broad view across all collections, and does not filter by MIME type.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.Audio` Collection of all media with MIME type of `audio/*`. |
| | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.DeletedFiles` Media provider table containing records of deleted media items. |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.DownloadColumns` Download metadata columns. |
| | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.Downloads` Collection of downloaded items. |
| | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.Files` Media provider table containing an index of all files in the media storage, including non-media files. |
| | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.Images` Collection of all media with MIME type of `image/*`. |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns` Common media metadata columns. |
| | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.PickerMediaColumns` Photo picker metadata columns. |
| | `https://developer.android.com/reference/kotlin/android/provider/MediaStore.Video` Collection of all media with MIME type of `video/*`. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACCESS_MEDIA_OWNER_PACKAGE_NAME_PERMISSION:kotlin.String` Permission that grants access to `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#OWNER_PACKAGE_NAME:kotlin.String` of every accessible media file. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACCESS_OEM_METADATA_PERMISSION:kotlin.String` Permission that grants access to `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#OEM_METADATA:kotlin.String` of every accessible media file. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_IMAGE_CAPTURE:kotlin.String` Standard Intent action that can be sent to have the camera application capture an image and return it. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_IMAGE_CAPTURE_SECURE:kotlin.String` Intent action that can be sent to have the camera application capture an image and return it when the device is secured (e.g. with a pin, password, pattern, or face unlock). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_MOTION_PHOTO_CAPTURE:kotlin.String` Standard Intent action that can be sent to have the camera application capture a [motion photo](https://developer.android.com/media/platform/motion-photo-format) and return it. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_MOTION_PHOTO_CAPTURE_SECURE:kotlin.String` Intent action that can be sent to have the camera application capture a [motion photo](https://developer.android.com/media/platform/motion-photo-format) and return it when the device is secured (e.g. with a pin, password, pattern, or face unlock). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String` Activity Action: Allow the user to select images or videos provided by system and return it. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES_SETTINGS:kotlin.String` Activity Action: Launch settings controlling images or videos selection with `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_REVIEW:kotlin.String` Standard action that can be sent to review the given media file. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_REVIEW_SECURE:kotlin.String` Standard action that can be sent to review the given media file when the device is secured (e.g. with a pin, password, pattern, or face unlock). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_VIDEO_CAPTURE:kotlin.String` Standard Intent action that can be sent to have the camera application capture a video and return it. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String` The authority for the media provider |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_ACCEPT_ORIGINAL_MEDIA_FORMAT:kotlin.String` /\*\* Specify that the caller wants to receive the original media format without transcoding. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_BRIGHTNESS:kotlin.String` When defined, the launched application is requested to set the given brightness value via `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#screenBrightness:kotlin.Float` to help ensure a smooth transition when launching `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_REVIEW:kotlin.String` or `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_REVIEW_SECURE:kotlin.String` intents. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_DURATION_LIMIT:kotlin.String` Specify the maximum allowed recording duration in seconds. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_FINISH_ON_COMPLETION:kotlin.String` The name of the Intent-extra used to control the onCompletion behavior of a MovieView. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_FULL_SCREEN:kotlin.String` The name of an Intent-extra used to control the UI of a ViewImage. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_MEDIA_ALBUM:kotlin.String` The name of the Intent-extra used to define the album |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_MEDIA_ARTIST:kotlin.String` The name of the Intent-extra used to define the artist |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_MEDIA_CAPABILITIES:kotlin.String` Specify the `https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities.html#` that should be used while opening a media or picking media files. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_MEDIA_CAPABILITIES_UID:kotlin.String` Specify the UID of the app that should be used to determine supported media capabilities while opening a media. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_MEDIA_FOCUS:kotlin.String` The name of the Intent-extra used to define the search focus. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_MEDIA_GENRE:kotlin.String` The name of the Intent-extra used to define the genre. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_MEDIA_PLAYLIST:kotlin.String` The name of the Intent-extra used to define the playlist. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_MEDIA_RADIO_CHANNEL:kotlin.String` The name of the Intent-extra used to define the radio channel. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_MEDIA_TITLE:kotlin.String` The name of the Intent-extra used to define the song title |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_OUTPUT:kotlin.String` The name of the Intent-extra used to indicate a content resolver Uri to be used to store the requested image or video. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICKER_PRE_SELECTION_URIS:kotlin.String` The name of an optional intent-extra used to specify URIs for pre-selection in photo picker opened with `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String` in multi-select mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_ACCENT_COLOR:kotlin.String` The name of an optional intent-extra used to allow apps to specify the picker accent color. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_ALBUM:kotlin.String` The name of an optional intent-extra used to allow apps to highlight media results of a photopicker album in the photopicker UI whenever feasible based on the given input album in `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_SEARCH_RESULTS:kotlin.String` The name of an optional intent-extra used to allow apps to highlight search results in the photopicker UI whenever feasible based on the given input text query in `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_SEARCH_TEXT_QUERY:kotlin.String` The extra can only be specified in `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_IN_ORDER:kotlin.String` The name of an optional intent-extra used to allow ordered selection of items. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_LAUNCH_TAB:kotlin.String` The name of an optional intent-extra used to allow apps to specify the tab the picker should open with. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_MAX:kotlin.String` The name of an optional intent-extra used to allow multiple selection of items and constrain maximum number of items that can be returned by `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`, action may still return nothing (0 items) if the user chooses to cancel. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_SELECTION_PARAMS:kotlin.String` The name of an optional intent-extra used to pass `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerSelectionParams.html#` to the photo picker. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_UI_CUSTOMIZATION_PARAMS:kotlin.String` The name of an optional intent-extra used to set the ui customization options in the PhotoPicker. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_REQUEST_LOCATION_METADATA_ACCESS:kotlin.String` The name of an optional intent-extra used to allow apps to request access to the location metadata of the media items selected by the user and returned by `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_SCREEN_ORIENTATION:kotlin.String` The name of the Intent-extra used to control the orientation of a ViewImage or a MovieView. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_SHOW_ACTION_ICONS:kotlin.String` The name of an Intent-extra used to control the UI of a ViewImage. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_SIZE_LIMIT:kotlin.String` Specify the maximum allowed size. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_VIDEO_QUALITY:kotlin.String` The name of the Intent-extra used to control the quality of a recorded video. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#INTENT_ACTION_MEDIA_PLAY_FROM_SEARCH:kotlin.String` An intent to perform a search for music media and automatically play content from the result when possible. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#INTENT_ACTION_MEDIA_SEARCH:kotlin.String` Activity Action: Perform a search for media. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#INTENT_ACTION_MUSIC_PLAYER:kotlin.String` Activity Action: Launch a music player. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#INTENT_ACTION_STILL_IMAGE_CAMERA:kotlin.String` The name of the Intent action used to launch a camera in still image mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#INTENT_ACTION_STILL_IMAGE_CAMERA_SECURE:kotlin.String` The name of the Intent action used to launch a camera in still image mode for use when the device is secured (e.g. with a pin, password, pattern, or face unlock). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#INTENT_ACTION_TEXT_OPEN_FROM_SEARCH:kotlin.String` An intent to perform a search for readable media and automatically play content from the result when possible. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#INTENT_ACTION_VIDEO_CAMERA:kotlin.String` The name of the Intent action used to launch a camera in video mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#INTENT_ACTION_VIDEO_PLAY_FROM_SEARCH:kotlin.String` An intent to perform a search for video media and automatically play content from the result when possible. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID:kotlin.String` One of the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` keys for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_ALBUM:kotlin.String` specifying the photopicker album for which the app can request to show highlighted media results in the photopicker. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_SEARCH_TEXT_QUERY:kotlin.String` One of the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` keys for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_SEARCH_RESULTS:kotlin.String` specifying the input query for which the app can request to show highlighted media results in the photopicker. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_TYPE:kotlin.String` One of the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` keys for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_SEARCH_RESULTS:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_ALBUM:kotlin.String` to specify the highlight type i. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MATCH_DEFAULT:kotlin.Int` Value indicating that the default matching behavior should be used, as defined by the key documentation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MATCH_EXCLUDE:kotlin.Int` Value indicating that operations should exclude items matching the criteria defined by this key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MATCH_INCLUDE:kotlin.Int` Value indicating that operations should include items matching the criteria defined by this key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MATCH_ONLY:kotlin.Int` Value indicating that operations should only operate on items explicitly matching the criteria defined by this key. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MEDIA_IGNORE_FILENAME:kotlin.String` Name of the file signaling the media scanner to ignore media in the containing directory and its subdirectories. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MEDIA_SCANNER_VOLUME:kotlin.String` Name of current volume being scanned by the media scanner. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#META_DATA_REVIEW_GALLERY_PREWARM_SERVICE:kotlin.String` Name under which an activity handling `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_REVIEW:kotlin.String` or `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_REVIEW_SECURE:kotlin.String` publishes the service name for its prewarm service. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#META_DATA_STILL_IMAGE_CAMERA_PREWARM_SERVICE:kotlin.String` Name under which an activity handling `https://developer.android.com/reference/kotlin/android/provider/MediaStore#INTENT_ACTION_STILL_IMAGE_CAMERA:kotlin.String` or `https://developer.android.com/reference/kotlin/android/provider/MediaStore#INTENT_ACTION_STILL_IMAGE_CAMERA_SECURE:kotlin.String` publishes the service name for its prewarm service. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_ALBUM_CAMERA:kotlin.String` One of the possible album highlight values for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID:kotlin.String` in case an app chooses to highlight media results from an album, in this case, the Camera album. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_ALBUM_DOWNLOADS:kotlin.String` One of the possible album highlight values for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID:kotlin.String` in case an app chooses to highlight media results from an album, in this case, the Downloads album. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_ALBUM_FAVORITES:kotlin.String` One of the possible album highlight values for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID:kotlin.String` in case an app chooses to highlight media results from an album, in this case, the Favorites album. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_ALBUM_SCREENSHOTS:kotlin.String` One of the possible album highlight values for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID:kotlin.String` in case an app chooses to highlight media results from from an album, in this case, the Screenshots album. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_ALBUM_VIDEOS:kotlin.String` One of the possible album highlight values for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID:kotlin.String` in case an app chooses to highlight media results from an album, in this case, the Videos album. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_TYPE_COLLAPSED:kotlin.Int` One of the permitted values for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_TYPE:kotlin.String` to highlight media results as a highlighted media section in the photopicker based on the given input query in `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_SEARCH_TEXT_QUERY:kotlin.String` or the given input photopicker album in MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID}. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_TYPE_EXPANDED:kotlin.Int` One of the permitted values for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_TYPE:kotlin.String` to show a highlighted media results grid based on the given input query in `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_SEARCH_TEXT_QUERY:kotlin.String` or the given input photopicker album in MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID}. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_TAB_ALBUMS:kotlin.Int` One of the permitted values for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_LAUNCH_TAB:kotlin.String` to open the picker with albums tab. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_TAB_IMAGES:kotlin.Int` One of the permitted values for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_LAUNCH_TAB:kotlin.String` to open the picker with photos tab. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#QUERY_ARG_INCLUDE_RECENTLY_UNMOUNTED_VOLUMES:kotlin.String` Flag that requests android. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#QUERY_ARG_LATEST_SELECTION_ONLY:kotlin.String` Flag that indicates if only the latest selection in the photoPicker for the calling app should be returned. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#QUERY_ARG_MATCH_FAVORITE:kotlin.String` Specify how `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_FAVORITE:kotlin.String` items should be filtered when performing a `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` operation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#QUERY_ARG_MATCH_PENDING:kotlin.String` Specify how `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_PENDING:kotlin.String` items should be filtered when performing a `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` operation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#QUERY_ARG_MATCH_TRASHED:kotlin.String` Specify how `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_TRASHED:kotlin.String` items should be filtered when performing a `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` operation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#QUERY_ARG_MEDIA_STANDARD_SORT_ORDER:kotlin.String` Flag that requests android. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#QUERY_ARG_RELATED_URI:kotlin.String` Specify a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` that is "related" to the current operation being performed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#UNKNOWN_STRING:kotlin.String` The string that is used when a media attribute is not known. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#VOLUME_EXTERNAL:kotlin.String` Synthetic volume name that provides a view of all content across the "external" storage of the device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#VOLUME_EXTERNAL_PRIMARY:kotlin.String` Specific volume name that represents the primary external storage device at `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageDirectory()`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#VOLUME_INTERNAL:kotlin.String` Synthetic volume name that provides a view of all content across the "internal" storage of the device. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MediaStore()()` <br /> |

| Public methods ||
|---|---|
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#canManageMedia(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Returns whether the calling app is granted `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_MEDIA:kotlin.String` or not. |
| static [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#createDeleteRequest(android.content.ContentResolver,%20kotlin.collections.MutableCollection)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>)` Create a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` that will prompt the user to permanently delete the requested media items. |
| static [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#createFavoriteRequest(android.content.ContentResolver,%20kotlin.collections.MutableCollection,%20kotlin.Boolean)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Create a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` that will prompt the user to favorite the requested media items. |
| static [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#createTrashRequest(android.content.ContentResolver,%20kotlin.collections.MutableCollection,%20kotlin.Boolean)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Create a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` that will prompt the user to trash the requested media items. |
| static [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#createWriteRequest(android.content.ContentResolver,%20kotlin.collections.MutableCollection)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>)` Create a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` that will prompt the user to grant your app write access for the requested media items. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getDocumentUri(android.content.Context,%20android.net.Uri)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, mediaUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Return a `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` Uri that is an equivalent to the given `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` Uri. |
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getExternalVolumeNames(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Return list of all specific volume names that make up `https://developer.android.com/reference/kotlin/android/provider/MediaStore#VOLUME_EXTERNAL:kotlin.String`. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getGeneration(android.content.Context,%20kotlin.String)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, volumeName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Return the latest generation value for the given volume. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getMediaScannerUri()()` Uri for querying the state of the media scanner. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getMediaUri(android.content.Context,%20android.net.Uri)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, documentUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Return a `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` Uri that is an equivalent to the given `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` Uri. |
| static [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getOriginalMediaFormatFileDescriptor(android.content.Context,%20android.os.ParcelFileDescriptor)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, fileDescriptor: https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)` Returns `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` representing the original media file format for `fileDescriptor`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getPackageForSearchMediaService(android.content.ContentResolver)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#)` Gets the package name of the `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` that client apps use to connect. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getPickImagesMaxLimit()()` The maximum limit for the number of items that can be selected using `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String` when launched in multiple selection mode. |
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getRecentExternalVolumeNames(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Return list of all recent volume names that have been part of `https://developer.android.com/reference/kotlin/android/provider/MediaStore#VOLUME_EXTERNAL:kotlin.String`. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getRedactedUri(android.content.ContentResolver,%20android.net.Uri)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Returns an EXIF redacted version of `uri` i. |
| static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\> | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getRedactedUri(android.content.ContentResolver,%20kotlin.collections.MutableList)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>)` Returns a list of EXIF redacted version of `uris` i. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getRequireOriginal(android.net.Uri)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Return if the caller requires the original file contents when calling `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFileDescriptor(android.net.Uri,%20kotlin.String)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getVersion(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Return an opaque version string describing the `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` state. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getVersion(android.content.Context,%20kotlin.String)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, volumeName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Return an opaque version string describing the `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` state. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getVolumeName(android.net.Uri)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Return the volume name that the given `https://developer.android.com/reference/kotlin/android/net/Uri.html#` references. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#isCurrentCloudMediaProviderAuthority(android.content.ContentResolver,%20kotlin.String)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns `true` if and only if the caller with `authority` is the currently enabled `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider`. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#isCurrentSystemGallery(android.content.ContentResolver,%20kotlin.Int,%20kotlin.String)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns true if the given application is the current system gallery of the device. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#isSupportedCloudMediaProviderAuthority(android.content.ContentResolver,%20kotlin.String)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns `true` if and only if the caller with `authority` is a supported `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider`. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#markIsFavoriteStatus(android.content.ContentResolver,%20kotlin.collections.MutableCollection,%20kotlin.Boolean)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>, areFavorites: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets the media isFavorite status if the calling app has wider read permission on media files for given type. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#notifyCloudMediaChangedEvent(android.content.ContentResolver,%20kotlin.String,%20kotlin.String)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, currentMediaCollectionId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Notifies the OS about a cloud media event requiring a full or incremental media collection sync for the currently enabled cloud provider, `authority`. |
| static [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#)? | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#openAssetFileDescriptor(android.content.ContentResolver,%20android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Works exactly the same as `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal)`, but only works for `https://developer.android.com/reference/kotlin/android/net/Uri.html#` whose scheme is `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_CONTENT:kotlin.String` and its authority is `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String`. |
| static [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#openFileDescriptor(android.content.ContentResolver,%20android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Works exactly the same as `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal)`, but only works for `https://developer.android.com/reference/kotlin/android/net/Uri.html#` whose scheme is `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_CONTENT:kotlin.String` and its authority is `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String`. |
| static [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#)? | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#openTypedAssetFileDescriptor(android.content.ContentResolver,%20android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, mimeType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, opts: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Works exactly the same as `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openTypedAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)`, but only works for `https://developer.android.com/reference/kotlin/android/net/Uri.html#` whose scheme is `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_CONTENT:kotlin.String` and its authority is `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String`. |
| static [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#queryDeletedFiles(android.content.ContentResolver,%20android.os.Bundle,%20android.os.CancellationSignal)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, queryArgs: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?)` Returns a cursor of deleted items matching the given query arguments. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#restoreFileFromTrash(android.content.ContentResolver,%20kotlin.String,%20kotlin.String)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, targetPath: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Restores a file or directory from a trashed state. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#setIncludePending(android.net.Uri)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Update the given `https://developer.android.com/reference/kotlin/android/net/Uri.html#` to also include any pending media items from calls such as `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)`. |
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#setRequireOriginal(android.net.Uri)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Update the given `https://developer.android.com/reference/kotlin/android/net/Uri.html#` to indicate that the caller requires the original file contents when calling `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFileDescriptor(android.net.Uri,%20kotlin.String)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#trashFile(android.content.ContentResolver,%20kotlin.String)(resolver: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Moves a file or directory to a trashed state. |

| Properties ||
|---|---|
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY_URI:android.net.Uri` A content:// style uri to the authority for the media provider |

## Constants

### ACCESS_MEDIA_OWNER_PACKAGE_NAME_PERMISSION

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACCESS_MEDIA_OWNER_PACKAGE_NAME_PERMISSION: String
```

Permission that grants access to `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#OWNER_PACKAGE_NAME:kotlin.String` of every accessible media file.

 Value: "com.android.providers.media.permission.ACCESS_MEDIA_OWNER_PACKAGE_NAME"

### ACCESS_OEM_METADATA_PERMISSION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 15](https://developer.android.com/sdkExtensions)

```
static val ACCESS_OEM_METADATA_PERMISSION: String
```

Permission that grants access to `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#OEM_METADATA:kotlin.String` of every accessible media file.

 Value: "com.android.providers.media.permission.ACCESS_OEM_METADATA"

### ACTION_IMAGE_CAPTURE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_IMAGE_CAPTURE: String
```

Standard Intent action that can be sent to have the camera application capture an image and return it.

The caller may pass an extra EXTRA_OUTPUT to control where this image will be written. If the EXTRA_OUTPUT is not present, then a small sized image is returned as a Bitmap object in the extra field. This is useful for applications that only need a small image. If the EXTRA_OUTPUT is present, then the full-sized image will be written to the Uri value of EXTRA_OUTPUT. As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`, this uri can also be supplied through `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClipData(android.content.ClipData)`. If using this approach, you still must supply the uri through the EXTRA_OUTPUT field for compatibility with old applications. If you don't set a ClipData, it will be copied there for you when calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)`.

Regardless of whether or not EXTRA_OUTPUT is present, when an image is captured via this intent, `https://developer.android.com/reference/kotlin/android/hardware/Camera.html#ACTION_NEW_PICTURE:kotlin.String` won't be broadcasted.

Note: if you app targets `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int` and above and declares as using the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` permission which is not granted, then attempting to use this action will result in a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

 Value: "android.media.action.IMAGE_CAPTURE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_OUTPUT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/hardware/Camera.html#ACTION_NEW_PICTURE:kotlin.String`

### ACTION_IMAGE_CAPTURE_SECURE

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_IMAGE_CAPTURE_SECURE: String
```

Intent action that can be sent to have the camera application capture an image and return it when the device is secured (e.g. with a pin, password, pattern, or face unlock). Applications responding to this intent must not expose any personal content like existing photos or videos on the device. The applications should be careful not to share any photo or video with other applications or Internet. The activity should use `https://developer.android.com/reference/kotlin/android/app/Activity.html#setShowWhenLocked(kotlin.Boolean)` to display on top of the lock screen while secured. There is no activity stack when this flag is used, so launching more than one activity is strongly discouraged.

The caller may pass an extra EXTRA_OUTPUT to control where this image will be written. If the EXTRA_OUTPUT is not present, then a small sized image is returned as a Bitmap object in the extra field. This is useful for applications that only need a small image. If the EXTRA_OUTPUT is present, then the full-sized image will be written to the Uri value of EXTRA_OUTPUT. As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`, this uri can also be supplied through `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClipData(android.content.ClipData)`. If using this approach, you still must supply the uri through the EXTRA_OUTPUT field for compatibility with old applications. If you don't set a ClipData, it will be copied there for you when calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)`.

Regardless of whether or not EXTRA_OUTPUT is present, when an image is captured via this intent, `https://developer.android.com/reference/kotlin/android/hardware/Camera.html#ACTION_NEW_PICTURE:kotlin.String` won't be broadcasted.

 Value: "android.media.action.IMAGE_CAPTURE_SECURE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_IMAGE_CAPTURE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_OUTPUT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/hardware/Camera.html#ACTION_NEW_PICTURE:kotlin.String`

### ACTION_MOTION_PHOTO_CAPTURE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MOTION_PHOTO_CAPTURE: String
```

Standard Intent action that can be sent to have the camera application capture a [motion photo](https://developer.android.com/media/platform/motion-photo-format) and return it.

The caller must either pass an extra EXTRA_OUTPUT to control where the image will be written, or a uri through `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClipData(android.content.ClipData)`. If you don't set a ClipData, it will be copied there for you when calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)`.

When an image is captured via this intent, `https://developer.android.com/reference/kotlin/android/hardware/Camera.html#ACTION_NEW_PICTURE:kotlin.String` won't be broadcasted.

Note: If your app declares as using the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` permission which is not granted, then attempting to use this action will result in a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

 Value: "android.provider.action.MOTION_PHOTO_CAPTURE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_OUTPUT:kotlin.String`

### ACTION_MOTION_PHOTO_CAPTURE_SECURE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MOTION_PHOTO_CAPTURE_SECURE: String
```

Intent action that can be sent to have the camera application capture a [motion photo](https://developer.android.com/media/platform/motion-photo-format) and return it when the device is secured (e.g. with a pin, password, pattern, or face unlock). Applications responding to this intent must not expose any personal content like existing photos or videos on the device. The applications should be careful not to share any photo or video with other applications or Internet. The activity should use `https://developer.android.com/reference/kotlin/android/app/Activity.html#setShowWhenLocked(kotlin.Boolean)` to display on top of the lock screen while secured. There is no activity stack when this flag is used, so launching more than one activity is strongly discouraged.

The caller must either pass an extra EXTRA_OUTPUT to control where the image will be written, or a uri through `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClipData(android.content.ClipData)`. If you don't set a ClipData, it will be copied there for you when calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)`.

When an image is captured via this intent, `https://developer.android.com/reference/kotlin/android/hardware/Camera.html#ACTION_NEW_PICTURE:kotlin.String` won't be broadcasted.

 Value: "android.provider.action.MOTION_PHOTO_CAPTURE_SECURE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_MOTION_PHOTO_CAPTURE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_OUTPUT:kotlin.String`

### ACTION_PICK_IMAGES

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 2](https://developer.android.com/sdkExtensions)

```
static val ACTION_PICK_IMAGES: String
```

Activity Action: Allow the user to select images or videos provided by system and return it. This is different than `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PICK:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_GET_CONTENT:kotlin.String` in that

- the data for this action is provided by the system
- this action is only used for picking images and videos
- caller gets read access to user picked items even without storage permissions

<br />

Callers can optionally specify MIME type (such as `image/*` or `video/*`), resulting in a range of content selection that the caller is interested in. The optional MIME type can be requested with `https://developer.android.com/reference/kotlin/android/content/Intent.html#setType(kotlin.String)`.

If the caller needs multiple returned items (or caller wants to allow multiple selection), then it can specify `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_MAX:kotlin.String` to indicate this.

When the caller requests multiple selection, the value of `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_MAX:kotlin.String` must be a positive integer greater than 1 and less than or equal to `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getPickImagesMaxLimit()`, otherwise `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int` is returned. Use `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_IN_ORDER:kotlin.String` in multiple selection mode to allow the user to pick images in order.

If the caller needs to specify the `https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities.html#` that should be used while picking video files, use `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_MEDIA_CAPABILITIES:kotlin.String` to indicate this.

When the requested file format does not match the capabilities specified by caller and the video duration is within the range that the system can handle, it will get transcoded to a default supported format, otherwise, the caller will receive the original file.

Callers may use `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_LOCAL_ONLY:kotlin.String` to limit content selection to local data.

For system stability, it is preferred to open the URIs obtained from using this action by calling `https://developer.android.com/reference/kotlin/android/provider/MediaStore#openFileDescriptor(android.content.ContentResolver,%20android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal)`, `https://developer.android.com/reference/kotlin/android/provider/MediaStore#openAssetFileDescriptor(android.content.ContentResolver,%20android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal)` or `https://developer.android.com/reference/kotlin/android/provider/MediaStore#openTypedAssetFileDescriptor(android.content.ContentResolver,%20android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)` instead of `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#` open APIs.

Output: MediaStore content URI(s) of the item(s) that was picked. Unlike other MediaStore URIs, these are referred to as 'picker' URIs and expose a limited set of read-only operations. Specifically, picker URIs can only be opened for read and queried for columns in `https://developer.android.com/reference/kotlin/android/provider/MediaStore.PickerMediaColumns`.

Before this API, apps could use `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_GET_CONTENT:kotlin.String`. However, `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String` is now the recommended option for images and videos, since it offers a better user experience.

 Value: "android.provider.action.PICK_IMAGES"

### ACTION_PICK_IMAGES_SETTINGS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
static val ACTION_PICK_IMAGES_SETTINGS: String
```

Activity Action: Launch settings controlling images or videos selection with `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`. The settings page allows a user to change the enabled `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider` on the device and other media selection configurations.

 Value: "android.provider.action.PICK_IMAGES_SETTINGS"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#isCurrentCloudMediaProviderAuthority(android.content.ContentResolver,%20kotlin.String)`

### ACTION_REVIEW

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_REVIEW: String
```

Standard action that can be sent to review the given media file.

The launched application is expected to provide a large-scale view of the given media file, while allowing the user to quickly access other recently captured media files.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()` is URI of the primary media item to initially display.

 Value: "android.provider.action.REVIEW"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_REVIEW_SECURE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_BRIGHTNESS:kotlin.String`

### ACTION_REVIEW_SECURE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_REVIEW_SECURE: String
```

Standard action that can be sent to review the given media file when the device is secured (e.g. with a pin, password, pattern, or face unlock). The applications should be careful not to share any media with other applications or Internet. The activity should use `https://developer.android.com/reference/kotlin/android/app/Activity.html#setShowWhenLocked(kotlin.Boolean)` to display on top of the lock screen while secured. There is no activity stack when this flag is used, so launching more than one activity is strongly discouraged.

The launched application is expected to provide a large-scale view of the given primary media file, while only allowing the user to quickly access other media from an explicit secondary list.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()` is URI of the primary media item to initially display. `https://developer.android.com/reference/kotlin/android/content/Intent.html#getClipData()` is the limited list of secondary media items that the user is allowed to review. If `https://developer.android.com/reference/kotlin/android/content/Intent.html#getClipData()` is undefined, then no other media access should be allowed.

 Value: "android.provider.action.REVIEW_SECURE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_BRIGHTNESS:kotlin.String`

### ACTION_VIDEO_CAPTURE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_VIDEO_CAPTURE: String
```

Standard Intent action that can be sent to have the camera application capture a video and return it.

The caller may pass in an extra EXTRA_VIDEO_QUALITY to control the video quality.

The caller may pass in an extra EXTRA_OUTPUT to control where the video is written.

- If EXTRA_OUTPUT is not present, the video will be written to the standard location for videos, and the Uri of that location will be returned in the data field of the Uri. `https://developer.android.com/reference/kotlin/android/hardware/Camera.html#ACTION_NEW_VIDEO:kotlin.String` will also be broadcasted when the video is recorded.
- If EXTRA_OUTPUT is assigned a Uri value, no `https://developer.android.com/reference/kotlin/android/hardware/Camera.html#ACTION_NEW_VIDEO:kotlin.String` will be broadcasted. As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`, this uri can also be supplied through `https://developer.android.com/reference/kotlin/android/content/Intent.html#setClipData(android.content.ClipData)`. If using this approach, you still must supply the uri through the EXTRA_OUTPUT field for compatibility with old applications. If you don't set a ClipData, it will be copied there for you when calling `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)`.

Note: if you app targets `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int` and above and declares as using the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` permission which is not granted, then atempting to use this action will result in a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

 Value: "android.media.action.VIDEO_CAPTURE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_OUTPUT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_VIDEO_QUALITY:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_SIZE_LIMIT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_DURATION_LIMIT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/hardware/Camera.html#ACTION_NEW_VIDEO:kotlin.String`

### AUTHORITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHORITY: String
```

The authority for the media provider

 Value: "media"

### EXTRA_ACCEPT_ORIGINAL_MEDIA_FORMAT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ACCEPT_ORIGINAL_MEDIA_FORMAT: String
```

/\*\* Specify that the caller wants to receive the original media format without transcoding. **Caution: using this flag can cause app compatibility issues whenever Android adds support for new media formats.** Clients should instead specify their supported media capabilities explicitly in their manifest or with the `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_MEDIA_CAPABILITIES:kotlin.String` `open` flag. This option is useful for apps that don't attempt to parse the actual byte contents of media files, such as playback using `https://developer.android.com/reference/kotlin/android/media/MediaPlayer.html#` or for off-device backup. Note that the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_MEDIA_LOCATION:kotlin.String` permission will still be required to avoid sensitive metadata redaction, similar to `https://developer.android.com/reference/kotlin/android/provider/MediaStore#setRequireOriginal(android.net.Uri)`. Note that this flag overrides any explicitly declared `media_capabilities.xml` or `https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities.html#` extras specified in the same `open` request.

This option can be added to the `opts` `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` in various `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#` `open` methods.

 Value: "android.provider.extra.ACCEPT_ORIGINAL_MEDIA_FORMAT"

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openTypedAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openTypedAssetFile(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#setRequireOriginal(android.net.Uri)`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getOriginalMediaFormatFileDescriptor(android.content.Context,%20android.os.ParcelFileDescriptor)`

### EXTRA_BRIGHTNESS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_BRIGHTNESS: String
```

When defined, the launched application is requested to set the given brightness value via `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#screenBrightness:kotlin.Float` to help ensure a smooth transition when launching `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_REVIEW:kotlin.String` or `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_REVIEW_SECURE:kotlin.String` intents.

 Value: "android.provider.extra.BRIGHTNESS"

### EXTRA_DURATION_LIMIT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DURATION_LIMIT: String
```

Specify the maximum allowed recording duration in seconds.

 Value: "android.intent.extra.durationLimit"

### EXTRA_FINISH_ON_COMPLETION

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_FINISH_ON_COMPLETION: String
```

The name of the Intent-extra used to control the onCompletion behavior of a MovieView. This is a boolean property that specifies whether or not to finish the MovieView activity when the movie completes playing. The default value is true, which means to automatically exit the movie player activity when the movie completes playing.

 Value: "android.intent.extra.finishOnCompletion"

### EXTRA_FULL_SCREEN

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_FULL_SCREEN: String
```

The name of an Intent-extra used to control the UI of a ViewImage. This is a boolean property that overrides the activity's default fullscreen state.

 Value: "android.intent.extra.fullScreen"

### EXTRA_MEDIA_ALBUM

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MEDIA_ALBUM: String
```

The name of the Intent-extra used to define the album

 Value: "android.intent.extra.album"

### EXTRA_MEDIA_ARTIST

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MEDIA_ARTIST: String
```

The name of the Intent-extra used to define the artist

 Value: "android.intent.extra.artist"

### EXTRA_MEDIA_CAPABILITIES

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MEDIA_CAPABILITIES: String
```

Specify the `https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities.html#` that should be used while opening a media or picking media files.

If the capabilities specified matches the format of the original file, the app will receive the original file, otherwise, it will get transcoded to a default supported format.

When used while opening a media, add this option to the `opts` `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` in various `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#` `open` methods. This flag takes higher precedence over the applications declared `media_capabilities.xml` and is useful for apps that want to have more granular control over their supported media capabilities.

When used while picking media files, add this option to the intent-extra of `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`.

 Value: "android.provider.extra.MEDIA_CAPABILITIES"

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openTypedAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openTypedAssetFile(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`

### EXTRA_MEDIA_CAPABILITIES_UID

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MEDIA_CAPABILITIES_UID: String
```

Specify the UID of the app that should be used to determine supported media capabilities while opening a media. If this specified UID is found to be capable of handling the original media file format, the app will receive the original file, otherwise, the file will get transcoded to a default format supported by the specified UID.

 Value: "android.provider.extra.MEDIA_CAPABILITIES_UID"

### EXTRA_MEDIA_FOCUS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MEDIA_FOCUS: String
```

The name of the Intent-extra used to define the search focus. The search focus indicates whether the search should be for things related to the artist, album or song that is identified by the other extras.

 Value: "android.intent.extra.focus"

### EXTRA_MEDIA_GENRE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MEDIA_GENRE: String
```

The name of the Intent-extra used to define the genre.

 Value: "android.intent.extra.genre"

### EXTRA_MEDIA_PLAYLIST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MEDIA_PLAYLIST: String
```

**Deprecated:** *Android playlists are now deprecated. We will keep the current functionality for compatibility resons, but we will no longer take feature request. We do not advise adding new usages of Android Playlists. M3U files can be used as an alternative.*

The name of the Intent-extra used to define the playlist.

 Value: "android.intent.extra.playlist"

### EXTRA_MEDIA_RADIO_CHANNEL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MEDIA_RADIO_CHANNEL: String
```

The name of the Intent-extra used to define the radio channel.

 Value: "android.intent.extra.radio_channel"

### EXTRA_MEDIA_TITLE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MEDIA_TITLE: String
```

The name of the Intent-extra used to define the song title

 Value: "android.intent.extra.title"

### EXTRA_OUTPUT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_OUTPUT: String
```

The name of the Intent-extra used to indicate a content resolver Uri to be used to store the requested image or video.

 Value: "output"

### EXTRA_PICKER_PRE_SELECTION_URIS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 15](https://developer.android.com/sdkExtensions)

```
static val EXTRA_PICKER_PRE_SELECTION_URIS: String
```

The name of an optional intent-extra used to specify URIs for pre-selection in photo picker opened with `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String` in multi-select mode.

Only MediaStore content URI(s) of the item(s) received as a result of `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String` action are accepted. The value of this intent-extra should be an ArrayList of type URIs. Default value is null. Maximum number of URIs that can be accepted is limited by the value passed in `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_MAX:kotlin.String` as part of the `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String` intent. In case the count of input URIs is greater than the limit then `IllegalArgumentException` is thrown.

The provided list will be checked for permissions and authority. Any URI that is inaccessible, doesn't match the current authorities(local or cloud) or is invalid will be filtered out. Additionally, items that are disabled based on the provided `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_SELECTION_PARAMS:kotlin.String` will also be filtered out.

The remaining items will appear selected when the photo picker is opened, provided they satisfy the aggregate constraints such as `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_MAX:kotlin.String` and `PhotoPickerSelectionParams.getMaxSelectionBatchSizeInBytes()`. In the case of `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_IN_ORDER:kotlin.String` the chronological order of the input list will be used for ordered selection of the pre-selected items.

This is not a mechanism to revoke permissions for items, i.e. de-selection of a pre-selected item by the user will not result in revocation of the grant.

 Value: "android.provider.extra.PICKER_PRE_SELECTION_URIS"

### EXTRA_PICK_IMAGES_ACCENT_COLOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 12](https://developer.android.com/sdkExtensions)

```
static val EXTRA_PICK_IMAGES_ACCENT_COLOR: String
```

The name of an optional intent-extra used to allow apps to specify the picker accent color. The extra can only be specified in `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`. The accent color will be used for various primary elements in the PhotoPicker view. All other colors will be set based on android material guidelines.

The value of this intent extra should be a long color value. The alpha component of the given color is not taken into account while setting the accent color. We assume full color opacity. Only colors with luminance(can also be understood as brightness) greater than 0.05 and less than 0.9 are permitted. Luminance of a color is determined using: luminance = Color.luminance(color) where color is the input accent color to be set. Check Color docs for more details on color luminance and long color values. In case the luminance of the input color is unacceptable, picker colors will be set based on the colors of the device android theme. In case of an invalid input color value i.e. the input color cannot be parsed, `IllegalArgumentException` is thrown.

 Value: "android.provider.extra.PICK_IMAGES_ACCENT_COLOR"

### EXTRA_PICK_IMAGES_HIGHLIGHT_ALBUM

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PICK_IMAGES_HIGHLIGHT_ALBUM: String
```

The name of an optional intent-extra used to allow apps to highlight media results of a photopicker album in the photopicker UI whenever feasible based on the given input album in `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID:kotlin.String`. The extra can only be specified in `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`.

This intent extra will accept a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` object. The bundle object should have two keys specified. The first key `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_TYPE:kotlin.String` will specify the type of media highlight the app wants to opt for and should be one of `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_TYPE_COLLAPSED:kotlin.Int` for a highlighted media section to be shown when the photopicker launches or `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_TYPE_EXPANDED:kotlin.Int` to open the photopicker to show a highlighted media results grid based on the given input album. Any other value for this key will result in throwing `IllegalArgumentException`. The second bundle key `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID:kotlin.String` will specify the album to be highlighted and its value should be one of: `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_ALBUM_FAVORITES:kotlin.String` for the Favorites album, `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_ALBUM_CAMERA:kotlin.String` for the Camera album, `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_ALBUM_SCREENSHOTS:kotlin.String` for the Screenshots album, `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_ALBUM_VIDEOS:kotlin.String` for the Videos album and `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_ALBUM_DOWNLOADS:kotlin.String` for the Downloads album. Any other value for this key will result in throwing `IllegalArgumentException`. Highlighting media results based on an input string text query is also supported. See `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_SEARCH_RESULTS:kotlin.String` for more details. Only one of `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_SEARCH_RESULTS:kotlin.String` or `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_ALBUM:kotlin.String` should be used at any given time. Specifying both will result in `IllegalArgumentException` to be thrown.

 Value: "android.provider.extra.PICK_IMAGES_HIGHLIGHT_ALBUM"

### EXTRA_PICK_IMAGES_HIGHLIGHT_SEARCH_RESULTS

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PICK_IMAGES_HIGHLIGHT_SEARCH_RESULTS: String
```

The name of an optional intent-extra used to allow apps to highlight search results in the photopicker UI whenever feasible based on the given input text query in `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_SEARCH_TEXT_QUERY:kotlin.String` The extra can only be specified in `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`.

This intent extra will accept a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` object. The bundle object should have two keys specified. The first key `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_TYPE:kotlin.String` will specify the type of media highlight the app wants to opt for and should be one of `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_TYPE_COLLAPSED:kotlin.Int` for a highlighted media section to be shown when the photopicker launches or `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_TYPE_EXPANDED:kotlin.Int` to open the photopicker to show a highlighted media results grid based on the given input query. Any other value for this key will result in throwing `IllegalArgumentException`. The second bundle key `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_SEARCH_TEXT_QUERY:kotlin.String` will accept a string value specifying the query for highlighting media results. If this input value is empty, the request to highlight media will be ignored and no highlight will be shown at all. In case of null input query, `IllegalArgumentException` is thrown. Highlighting media results of a photopicker album is also supported. See `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_ALBUM:kotlin.String` for more details. Only one of `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_SEARCH_RESULTS:kotlin.String` or `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_ALBUM:kotlin.String` should be used at any given time. Specifying both will result in `IllegalArgumentException` to be thrown.

 Value: "android.provider.extra.PICK_IMAGES_HIGHLIGHT_SEARCH_RESULTS"

### EXTRA_PICK_IMAGES_IN_ORDER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 12](https://developer.android.com/sdkExtensions)

```
static val EXTRA_PICK_IMAGES_IN_ORDER: String
```

The name of an optional intent-extra used to allow ordered selection of items. Set this extra to true to allow the user to see the order of their selected items. The result returned to the caller will be the same as the user selected order. This extra is only allowed via the `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`.

The value of this intent-extra should be a boolean. Default value is false.

 Value: "android.provider.extra.PICK_IMAGES_IN_ORDER"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`

### EXTRA_PICK_IMAGES_LAUNCH_TAB

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 12](https://developer.android.com/sdkExtensions)

```
static val EXTRA_PICK_IMAGES_LAUNCH_TAB: String
```

The name of an optional intent-extra used to allow apps to specify the tab the picker should open with. The extra can only be specified in `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`.

The value of this intent-extra must be one of: `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_TAB_ALBUMS:kotlin.Int` for the albums tab and `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_TAB_IMAGES:kotlin.Int` for the photos tab. The system will decide which tab to open by default and in most cases, it is `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_TAB_IMAGES:kotlin.Int` i.e. the photos tab.

 Value: "android.provider.extra.PICK_IMAGES_LAUNCH_TAB"

### EXTRA_PICK_IMAGES_MAX

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 2](https://developer.android.com/sdkExtensions)

```
static val EXTRA_PICK_IMAGES_MAX: String
```

The name of an optional intent-extra used to allow multiple selection of items and constrain maximum number of items that can be returned by `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`, action may still return nothing (0 items) if the user chooses to cancel.

The value of this intent-extra should be a positive integer greater than 1 and less than or equal to `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getPickImagesMaxLimit()`, otherwise `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int` is returned.

If `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICKER_PRE_SELECTION_URIS:kotlin.String` is also provided, the number of URIs in that list must not exceed this value, otherwise an `IllegalIntentExtraException` will be thrown.

 Value: "android.provider.extra.PICK_IMAGES_MAX"

### EXTRA_PICK_IMAGES_SELECTION_PARAMS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PICK_IMAGES_SELECTION_PARAMS: String
```

The name of an optional intent-extra used to pass `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerSelectionParams.html#` to the photo picker. This extra can only be specified in `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`.

The `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerSelectionParams.html#` object allows the calling app to set constraints on the media items that can be selected by the user. Media items that fail to satisfy these constraints will be disabled for selection.

Not passing this EXTRA, means the photo picker will not apply any restrictions on what media items users can select (except for the MIME type specified in the `https://developer.android.com/reference/kotlin/android/content/Intent.html#setType(kotlin.String)` extra).

To use this key, calling apps should construct a `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerSelectionParams.html#` object using its `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerSelectionParams.Builder.html#` and pass it as the value. 
Example: If the calling app wants to allow selection of only those media items that have a maximum size of 10,000 bytes and a minimum resolution of 500 pixels:

```kotlin
PhotoPickerSelectionParams selectionParams = new PhotoPickerSelectionParams.Builder()
      .setMaxMediaItemSizeInBytes(10000L)
      .setMinMediaItemResolutionInPixels(500L)
      .build();
  Intent intent = new Intent(MediaStore.ACTION_PICK_IMAGES);
  intent.putExtra(MediaStore.EXTRA_PICK_IMAGES_SELECTION_PARAMS, selectionParams);
  
```

 Value: "android.provider.extra.PICK_IMAGES_SELECTION_PARAMS"

### EXTRA_PICK_IMAGES_UI_CUSTOMIZATION_PARAMS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PICK_IMAGES_UI_CUSTOMIZATION_PARAMS: String
```

The name of an optional intent-extra used to set the ui customization options in the PhotoPicker.

The value of this intent-extra should be a `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams.html#` object. The extra can only be specified in `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`.

Not passing this EXTRA, means the photo picker will use its default UI (e.g. rendering the media items grid in 1:1 aspect ratio).

To use this key, calling apps should construct a `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams.html#` object using its `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams.Builder.html#` and pass it as the value. 
Example: If the calling app wants to allow the Photo Picker to use a 9:16 aspect ratio for the thumbnails:

```kotlin
PhotoPickerUiCustomizationParams params = new PhotoPickerUiCustomizationParams.Builder()
      .setAspectRatio(PhotoPickerUiCustomizationParams.ASPECT_RATIO_PORTRAIT_9_16)
      .build();
  Intent intent = new Intent(MediaStore.ACTION_PICK_IMAGES);
  intent.putExtra(MediaStore.EXTRA_PICK_IMAGES_UI_CUSTOMIZATION_PARAMS, params);
  
```

 Value: "android.provider.extra.PICK_IMAGES_UI_CUSTOMIZATION_PARAMS"

**See Also**

- `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams.html#`

### EXTRA_REQUEST_LOCATION_METADATA_ACCESS

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_REQUEST_LOCATION_METADATA_ACCESS: String
```

The name of an optional intent-extra used to allow apps to request access to the location metadata of the media items selected by the user and returned by `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`.

This is a boolean intent extra which when set to `true` informs the photopicker that the app is requesting location information for the media items selected by the user. The default value for this extra will always be `false` i.e. not sharing the location metadata of the selected media items with the calling app.

**For `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`:** This extra is always required to request location metadata. If excluded, location metadata is redacted by default.

**Note on User Choice:** For `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`, using this intent extra does not guarantee that the calling app will get the location information. The photopicker reserves the right to inform the user of this request via the UI. The user's choice to allow or deny location sharing in the picker UI is **final**.

If location access is ultimately granted, calling apps can extract this metadata when the selected media files are opened using the returned picker URIs.

 Value: "android.provider.extra.REQUEST_LOCATION_METADATA_ACCESS"

### EXTRA_SCREEN_ORIENTATION

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SCREEN_ORIENTATION: String
```

The name of the Intent-extra used to control the orientation of a ViewImage or a MovieView. This is an int property that overrides the activity's requestedOrientation.

 Value: "android.intent.extra.screenOrientation"

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#SCREEN_ORIENTATION_UNSPECIFIED:kotlin.Int`

### EXTRA_SHOW_ACTION_ICONS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SHOW_ACTION_ICONS: String
```

The name of an Intent-extra used to control the UI of a ViewImage. This is a boolean property that specifies whether or not to show action icons.

 Value: "android.intent.extra.showActionIcons"

### EXTRA_SIZE_LIMIT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SIZE_LIMIT: String
```

Specify the maximum allowed size.

 Value: "android.intent.extra.sizeLimit"

### EXTRA_VIDEO_QUALITY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_VIDEO_QUALITY: String
```

The name of the Intent-extra used to control the quality of a recorded video. This is an integer property. Currently value 0 means low quality, suitable for MMS messages, and value 1 means high quality. In the future other quality levels may be added.

 Value: "android.intent.extra.videoQuality"

### INTENT_ACTION_MEDIA_PLAY_FROM_SEARCH

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTENT_ACTION_MEDIA_PLAY_FROM_SEARCH: String
```

An intent to perform a search for music media and automatically play content from the result when possible. This can be fired, for example, by the result of a voice recognition command to listen to music.

This intent always includes the `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_MEDIA_FOCUS:kotlin.String` and `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#QUERY:kotlin.String` extras. The `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_MEDIA_FOCUS:kotlin.String` extra determines the search mode, and the value of the `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#QUERY:kotlin.String` extra depends on the search mode. For more information about the search modes for this intent, see [Play music based on a search query](https://developer.android.com/guide/components/intents-common.html#PlaySearch) in [Common Intents](https://developer.android.com/guide/components/intents-common.html).

This intent makes the most sense for apps that can support large-scale search of music, such as services connected to an online database of music which can be streamed and played on the device.

 Value: "android.media.action.MEDIA_PLAY_FROM_SEARCH"

### INTENT_ACTION_MEDIA_SEARCH

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTENT_ACTION_MEDIA_SEARCH: String
```

Activity Action: Perform a search for media. Contains at least the `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#QUERY:kotlin.String` extra. May also contain any combination of the following extras: EXTRA_MEDIA_ARTIST, EXTRA_MEDIA_ALBUM, EXTRA_MEDIA_TITLE, EXTRA_MEDIA_FOCUS

 Value: "android.intent.action.MEDIA_SEARCH"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_MEDIA_ARTIST:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_MEDIA_ALBUM:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_MEDIA_TITLE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_MEDIA_FOCUS:kotlin.String`

### INTENT_ACTION_MUSIC_PLAYER

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTENT_ACTION_MUSIC_PLAYER: String
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_APP_MUSIC:kotlin.String` instead.*

Activity Action: Launch a music player. The activity should be able to play, browse, or manipulate music files stored on the device.

 Value: "android.intent.action.MUSIC_PLAYER"

### INTENT_ACTION_STILL_IMAGE_CAMERA

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTENT_ACTION_STILL_IMAGE_CAMERA: String
```

The name of the Intent action used to launch a camera in still image mode.

 Value: "android.media.action.STILL_IMAGE_CAMERA"

### INTENT_ACTION_STILL_IMAGE_CAMERA_SECURE

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTENT_ACTION_STILL_IMAGE_CAMERA_SECURE: String
```

The name of the Intent action used to launch a camera in still image mode for use when the device is secured (e.g. with a pin, password, pattern, or face unlock). Applications responding to this intent must not expose any personal content like existing photos or videos on the device. The applications should be careful not to share any photo or video with other applications or internet. The activity should use `https://developer.android.com/reference/kotlin/android/app/Activity.html#setShowWhenLocked(kotlin.Boolean)` to display on top of the lock screen while secured. There is no activity stack when this flag is used, so launching more than one activity is strongly discouraged.

 Value: "android.media.action.STILL_IMAGE_CAMERA_SECURE"

### INTENT_ACTION_TEXT_OPEN_FROM_SEARCH

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTENT_ACTION_TEXT_OPEN_FROM_SEARCH: String
```

An intent to perform a search for readable media and automatically play content from the result when possible. This can be fired, for example, by the result of a voice recognition command to read a book or magazine.

Contains the `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#QUERY:kotlin.String` extra, which is a string that can contain any type of unstructured text search, like the name of a book or magazine, an author a genre, a publisher, or any combination of these.

Because this intent includes an open-ended unstructured search string, it makes the most sense for apps that can support large-scale search of text media, such as services connected to an online database of books and/or magazines which can be read on the device.

 Value: "android.media.action.TEXT_OPEN_FROM_SEARCH"

### INTENT_ACTION_VIDEO_CAMERA

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTENT_ACTION_VIDEO_CAMERA: String
```

The name of the Intent action used to launch a camera in video mode.

 Value: "android.media.action.VIDEO_CAMERA"

### INTENT_ACTION_VIDEO_PLAY_FROM_SEARCH

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTENT_ACTION_VIDEO_PLAY_FROM_SEARCH: String
```

An intent to perform a search for video media and automatically play content from the result when possible. This can be fired, for example, by the result of a voice recognition command to play movies.

Contains the `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#QUERY:kotlin.String` extra, which is a string that can contain any type of unstructured video search, like the name of a movie, one or more actors, a genre, or any combination of these.

Because this intent includes an open-ended unstructured search string, it makes the most sense for apps that can support large-scale search of video, such as services connected to an online database of videos which can be streamed and played on the device.

 Value: "android.media.action.VIDEO_PLAY_FROM_SEARCH"

### KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID: String
```

One of the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` keys for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_ALBUM:kotlin.String` specifying the photopicker album for which the app can request to show highlighted media results in the photopicker. The value of this key should be one of `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_ALBUM_FAVORITES:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_ALBUM_CAMERA:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_ALBUM_VIDEOS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_ALBUM_SCREENSHOTS:kotlin.String` or `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_ALBUM_DOWNLOADS:kotlin.String`. Any other value for this key will result in throwing `IllegalArgumentException`. See: `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_ALBUM:kotlin.String`

 Value: "android.provider.media.key.PICK_IMAGES_HIGHLIGHT_MEDIA_ALBUM_ID"

### KEY_PICK_IMAGES_HIGHLIGHT_SEARCH_TEXT_QUERY

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PICK_IMAGES_HIGHLIGHT_SEARCH_TEXT_QUERY: String
```

One of the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` keys for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_SEARCH_RESULTS:kotlin.String` specifying the input query for which the app can request to show highlighted media results in the photopicker. The photopicker will trigger a search based on this input value to show highlighted media results. The value of this key can be any string value for which the app wants to show highlighted results. In case the input text query is null, `IllegalArgumentException` is thrown. Read more: `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_SEARCH_RESULTS:kotlin.String`

 Value: "android.provider.media.key.PICK_IMAGES_HIGHLIGHT_SEARCH_TEXT_QUERY"

### KEY_PICK_IMAGES_HIGHLIGHT_TYPE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 19](https://developer.android.com/sdkExtensions)

```
static val KEY_PICK_IMAGES_HIGHLIGHT_TYPE: String
```

One of the `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` keys for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_SEARCH_RESULTS:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_ALBUM:kotlin.String` to specify the highlight type i.e. the way the highlighted media results will be shown in the photopicker. The value can be one of `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_TYPE_COLLAPSED:kotlin.Int` to show a highlight media section in the photopicker or `https://developer.android.com/reference/kotlin/android/provider/MediaStore#PICK_IMAGES_HIGHLIGHT_TYPE_EXPANDED:kotlin.Int` to show a highlighted media results grid. Any other value for this key will result in throwing `IllegalArgumentException`. Read more: `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_SEARCH_RESULTS:kotlin.String`

 Value: "android.provider.media.key.PICK_IMAGES_HIGHLIGHT_TYPE"

### MATCH_DEFAULT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_DEFAULT: Int
```

Value indicating that the default matching behavior should be used, as defined by the key documentation.

 Value: 0

### MATCH_EXCLUDE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_EXCLUDE: Int
```

Value indicating that operations should exclude items matching the criteria defined by this key.

 Value: 2

### MATCH_INCLUDE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_INCLUDE: Int
```

Value indicating that operations should include items matching the criteria defined by this key.

Note that items *not* matching the criteria *may* also be included depending on the default behavior documented by the key. If you want to operate exclusively on matching items, use `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MATCH_ONLY:kotlin.Int`.

 Value: 1

### MATCH_ONLY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_ONLY: Int
```

Value indicating that operations should only operate on items explicitly matching the criteria defined by this key.

 Value: 3

### MEDIA_IGNORE_FILENAME

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEDIA_IGNORE_FILENAME: String
```

Name of the file signaling the media scanner to ignore media in the containing directory and its subdirectories. Developers should use this to avoid application graphics showing up in the Gallery and likewise prevent application sounds and music from showing up in the Music app.

 Value: ".nomedia"

### MEDIA_SCANNER_VOLUME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEDIA_SCANNER_VOLUME: String
```

Name of current volume being scanned by the media scanner.

 Value: "volume"

### META_DATA_REVIEW_GALLERY_PREWARM_SERVICE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_DATA_REVIEW_GALLERY_PREWARM_SERVICE: String
```

Name under which an activity handling `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_REVIEW:kotlin.String` or `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_REVIEW_SECURE:kotlin.String` publishes the service name for its prewarm service.

This meta-data should reference the fully qualified class name of the prewarm service

The prewarm service can be bound before starting `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_REVIEW:kotlin.String` or `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_REVIEW_SECURE:kotlin.String`. An application implementing this prewarm service should do the absolute minimum amount of work to initialize its resources to efficiently handle an `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_REVIEW:kotlin.String` or `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_REVIEW_SECURE:kotlin.String` in the near future.

 Value: "android.media.review_gallery_prewarm_service"

### META_DATA_STILL_IMAGE_CAMERA_PREWARM_SERVICE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_DATA_STILL_IMAGE_CAMERA_PREWARM_SERVICE: String
```

Name under which an activity handling `https://developer.android.com/reference/kotlin/android/provider/MediaStore#INTENT_ACTION_STILL_IMAGE_CAMERA:kotlin.String` or `https://developer.android.com/reference/kotlin/android/provider/MediaStore#INTENT_ACTION_STILL_IMAGE_CAMERA_SECURE:kotlin.String` publishes the service name for its prewarm service.

This meta-data should reference the fully qualified class name of the prewarm service extending `CameraPrewarmService`.

The prewarm service will get bound and receive a prewarm signal `CameraPrewarmService#onPrewarm()` when a camera launch intent fire might be imminent. An application implementing a prewarm service should do the absolute minimum amount of work to initialize the camera in order to reduce startup time in likely case that shortly after a camera launch intent would be sent.

 Value: "android.media.still_image_camera_preview_service"

### PICK_IMAGES_HIGHLIGHT_ALBUM_CAMERA

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 19](https://developer.android.com/sdkExtensions)

```
static val PICK_IMAGES_HIGHLIGHT_ALBUM_CAMERA: String
```

One of the possible album highlight values for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID:kotlin.String` in case an app chooses to highlight media results from an album, in this case, the Camera album. Read more: `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_ALBUM:kotlin.String`

 Value: "android.provider.media.PICK_IMAGES_HIGHLIGHT_ALBUM_CAMERA"

### PICK_IMAGES_HIGHLIGHT_ALBUM_DOWNLOADS

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 19](https://developer.android.com/sdkExtensions)

```
static val PICK_IMAGES_HIGHLIGHT_ALBUM_DOWNLOADS: String
```

One of the possible album highlight values for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID:kotlin.String` in case an app chooses to highlight media results from an album, in this case, the Downloads album. Read more: `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_ALBUM:kotlin.String`

 Value: "android.provider.media.PICK_IMAGES_HIGHLIGHT_ALBUM_DOWNLOADS"

### PICK_IMAGES_HIGHLIGHT_ALBUM_FAVORITES

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 19](https://developer.android.com/sdkExtensions)

```
static val PICK_IMAGES_HIGHLIGHT_ALBUM_FAVORITES: String
```

One of the possible album highlight values for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID:kotlin.String` in case an app chooses to highlight media results from an album, in this case, the Favorites album. Read more: `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_ALBUM:kotlin.String`

 Value: "android.provider.media.PICK_IMAGES_HIGHLIGHT_ALBUM_FAVORITES"

### PICK_IMAGES_HIGHLIGHT_ALBUM_SCREENSHOTS

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 19](https://developer.android.com/sdkExtensions)

```
static val PICK_IMAGES_HIGHLIGHT_ALBUM_SCREENSHOTS: String
```

One of the possible album highlight values for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID:kotlin.String` in case an app chooses to highlight media results from from an album, in this case, the Screenshots album. Read more: `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_ALBUM:kotlin.String`

 Value: "android.provider.media.PICK_IMAGES_HIGHLIGHT_ALBUM_SCREENSHOTS"

### PICK_IMAGES_HIGHLIGHT_ALBUM_VIDEOS

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 19](https://developer.android.com/sdkExtensions)

```
static val PICK_IMAGES_HIGHLIGHT_ALBUM_VIDEOS: String
```

One of the possible album highlight values for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID:kotlin.String` in case an app chooses to highlight media results from an album, in this case, the Videos album. Read more: `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_ALBUM:kotlin.String`

 Value: "android.provider.media.PICK_IMAGES_HIGHLIGHT_ALBUM_VIDEOS"

### PICK_IMAGES_HIGHLIGHT_TYPE_COLLAPSED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 19](https://developer.android.com/sdkExtensions)

```
static val PICK_IMAGES_HIGHLIGHT_TYPE_COLLAPSED: Int
```

One of the permitted values for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_TYPE:kotlin.String` to highlight media results as a highlighted media section in the photopicker based on the given input query in `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_SEARCH_TEXT_QUERY:kotlin.String` or the given input photopicker album in MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID}. Read more: `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_SEARCH_RESULTS:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_ALBUM:kotlin.String`

 Value: 0

### PICK_IMAGES_HIGHLIGHT_TYPE_EXPANDED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 19](https://developer.android.com/sdkExtensions)

```
static val PICK_IMAGES_HIGHLIGHT_TYPE_EXPANDED: Int
```

One of the permitted values for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_TYPE:kotlin.String` to show a highlighted media results grid based on the given input query in `https://developer.android.com/reference/kotlin/android/provider/MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_SEARCH_TEXT_QUERY:kotlin.String` or the given input photopicker album in MediaStore#KEY_PICK_IMAGES_HIGHLIGHT_ALBUM_ID}. Read more: `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_SEARCH_RESULTS:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_HIGHLIGHT_ALBUM:kotlin.String`

 Value: 1

### PICK_IMAGES_TAB_ALBUMS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PICK_IMAGES_TAB_ALBUMS: Int
```

One of the permitted values for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_LAUNCH_TAB:kotlin.String` to open the picker with albums tab.

 Value: 0

### PICK_IMAGES_TAB_IMAGES

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PICK_IMAGES_TAB_IMAGES: Int
```

One of the permitted values for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_LAUNCH_TAB:kotlin.String` to open the picker with photos tab.

 Value: 1

### QUERY_ARG_INCLUDE_RECENTLY_UNMOUNTED_VOLUMES

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUERY_ARG_INCLUDE_RECENTLY_UNMOUNTED_VOLUMES: String
```

Flag that requests android.content.ContentResolver#query to include content from recently unmounted volumes.

When the flag is set, android.content.ContentResolver#query will return content from all volumes(i.e., both mounted and recently unmounted volume whose content is still held by MediaProvider).

Note that the query result doesn't provide any hint for content from unmounted volume. It's strongly recommended to use default query to avoid accessing/operating on the content that are not available on the device.

The flag is useful for apps which manage their own database and query MediaStore in order to synchronize between MediaStore database and their own database.

 Value: "android:query-arg-recently-unmounted-volumes"

### QUERY_ARG_LATEST_SELECTION_ONLY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 12](https://developer.android.com/sdkExtensions)

```
static val QUERY_ARG_LATEST_SELECTION_ONLY: String
```

Flag that indicates if only the latest selection in the photoPicker for the calling app should be returned. If set to true, all items that were granted to the calling app in the last selection are returned.

Selection in this scenario refers to when the user selects items in **the permission prompt photo picker**. The access for these items is granted to the calling app and these grants are persisted unless the user deselects a granted item explicitly.

The result excludes items owned by the calling app unless they are explicitly selected by the user.

Note: If there has been no user selections after the introduction of this feature then all the granted items will be returned.

This key can be placed in a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` of extras and passed to android.content.ContentResolver#query.

 Value: "android:query-arg-latest-selection-only"

**See Also**

- `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_MEDIA_VISUAL_USER_SELECTED:kotlin.String`

### QUERY_ARG_MATCH_FAVORITE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUERY_ARG_MATCH_FAVORITE: String
```

Specify how `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_FAVORITE:kotlin.String` items should be filtered when performing a `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` operation.

This key can be placed in a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` of extras and passed to android.content.ContentResolver#query, android.content.ContentResolver#update, or android.content.ContentResolver#delete.

By default, favorite items are *not* filtered away from operations. 
Value is either `0` or a combination of the following:

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MATCH_DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MATCH_INCLUDE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MATCH_EXCLUDE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MATCH_ONLY:kotlin.Int`

 Value: "android:query-arg-match-favorite"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_FAVORITE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#QUERY_ARG_MATCH_FAVORITE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#createFavoriteRequest(android.content.ContentResolver,%20kotlin.collections.MutableCollection,%20kotlin.Boolean)`

### QUERY_ARG_MATCH_PENDING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUERY_ARG_MATCH_PENDING: String
```

Specify how `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_PENDING:kotlin.String` items should be filtered when performing a `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` operation.

This key can be placed in a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` of extras and passed to android.content.ContentResolver#query, android.content.ContentResolver#update, or android.content.ContentResolver#delete.

By default, pending items are filtered away from operations. 
Value is either `0` or a combination of the following:

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MATCH_DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MATCH_INCLUDE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MATCH_EXCLUDE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MATCH_ONLY:kotlin.Int`

 Value: "android:query-arg-match-pending"

### QUERY_ARG_MATCH_TRASHED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUERY_ARG_MATCH_TRASHED: String
```

Specify how `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_TRASHED:kotlin.String` items should be filtered when performing a `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` operation.

This key can be placed in a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` of extras and passed to android.content.ContentResolver#query, android.content.ContentResolver#update, or android.content.ContentResolver#delete.

By default, trashed items are filtered away from operations. 
Value is either `0` or a combination of the following:

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MATCH_DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MATCH_INCLUDE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MATCH_EXCLUDE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#MATCH_ONLY:kotlin.Int`

 Value: "android:query-arg-match-trashed"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_TRASHED:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#QUERY_ARG_MATCH_TRASHED:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#createTrashRequest(android.content.ContentResolver,%20kotlin.collections.MutableCollection,%20kotlin.Boolean)`

### QUERY_ARG_MEDIA_STANDARD_SORT_ORDER

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 15](https://developer.android.com/sdkExtensions)

```
static val QUERY_ARG_MEDIA_STANDARD_SORT_ORDER: String
```

Flag that requests android.content.ContentResolver#query to sort the result in descending order based on `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#INFERRED_DATE:kotlin.String`.

When this flag is used as an extra in a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` passed to android.content.ContentResolver#query, all other sorting options such as `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#QUERY_ARG_SORT_COLUMNS:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#QUERY_ARG_SQL_SORT_ORDER:kotlin.String` are disregarded.

 Value: "android:query-arg-media-standard-sort-order"

### QUERY_ARG_RELATED_URI

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUERY_ARG_RELATED_URI: String
```

Specify a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` that is "related" to the current operation being performed.

This is typically used to allow an operation that may normally be rejected, such as making a copy of a pre-existing image located under a `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#RELATIVE_PATH:kotlin.String` where new images are not allowed.

It's strongly recommended that when making a copy of pre-existing content that you define the "original document ID" GUID as defined by the *XMP Media Management* standard.

This key can be placed in a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` of extras and passed to android.content.ContentResolver#insert.

 Value: "android:query-arg-related-uri"

### UNKNOWN_STRING

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNKNOWN_STRING: String
```

The string that is used when a media attribute is not known. For example, if an audio file does not have any meta data, the artist and album columns will be set to this value.

 Value: "<unknown>"

### VOLUME_EXTERNAL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VOLUME_EXTERNAL: String
```

Synthetic volume name that provides a view of all content across the "external" storage of the device.

This synthetic volume provides a merged view of all media across all currently attached external storage devices.

Because this is a synthetic volume, you can't insert new content into this volume. Instead, you can insert content into a specific storage volume obtained from `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getExternalVolumeNames(android.content.Context)`.

 Value: "external"

### VOLUME_EXTERNAL_PRIMARY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VOLUME_EXTERNAL_PRIMARY: String
```

Specific volume name that represents the primary external storage device at `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageDirectory()`.

This volume may not always be available, such as when the user has ejected the device. You can find a list of all specific volume names using `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getExternalVolumeNames(android.content.Context)`.

 Value: "external_primary"

### VOLUME_INTERNAL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VOLUME_INTERNAL: String
```

Synthetic volume name that provides a view of all content across the "internal" storage of the device.

This synthetic volume provides a merged view of all media distributed with the device, such as built-in ringtones and wallpapers.

Because this is a synthetic volume, you can't insert new content into this volume.

 Value: "internal"

## Public constructors

### MediaStore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MediaStore()
```

## Public methods

### canManageMedia

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun canManageMedia(context: Context): Boolean
```

Returns whether the calling app is granted `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_MEDIA:kotlin.String` or not.

Declaring the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_MEDIA:kotlin.String` isn't enough to gain the access.

To request access, use `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_REQUEST_MANAGE_MEDIA:kotlin.String`.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): the request context. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true, the calling app is granted the permission. Otherwise, false |

**See Also**

- `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_MEDIA:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/Settings#ACTION_REQUEST_MANAGE_MEDIA:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#createDeleteRequest(android.content.ContentResolver,%20kotlin.collections.MutableCollection)`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#createTrashRequest(android.content.ContentResolver,%20kotlin.collections.MutableCollection,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#createWriteRequest(android.content.ContentResolver,%20kotlin.collections.MutableCollection)`

### createDeleteRequest

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createDeleteRequest(
    resolver: ContentResolver, 
    uris: MutableCollection<Uri!>
): PendingIntent
```

Create a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` that will prompt the user to permanently delete the requested media items. When the user approves this request, android.content.ContentResolver#delete will be called on these items.

This call only generates the request for a prompt; to display the prompt, call android.app.Activity#startIntentSenderForResult with `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#getIntentSender()`. You can then determine if the user granted your request by testing for `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` in android.app.Activity#onActivityResult. The requested operation will have completely finished before this activity result is delivered.

The displayed prompt will reflect all the media items you're requesting, including those for which you already hold write access. If you want to determine if you already hold write access before requesting access, use `https://developer.android.com/reference/kotlin/android/content/Context.html#checkUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` with `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int`.

Note: if your app targets `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int` and above, you can send a maximum of 2000 uris in each request. Attempting to send more than 2000 uris will result in a `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): Used to connect with `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String`. Typically this value is `https://developer.android.com/reference/kotlin/android/content/Context.html#getContentResolver()`, but if you need more explicit lifecycle controls, you can obtain a `https://developer.android.com/reference/kotlin/android/content/ContentProviderClient.html#` and wrap it using `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#wrap(android.content.ContentProviderClient)`. This value cannot be `null`. |
| `uris` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>: The set of media items to include in this request. Each item must be hosted by `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String` and must reference a specific media item by `https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String`. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` | This value cannot be `null`. |

### createFavoriteRequest

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createFavoriteRequest(
    resolver: ContentResolver, 
    uris: MutableCollection<Uri!>, 
    value: Boolean
): PendingIntent
```

Create a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` that will prompt the user to favorite the requested media items. When the user approves this request, `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_FAVORITE:kotlin.String` is set on these items.

This call only generates the request for a prompt; to display the prompt, call android.app.Activity#startIntentSenderForResult with `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#getIntentSender()`. You can then determine if the user granted your request by testing for `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` in android.app.Activity#onActivityResult. The requested operation will have completely finished before this activity result is delivered.

The displayed prompt will reflect all the media items you're requesting, including those for which you already hold write access. If you want to determine if you already hold write access before requesting access, use `https://developer.android.com/reference/kotlin/android/content/Context.html#checkUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` with `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int`.

Note: if your app targets `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int` and above, you can send a maximum of 2000 uris in each request. Attempting to send more than 2000 uris will result in a `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): Used to connect with `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String`. Typically this value is `https://developer.android.com/reference/kotlin/android/content/Context.html#getContentResolver()`, but if you need more explicit lifecycle controls, you can obtain a `https://developer.android.com/reference/kotlin/android/content/ContentProviderClient.html#` and wrap it using `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#wrap(android.content.ContentProviderClient)`. This value cannot be `null`. |
| `uris` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>: The set of media items to include in this request. Each item must be hosted by `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String` and must reference a specific media item by `https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String`. This value cannot be `null`. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_FAVORITE:kotlin.String` value to apply. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_FAVORITE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#QUERY_ARG_MATCH_FAVORITE:kotlin.String`

### createTrashRequest

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createTrashRequest(
    resolver: ContentResolver, 
    uris: MutableCollection<Uri!>, 
    value: Boolean
): PendingIntent
```

Create a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` that will prompt the user to trash the requested media items. When the user approves this request, `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_TRASHED:kotlin.String` is set on these items.

This call only generates the request for a prompt; to display the prompt, call android.app.Activity#startIntentSenderForResult with `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#getIntentSender()`. You can then determine if the user granted your request by testing for `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` in android.app.Activity#onActivityResult. The requested operation will have completely finished before this activity result is delivered.

The displayed prompt will reflect all the media items you're requesting, including those for which you already hold write access. If you want to determine if you already hold write access before requesting access, use `https://developer.android.com/reference/kotlin/android/content/Context.html#checkUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` with `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int`.

Note: if your app targets `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int` and above, you can send a maximum of 2000 uris in each request. Attempting to send more than 2000 uris will result in a `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): Used to connect with `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String`. Typically this value is `https://developer.android.com/reference/kotlin/android/content/Context.html#getContentResolver()`, but if you need more explicit lifecycle controls, you can obtain a `https://developer.android.com/reference/kotlin/android/content/ContentProviderClient.html#` and wrap it using `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#wrap(android.content.ContentProviderClient)`. This value cannot be `null`. |
| `uris` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>: The set of media items to include in this request. Each item must be hosted by `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String` and must reference a specific media item by `https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String`. This value cannot be `null`. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_TRASHED:kotlin.String` value to apply. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_TRASHED:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#QUERY_ARG_MATCH_TRASHED:kotlin.String`

### createWriteRequest

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createWriteRequest(
    resolver: ContentResolver, 
    uris: MutableCollection<Uri!>
): PendingIntent
```

Create a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` that will prompt the user to grant your app write access for the requested media items.

This call only generates the request for a prompt; to display the prompt, call android.app.Activity#startIntentSenderForResult with `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#getIntentSender()`. You can then determine if the user granted your request by testing for `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` in android.app.Activity#onActivityResult. The requested operation will have completely finished before this activity result is delivered.

Permissions granted through this mechanism are tied to the lifecycle of the `https://developer.android.com/reference/kotlin/android/app/Activity.html#` that requests them. If you need to retain longer-term access for background actions, you can place items into a `https://developer.android.com/reference/kotlin/android/content/ClipData.html#` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#` which can then be passed to `https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)` or `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder.html#setClipData(android.content.ClipData,%20kotlin.Int)`. Be sure to include any relevant access modes you want to retain, such as `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int`.

The displayed prompt will reflect all the media items you're requesting, including those for which you already hold write access. If you want to determine if you already hold write access before requesting access, use `https://developer.android.com/reference/kotlin/android/content/Context.html#checkUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` with `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int`.

For security and performance reasons this method does not support `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_PERSISTABLE_URI_PERMISSION:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_PREFIX_URI_PERMISSION:kotlin.Int`.

The write access granted through this request is general-purpose, and once obtained you can directly android.content.ContentResolver#update columns like `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_FAVORITE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_TRASHED:kotlin.String`, or android.content.ContentResolver#delete.

Note: if your app targets `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int` and above, you can send a maximum of 2000 uris in each request. Attempting to send more than 2000 uris will result in a `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): Used to connect with `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String`. Typically this value is `https://developer.android.com/reference/kotlin/android/content/Context.html#getContentResolver()`, but if you need more explicit lifecycle controls, you can obtain a `https://developer.android.com/reference/kotlin/android/content/ContentProviderClient.html#` and wrap it using `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#wrap(android.content.ContentProviderClient)`. This value cannot be `null`. |
| `uris` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>: The set of media items to include in this request. Each item must be hosted by `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String` and must reference a specific media item by `https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String`. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` | This value cannot be `null`. |

### getDocumentUri

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDocumentUri(
    context: Context, 
    mediaUri: Uri
): Uri?
```

Return a `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` Uri that is an equivalent to the given `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` Uri.

This allows apps with Storage Access Framework permissions to convert between `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` and `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` Uris that refer to the same underlying item. Note that this method doesn't grant any new permissions; callers must already hold permissions obtained with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT:kotlin.String` or related APIs.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |
| `mediaUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): The `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` Uri to convert. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | An equivalent `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` Uri. Returns `null` if no equivalent was found. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getMediaUri(android.content.Context,%20android.net.Uri)`

### getExternalVolumeNames

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getExternalVolumeNames(context: Context): MutableSet<String!>
```

Return list of all specific volume names that make up `https://developer.android.com/reference/kotlin/android/provider/MediaStore#VOLUME_EXTERNAL:kotlin.String`. This includes a unique volume name for each shared storage device that is currently attached, which typically includes `https://developer.android.com/reference/kotlin/android/provider/MediaStore#VOLUME_EXTERNAL_PRIMARY:kotlin.String`.

Each specific volume name can be passed to APIs like `https://developer.android.com/reference/kotlin/android/provider/MediaStore.Images.Media#getContentUri(kotlin.String)` to interact with media on that storage device.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

### getGeneration

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 1](https://developer.android.com/sdkExtensions)

```
static fun getGeneration(
    context: Context, 
    volumeName: String
): Long
```

Return the latest generation value for the given volume.

Generation numbers are useful for apps that are attempting to quickly identify exactly which media items have been added or changed since a previous point in time. Generation numbers are monotonically increasing over time, and can be safely arithmetically compared.

Detecting media changes using generation numbers is more robust than using `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DATE_ADDED:kotlin.String` or `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#DATE_MODIFIED:kotlin.String`, since those values may change in unexpected ways when apps use `https://developer.android.com/reference/kotlin/java/io/File.html#setLastModified(kotlin.Long)` or when the system clock is set incorrectly.

Note that before comparing these detailed generation values, you should first confirm that the overall version hasn't changed by checking `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getVersion(android.content.Context,%20kotlin.String)`, since that indicates when a more radical change has occurred. If the overall version changes, you should assume that generation numbers have been reset and perform a full synchronization pass.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |
| `volumeName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): specific volume to obtain an generation value for. Must be one of the values returned from `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getExternalVolumeNames(android.content.Context)`. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#GENERATION_ADDED:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#GENERATION_MODIFIED:kotlin.String`

### getMediaScannerUri

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getMediaScannerUri(): Uri!
```

Uri for querying the state of the media scanner.

### getMediaUri

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getMediaUri(
    context: Context, 
    documentUri: Uri
): Uri?
```

Return a `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` Uri that is an equivalent to the given `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` Uri. This only supports `ExternalStorageProvider` and `MediaDocumentsProvider` Uris.

This allows apps with Storage Access Framework permissions to convert between `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` and `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` Uris that refer to the same underlying item. Note that this method doesn't grant any new permissions, but it grants the same access to the Media Store Uri as the caller has to the given DocumentsProvider Uri; callers must already hold permissions for documentUri obtained with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_OPEN_DOCUMENT:kotlin.String` or related APIs.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |
| `documentUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): The `https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider` Uri to convert. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | An equivalent `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` Uri. Returns `null` if no equivalent was found. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getDocumentUri(android.content.Context,%20android.net.Uri)`

### getOriginalMediaFormatFileDescriptor

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getOriginalMediaFormatFileDescriptor(
    context: Context, 
    fileDescriptor: ParcelFileDescriptor
): ParcelFileDescriptor
```

Returns `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` representing the original media file format for `fileDescriptor`.

Media files may get transcoded based on an application's media capabilities requirements. However, in various cases, when the application needs access to the original media file, or doesn't attempt to parse the actual byte contents of media files, such as playback using `https://developer.android.com/reference/kotlin/android/media/MediaPlayer.html#` or for off-device backup, this method can be useful.

This method is applicable only for media files managed by `https://developer.android.com/reference/kotlin/android/provider/MediaStore#`.

The method returns the original file descriptor with the same permission that the caller has for the input file descriptor.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |
| `fileDescriptor` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if the given `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` could not be converted |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_ACCEPT_ORIGINAL_MEDIA_FORMAT:kotlin.String`

### getPackageForSearchMediaService

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 22](https://developer.android.com/sdkExtensions)

```
static fun getPackageForSearchMediaService(resolver: ContentResolver): String
```

Gets the package name of the `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` that client apps use to connect. If the package name is an empty string, it indicates that search service is not supported or there are no valid implementations of the service.

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getPickImagesMaxLimit

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 2](https://developer.android.com/sdkExtensions)

```
static fun getPickImagesMaxLimit(): Int
```

The maximum limit for the number of items that can be selected using `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String` when launched in multiple selection mode. This can be used as a constant value for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#EXTRA_PICK_IMAGES_MAX:kotlin.String`.

### getRecentExternalVolumeNames

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getRecentExternalVolumeNames(context: Context): MutableSet<String!>
```

Return list of all recent volume names that have been part of `https://developer.android.com/reference/kotlin/android/provider/MediaStore#VOLUME_EXTERNAL:kotlin.String`.

These volume names are not currently mounted, but they're likely to reappear in the future, so apps are encouraged to preserve any indexed metadata related to these volumes to optimize user experiences.

Each specific volume name can be passed to APIs like `https://developer.android.com/reference/kotlin/android/provider/MediaStore.Images.Media#getContentUri(kotlin.String)` to interact with media on that storage device.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

### getRedactedUri

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getRedactedUri(
    resolver: ContentResolver, 
    uri: Uri
): Uri?
```

Returns an EXIF redacted version of `uri` i.e. a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` with metadata such as location, GPS datestamp etc. redacted from the EXIF headers.

A redacted Uri can be used to share a file with another application wherein exposing sensitive information in EXIF headers is not desirable. Note: 1. Redacted uris cannot be granted write access and can neither be used to perform any kind of write operations. 2. To get a redacted uri the caller must hold read permission to `uri`.

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): The `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#` used to connect with `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String`. Typically this value is gotten from `https://developer.android.com/reference/kotlin/android/content/Context.html#getContentResolver()` This value cannot be `null`. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): the `https://developer.android.com/reference/kotlin/android/net/Uri.html#` Uri to convert. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | redacted version of the `uri`. Returns `null` when the given `https://developer.android.com/reference/kotlin/android/net/Uri.html#` could not be found or is unsupported |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller doesn't have the read access to `uri` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getRedactedUri(android.content.ContentResolver,%20kotlin.collections.MutableList)`

### getRedactedUri

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getRedactedUri(
    resolver: ContentResolver, 
    uris: MutableList<Uri!>
): MutableList<Uri!>
```

Returns a list of EXIF redacted version of `uris` i.e. a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` with metadata such as location, GPS datestamp etc. redacted from the EXIF headers.

A redacted Uri can be used to share a file with another application wherein exposing sensitive information in EXIF headers is not desirable. Note: 1. Order of the returned uris follow the order of the `uris`. 2. Redacted uris cannot be granted write access and can neither be used to perform any kind of write operations. 3. To get a redacted uri the caller must hold read permission to its corresponding uri.

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): The `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#` used to connect with `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String`. Typically this value is gotten from `https://developer.android.com/reference/kotlin/android/content/Context.html#getContentResolver()` This value cannot be `null`. |
| `uris` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>: the list of `https://developer.android.com/reference/kotlin/android/net/Uri.html#` Uri to convert. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>` | a list with redacted version of `uris`, in the same order. Returns `null` when the corresponding `https://developer.android.com/reference/kotlin/android/net/Uri.html#` could not be found or is unsupported |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if all the uris in `uris` don't belong to same user id |
| `java.lang.SecurityException` | if the caller doesn't have the read access to all the elements in `uris` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getRedactedUri(android.content.ContentResolver,%20android.net.Uri)`

### getRequireOriginal

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getRequireOriginal(uri: Uri): Boolean
```

Return if the caller requires the original file contents when calling `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFileDescriptor(android.net.Uri,%20kotlin.String)`.

| Parameters ||
|---|---|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#setRequireOriginal(android.net.Uri)`

### getVersion

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getVersion(context: Context): String
```

Return an opaque version string describing the `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` state.

Applications that import data from `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` into their own caches can use this to detect that `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` has undergone substantial changes, and that data should be rescanned.

No other assumptions should be made about the meaning of the version. It can return null if external primary volume is not mounted. Apps should check for volume to be present in `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getExternalVolumeNames(android.content.Context)` before using this API.

This method returns the version for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#VOLUME_EXTERNAL_PRIMARY:kotlin.String`; to obtain a version for a different volume, use `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getVersion(android.content.Context,%20kotlin.String)`.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |

### getVersion

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getVersion(
    context: Context, 
    volumeName: String
): String
```

Return an opaque version string describing the `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` state.

Applications that import data from `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` into their own caches can use this to detect that `https://developer.android.com/reference/kotlin/android/provider/MediaStore#` has undergone substantial changes, and that data should be rescanned.

No other assumptions should be made about the meaning of the version. It can return null if requested volume is not mounted. Apps should check for volume to be present in `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getExternalVolumeNames(android.content.Context)` before using this API.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |
| `volumeName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): specific volume to obtain an opaque version string for. Must be one of the values returned from `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getExternalVolumeNames(android.content.Context)`. This value cannot be `null`. |

### getVolumeName

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getVolumeName(uri: Uri): String
```

Return the volume name that the given `https://developer.android.com/reference/kotlin/android/net/Uri.html#` references.

| Parameters ||
|---|---|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### isCurrentCloudMediaProviderAuthority

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
static fun isCurrentCloudMediaProviderAuthority(
    resolver: ContentResolver, 
    authority: String
): Boolean
```

Returns `true` if and only if the caller with `authority` is the currently enabled `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider`. More specifically, `false` is also returned if the calling uid doesn't match the uid of the `authority`.

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): This value cannot be `null`. |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#isSupportedCloudMediaProviderAuthority(android.content.ContentResolver,%20kotlin.String)`

### isCurrentSystemGallery

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isCurrentSystemGallery(
    resolver: ContentResolver, 
    uid: Int, 
    packageName: String
): Boolean
```

Returns true if the given application is the current system gallery of the device.

The system gallery is one app chosen by the OEM that has read \& write access to all photos and videos on the device and control over folders in media collections.

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): The `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#` used to connect with `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String`. Typically this value is `https://developer.android.com/reference/kotlin/android/content/Context.html#getContentResolver()`. This value cannot be `null`. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The uid to be checked if it is the current system gallery. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package name to be checked if it is the current system gallery. This value cannot be `null`. |

### isSupportedCloudMediaProviderAuthority

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
static fun isSupportedCloudMediaProviderAuthority(
    resolver: ContentResolver, 
    authority: String
): Boolean
```

Returns `true` if and only if the caller with `authority` is a supported `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider`. More specifically, `false` is also returned if the calling uid doesn't match the uid of the `authority`.

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): This value cannot be `null`. |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider`
- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#isCurrentCloudMediaProviderAuthority(android.content.ContentResolver,%20kotlin.String)`

### markIsFavoriteStatus

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 16](https://developer.android.com/sdkExtensions)

```
static fun markIsFavoriteStatus(
    resolver: ContentResolver, 
    uris: MutableCollection<Uri!>, 
    areFavorites: Boolean
): Unit
```

Sets the media isFavorite status if the calling app has wider read permission on media files for given type. Calling app should have one of READ_EXTERNAL_STORAGE or WRITE_EXTERNAL_STORAGE if target sdk \<= T. For target sdk \> T, it should have READ_MEDIA_IMAGES for images, READ_MEDIA_VIDEOS for videos or READ_MEDIA_AUDIO for audio files or MANAGE_EXTERNAL_STORAGE permission.

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): used to connect with `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String` This value cannot be `null`. |
| `uris` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>: a collection of media items to include in this request. Each item must be hosted by `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String` and must reference a specific media item by `https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String` sample uri - content://media/external_primary/images/media/24. This value cannot be `null`. |
| `areFavorites` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_FAVORITE:kotlin.String` value to apply. |

### notifyCloudMediaChangedEvent

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 3](https://developer.android.com/sdkExtensions)

```
static fun notifyCloudMediaChangedEvent(
    resolver: ContentResolver, 
    authority: String, 
    currentMediaCollectionId: String
): Unit
```

Notifies the OS about a cloud media event requiring a full or incremental media collection sync for the currently enabled cloud provider, `authority`. The OS will schedule the sync in the background and will attempt to batch frequent notifications into a single sync event. If the caller is not the currently enabled cloud provider as returned by `https://developer.android.com/reference/kotlin/android/provider/MediaStore#isCurrentCloudMediaProviderAuthority(android.content.ContentResolver,%20kotlin.String)`, the request will be unsuccessful.

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): This value cannot be `null`. |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `currentMediaCollectionId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the request was unsuccessful. |

### openAssetFileDescriptor

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 15](https://developer.android.com/sdkExtensions)

```
static fun openAssetFileDescriptor(
    resolver: ContentResolver, 
    uri: Uri, 
    mode: String, 
    cancellationSignal: CancellationSignal?
): AssetFileDescriptor?
```

Works exactly the same as `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal)`, but only works for `https://developer.android.com/reference/kotlin/android/net/Uri.html#` whose scheme is `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_CONTENT:kotlin.String` and its authority is `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String`.

This API is preferred over `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal)` when opening media Uri for ensuring system stability especially when opening URIs returned as a result of using `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): The `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#` used to connect with `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String`. Typically this value is gotten from `https://developer.android.com/reference/kotlin/android/content/Context.html#getContentResolver()` This value cannot be `null`. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): The desired URI to open. This value cannot be `null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The string representation of the file mode. Can be "r", "w", "wt", "wa", "rw" or "rwt". Please note the exact implementation of these may differ for each Provider implementation - for example, "w" may or may not truncate. This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#?` | a new ParcelFileDescriptor pointing to the file or `null` if the provider recently crashed. You own this descriptor and are responsible for closing it when done. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | if no file exists under the URI. |
| `java.lang.IllegalArgumentException` | if The URI is not for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String` |

### openFileDescriptor

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 15](https://developer.android.com/sdkExtensions)

```
static fun openFileDescriptor(
    resolver: ContentResolver, 
    uri: Uri, 
    mode: String, 
    cancellationSignal: CancellationSignal?
): ParcelFileDescriptor?
```

Works exactly the same as `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal)`, but only works for `https://developer.android.com/reference/kotlin/android/net/Uri.html#` whose scheme is `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_CONTENT:kotlin.String` and its authority is `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String`.

This API is preferred over `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal)` when opening media Uri for ensuring system stability especially when opening URIs returned as a result of using `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): The `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#` used to connect with `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String`. Typically this value is gotten from `https://developer.android.com/reference/kotlin/android/content/Context.html#getContentResolver()` This value cannot be `null`. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): The desired URI to open. This value cannot be `null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The string representation of the file mode. Can be "r", "w", "wt", "wa", "rw" or "rwt". Please note the exact implementation of these may differ for each Provider implementation - for example, "w" may or may not truncate. This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: A signal to cancel the operation in progress, or null if none. If the operation is canceled, then `https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#` will be thrown. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#?` | a new ParcelFileDescriptor pointing to the file or `null` if the provider recently crashed. You own this descriptor and are responsible for closing it when done. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | if no file exists under the URI. |
| `java.lang.IllegalArgumentException` | if The URI is not for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String` |

### openTypedAssetFileDescriptor

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [R Extensions 15](https://developer.android.com/sdkExtensions)

```
static fun openTypedAssetFileDescriptor(
    resolver: ContentResolver, 
    uri: Uri, 
    mimeType: String, 
    opts: Bundle?, 
    cancellationSignal: CancellationSignal?
): AssetFileDescriptor?
```

Works exactly the same as `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openTypedAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)`, but only works for `https://developer.android.com/reference/kotlin/android/net/Uri.html#` whose scheme is `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_CONTENT:kotlin.String` and its authority is `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String`.

This API is preferred over `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openTypedAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)` when opening media Uri for ensuring system stability especially when opening URIs returned as a result of using `https://developer.android.com/reference/kotlin/android/provider/MediaStore#ACTION_PICK_IMAGES:kotlin.String`

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): The `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#` used to connect with `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String`. Typically this value is gotten from `https://developer.android.com/reference/kotlin/android/content/Context.html#getContentResolver()` This value cannot be `null`. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): The desired URI to open. This value cannot be `null`. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The desired MIME type of the returned data. This can be a pattern such as \*/\*, which will allow the content provider to select a type, though there is no way for you to determine what type it is returning. This value cannot be `null`. |
| `opts` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: Additional provider-dependent options. This value may be `null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#?` | a new ParcelFileDescriptor from which you can read the data stream from the provider or `null` if the provider recently crashed. Note that this may be a pipe, meaning you can't seek in it. The only seek you should do is if the AssetFileDescriptor contains an offset, to move to that offset before reading. You own this descriptor and are responsible for closing it when done. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | if no data of the desired type exists under the URI. |
| `java.lang.IllegalArgumentException` | if The URI is not for `https://developer.android.com/reference/kotlin/android/provider/MediaStore#AUTHORITY:kotlin.String` |

### queryDeletedFiles

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 23](https://developer.android.com/sdkExtensions)

```
static fun queryDeletedFiles(
    resolver: ContentResolver, 
    queryArgs: Bundle?, 
    signal: CancellationSignal?
): Cursor?
```

Returns a cursor of deleted items matching the given query arguments.

**Note:** This method only returns deleted items for external volumes. Items deleted from the internal volume are not tracked or returned by this API.

**Note:** If an external volume (such as an SD card) is removed from the device, its associated deleted items are no longer tracked or returned by this API.

The returned cursor includes columns such as `https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/MediaStore.DeletedFiles.DeletedFilesColumns#MEDIA_TYPE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/MediaStore.DeletedFiles.DeletedFilesColumns#DELETED_GENERATION:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/provider/MediaStore.DeletedFiles.DeletedFilesColumns#VOLUME_NAME:kotlin.String`.

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): The ContentResolver to use for the call. This value cannot be `null`. |
| `queryArgs` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: Arguments for the query. Supported arguments include `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#QUERY_ARG_SQL_SELECTION:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#QUERY_ARG_SQL_SELECTION_ARGS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#QUERY_ARG_SQL_SORT_ORDER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#QUERY_ARG_LIMIT:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#QUERY_ARG_OFFSET:kotlin.String`. The selection and sort order can filter and sort on any of the columns defined in `https://developer.android.com/reference/kotlin/android/provider/MediaStore.DeletedFiles.DeletedFilesColumns`. This value may be `null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: A cancellation signal to cancel the operation in progress. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/Cursor.html#?` | A cursor of deleted items, or null if the operation failed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore.DeletedFiles.DeletedFilesColumns`

### restoreFileFromTrash

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 22](https://developer.android.com/sdkExtensions)

```
static fun restoreFileFromTrash(
    resolver: ContentResolver, 
    path: String, 
    targetPath: String?
): String
```

Restores a file or directory from a trashed state.

The item will be restored from the system's trash to its original location by default. If the original parent directories do not exist, they will be created as part of the restoration process. Optionally, a new `targetPath` can be specified to restore the item to a different location. If the specified `path` refers to a trashed directory, all its trashed contents will also be restored. If restoring a file would create a name conflict with an existing file, the system resolves this by appending a numerical suffix. For example, if `image.jpeg` exists, the restored file will be named `image (1).jpeg`.

Apps using this API must declare the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` permission in their manifest and be granted it by the user.

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): The `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#` to use for the call. This value cannot be `null`. |
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The absolute path of the trashed file or directory to be restored. This path should be the path of the item as it exists in the trash. This value cannot be `null`. |
| `targetPath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: An optional absolute path where the item should be restored. If `null`, the item will be restored to its original location prior to being trashed. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The absolute path of the item after it has been restored. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the provided `path` is null or empty, or if the `targetPath` (if provided) is invalid. |
| `java.lang.IllegalStateException` | If the restoration operation fails due to an unexpected internal system error, such as the system being unable to restore the file |
| `java.lang.SecurityException` | if the caller lacks the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` permission. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#trashFile(android.content.ContentResolver,%20kotlin.String)`

### setIncludePending

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setIncludePending(uri: Uri): Uri
```

**Deprecated:** *consider migrating to `https://developer.android.com/reference/kotlin/android/provider/MediaStore#QUERY_ARG_MATCH_PENDING:kotlin.String` which is more expressive.*

Update the given `https://developer.android.com/reference/kotlin/android/net/Uri.html#` to also include any pending media items from calls such as `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)`. By default no pending items are returned.

| Parameters ||
|---|---|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns#IS_PENDING:kotlin.String`

### setRequireOriginal

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setRequireOriginal(uri: Uri): Uri
```

Update the given `https://developer.android.com/reference/kotlin/android/net/Uri.html#` to indicate that the caller requires the original file contents when calling `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openFileDescriptor(android.net.Uri,%20kotlin.String)`.

This can be useful when the caller wants to ensure they're backing up the exact bytes of the underlying media, without any Exif redaction being performed.

If the original file contents cannot be provided, a `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#` will be thrown when the returned `https://developer.android.com/reference/kotlin/android/net/Uri.html#` is used, such as when the caller doesn't hold `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_MEDIA_LOCATION:kotlin.String`.

| Parameters ||
|---|---|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#getRequireOriginal(android.net.Uri)`

### trashFile

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 22](https://developer.android.com/sdkExtensions)

```
static fun trashFile(
    resolver: ContentResolver, 
    path: String
): String
```

Moves a file or directory to a trashed state.

If the specified `path` is a directory, all its contents (files and subdirectories) will also be trashed recursively.

Apps using this API must declare the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` permission in their manifest and be granted it by the user.

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#): The `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#` to use for the call. This value cannot be `null`. |
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The absolute path of the file or directory to be trashed. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The path of the item that was trashed, which may differ from the input path if the system modifies it for trash management. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the file path is null or empty. |
| `java.lang.IllegalStateException` | if the trash directory cannot be created or if the file cannot be trashed. |
| `java.lang.SecurityException` | if the caller lacks the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` permission. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/MediaStore#restoreFileFromTrash(android.content.ContentResolver,%20kotlin.String,%20kotlin.String)`

## Properties

### AUTHORITY_URI

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHORITY_URI: Uri
```

A content:// style uri to the authority for the media provider
