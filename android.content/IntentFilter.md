Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntentFilter

Kotlin | [Java](IntentFilter.md)
| --- | --- |

```
open class IntentFilter : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.IntentFilter](IntentFilter.md) |

Structured description of Intent values to be matched. An IntentFilter can match against actions, categories, and data (either via its type, scheme, and/or path) in an Intent. It also includes a "priority" value which is used to order multiple matching filters.

IntentFilter objects are often created in XML as part of a package's `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifest:kotlin.IntArray` file, using `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestIntentFilter:kotlin.IntArray` tags.

There are three Intent characteristics you can filter on: the *action* , *data* , and *categories* . For each of these characteristics you can provide multiple possible matching values (via addAction, addDataType, addDataScheme, addDataSchemeSpecificPart, addDataAuthority, addDataPath, and addCategory, respectively). For actions, if no data characteristics are specified, then the filter will only match intents that contain no data.

The data characteristic is itself divided into three attributes: type, scheme, authority, and path. Any that are specified must match the contents of the Intent. If you specify a scheme but no type, only Intent that does not have a type (such as mailto:) will match; a content: URI will never match because they always have a MIME type that is supplied by their content provider. Specifying a type with no scheme has somewhat special meaning: it will match either an Intent with no URI field, or an Intent with a content: or file: URI. If you specify neither, then only an Intent with no data or type will match. To specify an authority, you must also specify one or more schemes that it is associated with. To specify a path, you also must specify both one or more authorities and one or more schemes it is associated with.
|
| ### Developer Guides
|
| For information about how to create and resolve intents, read the [Intents and Intent Filters](https://developer.android.com/guide/topics/intents/intents-filters.html) developer guide.

### Filter Rules

A match is based on the following rules. Note that for an IntentFilter to match an Intent, three conditions must hold: the **action** and **category** must match, and the data (both the **data type** and **data scheme+authority+path** if specified) must match (see match for more details on how the data fields match).

**Action** matches if any of the given values match the Intent action; if the filter specifies no actions, then it will only match Intents that do not contain an action.

**Data Type** matches if any of the given values match the Intent type. The Intent type is determined by calling android.content.Intent#resolveType. A wildcard can be used for the MIME sub-type, in both the Intent and IntentFilter, so that the type "audio/\*" will match "audio/mpeg", "audio/aiff", "audio/\*", etc. *Note that MIME type matching here is **case sensitive**, unlike formal RFC MIME types!* You should thus always use lower case letters for your MIME types.

**Data Scheme** matches if any of the given values match the Intent data's scheme. The Intent scheme is determined by calling getData and getScheme on that URI. *Note that scheme matching here is **case sensitive**, unlike formal RFC schemes!* You should thus always use lower case letters for your schemes.

**Data Scheme Specific Part** matches if any of the given values match the Intent's data scheme specific part *and* one of the data schemes in the filter has matched the Intent, *or* no scheme specific parts were supplied in the filter. The Intent scheme specific part is determined by calling getData and getSchemeSpecificPart on that URI. *Note that scheme specific part matching is **case sensitive**.*

**Data Authority** matches if any of the given values match the Intent's data authority *and* one of the data schemes in the filter has matched the Intent, *or* no authorities were supplied in the filter. The Intent authority is determined by calling getData and getAuthority on that URI. *Note that authority matching here is **case sensitive**, unlike formal RFC host names!* You should thus always use lower case letters for your authority.

**Data Path** matches if any of the given values match the Intent's data path *and* both a scheme and authority in the filter has matched against the Intent, *or* no paths were supplied in the filter. The Intent authority is determined by calling getData and getPath on that URI.

**Categories** match if *all* of the categories in the Intent match categories given in the filter. Extra categories in the filter that are not in the Intent will not cause the match to fail. Note that unlike the action, an IntentFilter with no categories will only match an Intent that does not have any categories.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/content/IntentFilter.AuthorityEntry` This is an entry for a single authority in the Iterator returned by authoritiesIterator. |
| open | `https://developer.android.com/reference/kotlin/android/content/IntentFilter.MalformedMimeTypeException` This exception is thrown when a given MIME type does not have a valid syntax. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_ADJUSTMENT_MASK:kotlin.Int` The part of a match constant that applies a quality adjustment to the basic category of match. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_ADJUSTMENT_NORMAL:kotlin.Int` Quality adjustment applied to the category of match that signifies the default, base value; higher numbers improve the quality while lower numbers reduce it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_EMPTY:kotlin.Int` The filter matched an intent that had no data specified. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_HOST:kotlin.Int` The filter matched an intent with the same data URI scheme and authority host. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_MASK:kotlin.Int` The part of a match constant that describes the category of match that occurred. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_PATH:kotlin.Int` The filter matched an intent with the same data URI scheme, authority, and path. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_PORT:kotlin.Int` The filter matched an intent with the same data URI scheme and authority host and port. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_SCHEME:kotlin.Int` The filter matched an intent with the same data URI scheme. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_SCHEME_SPECIFIC_PART:kotlin.Int` The filter matched an intent with the same data URI scheme and scheme specific part. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_TYPE:kotlin.Int` The filter matched an intent with the same data MIME type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/IntentFilter#NO_MATCH_ACTION:kotlin.Int` The filter didn't match due to different actions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/IntentFilter#NO_MATCH_CATEGORY:kotlin.Int` The filter didn't match because it required one or more categories that were not in the Intent. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/IntentFilter#NO_MATCH_DATA:kotlin.Int` The filter didn't match due to different data URIs. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/IntentFilter#NO_MATCH_TYPE:kotlin.Int` The filter didn't match due to different MIME types. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/IntentFilter#SYSTEM_HIGH_PRIORITY:kotlin.Int` The filter setPriority value at which system high-priority receivers are placed; that is, receivers that should execute before application code. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/IntentFilter#SYSTEM_LOW_PRIORITY:kotlin.Int` The filter setPriority value at which system low-priority receivers are placed; that is, receivers that should execute after application code. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| IntentFilter New empty IntentFilter. |
| IntentFilter New IntentFilter containing a copy of an existing filter. |
| IntentFilter New IntentFilter that matches a single action with no data. |
| IntentFilter New IntentFilter that matches a single action and data type. |

