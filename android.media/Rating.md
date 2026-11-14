# Rating

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Rating

Kotlin| [Java](../android/media/Rating.md) 
| --- | --- |

```
class Rating : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.Rating](../android/media/Rating.md) |

A class to encapsulate rating information used as content metadata. A rating is defined by its rating style (see [RATING_HEART](../android/media/Rating.md), [RATING_THUMB_UP_DOWN](../android/media/Rating.md), [RATING_3_STARS](../android/media/Rating.md), [RATING_4_STARS](../android/media/Rating.md), [RATING_5_STARS](../android/media/Rating.md) or [RATING_PERCENTAGE](../android/media/Rating.md)) and the actual rating value (which may be defined as "unrated"), both of which are defined when the rating instance is constructed through one of the factory methods.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATING_3_STARS](../android/media/Rating.md) A rating style with 0 to 3 stars. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATING_4_STARS](../android/media/Rating.md) A rating style with 0 to 4 stars. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATING_5_STARS](../android/media/Rating.md) A rating style with 0 to 5 stars. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATING_HEART](../android/media/Rating.md) A rating style with a single degree of rating, "heart" vs "no heart". |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATING_NONE](../android/media/Rating.md) Indicates a rating style is not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATING_PERCENTAGE](../android/media/Rating.md) A rating style expressed as a percentage. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATING_THUMB_UP_DOWN](../android/media/Rating.md) A rating style for "thumb up" vs "thumb down". |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/media/Rating.md))`()` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getPercentRating](../android/media/Rating.md))`()` Return the percentage-based rating value. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRatingStyle](../android/media/Rating.md))`()` Return the rating style. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getStarRating](../android/media/Rating.md))`()` Return the star-based rating value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasHeart](../android/media/Rating.md))`()` Return whether the rating is "heart selected". |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRated](../android/media/Rating.md))`()` Return whether there is a rating value available. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isThumbUp](../android/media/Rating.md))`()` Return whether the rating is "thumb up". |
| static [Rating](../android/media/Rating.md)! | [newHeartRating](../android/media/Rating.md))`(`hasHeart:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Return a Rating instance with a heart-based rating. |
| static [Rating](../android/media/Rating.md)! | [newPercentageRating](../android/media/Rating.md))`(`percent:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Return a Rating instance with a percentage-based rating. |
| --- | --- |
| static [Rating](../android/media/Rating.md)! | [newStarRating](../android/media/Rating.md))`(`starRatingStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `starRating:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Return a Rating instance with a star-based rating. |
| static [Rating](../android/media/Rating.md)! | [newThumbRating](../android/media/Rating.md))`(`thumbIsUp:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Return a Rating instance with a thumb-based rating. |
| static [Rating](../android/media/Rating.md)! | [newUnratedRating](../android/media/Rating.md))`(`ratingStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a Rating instance with no rating. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/media/Rating.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/media/Rating.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Rating](../android/media/Rating.md)!\> | [CREATOR](../android/media/Rating.md) <br /> |

## Constants

### RATING_3_STARS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RATING_3_STARS: Int
```

A rating style with 0 to 3 stars. 

 Value: 3

### RATING_4_STARS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RATING_4_STARS: Int
```

A rating style with 0 to 4 stars. 

 Value: 4

### RATING_5_STARS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RATING_5_STARS: Int
```

A rating style with 0 to 5 stars. 

 Value: 5

### RATING_HEART

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RATING_HEART: Int
```

A rating style with a single degree of rating, "heart" vs "no heart". Can be used to indicate the content referred to is a favorite (or not). 

 Value: 1

### RATING_NONE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RATING_NONE: Int
```

Indicates a rating style is not supported. A Rating will never have this type, but can be used by other classes to indicate they do not support Rating. 

 Value: 0

### RATING_PERCENTAGE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RATING_PERCENTAGE: Int
```

A rating style expressed as a percentage. 

 Value: 6

### RATING_THUMB_UP_DOWN

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RATING_THUMB_UP_DOWN: Int
```

A rating style for "thumb up" vs "thumb down". 

 Value: 2

## Public methods

### describeContents

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getPercentRating

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPercentRating(): Float
```

Return the percentage-based rating value.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a rating value greater or equal to 0.0f, or a negative value if the rating style is not percentage-based, or if it is unrated. |

### getRatingStyle

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRatingStyle(): Int
```

Return the rating style.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | one of [RATING_HEART](../android/media/Rating.md), [RATING_THUMB_UP_DOWN](../android/media/Rating.md), [RATING_3_STARS](../android/media/Rating.md), [RATING_4_STARS](../android/media/Rating.md), [RATING_5_STARS](../android/media/Rating.md), or [RATING_PERCENTAGE](../android/media/Rating.md). Value is [android.media.Rating#RATING_NONE](../android/media/Rating.md), [android.media.Rating#RATING_HEART](../android/media/Rating.md), [android.media.Rating#RATING_THUMB_UP_DOWN](../android/media/Rating.md), [android.media.Rating#RATING_3_STARS](../android/media/Rating.md), [android.media.Rating#RATING_4_STARS](../android/media/Rating.md), [android.media.Rating#RATING_5_STARS](../android/media/Rating.md), or [android.media.Rating#RATING_PERCENTAGE](../android/media/Rating.md) |

### getStarRating

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStarRating(): Float
```

