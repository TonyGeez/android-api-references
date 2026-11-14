# SQLiteQueryBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteQueryBuilder

Kotlin| [Java](https://developer.android.com/reference/android/database/sqlite/SQLiteQueryBuilder "View this page in Java") 

```
open class SQLiteQueryBuilder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.database.sqlite.SQLiteQueryBuilder](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#) |

This is a convenience class that helps build SQL queries to be sent to [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase) objects.

This class is often used to compose a SQL query from client-supplied fragments. Best practice to protect against invalid or illegal SQL is to set the following:

- [setStrict](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setStrict(kotlin.Boolean))true.
- [setProjectionMap](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setProjectionMap(kotlin.collections.MutableMap))with the list of queryable columns.
- [setStrictColumns](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setStrictColumns(kotlin.Boolean))true.
- [setStrictGrammar](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setStrictGrammar(kotlin.Boolean))true.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLiteQueryBuilder](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#SQLiteQueryBuilder())`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [appendColumns](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#appendColumns(java.lang.StringBuilder,%20kotlin.Array))`(`s:` ` [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)!`, `columns:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Add the names that are non-null in columns to s, separating them with commas. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [appendWhere](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#appendWhere(kotlin.CharSequence))`(`inWhere:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`)` Append a chunk to the`WHERE`clause of the query. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [appendWhereEscapeString](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#appendWhereEscapeString(kotlin.String))`(`inWhere:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Append a chunk to the`WHERE`clause of the query. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [appendWhereStandalone](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#appendWhereStandalone(kotlin.CharSequence))`(`inWhere:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`)` Add a standalone chunk to the`WHERE`clause of this query. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [buildQuery](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#buildQuery(kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`projectionIn:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `groupBy:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `having:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `limit:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Construct a`SELECT`statement suitable for use in a group of`SELECT`statements that will be joined through`UNION`operators in buildUnionQuery. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [buildQuery](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#buildQuery(kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`projectionIn:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `groupBy:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `having:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `limit:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [buildQueryString](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#buildQueryString(kotlin.Boolean,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`distinct:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `tables:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `columns:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `where:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `groupBy:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `having:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `orderBy:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `limit:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Build an SQL query string from the given clauses. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [buildUnionQuery](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#buildUnionQuery(kotlin.Array,%20kotlin.String,%20kotlin.String))`(`subQueries:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `limit:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Given a set of subqueries, all of which are`SELECT`statements, construct a query that returns the union of what those subqueries return. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [buildUnionSubQuery](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#buildUnionSubQuery(kotlin.String,%20kotlin.Array,%20kotlin.collections.MutableSet,%20kotlin.Int,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`typeDiscriminatorColumn:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `unionColumns:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `columnsPresentInTable:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `computedColumnsOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `typeDiscriminatorValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `groupBy:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `having:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Construct a`SELECT`statement suitable for use in a group of`SELECT`statements that will be joined through`UNION`operators in buildUnionQuery. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [buildUnionSubQuery](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#buildUnionSubQuery(kotlin.String,%20kotlin.Array,%20kotlin.collections.MutableSet,%20kotlin.Int,%20kotlin.String,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.String))`(`typeDiscriminatorColumn:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `unionColumns:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `columnsPresentInTable:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `computedColumnsOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `typeDiscriminatorValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `groupBy:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `having:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [delete](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#delete(android.database.sqlite.SQLiteDatabase,%20kotlin.String,%20kotlin.Array))`(`db:` ` [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase)`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Perform a delete by combining all current settings and the information passed into this method. |
| open [SQLiteDatabase.CursorFactory](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory)? | [getCursorFactory](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#getCursorFactory())`()` Gets the cursor factory to be used for the query, as last configured by [setCursorFactory(android.database.sqlite.SQLiteDatabase.CursorFactory)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setCursorFactory(android.database.sqlite.SQLiteDatabase.CursorFactory)). |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#)!\>? | [getProjectionGreylist](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#getProjectionGreylist())`()` Gets the projection greylist for the query, as last configured by [setProjectionGreylist](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setProjectionGreylist(kotlin.collections.MutableCollection)). |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [getProjectionMap](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#getProjectionMap())`()` Gets the projection map for the query, as last configured by [setProjectionMap(java.util.Map)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setProjectionMap(kotlin.collections.MutableMap)). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getTables](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#getTables())`()` Returns the list of tables being queried |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [insert](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#insert(android.database.sqlite.SQLiteDatabase,%20android.content.ContentValues))`(`db:` ` [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase)`, `values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)`)` Perform an insert by combining all current settings and the information passed into this method. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDistinct](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#isDistinct())`()` Get if the query is marked as`DISTINCT`, as last configured by [setDistinct(boolean)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setDistinct(kotlin.Boolean)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStrict](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#isStrict())`()` Get if the query is marked as strict, as last configured by [setStrict(boolean)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setStrict(kotlin.Boolean)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStrictColumns](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#isStrictColumns())`()` Get if the query is marked as strict, as last configured by [setStrictColumns(boolean)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setStrictColumns(kotlin.Boolean)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStrictGrammar](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#isStrictGrammar())`()` Get if the query is marked as strict, as last configured by [setStrictGrammar(boolean)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setStrictGrammar(kotlin.Boolean)). |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [query](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#query(android.database.sqlite.SQLiteDatabase,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`db:` ` [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase)!`, `projectionIn:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `groupBy:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `having:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Perform a query by combining all current settings and the information passed into this method. |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [query](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#query(android.database.sqlite.SQLiteDatabase,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`db:` ` [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase)!`, `projectionIn:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `groupBy:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `having:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `limit:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Perform a query by combining all current settings and the information passed into this method. |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [query](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#query(android.database.sqlite.SQLiteDatabase,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20android.os.CancellationSignal))`(`db:` ` [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase)!`, `projectionIn:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `groupBy:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `having:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `limit:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)!`)` Perform a query by combining all current settings and the information passed into this method. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCursorFactory](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setCursorFactory(android.database.sqlite.SQLiteDatabase.CursorFactory))`(`factory:` ` [SQLiteDatabase.CursorFactory](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory)?`)` Sets the cursor factory to be used for the query. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDistinct](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setDistinct(kotlin.Boolean))`(`distinct:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Mark the query as`DISTINCT`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProjectionGreylist](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setProjectionGreylist(kotlin.collections.MutableCollection))`(`projectionGreylist:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#)!>?`)` Sets a projection greylist of columns that will be allowed through, even when [setStrict(boolean)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setStrict(kotlin.Boolean))is enabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProjectionMap](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setProjectionMap(kotlin.collections.MutableMap))`(`columnMap:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Sets the projection map for the query. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStrict](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setStrict(kotlin.Boolean))`(`strict:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` When set, the selection is verified against malicious arguments. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStrictColumns](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setStrictColumns(kotlin.Boolean))`(`strictColumns:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` When enabled, verify that all projections and [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#) only contain valid columns as defined by [setProjectionMap(java.util.Map)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setProjectionMap(kotlin.collections.MutableMap)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStrictGrammar](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setStrictGrammar(kotlin.Boolean))`(`strictGrammar:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` When enabled, verify that all untrusted SQL conforms to a restricted SQL grammar. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTables](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setTables(kotlin.String))`(`inTables:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the list of tables to query. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [update](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#update(android.database.sqlite.SQLiteDatabase,%20android.content.ContentValues,%20kotlin.String,%20kotlin.Array))`(`db:` ` [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase)`, `values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Perform an update by combining all current settings and the information passed into this method. |

## Public constructors

### SQLiteQueryBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLiteQueryBuilder()
```

## Public methods

### appendColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun appendColumns(
    s: StringBuilder!, 
    columns: Array<String!>!
): Unit
```

Add the names that are non-null in columns to s, separating them with commas. 

### appendWhere

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun appendWhere(inWhere: CharSequence): Unit
```

Append a chunk to the`WHERE`clause of the query. All chunks appended are surrounded by parenthesis and`AND`ed with the selection passed to #query. The final`WHERE`clause looks like:

WHERE (\<append chunk 1\>\<append chunk2\>) AND (\<query() selection parameter\>)

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inWhere` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):the chunk of text to append to the`WHERE`clause. This value cannot be`null`. |

### appendWhereEscapeString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun appendWhereEscapeString(inWhere: String): Unit
```

Append a chunk to the`WHERE`clause of the query. All chunks appended are surrounded by parenthesis and ANDed with the selection passed to #query. The final`WHERE`clause looks like:

WHERE (\<append chunk 1\>\<append chunk2\>) AND (\<query() selection parameter\>)

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inWhere` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the chunk of text to append to the`WHERE`clause. it will be escaped to avoid SQL injection attacks This value cannot be`null`. |

### appendWhereStandalone

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun appendWhereStandalone(inWhere: CharSequence): Unit
```

Add a standalone chunk to the`WHERE`clause of this query.

This method differs from [appendWhere(java.lang.CharSequence)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#appendWhere(kotlin.CharSequence))in that it automatically appends`AND`to any existing`WHERE`clause already under construction before appending the given standalone expression wrapped in parentheses.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inWhere` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):the standalone expression to append to the`WHERE`clause. It will be wrapped in parentheses when it's appended. This value cannot be`null`. |

### buildQuery

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun buildQuery(
    projectionIn: Array<String!>!, 
    selection: String!, 
    groupBy: String!, 
    having: String!, 
    sortOrder: String!, 
    limit: String!
): String!
```

Construct a`SELECT`statement suitable for use in a group of`SELECT`statements that will be joined through`UNION`operators in buildUnionQuery.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `projectionIn` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of which columns to return. Passing null will return all columns, which is discouraged to prevent reading data from storage that isn't going to be used. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declaring which rows to return, formatted as an SQL`WHERE`clause (excluding the`WHERE`itself). Passing null will return all rows for the given URL. |
| `groupBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declaring how to group rows, formatted as an SQL`GROUP BY`clause (excluding the`GROUP BY`itself). Passing null will cause the rows to not be grouped. |
| `having` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declare which row groups to include in the cursor, if row grouping is being used, formatted as an SQL`HAVING`clause (excluding the`HAVING`itself). Passing null will cause all row groups to be included, and is required when row grouping is not being used. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:How to order the rows, formatted as an SQL`ORDER BY`clause (excluding the`ORDER BY`itself). Passing null will use the default sort order, which may be unordered. |
| `limit` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Limits the number of rows returned by the query, formatted as`LIMIT`clause. Passing null denotes no`LIMIT`clause. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the resulting SQL`SELECT`statement |

### buildQuery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun buildQuery(
    projectionIn: Array<String!>!, 
    selection: String!, 
    selectionArgs: Array<String!>!, 
    groupBy: String!, 
    having: String!, 
    sortOrder: String!, 
    limit: String!
): String!
```

**Deprecated:** *This method's signature is misleading since no SQL parameter substitution is carried out. The selection arguments parameter does not get used at all. To avoid confusion, call[buildQuery(java.lang.String[],java.lang.String,java.lang.String,java.lang.String,java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#buildQuery(kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))instead.* 

### buildQueryString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun buildQueryString(
    distinct: Boolean, 
    tables: String!, 
    columns: Array<String!>!, 
    where: String!, 
    groupBy: String!, 
    having: String!, 
    orderBy: String!, 
    limit: String!
): String!
```