| Public methods ||
|---|---|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | actionsIterator Return an iterator over the filter's actions. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addAction Add a new Intent action to match against. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addCategory Add a new Intent category to match against. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addDataAuthority Add a new Intent data authority to match against. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addDataPath Add a new Intent data path to match against. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addDataScheme Add a new Intent data scheme to match against. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addDataSchemeSpecificPart Add a new Intent data "scheme specific part" to match against. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addDataType Add a new Intent data type to match against. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addUriRelativeFilterGroup Add a new URI relative filter group to match against the Intent data. |
| --- | --- |
| open [Predicate](../java.util.function/Predicate.md)\< [Intent](Intent.md)!\> | asPredicate Return a `https://developer.android.com/reference/kotlin/java/util/function/Predicate.html#` which tests whether this filter matches the given intent. |
| open [Predicate](../java.util.function/Predicate.md)\< [Intent](Intent.md)!\> | asPredicateWithTypeResolution Return a `https://developer.android.com/reference/kotlin/java/util/function/Predicate.html#` which tests whether this filter matches the given intent. |
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [IntentFilter.AuthorityEntry](../android/content/IntentFilter.AuthorityEntry.md)!\>! | authoritiesIterator Return an iterator over the filter's data authorities. |
| --- | --- |
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | categoriesIterator Return an iterator over the filter's categories. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clearUriRelativeFilterGroups Removes all existing URI relative filter groups in the intent filter. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | countActions Return the number of actions in the filter. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | countCategories Return the number of categories in the filter. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | countDataAuthorities Return the number of data authorities in the filter. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | countDataPaths Return the number of data paths in the filter. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | countDataSchemeSpecificParts Return the number of data scheme specific parts in the filter. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | countDataSchemes Return the number of data schemes in the filter. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | countDataTypes Return the number of data types in the filter. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | countUriRelativeFilterGroups Return the number of URI relative filter groups in the intent filter. |
| open static [IntentFilter](IntentFilter.md)! | create Create a new IntentFilter instance with a specified action and MIME type, where you know the MIME type is correctly formatted. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dump <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getAction Return an action in the filter. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getCategory Return a category in the filter. |
| --- | --- |
| [IntentFilter.AuthorityEntry](../android/content/IntentFilter.AuthorityEntry.md)! | getDataAuthority Return a data authority in the filter. |
| [PatternMatcher](../android.os/PatternMatcher.md)! | getDataPath Return a data path in the filter. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getDataScheme Return a data scheme in the filter. |
| --- | --- |
| [PatternMatcher](../android.os/PatternMatcher.md)! | getDataSchemeSpecificPart Return a data scheme specific part in the filter. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getDataType Return a data type in the filter. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPriority Return the priority of this filter. |
| --- | --- |
| [UriRelativeFilterGroup](UriRelativeFilterGroup.md) | getUriRelativeFilterGroup Return a URI relative filter group in the intent filter. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasAction Is the given action included in the filter? Note that if the filter does not include any actions, false will *always* be returned. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasCategory Is the given category included in the filter? |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasDataAuthority Is the given data authority included in the filter? Note that if the filter does not include any authorities, false will *always* be returned. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasDataPath Is the given data path included in the filter? Note that if the filter does not include any paths, false will *always* be returned. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasDataScheme Is the given data scheme included in the filter? Note that if the filter does not include any scheme, false will *always* be returned. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasDataSchemeSpecificPart Is the given data scheme specific part included in the filter? Note that if the filter does not include any scheme specific parts, false will *always* be returned. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasDataType Is the given data type included in the filter? Note that if the filter does not include any type, false will *always* be returned. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | match Test whether this filter matches the given intent. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | match Test whether this filter matches the given intent data. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | matchAction Match this filter against an Intent's action. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | matchCategories Match this filter against an Intent's categories. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | matchData Match this filter against an Intent's data (type, scheme and path). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | matchDataAuthority Match this intent filter against the given Intent data. |
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [PatternMatcher](../android.os/PatternMatcher.md)!\>! | pathsIterator Return an iterator over the filter's data paths. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | readFromXml <br /> |
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [PatternMatcher](../android.os/PatternMatcher.md)!\>! | schemeSpecificPartsIterator Return an iterator over the filter's data scheme specific parts. |
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | schemesIterator Return an iterator over the filter's data schemes. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPriority Modify priority of this filter. |
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | typesIterator Return an iterator over the filter's data types. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToXml Write the contents of the IntentFilter as an XML stream. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [IntentFilter](IntentFilter.md)!\> | `https://developer.android.com/reference/kotlin/android/content/IntentFilter#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### MATCH_ADJUSTMENT_MASK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_ADJUSTMENT_MASK: Int
```

The part of a match constant that applies a quality adjustment to the basic category of match. The value `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_ADJUSTMENT_NORMAL:kotlin.Int` is no adjustment; higher numbers than that improve the quality, while lower numbers reduce it.

 Value: 65535

### MATCH_ADJUSTMENT_NORMAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_ADJUSTMENT_NORMAL: Int
```

