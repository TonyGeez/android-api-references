# MediaRouter2.DeviceSuggestionsUpdatesCallback

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeviceSuggestionsUpdatesCallback

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback "View this page in Java") 
| --- | --- |

```
interface DeviceSuggestionsUpdatesCallback
```

| [android.media.MediaRouter2.DeviceSuggestionsUpdatesCallback](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback#) |

Callback for receiving events about device suggestions

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuggestionsCleared](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback#onSuggestionsCleared(kotlin.String))`(`suggestingPackageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Called when suggestions are cleared. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuggestionsRequested](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback#onSuggestionsRequested())`()` Called when a router requests a suggestion from suggestion providers. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuggestionsUpdated](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback#onSuggestionsUpdated(kotlin.String,%20kotlin.collections.MutableList))`(`suggestingPackageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `suggestedDeviceInfo:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [SuggestedDeviceInfo](https://developer.android.com/reference/kotlin/android/media/SuggestedDeviceInfo)!>`)` Called when suggestions are updated. |
| --- | --- |

## Public methods

### onSuggestionsCleared

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSuggestionsCleared(suggestingPackageName: String): Unit
```

Called when suggestions are cleared.

| Parameters ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `suggestingPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the package that cleared their provided suggestions. This value cannot be`null`. |

### onSuggestionsRequested

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSuggestionsRequested(): Unit
```

Called when a router requests a suggestion from suggestion providers. 

### onSuggestionsUpdated

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSuggestionsUpdated(
    suggestingPackageName: String, 
    suggestedDeviceInfo: MutableList<SuggestedDeviceInfo!>
): Unit
```

Called when suggestions are updated.

| Parameters ||
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `suggestingPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the package that provided the suggestions. This value cannot be`null`. |
| `suggestedDeviceInfo` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SuggestedDeviceInfo](https://developer.android.com/reference/kotlin/android/media/SuggestedDeviceInfo)!\>:the suggestions provided by the package. This value cannot be`null`. |
