Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SearchResult

```
class SearchResult : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.SearchResult](../android/app/appsearch/SearchResult.md) |

This class represents one of the results obtained from an AppSearch query.

This allows clients to obtain:

- The document which matched, using `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#getGenericDocument()`
- Information about which properties in the document matched, and "snippet" information containing textual summaries of the document's matches, using `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#getMatchInfos()`

"Snippet" refers to a substring of text from the content of document that is returned as a part of search result.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult.Builder` Builder for `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#` objects. |
| | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult.EmbeddingMatchInfo` This class represents match objects for any snippets that might be present in `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults` from an embedding query. |
| | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult.MatchInfo` This class represents match objects for any snippets that might be present in `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults` from a query. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult.MatchRange` Class providing the position range of a text match information. |
| | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult.TextMatchInfo` This class represents match objects for any text match snippets that might be present in `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults` from a string query. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#getDatabaseName()()` Contains the database name that stored the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument`. |
| [GenericDocument](../android/app/appsearch/GenericDocument.md) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#getGenericDocument()()` Contains the matching `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument`. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#getInformationalRankingSignals()()` Returns the informational ranking signals of the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument`, according to the expressions added in android. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SearchResult](../android/app/appsearch/SearchResult.md)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#getJoinedResults()()` Gets a list of `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#` joined from the join operation. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SearchResult.MatchInfo](../android/app/appsearch/SearchResult.MatchInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#getMatchInfos()()` Returns a list of `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult.MatchInfo`s providing information about how the document in `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#getGenericDocument()` matched the query. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#getPackageName()()` Contains the package name of the app that stored the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument`. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#getParentTypeMap()()` Returns the map from schema type names to the list of their parent types. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#getRankingSignal()()` Returns the ranking signal of the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument`, according to the ranking strategy set in `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec.Builder#setRankingStrategy(kotlin.Int)`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SearchResult](../android/app/appsearch/SearchResult.md)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#CREATOR:android.os.Parcelable.Creator` <br /> |

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

### getDatabaseName

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDatabaseName(): String
```

Contains the database name that stored the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | Name of the database within which the document is stored. This value cannot be `null`. |

### getGenericDocument

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getGenericDocument(): GenericDocument
```

Contains the matching `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument` | Document object which matched the query. This value cannot be `null`. |

### getInformationalRankingSignals

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 16](https://developer.android.com/sdkExtensions)

```
fun getInformationalRankingSignals(): MutableList<Double!>
```

Returns the informational ranking signals of the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument`, according to the expressions added in android.app.appsearch.SearchSpec.Builder#addInformationalRankingExpressions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html!>` | This value cannot be `null`. |

### getJoinedResults

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getJoinedResults(): MutableList<SearchResult!>
```

Gets a list of `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#` joined from the join operation.

These joined documents match the outer document as specified in the `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec` with parentPropertyExpression and childPropertyExpression. They are ordered according to the `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#getNestedSearchSpec()`, and as many SearchResults as specified by `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#getMaxJoinedResultCount()` will be returned. If no `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec` was specified, this returns an empty list.

This method is inefficient to call repeatedly, as new `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#` objects are created each time.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#!>` | a List of SearchResults containing joined documents. This value cannot be `null`. |

### getMatchInfos

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMatchInfos(): MutableList<SearchResult.MatchInfo!>
```

Returns a list of `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult.MatchInfo`s providing information about how the document in `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#getGenericDocument()` matched the query.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult.MatchInfo!>` | List of matches based on `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec`. If snippeting is disabled using `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec.Builder#setSnippetCount(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec.Builder#setSnippetCountPerProperty(kotlin.Int)`, for all results after that value, this method returns an empty list. This value cannot be `null`. |

### getPackageName

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPackageName(): String
```

Contains the package name of the app that stored the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | Package name that stored the document. This value cannot be `null`. |

### getParentTypeMap

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

```
fun getParentTypeMap(): MutableMap<String!, MutableList<String!>!>
```

Returns the map from schema type names to the list of their parent types.

The map includes entries for the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument`'s own type and all of the nested documents' types. Child types are guaranteed to appear before parent types in each list.

Parent types include transitive parents.

Calling this function repeatedly is inefficient. Prefer to retain the Map returned by this function, rather than calling it multiple times.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!>` | This value cannot be `null`. |

### getRankingSignal

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRankingSignal(): Double
```

Returns the ranking signal of the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument`, according to the ranking strategy set in `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec.Builder#setRankingStrategy(kotlin.Int)`.

The meaning of the ranking signal and its value is determined by the selected ranking strategy:

- `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_NONE:kotlin.Int` - this value will be 0
- `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_DOCUMENT_SCORE:kotlin.Int` - the value returned by calling `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getScore()` on the document returned by `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#getGenericDocument()`
- `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_CREATION_TIMESTAMP:kotlin.Int` - the value returned by calling `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getCreationTimestampMillis()` on the document returned by `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#getGenericDocument()`
- `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_RELEVANCE_SCORE:kotlin.Int` - an arbitrary double value where a higher value means more relevant
- `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_USAGE_COUNT:kotlin.Int` - the number of times usage has been reported for the document returned by `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#getGenericDocument()`
- `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_USAGE_LAST_USED_TIMESTAMP:kotlin.Int` - the timestamp of the most recent usage that has been reported for the document returned by `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#getGenericDocument()`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | Ranking signal of the document |

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
static val CREATOR: Parcelable.Creator<SearchResult!>
```