Quality adjustment applied to the category of match that signifies the default, base value; higher numbers improve the quality while lower numbers reduce it.

 Value: 32768

### MATCH_CATEGORY_EMPTY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_CATEGORY_EMPTY: Int
```

The filter matched an intent that had no data specified.

 Value: 1048576

### MATCH_CATEGORY_HOST

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_CATEGORY_HOST: Int
```

The filter matched an intent with the same data URI scheme and authority host.

 Value: 3145728

### MATCH_CATEGORY_MASK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_CATEGORY_MASK: Int
```

The part of a match constant that describes the category of match that occurred. May be either `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_EMPTY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_SCHEME:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_SCHEME_SPECIFIC_PART:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_HOST:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_PORT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_PATH:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_TYPE:kotlin.Int`. Higher values indicate a better match.

 Value: 268369920

### MATCH_CATEGORY_PATH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_CATEGORY_PATH: Int
```

The filter matched an intent with the same data URI scheme, authority, and path.

 Value: 5242880

### MATCH_CATEGORY_PORT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_CATEGORY_PORT: Int
```

The filter matched an intent with the same data URI scheme and authority host and port.

 Value: 4194304

### MATCH_CATEGORY_SCHEME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_CATEGORY_SCHEME: Int
```

The filter matched an intent with the same data URI scheme.

 Value: 2097152

### MATCH_CATEGORY_SCHEME_SPECIFIC_PART

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_CATEGORY_SCHEME_SPECIFIC_PART: Int
```

The filter matched an intent with the same data URI scheme and scheme specific part.

 Value: 5767168

### MATCH_CATEGORY_TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_CATEGORY_TYPE: Int
```

The filter matched an intent with the same data MIME type.

 Value: 6291456

