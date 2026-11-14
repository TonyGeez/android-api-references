Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

# SearchSuggestionSpec

```
class SearchSuggestionSpec : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.SearchSuggestionSpec](../android/app/appsearch/SearchSuggestionSpec.md) |

This class represents the specification logic for AppSearch. It can be used to set the filter and settings of search a suggestions.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec.Builder` Builder for `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec#`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec#SUGGESTION_RANKING_STRATEGY_DOCUMENT_COUNT:kotlin.Int` Ranked by the document count that contains the term. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec#SUGGESTION_RANKING_STRATEGY_NONE:kotlin.Int` No Ranking, results are returned in arbitrary order. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec#SUGGESTION_RANKING_STRATEGY_TERM_FREQUENCY:kotlin.Int` Ranked by the term appear frequency. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec#getFilterDocumentIds()()` Returns the map of namespace and target document ids to search over. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec#getFilterNamespaces()()` Returns the list of namespaces to search over. |
| --- | --- |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec#getFilterProperties()()` Returns the map of schema and target properties to search over. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec#getFilterSchemas()()` Returns the list of schema to search the suggestion over. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec#getMaximumResultCount()()` Returns the maximum number of wanted suggestion that will be returned in the result object. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec#getRankingStrategy()()` Returns the ranking strategy. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec#getSearchStringParameters()()` Returns the list of String parameters that can be referenced in the query through the "getSearchStringParameter({index})" function. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SearchSuggestionSpec](../android/app/appsearch/SearchSuggestionSpec.md)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### SUGGESTION_RANKING_STRATEGY_DOCUMENT_COUNT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
static val SUGGESTION_RANKING_STRATEGY_DOCUMENT_COUNT: Int
```

Ranked by the document count that contains the term.

Suppose the following document is in the index.

```kotlin
Doc1 contains: term1 term2 term2 term2
```

```kotlin
Doc2 contains: term1
```

Then, suppose that a search suggestion for "t" is issued with the DOCUMENT_COUNT, the returned `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionResult`s will be: term1, term2. The term1 will have higher score and appear in the results first.

 Value: 0

### SUGGESTION_RANKING_STRATEGY_NONE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
static val SUGGESTION_RANKING_STRATEGY_NONE: Int
```

No Ranking, results are returned in arbitrary order.

 Value: 2

### SUGGESTION_RANKING_STRATEGY_TERM_FREQUENCY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
static val SUGGESTION_RANKING_STRATEGY_TERM_FREQUENCY: Int
```

Ranked by the term appear frequency.

Suppose the following document is in the index.

```kotlin
Doc1 contains: term1 term2 term2 term2
```

```kotlin
Doc2 contains: term1
```

Then, suppose that a search suggestion for "t" is issued with the TERM_FREQUENCY, the returned `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionResult`s will be: term2, term1. The term2 will have higher score and appear in the results first.

 Value: 1

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getFilterDocumentIds

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getFilterDocumentIds(): MutableMap<String!, MutableList<String!>!>
```

Returns the map of namespace and target document ids to search over.

The keys of the returned map are namespaces, and the values are the target document ids in that namespace to search over.

If android.app.appsearch.SearchSuggestionSpec.Builder#addFilterDocumentIds was never called, returns an empty map. In this case AppSearch will search over all namespace and document ids.

Calling this function repeatedly is inefficient. Prefer to retain the Map returned by this function, rather than calling it multiple times.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!>` | This value cannot be `null`. |

### getFilterNamespaces

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getFilterNamespaces(): MutableList<String!>
```

Returns the list of namespaces to search over.

If empty, will search over all namespaces.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

### getFilterProperties

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getFilterProperties(): MutableMap<String!, MutableList<String!>!>
```

Returns the map of schema and target properties to search over.

The keys of the returned map are schema types, and the values are the target property path in that schema to search over.

If `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec.Builder#addFilterPropertyPaths(kotlin.String,%20kotlin.collections.MutableCollection)` was never called, returns an empty map. In this case AppSearch will search over all schemas and properties.

Calling this function repeatedly is inefficient. Prefer to retain the Map returned by this function, rather than calling it multiple times.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!>` | This value cannot be `null`. |

### getFilterSchemas

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getFilterSchemas(): MutableList<String!>
```

Returns the list of schema to search the suggestion over.

If empty, will search over all schemas.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

### getMaximumResultCount

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getMaximumResultCount(): Int
```

Returns the maximum number of wanted suggestion that will be returned in the result object.

### getRankingStrategy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getRankingStrategy(): Int
```

Returns the ranking strategy.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec#SUGGESTION_RANKING_STRATEGY_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec#SUGGESTION_RANKING_STRATEGY_DOCUMENT_COUNT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSuggestionSpec#SUGGESTION_RANKING_STRATEGY_TERM_FREQUENCY:kotlin.Int` |

### getSearchStringParameters

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 16](https://developer.android.com/sdkExtensions)

```
fun getSearchStringParameters(): MutableList<String!>
```

Returns the list of String parameters that can be referenced in the query through the "getSearchStringParameter({index})" function.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#search(kotlin.String,%20android.app.appsearch.SearchSpec)`

### writeToParcel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions)

```
static val CREATOR: Parcelable.Creator<SearchSuggestionSpec!>
```
