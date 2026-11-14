Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SearchSpec

```
class SearchSpec : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.SearchSpec](SearchSpec.md) |

This class represents the specification logic for AppSearch. It can be used to set the type of search, like prefix or exact only or apply filters to search for a specific schema type only etc.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec.Builder` Builder for SearchSpec. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#EMBEDDING_SEARCH_METRIC_TYPE_COSINE:kotlin.Int` Cosine similarity as metric for embedding search and ranking. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#EMBEDDING_SEARCH_METRIC_TYPE_DEFAULT:kotlin.Int` Use the default metric set in getDefaultEmbeddingSearchMetricType for embedding search and ranking. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#EMBEDDING_SEARCH_METRIC_TYPE_DOT_PRODUCT:kotlin.Int` Dot product similarity as metric for embedding search and ranking. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#EMBEDDING_SEARCH_METRIC_TYPE_EUCLIDEAN:kotlin.Int` Euclidean distance as metric for embedding search and ranking. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#GROUPING_TYPE_PER_NAMESPACE:kotlin.Int` Results should be grouped together by namespace for the purpose of enforcing a limit on the number of results returned per namespace. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#GROUPING_TYPE_PER_PACKAGE:kotlin.Int` Results should be grouped together by package for the purpose of enforcing a limit on the number of results returned per package. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#GROUPING_TYPE_PER_SCHEMA:kotlin.Int` Results should be grouped together by schema type for the purpose of enforcing a limit on the number of results returned per schema type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#ORDER_ASCENDING:kotlin.Int` Search results will be returned in an ascending order. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#ORDER_DESCENDING:kotlin.Int` Search results will be returned in a descending order. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#PROJECTION_SCHEMA_TYPE_WILDCARD:kotlin.String` Schema type to be used in addProjection to apply property paths to all results, excepting any types that have had their own, specific property paths set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_ADVANCED_RANKING_EXPRESSION:kotlin.Int` Ranked by the advanced ranking expression provided. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_CREATION_TIMESTAMP:kotlin.Int` Ranked by document creation timestamps. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_DOCUMENT_SCORE:kotlin.Int` Ranked by app-provided document scores. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_JOIN_AGGREGATE_SCORE:kotlin.Int` Ranked by the aggregated ranking signal of the joined documents. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_NONE:kotlin.Int` No Ranking, results are returned in arbitrary order. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_RELEVANCE_SCORE:kotlin.Int` Ranked by document relevance score. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_SYSTEM_USAGE_COUNT:kotlin.Int` Ranked by number of usages from a system UI surface. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_SYSTEM_USAGE_LAST_USED_TIMESTAMP:kotlin.Int` Ranked by timestamp of last usage from a system UI surface. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_USAGE_COUNT:kotlin.Int` Ranked by number of usages, as reported by the app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_USAGE_LAST_USED_TIMESTAMP:kotlin.Int` Ranked by timestamp of last usage, as reported by the app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#SCHEMA_TYPE_WILDCARD:kotlin.String` Schema type to be used in addFilterProperties and addProjection to apply property paths to all results, excepting any types that have had their own, specific property paths set. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#TERM_MATCH_EXACT_ONLY:kotlin.Int` Query terms will only match exact tokens in the index. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#TERM_MATCH_PREFIX:kotlin.Int` Query terms will match indexed tokens when the query term is a prefix of the token. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getAdvancedRankingExpression Get the advanced ranking expression, or "" if setRankingStrategy was not called. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDefaultEmbeddingSearchMetricType Returns the default embedding metric type used for embedding search (see search) and ranking (see setRankingStrategy). |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [EmbeddingVector](EmbeddingVector.md)!\> | getEmbeddingParameters Returns the list of EmbeddingVector that can be referenced in the query through the "getEmbeddingParameter({index})" function. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | getFilterDocumentIds Returns the list of document ids to search over. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | getFilterNamespaces Returns the list of namespaces to search over. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | getFilterPackageNames Returns the list of package name filters to search over. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\> | getFilterProperties Returns the map of schema and target properties to search over. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | getFilterSchemas Returns the list of schema types to search for. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | getInformationalRankingExpressions Returns the informational ranking expressions. |
| [JoinSpec](JoinSpec.md)? | getJoinSpec Returns specification on which documents need to be joined. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMaxSnippetSize Returns the maximum size of a snippet in characters. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getOrder Returns the order of returned search results (descending or ascending). |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PropertyPath](PropertyPath.md)!\>!\> | getProjectionPaths Returns a map from schema type to property paths to be used for projection. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\> | getProjections Returns a map from schema type to property paths to be used for projection. |
| --- | --- |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [PropertyPath](PropertyPath.md)!, [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!\>!\> | getPropertyWeightPaths Returns properties weights to be used for scoring. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!\>!\> | getPropertyWeights Returns properties weights to be used for scoring. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getRankingStrategy Returns the ranking strategy. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getResultCountPerPage Returns the number of results per page in the result set. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getResultGroupingLimit Get the maximum number of results to return for each group. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getResultGroupingTypeFlags Get the type of grouping limit to apply, or 0 if setResultGrouping was not called. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getSearchSourceLogTag Gets a tag to indicate the source of this search, or `null` if setSearchSourceLogTag was not called. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | getSearchStringParameters Returns the list of String parameters that can be referenced in the query through the "getSearchStringParameter({index})" function. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSnippetCount Returns how many documents to generate snippets for. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSnippetCountPerProperty Returns how many matches for each property of a matching document to generate snippets for. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getTermMatch Returns how the query terms should match terms in the index. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isListFilterHasPropertyFunctionEnabled Returns whether the LIST_FILTER_HAS_PROPERTY_FUNCTION feature is enabled. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isListFilterMatchScoreExpressionFunctionEnabled Returns whether the LIST_FILTER_MATCH_SCORE_EXPRESSION_FUNCTION feature is enabled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isListFilterQueryLanguageEnabled Returns whether the LIST_FILTER_QUERY_LANGUAGE feature is enabled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isNumericSearchEnabled Returns whether the NUMERIC_SEARCH feature is enabled. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isScorablePropertyRankingEnabled Returns whether the ScorablePropertyRanking feature is enabled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isVerbatimSearchEnabled Returns whether the VERBATIM_SEARCH feature is enabled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | shouldRetrieveEmbeddingMatchInfos Returns whether to retrieve embedding match infos as a part of getMatchInfos |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SearchSpec](SearchSpec.md)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#CREATOR:android.os.Parcelable.Creator` Creator class for SearchSpec. |