Build an SQL query string from the given clauses.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `distinct` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if you want each row to be unique, false otherwise. |
| `tables` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The table names to compile the query against. |
| `columns` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of which columns to return. Passing null will return all columns, which is discouraged to prevent reading data from storage that isn't going to be used. |
| `where` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declaring which rows to return, formatted as an SQL`WHERE`clause (excluding the`WHERE`itself). Passing`null`will return all rows for the given URL. |
| `groupBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declaring how to group rows, formatted as an SQL`GROUP BY`clause (excluding the`GROUP BY`itself). Passing`null`will cause the rows to not be grouped. |
| `having` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declare which row groups to include in the cursor, if row grouping is being used, formatted as an SQL`HAVING`clause (excluding the`HAVING`itself). Passing null will cause all row groups to be included, and is required when row grouping is not being used. |
| `orderBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:How to order the rows, formatted as an SQL`ORDER BY`clause (excluding the`ORDER BY`itself). Passing null will use the default sort order, which may be unordered. |
| `limit` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Limits the number of rows returned by the query, formatted as`LIMIT`clause. Passing null denotes no`LIMIT`clause. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the SQL query string |

### buildUnionQuery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun buildUnionQuery(
    subQueries: Array<String!>!, 
    sortOrder: String!, 
    limit: String!
): String!
```

Given a set of subqueries, all of which are`SELECT`statements, construct a query that returns the union of what those subqueries return.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `subQueries` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:an array of SQL`SELECT`statements, all of which must have the same columns as the same positions in their results |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:How to order the rows, formatted as an SQL`ORDER BY`clause (excluding the`ORDER BY`itself). Passing null will use the default sort order, which may be unordered. |
| `limit` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The limit clause, which applies to the entire union result set |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the resulting SQL`SELECT`statement |

### buildUnionSubQuery

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun buildUnionSubQuery(
    typeDiscriminatorColumn: String!, 
    unionColumns: Array<String!>!, 
    columnsPresentInTable: MutableSet<String!>!, 
    computedColumnsOffset: Int, 
    typeDiscriminatorValue: String!, 
    selection: String!, 
    groupBy: String!, 
    having: String!
): String!
```

