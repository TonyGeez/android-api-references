Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

# JoinSpec

```
class JoinSpec : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.appsearch.JoinSpec](https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#) |

This class represents the specifications for the joining operation in search.

Joins are only possible for matching on the qualified id of an outer document and a property value within a subquery document. In the subquery documents, these values may be referred to with a property path such as "email.recipient.id" or "entityId" or a property expression. One such property expression is "this.qualifiedId()", which refers to the document's combined package, database, namespace, and id.

Note that in order for perform the join, the property referred to by `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#getChildPropertyExpression()` has to be a property with `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema.StringPropertyConfig#getJoinableValueType()` set to `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema.StringPropertyConfig#JOINABLE_VALUE_TYPE_QUALIFIED_ID:kotlin.Int`. Otherwise no documents will be joined to any `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult`.

Take these outer query and subquery results for example:

```kotlin
<code>Outer result {
    id: id1
    score: 5
  }
  Subquery result 1 {
    id: id2
    score: 2
    entityId: pkg$db/ns#id1
    notes: This is some doc
  }
  Subquery result 2 {
    id: id3
    score: 3
    entityId: pkg$db/ns#id2
    notes: This is another doc
  }
  </code>
```

In this example, subquery result 1 contains a property "entityId" whose value is "pkg$db/ns#id1", referring to the outer result. If you call `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec.Builder` with "entityId", we will retrieve the value of the property "entityId" from the child document, which is "pkg$db#ns/id1". Let's say the qualified id of the outer result is "pkg$db#ns/id1". This would mean the subquery result 1 document will be matched to that parent document. This is done by adding a `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult` containing the child document to the top-level parent `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#getJoinedResults()`.

If `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#getChildPropertyExpression()` is "notes", we will check the values of the notes property in the subquery results. In subquery result 1, this values is "This is some doc", which does not equal the qualified id of the outer query result. As such, subquery result 1 will not be joined to the outer query result.

It's possible to define an advanced ranking strategy in the nested `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec` and also use `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_JOIN_AGGREGATE_SCORE:kotlin.Int` in the outer `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec`. In this case, the parents will be ranked based on an aggregation, such as the sum, of the signals calculated by scoring the joined documents with the advanced ranking strategy.

In terms of scoring, if `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_JOIN_AGGREGATE_SCORE:kotlin.Int` is set in `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#getRankingStrategy()`, the scores of the outer SearchResults can be influenced by the ranking signals of the subquery results. For example, if the `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#getAggregationScoringStrategy()` is set to:

- `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_MIN_RANKING_SIGNAL:kotlin.Int`, the ranking signal of the outer `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult` will be set to the minimum of the ranking signals of the subquery results. In this case, it will be the minimum of 2 and 3, which is 2.
- `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_MAX_RANKING_SIGNAL:kotlin.Int`, the ranking signal of the outer `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult` will be 3.
- `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_AVG_RANKING_SIGNAL:kotlin.Int`, the ranking signal of the outer `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult` will be 2.5.
- `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_RESULT_COUNT:kotlin.Int`, the ranking signal of the outer `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult` will be 2 as there are two joined results.
- `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_SUM_RANKING_SIGNAL:kotlin.Int`, the ranking signal of the outer `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult` will be 5, the sum of 2 and 3.
- `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_OUTER_RESULT_RANKING_SIGNAL:kotlin.Int`, the ranking signal of the outer `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult` will stay as it is.

