# FontVariationAxis

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FontVariationAxis

Kotlin| [Java](FontVariationAxis.md) 
| --- | --- |

```
class FontVariationAxis
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.fonts.FontVariationAxis](FontVariationAxis.md) |

Class that holds information about single font variation axis.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FontVariationAxis](FontVariationAxis.md))`(`tagString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `styleValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Construct FontVariationAxis. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](FontVariationAxis.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FontVariationAxis](FontVariationAxis.md)!\>? | [fromFontVariationSettings](FontVariationAxis.md))`(`settings:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Construct FontVariationAxis array from font variation settings. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getStyleValue](FontVariationAxis.md))`()` Returns the style value associated to the given axis for this font. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTag](FontVariationAxis.md))`()` Returns the variable font axis tag associated to this axis. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](FontVariationAxis.md))`()` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toFontVariationSettings](FontVariationAxis.md))`(`axes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [FontVariationAxis](FontVariationAxis.md)!>?`)` Stringify the array of FontVariationAxis. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](FontVariationAxis.md))`()` Returns a valid font variation setting string for this object. |

## Public constructors

### FontVariationAxis

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FontVariationAxis(
    tagString: String, 
    styleValue: Float)
```

Construct FontVariationAxis. The axis tag must contain four ASCII characters. Tag string that are longer or shorter than four characters, or contains characters outside of U+0020..U+007E are invalid.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------|
| `tagString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.IllegalArgumentException` | If given tag string is invalid. |

## Public methods

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### fromFontVariationSettings

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromFontVariationSettings(settings: String?): Array<FontVariationAxis!>?
```

Construct FontVariationAxis array from font variation settings. The settings string is constructed from multiple pairs of axis tag and style values. The axis tag must contain four ASCII characters and must be wrapped with single quotes (U+0027) or double quotes (U+0022). Axis strings that are longer or shorter than four characters, or contain characters outside of U+0020..U+007E are invalid. If a specified axis name is not defined in the font, the settings will be ignored. 

```kotlin
FontVariationAxis.fromFontVariationSettings("'wdth' 1.0");
    FontVariationAxis.fromFontVariationSettings("'AX  ' 1.0, 'FB  ' 2.0");
  
```

<br />

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `settings` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:font variation settings. This value may be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [FontVariationAxis](FontVariationAxis.md)!>? | FontVariationAxis\[\] the array of parsed font variation axis.`null`if settings has no font variation settings. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If given string is not a valid font variation settings format. |

### getStyleValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStyleValue(): Float
```

Returns the style value associated to the given axis for this font. 

### getTag

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTag(): String!
```

Returns the variable font axis tag associated to this axis. 

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toFontVariationSettings

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toFontVariationSettings(axes: Array<FontVariationAxis!>?): String
```

Stringify the array of FontVariationAxis.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `axes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FontVariationAxis](FontVariationAxis.md)!\>?:an array of FontVariationAxis. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | String a valid font variation settings string. This value cannot be`null`. |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a valid font variation setting string for this object.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |
