# Typeface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Typeface

Kotlin| [Java](../android/graphics/Typeface.md) 
| --- | --- |

```
open class Typeface
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Typeface](../android/graphics/Typeface.md) |

The Typeface class specifies the typeface and intrinsic style of a font. This is used in the paint, along with optionally Paint settings like textSize, textSkewX, textScaleX to specify how text appears when drawn (and measured).

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/graphics/Typeface.Builder.md) A builder class for creating new Typeface instance. |
| | [CustomFallbackBuilder](../android/graphics/Typeface.CustomFallbackBuilder.md) A builder class for creating new Typeface instance. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BOLD](../android/graphics/Typeface.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BOLD_ITALIC](../android/graphics/Typeface.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ITALIC](../android/graphics/Typeface.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NORMAL](../android/graphics/Typeface.md) <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Typeface](../android/graphics/Typeface.md)! | [create](../android/graphics/Typeface.md))`(`family:` ` [Typeface](../android/graphics/Typeface.md)!`, `style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a typeface object that best matches the specified existing typeface and the specified Style. |
| openstatic [Typeface](../android/graphics/Typeface.md) | [create](../android/graphics/Typeface.md))`(`family:` ` [Typeface](../android/graphics/Typeface.md)?`, `weight:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `italic:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a typeface object that best matches the specified existing typeface and the specified weight and italic style |
| openstatic [Typeface](../android/graphics/Typeface.md)! | [create](../android/graphics/Typeface.md))`(`familyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a typeface object given a family name, and option style information. |
| --- | --- |
| openstatic [Typeface](../android/graphics/Typeface.md)! | [createFromAsset](../android/graphics/Typeface.md))`(`mgr:` ` [AssetManager](../android/content/res/AssetManager.md)!`, `path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new typeface from the specified font data. |
| openstatic [Typeface](../android/graphics/Typeface.md)! | [createFromFile](../android/graphics/Typeface.md))`(`file:` ` [File](../java/io/File.md)?`)` Create a new typeface from the specified font file. |
| openstatic [Typeface](../android/graphics/Typeface.md)! | [createFromFile](../android/graphics/Typeface.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Create a new typeface from the specified font file. |
| --- | --- |
| openstatic [Typeface](../android/graphics/Typeface.md)! | [defaultFromStyle](../android/graphics/Typeface.md))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns one of the default typeface objects, based on the specified style |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/graphics/Typeface.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStyle](../android/graphics/Typeface.md))`()` Returns the typeface's intrinsic style attributes |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getSystemFontFamilyName](../android/graphics/Typeface.md))`()` Returns the system font family name if the typeface was created from a system font family, otherwise returns null. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWeight](../android/graphics/Typeface.md))`()` Returns the typeface's weight value |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/graphics/Typeface.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBold](../android/graphics/Typeface.md))`()` Returns true if getStyle() has the BOLD bit set. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isItalic](../android/graphics/Typeface.md))`()` Returns true if getStyle() has the ITALIC bit set. |

| Properties ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Typeface](../android/graphics/Typeface.md)! | [DEFAULT](../android/graphics/Typeface.md) The default NORMAL typeface object |
| static [Typeface](../android/graphics/Typeface.md)! | [DEFAULT_BOLD](../android/graphics/Typeface.md) The default BOLD typeface object. |
| static [Typeface](../android/graphics/Typeface.md)! | [MONOSPACE](../android/graphics/Typeface.md) The NORMAL style of the default monospace typeface. |
| --- | --- |
| static [Typeface](../android/graphics/Typeface.md)! | [SANS_SERIF](../android/graphics/Typeface.md) The NORMAL style of the default sans serif typeface. |
| static [Typeface](../android/graphics/Typeface.md)! | [SERIF](../android/graphics/Typeface.md) The NORMAL style of the default serif typeface. |

## Constants

### BOLD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BOLD: Int
```  

 Value: 1

### BOLD_ITALIC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BOLD_ITALIC: Int
```  

 Value: 3

### ITALIC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ITALIC: Int
```  

 Value: 2

### NORMAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NORMAL: Int
```  

 Value: 0

## Public methods

### create

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    family: Typeface!, 
    style: Int
): Typeface!
```

Create a typeface object that best matches the specified existing typeface and the specified Style. Use this call if you want to pick a new style from the same family of an existing typeface object. If family is null, this selects from the default font's family.

This method is not thread safe on API 27 or before. This method is thread safe on API 28 or after.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `family` | [Typeface](../android/graphics/Typeface.md)!:An existing [Typeface](../android/graphics/Typeface.md) object. In case of`null`, the default typeface is used instead. |
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The style (normal, bold, italic) of the typeface. e.g. NORMAL, BOLD, ITALIC, BOLD_ITALIC Value is [android.graphics.Typeface#NORMAL](../android/graphics/Typeface.md), [android.graphics.Typeface#BOLD](../android/graphics/Typeface.md), [android.graphics.Typeface#ITALIC](../android/graphics/Typeface.md), or [android.graphics.Typeface#BOLD_ITALIC](../android/graphics/Typeface.md) |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Typeface](../android/graphics/Typeface.md)! | The best matching typeface. |

### create

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    family: Typeface?, 
    weight: Int, 
    italic: Boolean
): Typeface
```