## Constants

### EMBEDDING_SEARCH_METRIC_TYPE_COSINE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 16](https://developer.android.com/sdkExtensions)

```
static val EMBEDDING_SEARCH_METRIC_TYPE_COSINE: Int
```

Cosine similarity as metric for embedding search and ranking.

 Value: 1

### EMBEDDING_SEARCH_METRIC_TYPE_DEFAULT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 16](https://developer.android.com/sdkExtensions)

```
static val EMBEDDING_SEARCH_METRIC_TYPE_DEFAULT: Int
```

Use the default metric set in getDefaultEmbeddingSearchMetricType for embedding search and ranking.

 Value: 0

### EMBEDDING_SEARCH_METRIC_TYPE_DOT_PRODUCT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 16](https://developer.android.com/sdkExtensions)

```
static val EMBEDDING_SEARCH_METRIC_TYPE_DOT_PRODUCT: Int
```

Dot product similarity as metric for embedding search and ranking.

 Value: 2

### EMBEDDING_SEARCH_METRIC_TYPE_EUCLIDEAN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 16](https://developer.android.com/sdkExtensions)

```
static val EMBEDDING_SEARCH_METRIC_TYPE_EUCLIDEAN: Int
```

Euclidean distance as metric for embedding search and ranking.

 Value: 3

### GROUPING_TYPE_PER_NAMESPACE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUPING_TYPE_PER_NAMESPACE: Int
```

Results should be grouped together by namespace for the purpose of enforcing a limit on the number of results returned per namespace.

 Value: 2

### GROUPING_TYPE_PER_PACKAGE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUPING_TYPE_PER_PACKAGE: Int
```

Results should be grouped together by package for the purpose of enforcing a limit on the number of results returned per package.

 Value: 1

