# MediaRouter2.DeviceSuggestionsUpdatesCallback

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeviceSuggestionsUpdatesCallback

Kotlin| [Java](../android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback.md) 
| --- | --- |

```
interface DeviceSuggestionsUpdatesCallback
```

| [android.media.MediaRouter2.DeviceSuggestionsUpdatesCallback](../android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback.md) |

Callback for receiving events about device suggestions

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuggestionsCleared](../android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback.md))`(`suggestingPackageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Called when suggestions are cleared. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuggestionsRequested](../android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback.md))`()` Called when a router requests a suggestion from suggestion providers. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuggestionsUpdated](../android/media/MediaRouter2.DeviceSuggestionsUpdatesCallback.md))`(`suggestingPackageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `suggestedDeviceInfo:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [SuggestedDeviceInfo](../android/media/SuggestedDeviceInfo.md)!>`)` Called when suggestions are updated. |
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
| `suggestedDeviceInfo` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SuggestedDeviceInfo](../android/media/SuggestedDeviceInfo.md)!\>:the suggestions provided by the package. This value cannot be`null`. |