Construct a`SELECT`statement suitable for use in a group of`SELECT`statements that will be joined through`UNION`operators in buildUnionQuery.

| Parameters ||
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `typeDiscriminatorColumn` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the result column whose cells will contain the name of the table from which each row was drawn. |
| `unionColumns` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the names of the columns to appear in the result. This may include columns that do not appear in the table this`SELECT`is querying (i.e. mTables), but that do appear in one of the other tables in the`UNION`query that we are constructing. |
| `columnsPresentInTable` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:a Set of the names of the columns that appear in this table (i.e. in the table whose name is mTables). Since columns in unionColumns include columns that appear only in other tables, we use this array to distinguish which ones actually are present. Other columns will have NULL values for results from this subquery. |
| `computedColumnsOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):all columns in unionColumns before this index are included under the assumption that they're computed and therefore won't appear in columnsPresentInTable, e.g. "date \* 1000 as normalized_date" |
| `typeDiscriminatorValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the value used for the type-discriminator column in this subquery |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declaring which rows to return, formatted as an SQL`WHERE`clause (excluding the`WHERE`itself). Passing null will return all rows for the given URL. |
| `groupBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declaring how to group rows, formatted as an SQL`GROUP BY`clause (excluding the`GROUP BY`itself). Passing null will cause the rows to not be grouped. |
| `having` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declare which row groups to include in the cursor, if row grouping is being used, formatted as an SQL`HAVING`clause (excluding the`HAVING`itself). Passing null will cause all row groups to be included, and is required when row grouping is not being used. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the resulting SQL`SELECT`statement |

### buildUnionSubQuery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun buildUnionSubQuery(
    typeDiscriminatorColumn: String!, 
    unionColumns: Array<String!>!, 
    columnsPresentInTable: MutableSet<String!>!, 
    computedColumnsOffset: Int, 
    typeDiscriminatorValue: String!, 
    selection: String!, 
    selectionArgs: Array<String!>!, 
    groupBy: String!, 
    having: String!
): String!
```

