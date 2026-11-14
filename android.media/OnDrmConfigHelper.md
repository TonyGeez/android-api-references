# MediaPlayer.OnDrmConfigHelper

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDrmConfigHelper

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaPlayer.OnDrmConfigHelper "View this page in Java") 
| --- | --- |

```
interface OnDrmConfigHelper
```

| [android.media.MediaPlayer.OnDrmConfigHelper](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnDrmConfigHelper#) |

Interface definition of a callback to be invoked when the app can do DRM configuration (get/set properties) before the session is opened. This facilitates configuration of the properties, like 'securityLevel', which has to be set after DRM scheme creation but before the DRM session is opened. The only allowed DRM calls in this listener are`getDrmPropertyString`and`setDrmPropertyString`.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDrmConfig](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnDrmConfigHelper#onDrmConfig(android.media.MediaPlayer))`(`mp:` ` [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!`)` Called to give the app the opportunity to configure DRM before the session is created |

## Public methods

### onDrmConfig

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDrmConfig(mp: MediaPlayer!): Unit
```

Called to give the app the opportunity to configure DRM before the session is created

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------|
| `mp` | [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!:the`MediaPlayer`associated with this callback |
