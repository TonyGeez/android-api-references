# Html

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Html

Kotlin| [Java](../android/text/Html.md) 
| --- | --- |

```
open class Html
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.Html](../android/text/Html.md) |

This class processes HTML strings into displayable styled text. Not all HTML tags are supported.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [ImageGetter](../android/text/Html.ImageGetter.md) Retrieves images for HTML \<img\> tags. |
| abstract | [TagHandler](../android/text/Html.TagHandler.md) Is notified when HTML tags are encountered that the parser does not know how to interpret. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_HTML_MODE_COMPACT](../android/text/Html.md) Flags for [fromHtml(java.lang.String,int,android.text.Html.ImageGetter,android.text.Html.TagHandler)](../android/text/Html.md)): Separate block-level elements with line breaks (single newline character) in between. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_HTML_MODE_LEGACY](../android/text/Html.md) Flags for [fromHtml(java.lang.String,int,android.text.Html.ImageGetter,android.text.Html.TagHandler)](../android/text/Html.md)): Separate block-level elements with blank lines (two newline characters) in between. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_HTML_OPTION_USE_CSS_COLORS](../android/text/Html.md) Flag indicating that CSS color values should be used instead of those defined in [Color](../android/graphics/Color.md). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_HTML_SEPARATOR_LINE_BREAK_BLOCKQUOTE](../android/text/Html.md) Flag indicating that texts inside \<blockquote\> elements will be separated from other texts with one newline character by default. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_HTML_SEPARATOR_LINE_BREAK_DIV](../android/text/Html.md) Flag indicating that texts inside \<div\> elements will be separated from other texts with one newline character by default. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_HTML_SEPARATOR_LINE_BREAK_HEADING](../android/text/Html.md) Flag indicating that texts inside \<h1\>\~\<h6\> elements will be separated from other texts with one newline character by default. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_HTML_SEPARATOR_LINE_BREAK_LIST](../android/text/Html.md) Flag indicating that texts inside \<ul\> elements will be separated from other texts with one newline character by default. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_HTML_SEPARATOR_LINE_BREAK_LIST_ITEM](../android/text/Html.md) Flag indicating that texts inside \<li\> elements will be separated from other texts with one newline character by default. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_HTML_SEPARATOR_LINE_BREAK_PARAGRAPH](../android/text/Html.md) Flag indicating that texts inside \<p\> elements will be separated from other texts with one newline character by default. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TO_HTML_PARAGRAPH_LINES_CONSECUTIVE](../android/text/Html.md) Option for [toHtml(android.text.Spanned,int)](../android/text/Html.md)): Wrap consecutive lines of text delimited by '\\n' inside \<p\> elements. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TO_HTML_PARAGRAPH_LINES_INDIVIDUAL](../android/text/Html.md) Option for [toHtml(android.text.Spanned,int)](../android/text/Html.md)): Wrap each line of text delimited by '\\n' inside a \<p\> or a \<li\> element. |

| Public methods ||
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [escapeHtml](../android/text/Html.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Returns an HTML escaped representation of the given plain text. |
| openstatic [Spanned](../android/text/Spanned.md)! | [fromHtml](../android/text/Html.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns displayable styled text from the provided HTML string with the legacy flags [FROM_HTML_MODE_LEGACY](../android/text/Html.md). |
| openstatic [Spanned](../android/text/Spanned.md)! | [fromHtml](../android/text/Html.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `imageGetter:` ` [Html.ImageGetter](../android/text/Html.ImageGetter.md)!`, `tagHandler:` ` [Html.TagHandler](../android/text/Html.TagHandler.md)!`)` Returns displayable styled text from the provided HTML string with the legacy flags [FROM_HTML_MODE_LEGACY](../android/text/Html.md). |
| --- | --- |
| openstatic [Spanned](../android/text/Spanned.md)! | [fromHtml](../android/text/Html.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns displayable styled text from the provided HTML string. |
| openstatic [Spanned](../android/text/Spanned.md)! | [fromHtml](../android/text/Html.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `imageGetter:` ` [Html.ImageGetter](../android/text/Html.ImageGetter.md)!`, `tagHandler:` ` [Html.TagHandler](../android/text/Html.TagHandler.md)!`)` Returns displayable styled text from the provided HTML string. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toHtml](../android/text/Html.md))`(`text:` ` [Spanned](../android/text/Spanned.md)!`)` <br /> |
| --- | --- |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toHtml](../android/text/Html.md))`(`text:` ` [Spanned](../android/text/Spanned.md)!`, `option:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns an HTML representation of the provided Spanned text. |

## Constants

### FROM_HTML_MODE_COMPACT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FROM_HTML_MODE_COMPACT: Int
```

Flags for [fromHtml(java.lang.String,int,android.text.Html.ImageGetter,android.text.Html.TagHandler)](../android/text/Html.md)): Separate block-level elements with line breaks (single newline character) in between. This inverts the [Spanned](../android/text/Spanned.md) to HTML string conversion done with the option [TO_HTML_PARAGRAPH_LINES_INDIVIDUAL](../android/text/Html.md). 

 Value: 63

### FROM_HTML_MODE_LEGACY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FROM_HTML_MODE_LEGACY: Int
```

Flags for [fromHtml(java.lang.String,int,android.text.Html.ImageGetter,android.text.Html.TagHandler)](../android/text/Html.md)): Separate block-level elements with blank lines (two newline characters) in between. This is the legacy behavior prior to N. 

 Value: 0

### FROM_HTML_OPTION_USE_CSS_COLORS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FROM_HTML_OPTION_USE_CSS_COLORS: Int
```

Flag indicating that CSS color values should be used instead of those defined in [Color](../android/graphics/Color.md). 

 Value: 256

### FROM_HTML_SEPARATOR_LINE_BREAK_BLOCKQUOTE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FROM_HTML_SEPARATOR_LINE_BREAK_BLOCKQUOTE: Int
```

Flag indicating that texts inside \<blockquote\> elements will be separated from other texts with one newline character by default. 

 Value: 32

### FROM_HTML_SEPARATOR_LINE_BREAK_DIV

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FROM_HTML_SEPARATOR_LINE_BREAK_DIV: Int
```

Flag indicating that texts inside \<div\> elements will be separated from other texts with one newline character by default. 

 Value: 16

### FROM_HTML_SEPARATOR_LINE_BREAK_HEADING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FROM_HTML_SEPARATOR_LINE_BREAK_HEADING: Int
```

Flag indicating that texts inside \<h1\>\~\<h6\> elements will be separated from other texts with one newline character by default. 

 Value: 2

### FROM_HTML_SEPARATOR_LINE_BREAK_LIST

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FROM_HTML_SEPARATOR_LINE_BREAK_LIST: Int
```

Flag indicating that texts inside \<ul\> elements will be separated from other texts with one newline character by default. 

 Value: 8

### FROM_HTML_SEPARATOR_LINE_BREAK_LIST_ITEM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FROM_HTML_SEPARATOR_LINE_BREAK_LIST_ITEM: Int
```

Flag indicating that texts inside \<li\> elements will be separated from other texts with one newline character by default. 

 Value: 4

### FROM_HTML_SEPARATOR_LINE_BREAK_PARAGRAPH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FROM_HTML_SEPARATOR_LINE_BREAK_PARAGRAPH: Int
```

Flag indicating that texts inside \<p\> elements will be separated from other texts with one newline character by default. 

 Value: 1

### TO_HTML_PARAGRAPH_LINES_CONSECUTIVE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TO_HTML_PARAGRAPH_LINES_CONSECUTIVE: Int
```

Option for [toHtml(android.text.Spanned,int)](../android/text/Html.md)): Wrap consecutive lines of text delimited by '\\n' inside \<p\> elements. [BulletSpan](../android/text/style/BulletSpan.md) s are ignored. 

 Value: 0

### TO_HTML_PARAGRAPH_LINES_INDIVIDUAL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TO_HTML_PARAGRAPH_LINES_INDIVIDUAL: Int
```

Option for [toHtml(android.text.Spanned,int)](../android/text/Html.md)): Wrap each line of text delimited by '\\n' inside a \<p\> or a \<li\> element. This allows [ParagraphStyle](../android/text/style/ParagraphStyle.md) s attached to be encoded as CSS styles within the corresponding \<p\> or \<li\> element. 

 Value: 1

