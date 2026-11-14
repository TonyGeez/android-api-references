Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

# RenderParams

```
class RenderParams
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.pdf.RenderParams](RenderParams.md) |

Represents a set of parameters that will be used to render a page of the PDF document.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams.Builder` Builder for constructing `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#FLAG_RENDER_FREETEXT_ANNOTATIONS:kotlin.Int` Flag to enable rendering of freetext annotation on the page. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#FLAG_RENDER_HIGHLIGHT_ANNOTATIONS:kotlin.Int` Flag to enable rendering of highlight annotation on the page. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#FLAG_RENDER_STAMP_ANNOTATIONS:kotlin.Int` Flag to enable rendering of stamp annotation on the page. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#FLAG_RENDER_TEXT_ANNOTATIONS:kotlin.Int` Flag to enable rendering of text annotation on the page. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_FORM_CONTENT_DEFAULT:kotlin.Int` Mode to rely on the default behavior with respect to including PDF form content in rendered PDF bitmaps. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_FORM_CONTENT_DISABLED:kotlin.Int` Mode to exclude PDF form content from rendered PDF bitmaps. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_FORM_CONTENT_ENABLED:kotlin.Int` Mode to include PDF form content in rendered PDF bitmaps. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_MODE_FOR_DISPLAY:kotlin.Int` Mode to render the content for display on a screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_MODE_FOR_PRINT:kotlin.Int` Mode to render the content for printing. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_PAGE_OBJECT_EXCLUDE_IMAGE:kotlin.Int` Flag to exclude `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageImageObject` in the rendered page bitmaps |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_PAGE_OBJECT_EXCLUDE_NONE:kotlin.Int` Flag to include all the page objects in the rendered page bitmaps |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_PAGE_OBJECT_EXCLUDE_PATH:kotlin.Int` Flag to exclude `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject` in the rendered page bitmaps |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_PAGE_OBJECT_EXCLUDE_TEXT:kotlin.Int` Flag to exclude `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject` in the rendered page bitmaps |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#getRenderFlags()()` Returns the bitmask of the render flags. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#getRenderFormContentMode()()` Returns the mode for rendering PDF form content, one of: `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_FORM_CONTENT_ENABLED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_FORM_CONTENT_DISABLED:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_FORM_CONTENT_DEFAULT:kotlin.Int` |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#getRenderMode()()` Returns the render mode. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#getRenderPageObjectFlags()()` Returns the bitmask of the render page object flags. |

## Constants

### FLAG_RENDER_FREETEXT_ANNOTATIONS

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

```
static val FLAG_RENDER_FREETEXT_ANNOTATIONS: Int
```

Flag to enable rendering of freetext annotation on the page.

 Value: 16

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#getRenderFlags()`
- `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams.Builder#setRenderFlags(kotlin.Int)`

### FLAG_RENDER_HIGHLIGHT_ANNOTATIONS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

```
static val FLAG_RENDER_HIGHLIGHT_ANNOTATIONS: Int
```

Flag to enable rendering of highlight annotation on the page.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#getRenderFlags()`
- `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams.Builder#setRenderFlags(kotlin.Int)`

### FLAG_RENDER_STAMP_ANNOTATIONS

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

```
static val FLAG_RENDER_STAMP_ANNOTATIONS: Int
```

Flag to enable rendering of stamp annotation on the page.

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#getRenderFlags()`
- `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams.Builder#setRenderFlags(kotlin.Int)`

### FLAG_RENDER_TEXT_ANNOTATIONS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

```
static val FLAG_RENDER_TEXT_ANNOTATIONS: Int
```

Flag to enable rendering of text annotation on the page.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#getRenderFlags()`
- `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams.Builder#setRenderFlags(kotlin.Int)`

### RENDER_FORM_CONTENT_DEFAULT

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 19](https://developer.android.com/sdkExtensions)

```
static val RENDER_FORM_CONTENT_DEFAULT: Int
```

Mode to rely on the default behavior with respect to including PDF form content in rendered PDF bitmaps.

`https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRenderer` will render form content by default if the application is targeting SDK version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` or higher.

`https://developer.android.com/reference/kotlin/android/graphics/pdf/PdfRendererPreV` will always render form content by default.

 Value: 3

### RENDER_FORM_CONTENT_DISABLED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 19](https://developer.android.com/sdkExtensions)

```
static val RENDER_FORM_CONTENT_DISABLED: Int
```

Mode to exclude PDF form content from rendered PDF bitmaps.

 Value: 2

### RENDER_FORM_CONTENT_ENABLED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 19](https://developer.android.com/sdkExtensions)

```
static val RENDER_FORM_CONTENT_ENABLED: Int
```

Mode to include PDF form content in rendered PDF bitmaps.

 Value: 1

### RENDER_MODE_FOR_DISPLAY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

```
static val RENDER_MODE_FOR_DISPLAY: Int
```

Mode to render the content for display on a screen.

 Value: 1

### RENDER_MODE_FOR_PRINT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

```
static val RENDER_MODE_FOR_PRINT: Int
```

Mode to render the content for printing.

 Value: 2

### RENDER_PAGE_OBJECT_EXCLUDE_IMAGE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 24](https://developer.android.com/sdkExtensions)

```
static val RENDER_PAGE_OBJECT_EXCLUDE_IMAGE: Int
```

Flag to exclude `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageImageObject` in the rendered page bitmaps

 Value: 4

### RENDER_PAGE_OBJECT_EXCLUDE_NONE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 24](https://developer.android.com/sdkExtensions)

```
static val RENDER_PAGE_OBJECT_EXCLUDE_NONE: Int
```

Flag to include all the page objects in the rendered page bitmaps

 Value: 0

### RENDER_PAGE_OBJECT_EXCLUDE_PATH

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 24](https://developer.android.com/sdkExtensions)

```
static val RENDER_PAGE_OBJECT_EXCLUDE_PATH: Int
```

Flag to exclude `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject` in the rendered page bitmaps

 Value: 2

### RENDER_PAGE_OBJECT_EXCLUDE_TEXT

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 24](https://developer.android.com/sdkExtensions)

```
static val RENDER_PAGE_OBJECT_EXCLUDE_TEXT: Int
```

Flag to exclude `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject` in the rendered page bitmaps

 Value: 8

## Public methods

### getRenderFlags

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getRenderFlags(): Int
```

Returns the bitmask of the render flags.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#FLAG_RENDER_TEXT_ANNOTATIONS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#FLAG_RENDER_HIGHLIGHT_ANNOTATIONS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#FLAG_RENDER_STAMP_ANNOTATIONS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#FLAG_RENDER_FREETEXT_ANNOTATIONS:kotlin.Int` |

### getRenderFormContentMode

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 19](https://developer.android.com/sdkExtensions)

```
fun getRenderFormContentMode(): Int
```

Returns the mode for rendering PDF form content, one of: `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_FORM_CONTENT_ENABLED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_FORM_CONTENT_DISABLED:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_FORM_CONTENT_DEFAULT:kotlin.Int`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_FORM_CONTENT_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_FORM_CONTENT_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_FORM_CONTENT_DEFAULT:kotlin.Int` |

### getRenderMode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getRenderMode(): Int
```

Returns the render mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_MODE_FOR_DISPLAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_MODE_FOR_PRINT:kotlin.Int` |

### getRenderPageObjectFlags

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 24](https://developer.android.com/sdkExtensions)

```
fun getRenderPageObjectFlags(): Int
```

Returns the bitmask of the render page object flags.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_PAGE_OBJECT_EXCLUDE_PATH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_PAGE_OBJECT_EXCLUDE_IMAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_PAGE_OBJECT_EXCLUDE_TEXT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/pdf/RenderParams#RENDER_PAGE_OBJECT_EXCLUDE_NONE:kotlin.Int` |

**See Also**
