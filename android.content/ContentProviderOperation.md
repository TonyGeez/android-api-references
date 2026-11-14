# ContentProviderOperation

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentProviderOperation

Kotlin| [Java](../android/content/ContentProviderOperation.md) 
| --- | --- |

```
open class ContentProviderOperation : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.ContentProviderOperation](../android/content/ContentProviderOperation.md) |

Represents a single operation to be performed as part of a batch of operations.

## Summary

| Nested classes ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Builder](../android/content/ContentProviderOperation.Builder.md) Used to add parameters to a [ContentProviderOperation](../android/content/ContentProviderOperation.md). |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ContentProviderResult](../android/content/ContentProviderResult.md) | [apply](../android/content/ContentProviderOperation.md))`(`provider:` ` [ContentProvider](../android/content/ContentProvider.md)`, `backRefs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](../android/content/ContentProviderResult.md)!>`, `numBackRefs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Applies this operation using the given provider. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/content/ContentProviderOperation.md))`()` <br /> |
| open [Uri](../android/net/Uri.md) | [getUri](../android/content/ContentProviderOperation.md))`()` Gets the Uri for the target of the operation. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAssertQuery](../android/content/ContentProviderOperation.md))`()` Returns true if the operation represents an assert query. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCall](../android/content/ContentProviderOperation.md))`()` Returns true if the operation represents a android. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDelete](../android/content/ContentProviderOperation.md))`()` Returns true if the operation represents a android. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExceptionAllowed](../android/content/ContentProviderOperation.md))`()` Returns true if this operation allows subsequent operations to continue even if this operation throws an exception. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInsert](../android/content/ContentProviderOperation.md))`()` Returns true if the operation represents a android. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOperation](../android/content/ContentProviderOperation.md))`()` Returns true if the operation represents an assert query. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUpdate](../android/content/ContentProviderOperation.md))`()` Returns true if the operation represents a android. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWriteOperation](../android/content/ContentProviderOperation.md))`()` Returns true if the operation represents an insertion, deletion, or update. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isYieldAllowed](../android/content/ContentProviderOperation.md))`()` Returns true if the operation allows yielding the database to other transactions if the database is contended. |
| --- | --- |
| openstatic [ContentProviderOperation.Builder](../android/content/ContentProviderOperation.Builder.md) | [newAssertQuery](../android/content/ContentProviderOperation.md))`(`uri:` ` [Uri](../android/net/Uri.md)`)` Create a [Builder](../android/content/ContentProviderOperation.Builder.md) suitable for building a [ContentProviderOperation](../android/content/ContentProviderOperation.md) to assert a set of values as provided through [Builder.withValues(ContentValues)](../android/content/ContentProviderOperation.Builder.md)). |
| openstatic [ContentProviderOperation.Builder](../android/content/ContentProviderOperation.Builder.md) | [newCall](../android/content/ContentProviderOperation.md))`(`uri:` ` [Uri](../android/net/Uri.md)`, `method:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `arg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Create a [Builder](../android/content/ContentProviderOperation.Builder.md) suitable for building an operation that will invoke android. |
| openstatic [ContentProviderOperation.Builder](../android/content/ContentProviderOperation.Builder.md) | [newDelete](../android/content/ContentProviderOperation.md))`(`uri:` ` [Uri](../android/net/Uri.md)`)` Create a [Builder](../android/content/ContentProviderOperation.Builder.md) suitable for building an operation that will invoke android. |
| --- | --- |
| openstatic [ContentProviderOperation.Builder](../android/content/ContentProviderOperation.Builder.md) | [newInsert](../android/content/ContentProviderOperation.md))`(`uri:` ` [Uri](../android/net/Uri.md)`)` Create a [Builder](../android/content/ContentProviderOperation.Builder.md) suitable for building an operation that will invoke android. |
| openstatic [ContentProviderOperation.Builder](../android/content/ContentProviderOperation.Builder.md) | [newUpdate](../android/content/ContentProviderOperation.md))`(`uri:` ` [Uri](../android/net/Uri.md)`)` Create a [Builder](../android/content/ContentProviderOperation.Builder.md) suitable for building an operation that will invoke android. |
| open [Bundle](../android/os/Bundle.md)? | [resolveExtrasBackReferences](../android/content/ContentProviderOperation.md))`(`backRefs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](../android/content/ContentProviderResult.md)!>`, `numBackRefs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the extras for this operation after resolving any requested back-references using the given results. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [resolveSelectionArgsBackReferences](../android/content/ContentProviderOperation.md))`(`backRefs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](../android/content/ContentProviderResult.md)!>`, `numBackRefs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the selection arguments for this operation after resolving any requested back-references using the given results. |
| open [ContentValues](../android/content/ContentValues.md)? | [resolveValueBackReferences](../android/content/ContentProviderOperation.md))`(`backRefs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](../android/content/ContentProviderResult.md)!>`, `numBackRefs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the values for this operation after resolving any requested back-references using the given results. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/content/ContentProviderOperation.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/content/ContentProviderOperation.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ContentProviderOperation](../android/content/ContentProviderOperation.md)!\> | [CREATOR](../android/content/ContentProviderOperation.md) <br /> |

