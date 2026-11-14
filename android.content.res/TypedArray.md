# TypedArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TypedArray

Kotlin| [Java](https://developer.android.com/reference/android/content/res/TypedArray "View this page in Java") 

```
open class TypedArray : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.res.TypedArray](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#) |

Container for an array of values that were retrieved with[Resources.Theme.obtainStyledAttributes(AttributeSet, int[], int, int)](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme#obtainStyledAttributes(android.util.AttributeSet,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.Int))or [Resources.obtainAttributes](https://developer.android.com/reference/kotlin/android/content/res/Resources#obtainAttributes(android.util.AttributeSet,%20kotlin.IntArray)). Be sure to call [recycle](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#recycle())when done with them. The indices used to retrieve values from this structure correspond to the positions of the attributes given to obtainStyledAttributes.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#close())`()` Recycles the TypedArray, to be re-used by a later caller. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBoolean](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getBoolean(kotlin.Int,%20kotlin.Boolean))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Retrieve the boolean value for the attribute at index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChangingConfigurations](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getChangingConfigurations())`()` Return a mask of the configuration parameters for which the values in this typed array may change. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColor](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getColor(kotlin.Int,%20kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve the color value for the attribute at index. |
| open [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList)? | [getColorStateList](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getColorStateList(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve the ColorStateList for the attribute at index. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDimension](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getDimension(kotlin.Int,%20kotlin.Float))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Retrieve a dimensional unit attribute at index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDimensionPixelOffset](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getDimensionPixelOffset(kotlin.Int,%20kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve a dimensional unit attribute at index for use as an offset in raw pixels. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDimensionPixelSize](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getDimensionPixelSize(kotlin.Int,%20kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve a dimensional unit attribute at index for use as a size in raw pixels. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | [getDrawable](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getDrawable(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve the Drawable for the attribute at index. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getFloat(kotlin.Int,%20kotlin.Float))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Retrieve the float value for the attribute at index. |
| open [Typeface](https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#)? | [getFont](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getFont(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve the Typeface for the attribute at index. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFraction](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getFraction(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `base:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pbase:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Retrieves a fractional unit attribute at index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getIndex(kotlin.Int))`(`at:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns an index in the array that has data. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndexCount](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getIndexCount())`()` Returns the number of indices in the array that actually have data. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getInt(kotlin.Int,%20kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve the integer value for the attribute at index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInteger](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getInteger(kotlin.Int,%20kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve the integer value for the attribute at index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDimension](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getLayoutDimension(kotlin.Int,%20kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Special version of [getDimensionPixelSize](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getDimensionPixelSize(kotlin.Int,%20kotlin.Int))for retrieving [android.view.ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)'s layout_width and layout_height attributes. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutDimension](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getLayoutDimension(kotlin.Int,%20kotlin.String))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Special version of [getDimensionPixelSize](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getDimensionPixelSize(kotlin.Int,%20kotlin.Int))for retrieving [android.view.ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)'s layout_width and layout_height attributes. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNonResourceString](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getNonResourceString(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the string value for the attribute at index, but only if that string comes from an immediate value in an XML file. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPositionDescription](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getPositionDescription())`()` Returns a message about the parser state suitable for printing error messages. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResourceId](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getResourceId(kotlin.Int,%20kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the resource identifier for the attribute at index. |
| open [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources)! | [getResources](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getResources())`()` Returns the Resources object this array was loaded from. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSourceResourceId](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getSourceResourceId(kotlin.Int,%20kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defaultValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the resource ID of the style or layout against which the specified attribute was resolved, otherwise returns defValue. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getString](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getString(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the string value for the attribute at index. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getText](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getText(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the styled string value for the attribute at index. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>! | [getTextArray](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getTextArray(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve the CharSequence\[\] for the attribute at index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getType(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the type of attribute at the specified index. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getValue](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getValue(kotlin.Int,%20android.util.TypedValue))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outValue:` ` [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)!`)` Retrieve the raw TypedValue for the attribute at index. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasValue](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#hasValue(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines whether there is an attribute at index. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasValueOrEmpty](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#hasValueOrEmpty(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines whether there is an attribute at index, returning`true`if the attribute was explicitly set to`@empty`and`false`only if the attribute was undefined. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#length())`()` Returns the number of values in this array. |
| open [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)! | [peekValue](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#peekValue(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve the raw TypedValue for the attribute at index and return a temporary object holding its data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [recycle](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#recycle())`()` Recycles the TypedArray, to be re-used by a later caller. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#toString())`()` <br /> |

## Public methods

### close

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Recycles the TypedArray, to be re-used by a later caller. After calling this function you must not ever touch the typed array again.

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/content/res/TypedArray#recycle()> 

### getBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBoolean(
    index: Int, 
    defValue: Boolean
): Boolean
```

Retrieve the boolean value for the attribute at index.

If the attribute is an integer value, this method returns false if the attribute is equal to zero, and true otherwise. If the attribute is not a boolean or integer value, this method will attempt to coerce it to an integer using [Integer.decode(String)](https://developer.android.com/reference/kotlin/java/lang/Integer.html#decode(kotlin.String))and return whether it is equal to zero.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |
| `defValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Value to return if the attribute is not defined or cannot be coerced to an integer. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Boolean value of the attribute, or defValue if the attribute was not defined or could not be coerced to an integer. |

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### getChangingConfigurations

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChangingConfigurations(): Int
```

Return a mask of the configuration parameters for which the values in this typed array may change.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Returns a mask of the changing configuration parameters, as defined by [android.content.pm.ActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#). Value is either`0`or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MCC:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_MNC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MNC:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_LOCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LOCALE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_TOUCHSCREEN:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD_HIDDEN:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_NAVIGATION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ORIENTATION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_LAYOUT:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_UI_MODE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_SIZE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SMALLEST_SCREEN_SIZE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_DENSITY](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_DENSITY:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LAYOUT_DIRECTION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_COLOR_MODE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_SCALE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_GRAMMATICAL_GENDER:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_WEIGHT_ADJUSTMENT:kotlin.Int), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ASSETS_PATHS:kotlin.Int), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_RESOURCES_UNUSED:kotlin.Int) |

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

**See Also**

- [android.content.pm.ActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#) 

### getColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColor(
    index: Int, 
    defValue: Int
): Int
```

Retrieve the color value for the attribute at index. If the attribute references a color resource holding a complex [android.content.res.ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList), then the default color from the set is returned.

This method will throw an exception if the attribute is defined but is not an integer color or color state list.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |
| `defValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value to return if the attribute is not defined or not a resource. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Attribute color value, or defValue if not defined. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |
| `java.lang.UnsupportedOperationException` | if the attribute is defined but is not an integer color or color state list. |

### getColorStateList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColorStateList(index: Int): ColorStateList?
```

Retrieve the ColorStateList for the attribute at index. The value may be either a single solid color or a reference to a color or complex [android.content.res.ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList) description.

This method will return`null`if the attribute is not defined or is not an integer color or color state list.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |

| Return ||
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList)? | ColorStateList for the attribute, or`null`if not defined. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------|
| `java.lang.RuntimeException` | if the attribute if the TypedArray has already been recycled. |
| `java.lang.UnsupportedOperationException` | if the attribute is defined but is not an integer color or color state list. |

### getDimension

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDimension(
    index: Int, 
    defValue: Float
): Float
```

Retrieve a dimensional unit attribute at index. Unit conversions are based on the current [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#) associated with the resources this [TypedArray](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#) object came from.

This method will throw an exception if the attribute is defined but is not a dimension.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |
| `defValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Value to return if the attribute is not defined or not a resource. |

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Attribute dimension value multiplied by the appropriate metric, or defValue if not defined. |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |
| `java.lang.UnsupportedOperationException` | if the attribute is defined but is not an integer. |

**See Also**

- [#getDimensionPixelOffset](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getDimensionPixelOffset(kotlin.Int,%20kotlin.Int))
- [#getDimensionPixelSize](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getDimensionPixelSize(kotlin.Int,%20kotlin.Int)) 

### getDimensionPixelOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDimensionPixelOffset(
    index: Int, 
    defValue: Int
): Int
```

Retrieve a dimensional unit attribute at index for use as an offset in raw pixels. This is the same as [getDimension](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getDimension(kotlin.Int,%20kotlin.Float)), except the returned value is converted to integer pixels for you. An offset conversion involves simply truncating the base value to an integer.

This method will throw an exception if the attribute is defined but is not a dimension.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |
| `defValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value to return if the attribute is not defined or not a resource. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Attribute dimension value multiplied by the appropriate metric and truncated to integer pixels, or defValue if not defined. |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |
| `java.lang.UnsupportedOperationException` | if the attribute is defined but is not an integer. |

**See Also**

- [#getDimension](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getDimension(kotlin.Int,%20kotlin.Float))
- [#getDimensionPixelSize](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getDimensionPixelSize(kotlin.Int,%20kotlin.Int)) 

### getDimensionPixelSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDimensionPixelSize(
    index: Int, 
    defValue: Int
): Int
```

Retrieve a dimensional unit attribute at index for use as a size in raw pixels. This is the same as [getDimension](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getDimension(kotlin.Int,%20kotlin.Float)), except the returned value is converted to integer pixels for use as a size. A size conversion involves rounding the base value, and ensuring that a non-zero base value is at least one pixel in size.

This method will throw an exception if the attribute is defined but is not a dimension.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |
| `defValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value to return if the attribute is not defined or not a resource. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Attribute dimension value multiplied by the appropriate metric and truncated to integer pixels, or defValue if not defined. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |
| `java.lang.UnsupportedOperationException` | if the attribute is defined but is not a dimension. |

**See Also**

- [#getDimension](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getDimension(kotlin.Int,%20kotlin.Float))
- [#getDimensionPixelOffset](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getDimensionPixelOffset(kotlin.Int,%20kotlin.Int)) 

### getDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDrawable(index: Int): Drawable?
```

Retrieve the Drawable for the attribute at index.

This method will throw an exception if the attribute is defined but is not a color or drawable resource.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |

| Return ||
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | Drawable for the attribute, or`null`if not defined. |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |
| `java.lang.UnsupportedOperationException` | if the attribute is defined but is not a color or drawable resource. |

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFloat(
    index: Int, 
    defValue: Float
): Float
```

Retrieve the float value for the attribute at index.

If the attribute is not a float or an integer, this method will attempt to coerce it to a float using [Float.parseFloat(String)](https://developer.android.com/reference/kotlin/java/lang/Float.html#parseFloat(kotlin.String)).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Attribute float value, or defValue if the attribute was not defined or could not be coerced to a float. |

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### getFont

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFont(index: Int): Typeface?
```

Retrieve the Typeface for the attribute at index.

This method will throw an exception if the attribute is defined but is not a font.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |

| Return ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Typeface](https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#)? | Typeface for the attribute, or`null`if not defined. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |
| `java.lang.UnsupportedOperationException` | if the attribute is defined but is not a font resource. |

### getFraction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFraction(
    index: Int, 
    base: Int, 
    pbase: Int, 
    defValue: Float
): Float
```

Retrieves a fractional unit attribute at index.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |
| `base` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The base value of this fraction. In other words, a standard fraction is multiplied by this value. |
| `pbase` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The parent base value of this fraction. In other words, a parent fraction (nn%p) is multiplied by this value. |
| `defValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Value to return if the attribute is not defined or not a resource. |

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Attribute fractional value multiplied by the appropriate base value, or defValue if not defined. |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |
| `java.lang.UnsupportedOperationException` | if the attribute is defined but is not a fraction. |

### getIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIndex(at: Int): Int
```

Returns an index in the array that has data. Attributes with a value of @empty are included, as this is an explicit indicator.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `at` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index you would like to returned, ranging from 0 to [getIndexCount()](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getIndexCount()). |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The index at the given offset, which can be used with [getValue](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getValue(kotlin.Int,%20android.util.TypedValue))and related APIs. |

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### getIndexCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIndexCount(): Int
```

Returns the number of indices in the array that actually have data. Attributes with a value of @empty are included, as this is an explicit indicator.

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### getInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInt(
    index: Int, 
    defValue: Int
): Int
```

Retrieve the integer value for the attribute at index.

If the attribute is not an integer, this method will attempt to coerce it to an integer using [Integer.decode(String)](https://developer.android.com/reference/kotlin/java/lang/Integer.html#decode(kotlin.String)).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |
| `defValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value to return if the attribute is not defined or cannot be coerced to an integer. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Integer value of the attribute, or defValue if the attribute was not defined or could not be coerced to an integer. |

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### getInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInteger(
    index: Int, 
    defValue: Int
): Int
```

Retrieve the integer value for the attribute at index.

Unlike [getInt(int,int)](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getInt(kotlin.Int,%20kotlin.Int)), this method will throw an exception if the attribute is defined but is not an integer.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |
| `defValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value to return if the attribute is not defined or not a resource. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Attribute integer value, or defValue if not defined. |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |
| `java.lang.UnsupportedOperationException` | if the attribute is defined but is not an integer. |

### getLayoutDimension

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLayoutDimension(
    index: Int, 
    defValue: Int
): Int
```

Special version of [getDimensionPixelSize](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getDimensionPixelSize(kotlin.Int,%20kotlin.Int))for retrieving [android.view.ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)'s layout_width and layout_height attributes. This is only here for performance reasons; applications should use [getDimensionPixelSize](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getDimensionPixelSize(kotlin.Int,%20kotlin.Int)).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the attribute to retrieve. |
| `defValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The default value to return if this attribute is not default or contains the wrong type of data. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Attribute dimension value multiplied by the appropriate metric and truncated to integer pixels. |

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### getLayoutDimension

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLayoutDimension(
    index: Int, 
    name: String!
): Int
```

Special version of [getDimensionPixelSize](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getDimensionPixelSize(kotlin.Int,%20kotlin.Int))for retrieving [android.view.ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)'s layout_width and layout_height attributes. This is only here for performance reasons; applications should use [getDimensionPixelSize](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#getDimensionPixelSize(kotlin.Int,%20kotlin.Int)).

This method will throw an exception if the attribute is defined but is not a dimension or integer (enum).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the attribute to retrieve. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Textual name of attribute for error reporting. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Attribute dimension value multiplied by the appropriate metric and truncated to integer pixels. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |
| `java.lang.UnsupportedOperationException` | if the attribute is defined but is not a dimension or integer (enum). |

### getNonResourceString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNonResourceString(index: Int): String!
```

Retrieves the string value for the attribute at index, but only if that string comes from an immediate value in an XML file. That is, this does not allow references to string resources, string attributes, or conversions from other types. As such, this method will only return strings for TypedArray objects that come from attributes in an XML file.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | String holding string data. Any styling information is removed. Returns`null`if the attribute is not defined or is not an immediate string value. |

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### getPositionDescription

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPositionDescription(): String!
```

Returns a message about the parser state suitable for printing error messages.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Human-readable description of current parser state. |

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### getResourceId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResourceId(
    index: Int, 
    defValue: Int
): Int
```

Retrieves the resource identifier for the attribute at index. Note that attribute resource as resolved when the overall [TypedArray](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#) object is retrieved. As a result, this function will return the resource identifier of the final resource value that was found,*not*necessarily the original resource that was specified by the attribute.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |
| `defValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value to return if the attribute is not defined or not a resource. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Attribute resource identifier, or defValue if not defined. |

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### getResources

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResources(): Resources!
```

Returns the Resources object this array was loaded from.

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### getSourceResourceId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSourceResourceId(
    index: Int, 
    defaultValue: Int
): Int
```

Returns the resource ID of the style or layout against which the specified attribute was resolved, otherwise returns defValue. For example, if you we resolving two attributes`android:attribute1`and`android:attribute2`and you were inflating a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) from`layout/my_layout.xml`: 

```kotlin
<View
          style="@style/viewStyle"
          android:layout_width="wrap_content"
          android:layout_height="wrap_content"
          android:attribute1="foo"/>
  
```
and`@style/viewStyle`is: 

```kotlin
<style android:name="viewStyle">
          <item name="android:attribute2">bar<item/>
      <style/>
  
```
then resolved [TypedArray](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#) will have values that return source resource ID of`R.layout.my_layout`for`android:attribute1`and`R.style.viewStyle`for`android:attribute2`.

<br />

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute whose source style to retrieve. |
| `defaultValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value to return if the attribute is not defined or not a resource. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Either a style resource ID, layout resource ID, or defaultValue if it was not resolved in a style or layout. |

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### getString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getString(index: Int): String?
```

Retrieves the string value for the attribute at index.

If the attribute is not a string, this method will attempt to coerce it to a string.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | String holding string data. Any styling information is removed. Returns`null`if the attribute is not defined or could not be coerced to a string. |

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### getText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getText(index: Int): CharSequence!
```

Retrieves the styled string value for the attribute at index.

If the attribute is not a string, this method will attempt to coerce it to a string.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | CharSequence holding string data. May be styled. Returns`null`if the attribute is not defined or could not be coerced to a string. |

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### getTextArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTextArray(index: Int): Array<CharSequence!>!
```

Retrieve the CharSequence\[\] for the attribute at index. This gets the resource ID of the selected attribute, and uses [Resources.getTextArray](https://developer.android.com/reference/kotlin/android/content/res/Resources#getTextArray(kotlin.Int))of the owning Resources object to retrieve its String\[\].

This method will throw an exception if the attribute is defined but is not a text array resource.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>! | CharSequence\[\] for the attribute, or`null`if not defined. |

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### getType

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(index: Int): Int
```

Returns the type of attribute at the specified index.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute whose type to retrieve. |

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Attribute type. |

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(
    index: Int, 
    outValue: TypedValue!
): Boolean
```

Retrieve the raw TypedValue for the attribute at index.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |
| `outValue` | [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)!:TypedValue object in which to place the attribute's data. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the value was retrieved and not @empty,`false`otherwise. |

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### hasValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasValue(index: Int): Boolean
```

Determines whether there is an attribute at index.

**Note:** If the attribute was set to`@empty`or`@undefined`, this method returns`false`.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the attribute has a value, false otherwise. |

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### hasValueOrEmpty

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasValueOrEmpty(index: Int): Boolean
```

Determines whether there is an attribute at index, returning`true`if the attribute was explicitly set to`@empty`and`false`only if the attribute was undefined.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the attribute has a value or is empty, false otherwise. |

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun length(): Int
```

Returns the number of values in this array.

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### peekValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun peekValue(index: Int): TypedValue!
```

Retrieve the raw TypedValue for the attribute at index and return a temporary object holding its data. This object is only valid until the next call on to [TypedArray](https://developer.android.com/reference/kotlin/android/content/res/TypedArray#).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of attribute to retrieve. |

| Return ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)! | Returns a TypedValue object if the attribute is defined, containing its data; otherwise returns null. (You will not receive a TypedValue whose type is TYPE_NULL.) |

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### recycle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun recycle(): Unit
```

Recycles the TypedArray, to be re-used by a later caller. After calling this function you must not ever touch the typed array again.

| Exceptions ||
|------------------------------|----------------------------------------------|
| `java.lang.RuntimeException` | if the TypedArray has already been recycled. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
