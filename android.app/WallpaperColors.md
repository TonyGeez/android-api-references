# WallpaperColors

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WallpaperColors

Kotlin| [Java](https://developer.android.com/reference/android/app/WallpaperColors "View this page in Java") 

```
class WallpaperColors : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.WallpaperColors](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#) |

Provides information about the colors of a wallpaper.

Exposes the 3 most visually representative colors of a wallpaper. Can be either [WallpaperColors.getPrimaryColor()](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#getPrimaryColor()), [WallpaperColors.getSecondaryColor()](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#getSecondaryColor())or [WallpaperColors.getTertiaryColor()](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#getTertiaryColor()).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HINT_SUPPORTS_DARK_TEXT](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#HINT_SUPPORTS_DARK_TEXT:kotlin.Int) Specifies that dark text is preferred over the current wallpaper for best presentation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HINT_SUPPORTS_DARK_THEME](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#HINT_SUPPORTS_DARK_THEME:kotlin.Int) Specifies that dark theme is preferred over the current wallpaper for best presentation. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WallpaperColors](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#WallpaperColors(android.graphics.Color,%20android.graphics.Color,%20android.graphics.Color))`(`primaryColor:` ` [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#)`, `secondaryColor:` ` [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#)?`, `tertiaryColor:` ` [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#)?`)` Constructs a new object from three colors. |
| [WallpaperColors](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#WallpaperColors(android.graphics.Color,%20android.graphics.Color,%20android.graphics.Color,%20kotlin.Int))`(`primaryColor:` ` [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#)`, `secondaryColor:` ` [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#)?`, `tertiaryColor:` ` [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#)?`, `colorHints:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new object from three colors, where hints can be specified. |
| [WallpaperColors](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#WallpaperColors(android.os.Parcel))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`)` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| static [WallpaperColors](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#)! | [fromBitmap](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#fromBitmap(android.graphics.Bitmap))`(`bitmap:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)`)` Constructs [WallpaperColors](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#) from a bitmap. |
| static [WallpaperColors](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#)! | [fromDrawable](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#fromDrawable(android.graphics.drawable.Drawable))`(`drawable:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!`)` Constructs [WallpaperColors](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#) from a drawable. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColorHints](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#getColorHints())`()` Returns the color hints for this instance. |
| [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#) | [getPrimaryColor](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#getPrimaryColor())`()` Gets the most visually representative color of the wallpaper. |
| [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#)? | [getSecondaryColor](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#getSecondaryColor())`()` Gets the second most preeminent color of the wallpaper. |
| [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#)? | [getTertiaryColor](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#getTertiaryColor())`()` Gets the third most preeminent color of the wallpaper. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [WallpaperColors](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### HINT_SUPPORTS_DARK_TEXT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HINT_SUPPORTS_DARK_TEXT: Int
```

Specifies that dark text is preferred over the current wallpaper for best presentation.

eg. A launcher may set its text color to black if this flag is specified. 

 Value: 1

### HINT_SUPPORTS_DARK_THEME

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HINT_SUPPORTS_DARK_THEME: Int
```

Specifies that dark theme is preferred over the current wallpaper for best presentation.

eg. A launcher may set its drawer color to black if this flag is specified. 

 Value: 2

## Public constructors

### WallpaperColors

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WallpaperColors(
    primaryColor: Color, 
    secondaryColor: Color?, 
    tertiaryColor: Color?)
```

Constructs a new object from three colors.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `primaryColor` | [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#):Primary color. This value cannot be`null`. |
| `secondaryColor` | [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#)?:Secondary color. This value may be`null`. |
| `tertiaryColor` | [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#)?:Tertiary color. This value may be`null`. |

**See Also**

- [android.app.WallpaperColors#fromBitmap(Bitmap)](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#fromBitmap(android.graphics.Bitmap))
- [android.app.WallpaperColors#fromDrawable(Drawable)](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#fromDrawable(android.graphics.drawable.Drawable)) 

### WallpaperColors

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WallpaperColors(
    primaryColor: Color, 
    secondaryColor: Color?, 
    tertiaryColor: Color?, 
    colorHints: Int)
```

Constructs a new object from three colors, where hints can be specified.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `primaryColor` | [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#):Primary color. This value cannot be`null`. |
| `secondaryColor` | [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#)?:Secondary color. This value may be`null`. |
| `tertiaryColor` | [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#)?:Tertiary color. This value may be`null`. |
| `colorHints` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A combination of color hints. Value is either`0`or a combination of [android.app.WallpaperColors#HINT_SUPPORTS_DARK_TEXT](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#HINT_SUPPORTS_DARK_TEXT:kotlin.Int), and [android.app.WallpaperColors#HINT_SUPPORTS_DARK_THEME](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#HINT_SUPPORTS_DARK_THEME:kotlin.Int) |

**See Also**

- [android.app.WallpaperColors#fromBitmap(Bitmap)](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#fromBitmap(android.graphics.Bitmap))
- [android.app.WallpaperColors#fromDrawable(Drawable)](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#fromDrawable(android.graphics.drawable.Drawable)) 

### WallpaperColors

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WallpaperColors(parcel: Parcel!)
```

## Public methods

### describeContents

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### fromBitmap

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromBitmap(bitmap: Bitmap): WallpaperColors!
```

Constructs [WallpaperColors](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#) from a bitmap.

Main colors will be extracted from the bitmap.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#):Source where to extract from. This value cannot be`null`. |

### fromDrawable

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromDrawable(drawable: Drawable!): WallpaperColors!
```

Constructs [WallpaperColors](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#) from a drawable.

Main colors will be extracted from the drawable.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------|
| `drawable` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!:Source where to extract from. |

### getColorHints

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getColorHints(): Int
```

Returns the color hints for this instance.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The color hints. Value is either`0`or a combination of [android.app.WallpaperColors#HINT_SUPPORTS_DARK_TEXT](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#HINT_SUPPORTS_DARK_TEXT:kotlin.Int), and [android.app.WallpaperColors#HINT_SUPPORTS_DARK_THEME](https://developer.android.com/reference/kotlin/android/app/WallpaperColors#HINT_SUPPORTS_DARK_THEME:kotlin.Int) |

### getPrimaryColor

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrimaryColor(): Color
```

Gets the most visually representative color of the wallpaper. "Visually representative" means easily noticeable in the image, probably happening at high frequency. fromBitmap

| Return ||
|--------------------------------------------------------------------------------------|--------------------------------------|
| [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#) | A color. This value cannot be`null`. |

### getSecondaryColor

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSecondaryColor(): Color?
```

Gets the second most preeminent color of the wallpaper. Can be null.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------|
| [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#)? | A color, may be null. |

### getTertiaryColor

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTertiaryColor(): Color?
```

Gets the third most preeminent color of the wallpaper. Can be null.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------|
| [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#)? | A color, may be null. |

### hashCode

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WallpaperColors!>
```
