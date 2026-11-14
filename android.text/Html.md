# Html

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Html

Kotlin| [Java](https://developer.android.com/reference/android/text/Html "View this page in Java") 
| --- | --- |

```
open class Html
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.Html](https://developer.android.com/reference/kotlin/android/text/Html#) |

This class processes HTML strings into displayable styled text. Not all HTML tags are supported.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [ImageGetter](https://developer.android.com/reference/kotlin/android/text/Html.ImageGetter) Retrieves images for HTML \<img\> tags. |
| abstract | [TagHandler](https://developer.android.com/reference/kotlin/android/text/Html.TagHandler) Is notified when HTML tags are encountered that the parser does not know how to interpret. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_HTML_MODE_COMPACT](https://developer.android.com/reference/kotlin/android/text/Html#FROM_HTML_MODE_COMPACT:kotlin.Int) Flags for [fromHtml(java.lang.String,int,android.text.Html.ImageGetter,android.text.Html.TagHandler)](https://developer.android.com/reference/kotlin/android/text/Html#fromHtml(kotlin.String,%20kotlin.Int,%20android.text.Html.ImageGetter,%20android.text.Html.TagHandler)): Separate block-level elements with line breaks (single newline character) in between. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_HTML_MODE_LEGACY](https://developer.android.com/reference/kotlin/android/text/Html#FROM_HTML_MODE_LEGACY:kotlin.Int) Flags for [fromHtml(java.lang.String,int,android.text.Html.ImageGetter,android.text.Html.TagHandler)](https://developer.android.com/reference/kotlin/android/text/Html#fromHtml(kotlin.String,%20kotlin.Int,%20android.text.Html.ImageGetter,%20android.text.Html.TagHandler)): Separate block-level elements with blank lines (two newline characters) in between. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_HTML_OPTION_USE_CSS_COLORS](https://developer.android.com/reference/kotlin/android/text/Html#FROM_HTML_OPTION_USE_CSS_COLORS:kotlin.Int) Flag indicating that CSS color values should be used instead of those defined in [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_HTML_SEPARATOR_LINE_BREAK_BLOCKQUOTE](https://developer.android.com/reference/kotlin/android/text/Html#FROM_HTML_SEPARATOR_LINE_BREAK_BLOCKQUOTE:kotlin.Int) Flag indicating that texts inside \<blockquote\> elements will be separated from other texts with one newline character by default. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_HTML_SEPARATOR_LINE_BREAK_DIV](https://developer.android.com/reference/kotlin/android/text/Html#FROM_HTML_SEPARATOR_LINE_BREAK_DIV:kotlin.Int) Flag indicating that texts inside \<div\> elements will be separated from other texts with one newline character by default. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_HTML_SEPARATOR_LINE_BREAK_HEADING](https://developer.android.com/reference/kotlin/android/text/Html#FROM_HTML_SEPARATOR_LINE_BREAK_HEADING:kotlin.Int) Flag indicating that texts inside \<h1\>\~\<h6\> elements will be separated from other texts with one newline character by default. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_HTML_SEPARATOR_LINE_BREAK_LIST](https://developer.android.com/reference/kotlin/android/text/Html#FROM_HTML_SEPARATOR_LINE_BREAK_LIST:kotlin.Int) Flag indicating that texts inside \<ul\> elements will be separated from other texts with one newline character by default. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_HTML_SEPARATOR_LINE_BREAK_LIST_ITEM](https://developer.android.com/reference/kotlin/android/text/Html#FROM_HTML_SEPARATOR_LINE_BREAK_LIST_ITEM:kotlin.Int) Flag indicating that texts inside \<li\> elements will be separated from other texts with one newline character by default. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FROM_HTML_SEPARATOR_LINE_BREAK_PARAGRAPH](https://developer.android.com/reference/kotlin/android/text/Html#FROM_HTML_SEPARATOR_LINE_BREAK_PARAGRAPH:kotlin.Int) Flag indicating that texts inside \<p\> elements will be separated from other texts with one newline character by default. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TO_HTML_PARAGRAPH_LINES_CONSECUTIVE](https://developer.android.com/reference/kotlin/android/text/Html#TO_HTML_PARAGRAPH_LINES_CONSECUTIVE:kotlin.Int) Option for [toHtml(android.text.Spanned,int)](https://developer.android.com/reference/kotlin/android/text/Html#toHtml(android.text.Spanned,%20kotlin.Int)): Wrap consecutive lines of text delimited by '\\n' inside \<p\> elements. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TO_HTML_PARAGRAPH_LINES_INDIVIDUAL](https://developer.android.com/reference/kotlin/android/text/Html#TO_HTML_PARAGRAPH_LINES_INDIVIDUAL:kotlin.Int) Option for [toHtml(android.text.Spanned,int)](https://developer.android.com/reference/kotlin/android/text/Html#toHtml(android.text.Spanned,%20kotlin.Int)): Wrap each line of text delimited by '\\n' inside a \<p\> or a \<li\> element. |

| Public methods ||
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [escapeHtml](https://developer.android.com/reference/kotlin/android/text/Html#escapeHtml(kotlin.CharSequence))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Returns an HTML escaped representation of the given plain text. |
| openstatic [Spanned](https://developer.android.com/reference/kotlin/android/text/Spanned)! | [fromHtml](https://developer.android.com/reference/kotlin/android/text/Html#fromHtml(kotlin.String))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns displayable styled text from the provided HTML string with the legacy flags [FROM_HTML_MODE_LEGACY](https://developer.android.com/reference/kotlin/android/text/Html#FROM_HTML_MODE_LEGACY:kotlin.Int). |
| openstatic [Spanned](https://developer.android.com/reference/kotlin/android/text/Spanned)! | [fromHtml](https://developer.android.com/reference/kotlin/android/text/Html#fromHtml(kotlin.String,%20android.text.Html.ImageGetter,%20android.text.Html.TagHandler))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `imageGetter:` ` [Html.ImageGetter](https://developer.android.com/reference/kotlin/android/text/Html.ImageGetter)!`, `tagHandler:` ` [Html.TagHandler](https://developer.android.com/reference/kotlin/android/text/Html.TagHandler)!`)` Returns displayable styled text from the provided HTML string with the legacy flags [FROM_HTML_MODE_LEGACY](https://developer.android.com/reference/kotlin/android/text/Html#FROM_HTML_MODE_LEGACY:kotlin.Int). |
| --- | --- |
| openstatic [Spanned](https://developer.android.com/reference/kotlin/android/text/Spanned)! | [fromHtml](https://developer.android.com/reference/kotlin/android/text/Html#fromHtml(kotlin.String,%20kotlin.Int))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns displayable styled text from the provided HTML string. |
| openstatic [Spanned](https://developer.android.com/reference/kotlin/android/text/Spanned)! | [fromHtml](https://developer.android.com/reference/kotlin/android/text/Html#fromHtml(kotlin.String,%20kotlin.Int,%20android.text.Html.ImageGetter,%20android.text.Html.TagHandler))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `imageGetter:` ` [Html.ImageGetter](https://developer.android.com/reference/kotlin/android/text/Html.ImageGetter)!`, `tagHandler:` ` [Html.TagHandler](https://developer.android.com/reference/kotlin/android/text/Html.TagHandler)!`)` Returns displayable styled text from the provided HTML string. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toHtml](https://developer.android.com/reference/kotlin/android/text/Html#toHtml(android.text.Spanned))`(`text:` ` [Spanned](https://developer.android.com/reference/kotlin/android/text/Spanned)!`)` <br /> |
| --- | --- |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toHtml](https://developer.android.com/reference/kotlin/android/text/Html#toHtml(android.text.Spanned,%20kotlin.Int))`(`text:` ` [Spanned](https://developer.android.com/reference/kotlin/android/text/Spanned)!`, `option:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns an HTML representation of the provided Spanned text. |

## Constants

### FROM_HTML_MODE_COMPACT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FROM_HTML_MODE_COMPACT: Int
```

Flags for [fromHtml(java.lang.String,int,android.text.Html.ImageGetter,android.text.Html.TagHandler)](https://developer.android.com/reference/kotlin/android/text/Html#fromHtml(kotlin.String,%20kotlin.Int,%20android.text.Html.ImageGetter,%20android.text.Html.TagHandler)): Separate block-level elements with line breaks (single newline character) in between. This inverts the [Spanned](https://developer.android.com/reference/kotlin/android/text/Spanned) to HTML string conversion done with the option [TO_HTML_PARAGRAPH_LINES_INDIVIDUAL](https://developer.android.com/reference/kotlin/android/text/Html#TO_HTML_PARAGRAPH_LINES_INDIVIDUAL:kotlin.Int). 

 Value: 63

### FROM_HTML_MODE_LEGACY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FROM_HTML_MODE_LEGACY: Int
```

Flags for [fromHtml(java.lang.String,int,android.text.Html.ImageGetter,android.text.Html.TagHandler)](https://developer.android.com/reference/kotlin/android/text/Html#fromHtml(kotlin.String,%20kotlin.Int,%20android.text.Html.ImageGetter,%20android.text.Html.TagHandler)): Separate block-level elements with blank lines (two newline characters) in between. This is the legacy behavior prior to N. 

 Value: 0

### FROM_HTML_OPTION_USE_CSS_COLORS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FROM_HTML_OPTION_USE_CSS_COLORS: Int
```

Flag indicating that CSS color values should be used instead of those defined in [Color](https://developer.android.com/reference/kotlin/android/graphics/Color.html#). 

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

Option for [toHtml(android.text.Spanned,int)](https://developer.android.com/reference/kotlin/android/text/Html#toHtml(android.text.Spanned,%20kotlin.Int)): Wrap consecutive lines of text delimited by '\\n' inside \<p\> elements. [BulletSpan](https://developer.android.com/reference/kotlin/android/text/style/BulletSpan) s are ignored. 

 Value: 0

### TO_HTML_PARAGRAPH_LINES_INDIVIDUAL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TO_HTML_PARAGRAPH_LINES_INDIVIDUAL: Int
```

Option for [toHtml(android.text.Spanned,int)](https://developer.android.com/reference/kotlin/android/text/Html#toHtml(android.text.Spanned,%20kotlin.Int)): Wrap each line of text delimited by '\\n' inside a \<p\> or a \<li\> element. This allows [ParagraphStyle](https://developer.android.com/reference/kotlin/android/text/style/ParagraphStyle) s attached to be encoded as CSS styles within the corresponding \<p\> or \<li\> element. 

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

**Deprecated:** *use [fromHtml(java.lang.String,int)](https://developer.android.com/reference/kotlin/android/text/Html#fromHtml(kotlin.String,%20kotlin.Int))instead.*

Returns displayable styled text from the provided HTML string with the legacy flags [FROM_HTML_MODE_LEGACY](https://developer.android.com/reference/kotlin/android/text/Html#FROM_HTML_MODE_LEGACY:kotlin.Int). 

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

**Deprecated:** *use [fromHtml(java.lang.String,int,android.text.Html.ImageGetter,android.text.Html.TagHandler)](https://developer.android.com/reference/kotlin/android/text/Html#fromHtml(kotlin.String,%20kotlin.Int,%20android.text.Html.ImageGetter,%20android.text.Html.TagHandler))instead.*

Returns displayable styled text from the provided HTML string with the legacy flags [FROM_HTML_MODE_LEGACY](https://developer.android.com/reference/kotlin/android/text/Html#FROM_HTML_MODE_LEGACY:kotlin.Int). 

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

**Deprecated:** *use [toHtml(android.text.Spanned,int)](https://developer.android.com/reference/kotlin/android/text/Html#toHtml(android.text.Spanned,%20kotlin.Int))instead.* 

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
| `text` | [Spanned](https://developer.android.com/reference/kotlin/android/text/Spanned)!:input text to convert |
| `option` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [TO_HTML_PARAGRAPH_LINES_CONSECUTIVE](https://developer.android.com/reference/kotlin/android/text/Html#TO_HTML_PARAGRAPH_LINES_CONSECUTIVE:kotlin.Int) or [TO_HTML_PARAGRAPH_LINES_INDIVIDUAL](https://developer.android.com/reference/kotlin/android/text/Html#TO_HTML_PARAGRAPH_LINES_INDIVIDUAL:kotlin.Int) |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | string containing input converted to HTML |