**Deprecated:** *This method's signature is misleading since no SQL parameter substitution is carried out. The selection arguments parameter does not get used at all. To avoid confusion, call #buildUnionSubQuery instead.* 

### delete

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun delete(
    db: SQLiteDatabase, 
    selection: String?, 
    selectionArgs: Array<String!>?
): Int
```

Perform a delete by combining all current settings and the information passed into this method.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `db` | [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase):the database to delete on This value cannot be`null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:A filter declaring which rows to return, formatted as an SQL`WHERE`clause (excluding the`WHERE`itself). Passing null will return all rows for the given URL. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:You may include ?s in selection, which will be replaced by the values from selectionArgs, in order that they appear in the selection. The values will be bound as Strings. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of rows deleted |

### getCursorFactory

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCursorFactory(): SQLiteDatabase.CursorFactory?
```

Gets the cursor factory to be used for the query, as last configured by [setCursorFactory(android.database.sqlite.SQLiteDatabase.CursorFactory)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setCursorFactory(android.database.sqlite.SQLiteDatabase.CursorFactory)).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [SQLiteDatabase.CursorFactory](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory)? | This value may be`null`. |

### getProjectionGreylist

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProjectionGreylist(): MutableCollection<Pattern!>?
```

Gets the projection greylist for the query, as last configured by [setProjectionGreylist](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setProjectionGreylist(kotlin.collections.MutableCollection)).

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#)!>? | This value may be`null`. |