### NO_MATCH_ACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NO_MATCH_ACTION: Int
```

The filter didn't match due to different actions.

 Value: -3

### NO_MATCH_CATEGORY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NO_MATCH_CATEGORY: Int
```

The filter didn't match because it required one or more categories that were not in the Intent.

 Value: -4

### NO_MATCH_DATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NO_MATCH_DATA: Int
```

The filter didn't match due to different data URIs.

 Value: -2

### NO_MATCH_TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NO_MATCH_TYPE: Int
```

The filter didn't match due to different MIME types.

 Value: -1

### SYSTEM_HIGH_PRIORITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYSTEM_HIGH_PRIORITY: Int
```

The filter setPriority value at which system high-priority receivers are placed; that is, receivers that should execute before application code. Applications should never use filters with this or higher priorities.

 Value: 1000

**See Also**

- setPriority

### SYSTEM_LOW_PRIORITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYSTEM_LOW_PRIORITY: Int
```

The filter setPriority value at which system low-priority receivers are placed; that is, receivers that should execute after application code. Applications should never use filters with this or lower priorities.

 Value: -1000

**See Also**

- setPriority

## Public constructors

### IntentFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
IntentFilter()
```

New empty IntentFilter.

### IntentFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
IntentFilter(o: IntentFilter!)
```

New IntentFilter containing a copy of an existing filter.

| Parameters ||
|---|---|
| `o` | [IntentFilter](IntentFilter.md)!: The original filter to copy. |

### IntentFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
IntentFilter(action: String!)
```

New IntentFilter that matches a single action with no data. If no data characteristics are subsequently specified, then the filter will only match intents that contain no data.

| Parameters ||
|---|---|
| `action` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The action to match, such as Intent.ACTION_MAIN. |

### IntentFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
IntentFilter(
    action: String!, 
    dataType: String!)
```

New IntentFilter that matches a single action and data type.

*Note: MIME type matching in the Android framework is case-sensitive, unlike formal RFC MIME types. As a result, you should always write your MIME types with lower case letters, and any MIME types you receive from outside of Android should be converted to lower case before supplying them here.*

Throws `https://developer.android.com/reference/kotlin/android/content/IntentFilter.MalformedMimeTypeException` if the given MIME type is not syntactically correct.

| Parameters ||
|---|---|
| `action` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The action to match, such as Intent.ACTION_VIEW. |
| `dataType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The type to match, such as "vnd.android.cursor.dir/person". |

## Public methods

### actionsIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun actionsIterator(): MutableIterator<String!>!
```

Return an iterator over the filter's actions. If there are no actions, returns null.

### addAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addAction(action: String!): Unit
```

Add a new Intent action to match against. If any actions are included in the filter, then an Intent's action must be one of those values for it to match. If no actions are included, the Intent action is ignored.

| Parameters ||
|---|---|
| `action` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Name of the action to match, such as Intent.ACTION_VIEW. |

### addCategory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addCategory(category: String!): Unit
```

Add a new Intent category to match against. The semantics of categories is the opposite of actions -- an Intent includes the categories that it requires, all of which must be included in the filter in order to match. In other words, adding a category to the filter has no impact on matching unless that category is specified in the intent.

| Parameters ||
|---|---|
| `category` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Name of category to match, such as Intent.CATEGORY_EMBED. |

### addDataAuthority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addDataAuthority(
    host: String!, 
    port: String!
): Unit
```

Add a new Intent data authority to match against. The filter must include one or more schemes (via addDataScheme) for the authority to be considered. If any authorities are included in the filter, then an Intent's data must match one of them. If no authorities are included, then only the scheme must match.

*Note: host name in the Android framework is case-sensitive, unlike formal RFC host names. As a result, you should always write your host names with lower case letters, and any host names you receive from outside of Android should be converted to lower case before supplying them here.*

| Parameters ||
|---|---|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The host part of the authority to match. May start with a single '\*' to wildcard the front of the host name. |
| `port` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Optional port part of the authority to match. If null, any port is allowed. |

**See Also**

- matchData
- addDataScheme

### addDataPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addDataPath(
    path: String!, 
    type: Int
): Unit
```

Add a new Intent data path to match against. The filter must include one or more schemes (via addDataScheme) *and* one or more authorities (via addDataAuthority) for the path to be considered. If any paths are included in the filter, then an Intent's data must match one of them. If no paths are included, then only the scheme/authority must match.

