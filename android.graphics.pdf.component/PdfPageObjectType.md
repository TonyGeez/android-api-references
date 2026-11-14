# PdfPageObjectType

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

# PdfPageObjectType

Kotlin| [Java](../android/graphics/pdf/component/PdfPageObjectType.md) 
| --- | --- |

```
class PdfPageObjectType
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.pdf.component.PdfPageObjectType](../android/graphics/pdf/component/PdfPageObjectType.md) |

This class holds the set of constants representing the types of a PDF page objects.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IMAGE](../android/graphics/pdf/component/PdfPageObjectType.md) Represents an image page object |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PATH](../android/graphics/pdf/component/PdfPageObjectType.md) Represents a path page object |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TEXT](../android/graphics/pdf/component/PdfPageObjectType.md) Represents a text page object |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNKNOWN](../android/graphics/pdf/component/PdfPageObjectType.md) Represents the type of page object that cannot be determined |

| Public methods ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValidType](../android/graphics/pdf/component/PdfPageObjectType.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks if the given type is a valid PDF page object type. |

## Constants

### IMAGE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
static val IMAGE: Int
```

Represents an image page object 

 Value: 3

### PATH

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
static val PATH: Int
```

Represents a path page object 

 Value: 2

### TEXT

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
static val TEXT: Int
```

Represents a text page object 

 Value: 1

### UNKNOWN

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
static val UNKNOWN: Int
```

Represents the type of page object that cannot be determined 

 Value: 0

## Public methods

### isValidType

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
static fun isValidType(type: Int): Boolean
```

Checks if the given type is a valid PDF page object type.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type to check. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the type is valid,`false`otherwise. |