### getProjectionMap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProjectionMap(): MutableMap<String!, String!>?
```

Gets the projection map for the query, as last configured by [setProjectionMap(java.util.Map)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setProjectionMap(kotlin.collections.MutableMap)).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>? | This value may be`null`. |

### getTables

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTables(): String?
```

Returns the list of tables being queried

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the list of tables being queried This value may be`null`. |

### insert

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun insert(
    db: SQLiteDatabase, 
    values: ContentValues
): Long
```

Perform an insert by combining all current settings and the information passed into this method.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `db` | [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase):the database to insert on This value cannot be`null`. |
| `values` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the row ID of the newly inserted row, or -1 if an error occurred |

### isDistinct

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isDistinct(): Boolean
```

Get if the query is marked as`DISTINCT`, as last configured by [setDistinct(boolean)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setDistinct(kotlin.Boolean)). 

### isStrict

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isStrict(): Boolean
```

Get if the query is marked as strict, as last configured by [setStrict(boolean)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setStrict(kotlin.Boolean)). 

### isStrictColumns

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isStrictColumns(): Boolean
```

Get if the query is marked as strict, as last configured by [setStrictColumns(boolean)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setStrictColumns(kotlin.Boolean)). 

### isStrictGrammar

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isStrictGrammar(): Boolean
```

Get if the query is marked as strict, as last configured by [setStrictGrammar(boolean)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setStrictGrammar(kotlin.Boolean)). 

### query

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun query(
    db: SQLiteDatabase!, 
    projectionIn: Array<String!>!, 
    selection: String!, 
    selectionArgs: Array<String!>!, 
    groupBy: String!, 
    having: String!, 
    sortOrder: String!
): Cursor!
```

Perform a query by combining all current settings and the information passed into this method.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `db` | [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase)!:the database to query on |
| `projectionIn` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of which columns to return. Passing null will return all columns, which is discouraged to prevent reading data from storage that isn't going to be used. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declaring which rows to return, formatted as an SQL`WHERE`clause (excluding the`WHERE`itself). Passing null will return all rows for the given URL. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:You may include ?s in selection, which will be replaced by the values from selectionArgs, in order that they appear in the selection. The values will be bound as Strings. |
| `groupBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declaring how to group rows, formatted as an SQL`GROUP BY`clause (excluding the`GROUP BY`itself). Passing null will cause the rows to not be grouped. |
| `having` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declare which row groups to include in the cursor, if row grouping is being used, formatted as an SQL`HAVING`clause (excluding the`HAVING`itself). Passing null will cause all row groups to be included, and is required when row grouping is not being used. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:How to order the rows, formatted as an SQL`ORDER BY`clause (excluding the`ORDER BY`itself). Passing null will use the default sort order, which may be unordered. |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | a cursor over the result set |

**See Also**

- [android.content.ContentResolver#query(android.net.Uri, String[],
* String, String[], String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String)) 

### query

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun query(
    db: SQLiteDatabase!, 
    projectionIn: Array<String!>!, 
    selection: String!, 
    selectionArgs: Array<String!>!, 
    groupBy: String!, 
    having: String!, 
    sortOrder: String!, 
    limit: String!
): Cursor!
```