## Public methods

### escapeHtml

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun escapeHtml(text: CharSequence!): String!
```

Returns an HTML escaped representation of the given plain text. 

### fromHtml

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fromHtml(source: String!): Spanned!
```

**Deprecated:** *use [fromHtml(java.lang.String,int)](../android/text/Html.md))instead.*

Returns displayable styled text from the provided HTML string with the legacy flags [FROM_HTML_MODE_LEGACY](../android/text/Html.md). 

### fromHtml

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fromHtml(
    source: String!, 
    imageGetter: Html.ImageGetter!, 
    tagHandler: Html.TagHandler!
): Spanned!
```

**Deprecated:** *use [fromHtml(java.lang.String,int,android.text.Html.ImageGetter,android.text.Html.TagHandler)](../android/text/Html.md))instead.*

Returns displayable styled text from the provided HTML string with the legacy flags [FROM_HTML_MODE_LEGACY](../android/text/Html.md). 

### fromHtml

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fromHtml(
    source: String!, 
    flags: Int
): Spanned!
```

Returns displayable styled text from the provided HTML string. Any \<img\> tags in the HTML will display as a generic replacement image which your program can then go through and replace with real images.

This uses TagSoup to handle real HTML, including all of the brokenness found in the wild. 

### fromHtml

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fromHtml(
    source: String!, 
    flags: Int, 
    imageGetter: Html.ImageGetter!, 
    tagHandler: Html.TagHandler!
): Spanned!
```

Returns displayable styled text from the provided HTML string. Any \<img\> tags in the HTML will use the specified ImageGetter to request a representation of the image (use null if you don't want this) and the specified TagHandler to handle unknown tags (specify null if you don't want this).

This uses TagSoup to handle real HTML, including all of the brokenness found in the wild. 

### toHtml

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun toHtml(text: Spanned!): String!
```

**Deprecated:** *use [toHtml(android.text.Spanned,int)](../android/text/Html.md))instead.* 

### toHtml

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun toHtml(
    text: Spanned!, 
    option: Int
): String!
```

Returns an HTML representation of the provided Spanned text. A best effort is made to add HTML tags corresponding to spans. Also note that HTML metacharacters (such as "\<" and "\&") within the input text are escaped.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [Spanned](../android/text/Spanned.md)!:input text to convert |
| `option` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [TO_HTML_PARAGRAPH_LINES_CONSECUTIVE](../android/text/Html.md) or [TO_HTML_PARAGRAPH_LINES_INDIVIDUAL](../android/text/Html.md) |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | string containing input converted to HTML |
