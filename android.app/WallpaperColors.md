# WallpaperColors

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WallpaperColors

Kotlin| [Java](WallpaperColors.md) 
| --- | --- |

```
class WallpaperColors : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.WallpaperColors](WallpaperColors.md) |

Provides information about the colors of a wallpaper.

Exposes the 3 most visually representative colors of a wallpaper. Can be either [WallpaperColors.getPrimaryColor()](WallpaperColors.md)), [WallpaperColors.getSecondaryColor()](WallpaperColors.md))or [WallpaperColors.getTertiaryColor()](WallpaperColors.md)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HINT_SUPPORTS_DARK_TEXT](WallpaperColors.md) Specifies that dark text is preferred over the current wallpaper for best presentation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HINT_SUPPORTS_DARK_THEME](WallpaperColors.md) Specifies that dark theme is preferred over the current wallpaper for best presentation. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WallpaperColors](WallpaperColors.md))`(`primaryColor:` ` [Color](../android.graphics/Color.md)`, `secondaryColor:` ` [Color](../android.graphics/Color.md)?`, `tertiaryColor:` ` [Color](../android.graphics/Color.md)?`)` Constructs a new object from three colors. |
| [WallpaperColors](WallpaperColors.md))`(`primaryColor:` ` [Color](../android.graphics/Color.md)`, `secondaryColor:` ` [Color](../android.graphics/Color.md)?`, `tertiaryColor:` ` [Color](../android.graphics/Color.md)?`, `colorHints:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new object from three colors, where hints can be specified. |
| [WallpaperColors](WallpaperColors.md))`(`parcel:` ` [Parcel](../android.os/Parcel.md)!`)` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](WallpaperColors.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](WallpaperColors.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| static [WallpaperColors](WallpaperColors.md)! | [fromBitmap](WallpaperColors.md))`(`bitmap:` ` [Bitmap](../android.graphics/Bitmap.md)`)` Constructs [WallpaperColors](WallpaperColors.md) from a bitmap. |
| --- | --- |
| static [WallpaperColors](WallpaperColors.md)! | [fromDrawable](WallpaperColors.md))`(`drawable:` ` [Drawable](../android.graphics.drawable/Drawable.md)!`)` Constructs [WallpaperColors](WallpaperColors.md) from a drawable. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColorHints](WallpaperColors.md))`()` Returns the color hints for this instance. |
| [Color](../android.graphics/Color.md) | [getPrimaryColor](WallpaperColors.md))`()` Gets the most visually representative color of the wallpaper. |
| --- | --- |
| [Color](../android.graphics/Color.md)? | [getSecondaryColor](WallpaperColors.md))`()` Gets the second most preeminent color of the wallpaper. |
| [Color](../android.graphics/Color.md)? | [getTertiaryColor](WallpaperColors.md))`()` Gets the third most preeminent color of the wallpaper. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](WallpaperColors.md))`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](WallpaperColors.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](WallpaperColors.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [WallpaperColors](WallpaperColors.md)!\> | [CREATOR](WallpaperColors.md) <br /> |

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
| `primaryColor` | [Color](../android.graphics/Color.md):Primary color. This value cannot be`null`. |
| `secondaryColor` | [Color](../android.graphics/Color.md)?:Secondary color. This value may be`null`. |
| `tertiaryColor` | [Color](../android.graphics/Color.md)?:Tertiary color. This value may be`null`. |
| --- | --- |

**See Also**

- [android.app.WallpaperColors#fromBitmap(Bitmap)](WallpaperColors.md))
- [android.app.WallpaperColors#fromDrawable(Drawable)](WallpaperColors.md)) 

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
| `primaryColor` | [Color](../android.graphics/Color.md):Primary color. This value cannot be`null`. |
| `secondaryColor` | [Color](../android.graphics/Color.md)?:Secondary color. This value may be`null`. |
| `tertiaryColor` | [Color](../android.graphics/Color.md)?:Tertiary color. This value may be`null`. |
| --- | --- |
| `colorHints` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A combination of color hints. Value is either`0`or a combination of [android.app.WallpaperColors#HINT_SUPPORTS_DARK_TEXT](WallpaperColors.md), and [android.app.WallpaperColors#HINT_SUPPORTS_DARK_THEME](WallpaperColors.md) |

**See Also**

- [android.app.WallpaperColors#fromBitmap(Bitmap)](WallpaperColors.md))
- [android.app.WallpaperColors#fromDrawable(Drawable)](WallpaperColors.md)) 

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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

Constructs [WallpaperColors](WallpaperColors.md) from a bitmap.

Main colors will be extracted from the bitmap.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](../android.graphics/Bitmap.md):Source where to extract from. This value cannot be`null`. |

### fromDrawable

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromDrawable(drawable: Drawable!): WallpaperColors!
```

Constructs [WallpaperColors](WallpaperColors.md) from a drawable.

Main colors will be extracted from the drawable.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------|
| `drawable` | [Drawable](../android.graphics.drawable/Drawable.md)!:Source where to extract from. |

### getColorHints

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getColorHints(): Int
```

Returns the color hints for this instance.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The color hints. Value is either`0`or a combination of [android.app.WallpaperColors#HINT_SUPPORTS_DARK_TEXT](WallpaperColors.md), and [android.app.WallpaperColors#HINT_SUPPORTS_DARK_THEME](WallpaperColors.md) |

### getPrimaryColor

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrimaryColor(): Color
```

Gets the most visually representative color of the wallpaper. "Visually representative" means easily noticeable in the image, probably happening at high frequency. fromBitmap

| Return ||
|--------------------------------------------------------------------------------------|--------------------------------------|
| [Color](../android.graphics/Color.md) | A color. This value cannot be`null`. |

### getSecondaryColor

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSecondaryColor(): Color?
```

Gets the second most preeminent color of the wallpaper. Can be null.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------|
| [Color](../android.graphics/Color.md)? | A color, may be null. |

### getTertiaryColor

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTertiaryColor(): Color?
```

Gets the third most preeminent color of the wallpaper. Can be null.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------|
| [Color](../android.graphics/Color.md)? | A color, may be null. |

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
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WallpaperColors!>
```