Referring to "this.childrenRankingSignals()" in the ranking signal of the outer query will return the signals calculated by scoring the joined documents using the scoring strategy in the nested `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec`, as in `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult#getRankingSignal()`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec.Builder` Builder for `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_AVG_RANKING_SIGNAL:kotlin.Int` Score the aggregation of joined documents using the average ranking signal. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_MAX_RANKING_SIGNAL:kotlin.Int` Score the aggregation of joined documents using the largest ranking signal. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_MIN_RANKING_SIGNAL:kotlin.Int` Score the aggregation of joined documents using the smallest ranking signal. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_OUTER_RESULT_RANKING_SIGNAL:kotlin.Int` Do not score the aggregation of joined documents. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_RESULT_COUNT:kotlin.Int` Score the aggregation of joined documents by counting the number of results. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_SUM_RANKING_SIGNAL:kotlin.Int` Score the aggregation of joined documents using the sum of ranking signal. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#getAggregationScoringStrategy()()` Gets the joined document list scoring strategy. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#getChildPropertyExpression()()` The property expression that is used to get values from child documents, returned from the nested search. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#getMaxJoinedResultCount()()` Returns the max amount of `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult` objects to return with the parent document, with a default of 10 SearchResults. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#getNestedQuery()()` Returns the query to run on the joined documents. |
| [SearchSpec](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec) | `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#getNestedSearchSpec()()` Returns the search spec used to retrieve the joined documents. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [JoinSpec](https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#CREATOR:android.os.Parcelable.Creator` Creator class for `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#`. |

## Constants

### AGGREGATION_SCORING_AVG_RANKING_SIGNAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
static val AGGREGATION_SCORING_AVG_RANKING_SIGNAL: Int
```

Score the aggregation of joined documents using the average ranking signal.

 Value: 3

### AGGREGATION_SCORING_MAX_RANKING_SIGNAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
static val AGGREGATION_SCORING_MAX_RANKING_SIGNAL: Int
```

Score the aggregation of joined documents using the largest ranking signal.

 Value: 4

### AGGREGATION_SCORING_MIN_RANKING_SIGNAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
static val AGGREGATION_SCORING_MIN_RANKING_SIGNAL: Int
```

Score the aggregation of joined documents using the smallest ranking signal.

 Value: 2

### AGGREGATION_SCORING_OUTER_RESULT_RANKING_SIGNAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
static val AGGREGATION_SCORING_OUTER_RESULT_RANKING_SIGNAL: Int
```

Do not score the aggregation of joined documents. This is for the case where we want to perform a join, but keep the parent ranking signal.

 Value: 0

### AGGREGATION_SCORING_RESULT_COUNT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
static val AGGREGATION_SCORING_RESULT_COUNT: Int
```

Score the aggregation of joined documents by counting the number of results.

 Value: 1

### AGGREGATION_SCORING_SUM_RANKING_SIGNAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
static val AGGREGATION_SCORING_SUM_RANKING_SIGNAL: Int
```

Score the aggregation of joined documents using the sum of ranking signal.

 Value: 5

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

### getAggregationScoringStrategy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getAggregationScoringStrategy(): Int
```

Gets the joined document list scoring strategy.

The default scoring strategy is `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_OUTER_RESULT_RANKING_SIGNAL:kotlin.Int`, which specifies that the score of the outer parent document will be used.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_OUTER_RESULT_RANKING_SIGNAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_RESULT_COUNT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_MIN_RANKING_SIGNAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_AVG_RANKING_SIGNAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_MAX_RANKING_SIGNAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#AGGREGATION_SCORING_SUM_RANKING_SIGNAL:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec#RANKING_STRATEGY_JOIN_AGGREGATE_SCORE:kotlin.Int`

### getChildPropertyExpression

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getChildPropertyExpression(): String
```

The property expression that is used to get values from child documents, returned from the nested search. These values are then used to match them to parent documents. These are analogous to foreign keys.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the property expression to match in the child documents. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec.Builder`

### getMaxJoinedResultCount

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getMaxJoinedResultCount(): Int
```

Returns the max amount of `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult` objects to return with the parent document, with a default of 10 SearchResults.

### getNestedQuery

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getNestedQuery(): String
```

Returns the query to run on the joined documents.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getNestedSearchSpec

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getNestedSearchSpec(): SearchSpec
```

Returns the search spec used to retrieve the joined documents.

If `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec.Builder#setNestedSearch(kotlin.String,%20android.app.appsearch.SearchSpec)` is never called, this will return a `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec` with all default values. This will match every document, as the nested search query will be "" and no schema will be filtered out.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchSpec` | This value cannot be `null`. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions)

```
static val CREATOR: Parcelable.Creator<JoinSpec!>
```

Creator class for `https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec#`.
