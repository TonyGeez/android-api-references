Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

# StampAnnotation

Kotlin | [Java](StampAnnotation.md)
| --- | --- |

```
class StampAnnotation : PdfAnnotation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.pdf.component.PdfAnnotation](PdfAnnotation.md) ||
| | ↳ | [android.graphics.pdf.component.StampAnnotation](StampAnnotation.md) |

Represents a stamp annotation in a PDF document.

Only path, image, or text objects created using the `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject`, `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageImageObject`, or `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject` constructors respectively can be added to a stamp annotation.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/StampAnnotation#StampAnnotation(android.graphics.RectF)(bounds: https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)` Creates a new stamp annotation with the specified bounds. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/StampAnnotation#addObject(android.graphics.pdf.component.PdfPageObject)(pageObject: https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject)` Adds a PDF page object to the stamp annotation. |
| [RectF](../android.graphics/RectF.md) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/StampAnnotation#getBounds()()` Returns the bounding rectangle of the stamp annotation. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PdfPageObject](PdfPageObject.md)!\> | `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/StampAnnotation#getObjects()()` Returns all the known PDF page objects in the stamp annotation. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/StampAnnotation#removeObject(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Remove the page object at the given index inside the stamp annotation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/StampAnnotation#setBounds(android.graphics.RectF)(bounds: https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)` Sets the bounding rectangle of the stamp annotation. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfAnnotation` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfAnnotation#getPdfAnnotationType()()` Returns the type of the annotation. <br /> | ||

## Public constructors

### StampAnnotation

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

```
StampAnnotation(bounds: RectF)
```

Creates a new stamp annotation with the specified bounds.

The list of page objects inside the stamp annotation will be empty by default

| Parameters ||
|---|---|
| `bounds` | [RectF](../android.graphics/RectF.md): The bounding rectangle of the annotation. This value cannot be `null`. |

## Public methods

### addObject

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

```
fun addObject(pageObject: PdfPageObject): Unit
```

Adds a PDF page object to the stamp annotation.

The page object should be a path, text or an image.

| Parameters ||
|---|---|
| `pageObject` | [PdfPageObject](PdfPageObject.md): The PDF page object to add. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the page object is already added to a page or an annotation. |

### getBounds

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

```
fun getBounds(): RectF
```

Returns the bounding rectangle of the stamp annotation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#` | The bounding rectangle. This value cannot be `null`. |

### getObjects

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

```
fun getObjects(): MutableList<PdfPageObject!>
```

Returns all the known PDF page objects in the stamp annotation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject!>` | The list of page objects in the annotation. This value cannot be `null`. |

### removeObject

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

```
fun removeObject(index: Int): Unit
```

Remove the page object at the given index inside the stamp annotation. Here index is the index of the page object in the list of page objects returned by `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/StampAnnotation#getObjects()`

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): - index of the object to be removed. Value is 0 or greater |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if there is no object in the annotation with the given id |

### setBounds

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

```
fun setBounds(bounds: RectF): Unit
```

Sets the bounding rectangle of the stamp annotation.

| Parameters ||
|---|---|
| `bounds` | [RectF](../android.graphics/RectF.md): The new bounding rectangle. This value cannot be `null`. |