The path given here can either be a literal that must directly match or match against a prefix, or it can be a simple globbing pattern. If the latter, you can use '\*' anywhere in the pattern to match zero or more instances of the previous character, '.' as a wildcard to match any character, and '\\' to escape the next character.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Either a raw string that must exactly match the file path, or a simple pattern, depending on type. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Determines how path will be compared to determine a match: either `https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#PATTERN_LITERAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#PATTERN_PREFIX:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#PATTERN_SUFFIX:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#PATTERN_SIMPLE_GLOB:kotlin.Int`. |

**See Also**

- matchData
- addDataScheme
- addDataAuthority

### addDataScheme

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addDataScheme(scheme: String!): Unit
```

Add a new Intent data scheme to match against. If any schemes are included in the filter, then an Intent's data must be *either* one of these schemes *or* a matching data type. If no schemes are included, then an Intent will match only if it includes no data.

*Note: scheme matching in the Android framework is case-sensitive, unlike formal RFC schemes. As a result, you should always write your schemes with lower case letters, and any schemes you receive from outside of Android should be converted to lower case before supplying them here.*

| Parameters ||
|---|---|
| `scheme` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Name of the scheme to match, such as "http". |

**See Also**

- matchData

### addDataSchemeSpecificPart

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addDataSchemeSpecificPart(
    ssp: String!, 
    type: Int
): Unit
```

Add a new Intent data "scheme specific part" to match against. The filter must include one or more schemes (via addDataScheme) for the scheme specific part to be considered. If any scheme specific parts are included in the filter, then an Intent's data must match one of them. If no scheme specific parts are included, then only the scheme must match.

The "scheme specific part" that this matches against is the string returned by getSchemeSpecificPart. For Uris that contain a path, this kind of matching is not generally of interest, since addDataAuthority and addDataPath can provide a better mechanism for matching them. However, for Uris that do not contain a path, the authority and path are empty, so this is the only way to match against the non-scheme part.

| Parameters ||
|---|---|
| `ssp` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Either a raw string that must exactly match the scheme specific part path, or a simple pattern, depending on type. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Determines how ssp will be compared to determine a match: either `https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#PATTERN_LITERAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#PATTERN_PREFIX:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#PATTERN_SUFFIX:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/os/PatternMatcher.html#PATTERN_SIMPLE_GLOB:kotlin.Int`. |

**See Also**

- matchData
- addDataScheme

### addDataType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addDataType(type: String!): Unit
```

Add a new Intent data type to match against. If any types are included in the filter, then an Intent's data must be *either* one of these types *or* a matching scheme. If no data types are included, then an Intent will only match if it specifies no data.

*Note: MIME type matching in the Android framework is case-sensitive, unlike formal RFC MIME types. As a result, you should always write your MIME types with lower case letters, and any MIME types you receive from outside of Android should be converted to lower case before supplying them here.*

Throws `https://developer.android.com/reference/kotlin/android/content/IntentFilter.MalformedMimeTypeException` if the given MIME type is not syntactically correct.

| Parameters ||
|---|---|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Name of the data type to match, such as "vnd.android.cursor.dir/person". |

**See Also**

- matchData

### addUriRelativeFilterGroup

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addUriRelativeFilterGroup(group: UriRelativeFilterGroup): Unit
```

Add a new URI relative filter group to match against the Intent data. The intent filter must include one or more schemes (via addDataScheme) *and* one or more authorities (via addDataAuthority) for the group to be considered.

Groups will be matched in the order they were added and matching will only be done if no data paths match or if none are included. If both data paths and groups are not included, then only the scheme/authority must match.

| Parameters ||
|---|---|
| `group` | [UriRelativeFilterGroup](UriRelativeFilterGroup.md): A UriRelativeFilterGroup to match the URI. This value cannot be `null`. |

**See Also**

- UriRelativeFilterGroup
- matchData
- addDataScheme
- addDataAuthority

### asPredicate

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun asPredicate(): Predicate<Intent!>
```

Return a `https://developer.android.com/reference/kotlin/java/util/function/Predicate.html#` which tests whether this filter matches the given intent.

The intent's type will always be tested using a simple getType check. To instead perform a detailed type resolution before matching, use asPredicateWithTypeResolution.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/function/Predicate.html#<https://developer.android.com/reference/kotlin/android/content/Intent!>` | This value cannot be `null`. |

