# Linkify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Linkify

Kotlin| [Java](https://developer.android.com/reference/android/text/util/Linkify "View this page in Java") 

```
open class Linkify
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.text.util.Linkify](https://developer.android.com/reference/kotlin/android/text/util/Linkify#) |

Linkify take a piece of text and a regular expression and turns all of the regex matches in the text into clickable links. This is particularly useful for matching things like email addresses, web URLs, etc. and making them actionable. Alone with the pattern that is to be matched, a URL scheme prefix is also required. Any pattern match that does not begin with the supplied scheme will have the scheme prepended to the matched text when the clickable URL is created. For instance, if you are matching web URLs you would supply the scheme`http://`. If the pattern matches example.com, which does not have a URL scheme prefix, the supplied scheme will be prepended to create`http://example.com`when the clickable URL link is created.

**Note:** When using [MAP_ADDRESSES](https://developer.android.com/reference/kotlin/android/text/util/Linkify#MAP_ADDRESSES:kotlin.Int) or [ALL](https://developer.android.com/reference/kotlin/android/text/util/Linkify#ALL:kotlin.Int) to match street addresses on API level [android.os.Build.VERSION_CODES#O_MR1](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O_MR1:kotlin.Int) and earlier, methods in this class may throw [android.util.AndroidRuntimeException](https://developer.android.com/reference/kotlin/android/util/AndroidRuntimeException.html#) or other exceptions if the device's WebView implementation is currently being updated, because [android.webkit.WebView#findAddress](https://developer.android.com/reference/kotlin/android/webkit/WebView.html#findAddress(kotlin.String))is required to match street addresses.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [MatchFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.MatchFilter) MatchFilter enables client code to have more control over what is allowed to match and become a link, and what is not. |
| abstract | [TransformFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.TransformFilter) TransformFilter enables client code to have more control over how matched patterns are represented as URLs. |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALL](https://developer.android.com/reference/kotlin/android/text/util/Linkify#ALL:kotlin.Int) Bit mask indicating that all available patterns should be matched in methods that take an options mask. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMAIL_ADDRESSES](https://developer.android.com/reference/kotlin/android/text/util/Linkify#EMAIL_ADDRESSES:kotlin.Int) Bit field indicating that email addresses should be matched in methods that take an options mask |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAP_ADDRESSES](https://developer.android.com/reference/kotlin/android/text/util/Linkify#MAP_ADDRESSES:kotlin.Int) Bit field indicating that street addresses should be matched in methods that take an options mask. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PHONE_NUMBERS](https://developer.android.com/reference/kotlin/android/text/util/Linkify#PHONE_NUMBERS:kotlin.Int) Bit field indicating that phone numbers should be matched in methods that take an options mask |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WEB_URLS](https://developer.android.com/reference/kotlin/android/text/util/Linkify#WEB_URLS:kotlin.Int) Bit field indicating that web URLs should be matched in methods that take an options mask |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------|---|
| [Linkify](https://developer.android.com/reference/kotlin/android/text/util/Linkify#Linkify())`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addLinks](https://developer.android.com/reference/kotlin/android/text/util/Linkify#addLinks(android.text.Spannable,%20kotlin.Int))`(`text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)`, `mask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Scans the text of the provided Spannable and turns all occurrences of the link types indicated in the mask into clickable links. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addLinks](https://developer.android.com/reference/kotlin/android/text/util/Linkify#addLinks(android.text.Spannable,%20kotlin.Int,%20java.util.function.Function))`(`text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)`, `mask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `urlSpanFactory:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [URLSpan](https://developer.android.com/reference/kotlin/android/text/style/URLSpan.html#)!>?`)` Scans the text of the provided Spannable and turns all occurrences of the link types indicated in the mask into clickable links. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addLinks](https://developer.android.com/reference/kotlin/android/text/util/Linkify#addLinks(android.text.Spannable,%20java.util.regex.Pattern,%20kotlin.String))`(`text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)`, `pattern:` ` [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#)`, `scheme:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Applies a regex to a Spannable turning the matches into links. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addLinks](https://developer.android.com/reference/kotlin/android/text/util/Linkify#addLinks(android.text.Spannable,%20java.util.regex.Pattern,%20kotlin.String,%20android.text.util.Linkify.MatchFilter,%20android.text.util.Linkify.TransformFilter))`(`spannable:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)`, `pattern:` ` [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#)`, `scheme:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `matchFilter:` ` [Linkify.MatchFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.MatchFilter)?`, `transformFilter:` ` [Linkify.TransformFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.TransformFilter)?`)` Applies a regex to a Spannable turning the matches into links. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addLinks](https://developer.android.com/reference/kotlin/android/text/util/Linkify#addLinks(android.text.Spannable,%20java.util.regex.Pattern,%20kotlin.String,%20kotlin.Array,%20android.text.util.Linkify.MatchFilter,%20android.text.util.Linkify.TransformFilter))`(`spannable:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)`, `pattern:` ` [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#)`, `defaultScheme:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `schemes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `matchFilter:` ` [Linkify.MatchFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.MatchFilter)?`, `transformFilter:` ` [Linkify.TransformFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.TransformFilter)?`)` Applies a regex to a Spannable turning the matches into links. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addLinks](https://developer.android.com/reference/kotlin/android/text/util/Linkify#addLinks(android.text.Spannable,%20java.util.regex.Pattern,%20kotlin.String,%20kotlin.Array,%20android.text.util.Linkify.MatchFilter,%20android.text.util.Linkify.TransformFilter,%20java.util.function.Function))`(`spannable:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)`, `pattern:` ` [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#)`, `defaultScheme:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `schemes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `matchFilter:` ` [Linkify.MatchFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.MatchFilter)?`, `transformFilter:` ` [Linkify.TransformFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.TransformFilter)?`, `urlSpanFactory:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [URLSpan](https://developer.android.com/reference/kotlin/android/text/style/URLSpan.html#)!>?`)` Applies a regex to a Spannable turning the matches into links. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addLinks](https://developer.android.com/reference/kotlin/android/text/util/Linkify#addLinks(android.widget.TextView,%20kotlin.Int))`(`text:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)`, `mask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Scans the text of the provided TextView and turns all occurrences of the link types indicated in the mask into clickable links. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLinks](https://developer.android.com/reference/kotlin/android/text/util/Linkify#addLinks(android.widget.TextView,%20java.util.regex.Pattern,%20kotlin.String))`(`text:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)`, `pattern:` ` [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#)`, `scheme:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Applies a regex to the text of a TextView turning the matches into links. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLinks](https://developer.android.com/reference/kotlin/android/text/util/Linkify#addLinks(android.widget.TextView,%20java.util.regex.Pattern,%20kotlin.String,%20android.text.util.Linkify.MatchFilter,%20android.text.util.Linkify.TransformFilter))`(`text:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)`, `pattern:` ` [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#)`, `scheme:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `matchFilter:` ` [Linkify.MatchFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.MatchFilter)?`, `transformFilter:` ` [Linkify.TransformFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.TransformFilter)?`)` Applies a regex to the text of a TextView turning the matches into links. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLinks](https://developer.android.com/reference/kotlin/android/text/util/Linkify#addLinks(android.widget.TextView,%20java.util.regex.Pattern,%20kotlin.String,%20kotlin.Array,%20android.text.util.Linkify.MatchFilter,%20android.text.util.Linkify.TransformFilter))`(`text:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)`, `pattern:` ` [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#)`, `defaultScheme:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `schemes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `matchFilter:` ` [Linkify.MatchFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.MatchFilter)?`, `transformFilter:` ` [Linkify.TransformFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.TransformFilter)?`)` Applies a regex to the text of a TextView turning the matches into links. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Linkify.MatchFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.MatchFilter)! | [sPhoneNumberMatchFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify#sPhoneNumberMatchFilter:android.text.util.Linkify.MatchFilter) Filters out URL matches that don't have enough digits to be a phone number. |
| static [Linkify.TransformFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.TransformFilter)! | [sPhoneNumberTransformFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify#sPhoneNumberTransformFilter:android.text.util.Linkify.TransformFilter) Transforms matched phone number text into something suitable to be used in a tel: URL. |
| static [Linkify.MatchFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.MatchFilter)! | [sUrlMatchFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify#sUrlMatchFilter:android.text.util.Linkify.MatchFilter) Filters out web URL matches that occur after an at-sign (@). |

## Constants

### ALL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALL: Int
```

**Deprecated:** *use android.view.textclassifier.TextClassifier#generateLinks( \* TextLinks.Request) instead, and avoid [ALL](https://developer.android.com/reference/kotlin/android/text/util/Linkify#ALL:kotlin.Int) even when targeting API levels where no alternative is available.*

Bit mask indicating that all available patterns should be matched in methods that take an options mask. Note that this should be avoided, as the [MAP_ADDRESSES](https://developer.android.com/reference/kotlin/android/text/util/Linkify#MAP_ADDRESSES:kotlin.Int) field uses the [android.webkit.WebView#findAddress( * String)](https://developer.android.com/reference/kotlin/android/webkit/WebView.html#findAddress(kotlin.String))method, which has various limitations and has been deprecated: see the documentation for [android.webkit.WebView#findAddress(String)](https://developer.android.com/reference/kotlin/android/webkit/WebView.html#findAddress(kotlin.String))for more information. 

 Value: 15

### EMAIL_ADDRESSES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMAIL_ADDRESSES: Int
```

Bit field indicating that email addresses should be matched in methods that take an options mask 

 Value: 2

### MAP_ADDRESSES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAP_ADDRESSES: Int
```

**Deprecated:** *use android.view.textclassifier.TextClassifier#generateLinks( \* TextLinks.Request) instead, and avoid [MAP_ADDRESSES](https://developer.android.com/reference/kotlin/android/text/util/Linkify#MAP_ADDRESSES:kotlin.Int) even when targeting API levels where no alternative is available.*

Bit field indicating that street addresses should be matched in methods that take an options mask. Note that this should be avoided, as it uses the [android.webkit.WebView#findAddress(String)](https://developer.android.com/reference/kotlin/android/webkit/WebView.html#findAddress(kotlin.String))method, which has various limitations and has been deprecated: see the documentation for [android.webkit.WebView#findAddress(String)](https://developer.android.com/reference/kotlin/android/webkit/WebView.html#findAddress(kotlin.String))for more information. 

 Value: 8

### PHONE_NUMBERS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHONE_NUMBERS: Int
```

Bit field indicating that phone numbers should be matched in methods that take an options mask 

 Value: 4

### WEB_URLS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEB_URLS: Int
```

Bit field indicating that web URLs should be matched in methods that take an options mask 

 Value: 1

## Public constructors

### Linkify

```
Linkify()
```

## Public methods

### addLinks

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun addLinks(
    text: Spannable, 
    mask: Int
): Boolean
```

Scans the text of the provided Spannable and turns all occurrences of the link types indicated in the mask into clickable links. If the mask is nonzero, it also removes any existing URLSpans attached to the Spannable, to avoid problems if you call it repeatedly on the same text.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#):Spannable whose text is to be marked-up with links This value cannot be`null`. |
| `mask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Mask to define which kinds of links will be searched. Value is either`0`or a combination of [android.text.util.Linkify#WEB_URLS](https://developer.android.com/reference/kotlin/android/text/util/Linkify#WEB_URLS:kotlin.Int), [android.text.util.Linkify#EMAIL_ADDRESSES](https://developer.android.com/reference/kotlin/android/text/util/Linkify#EMAIL_ADDRESSES:kotlin.Int), [android.text.util.Linkify#PHONE_NUMBERS](https://developer.android.com/reference/kotlin/android/text/util/Linkify#PHONE_NUMBERS:kotlin.Int), [android.text.util.Linkify#MAP_ADDRESSES](https://developer.android.com/reference/kotlin/android/text/util/Linkify#MAP_ADDRESSES:kotlin.Int), and [android.text.util.Linkify#ALL](https://developer.android.com/reference/kotlin/android/text/util/Linkify#ALL:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if at least one link is found and applied. |

**See Also**

- [#addLinks(Spannable, int, Function)](https://developer.android.com/reference/kotlin/android/text/util/Linkify#addLinks(android.text.Spannable,%20kotlin.Int,%20java.util.function.Function)) 

### addLinks

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun addLinks(
    text: Spannable, 
    mask: Int, 
    urlSpanFactory: Function<String!, URLSpan!>?
): Boolean
```

Scans the text of the provided Spannable and turns all occurrences of the link types indicated in the mask into clickable links. If the mask is nonzero, it also removes any existing URLSpans attached to the Spannable, to avoid problems if you call it repeatedly on the same text.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#):Spannable whose text is to be marked-up with links This value cannot be`null`. |
| `mask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):mask to define which kinds of links will be searched Value is either`0`or a combination of [android.text.util.Linkify#WEB_URLS](https://developer.android.com/reference/kotlin/android/text/util/Linkify#WEB_URLS:kotlin.Int), [android.text.util.Linkify#EMAIL_ADDRESSES](https://developer.android.com/reference/kotlin/android/text/util/Linkify#EMAIL_ADDRESSES:kotlin.Int), [android.text.util.Linkify#PHONE_NUMBERS](https://developer.android.com/reference/kotlin/android/text/util/Linkify#PHONE_NUMBERS:kotlin.Int), [android.text.util.Linkify#MAP_ADDRESSES](https://developer.android.com/reference/kotlin/android/text/util/Linkify#MAP_ADDRESSES:kotlin.Int), and [android.text.util.Linkify#ALL](https://developer.android.com/reference/kotlin/android/text/util/Linkify#ALL:kotlin.Int) |
| `urlSpanFactory` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [URLSpan](https://developer.android.com/reference/kotlin/android/text/style/URLSpan.html#)!\>?:function used to create [URLSpan](https://developer.android.com/reference/kotlin/android/text/style/URLSpan.html#) s This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if at least one link is found and applied. |

### addLinks

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun addLinks(
    text: Spannable, 
    pattern: Pattern, 
    scheme: String?
): Boolean
```

Applies a regex to a Spannable turning the matches into links.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#):Spannable whose text is to be marked-up with links This value cannot be`null`. |
| `pattern` | [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#):Regex pattern to be used for finding links This value cannot be`null`. |
| `scheme` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:URL scheme string (eg`http://`) to be prepended to the links that do not start with this scheme. This value may be`null`. |

**See Also**

- [#addLinks(Spannable, Pattern, String, String[], MatchFilter, TransformFilter, Function)](https://developer.android.com/reference/kotlin/android/text/util/Linkify#addLinks(android.text.Spannable,%20java.util.regex.Pattern,%20kotlin.String,%20kotlin.Array,%20android.text.util.Linkify.MatchFilter,%20android.text.util.Linkify.TransformFilter,%20java.util.function.Function)) 

### addLinks

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun addLinks(
    spannable: Spannable, 
    pattern: Pattern, 
    scheme: String?, 
    matchFilter: Linkify.MatchFilter?, 
    transformFilter: Linkify.TransformFilter?
): Boolean
```

Applies a regex to a Spannable turning the matches into links.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `spannable` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#):Spannable whose text is to be marked-up with links This value cannot be`null`. |
| `pattern` | [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#):Regex pattern to be used for finding links This value cannot be`null`. |
| `scheme` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:URL scheme string (eg`http://`) to be prepended to the links that do not start with this scheme. This value may be`null`. |
| `matchFilter` | [Linkify.MatchFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.MatchFilter)?:The filter that is used to allow the client code additional control over which pattern matches are to be converted into links. This value may be`null`. |
| `transformFilter` | [Linkify.TransformFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.TransformFilter)?:Filter to allow the client code to update the link found. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if at least one link is found and applied. |

**See Also**

- [#addLinks(Spannable, Pattern, String, String[], MatchFilter, TransformFilter, Function)](https://developer.android.com/reference/kotlin/android/text/util/Linkify#addLinks(android.text.Spannable,%20java.util.regex.Pattern,%20kotlin.String,%20kotlin.Array,%20android.text.util.Linkify.MatchFilter,%20android.text.util.Linkify.TransformFilter,%20java.util.function.Function)) 

### addLinks

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun addLinks(
    spannable: Spannable, 
    pattern: Pattern, 
    defaultScheme: String?, 
    schemes: Array<String!>?, 
    matchFilter: Linkify.MatchFilter?, 
    transformFilter: Linkify.TransformFilter?
): Boolean
```

Applies a regex to a Spannable turning the matches into links.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `spannable` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#):Spannable whose text is to be marked-up with links. This value cannot be`null`. |
| `pattern` | [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#):Regex pattern to be used for finding links. This value cannot be`null`. |
| `defaultScheme` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The default scheme to be prepended to links if the link does not start with one of the`schemes`given. This value may be`null`. |
| `schemes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:Array of schemes (eg`http://`) to check if the link found contains a scheme. Passing a null or empty value means prepend defaultScheme to all links. |
| `matchFilter` | [Linkify.MatchFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.MatchFilter)?:The filter that is used to allow the client code additional control over which pattern matches are to be converted into links. This value may be`null`. |
| `transformFilter` | [Linkify.TransformFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.TransformFilter)?:Filter to allow the client code to update the link found. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if at least one link is found and applied. |

**See Also**

- [#addLinks(Spannable, Pattern, String, String[], MatchFilter, TransformFilter, Function)](https://developer.android.com/reference/kotlin/android/text/util/Linkify#addLinks(android.text.Spannable,%20java.util.regex.Pattern,%20kotlin.String,%20kotlin.Array,%20android.text.util.Linkify.MatchFilter,%20android.text.util.Linkify.TransformFilter,%20java.util.function.Function)) 

### addLinks

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun addLinks(
    spannable: Spannable, 
    pattern: Pattern, 
    defaultScheme: String?, 
    schemes: Array<String!>?, 
    matchFilter: Linkify.MatchFilter?, 
    transformFilter: Linkify.TransformFilter?, 
    urlSpanFactory: Function<String!, URLSpan!>?
): Boolean
```

Applies a regex to a Spannable turning the matches into links.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `spannable` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#):spannable whose text is to be marked-up with links. This value cannot be`null`. |
| `pattern` | [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#):regex pattern to be used for finding links. This value cannot be`null`. |
| `defaultScheme` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the default scheme to be prepended to links if the link does not start with one of the`schemes`given. This value may be`null`. |
| `schemes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:array of schemes (eg`http://`) to check if the link found contains a scheme. Passing a null or empty value means prepend defaultScheme to all links. |
| `matchFilter` | [Linkify.MatchFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.MatchFilter)?:the filter that is used to allow the client code additional control over which pattern matches are to be converted into links. This value may be`null`. |
| `transformFilter` | [Linkify.TransformFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.TransformFilter)?:filter to allow the client code to update the link found. This value may be`null`. |
| `urlSpanFactory` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [URLSpan](https://developer.android.com/reference/kotlin/android/text/style/URLSpan.html#)!\>?:function used to create [URLSpan](https://developer.android.com/reference/kotlin/android/text/style/URLSpan.html#) s This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if at least one link is found and applied. |

### addLinks

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun addLinks(
    text: TextView, 
    mask: Int
): Boolean
```

Scans the text of the provided TextView and turns all occurrences of the link types indicated in the mask into clickable links. If matches are found the movement method for the TextView is set to LinkMovementMethod.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#):TextView whose text is to be marked-up with links This value cannot be`null`. |
| `mask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Mask to define which kinds of links will be searched. Value is either`0`or a combination of [android.text.util.Linkify#WEB_URLS](https://developer.android.com/reference/kotlin/android/text/util/Linkify#WEB_URLS:kotlin.Int), [android.text.util.Linkify#EMAIL_ADDRESSES](https://developer.android.com/reference/kotlin/android/text/util/Linkify#EMAIL_ADDRESSES:kotlin.Int), [android.text.util.Linkify#PHONE_NUMBERS](https://developer.android.com/reference/kotlin/android/text/util/Linkify#PHONE_NUMBERS:kotlin.Int), [android.text.util.Linkify#MAP_ADDRESSES](https://developer.android.com/reference/kotlin/android/text/util/Linkify#MAP_ADDRESSES:kotlin.Int), and [android.text.util.Linkify#ALL](https://developer.android.com/reference/kotlin/android/text/util/Linkify#ALL:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if at least one link is found and applied. |

**See Also**

- [#addLinks(Spannable, int, Function)](https://developer.android.com/reference/kotlin/android/text/util/Linkify#addLinks(android.text.Spannable,%20kotlin.Int,%20java.util.function.Function)) 

### addLinks

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun addLinks(
    text: TextView, 
    pattern: Pattern, 
    scheme: String?
): Unit
```

Applies a regex to the text of a TextView turning the matches into links. If links are found then UrlSpans are applied to the link text match areas, and the movement method for the text is changed to LinkMovementMethod.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#):TextView whose text is to be marked-up with links This value cannot be`null`. |
| `pattern` | [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#):Regex pattern to be used for finding links This value cannot be`null`. |
| `scheme` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:URL scheme string (eg`http://`) to be prepended to the links that do not start with this scheme. This value may be`null`. |

### addLinks

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun addLinks(
    text: TextView, 
    pattern: Pattern, 
    scheme: String?, 
    matchFilter: Linkify.MatchFilter?, 
    transformFilter: Linkify.TransformFilter?
): Unit
```

Applies a regex to the text of a TextView turning the matches into links. If links are found then UrlSpans are applied to the link text match areas, and the movement method for the text is changed to LinkMovementMethod.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#):TextView whose text is to be marked-up with links This value cannot be`null`. |
| `pattern` | [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#):Regex pattern to be used for finding links This value cannot be`null`. |
| `scheme` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:URL scheme string (eg`http://`) to be prepended to the links that do not start with this scheme. This value may be`null`. |
| `matchFilter` | [Linkify.MatchFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.MatchFilter)?:The filter that is used to allow the client code additional control over which pattern matches are to be converted into links. This value may be`null`. |
| `transformFilter` | [Linkify.TransformFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.TransformFilter)?:This value may be`null`. |

### addLinks

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun addLinks(
    text: TextView, 
    pattern: Pattern, 
    defaultScheme: String?, 
    schemes: Array<String!>?, 
    matchFilter: Linkify.MatchFilter?, 
    transformFilter: Linkify.TransformFilter?
): Unit
```

Applies a regex to the text of a TextView turning the matches into links. If links are found then UrlSpans are applied to the link text match areas, and the movement method for the text is changed to LinkMovementMethod.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#):TextView whose text is to be marked-up with links. This value cannot be`null`. |
| `pattern` | [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#):Regex pattern to be used for finding links. This value cannot be`null`. |
| `defaultScheme` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The default scheme to be prepended to links if the link does not start with one of the`schemes`given. This value may be`null`. |
| `schemes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:Array of schemes (eg`http://`) to check if the link found contains a scheme. Passing a null or empty value means prepend defaultScheme to all links. |
| `matchFilter` | [Linkify.MatchFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.MatchFilter)?:The filter that is used to allow the client code additional control over which pattern matches are to be converted into links. This value may be`null`. |
| `transformFilter` | [Linkify.TransformFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.TransformFilter)?:Filter to allow the client code to update the link found. This value may be`null`. |

## Properties

### sPhoneNumberMatchFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val sPhoneNumberMatchFilter: Linkify.MatchFilter!
```

Filters out URL matches that don't have enough digits to be a phone number. 

### sPhoneNumberTransformFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val sPhoneNumberTransformFilter: Linkify.TransformFilter!
```

Transforms matched phone number text into something suitable to be used in a tel: URL. It does this by removing everything but the digits and plus signs. For instance: '+1 (919) 555-1212' becomes '+19195551212' 

### sUrlMatchFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val sUrlMatchFilter: Linkify.MatchFilter!
```

Filters out web URL matches that occur after an at-sign (@). This is to prevent turning the domain name in an email address into a web link.
