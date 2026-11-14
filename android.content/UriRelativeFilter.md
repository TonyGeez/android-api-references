# UriRelativeFilter

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UriRelativeFilter

Kotlin| [Java](UriRelativeFilter.md) 
| --- | --- |

```
class UriRelativeFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.UriRelativeFilter](UriRelativeFilter.md) |

A filter for matching Intent URI Data as part of a [UriRelativeFilterGroup](UriRelativeFilterGroup.md). A single filter can only be matched against either a URI path, query or fragment

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FRAGMENT](UriRelativeFilter.md) Value to indicate that the filter is to be applied to a URI fragment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PATH](UriRelativeFilter.md) Value to indicate that the filter is to be applied to a URI path. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUERY](UriRelativeFilter.md) Value to indicate that the filter is to be applied to a URI query. |
| --- | --- |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UriRelativeFilter](UriRelativeFilter.md))`(`uriPart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `patternType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `filter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Creates a new UriRelativeFilter. |

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](UriRelativeFilter.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getFilter](UriRelativeFilter.md))`()` The string used to filter the URI. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPatternType](UriRelativeFilter.md))`()` The pattern type of the filter. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUriPart](UriRelativeFilter.md))`()` The URI part this filter operates on. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](UriRelativeFilter.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [matchData](UriRelativeFilter.md))`(`data:` ` [Uri](../android.net/Uri.md)`)` Match this URI filter against an Intent's data. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](UriRelativeFilter.md))`()` <br /> |

## Constants

### FRAGMENT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FRAGMENT: Int
```

Value to indicate that the filter is to be applied to a URI fragment. 

 Value: 2

### PATH

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PATH: Int
```

Value to indicate that the filter is to be applied to a URI path. 

 Value: 0

### QUERY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERY: Int
```

Value to indicate that the filter is to be applied to a URI query. 

 Value: 1

## Public constructors

### UriRelativeFilter

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UriRelativeFilter(
    uriPart: Int, 
    patternType: Int, 
    filter: String)
```

Creates a new UriRelativeFilter.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uriPart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The URI part this filter operates on. Can be either a [UriRelativeFilter.PATH](UriRelativeFilter.md), [UriRelativeFilter.QUERY](UriRelativeFilter.md), or [UriRelativeFilter.FRAGMENT](UriRelativeFilter.md). Value is [android.content.UriRelativeFilter#PATH](UriRelativeFilter.md), [android.content.UriRelativeFilter#QUERY](UriRelativeFilter.md), or [android.content.UriRelativeFilter#FRAGMENT](UriRelativeFilter.md) |
| `patternType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The pattern type of the filter. Can be either a [PatternMatcher.PATTERN_LITERAL](../android.os/PatternMatcher.md), [PatternMatcher.PATTERN_PREFIX](../android.os/PatternMatcher.md), [PatternMatcher.PATTERN_SUFFIX](../android.os/PatternMatcher.md), [PatternMatcher.PATTERN_SIMPLE_GLOB](../android.os/PatternMatcher.md), or [PatternMatcher.PATTERN_ADVANCED_GLOB](../android.os/PatternMatcher.md). Value is [android.os.PatternMatcher#PATTERN_LITERAL](../android.os/PatternMatcher.md), [android.os.PatternMatcher#PATTERN_PREFIX](../android.os/PatternMatcher.md), [android.os.PatternMatcher#PATTERN_SIMPLE_GLOB](../android.os/PatternMatcher.md), [android.os.PatternMatcher#PATTERN_ADVANCED_GLOB](../android.os/PatternMatcher.md), or [android.os.PatternMatcher#PATTERN_SUFFIX](../android.os/PatternMatcher.md) |
| `filter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):A literal or pattern string depedning on patterType used to match a uriPart . This value cannot be`null`. |
| --- | --- |

## Public methods

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### getFilter

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFilter(): String
```

The string used to filter the URI.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getPatternType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPatternType(): Int
```

The pattern type of the filter.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.os.PatternMatcher#PATTERN_LITERAL](../android.os/PatternMatcher.md), [android.os.PatternMatcher#PATTERN_PREFIX](../android.os/PatternMatcher.md), [android.os.PatternMatcher#PATTERN_SIMPLE_GLOB](../android.os/PatternMatcher.md), [android.os.PatternMatcher#PATTERN_ADVANCED_GLOB](../android.os/PatternMatcher.md), or [android.os.PatternMatcher#PATTERN_SUFFIX](../android.os/PatternMatcher.md) |

### getUriPart

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUriPart(): Int
```

The URI part this filter operates on.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.content.UriRelativeFilter#PATH](UriRelativeFilter.md), [android.content.UriRelativeFilter#QUERY](UriRelativeFilter.md), or [android.content.UriRelativeFilter#FRAGMENT](UriRelativeFilter.md) |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### matchData

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun matchData(data: Uri): Boolean
```

Match this URI filter against an Intent's data. QUERY filters can match against any key value pair in the query string. PATH and FRAGMENT filters must match the entire string.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [Uri](../android.net/Uri.md):The full data string to match against, as supplied in Intent.data. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if there is a match. |

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
