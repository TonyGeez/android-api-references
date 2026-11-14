# RatingBar.OnRatingBarChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnRatingBarChangeListener

Kotlin| [Java](../android/widget/RatingBar.OnRatingBarChangeListener.md) 
| --- | --- |

```
interface OnRatingBarChangeListener
```

| [android.widget.RatingBar.OnRatingBarChangeListener](../android/widget/RatingBar.OnRatingBarChangeListener.md) |

A callback that notifies clients when the rating has been changed. This includes changes that were initiated by the user through a touch gesture or arrow key/trackball as well as changes that were initiated programmatically.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRatingChanged](../android/widget/RatingBar.OnRatingBarChangeListener.md))`(`ratingBar:` ` [RatingBar](RatingBar.md)!`, `rating:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `fromUser:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Notification that the rating has changed. |

## Public methods

### onRatingChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onRatingChanged(
    ratingBar: RatingBar!, 
    rating: Float, 
    fromUser: Boolean
): Unit
```

Notification that the rating has changed. Clients can use the fromUser parameter to distinguish user-initiated changes from those that occurred programmatically. This will not be called continuously while the user is dragging, only when the user finalizes a rating by lifting the touch.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ratingBar` | [RatingBar](RatingBar.md)!:The RatingBar whose rating has changed. |
| `rating` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The current rating. This will be in the range 0..numStars. |
| `fromUser` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the rating change was initiated by a user's touch gesture or arrow key/horizontal trackbell movement. |
| --- | --- |