Perform a query by combining all current settings and the information passed into this method.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `db` | [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase)!:the database to query on |
| `projectionIn` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of which columns to return. Passing null will return all columns, which is discouraged to prevent reading data from storage that isn't going to be used. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declaring which rows to return, formatted as an SQL`WHERE`clause (excluding the`WHERE`itself). Passing null will return all rows for the given URL. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:You may include ?s in selection, which will be replaced by the values from selectionArgs, in order that they appear in the selection. The values will be bound as Strings. |
| `groupBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declaring how to group rows, formatted as an SQL`GROUP BY`clause (excluding the`GROUP BY`itself). Passing null will cause the rows to not be grouped. |
| `having` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declare which row groups to include in the cursor, if row grouping is being used, formatted as an SQL`HAVING`clause (excluding the`HAVING`itself). Passing null will cause all row groups to be included, and is required when row grouping is not being used. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:How to order the rows, formatted as an SQL`ORDER BY`clause (excluding the`ORDER BY`itself). Passing null will use the default sort order, which may be unordered. |
| `limit` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Limits the number of rows returned by the query, formatted as`LIMIT`clause. Passing null denotes no`LIMIT`clause. |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | a cursor over the result set |

**See Also**

- [android.content.ContentResolver#query(android.net.Uri, String[],
* String, String[], String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String)) 

### query

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun query(
    db: SQLiteDatabase!, 
    projectionIn: Array<String!>!, 
    selection: String!, 
    selectionArgs: Array<String!>!, 
    groupBy: String!, 
    having: String!, 
    sortOrder: String!, 
    limit: String!, 
    cancellationSignal: CancellationSignal!
): Cursor!
```

Perform a query by combining all current settings and the information passed into this method.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `db` | [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase)!:the database to query on |
| `projectionIn` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of which columns to return. Passing null will return all columns, which is discouraged to prevent reading data from storage that isn't going to be used. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declaring which rows to return, formatted as an SQL`WHERE`clause (excluding the`WHERE`itself). Passing null will return all rows for the given URL. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:You may include ?s in selection, which will be replaced by the values from selectionArgs, in order that they appear in the selection. The values will be bound as Strings. |
| `groupBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declaring how to group rows, formatted as an SQL`GROUP BY`clause (excluding the`GROUP BY`itself). Passing null will cause the rows to not be grouped. |
| `having` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A filter declare which row groups to include in the cursor, if row grouping is being used, formatted as an SQL`HAVING`clause (excluding the`HAVING`itself). Passing null will cause all row groups to be included, and is required when row grouping is not being used. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:How to order the rows, formatted as an SQL`ORDER BY`clause (excluding the`ORDER BY`itself). Passing null will use the default sort order, which may be unordered. |
| `limit` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Limits the number of rows returned by the query, formatted as`LIMIT`clause. Passing null denotes no`LIMIT`clause. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)!:A signal to cancel the operation in progress, or null if none. If the operation is canceled, then [OperationCanceledException](https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#) will be thrown when the query is executed. |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | a cursor over the result set |

**See Also**

- [android.content.ContentResolver#query(android.net.Uri, String[],
* String, String[], String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String)) 

### setCursorFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCursorFactory(factory: SQLiteDatabase.CursorFactory?): Unit
```

Sets the cursor factory to be used for the query. You can use one factory for all queries on a database but it is normally easier to specify the factory when doing this query.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `factory` | [SQLiteDatabase.CursorFactory](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory)?:the factory to use. This value may be`null`. |

### setDistinct

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDistinct(distinct: Boolean): Unit
```

Mark the query as`DISTINCT`.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `distinct` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true the query is`DISTINCT`, otherwise it isn't |

### setProjectionGreylist

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProjectionGreylist(projectionGreylist: MutableCollection<Pattern!>?): Unit
```

Sets a projection greylist of columns that will be allowed through, even when [setStrict(boolean)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setStrict(kotlin.Boolean))is enabled. This provides a way for abusive custom columns like`COUNT(*)`to continue working.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `projectionGreylist` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#)!\>?:This value may be`null`. |

### setProjectionMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProjectionMap(columnMap: MutableMap<String!, String!>?): Unit
```

Sets the projection map for the query. The projection map maps from column names that the caller passes into query to database column names. This is useful for renaming columns as well as disambiguating column names when doing joins. For example you could map "name" to "people.name". If a projection map is set it must contain all column names the user may request, even if the key and value are the same.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `columnMap` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:maps from the user column names to the database column names This value may be`null`. |

### setStrict

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStrict(strict: Boolean): Unit
```

