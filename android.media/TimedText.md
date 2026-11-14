# TimedText

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimedText

Kotlin| [Java](https://developer.android.com/reference/android/media/TimedText "View this page in Java") 
| --- | --- |

```
class TimedText
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.TimedText](https://developer.android.com/reference/kotlin/android/media/TimedText#) |

Class to hold the timed text's metadata, including:

- The characters for rendering
- The rendering position for the timed text

<br />

To render the timed text, applications need to do the following:

- Implement the [MediaPlayer.OnTimedTextListener](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnTimedTextListener) interface
- Register the [MediaPlayer.OnTimedTextListener](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnTimedTextListener) callback on a MediaPlayer object that is used for playback
- When a onTimedText callback is received, do the following:
 - call [getText](https://developer.android.com/reference/kotlin/android/media/TimedText#getText())to get the characters for rendering
 - call [getBounds](https://developer.android.com/reference/kotlin/android/media/TimedText#getBounds())to get the text rendering area/region

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)! | [getBounds](https://developer.android.com/reference/kotlin/android/media/TimedText#getBounds())`()` Get the rectangle area or region for rendering the timed text as specified by a Rect object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getText](https://developer.android.com/reference/kotlin/android/media/TimedText#getText())`()` Get the characters in the timed text. |

## Public methods

### getBounds

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBounds(): Rect!
```

Get the rectangle area or region for rendering the timed text as specified by a Rect object.

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)! | the rectangle region to render the characters in the timed text. If no bounds information is available (a null is returned), render the timed text at the center bottom of the display. |

### getText

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getText(): String!
```

Get the characters in the timed text.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the characters as a String object in the TimedText. Applications should stop rendering previous timed text at the current rendering region if a null is returned, until the next non-null timed text is received. |