## Public methods

### apply

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun apply(
    provider: ContentProvider, 
    backRefs: Array<ContentProviderResult!>, 
    numBackRefs: Int
): ContentProviderResult
```

Applies this operation using the given provider. The backRefs array is used to resolve any back references that were requested using [Builder.withValueBackReferences(ContentValues)](../android/content/ContentProviderOperation.Builder.md))and android.content.ContentProviderOperation.Builder#withSelectionBackReference.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [ContentProvider](../android/content/ContentProvider.md):the [ContentProvider](../android/content/ContentProvider.md) on which this batch is applied This value cannot be`null`. |
| `backRefs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentProviderResult](../android/content/ContentProviderResult.md)!\>:a [ContentProviderResult](../android/content/ContentProviderResult.md) array that will be consulted to resolve any requested back references. This value cannot be`null`. |
| `numBackRefs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of valid results on the backRefs array. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentProviderResult](../android/content/ContentProviderResult.md) | a [ContentProviderResult](../android/content/ContentProviderResult.md) that contains either the [Uri](../android/net/Uri.md) of the inserted row if this was an insert otherwise the number of rows affected. This value cannot be`null`. |

| Exceptions ||
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| `android.content.OperationApplicationException` | thrown if either the insert fails or if the number of rows affected didn't match the expected count |

### describeContents

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getUri

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUri(): Uri
```

Gets the Uri for the target of the operation.

| Return ||
|-----------------------------------------------------------------------------|-----------------------------|
| [Uri](../android/net/Uri.md) | This value cannot be`null`. |

### isAssertQuery

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAssertQuery(): Boolean
```

Returns true if the operation represents an assert query. 
**See Also**

- [#newAssertQuery](../android/content/ContentProviderOperation.md)) 

### isCall

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isCall(): Boolean
```

Returns true if the operation represents a android.content.ContentProvider#call operation. 
**See Also**