### GROUPING_TYPE_PER_SCHEMA

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions)

```
static val GROUPING_TYPE_PER_SCHEMA: Int
```

Results should be grouped together by schema type for the purpose of enforcing a limit on the number of results returned per schema type.

 Value: 4

### ORDER_ASCENDING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ORDER_ASCENDING: Int
```

Search results will be returned in an ascending order.

 Value: 1

### ORDER_DESCENDING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ORDER_DESCENDING: Int
```

Search results will be returned in a descending order.

 Value: 0

### PROJECTION_SCHEMA_TYPE_WILDCARD

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROJECTION_SCHEMA_TYPE_WILDCARD: String
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#SCHEMA_TYPE_WILDCARD:kotlin.String` instead.*

Schema type to be used in addProjection to apply property paths to all results, excepting any types that have had their own, specific property paths set.

 Value: "*"

### RANKING_STRATEGY_ADVANCED_RANKING_EXPRESSION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
static val RANKING_STRATEGY_ADVANCED_RANKING_EXPRESSION: Int
```

Ranked by the advanced ranking expression provided.

 Value: 9

### RANKING_STRATEGY_CREATION_TIMESTAMP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RANKING_STRATEGY_CREATION_TIMESTAMP: Int
```

Ranked by document creation timestamps.

 Value: 2

### RANKING_STRATEGY_DOCUMENT_SCORE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RANKING_STRATEGY_DOCUMENT_SCORE: Int
```

Ranked by app-provided document scores.

 Value: 1

### RANKING_STRATEGY_JOIN_AGGREGATE_SCORE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
static val RANKING_STRATEGY_JOIN_AGGREGATE_SCORE: Int
```

Ranked by the aggregated ranking signal of the joined documents.

Which aggregation strategy is used to determine a ranking signal is specified in the JoinSpec set by setJoinSpec. This ranking strategy may not be used if no JoinSpec is provided.

 Value: 8

**See Also**

- build

### RANKING_STRATEGY_NONE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RANKING_STRATEGY_NONE: Int
```

No Ranking, results are returned in arbitrary order.

 Value: 0

### RANKING_STRATEGY_RELEVANCE_SCORE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RANKING_STRATEGY_RELEVANCE_SCORE: Int
```

Ranked by document relevance score.

 Value: 3

### RANKING_STRATEGY_SYSTEM_USAGE_COUNT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RANKING_STRATEGY_SYSTEM_USAGE_COUNT: Int
```

Ranked by number of usages from a system UI surface.

 Value: 6

### RANKING_STRATEGY_SYSTEM_USAGE_LAST_USED_TIMESTAMP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RANKING_STRATEGY_SYSTEM_USAGE_LAST_USED_TIMESTAMP: Int
```

Ranked by timestamp of last usage from a system UI surface.

 Value: 7

### RANKING_STRATEGY_USAGE_COUNT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RANKING_STRATEGY_USAGE_COUNT: Int
```

Ranked by number of usages, as reported by the app.

 Value: 4

### RANKING_STRATEGY_USAGE_LAST_USED_TIMESTAMP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RANKING_STRATEGY_USAGE_LAST_USED_TIMESTAMP: Int
```

Ranked by timestamp of last usage, as reported by the app.

 Value: 5

### SCHEMA_TYPE_WILDCARD

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions)

```
static val SCHEMA_TYPE_WILDCARD: String
```

Schema type to be used in addFilterProperties and addProjection to apply property paths to all results, excepting any types that have had their own, specific property paths set.

 Value: "*"

### TERM_MATCH_EXACT_ONLY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TERM_MATCH_EXACT_ONLY: Int
```

Query terms will only match exact tokens in the index.

For example, a query term "foo" will only match indexed token "foo", and not "foot" or "football".

 Value: 1

### TERM_MATCH_PREFIX

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TERM_MATCH_PREFIX: Int
```

Query terms will match indexed tokens when the query term is a prefix of the token.

