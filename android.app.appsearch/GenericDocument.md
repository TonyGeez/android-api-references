Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GenericDocument

```
open class GenericDocument
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.GenericDocument](GenericDocument.md) |

| Known Direct Subclasses [AppSearchAccount](../android/app/appsearch/AppSearchAccount.md) |---|---| | [AppSearchAccount](../android/app/appsearch/AppSearchAccount.md) | Encapsulates a `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#` representing an `https://developer.android.com/reference/kotlin/android/accounts/Account.html#`. | |
| --- | --- | --- | --- | --- | --- | --- |

Represents a document unit.

Documents contain structured data conforming to their `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema` type. Each document is uniquely identified by a namespace and a String ID within that namespace.

Documents are constructed by using the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder`.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder` The builder class for `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#`. |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#GenericDocument(android.app.appsearch.GenericDocument)(document: https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#)` Creates a new `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#` from an existing instance. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getCreationTimestampMillis()()` Returns the creation timestamp of the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#`, in milliseconds. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getId()()` Returns the unique identifier of the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#`. |
| --- | --- |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getMaxIndexedProperties()()` The maximum number of indexed properties a document can have. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getNamespace()()` Returns the namespace of the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#`. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getProperty(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieves the property value with the given path as `https://developer.android.com/reference/kotlin/java/lang/Object.html#`. |
| --- | --- |
| open [AppSearchBlobHandle](AppSearchBlobHandle.md)? | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyBlobHandle(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieves an `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle` property by path. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [AppSearchBlobHandle](AppSearchBlobHandle.md)!\>? | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyBlobHandleArray(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieves a repeated `AppSearchBlobHandle[]` property by path. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyBoolean(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieves a `boolean` property by path. |
| --- | --- |
| open [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)? | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyBooleanArray(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieves a repeated `boolean` property by path. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyBytes(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieves a `byte[]` property by path. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyBytesArray(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieves a `byte[][]` property by path. |
| --- | --- |
| open [GenericDocument](GenericDocument.md)? | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyDocument(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieves a `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#` property by path. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [GenericDocument](GenericDocument.md)!\>? | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyDocumentArray(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieves a repeated `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#` property by path. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyDouble(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieves a `double` property by path. |
| --- | --- |
| open [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)? | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyDoubleArray(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieves a repeated `double` property by path. |
| open [EmbeddingVector](EmbeddingVector.md)? | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyEmbedding(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieves an `EmbeddingVector` property by path. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [EmbeddingVector](EmbeddingVector.md)!\>? | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyEmbeddingArray(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieves a repeated `EmbeddingVector[]` property by path. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyLong(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieves a `long` property by path. |
| open [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)? | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyLongArray(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieves a repeated `long[]` property by path. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyNames()()` Returns the names of all properties defined in this document. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyString(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieves a `https://developer.android.com/reference/kotlin/java/lang/String.html#` property by path. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyStringArray(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieves a repeated `String` property by path. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getSchemaType()()` Returns the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema` type of the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getScore()()` Returns the score of the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#`. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getTtlMillis()()` Returns the TTL (time-to-live) of the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#`, in milliseconds. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#hashCode()()` Returns a hash code value for the object. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#toString()()` Returns a string representation of the object. |

## Protected constructors

### GenericDocument

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected GenericDocument(document: GenericDocument)
```

Creates a new `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#` from an existing instance.

This method should be only used by constructor of a subclass.

| Parameters ||
|---|---|
| `document` | [GenericDocument](GenericDocument.md): This value cannot be `null`. |

## Public methods

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
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
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getCreationTimestampMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCreationTimestampMillis(): Long
```

Returns the creation timestamp of the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#`, in milliseconds.

The value is in the `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()` time base. 
Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |

### getId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getId(): String
```

Returns the unique identifier of the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getMaxIndexedProperties

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getMaxIndexedProperties(): Int
```

The maximum number of indexed properties a document can have.

Indexed properties are properties which are strings where the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema.StringPropertyConfig#getIndexingType()` value is anything other than `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema.StringPropertyConfig#INDEXING_TYPE_NONE:kotlin.Int`, as well as long properties where the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema.LongPropertyConfig#getIndexingType()` value is `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema.LongPropertyConfig#INDEXING_TYPE_RANGE:kotlin.Int`.

### getNamespace

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNamespace(): String
```

Returns the namespace of the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getProperty

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProperty(path: String): Any?
```

Retrieves the property value with the given path as `https://developer.android.com/reference/kotlin/java/lang/Object.html#`.

A path can be a simple property name, such as those returned by `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyNames()`. It may also be a dot-delimited path through the nested document hierarchy, with nested `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#` properties accessed via `'.'` and repeated properties optionally indexed into via `[n]`.

For example, given the following `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#`:

```kotlin
(Message) {
          from: "sender@example.com"
          to: [{
              name: "Albert Einstein"
              email: "einstein@example.com"
            }, {
              name: "Marie Curie"
              email: "curie@example.com"
            }]
          tags: ["important", "inbox"]
          subject: "Hello"
      }
  
```

Here are some example paths and their results:

- `"from"` returns `"sender@example.com"` as a `https://developer.android.com/reference/kotlin/java/lang/String.html#` array with one element
- `"to"` returns the two nested documents containing contact information as a `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#` array with two elements
- `"to[1]"` returns the second nested document containing Marie Curie's contact information as a `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#` array with one element
- `"to[1].email"` returns `"curie@example.com"`
- `"to[100].email"` returns `null` as this particular document does not have that many elements in its `"to"` array.
- `"to.email"` aggregates emails across all nested documents that have them, returning `["einstein@example.com", "curie@example.com"]` as a `https://developer.android.com/reference/kotlin/java/lang/String.html#` array with two elements.

If you know the expected type of the property you are retrieving, it is recommended to use one of the typed versions of this method instead, such as `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyString(kotlin.String)` or `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getPropertyStringArray(kotlin.String)`.

If the property was assigned as an empty array using one of the `Builder#setProperty` functions, this method will return an empty array. If no such property exists at all, this method returns `null`.

Note: If the property is an empty `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#`\[\] or `byte[][]`, this method will return a `null` value in versions of Android prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`. Starting in Android T it will return an empty array if the property has been set as an empty array, matching the behavior of other property types.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to look for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?` | The entry with the given path as an object or `null` if there is no such path. The returned object will be one of the following types: `String[]`, `long[]`, `double[]`, `boolean[]`, `byte[][]`, `GenericDocument[]`. |

### getPropertyBlobHandle

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

```
open fun getPropertyBlobHandle(path: String): AppSearchBlobHandle?
```

Retrieves an `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle` property by path.

See `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getProperty(kotlin.String)` for a detailed description of the path syntax.

See `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#openBlobForRead(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` for how to use `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle` to retrieve blob data.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to look for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle?` | The first `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle` associated with the given path or `null` if there is no such value or the value is of a different type. |

### getPropertyBlobHandleArray

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

```
open fun getPropertyBlobHandleArray(path: String): Array<AppSearchBlobHandle!>?
```

Retrieves a repeated `AppSearchBlobHandle[]` property by path.

See `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getProperty(kotlin.String)` for a detailed description of the path syntax.

If the property has not been set via `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyBlobHandle(kotlin.String,%20android.app.appsearch.AppSearchBlobHandle)`, this method returns `null`.

If it has been set via `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyBlobHandle(kotlin.String,%20android.app.appsearch.AppSearchBlobHandle)` to an empty `AppSearchBlobHandle[]`, this method returns an empty `AppSearchBlobHandle[]`.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to look for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle!>?` | The `AppSearchBlobHandle[]` associated with the given path, or `null` if no value is set or the value is of a different type. |

### getPropertyBoolean

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPropertyBoolean(path: String): Boolean
```

Retrieves a `boolean` property by path.

See `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getProperty(kotlin.String)` for a detailed description of the path syntax.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to look for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | The first `boolean` associated with the given path or default value `false` if there is no such value or the value is of a different type. |

### getPropertyBooleanArray

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPropertyBooleanArray(path: String): BooleanArray?
```

Retrieves a repeated `boolean` property by path.

See `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getProperty(kotlin.String)` for a detailed description of the path syntax.

If the property has not been set via `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyBoolean(kotlin.String,%20kotlin.Boolean)`, this method returns `null`.

If it has been set via `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyBoolean(kotlin.String,%20kotlin.Boolean)` to an empty `boolean[]`, this method returns an empty `boolean[]`.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to look for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html?` | The `boolean[]` associated with the given path, or `null` if no value is set or the value is of a different type. |

### getPropertyBytes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPropertyBytes(path: String): ByteArray?
```

Retrieves a `byte[]` property by path.

See `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getProperty(kotlin.String)` for a detailed description of the path syntax.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to look for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | The first `byte[]` associated with the given path or `null` if there is no such value or the value is of a different type. |

### getPropertyBytesArray

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPropertyBytesArray(path: String): Array<ByteArray!>?
```

Retrieves a `byte[][]` property by path.

See `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getProperty(kotlin.String)` for a detailed description of the path syntax.

If the property has not been set via `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyBytes(kotlin.String,%20kotlin.ByteArray)`, this method returns `null`.

If it has been set via `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyBytes(kotlin.String,%20kotlin.ByteArray)` to an empty `byte[][]`, this method returns an empty `byte[][]` starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` and `null` in earlier versions of Android.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to look for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!>?` | The `byte[][]` associated with the given path, or `null` if no value is set or the value is of a different type. |

### getPropertyDocument

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPropertyDocument(path: String): GenericDocument?
```

Retrieves a `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#` property by path.

See `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getProperty(kotlin.String)` for a detailed description of the path syntax.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to look for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#?` | The first `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#` associated with the given path or `null` if there is no such value or the value is of a different type. |

### getPropertyDocumentArray

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPropertyDocumentArray(path: String): Array<GenericDocument!>?
```

Retrieves a repeated `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#` property by path.

See `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getProperty(kotlin.String)` for a detailed description of the path syntax.

If the property has not been set via `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyDocument(kotlin.String,%20android.app.appsearch.GenericDocument)`, this method returns `null`.

If it has been set via `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyDocument(kotlin.String,%20android.app.appsearch.GenericDocument)` to an empty `GenericDocument[]`, this method returns an empty `GenericDocument[]` starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` and `null` in earlier versions of Android.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to look for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#!>?` | The `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#`\[\] associated with the given path, or `null` if no value is set or the value is of a different type. |

### getPropertyDouble

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPropertyDouble(path: String): Double
```

Retrieves a `double` property by path.

See `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getProperty(kotlin.String)` for a detailed description of the path syntax.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to look for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | The first `double` associated with the given path or default value `0.0` if there is no such value or the value is of a different type. |

### getPropertyDoubleArray

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPropertyDoubleArray(path: String): DoubleArray?
```

Retrieves a repeated `double` property by path.

See `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getProperty(kotlin.String)` for a detailed description of the path syntax.

If the property has not been set via `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyDouble(kotlin.String,%20kotlin.Double)`, this method returns `null`.

If it has been set via `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyDouble(kotlin.String,%20kotlin.Double)` to an empty `double[]`, this method returns an empty `double[]`.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to look for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html?` | The `double[]` associated with the given path, or `null` if no value is set or the value is of a different type. |

### getPropertyEmbedding

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 16](https://developer.android.com/sdkExtensions)

```
open fun getPropertyEmbedding(path: String): EmbeddingVector?
```

Retrieves an `EmbeddingVector` property by path.

See `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getProperty(kotlin.String)` for a detailed description of the path syntax.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to look for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/appsearch/EmbeddingVector?` | The first `EmbeddingVector[]` associated with the given path or `null` if there is no such value or the value is of a different type. |

### getPropertyEmbeddingArray

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 16](https://developer.android.com/sdkExtensions)

```
open fun getPropertyEmbeddingArray(path: String): Array<EmbeddingVector!>?
```

Retrieves a repeated `EmbeddingVector[]` property by path.

See `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getProperty(kotlin.String)` for a detailed description of the path syntax.

If the property has not been set via `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyEmbedding(kotlin.String,%20android.app.appsearch.EmbeddingVector)`, this method returns `null`.

If it has been set via `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyEmbedding(kotlin.String,%20android.app.appsearch.EmbeddingVector)` to an empty `EmbeddingVector[]`, this method returns an empty `EmbeddingVector[]`.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to look for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/app/appsearch/EmbeddingVector!>?` | The `EmbeddingVector[]` associated with the given path, or `null` if no value is set or the value is of a different type. |

### getPropertyLong

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPropertyLong(path: String): Long
```

Retrieves a `long` property by path.

See `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getProperty(kotlin.String)` for a detailed description of the path syntax.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to look for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The first `long` associated with the given path or default value `0` if there is no such value or the value is of a different type. |

### getPropertyLongArray

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPropertyLongArray(path: String): LongArray?
```

Retrieves a repeated `long[]` property by path.

See `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getProperty(kotlin.String)` for a detailed description of the path syntax.

If the property has not been set via `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyLong(kotlin.String,%20kotlin.Long)`, this method returns `null`.

If it has been set via `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyLong(kotlin.String,%20kotlin.Long)` to an empty `long[]`, this method returns an empty `long[]`.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to look for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html?` | The `long[]` associated with the given path, or `null` if no value is set or the value is of a different type. |

### getPropertyNames

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPropertyNames(): MutableSet<String!>
```

Returns the names of all properties defined in this document.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

### getPropertyString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPropertyString(path: String): String?
```

Retrieves a `https://developer.android.com/reference/kotlin/java/lang/String.html#` property by path.

See `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getProperty(kotlin.String)` for a detailed description of the path syntax.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to look for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The first `https://developer.android.com/reference/kotlin/java/lang/String.html#` associated with the given path or `null` if there is no such value or the value is of a different type. |

### getPropertyStringArray

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPropertyStringArray(path: String): Array<String!>?
```

Retrieves a repeated `String` property by path.

See `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getProperty(kotlin.String)` for a detailed description of the path syntax.

If the property has not been set via `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyString(kotlin.String,%20kotlin.String)`, this method returns `null`.

If it has been set via `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.Builder#setPropertyString(kotlin.String,%20kotlin.String)` to an empty `String[]`, this method returns an empty `String[]`.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to look for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | The `String[]` associated with the given path, or `null` if no value is set or the value is of a different type. |

### getSchemaType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSchemaType(): String
```

Returns the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema` type of the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getScore

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getScore(): Int
```

Returns the score of the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#`.

The score is a query-independent measure of the document's quality, relative to other `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#` objects of the same `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema` type.

Results may be sorted by score using android.app.appsearch.SearchSpec.Builder#setRankingStrategy. Documents with higher scores are considered better than documents with lower scores.

Any non-negative integer can be used a score.

### getTtlMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTtlMillis(): Long
```

Returns the TTL (time-to-live) of the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#`, in milliseconds.

The TTL is measured against `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument#getCreationTimestampMillis()`. At the timestamp of `creationTimestampMillis + ttlMillis`, measured in the `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()` time base, the document will be auto-deleted.

The default value is 0, which means the document is permanent and won't be auto-deleted until the app is uninstalled or android.app.appsearch.AppSearchSession#remove is called.

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |
