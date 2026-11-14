# FontStyle

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FontStyle

Kotlin| [Java](https://developer.android.com/reference/android/graphics/fonts/FontStyle "View this page in Java") 

```
class FontStyle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.fonts.FontStyle](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#) |

A font style object. This class represents a single font style which is a pair of weight value and slant value. Here are common font styles examples:

<br />

```kotlin
<code>
  final FontStyle NORMAL = new FontStyle(FONT_WEIGHT_NORMAL, FONT_SLANT_UPRIGHT);
  final FontStyle BOLD = new FontStyle(FONT_WEIGHT_BOLD, FONT_SLANT_UPRIGHT);
  final FontStyle ITALIC = new FontStyle(FONT_WEIGHT_NORMAL, FONT_SLANT_ITALIC);
  final FontStyle BOLD_ITALIC = new FontStyle(FONT_WEIGHT_BOLD, FONT_SLANT_ITALIC);
  </code>
```

<br />

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_SLANT_ITALIC](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_SLANT_ITALIC:kotlin.Int) A font slant value for italic |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_SLANT_UPRIGHT](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_SLANT_UPRIGHT:kotlin.Int) A font slant value for upright |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_WEIGHT_BLACK](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_BLACK:kotlin.Int) A font weight value for the black weight |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_WEIGHT_BOLD](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_BOLD:kotlin.Int) A font weight value for the bold weight. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_WEIGHT_EXTRA_BOLD](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_EXTRA_BOLD:kotlin.Int) A font weight value for the extra-bold weight |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_WEIGHT_EXTRA_LIGHT](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_EXTRA_LIGHT:kotlin.Int) A font weight value for the extra-light weight |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_WEIGHT_LIGHT](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_LIGHT:kotlin.Int) A font weight value for the light weight |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_WEIGHT_MAX](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_MAX:kotlin.Int) A maximum weight value for the font |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_WEIGHT_MEDIUM](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_MEDIUM:kotlin.Int) A font weight value for the medium weight |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_WEIGHT_MIN](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_MIN:kotlin.Int) A minimum weight value for the font |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_WEIGHT_NORMAL](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_NORMAL:kotlin.Int) A font weight value for the normal weight |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_WEIGHT_SEMI_BOLD](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_SEMI_BOLD:kotlin.Int) A font weight value for the semi-bold weight |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_WEIGHT_THIN](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_THIN:kotlin.Int) A font weight value for the thin weight |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_WEIGHT_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_UNSPECIFIED:kotlin.Int) A default value when font weight is unspecified |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FontStyle](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FontStyle())`()` <br /> |
| [FontStyle](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FontStyle(kotlin.Int,%20kotlin.Int))`(`weight:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `slant:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create FontStyle with specific weight and italic |

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSlant](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#getSlant())`()` Gets the slant value |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWeight](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#getWeight())`()` Gets the weight value |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#toString())`()` <br /> |

## Constants

### FONT_SLANT_ITALIC

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FONT_SLANT_ITALIC: Int
```

A font slant value for italic 

 Value: 1

### FONT_SLANT_UPRIGHT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FONT_SLANT_UPRIGHT: Int
```

A font slant value for upright 

 Value: 0

### FONT_WEIGHT_BLACK

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FONT_WEIGHT_BLACK: Int
```

A font weight value for the black weight 

 Value: 900

### FONT_WEIGHT_BOLD

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FONT_WEIGHT_BOLD: Int
```

A font weight value for the bold weight. 

 Value: 700

### FONT_WEIGHT_EXTRA_BOLD

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FONT_WEIGHT_EXTRA_BOLD: Int
```

A font weight value for the extra-bold weight 

 Value: 800

### FONT_WEIGHT_EXTRA_LIGHT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FONT_WEIGHT_EXTRA_LIGHT: Int
```

A font weight value for the extra-light weight 

 Value: 200

### FONT_WEIGHT_LIGHT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FONT_WEIGHT_LIGHT: Int
```

A font weight value for the light weight 

 Value: 300

### FONT_WEIGHT_MAX

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FONT_WEIGHT_MAX: Int
```

A maximum weight value for the font 

 Value: 1000

### FONT_WEIGHT_MEDIUM

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FONT_WEIGHT_MEDIUM: Int
```

A font weight value for the medium weight 

 Value: 500

### FONT_WEIGHT_MIN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FONT_WEIGHT_MIN: Int
```

A minimum weight value for the font 

 Value: 1

### FONT_WEIGHT_NORMAL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FONT_WEIGHT_NORMAL: Int
```

A font weight value for the normal weight 

 Value: 400

### FONT_WEIGHT_SEMI_BOLD

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FONT_WEIGHT_SEMI_BOLD: Int
```

A font weight value for the semi-bold weight 

 Value: 600

### FONT_WEIGHT_THIN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FONT_WEIGHT_THIN: Int
```

A font weight value for the thin weight 

 Value: 100

### FONT_WEIGHT_UNSPECIFIED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FONT_WEIGHT_UNSPECIFIED: Int
```

A default value when font weight is unspecified 

 Value: -1

## Public constructors

### FontStyle

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FontStyle()
```  

### FontStyle

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FontStyle(
    weight: Int, 
    slant: Int)
```

Create FontStyle with specific weight and italic

<br />

<br />

| Value | Name | Android Definition |
|-------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| 100 | Thin | [FontStyle.FONT_WEIGHT_THIN](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_THIN:kotlin.Int) |
| 200 | Extra Light (Ultra Light) | [FontStyle.FONT_WEIGHT_EXTRA_LIGHT](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_EXTRA_LIGHT:kotlin.Int) |
| 300 | Light | [FontStyle.FONT_WEIGHT_LIGHT](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_LIGHT:kotlin.Int) |
| 400 | Normal (Regular) | [FontStyle.FONT_WEIGHT_NORMAL](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_NORMAL:kotlin.Int) |
| 500 | Medium | [FontStyle.FONT_WEIGHT_MEDIUM](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_MEDIUM:kotlin.Int) |
| 600 | Semi Bold (Demi Bold) | [FontStyle.FONT_WEIGHT_SEMI_BOLD](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_SEMI_BOLD:kotlin.Int) |
| 700 | Bold | [FontStyle.FONT_WEIGHT_BOLD](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_BOLD:kotlin.Int) |
| 800 | Extra Bold (Ultra Bold) | [FontStyle.FONT_WEIGHT_EXTRA_BOLD](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_EXTRA_BOLD:kotlin.Int) |
| 900 | Black (Heavy) | [FontStyle.FONT_WEIGHT_BLACK](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_BLACK:kotlin.Int) |

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `weight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a weight value |
| `slant` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a slant value Value is [android.graphics.fonts.FontStyle#FONT_SLANT_UPRIGHT](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_SLANT_UPRIGHT:kotlin.Int), or [android.graphics.fonts.FontStyle#FONT_SLANT_ITALIC](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_SLANT_ITALIC:kotlin.Int) |

**See Also**

- [android.graphics.fonts.FontStyle#FONT_WEIGHT_THIN](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_THIN:kotlin.Int)
- [android.graphics.fonts.FontStyle#FONT_WEIGHT_EXTRA_LIGHT](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_EXTRA_LIGHT:kotlin.Int)
- [android.graphics.fonts.FontStyle#FONT_WEIGHT_LIGHT](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_LIGHT:kotlin.Int)
- [android.graphics.fonts.FontStyle#FONT_WEIGHT_NORMAL](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_NORMAL:kotlin.Int)
- [android.graphics.fonts.FontStyle#FONT_WEIGHT_MEDIUM](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_MEDIUM:kotlin.Int)
- [android.graphics.fonts.FontStyle#FONT_WEIGHT_SEMI_BOLD](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_SEMI_BOLD:kotlin.Int)
- [android.graphics.fonts.FontStyle#FONT_WEIGHT_BOLD](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_BOLD:kotlin.Int)
- [android.graphics.fonts.FontStyle#FONT_WEIGHT_EXTRA_BOLD](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_EXTRA_BOLD:kotlin.Int)
- [android.graphics.fonts.FontStyle#FONT_WEIGHT_BLACK](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_WEIGHT_BLACK:kotlin.Int)

## Public methods

### equals

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### getSlant

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSlant(): Int
```

Gets the slant value

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a slant value Value is [android.graphics.fonts.FontStyle#FONT_SLANT_UPRIGHT](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_SLANT_UPRIGHT:kotlin.Int), or [android.graphics.fonts.FontStyle#FONT_SLANT_ITALIC](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FONT_SLANT_ITALIC:kotlin.Int) |

### getWeight

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWeight(): Int
```

Gets the weight value

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a weight value Value is between 0 and 1000 inclusive |

**See Also**

- [#FontStyle(int, int)](https://developer.android.com/reference/kotlin/android/graphics/fonts/FontStyle#FontStyle(kotlin.Int,%20kotlin.Int)) 

### hashCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