When set, the selection is verified against malicious arguments. When using this class to create a statement using[buildQueryString(boolean,java.lang.String,java.lang.String[],java.lang.String,java.lang.String,java.lang.String,java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#buildQueryString(kotlin.Boolean,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String)), non-numeric limits will raise an exception. If a projection map is specified, fields not in that map will be ignored. If this class is used to execute the statement directly using[query(android.database.sqlite.SQLiteDatabase,java.lang.String[],java.lang.String,java.lang.String[],java.lang.String,java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#query(android.database.sqlite.SQLiteDatabase,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.String))or[query(android.database.sqlite.SQLiteDatabase,java.lang.String[],java.lang.String,java.lang.String[],java.lang.String,java.lang.String,java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#query(android.database.sqlite.SQLiteDatabase,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String)), additionally also parenthesis escaping selection are caught. To summarize: To get maximum protection against malicious third party apps (for example content provider consumers), make sure to do the following:

- Set this value to true
- Use a projection map
- Use one of the query overloads instead of getting the statement as a sql string

<br />

This feature is disabled by default on each newly constructed [SQLiteQueryBuilder](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#) and needs to be manually enabled. 

### setStrictColumns

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStrictColumns(strictColumns: Boolean): Unit
```

When enabled, verify that all projections and [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#) only contain valid columns as defined by [setProjectionMap(java.util.Map)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setProjectionMap(kotlin.collections.MutableMap)).

This enforcement applies to [insert](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#insert(android.database.sqlite.SQLiteDatabase,%20android.content.ContentValues)), #query, and [update](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#update(android.database.sqlite.SQLiteDatabase,%20android.content.ContentValues,%20kotlin.String,%20kotlin.Array))operations. Any enforcement failures will throw an [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#).

This feature is disabled by default on each newly constructed [SQLiteQueryBuilder](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#) and needs to be manually enabled. 

### setStrictGrammar

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStrictGrammar(strictGrammar: Boolean): Unit
```

When enabled, verify that all untrusted SQL conforms to a restricted SQL grammar. Here are the restrictions applied:

- In`WHERE`and`HAVING`clauses: subqueries, raising, and windowing terms are rejected.
- In`GROUP BY`clauses: only valid columns are allowed.
- In`ORDER BY`clauses: only valid columns, collation, and ordering terms are allowed.
- In`LIMIT`clauses: only numerical values and offset terms are allowed.

All column references must be valid as defined by [setProjectionMap(java.util.Map)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#setProjectionMap(kotlin.collections.MutableMap)).

<br />

This enforcement applies to #query, [update](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#update(android.database.sqlite.SQLiteDatabase,%20android.content.ContentValues,%20kotlin.String,%20kotlin.Array))and [delete](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#delete(android.database.sqlite.SQLiteDatabase,%20kotlin.String,%20kotlin.Array))operations. This enforcement does not apply to trusted inputs, such as those provided by [appendWhere](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#appendWhere(kotlin.CharSequence)). Any enforcement failures will throw an [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#).

This feature is disabled by default on each newly constructed [SQLiteQueryBuilder](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQueryBuilder#) and needs to be manually enabled. 

### setTables

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTables(inTables: String?): Unit
```

Sets the list of tables to query. Multiple tables can be specified to perform a join. For example: setTables("foo, bar") setTables("foo LEFT OUTER JOIN bar ON (foo.id = bar.foo_id)")

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `inTables` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the list of tables to query on This value may be`null`. |

### update

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(
    db: SQLiteDatabase, 
    values: ContentValues, 
    selection: String?, 
    selectionArgs: Array<String!>?
): Int
```

Perform an update by combining all current settings and the information passed into this method.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `db` | [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase):the database to update on This value cannot be`null`. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:A filter declaring which rows to return, formatted as an SQL`WHERE`clause (excluding the`WHERE`itself). Passing null will return all rows for the given URL. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:You may include ?s in selection, which will be replaced by the values from selectionArgs, in order that they appear in the selection. The values will be bound as Strings. This value may be`null`. |
| `values` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#):This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of rows updated |
