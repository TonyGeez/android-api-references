# WebView.PictureListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PictureListener

Kotlin| [Java](../android/webkit/WebView.PictureListener.md) 
| --- | --- |

```
interface PictureListener
```

| [android.webkit.WebView.PictureListener](../android/webkit/WebView.PictureListener.md) |

| **This interface was deprecated in API level 12.**
|
| This interface is now obsolete.

Interface to listen for new pictures as they change.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNewPicture](../android/webkit/WebView.PictureListener.md))`(`view:` ` [WebView](WebView.md)!`, `picture:` ` [Picture](../android.graphics/Picture.md)?`)` Used to provide notification that the WebView's picture has changed. |

## Public methods

### onNewPicture

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onNewPicture(
    view: WebView!, 
    picture: Picture?
): Unit
```

**Deprecated:** *Deprecated due to internal changes.*

Used to provide notification that the WebView's picture has changed. See [WebView.capturePicture](WebView.md))for details of the picture.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](WebView.md)!:the WebView that owns the picture |
| `picture` | [Picture](../android.graphics/Picture.md)?:the new picture. Applications targeting [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md) or above will always receive a`null`Picture. |