For example, a query term "foo" will match indexed tokens like "foo", "foot", and "football".

 Value: 2

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getAdvancedRankingExpression

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getAdvancedRankingExpression(): String
```

Get the advanced ranking expression, or "" if setRankingStrategy was not called.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getDefaultEmbeddingSearchMetricType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 16](https://developer.android.com/sdkExtensions)

```
fun getDefaultEmbeddingSearchMetricType(): Int
```

Returns the default embedding metric type used for embedding search (see search) and ranking (see setRankingStrategy).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#EMBEDDING_SEARCH_METRIC_TYPE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#EMBEDDING_SEARCH_METRIC_TYPE_COSINE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#EMBEDDING_SEARCH_METRIC_TYPE_DOT_PRODUCT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#EMBEDDING_SEARCH_METRIC_TYPE_EUCLIDEAN:kotlin.Int` |

### getEmbeddingParameters

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 16](https://developer.android.com/sdkExtensions)

```
fun getEmbeddingParameters(): MutableList<EmbeddingVector!>
```

Returns the list of EmbeddingVector that can be referenced in the query through the "getEmbeddingParameter({index})" function.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/appsearch/EmbeddingVector!>` | This value cannot be `null`. |

**See Also**

- search

### getFilterDocumentIds

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

```
fun getFilterDocumentIds(): MutableList<String!>
```

Returns the list of document ids to search over.

If empty, the query will search over all documents.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

### getFilterNamespaces

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFilterNamespaces(): MutableList<String!>
```

Returns the list of namespaces to search over.

If empty, the query will search over all namespaces.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

### getFilterPackageNames

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFilterPackageNames(): MutableList<String!>
```

Returns the list of package name filters to search over.

If empty, the query will search over all packages that the caller has access to. If package names are specified which caller doesn't have access to, then those package names will be ignored.

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

If empty, will search over all schema and properties.

Calling this function repeatedly is inefficient. Prefer to retain the Map returned by this function, rather than calling it multiple times.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!>` | This value cannot be `null`. |

### getFilterSchemas

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFilterSchemas(): MutableList<String!>
```

Returns the list of schema types to search for.

If empty, the query will search over all schema types.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

### getInformationalRankingExpressions

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 16](https://developer.android.com/sdkExtensions)

```
fun getInformationalRankingExpressions(): MutableList<String!>
```

Returns the informational ranking expressions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

**See Also**

### getJoinSpec

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getJoinSpec(): JoinSpec?
```

Returns specification on which documents need to be joined.

| Return ||
|---|---|
| JoinSpec | This value may be `null`. |

### getMaxSnippetSize

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaxSnippetSize(): Int
```

Returns the maximum size of a snippet in characters.

### getOrder

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOrder(): Int
```

Returns the order of returned search results (descending or ascending).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#ORDER_DESCENDING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#ORDER_ASCENDING:kotlin.Int` |

### getProjectionPaths

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getProjectionPaths(): MutableMap<String!, MutableList<PropertyPath!>!>
```

Returns a map from schema type to property paths to be used for projection.

If the map is empty, then all properties will be retrieved for all results.

Calling this function repeatedly is inefficient. Prefer to retain the Map returned by this function, rather than calling it multiple times.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath!>!>` | A mapping of schema types to lists of projection PropertyPath objects. This value cannot be `null`. |

### getProjections

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProjections(): MutableMap<String!, MutableList<String!>!>
```

Returns a map from schema type to property paths to be used for projection.

If the map is empty, then all properties will be retrieved for all results.

Calling this function repeatedly is inefficient. Prefer to retain the Map returned by this function, rather than calling it multiple times.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!>` | A mapping of schema types to lists of projection strings. This value cannot be `null`. |

### getPropertyWeightPaths

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getPropertyWeightPaths(): MutableMap<String!, MutableMap<PropertyPath!, Double!>!>
```

Returns properties weights to be used for scoring.

Calling this function repeatedly is inefficient. Prefer to retain the `https://developer.android.com/reference/kotlin/java/util/Map.html#` returned by this function, rather than calling it multiple times.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html!>!>` | a `https://developer.android.com/reference/kotlin/java/util/Map.html#` of schema type to an inner-map of property paths of the schema type to the weight to set for that property. This value cannot be `null`. |

### getPropertyWeights

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getPropertyWeights(): MutableMap<String!, MutableMap<String!, Double!>!>
```

Returns properties weights to be used for scoring.

Calling this function repeatedly is inefficient. Prefer to retain the `https://developer.android.com/reference/kotlin/java/util/Map.html#` returned by this function, rather than calling it multiple times.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html!>!>` | a `https://developer.android.com/reference/kotlin/java/util/Map.html#` of schema type to an inner-map of property paths of the schema type to the weight to set for that property. This value cannot be `null`. |

### getRankingStrategy

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRankingStrategy(): Int
```

Returns the ranking strategy.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_DOCUMENT_SCORE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_CREATION_TIMESTAMP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_RELEVANCE_SCORE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_USAGE_COUNT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_USAGE_LAST_USED_TIMESTAMP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_SYSTEM_USAGE_COUNT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_SYSTEM_USAGE_LAST_USED_TIMESTAMP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_JOIN_AGGREGATE_SCORE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_ADVANCED_RANKING_EXPRESSION:kotlin.Int` |

### getResultCountPerPage

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getResultCountPerPage(): Int
```

Returns the number of results per page in the result set.

### getResultGroupingLimit

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getResultGroupingLimit(): Int
```

Get the maximum number of results to return for each group.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum number of results to return for each group or 0 if setResultGrouping was not called. |

### getResultGroupingTypeFlags

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getResultGroupingTypeFlags(): Int
```

Get the type of grouping limit to apply, or 0 if setResultGrouping was not called.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#GROUPING_TYPE_PER_PACKAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#GROUPING_TYPE_PER_NAMESPACE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#GROUPING_TYPE_PER_SCHEMA:kotlin.Int` |

### getSearchSourceLogTag

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getSearchSourceLogTag(): String?
```

Gets a tag to indicate the source of this search, or `null` if setSearchSourceLogTag was not called.

Some AppSearch implementations may log a hash of this tag using statsd. This tag may be used for tracing performance issues and crashes to a component of an app.

Call setSearchSourceLogTag and give a unique value if you want to distinguish this search scenario with other search scenarios during performance analysis.

Under no circumstances will AppSearch log the raw String value using statsd, but it will be provided as-is to custom `AppSearchLogger` implementations you have registered in your app.

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

- search

### getSnippetCount

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSnippetCount(): Int
```

Returns how many documents to generate snippets for.

### getSnippetCountPerProperty

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSnippetCountPerProperty(): Int
```

Returns how many matches for each property of a matching document to generate snippets for.

### getTermMatch

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTermMatch(): Int
```

Returns how the query terms should match terms in the index.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#TERM_MATCH_EXACT_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#TERM_MATCH_PREFIX:kotlin.Int` |

### isListFilterHasPropertyFunctionEnabled

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions)

