# Rating

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Rating

Kotlin| [Java](https://developer.android.com/reference/android/media/Rating "View this page in Java") 
| --- | --- |

```
class Rating : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.Rating](https://developer.android.com/reference/kotlin/android/media/Rating#) |

A class to encapsulate rating information used as content metadata. A rating is defined by its rating style (see [RATING_HEART](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_HEART:kotlin.Int), [RATING_THUMB_UP_DOWN](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_THUMB_UP_DOWN:kotlin.Int), [RATING_3_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_3_STARS:kotlin.Int), [RATING_4_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_4_STARS:kotlin.Int), [RATING_5_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_5_STARS:kotlin.Int) or [RATING_PERCENTAGE](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_PERCENTAGE:kotlin.Int)) and the actual rating value (which may be defined as "unrated"), both of which are defined when the rating instance is constructed through one of the factory methods.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATING_3_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_3_STARS:kotlin.Int) A rating style with 0 to 3 stars. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATING_4_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_4_STARS:kotlin.Int) A rating style with 0 to 4 stars. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATING_5_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_5_STARS:kotlin.Int) A rating style with 0 to 5 stars. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATING_HEART](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_HEART:kotlin.Int) A rating style with a single degree of rating, "heart" vs "no heart". |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATING_NONE](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_NONE:kotlin.Int) Indicates a rating style is not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATING_PERCENTAGE](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_PERCENTAGE:kotlin.Int) A rating style expressed as a percentage. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATING_THUMB_UP_DOWN](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_THUMB_UP_DOWN:kotlin.Int) A rating style for "thumb up" vs "thumb down". |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/Rating#describeContents())`()` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getPercentRating](https://developer.android.com/reference/kotlin/android/media/Rating#getPercentRating())`()` Return the percentage-based rating value. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRatingStyle](https://developer.android.com/reference/kotlin/android/media/Rating#getRatingStyle())`()` Return the rating style. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getStarRating](https://developer.android.com/reference/kotlin/android/media/Rating#getStarRating())`()` Return the star-based rating value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasHeart](https://developer.android.com/reference/kotlin/android/media/Rating#hasHeart())`()` Return whether the rating is "heart selected". |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRated](https://developer.android.com/reference/kotlin/android/media/Rating#isRated())`()` Return whether there is a rating value available. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isThumbUp](https://developer.android.com/reference/kotlin/android/media/Rating#isThumbUp())`()` Return whether the rating is "thumb up". |
| static [Rating](https://developer.android.com/reference/kotlin/android/media/Rating#)! | [newHeartRating](https://developer.android.com/reference/kotlin/android/media/Rating#newHeartRating(kotlin.Boolean))`(`hasHeart:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Return a Rating instance with a heart-based rating. |
| static [Rating](https://developer.android.com/reference/kotlin/android/media/Rating#)! | [newPercentageRating](https://developer.android.com/reference/kotlin/android/media/Rating#newPercentageRating(kotlin.Float))`(`percent:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Return a Rating instance with a percentage-based rating. |
| --- | --- |
| static [Rating](https://developer.android.com/reference/kotlin/android/media/Rating#)! | [newStarRating](https://developer.android.com/reference/kotlin/android/media/Rating#newStarRating(kotlin.Int,%20kotlin.Float))`(`starRatingStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `starRating:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Return a Rating instance with a star-based rating. |
| static [Rating](https://developer.android.com/reference/kotlin/android/media/Rating#)! | [newThumbRating](https://developer.android.com/reference/kotlin/android/media/Rating#newThumbRating(kotlin.Boolean))`(`thumbIsUp:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Return a Rating instance with a thumb-based rating. |
| static [Rating](https://developer.android.com/reference/kotlin/android/media/Rating#)! | [newUnratedRating](https://developer.android.com/reference/kotlin/android/media/Rating#newUnratedRating(kotlin.Int))`(`ratingStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a Rating instance with no rating. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/media/Rating#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/Rating#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [Rating](https://developer.android.com/reference/kotlin/android/media/Rating#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/Rating#CREATOR:android.os.Parcelable.Creator) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | one of [RATING_HEART](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_HEART:kotlin.Int), [RATING_THUMB_UP_DOWN](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_THUMB_UP_DOWN:kotlin.Int), [RATING_3_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_3_STARS:kotlin.Int), [RATING_4_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_4_STARS:kotlin.Int), [RATING_5_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_5_STARS:kotlin.Int), or [RATING_PERCENTAGE](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_PERCENTAGE:kotlin.Int). Value is [android.media.Rating#RATING_NONE](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_NONE:kotlin.Int), [android.media.Rating#RATING_HEART](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_HEART:kotlin.Int), [android.media.Rating#RATING_THUMB_UP_DOWN](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_THUMB_UP_DOWN:kotlin.Int), [android.media.Rating#RATING_3_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_3_STARS:kotlin.Int), [android.media.Rating#RATING_4_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_4_STARS:kotlin.Int), [android.media.Rating#RATING_5_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_5_STARS:kotlin.Int), or [android.media.Rating#RATING_PERCENTAGE](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_PERCENTAGE:kotlin.Int) |

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
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the rating is "heart selected", false if the rating is "heart unselected", if the rating style is not [RATING_HEART](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_HEART:kotlin.Int) or if it is unrated. |

### isRated

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRated(): Boolean
```

Return whether there is a rating value available.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the instance was not created with [newUnratedRating(int)](https://developer.android.com/reference/kotlin/android/media/Rating#newUnratedRating(kotlin.Int)). |

### isThumbUp

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isThumbUp(): Boolean
```

Return whether the rating is "thumb up".

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the rating is "thumb up", false if the rating is "thumb down", if the rating style is not [RATING_THUMB_UP_DOWN](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_THUMB_UP_DOWN:kotlin.Int) or if it is unrated. |

### newHeartRating

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newHeartRating(hasHeart: Boolean): Rating!
```

Return a Rating instance with a heart-based rating. Create and return a new Rating instance with a rating style of [RATING_HEART](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_HEART:kotlin.Int), and a heart-based rating.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `hasHeart` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true for a "heart selected" rating, false for "heart unselected". |

| Return ||
|---------------------------------------------------------------------------------|------------------------|
| [Rating](https://developer.android.com/reference/kotlin/android/media/Rating#)! | a new Rating instance. |

### newPercentageRating

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newPercentageRating(percent: Float): Rating!
```

Return a Rating instance with a percentage-based rating. Create and return a new Rating instance with a [RATING_PERCENTAGE](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_PERCENTAGE:kotlin.Int) rating style, and a rating of the given percentage.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------|
| `percent` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the value of the rating |

| Return ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Rating](https://developer.android.com/reference/kotlin/android/media/Rating#)! | null if the rating is out of range, a new Rating instance otherwise. |

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
| `starRatingStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [RATING_3_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_3_STARS:kotlin.Int), [RATING_4_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_4_STARS:kotlin.Int), [RATING_5_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_5_STARS:kotlin.Int). Value is [android.media.Rating#RATING_3_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_3_STARS:kotlin.Int), [android.media.Rating#RATING_4_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_4_STARS:kotlin.Int), or [android.media.Rating#RATING_5_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_5_STARS:kotlin.Int) |
| `starRating` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):a number ranging from 0.0f to 3.0f, 4.0f or 5.0f according to the rating style. |

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Rating](https://developer.android.com/reference/kotlin/android/media/Rating#)! | null if the rating style is invalid, or the rating is out of range, a new Rating instance otherwise. |

### newThumbRating

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newThumbRating(thumbIsUp: Boolean): Rating!
```

Return a Rating instance with a thumb-based rating. Create and return a new Rating instance with a [RATING_THUMB_UP_DOWN](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_THUMB_UP_DOWN:kotlin.Int) rating style, and a "thumb up" or "thumb down" rating.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `thumbIsUp` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true for a "thumb up" rating, false for "thumb down". |

| Return ||
|---------------------------------------------------------------------------------|------------------------|
| [Rating](https://developer.android.com/reference/kotlin/android/media/Rating#)! | a new Rating instance. |

### newUnratedRating

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newUnratedRating(ratingStyle: Int): Rating!
```

Return a Rating instance with no rating. Create and return a new Rating instance with no rating known for the given rating style.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ratingStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [RATING_HEART](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_HEART:kotlin.Int), [RATING_THUMB_UP_DOWN](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_THUMB_UP_DOWN:kotlin.Int), [RATING_3_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_3_STARS:kotlin.Int), [RATING_4_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_4_STARS:kotlin.Int), [RATING_5_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_5_STARS:kotlin.Int), or [RATING_PERCENTAGE](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_PERCENTAGE:kotlin.Int). Value is [android.media.Rating#RATING_NONE](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_NONE:kotlin.Int), [android.media.Rating#RATING_HEART](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_HEART:kotlin.Int), [android.media.Rating#RATING_THUMB_UP_DOWN](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_THUMB_UP_DOWN:kotlin.Int), [android.media.Rating#RATING_3_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_3_STARS:kotlin.Int), [android.media.Rating#RATING_4_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_4_STARS:kotlin.Int), [android.media.Rating#RATING_5_STARS](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_5_STARS:kotlin.Int), or [android.media.Rating#RATING_PERCENTAGE](https://developer.android.com/reference/kotlin/android/media/Rating#RATING_PERCENTAGE:kotlin.Int) |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Rating](https://developer.android.com/reference/kotlin/android/media/Rating#)! | null if an invalid rating style is passed, a new Rating instance otherwise. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Rating!>
```
