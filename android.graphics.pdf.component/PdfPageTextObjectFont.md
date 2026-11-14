# PdfPageTextObjectFont

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

# PdfPageTextObjectFont

Kotlin| [Java](https://developer.android.com/reference/android/graphics/pdf/component/PdfPageTextObjectFont "View this page in Java") 

```
open class PdfPageTextObjectFont
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.pdf.component.PdfPageTextObjectFont](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#) |

Represents the font attributes of a [PdfPageTextObject](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject). This class encapsulates the attributes font family, boldness and italic styling.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_FAMILY_COURIER](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#FONT_FAMILY_COURIER:kotlin.Int) Constant representing the Courier font family. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_FAMILY_HELVETICA](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#FONT_FAMILY_HELVETICA:kotlin.Int) Constant representing the Helvetica font family. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_FAMILY_SYMBOL](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#FONT_FAMILY_SYMBOL:kotlin.Int) Constant representing the Symbol font family. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FONT_FAMILY_TIMES_NEW_ROMAN](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#FONT_FAMILY_TIMES_NEW_ROMAN:kotlin.Int) Constant representing the Times New Roman font family. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PdfPageTextObjectFont](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#PdfPageTextObjectFont(android.graphics.pdf.component.PdfPageTextObjectFont))`(`font:` ` [PdfPageTextObjectFont](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#)`)` Creates a new [PdfPageTextObjectFont](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#) by copying attributes from the another [PdfPageTextObjectFont](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#) instance. |
| [PdfPageTextObjectFont](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#PdfPageTextObjectFont(kotlin.Int,%20kotlin.Boolean,%20kotlin.Boolean))`(`fontFamily:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isBold:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `isItalic:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructs a new [PdfPageTextObjectFont](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#) with the specified attributes. |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFontFamily](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#getFontFamily())`()` Returns the font-family which is of type android. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBold](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#isBold())`()` Determines if the text is bold. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isItalic](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#isItalic())`()` Determines if the text is italic. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBold](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#setBold(kotlin.Boolean))`(`bold:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the text should be bold or not. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFontFamily](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#setFontFamily(kotlin.Int))`(`fontFamily:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the font family of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setItalic](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#setItalic(kotlin.Boolean))`(`italic:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether the text should be italic or not. |

## Constants

### FONT_FAMILY_COURIER

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
static val FONT_FAMILY_COURIER: Int
```

Constant representing the Courier font family. 

 Value: 0

### FONT_FAMILY_HELVETICA

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
static val FONT_FAMILY_HELVETICA: Int
```

Constant representing the Helvetica font family. 

 Value: 1

### FONT_FAMILY_SYMBOL

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
static val FONT_FAMILY_SYMBOL: Int
```

Constant representing the Symbol font family. Note: This font family only renders symbols and does not support bold or italic. 

 Value: 2

### FONT_FAMILY_TIMES_NEW_ROMAN

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
static val FONT_FAMILY_TIMES_NEW_ROMAN: Int
```

Constant representing the Times New Roman font family. 

 Value: 3

## Public constructors

### PdfPageTextObjectFont

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
PdfPageTextObjectFont(font: PdfPageTextObjectFont)
```

Creates a new [PdfPageTextObjectFont](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#) by copying attributes from the another [PdfPageTextObjectFont](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#) instance.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `font` | [PdfPageTextObjectFont](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#):The [PdfPageTextObjectFont](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#) instance to copy attributes from. This value cannot be`null`. |

### PdfPageTextObjectFont

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
PdfPageTextObjectFont(
    fontFamily: Int, 
    isBold: Boolean, 
    isItalic: Boolean)
```

Constructs a new [PdfPageTextObjectFont](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#) with the specified attributes.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fontFamily` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The font family, as defined by android.graphics.pdf.component.PdfPageTextObjectFont.FontFamily Value is [android.graphics.pdf.component.PdfPageTextObjectFont#FONT_FAMILY_COURIER](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#FONT_FAMILY_COURIER:kotlin.Int), [android.graphics.pdf.component.PdfPageTextObjectFont#FONT_FAMILY_HELVETICA](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#FONT_FAMILY_HELVETICA:kotlin.Int), [android.graphics.pdf.component.PdfPageTextObjectFont#FONT_FAMILY_SYMBOL](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#FONT_FAMILY_SYMBOL:kotlin.Int), or [android.graphics.pdf.component.PdfPageTextObjectFont#FONT_FAMILY_TIMES_NEW_ROMAN](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#FONT_FAMILY_TIMES_NEW_ROMAN:kotlin.Int) |
| `isBold` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the text should be bold, false otherwise |
| `isItalic` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the text should be italic, false otherwise |

## Public methods

### getFontFamily

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
open fun getFontFamily(): Int
```

Returns the font-family which is of type android.graphics.pdf.component.PdfPageTextObjectFont.FontFamily, previously set using [PdfPageTextObjectFont.setFontFamily(int)](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#setFontFamily(kotlin.Int))or the constructor.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The font-family. Value is [android.graphics.pdf.component.PdfPageTextObjectFont#FONT_FAMILY_COURIER](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#FONT_FAMILY_COURIER:kotlin.Int), [android.graphics.pdf.component.PdfPageTextObjectFont#FONT_FAMILY_HELVETICA](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#FONT_FAMILY_HELVETICA:kotlin.Int), [android.graphics.pdf.component.PdfPageTextObjectFont#FONT_FAMILY_SYMBOL](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#FONT_FAMILY_SYMBOL:kotlin.Int), or [android.graphics.pdf.component.PdfPageTextObjectFont#FONT_FAMILY_TIMES_NEW_ROMAN](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#FONT_FAMILY_TIMES_NEW_ROMAN:kotlin.Int) |

### isBold

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
open fun isBold(): Boolean
```

Determines if the text is bold.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the text is bold, false otherwise. |

### isItalic

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
open fun isItalic(): Boolean
```

Determines if the text is italic.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the text is italic, false otherwise. |

### setBold

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
open fun setBold(bold: Boolean): Unit
```

Sets whether the text should be bold or not.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------|
| `bold` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the text should be bold, false otherwise. |

### setFontFamily

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
open fun setFontFamily(fontFamily: Int): Unit
```

Set the font family of the object.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fontFamily` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The font family to be set. Value is [android.graphics.pdf.component.PdfPageTextObjectFont#FONT_FAMILY_COURIER](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#FONT_FAMILY_COURIER:kotlin.Int), [android.graphics.pdf.component.PdfPageTextObjectFont#FONT_FAMILY_HELVETICA](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#FONT_FAMILY_HELVETICA:kotlin.Int), [android.graphics.pdf.component.PdfPageTextObjectFont#FONT_FAMILY_SYMBOL](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#FONT_FAMILY_SYMBOL:kotlin.Int), or [android.graphics.pdf.component.PdfPageTextObjectFont#FONT_FAMILY_TIMES_NEW_ROMAN](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont#FONT_FAMILY_TIMES_NEW_ROMAN:kotlin.Int) |

### setItalic

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
open fun setItalic(italic: Boolean): Unit
```

Set whether the text should be italic or not.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `italic` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the text should be italic, false otherwise. |