```
fun isListFilterHasPropertyFunctionEnabled(): Boolean
```

Returns whether the LIST_FILTER_HAS_PROPERTY_FUNCTION feature is enabled.

### isListFilterMatchScoreExpressionFunctionEnabled

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

```
fun isListFilterMatchScoreExpressionFunctionEnabled(): Boolean
```

Returns whether the LIST_FILTER_MATCH_SCORE_EXPRESSION_FUNCTION feature is enabled.

### isListFilterQueryLanguageEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun isListFilterQueryLanguageEnabled(): Boolean
```

Returns whether the LIST_FILTER_QUERY_LANGUAGE feature is enabled.

### isNumericSearchEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun isNumericSearchEnabled(): Boolean
```

Returns whether the NUMERIC_SEARCH feature is enabled.

### isScorablePropertyRankingEnabled

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

```
fun isScorablePropertyRankingEnabled(): Boolean
```

Returns whether the ScorablePropertyRanking feature is enabled.

### isVerbatimSearchEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun isVerbatimSearchEnabled(): Boolean
```

Returns whether the VERBATIM_SEARCH feature is enabled.

### shouldRetrieveEmbeddingMatchInfos

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 18](https://developer.android.com/sdkExtensions)

```
fun shouldRetrieveEmbeddingMatchInfos(): Boolean
```

Returns whether to retrieve embedding match infos as a part of getMatchInfos

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
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions)

```
static val CREATOR: Parcelable.Creator<SearchSpec!>
```

Creator class for SearchSpec.