Return the star-based rating value.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a rating value greater or equal to 0.0f, or a negative value if the rating style is not star-based, or if it is unrated. |

### hasHeart

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasHeart(): Boolean
```

Return whether the rating is "heart selected".

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the rating is "heart selected", false if the rating is "heart unselected", if the rating style is not [RATING_HEART](../android/media/Rating.md) or if it is unrated. |

### isRated

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRated(): Boolean
```

Return whether there is a rating value available.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the instance was not created with [newUnratedRating(int)](../android/media/Rating.md)). |

### isThumbUp

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isThumbUp(): Boolean
```

Return whether the rating is "thumb up".

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the rating is "thumb up", false if the rating is "thumb down", if the rating style is not [RATING_THUMB_UP_DOWN](../android/media/Rating.md) or if it is unrated. |

### newHeartRating

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newHeartRating(hasHeart: Boolean): Rating!
```

Return a Rating instance with a heart-based rating. Create and return a new Rating instance with a rating style of [RATING_HEART](../android/media/Rating.md), and a heart-based rating.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `hasHeart` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true for a "heart selected" rating, false for "heart unselected". |

| Return ||
|---------------------------------------------------------------------------------|------------------------|
| [Rating](../android/media/Rating.md)! | a new Rating instance. |

### newPercentageRating

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newPercentageRating(percent: Float): Rating!
```

Return a Rating instance with a percentage-based rating. Create and return a new Rating instance with a [RATING_PERCENTAGE](../android/media/Rating.md) rating style, and a rating of the given percentage.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------|
| `percent` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the value of the rating |

| Return ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Rating](../android/media/Rating.md)! | null if the rating is out of range, a new Rating instance otherwise. |

### newStarRating

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newStarRating(
    starRatingStyle: Int, 
    starRating: Float
): Rating!
```

Return a Rating instance with a star-based rating. Create and return a new Rating instance with one of the star-base rating styles and the given integer or fractional number of stars. Non integer values can for instance be used to represent an average rating value, which might not be an integer number of stars.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `starRatingStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [RATING_3_STARS](../android/media/Rating.md), [RATING_4_STARS](../android/media/Rating.md), [RATING_5_STARS](../android/media/Rating.md). Value is [android.media.Rating#RATING_3_STARS](../android/media/Rating.md), [android.media.Rating#RATING_4_STARS](../android/media/Rating.md), or [android.media.Rating#RATING_5_STARS](../android/media/Rating.md) |
| `starRating` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):a number ranging from 0.0f to 3.0f, 4.0f or 5.0f according to the rating style. |

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Rating](../android/media/Rating.md)! | null if the rating style is invalid, or the rating is out of range, a new Rating instance otherwise. |

### newThumbRating

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newThumbRating(thumbIsUp: Boolean): Rating!
```

Return a Rating instance with a thumb-based rating. Create and return a new Rating instance with a [RATING_THUMB_UP_DOWN](../android/media/Rating.md) rating style, and a "thumb up" or "thumb down" rating.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `thumbIsUp` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true for a "thumb up" rating, false for "thumb down". |

| Return ||
|---------------------------------------------------------------------------------|------------------------|
| [Rating](../android/media/Rating.md)! | a new Rating instance. |

### newUnratedRating

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newUnratedRating(ratingStyle: Int): Rating!
```

Return a Rating instance with no rating. Create and return a new Rating instance with no rating known for the given rating style.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ratingStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [RATING_HEART](../android/media/Rating.md), [RATING_THUMB_UP_DOWN](../android/media/Rating.md), [RATING_3_STARS](../android/media/Rating.md), [RATING_4_STARS](../android/media/Rating.md), [RATING_5_STARS](../android/media/Rating.md), or [RATING_PERCENTAGE](../android/media/Rating.md). Value is [android.media.Rating#RATING_NONE](../android/media/Rating.md), [android.media.Rating#RATING_HEART](../android/media/Rating.md), [android.media.Rating#RATING_THUMB_UP_DOWN](../android/media/Rating.md), [android.media.Rating#RATING_3_STARS](../android/media/Rating.md), [android.media.Rating#RATING_4_STARS](../android/media/Rating.md), [android.media.Rating#RATING_5_STARS](../android/media/Rating.md), or [android.media.Rating#RATING_PERCENTAGE](../android/media/Rating.md) |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Rating](../android/media/Rating.md)! | null if an invalid rating style is passed, a new Rating instance otherwise. |

### toString

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Rating!>
```