Creates a typeface object that best matches the specified existing typeface and the specified weight and italic style

Below are numerical values and corresponding common weight names.

| Value | Common weight name |
|-------|--------------------|
| 100 | Thin |
| 200 | Extra Light |
| 300 | Light |
| --- | --- |
| 400 | Normal |
| 500 | Medium |
| 600 | Semi Bold |
| --- | --- |
| 700 | Bold |
| 800 | Extra Bold |
| 900 | Black |
| --- | --- |

This method is thread safe.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `family` | [Typeface](../android/graphics/Typeface.md)?:An existing [Typeface](../android/graphics/Typeface.md) object. In case of`null`, the default typeface is used instead. |
| `weight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired weight to be drawn. Value is between 1 and 1000 inclusive |
| `italic` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if italic style is desired to be drawn. Otherwise,`false` |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Typeface](../android/graphics/Typeface.md) | A [Typeface](../android/graphics/Typeface.md) object for drawing specified weight and italic style. Never returns`null` |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/Typeface#getWeight()>
- <https://developer.android.com/reference/kotlin/android/graphics/Typeface#isItalic()> 

### create

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    familyName: String!, 
    style: Int
): Typeface!
```

Create a typeface object given a family name, and option style information. If null is passed for the name, then the "default" font will be chosen. The resulting typeface object can be queried (getStyle()) to discover what its "real" style characteristics are.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `familyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:May be null. The name of the font family. |
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The style (normal, bold, italic) of the typeface. e.g. NORMAL, BOLD, ITALIC, BOLD_ITALIC Value is [android.graphics.Typeface#NORMAL](../android/graphics/Typeface.md), [android.graphics.Typeface#BOLD](../android/graphics/Typeface.md), [android.graphics.Typeface#ITALIC](../android/graphics/Typeface.md), or [android.graphics.Typeface#BOLD_ITALIC](../android/graphics/Typeface.md) |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Typeface](../android/graphics/Typeface.md)! | The best matching typeface. |

### createFromAsset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createFromAsset(
    mgr: AssetManager!, 
    path: String!
): Typeface!
```

Create a new typeface from the specified font data.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------|
| `mgr` | [AssetManager](../android/content/res/AssetManager.md)!:The application's asset manager |
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The file name of the font data in the assets directory |

| Return ||
|----------------------------------------------------------------------------------------|-------------------|
| [Typeface](../android/graphics/Typeface.md)! | The new typeface. |

### createFromFile

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createFromFile(file: File?): Typeface!
```

Create a new typeface from the specified font file.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](../java/io/File.md)?:The path to the font data. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------------------|-------------------|
| [Typeface](../android/graphics/Typeface.md)! | The new typeface. |

### createFromFile

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createFromFile(path: String?): Typeface!
```

Create a new typeface from the specified font file.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The full path to the font data. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------------------|-------------------|
| [Typeface](../android/graphics/Typeface.md)! | The new typeface. |

### defaultFromStyle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun defaultFromStyle(style: Int): Typeface!
```

Returns one of the default typeface objects, based on the specified style

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.graphics.Typeface#NORMAL](../android/graphics/Typeface.md), [android.graphics.Typeface#BOLD](../android/graphics/Typeface.md), [android.graphics.Typeface#ITALIC](../android/graphics/Typeface.md), or [android.graphics.Typeface#BOLD_ITALIC](../android/graphics/Typeface.md) |

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------------|
| [Typeface](../android/graphics/Typeface.md)! | the default typeface that corresponds to the style |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getStyle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStyle(): Int
```

Returns the typeface's intrinsic style attributes

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.graphics.Typeface#NORMAL](../android/graphics/Typeface.md), [android.graphics.Typeface#BOLD](../android/graphics/Typeface.md), [android.graphics.Typeface#ITALIC](../android/graphics/Typeface.md), or [android.graphics.Typeface#BOLD_ITALIC](../android/graphics/Typeface.md) |

### getSystemFontFamilyName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSystemFontFamilyName(): String?
```

Returns the system font family name if the typeface was created from a system font family, otherwise returns null. 

### getWeight

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWeight(): Int
```

Returns the typeface's weight value

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between 0 and 1000 inclusive |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isBold

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isBold(): Boolean
```

Returns true if getStyle() has the BOLD bit set. 

### isItalic

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isItalic(): Boolean
```

Returns true if getStyle() has the ITALIC bit set.

## Properties

### DEFAULT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT: Typeface!
```

The default NORMAL typeface object 

### DEFAULT_BOLD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT_BOLD: Typeface!
```

The default BOLD typeface object. Note: this may be not actually be bold, depending on what fonts are installed. Call getStyle() to know for sure. 

### MONOSPACE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MONOSPACE: Typeface!
```

The NORMAL style of the default monospace typeface. 

### SANS_SERIF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SANS_SERIF: Typeface!
```

The NORMAL style of the default sans serif typeface. 

### SERIF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERIF: Typeface!
```

The NORMAL style of the default serif typeface.
