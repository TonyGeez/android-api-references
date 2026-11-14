# WebView.PictureListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PictureListener

Kotlin| [Java](https://developer.android.com/reference/android/webkit/WebView.PictureListener "View this page in Java") 

```
interface PictureListener
```

| [android.webkit.WebView.PictureListener](https://developer.android.com/reference/kotlin/android/webkit/WebView.PictureListener#) |

| **This interface was deprecated in API level 12.**
|
| This interface is now obsolete.

Interface to listen for new pictures as they change.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNewPicture](https://developer.android.com/reference/kotlin/android/webkit/WebView.PictureListener#onNewPicture(android.webkit.WebView,%20android.graphics.Picture))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `picture:` ` [Picture](https://developer.android.com/reference/kotlin/android/graphics/Picture.html#)?`)` Used to provide notification that the WebView's picture has changed. |

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

Used to provide notification that the WebView's picture has changed. See [WebView.capturePicture](https://developer.android.com/reference/kotlin/android/webkit/WebView#capturePicture())for details of the picture.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:the WebView that owns the picture |
| `picture` | [Picture](https://developer.android.com/reference/kotlin/android/graphics/Picture.html#)?:the new picture. Applications targeting [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int) or above will always receive a`null`Picture. |
