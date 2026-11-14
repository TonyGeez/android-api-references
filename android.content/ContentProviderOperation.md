# ContentProviderOperation

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentProviderOperation

Kotlin| [Java](https://developer.android.com/reference/android/content/ContentProviderOperation "View this page in Java") 
| --- | --- |

```
open class ContentProviderOperation : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#) |

Represents a single operation to be performed as part of a batch of operations.

## Summary

| Nested classes ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) Used to add parameters to a [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult) | [apply](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#apply(android.content.ContentProvider,%20kotlin.Array,%20kotlin.Int))`(`provider:` ` [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider)`, `backRefs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult)!>`, `numBackRefs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Applies this operation using the given provider. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#describeContents())`()` <br /> |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | [getUri](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#getUri())`()` Gets the Uri for the target of the operation. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAssertQuery](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#isAssertQuery())`()` Returns true if the operation represents an assert query. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCall](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#isCall())`()` Returns true if the operation represents a android. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDelete](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#isDelete())`()` Returns true if the operation represents a android. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExceptionAllowed](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#isExceptionAllowed())`()` Returns true if this operation allows subsequent operations to continue even if this operation throws an exception. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInsert](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#isInsert())`()` Returns true if the operation represents a android. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#isReadOperation())`()` Returns true if the operation represents an assert query. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUpdate](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#isUpdate())`()` Returns true if the operation represents a android. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWriteOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#isWriteOperation())`()` Returns true if the operation represents an insertion, deletion, or update. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isYieldAllowed](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#isYieldAllowed())`()` Returns true if the operation allows yielding the database to other transactions if the database is contended. |
| --- | --- |
| openstatic [ContentProviderOperation.Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) | [newAssertQuery](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#newAssertQuery(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Create a [Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) suitable for building a [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#) to assert a set of values as provided through [Builder.withValues(ContentValues)](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder#withValues(android.content.ContentValues)). |
| openstatic [ContentProviderOperation.Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) | [newCall](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#newCall(android.net.Uri,%20kotlin.String,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `method:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `arg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Create a [Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) suitable for building an operation that will invoke android. |
| openstatic [ContentProviderOperation.Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) | [newDelete](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#newDelete(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Create a [Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) suitable for building an operation that will invoke android. |
| --- | --- |
| openstatic [ContentProviderOperation.Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) | [newInsert](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#newInsert(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Create a [Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) suitable for building an operation that will invoke android. |
| openstatic [ContentProviderOperation.Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) | [newUpdate](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#newUpdate(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Create a [Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) suitable for building an operation that will invoke android. |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | [resolveExtrasBackReferences](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#resolveExtrasBackReferences(kotlin.Array,%20kotlin.Int))`(`backRefs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult)!>`, `numBackRefs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the extras for this operation after resolving any requested back-references using the given results. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [resolveSelectionArgsBackReferences](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#resolveSelectionArgsBackReferences(kotlin.Array,%20kotlin.Int))`(`backRefs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult)!>`, `numBackRefs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the selection arguments for this operation after resolving any requested back-references using the given results. |
| open [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)? | [resolveValueBackReferences](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#resolveValueBackReferences(kotlin.Array,%20kotlin.Int))`(`backRefs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult)!>`, `numBackRefs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the values for this operation after resolving any requested back-references using the given results. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#toString())`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#CREATOR:android.os.Parcelable.Creator) <br /> |

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

Applies this operation using the given provider. The backRefs array is used to resolve any back references that were requested using [Builder.withValueBackReferences(ContentValues)](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder#withValueBackReferences(android.content.ContentValues))and android.content.ContentProviderOperation.Builder#withSelectionBackReference.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider):the [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) on which this batch is applied This value cannot be`null`. |
| `backRefs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult)!\>:a [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult) array that will be consulted to resolve any requested back references. This value cannot be`null`. |
| `numBackRefs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of valid results on the backRefs array. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult) | a [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult) that contains either the [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) of the inserted row if this was an insert otherwise the number of rows affected. This value cannot be`null`. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getUri

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUri(): Uri
```

Gets the Uri for the target of the operation.

| Return ||
|-----------------------------------------------------------------------------|-----------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | This value cannot be`null`. |

### isAssertQuery

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAssertQuery(): Boolean
```

Returns true if the operation represents an assert query. 
**See Also**

- [#newAssertQuery](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#newAssertQuery(android.net.Uri)) 

### isCall

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isCall(): Boolean
```

Returns true if the operation represents a android.content.ContentProvider#call operation. 
**See Also**

- [#newCall](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#newCall(android.net.Uri,%20kotlin.String,%20kotlin.String)) 

### isDelete

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isDelete(): Boolean
```

Returns true if the operation represents a android.content.ContentProvider#delete operation. 
**See Also**

- [#newDelete](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#newDelete(android.net.Uri)) 

### isExceptionAllowed

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isExceptionAllowed(): Boolean
```

Returns true if this operation allows subsequent operations to continue even if this operation throws an exception. When true, any encountered exception is returned via [ContentProviderResult.exception](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult#exception:kotlin.Throwable). 

### isInsert

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isInsert(): Boolean
```

Returns true if the operation represents a android.content.ContentProvider#insert operation. 
**See Also**

- [#newInsert](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#newInsert(android.net.Uri)) 

### isReadOperation

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isReadOperation(): Boolean
```

Returns true if the operation represents an assert query. 
**See Also**

- [#isAssertQuery](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#isAssertQuery()) 

### isUpdate

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isUpdate(): Boolean
```

Returns true if the operation represents a android.content.ContentProvider#update operation. 
**See Also**

- [#newUpdate](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#newUpdate(android.net.Uri)) 

### isWriteOperation

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isWriteOperation(): Boolean
```

Returns true if the operation represents an insertion, deletion, or update. 
**See Also**

- [#isInsert](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#isInsert())
- [#isDelete](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#isDelete())
- [#isUpdate](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#isUpdate()) 

### isYieldAllowed

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isYieldAllowed(): Boolean
```

Returns true if the operation allows yielding the database to other transactions if the database is contended. 
**See Also**

- [android.database.sqlite.SQLiteDatabase#yieldIfContendedSafely()](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.html#yieldIfContendedSafely()) 

### newAssertQuery

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newAssertQuery(uri: Uri): ContentProviderOperation.Builder
```

Create a [Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) suitable for building a [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#) to assert a set of values as provided through [Builder.withValues(ContentValues)](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder#withValues(android.content.ContentValues)).

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ContentProviderOperation.Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) | This value cannot be`null`. |

### newCall

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newCall(
    uri: Uri, 
    method: String?, 
    arg: String?
): ContentProviderOperation.Builder
```

Create a [Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) suitable for building an operation that will invoke android.content.ContentProvider#call.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) that is the target of the operation. This value cannot be`null`. |
| `method` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `arg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ContentProviderOperation.Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) | This value cannot be`null`. |

### newDelete

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newDelete(uri: Uri): ContentProviderOperation.Builder
```

Create a [Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) suitable for building an operation that will invoke android.content.ContentProvider#delete.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) that is the target of the operation. This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ContentProviderOperation.Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) | This value cannot be`null`. |

### newInsert

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInsert(uri: Uri): ContentProviderOperation.Builder
```

Create a [Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) suitable for building an operation that will invoke android.content.ContentProvider#insert.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) that is the target of the operation. This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ContentProviderOperation.Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) | This value cannot be`null`. |

### newUpdate

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newUpdate(uri: Uri): ContentProviderOperation.Builder
```

Create a [Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) suitable for building an operation that will invoke android.content.ContentProvider#update.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) that is the target of the operation. This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ContentProviderOperation.Builder](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.Builder) | This value cannot be`null`. |

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
| `backRefs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult)!\>:the results to use when resolving any back-references This value cannot be`null`. |
| `numBackRefs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of results which are valid |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | This value may be`null`. |

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
| `backRefs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult)!\>:the results to use when resolving any back-references This value cannot be`null`. |
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
| `backRefs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult)!\>:the results to use when resolving any back-references This value cannot be`null`. |
| `numBackRefs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of results which are valid |

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------|
| [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)? | This value may be`null`. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ContentProviderOperation!>
```