### asPredicateWithTypeResolution

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun asPredicateWithTypeResolution(resolver: ContentResolver): Predicate<Intent!>
```

Return a `https://developer.android.com/reference/kotlin/java/util/function/Predicate.html#` which tests whether this filter matches the given intent.

The intent's type will always be resolved by calling resolveType before matching.

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](ContentResolver.md): to be used when calling resolveType before matching. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/function/Predicate.html#<https://developer.android.com/reference/kotlin/android/content/Intent!>` | This value cannot be `null`. |

### authoritiesIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun authoritiesIterator(): MutableIterator<IntentFilter.AuthorityEntry!>!
```

Return an iterator over the filter's data authorities.

### categoriesIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun categoriesIterator(): MutableIterator<String!>!
```

Return an iterator over the filter's categories.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | Iterator if this filter has categories or `null` if none. |

### clearUriRelativeFilterGroups

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clearUriRelativeFilterGroups(): Unit
```

Removes all existing URI relative filter groups in the intent filter.

### countActions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun countActions(): Int
```

Return the number of actions in the filter.

### countCategories

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun countCategories(): Int
```

Return the number of categories in the filter.

### countDataAuthorities

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun countDataAuthorities(): Int
```

Return the number of data authorities in the filter.

### countDataPaths

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun countDataPaths(): Int
```

Return the number of data paths in the filter.

### countDataSchemeSpecificParts

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun countDataSchemeSpecificParts(): Int
```

Return the number of data scheme specific parts in the filter.

### countDataSchemes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun countDataSchemes(): Int
```

Return the number of data schemes in the filter.

### countDataTypes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun countDataTypes(): Int
```

Return the number of data types in the filter.

### countUriRelativeFilterGroups

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun countUriRelativeFilterGroups(): Int
```

Return the number of URI relative filter groups in the intent filter.

### create

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun create(
    action: String!, 
    dataType: String!
): IntentFilter!
```

Create a new IntentFilter instance with a specified action and MIME type, where you know the MIME type is correctly formatted. This catches the `https://developer.android.com/reference/kotlin/android/content/IntentFilter.MalformedMimeTypeException` exception that the constructor can call and turns it into a runtime exception.

| Parameters ||
|---|---|
| `action` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The action to match, such as Intent.ACTION_VIEW. |
| `dataType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The type to match, such as "vnd.android.cursor.dir/person". |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/IntentFilter#!` | A new IntentFilter for the given action and type. |

**See Also**

- IntentFilter

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### dump

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dump(
    du: Printer!, 
    prefix: String!
): Unit
```

### getAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAction(index: Int): String!
```

Return an action in the filter.

### getCategory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCategory(index: Int): String!
```

Return a category in the filter.

### getDataAuthority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDataAuthority(index: Int): IntentFilter.AuthorityEntry!
```

Return a data authority in the filter.

### getDataPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDataPath(index: Int): PatternMatcher!
```

Return a data path in the filter.

### getDataScheme

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDataScheme(index: Int): String!
```

Return a data scheme in the filter.

### getDataSchemeSpecificPart

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDataSchemeSpecificPart(index: Int): PatternMatcher!
```

Return a data scheme specific part in the filter.

### getDataType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDataType(index: Int): String!
```

Return a data type in the filter.

### getPriority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPriority(): Int
```

Return the priority of this filter.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The priority of the filter. |

**See Also**

- setPriority

### getUriRelativeFilterGroup

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUriRelativeFilterGroup(index: Int): UriRelativeFilterGroup
```

Return a URI relative filter group in the intent filter.

Note: use of this method will result in a NullPointerException if no groups exists for this intent filter.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of the element to return |

| Return ||
|---|---|
| UriRelativeFilterGroup | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if index is out of range |

### hasAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasAction(action: String!): Boolean
```

Is the given action included in the filter? Note that if the filter does not include any actions, false will *always* be returned.

| Parameters ||
|---|---|
| `action` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The action to look for. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the action is explicitly mentioned in the filter. |

### hasCategory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasCategory(category: String!): Boolean
```

Is the given category included in the filter?

| Parameters ||
|---|---|
| `category` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The category that the filter supports. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the category is explicitly mentioned in the filter. |

### hasDataAuthority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasDataAuthority(data: Uri!): Boolean
```

Is the given data authority included in the filter? Note that if the filter does not include any authorities, false will *always* be returned.

| Parameters ||
|---|---|
| `data` | [Uri](../android.net/Uri.md)!: The data whose authority is being looked for. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the data string matches an authority listed in the filter. |

### hasDataPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasDataPath(data: String!): Boolean
```

Is the given data path included in the filter? Note that if the filter does not include any paths, false will *always* be returned.

| Parameters ||
|---|---|
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The data path to look for. This is without the scheme prefix. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the data string matches a path listed in the filter. |

### hasDataScheme

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasDataScheme(scheme: String!): Boolean
```

Is the given data scheme included in the filter? Note that if the filter does not include any scheme, false will *always* be returned.

| Parameters ||
|---|---|
| `scheme` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The data scheme to look for. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the scheme is explicitly mentioned in the filter. |

### hasDataSchemeSpecificPart

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasDataSchemeSpecificPart(data: String!): Boolean
```

Is the given data scheme specific part included in the filter? Note that if the filter does not include any scheme specific parts, false will *always* be returned.

| Parameters ||
|---|---|
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The scheme specific part that is being looked for. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the data string matches a scheme specific part listed in the filter. |

### hasDataType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasDataType(type: String!): Boolean
```

Is the given data type included in the filter? Note that if the filter does not include any type, false will *always* be returned.

| Parameters ||
|---|---|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The data type to look for. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the type is explicitly mentioned in the filter. |

### match

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun match(
    resolver: ContentResolver!, 
    intent: Intent!, 
    resolve: Boolean, 
    logTag: String!
): Int
```

Test whether this filter matches the given intent.

| Parameters ||
|---|---|
| `intent` | [Intent](Intent.md)!: The Intent to compare against. |
| `resolve` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, the intent's type will be resolved by calling Intent.resolveType(); otherwise a simple match against Intent.type will be performed. |
| `logTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Tag to use in debugging messages. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns either a valid match constant (a combination of `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_MASK:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_ADJUSTMENT_MASK:kotlin.Int`), or one of the error codes `https://developer.android.com/reference/kotlin/android/content/IntentFilter#NO_MATCH_TYPE:kotlin.Int` if the type didn't match, `https://developer.android.com/reference/kotlin/android/content/IntentFilter#NO_MATCH_DATA:kotlin.Int` if the scheme/path didn't match, `https://developer.android.com/reference/kotlin/android/content/IntentFilter#NO_MATCH_ACTION:kotlin.Int` if the action didn't match, or `https://developer.android.com/reference/kotlin/android/content/IntentFilter#NO_MATCH_CATEGORY:kotlin.Int` if one or more categories didn't match. |

**See Also**

- match

### match

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun match(
    action: String!, 
    type: String!, 
    scheme: String!, 
    data: Uri!, 
    categories: MutableSet<String!>!, 
    logTag: String!
): Int
```

Test whether this filter matches the given intent data. A match is only successful if the actions and categories in the Intent match against the filter, as described in IntentFilter; in that case, the match result returned will be as per matchData.

| Parameters ||
|---|---|
| `action` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The intent action to match against (Intent.getAction). |
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The intent type to match against (Intent.resolveType()). |
| `scheme` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The data scheme to match against (Intent.getScheme()). |
| --- | --- |
| `data` | [Uri](../android.net/Uri.md)!: The data URI to match against (Intent.getData()). |
| `categories` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: The categories to match against (Intent.getCategories()). |
| `logTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Tag to use in debugging messages. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns either a valid match constant (a combination of `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_MASK:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_ADJUSTMENT_MASK:kotlin.Int`), or one of the error codes `https://developer.android.com/reference/kotlin/android/content/IntentFilter#NO_MATCH_TYPE:kotlin.Int` if the type didn't match, `https://developer.android.com/reference/kotlin/android/content/IntentFilter#NO_MATCH_DATA:kotlin.Int` if the scheme/path didn't match, `https://developer.android.com/reference/kotlin/android/content/IntentFilter#NO_MATCH_ACTION:kotlin.Int` if the action didn't match, or `https://developer.android.com/reference/kotlin/android/content/IntentFilter#NO_MATCH_CATEGORY:kotlin.Int` if one or more categories didn't match. |

**See Also**

- matchData
- getAction
- getScheme
- getData
- getCategories

### matchAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun matchAction(action: String!): Boolean
```

Match this filter against an Intent's action. If the filter does not specify any actions, the match will always fail.

| Parameters ||
|---|---|
| `action` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The desired action to look for. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the action is listed in the filter. |

### matchCategories

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun matchCategories(categories: MutableSet<String!>!): String!
```

Match this filter against an Intent's categories. Each category in the Intent must be specified by the filter; if any are not in the filter, the match fails.

| Parameters ||
|---|---|
| `categories` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: The categories included in the intent, as returned by Intent.getCategories(). |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | If all categories match (success), null; else the name of the first category that didn't match. |

### matchData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun matchData(
    type: String!, 
    scheme: String!, 
    data: Uri!
): Int
```

Match this filter against an Intent's data (type, scheme and path). If the filter does not specify any types and does not specify any schemes/paths, the match will only succeed if the intent does not also specify a type or data. If the filter does not specify any schemes, it will implicitly match intents with no scheme, or the schemes "content:" or "file:" (basically performing a MIME-type only match). If the filter does not specify any MIME types, the Intent also must not specify a MIME type.

Be aware that to match against an authority, you must also specify a base scheme the authority is in. To match against a data path, both a scheme and authority must be specified. If the filter does not specify any types or schemes that it matches against, it is considered to be empty (any authority or data path given is ignored, as if it were empty as well).

*Note: MIME type, Uri scheme, and host name matching in the Android framework is case-sensitive, unlike the formal RFC definitions. As a result, you should always write these elements with lower case letters, and normalize any MIME types or Uris you receive from outside of Android to ensure these elements are lower case before supplying them here.*

| Parameters ||
|---|---|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The desired data type to look for, as returned by Intent.resolveType(). |
| `scheme` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The desired data scheme to look for, as returned by Intent.getScheme(). |
| `data` | [Uri](../android.net/Uri.md)!: The full data string to match against, as supplied in Intent.data. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns either a valid match constant (a combination of `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_MASK:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_ADJUSTMENT_MASK:kotlin.Int`), or one of the error codes `https://developer.android.com/reference/kotlin/android/content/IntentFilter#NO_MATCH_TYPE:kotlin.Int` if the type didn't match or `https://developer.android.com/reference/kotlin/android/content/IntentFilter#NO_MATCH_DATA:kotlin.Int` if the scheme/path didn't match. |

**See Also**

### matchDataAuthority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun matchDataAuthority(data: Uri!): Int
```

Match this intent filter against the given Intent data. This ignores the data scheme -- unlike matchData, the authority will match regardless of whether there is a matching scheme.

| Parameters ||
|---|---|
| `data` | [Uri](../android.net/Uri.md)!: The data whose authority is being looked for. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns either `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_HOST:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/IntentFilter#MATCH_CATEGORY_PORT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/IntentFilter#NO_MATCH_DATA:kotlin.Int`. |

### pathsIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun pathsIterator(): MutableIterator<PatternMatcher!>!
```

Return an iterator over the filter's data paths.

### readFromXml

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readFromXml(parser: XmlPullParser!): Unit
```

### schemeSpecificPartsIterator

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun schemeSpecificPartsIterator(): MutableIterator<PatternMatcher!>!
```

Return an iterator over the filter's data scheme specific parts.

### schemesIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun schemesIterator(): MutableIterator<String!>!
```

Return an iterator over the filter's data schemes.

### setPriority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPriority(priority: Int): Unit
```

Modify priority of this filter. This only affects receiver filters. The priority of activity filters are set in XML and cannot be changed programmatically. The default priority is 0. Positive values will be before the default, lower values will be after it. Applications should use a value that is larger than `https://developer.android.com/reference/kotlin/android/content/IntentFilter#SYSTEM_LOW_PRIORITY:kotlin.Int` and smaller than `https://developer.android.com/reference/kotlin/android/content/IntentFilter#SYSTEM_HIGH_PRIORITY:kotlin.Int` .

| Parameters ||
|---|---|
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new priority value. |

**See Also**

- getPriority
- `https://developer.android.com/reference/kotlin/android/content/IntentFilter#SYSTEM_LOW_PRIORITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/IntentFilter#SYSTEM_HIGH_PRIORITY:kotlin.Int`

### typesIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun typesIterator(): MutableIterator<String!>!
```

Return an iterator over the filter's data types.

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

### writeToXml

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToXml(serializer: XmlSerializer!): Unit
```

Write the contents of the IntentFilter as an XML stream.

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<IntentFilter!>
```
