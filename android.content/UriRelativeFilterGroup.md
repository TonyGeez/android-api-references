Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UriRelativeFilterGroup

Kotlin | [Java](https://developer.android.com/reference/android/content/UriRelativeFilterGroup "View this page in Java")
| --- | --- |

```
class UriRelativeFilterGroup
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.UriRelativeFilterGroup](https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#) |

An intent data matching group based on a URI's relative reference which includes the path, query and fragment. The group is only considered as matching if *all* UriRelativeFilters in the group match. Each UriRelativeFilter defines a matching rule for a URI path, query or fragment. A group must contain one or more UriRelativeFilters to match but does not need to contain UriRelativeFilters for all existing parts of a URI to match.

For example, given a URI that contains path, query and fragment parts, a group containing only a path filter will match the URI if the path filter matches the URI path. If the group contains a path and query filter, then the group will only match if both path and query filters match. If a URI contains only a path with no query or fragment then a group can only match if it contains only a matching path filter. If the group also contained additional query or fragment filters then it will not match.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#ACTION_ALLOW:kotlin.Int` Value to indicate that the group match is allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#ACTION_BLOCK:kotlin.Int` Value to indicate that the group match is blocked. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#UriRelativeFilterGroup(kotlin.Int)(action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` New UriRelativeFilterGroup that matches a Intent data. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#addUriRelativeFilter(android.content.UriRelativeFilter)(uriRelativeFilter: https://developer.android.com/reference/kotlin/android/content/UriRelativeFilter)` Add a filter to the group. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#getAction()()` Return `https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#ACTION_ALLOW:kotlin.Int` if a URI is allowed when matched and `https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#ACTION_BLOCK:kotlin.Int` if a URI is blacked when matched. |
| --- | --- |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [UriRelativeFilter](https://developer.android.com/reference/kotlin/android/content/UriRelativeFilter)!\> | `https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#getUriRelativeFilters()()` Returns a unmodifiable view of the UriRelativeFilters list in this group. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#matchData(android.net.Uri)(data: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Match all URI filter in this group against `https://developer.android.com/reference/kotlin/android/content/Intent#getData()`. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#toString()()` Returns a string representation of the object. |

## Constants

### ACTION_ALLOW

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ALLOW: Int
```

Value to indicate that the group match is allowed.

 Value: 0

### ACTION_BLOCK

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_BLOCK: Int
```

Value to indicate that the group match is blocked.

 Value: 1

## Public constructors

### UriRelativeFilterGroup

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UriRelativeFilterGroup(action: Int)
```

New UriRelativeFilterGroup that matches a Intent data.

| Parameters ||
|---|---|
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Whether this matching group should be allowed or disallowed. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#ACTION_ALLOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#ACTION_BLOCK:kotlin.Int` |

## Public methods

### addUriRelativeFilter

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addUriRelativeFilter(uriRelativeFilter: UriRelativeFilter): Unit
```

Add a filter to the group.

| Parameters ||
|---|---|
| `uriRelativeFilter` | [UriRelativeFilter](https://developer.android.com/reference/kotlin/android/content/UriRelativeFilter): This value cannot be `null`. |

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `o` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getAction

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAction(): Int
```

Return `https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#ACTION_ALLOW:kotlin.Int` if a URI is allowed when matched and `https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#ACTION_BLOCK:kotlin.Int` if a URI is blacked when matched.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#ACTION_ALLOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/UriRelativeFilterGroup#ACTION_BLOCK:kotlin.Int` |

### getUriRelativeFilters

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUriRelativeFilters(): MutableCollection<UriRelativeFilter!>
```

Returns a unmodifiable view of the UriRelativeFilters list in this group.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/content/UriRelativeFilter!>` | This value cannot be `null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### matchData

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun matchData(data: Uri): Boolean
```

Match all URI filter in this group against `https://developer.android.com/reference/kotlin/android/content/Intent#getData()`.

| Parameters ||
|---|---|
| `data` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): The full data string to match against, as supplied in Intent.data. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if all filters match. |

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