- [#newCall](../android/content/ContentProviderOperation.md)) 

### isDelete

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isDelete(): Boolean
```

Returns true if the operation represents a android.content.ContentProvider#delete operation. 
**See Also**

- [#newDelete](../android/content/ContentProviderOperation.md)) 

### isExceptionAllowed

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isExceptionAllowed(): Boolean
```

Returns true if this operation allows subsequent operations to continue even if this operation throws an exception. When true, any encountered exception is returned via [ContentProviderResult.exception](../android/content/ContentProviderResult.md). 

### isInsert

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isInsert(): Boolean
```

Returns true if the operation represents a android.content.ContentProvider#insert operation. 
**See Also**

- [#newInsert](../android/content/ContentProviderOperation.md)) 

### isReadOperation

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isReadOperation(): Boolean
```

Returns true if the operation represents an assert query. 
**See Also**

- [#isAssertQuery](../android/content/ContentProviderOperation.md)) 

### isUpdate

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isUpdate(): Boolean
```

Returns true if the operation represents a android.content.ContentProvider#update operation. 
**See Also**

- [#newUpdate](../android/content/ContentProviderOperation.md)) 

### isWriteOperation

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isWriteOperation(): Boolean
```

Returns true if the operation represents an insertion, deletion, or update. 
**See Also**

- [#isInsert](../android/content/ContentProviderOperation.md))
- [#isDelete](../android/content/ContentProviderOperation.md))
- [#isUpdate](../android/content/ContentProviderOperation.md)) 

### isYieldAllowed

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isYieldAllowed(): Boolean
```

Returns true if the operation allows yielding the database to other transactions if the database is contended. 
**See Also**

- [android.database.sqlite.SQLiteDatabase#yieldIfContendedSafely()](../android/database/sqlite/SQLiteDatabase.md)) 

### newAssertQuery

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newAssertQuery(uri: Uri): ContentProviderOperation.Builder
```

Create a [Builder](../android/content/ContentProviderOperation.Builder.md) suitable for building a [ContentProviderOperation](../android/content/ContentProviderOperation.md) to assert a set of values as provided through [Builder.withValues(ContentValues)](../android/content/ContentProviderOperation.Builder.md)).

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android/net/Uri.md):This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ContentProviderOperation.Builder](../android/content/ContentProviderOperation.Builder.md) | This value cannot be`null`. |

### newCall

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newCall(
    uri: Uri, 
    method: String?, 
    arg: String?
): ContentProviderOperation.Builder
```

Create a [Builder](../android/content/ContentProviderOperation.Builder.md) suitable for building an operation that will invoke android.content.ContentProvider#call.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android/net/Uri.md):The [Uri](../android/net/Uri.md) that is the target of the operation. This value cannot be`null`. |
| `method` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `arg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ContentProviderOperation.Builder](../android/content/ContentProviderOperation.Builder.md) | This value cannot be`null`. |

### newDelete

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newDelete(uri: Uri): ContentProviderOperation.Builder
```

Create a [Builder](../android/content/ContentProviderOperation.Builder.md) suitable for building an operation that will invoke android.content.ContentProvider#delete.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android/net/Uri.md):The [Uri](../android/net/Uri.md) that is the target of the operation. This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ContentProviderOperation.Builder](../android/content/ContentProviderOperation.Builder.md) | This value cannot be`null`. |

### newInsert

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInsert(uri: Uri): ContentProviderOperation.Builder
```

Create a [Builder](../android/content/ContentProviderOperation.Builder.md) suitable for building an operation that will invoke android.content.ContentProvider#insert.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android/net/Uri.md):The [Uri](../android/net/Uri.md) that is the target of the operation. This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ContentProviderOperation.Builder](../android/content/ContentProviderOperation.Builder.md) | This value cannot be`null`. |

### newUpdate

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newUpdate(uri: Uri): ContentProviderOperation.Builder
```

Create a [Builder](../android/content/ContentProviderOperation.Builder.md) suitable for building an operation that will invoke android.content.ContentProvider#update.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android/net/Uri.md):The [Uri](../android/net/Uri.md) that is the target of the operation. This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ContentProviderOperation.Builder](../android/content/ContentProviderOperation.Builder.md) | This value cannot be`null`. |

### resolveExtrasBackReferences

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resolveExtrasBackReferences(
    backRefs: Array<ContentProviderResult!>, 
    numBackRefs: Int
): Bundle?
```

Return the extras for this operation after resolving any requested back-references using the given results.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `backRefs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentProviderResult](../android/content/ContentProviderResult.md)!\>:the results to use when resolving any back-references This value cannot be`null`. |
| `numBackRefs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of results which are valid |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [Bundle](../android/os/Bundle.md)? | This value may be`null`. |

### resolveSelectionArgsBackReferences

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resolveSelectionArgsBackReferences(
    backRefs: Array<ContentProviderResult!>, 
    numBackRefs: Int
): Array<String!>?
```

Return the selection arguments for this operation after resolving any requested back-references using the given results.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `backRefs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentProviderResult](../android/content/ContentProviderResult.md)!\>:the results to use when resolving any back-references This value cannot be`null`. |
| `numBackRefs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of results which are valid |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>? | This value may be`null`. |

### resolveValueBackReferences

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun resolveValueBackReferences(
    backRefs: Array<ContentProviderResult!>, 
    numBackRefs: Int
): ContentValues?
```

Return the values for this operation after resolving any requested back-references using the given results.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `backRefs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentProviderResult](../android/content/ContentProviderResult.md)!\>:the results to use when resolving any back-references This value cannot be`null`. |
| `numBackRefs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of results which are valid |

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------|
| [ContentValues](../android/content/ContentValues.md)? | This value may be`null`. |

### toString

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ContentProviderOperation!>
```
