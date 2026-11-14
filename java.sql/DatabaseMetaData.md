# DatabaseMetaData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DatabaseMetaData

```
interface DatabaseMetaData : Wrapper
```

| [java.sql.DatabaseMetaData](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#) |

Comprehensive information about the database as a whole.

This interface is implemented by driver vendors to let users know the capabilities of a Database Management System (DBMS) in combination with the driver based on JDBCTM technology ("JDBC driver") that is used with it. Different relational DBMSs often support different features, implement features in different ways, and use different data types. In addition, a driver may implement a feature on top of what the DBMS offers. Information returned by methods in this interface applies to the capabilities of a particular driver and a particular DBMS working together. Note that as used in this documentation, the term "database" is used generically to refer to both the driver and DBMS.

A user for this interface is commonly a tool that needs to discover how to deal with the underlying DBMS. This is especially true for applications that are intended to be used with more than one DBMS. For example, a tool might use the method`getTypeInfo`to find out what data types can be used in a`CREATE TABLE`statement. Or a user might call the method`supportsCorrelatedSubqueries`to see if it is possible to use a correlated subquery or`supportsBatchUpdates`to see if it is possible to use batch updates.

Some`DatabaseMetaData`methods return lists of information in the form of`ResultSet`objects. Regular`ResultSet`methods, such as`getString`and`getInt`, can be used to retrieve the data from these`ResultSet`objects. If a given form of metadata is not available, an empty`ResultSet`will be returned. Additional columns beyond the columns defined to be returned by the`ResultSet`object for a given method can be defined by the JDBC driver vendor and must be accessed by their**column label**.

Some`DatabaseMetaData`methods take arguments that are String patterns. These arguments all have names such as fooPattern. Within a pattern String, "%" means match any substring of 0 or more characters, and "_" means match any one character. Only metadata entries matching the search pattern are returned. If a search pattern argument is set to`null`, that argument's criterion will be dropped from the search.

<br />

## Summary

| Constants ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [attributeNoNulls](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#attributeNoNulls:kotlin.Short) Indicates that`NULL`values might not be allowed. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [attributeNullable](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#attributeNullable:kotlin.Short) Indicates that`NULL`values are definitely allowed. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [attributeNullableUnknown](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#attributeNullableUnknown:kotlin.Short) Indicates that whether`NULL`values are allowed is not known. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bestRowNotPseudo](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#bestRowNotPseudo:kotlin.Int) Indicates that the best row identifier is NOT a pseudo column. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bestRowPseudo](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#bestRowPseudo:kotlin.Int) Indicates that the best row identifier is a pseudo column. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bestRowSession](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#bestRowSession:kotlin.Int) Indicates that the scope of the best row identifier is the remainder of the current session. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bestRowTemporary](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#bestRowTemporary:kotlin.Int) Indicates that the scope of the best row identifier is very temporary, lasting only while the row is being used. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bestRowTransaction](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#bestRowTransaction:kotlin.Int) Indicates that the scope of the best row identifier is the remainder of the current transaction. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bestRowUnknown](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#bestRowUnknown:kotlin.Int) Indicates that the best row identifier may or may not be a pseudo column. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [columnNoNulls](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#columnNoNulls:kotlin.Int) Indicates that the column might not allow`NULL`values. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [columnNullable](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#columnNullable:kotlin.Int) Indicates that the column definitely allows`NULL`values. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [columnNullableUnknown](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#columnNullableUnknown:kotlin.Int) Indicates that the nullability of columns is unknown. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [functionColumnIn](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#functionColumnIn:kotlin.Int) Indicates that the parameter or column is an IN parameter. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [functionColumnInOut](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#functionColumnInOut:kotlin.Int) Indicates that the parameter or column is an INOUT parameter. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [functionColumnOut](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#functionColumnOut:kotlin.Int) Indicates that the parameter or column is an OUT parameter. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [functionColumnResult](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#functionColumnResult:kotlin.Int) Indicates that the parameter or column is a column in a result set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [functionColumnUnknown](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#functionColumnUnknown:kotlin.Int) Indicates that type of the parameter or column is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [functionNoNulls](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#functionNoNulls:kotlin.Int) Indicates that`NULL`values are not allowed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [functionNoTable](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#functionNoTable:kotlin.Int) Indicates that the function does not return a table. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [functionNullable](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#functionNullable:kotlin.Int) Indicates that`NULL`values are allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [functionNullableUnknown](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#functionNullableUnknown:kotlin.Int) Indicates that whether`NULL`values are allowed is unknown. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [functionResultUnknown](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#functionResultUnknown:kotlin.Int) Indicates that it is not known whether the function returns a result or a table. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [functionReturn](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#functionReturn:kotlin.Int) Indicates that the parameter or column is a return value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [functionReturnsTable](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#functionReturnsTable:kotlin.Int) Indicates that the function returns a table. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [importedKeyCascade](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#importedKeyCascade:kotlin.Int) For the column`UPDATE_RULE`, indicates that when the primary key is updated, the foreign key (imported key) is changed to agree with it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [importedKeyInitiallyDeferred](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#importedKeyInitiallyDeferred:kotlin.Int) Indicates deferrability. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [importedKeyInitiallyImmediate](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#importedKeyInitiallyImmediate:kotlin.Int) Indicates deferrability. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [importedKeyNoAction](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#importedKeyNoAction:kotlin.Int) For the columns`UPDATE_RULE`and`DELETE_RULE`, indicates that if the primary key has been imported, it cannot be updated or deleted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [importedKeyNotDeferrable](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#importedKeyNotDeferrable:kotlin.Int) Indicates deferrability. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [importedKeyRestrict](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#importedKeyRestrict:kotlin.Int) For the column`UPDATE_RULE`, indicates that a primary key may not be updated if it has been imported by another table as a foreign key. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [importedKeySetDefault](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#importedKeySetDefault:kotlin.Int) For the columns`UPDATE_RULE`and`DELETE_RULE`, indicates that if the primary key is updated or deleted, the foreign key (imported key) is set to the default value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [importedKeySetNull](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#importedKeySetNull:kotlin.Int) For the columns`UPDATE_RULE`and`DELETE_RULE`, indicates that when the primary key is updated or deleted, the foreign key (imported key) is changed to`NULL`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [procedureColumnIn](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#procedureColumnIn:kotlin.Int) Indicates that the column stores IN parameters. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [procedureColumnInOut](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#procedureColumnInOut:kotlin.Int) Indicates that the column stores INOUT parameters. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [procedureColumnOut](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#procedureColumnOut:kotlin.Int) Indicates that the column stores OUT parameters. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [procedureColumnResult](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#procedureColumnResult:kotlin.Int) Indicates that the column stores results. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [procedureColumnReturn](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#procedureColumnReturn:kotlin.Int) Indicates that the column stores return values. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [procedureColumnUnknown](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#procedureColumnUnknown:kotlin.Int) Indicates that type of the column is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [procedureNoNulls](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#procedureNoNulls:kotlin.Int) Indicates that`NULL`values are not allowed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [procedureNoResult](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#procedureNoResult:kotlin.Int) Indicates that the procedure does not return a result. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [procedureNullable](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#procedureNullable:kotlin.Int) Indicates that`NULL`values are allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [procedureNullableUnknown](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#procedureNullableUnknown:kotlin.Int) Indicates that whether`NULL`values are allowed is unknown. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [procedureResultUnknown](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#procedureResultUnknown:kotlin.Int) Indicates that it is not known whether the procedure returns a result. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [procedureReturnsResult](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#procedureReturnsResult:kotlin.Int) Indicates that the procedure returns a result. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [sqlStateSQL](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#sqlStateSQL:kotlin.Int) A possible return value for the method`DatabaseMetaData.getSQLStateType`which is used to indicate whether the value returned by the method`SQLException.getSQLState`is an SQLSTATE value. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [sqlStateSQL99](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#sqlStateSQL99:kotlin.Int) A possible return value for the method`DatabaseMetaData.getSQLStateType`which is used to indicate whether the value returned by the method`SQLException.getSQLState`is an SQL99 SQLSTATE value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [sqlStateXOpen](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#sqlStateXOpen:kotlin.Int) A possible return value for the method`DatabaseMetaData.getSQLStateType`which is used to indicate whether the value returned by the method`SQLException.getSQLState`is an X/Open (now know as Open Group) SQL CLI SQLSTATE value. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [tableIndexClustered](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#tableIndexClustered:kotlin.Short) Indicates that this table index is a clustered index. |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [tableIndexHashed](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#tableIndexHashed:kotlin.Short) Indicates that this table index is a hashed index. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [tableIndexOther](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#tableIndexOther:kotlin.Short) Indicates that this table index is not a clustered index, a hashed index, or table statistics; it is something other than these. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [tableIndexStatistic](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#tableIndexStatistic:kotlin.Short) Indicates that this column contains table statistics that are returned in conjunction with a table's index descriptions. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [typeNoNulls](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#typeNoNulls:kotlin.Int) Indicates that a`NULL`value is NOT allowed for this data type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [typeNullable](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#typeNullable:kotlin.Int) Indicates that a`NULL`value is allowed for this data type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [typeNullableUnknown](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#typeNullableUnknown:kotlin.Int) Indicates that it is not known whether a`NULL`value is allowed for this data type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [typePredBasic](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#typePredBasic:kotlin.Int) Indicates that the data type can be only be used in`WHERE`search clauses that do not use`LIKE`predicates. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [typePredChar](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#typePredChar:kotlin.Int) Indicates that the data type can be only be used in`WHERE`search clauses that use`LIKE`predicates. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [typePredNone](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#typePredNone:kotlin.Int) Indicates that`WHERE`search clauses are not supported for this type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [typeSearchable](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#typeSearchable:kotlin.Int) Indicates that all`WHERE`search clauses can be based on this type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [versionColumnNotPseudo](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#versionColumnNotPseudo:kotlin.Int) Indicates that this version column is NOT a pseudo column. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [versionColumnPseudo](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#versionColumnPseudo:kotlin.Int) Indicates that this version column is a pseudo column. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [versionColumnUnknown](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#versionColumnUnknown:kotlin.Int) Indicates that this version column may or may not be a pseudo column. |

| Public methods ||
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [allProceduresAreCallable](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#allProceduresAreCallable())`()` Retrieves whether the current user can call all the procedures returned by the method`getProcedures`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [allTablesAreSelectable](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#allTablesAreSelectable())`()` Retrieves whether the current user can use all the tables returned by the method`getTables`in a`SELECT`statement. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [autoCommitFailureClosesAllResultSets](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#autoCommitFailureClosesAllResultSets())`()` Retrieves whether a`SQLException`while autoCommit is`true`inidcates that all open ResultSets are closed, even ones that are holdable. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dataDefinitionCausesTransactionCommit](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#dataDefinitionCausesTransactionCommit())`()` Retrieves whether a data definition statement within a transaction forces the transaction to commit. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dataDefinitionIgnoredInTransactions](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#dataDefinitionIgnoredInTransactions())`()` Retrieves whether this database ignores a data definition statement within a transaction. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [deletesAreDetected](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#deletesAreDetected(kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves whether or not a visible row delete can be detected by calling the method`ResultSet.rowDeleted`. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [doesMaxRowSizeIncludeBlobs](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#doesMaxRowSizeIncludeBlobs())`()` Retrieves whether the return value for the method`getMaxRowSize`includes the SQL data types`LONGVARCHAR`and`LONGVARBINARY`. |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getAttributes](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getAttributes(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schemaPattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `typeNamePattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attributeNamePattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves a description of the given attribute of the given type for a user-defined type (UDT) that is available in the given schema and catalog. |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getBestRowIdentifier](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getBestRowIdentifier(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Boolean))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schema:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `table:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `scope:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `nullable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Retrieves a description of a table's optimal set of columns that uniquely identifies a row. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCatalogSeparator](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getCatalogSeparator())`()` Retrieves the`String`that this database uses as the separator between a catalog and table name. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCatalogTerm](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getCatalogTerm())`()` Retrieves the database vendor's preferred term for "catalog". |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getCatalogs](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getCatalogs())`()` Retrieves the catalog names available in this database. |
| --- | --- |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getClientInfoProperties](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getClientInfoProperties())`()` Retrieves a list of the client info properties that the driver supports. |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getColumnPrivileges](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getColumnPrivileges(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schema:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `table:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `columnNamePattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves a description of the access rights for a table's columns. |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getColumns](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getColumns(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schemaPattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `tableNamePattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `columnNamePattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves a description of table columns available in the specified catalog. |
| --- | --- |
| abstract [Connection](https://developer.android.com/reference/kotlin/java/sql/Connection)! | [getConnection](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getConnection())`()` Retrieves the connection that produced this metadata object. |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getCrossReference](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getCrossReference(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`parentCatalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `parentSchema:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `parentTable:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `foreignCatalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `foreignSchema:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `foreignTable:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves a description of the foreign key columns in the given foreign key table that reference the primary key or the columns representing a unique constraint of the parent table (could be the same or a different table). |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDatabaseMajorVersion](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getDatabaseMajorVersion())`()` Retrieves the major version number of the underlying database. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDatabaseMinorVersion](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getDatabaseMinorVersion())`()` Retrieves the minor version number of the underlying database. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDatabaseProductName](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getDatabaseProductName())`()` Retrieves the name of this database product. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDatabaseProductVersion](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getDatabaseProductVersion())`()` Retrieves the version number of this database product. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDefaultTransactionIsolation](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getDefaultTransactionIsolation())`()` Retrieves this database's default transaction isolation level. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDriverMajorVersion](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getDriverMajorVersion())`()` Retrieves this JDBC driver's major version number. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDriverMinorVersion](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getDriverMinorVersion())`()` Retrieves this JDBC driver's minor version number. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDriverName](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getDriverName())`()` Retrieves the name of this JDBC driver. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDriverVersion](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getDriverVersion())`()` Retrieves the version number of this JDBC driver as a`String`. |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getExportedKeys](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getExportedKeys(kotlin.String,%20kotlin.String,%20kotlin.String))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schema:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `table:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves a description of the foreign key columns that reference the given table's primary key columns (the foreign keys exported by a table). |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getExtraNameCharacters](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getExtraNameCharacters())`()` Retrieves all the "extra" characters that can be used in unquoted identifier names (those beyond a-z, A-Z, 0-9 and _). |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getFunctionColumns](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getFunctionColumns(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schemaPattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `functionNamePattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `columnNamePattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves a description of the given catalog's system or user function parameters and return type. |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getFunctions](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getFunctions(kotlin.String,%20kotlin.String,%20kotlin.String))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schemaPattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `functionNamePattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves a description of the system and user functions available in the given catalog. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getIdentifierQuoteString](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getIdentifierQuoteString())`()` Retrieves the string used to quote SQL identifiers. |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getImportedKeys](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getImportedKeys(kotlin.String,%20kotlin.String,%20kotlin.String))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schema:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `table:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves a description of the primary key columns that are referenced by the given table's foreign key columns (the primary keys imported by a table). |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getIndexInfo](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getIndexInfo(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.Boolean,%20kotlin.Boolean))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schema:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `table:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `unique:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `approximate:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Retrieves a description of the given table's indices and statistics. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getJDBCMajorVersion](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getJDBCMajorVersion())`()` Retrieves the major JDBC version number for this driver. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getJDBCMinorVersion](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getJDBCMinorVersion())`()` Retrieves the minor JDBC version number for this driver. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxBinaryLiteralLength](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxBinaryLiteralLength())`()` Retrieves the maximum number of hex characters this database allows in an inline binary literal. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxCatalogNameLength](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxCatalogNameLength())`()` Retrieves the maximum number of characters that this database allows in a catalog name. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxCharLiteralLength](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxCharLiteralLength())`()` Retrieves the maximum number of characters this database allows for a character literal. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxColumnNameLength](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxColumnNameLength())`()` Retrieves the maximum number of characters this database allows for a column name. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxColumnsInGroupBy](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxColumnsInGroupBy())`()` Retrieves the maximum number of columns this database allows in a`GROUP BY`clause. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxColumnsInIndex](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxColumnsInIndex())`()` Retrieves the maximum number of columns this database allows in an index. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxColumnsInOrderBy](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxColumnsInOrderBy())`()` Retrieves the maximum number of columns this database allows in an`ORDER BY`clause. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxColumnsInSelect](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxColumnsInSelect())`()` Retrieves the maximum number of columns this database allows in a`SELECT`list. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxColumnsInTable](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxColumnsInTable())`()` Retrieves the maximum number of columns this database allows in a table. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxConnections](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxConnections())`()` Retrieves the maximum number of concurrent connections to this database that are possible. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxCursorNameLength](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxCursorNameLength())`()` Retrieves the maximum number of characters that this database allows in a cursor name. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxIndexLength](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxIndexLength())`()` Retrieves the maximum number of bytes this database allows for an index, including all of the parts of the index. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxProcedureNameLength](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxProcedureNameLength())`()` Retrieves the maximum number of characters that this database allows in a procedure name. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxRowSize](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxRowSize())`()` Retrieves the maximum number of bytes this database allows in a single row. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxSchemaNameLength](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxSchemaNameLength())`()` Retrieves the maximum number of characters that this database allows in a schema name. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxStatementLength](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxStatementLength())`()` Retrieves the maximum number of characters this database allows in an SQL statement. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxStatements](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxStatements())`()` Retrieves the maximum number of active statements to this database that can be open at the same time. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxTableNameLength](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxTableNameLength())`()` Retrieves the maximum number of characters this database allows in a table name. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxTablesInSelect](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxTablesInSelect())`()` Retrieves the maximum number of tables this database allows in a`SELECT`statement. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxUserNameLength](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getMaxUserNameLength())`()` Retrieves the maximum number of characters this database allows in a user name. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNumericFunctions](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getNumericFunctions())`()` Retrieves a comma-separated list of math functions available with this database. |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getPrimaryKeys](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getPrimaryKeys(kotlin.String,%20kotlin.String,%20kotlin.String))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schema:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `table:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves a description of the given table's primary key columns. |
| --- | --- |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getProcedureColumns](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getProcedureColumns(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schemaPattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `procedureNamePattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `columnNamePattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves a description of the given catalog's stored procedure parameter and result columns. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getProcedureTerm](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getProcedureTerm())`()` Retrieves the database vendor's preferred term for "procedure". |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getProcedures](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getProcedures(kotlin.String,%20kotlin.String,%20kotlin.String))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schemaPattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `procedureNamePattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves a description of the stored procedures available in the given catalog. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultSetHoldability](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getResultSetHoldability())`()` Retrieves this database's default holdability for`ResultSet`objects. |
| abstract [RowIdLifetime](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime)! | [getRowIdLifetime](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getRowIdLifetime())`()` Indicates whether or not this data source supports the SQL`ROWID`type, and if so the lifetime for which a`RowId`object remains valid. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSQLKeywords](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSQLKeywords())`()` Retrieves a comma-separated list of all of this database's SQL keywords that are NOT also SQL:2003 keywords. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSQLStateType](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSQLStateType())`()` Indicates whether the SQLSTATE returned by`SQLException.getSQLState`is X/Open (now known as Open Group) SQL CLI or SQL:2003. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSchemaTerm](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSchemaTerm())`()` Retrieves the database vendor's preferred term for "schema". |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getSchemas](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSchemas())`()` Retrieves the schema names available in this database. |
| --- | --- |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getSchemas](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSchemas(kotlin.String,%20kotlin.String))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schemaPattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the schema names available in this database. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSearchStringEscape](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSearchStringEscape())`()` Retrieves the string that can be used to escape wildcard characters. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getStringFunctions](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getStringFunctions())`()` Retrieves a comma-separated list of string functions available with this database. |
| --- | --- |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getSuperTables](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSuperTables(kotlin.String,%20kotlin.String,%20kotlin.String))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schemaPattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `tableNamePattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves a description of the table hierarchies defined in a particular schema in this database. |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getSuperTypes](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSuperTypes(kotlin.String,%20kotlin.String,%20kotlin.String))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schemaPattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `typeNamePattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves a description of the user-defined type (UDT) hierarchies defined in a particular schema in this database. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemFunctions](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSystemFunctions())`()` Retrieves a comma-separated list of system functions available with this database. |
| --- | --- |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getTablePrivileges](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getTablePrivileges(kotlin.String,%20kotlin.String,%20kotlin.String))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schemaPattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `tableNamePattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves a description of the access rights for each table available in a catalog. |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getTableTypes](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getTableTypes())`()` Retrieves the table types available in this database. |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getTables](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getTables(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.Array))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schemaPattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `tableNamePattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `types:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Retrieves a description of the tables available in the given catalog. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTimeDateFunctions](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getTimeDateFunctions())`()` Retrieves a comma-separated list of the time and date functions available with this database. |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getTypeInfo](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getTypeInfo())`()` Retrieves a description of all the data types supported by this database. |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getUDTs](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getUDTs(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.IntArray))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schemaPattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `typeNamePattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `types:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Retrieves a description of the user-defined types (UDTs) defined in a particular schema. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getURL](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getURL())`()` Retrieves the URL for this DBMS. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getUserName](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getUserName())`()` Retrieves the user name as known to this database. |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getVersionColumns](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getVersionColumns(kotlin.String,%20kotlin.String,%20kotlin.String))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `schema:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `table:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves a description of a table's columns that are automatically updated when any value in a row is updated. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [insertsAreDetected](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#insertsAreDetected(kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves whether or not a visible row insert can be detected by calling the method`ResultSet.rowInserted`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCatalogAtStart](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#isCatalogAtStart())`()` Retrieves whether a catalog appears at the start of a fully qualified table name. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#isReadOnly())`()` Retrieves whether this database is in read-only mode. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [locatorsUpdateCopy](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#locatorsUpdateCopy())`()` Indicates whether updates made to a LOB are made on a copy or directly to the LOB. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nullPlusNonNullIsNull](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#nullPlusNonNullIsNull())`()` Retrieves whether this database supports concatenations between`NULL`and non-`NULL`values being`NULL`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nullsAreSortedAtEnd](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#nullsAreSortedAtEnd())`()` Retrieves whether`NULL`values are sorted at the end regardless of sort order. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nullsAreSortedAtStart](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#nullsAreSortedAtStart())`()` Retrieves whether`NULL`values are sorted at the start regardless of sort order. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nullsAreSortedHigh](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#nullsAreSortedHigh())`()` Retrieves whether`NULL`values are sorted high. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nullsAreSortedLow](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#nullsAreSortedLow())`()` Retrieves whether`NULL`values are sorted low. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [othersDeletesAreVisible](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#othersDeletesAreVisible(kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves whether deletes made by others are visible. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [othersInsertsAreVisible](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#othersInsertsAreVisible(kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves whether inserts made by others are visible. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [othersUpdatesAreVisible](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#othersUpdatesAreVisible(kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves whether updates made by others are visible. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [ownDeletesAreVisible](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#ownDeletesAreVisible(kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves whether a result set's own deletes are visible. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [ownInsertsAreVisible](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#ownInsertsAreVisible(kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves whether a result set's own inserts are visible. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [ownUpdatesAreVisible](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#ownUpdatesAreVisible(kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves whether for the given type of`ResultSet`object, the result set's own updates are visible. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [storesLowerCaseIdentifiers](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#storesLowerCaseIdentifiers())`()` Retrieves whether this database treats mixed case unquoted SQL identifiers as case insensitive and stores them in lower case. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [storesLowerCaseQuotedIdentifiers](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#storesLowerCaseQuotedIdentifiers())`()` Retrieves whether this database treats mixed case quoted SQL identifiers as case insensitive and stores them in lower case. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [storesMixedCaseIdentifiers](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#storesMixedCaseIdentifiers())`()` Retrieves whether this database treats mixed case unquoted SQL identifiers as case insensitive and stores them in mixed case. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [storesMixedCaseQuotedIdentifiers](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#storesMixedCaseQuotedIdentifiers())`()` Retrieves whether this database treats mixed case quoted SQL identifiers as case insensitive and stores them in mixed case. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [storesUpperCaseIdentifiers](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#storesUpperCaseIdentifiers())`()` Retrieves whether this database treats mixed case unquoted SQL identifiers as case insensitive and stores them in upper case. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [storesUpperCaseQuotedIdentifiers](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#storesUpperCaseQuotedIdentifiers())`()` Retrieves whether this database treats mixed case quoted SQL identifiers as case insensitive and stores them in upper case. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsANSI92EntryLevelSQL](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsANSI92EntryLevelSQL())`()` Retrieves whether this database supports the ANSI92 entry level SQL grammar. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsANSI92FullSQL](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsANSI92FullSQL())`()` Retrieves whether this database supports the ANSI92 full SQL grammar supported. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsANSI92IntermediateSQL](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsANSI92IntermediateSQL())`()` Retrieves whether this database supports the ANSI92 intermediate SQL grammar supported. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsAlterTableWithAddColumn](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsAlterTableWithAddColumn())`()` Retrieves whether this database supports`ALTER TABLE`with add column. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsAlterTableWithDropColumn](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsAlterTableWithDropColumn())`()` Retrieves whether this database supports`ALTER TABLE`with drop column. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsBatchUpdates](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsBatchUpdates())`()` Retrieves whether this database supports batch updates. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsCatalogsInDataManipulation](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsCatalogsInDataManipulation())`()` Retrieves whether a catalog name can be used in a data manipulation statement. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsCatalogsInIndexDefinitions](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsCatalogsInIndexDefinitions())`()` Retrieves whether a catalog name can be used in an index definition statement. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsCatalogsInPrivilegeDefinitions](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsCatalogsInPrivilegeDefinitions())`()` Retrieves whether a catalog name can be used in a privilege definition statement. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsCatalogsInProcedureCalls](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsCatalogsInProcedureCalls())`()` Retrieves whether a catalog name can be used in a procedure call statement. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsCatalogsInTableDefinitions](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsCatalogsInTableDefinitions())`()` Retrieves whether a catalog name can be used in a table definition statement. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsColumnAliasing](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsColumnAliasing())`()` Retrieves whether this database supports column aliasing. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsConvert](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsConvert())`()` Retrieves whether this database supports the JDBC scalar function`CONVERT`for the conversion of one JDBC type to another. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsConvert](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsConvert(kotlin.Int,%20kotlin.Int))`(`fromType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves whether this database supports the JDBC scalar function`CONVERT`for conversions between the JDBC types*fromType* and*toType*. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsCoreSQLGrammar](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsCoreSQLGrammar())`()` Retrieves whether this database supports the ODBC Core SQL grammar. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsCorrelatedSubqueries](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsCorrelatedSubqueries())`()` Retrieves whether this database supports correlated subqueries. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsDataDefinitionAndDataManipulationTransactions](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsDataDefinitionAndDataManipulationTransactions())`()` Retrieves whether this database supports both data definition and data manipulation statements within a transaction. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsDataManipulationTransactionsOnly](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsDataManipulationTransactionsOnly())`()` Retrieves whether this database supports only data manipulation statements within a transaction. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsDifferentTableCorrelationNames](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsDifferentTableCorrelationNames())`()` Retrieves whether, when table correlation names are supported, they are restricted to being different from the names of the tables. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsExpressionsInOrderBy](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsExpressionsInOrderBy())`()` Retrieves whether this database supports expressions in`ORDER BY`lists. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsExtendedSQLGrammar](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsExtendedSQLGrammar())`()` Retrieves whether this database supports the ODBC Extended SQL grammar. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsFullOuterJoins](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsFullOuterJoins())`()` Retrieves whether this database supports full nested outer joins. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsGetGeneratedKeys](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsGetGeneratedKeys())`()` Retrieves whether auto-generated keys can be retrieved after a statement has been executed |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsGroupBy](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsGroupBy())`()` Retrieves whether this database supports some form of`GROUP BY`clause. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsGroupByBeyondSelect](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsGroupByBeyondSelect())`()` Retrieves whether this database supports using columns not included in the`SELECT`statement in a`GROUP BY`clause provided that all of the columns in the`SELECT`statement are included in the`GROUP BY`clause. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsGroupByUnrelated](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsGroupByUnrelated())`()` Retrieves whether this database supports using a column that is not in the`SELECT`statement in a`GROUP BY`clause. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsIntegrityEnhancementFacility](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsIntegrityEnhancementFacility())`()` Retrieves whether this database supports the SQL Integrity Enhancement Facility. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsLikeEscapeClause](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsLikeEscapeClause())`()` Retrieves whether this database supports specifying a`LIKE`escape clause. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsLimitedOuterJoins](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsLimitedOuterJoins())`()` Retrieves whether this database provides limited support for outer joins. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsMinimumSQLGrammar](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsMinimumSQLGrammar())`()` Retrieves whether this database supports the ODBC Minimum SQL grammar. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsMixedCaseIdentifiers](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsMixedCaseIdentifiers())`()` Retrieves whether this database treats mixed case unquoted SQL identifiers as case sensitive and as a result stores them in mixed case. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsMixedCaseQuotedIdentifiers](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsMixedCaseQuotedIdentifiers())`()` Retrieves whether this database treats mixed case quoted SQL identifiers as case sensitive and as a result stores them in mixed case. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsMultipleOpenResults](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsMultipleOpenResults())`()` Retrieves whether it is possible to have multiple`ResultSet`objects returned from a`CallableStatement`object simultaneously. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsMultipleResultSets](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsMultipleResultSets())`()` Retrieves whether this database supports getting multiple`ResultSet`objects from a single call to the method`execute`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsMultipleTransactions](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsMultipleTransactions())`()` Retrieves whether this database allows having multiple transactions open at once (on different connections). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsNamedParameters](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsNamedParameters())`()` Retrieves whether this database supports named parameters to callable statements. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsNonNullableColumns](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsNonNullableColumns())`()` Retrieves whether columns in this database may be defined as non-nullable. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsOpenCursorsAcrossCommit](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsOpenCursorsAcrossCommit())`()` Retrieves whether this database supports keeping cursors open across commits. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsOpenCursorsAcrossRollback](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsOpenCursorsAcrossRollback())`()` Retrieves whether this database supports keeping cursors open across rollbacks. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsOpenStatementsAcrossCommit](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsOpenStatementsAcrossCommit())`()` Retrieves whether this database supports keeping statements open across commits. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsOpenStatementsAcrossRollback](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsOpenStatementsAcrossRollback())`()` Retrieves whether this database supports keeping statements open across rollbacks. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsOrderByUnrelated](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsOrderByUnrelated())`()` Retrieves whether this database supports using a column that is not in the`SELECT`statement in an`ORDER BY`clause. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsOuterJoins](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsOuterJoins())`()` Retrieves whether this database supports some form of outer join. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsPositionedDelete](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsPositionedDelete())`()` Retrieves whether this database supports positioned`DELETE`statements. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsPositionedUpdate](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsPositionedUpdate())`()` Retrieves whether this database supports positioned`UPDATE`statements. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsResultSetConcurrency](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsResultSetConcurrency(kotlin.Int,%20kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `concurrency:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves whether this database supports the given concurrency type in combination with the given result set type. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsResultSetHoldability](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsResultSetHoldability(kotlin.Int))`(`holdability:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves whether this database supports the given result set holdability. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsResultSetType](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsResultSetType(kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves whether this database supports the given result set type. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsSavepoints](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsSavepoints())`()` Retrieves whether this database supports savepoints. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsSchemasInDataManipulation](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsSchemasInDataManipulation())`()` Retrieves whether a schema name can be used in a data manipulation statement. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsSchemasInIndexDefinitions](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsSchemasInIndexDefinitions())`()` Retrieves whether a schema name can be used in an index definition statement. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsSchemasInPrivilegeDefinitions](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsSchemasInPrivilegeDefinitions())`()` Retrieves whether a schema name can be used in a privilege definition statement. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsSchemasInProcedureCalls](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsSchemasInProcedureCalls())`()` Retrieves whether a schema name can be used in a procedure call statement. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsSchemasInTableDefinitions](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsSchemasInTableDefinitions())`()` Retrieves whether a schema name can be used in a table definition statement. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsSelectForUpdate](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsSelectForUpdate())`()` Retrieves whether this database supports`SELECT FOR UPDATE`statements. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsStatementPooling](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsStatementPooling())`()` Retrieves whether this database supports statement pooling. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsStoredFunctionsUsingCallSyntax](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsStoredFunctionsUsingCallSyntax())`()` Retrieves whether this database supports invoking user-defined or vendor functions using the stored procedure escape syntax. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsStoredProcedures](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsStoredProcedures())`()` Retrieves whether this database supports stored procedure calls that use the stored procedure escape syntax. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsSubqueriesInComparisons](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsSubqueriesInComparisons())`()` Retrieves whether this database supports subqueries in comparison expressions. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsSubqueriesInExists](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsSubqueriesInExists())`()` Retrieves whether this database supports subqueries in`EXISTS`expressions. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsSubqueriesInIns](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsSubqueriesInIns())`()` Retrieves whether this database supports subqueries in`IN`expressions. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsSubqueriesInQuantifieds](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsSubqueriesInQuantifieds())`()` Retrieves whether this database supports subqueries in quantified expressions. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsTableCorrelationNames](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsTableCorrelationNames())`()` Retrieves whether this database supports table correlation names. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsTransactionIsolationLevel](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsTransactionIsolationLevel(kotlin.Int))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves whether this database supports the given transaction isolation level. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsTransactions](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsTransactions())`()` Retrieves whether this database supports transactions. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsUnion](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsUnion())`()` Retrieves whether this database supports SQL`UNION`. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsUnionAll](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#supportsUnionAll())`()` Retrieves whether this database supports SQL`UNION ALL`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [updatesAreDetected](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#updatesAreDetected(kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves whether or not a visible row update can be detected by calling the method`ResultSet.rowUpdated`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [usesLocalFilePerTable](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#usesLocalFilePerTable())`()` Retrieves whether this database uses a file for each table. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [usesLocalFiles](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#usesLocalFiles())`()` Retrieves whether this database stores tables in a local file. |

| Inherited functions ||
|---|---|
| From class [Wrapper](https://developer.android.com/reference/kotlin/java/sql/Wrapper) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWrapperFor](https://developer.android.com/reference/kotlin/java/sql/Wrapper#isWrapperFor(java.lang.Class))`(`iface:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`)` <br /> Returns true if this either implements the interface argument or is directly or indirectly a wrapper for an object that does. Returns false otherwise. If this implements the interface then return true, else if this is a wrapper then return the result of recursively calling`isWrapperFor`on the wrapped object. If this does not implement the interface and is not a wrapper, return false. This method should be implemented as a low-cost operation compared to`unwrap`so that callers can use this method to avoid expensive`unwrap`calls that may fail. If this method returns true then calling`unwrap`with the same argument should succeed. <br /> | | T | [unwrap](https://developer.android.com/reference/kotlin/java/sql/Wrapper#unwrap(java.lang.Class))`(`iface:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`)` <br /> Returns an object that implements the given interface to allow access to non-standard methods, or standard methods not exposed by the proxy. If the receiver implements the interface then the result is the receiver or a proxy for the receiver. If the receiver is a wrapper and the wrapped object implements the interface then the result is the wrapped object or a proxy for the wrapped object. Otherwise return the the result of calling`unwrap`recursively on the wrapped object or a proxy for that result. If the receiver is not a wrapper and does not implement the interface, then an`SQLException`is thrown. <br /> | ||

## Constants

### attributeNoNulls

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val attributeNoNulls: Short
```

Indicates that`NULL`values might not be allowed.

A possible value for the column`NULLABLE`in the`ResultSet`object returned by the method`getAttributes`. 

 Value: 0

### attributeNullable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val attributeNullable: Short
```

Indicates that`NULL`values are definitely allowed.

A possible value for the column`NULLABLE`in the`ResultSet`object returned by the method`getAttributes`. 

 Value: 1

### attributeNullableUnknown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val attributeNullableUnknown: Short
```

Indicates that whether`NULL`values are allowed is not known.

A possible value for the column`NULLABLE`in the`ResultSet`object returned by the method`getAttributes`. 

 Value: 2

### bestRowNotPseudo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val bestRowNotPseudo: Int
```

Indicates that the best row identifier is NOT a pseudo column.

A possible value for the column`PSEUDO_COLUMN`in the`ResultSet`object returned by the method`getBestRowIdentifier`. 

 Value: 1

### bestRowPseudo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val bestRowPseudo: Int
```

Indicates that the best row identifier is a pseudo column.

A possible value for the column`PSEUDO_COLUMN`in the`ResultSet`object returned by the method`getBestRowIdentifier`. 

 Value: 2

### bestRowSession

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val bestRowSession: Int
```

Indicates that the scope of the best row identifier is the remainder of the current session.

A possible value for the column`SCOPE`in the`ResultSet`object returned by the method`getBestRowIdentifier`. 

 Value: 2

### bestRowTemporary

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val bestRowTemporary: Int
```

Indicates that the scope of the best row identifier is very temporary, lasting only while the row is being used.

A possible value for the column`SCOPE`in the`ResultSet`object returned by the method`getBestRowIdentifier`. 

 Value: 0

### bestRowTransaction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val bestRowTransaction: Int
```

Indicates that the scope of the best row identifier is the remainder of the current transaction.

A possible value for the column`SCOPE`in the`ResultSet`object returned by the method`getBestRowIdentifier`. 

 Value: 1

### bestRowUnknown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val bestRowUnknown: Int
```

Indicates that the best row identifier may or may not be a pseudo column.

A possible value for the column`PSEUDO_COLUMN`in the`ResultSet`object returned by the method`getBestRowIdentifier`. 

 Value: 0

### columnNoNulls

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val columnNoNulls: Int
```

Indicates that the column might not allow`NULL`values.

A possible value for the column`NULLABLE`in the`ResultSet`returned by the method`getColumns`. 

 Value: 0

### columnNullable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val columnNullable: Int
```

Indicates that the column definitely allows`NULL`values.

A possible value for the column`NULLABLE`in the`ResultSet`returned by the method`getColumns`. 

 Value: 1

### columnNullableUnknown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val columnNullableUnknown: Int
```

Indicates that the nullability of columns is unknown.

A possible value for the column`NULLABLE`in the`ResultSet`returned by the method`getColumns`. 

 Value: 2

### functionColumnIn

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val functionColumnIn: Int
```

Indicates that the parameter or column is an IN parameter.

A possible value for the column`COLUMN_TYPE`in the`ResultSet`returned by the method`getFunctionColumns`. 

 Value: 1

### functionColumnInOut

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val functionColumnInOut: Int
```

Indicates that the parameter or column is an INOUT parameter.

A possible value for the column`COLUMN_TYPE`in the`ResultSet`returned by the method`getFunctionColumns`. 

 Value: 2

### functionColumnOut

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val functionColumnOut: Int
```

Indicates that the parameter or column is an OUT parameter.

A possible value for the column`COLUMN_TYPE`in the`ResultSet`returned by the method`getFunctionColumns`. 

 Value: 3

### functionColumnResult

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val functionColumnResult: Int
```

Indicates that the parameter or column is a column in a result set.

A possible value for the column`COLUMN_TYPE`in the`ResultSet`returned by the method`getFunctionColumns`. 

 Value: 5

### functionColumnUnknown

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val functionColumnUnknown: Int
```

Indicates that type of the parameter or column is unknown.

A possible value for the column`COLUMN_TYPE`in the`ResultSet`returned by the method`getFunctionColumns`. 

 Value: 0

### functionNoNulls

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val functionNoNulls: Int
```

Indicates that`NULL`values are not allowed.

A possible value for the column`NULLABLE`in the`ResultSet`object returned by the method`getFunctionColumns`. 

 Value: 0

### functionNoTable

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val functionNoTable: Int
```

Indicates that the function does not return a table.

A possible value for column`FUNCTION_TYPE`in the`ResultSet`object returned by the method`getFunctions`. 

 Value: 1

### functionNullable

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val functionNullable: Int
```

Indicates that`NULL`values are allowed.

A possible value for the column`NULLABLE`in the`ResultSet`object returned by the method`getFunctionColumns`. 

 Value: 1

### functionNullableUnknown

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val functionNullableUnknown: Int
```

Indicates that whether`NULL`values are allowed is unknown.

A possible value for the column`NULLABLE`in the`ResultSet`object returned by the method`getFunctionColumns`. 

 Value: 2

### functionResultUnknown

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val functionResultUnknown: Int
```

Indicates that it is not known whether the function returns a result or a table.

A possible value for column`FUNCTION_TYPE`in the`ResultSet`object returned by the method`getFunctions`. 

 Value: 0

### functionReturn

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val functionReturn: Int
```

Indicates that the parameter or column is a return value.

A possible value for the column`COLUMN_TYPE`in the`ResultSet`returned by the method`getFunctionColumns`. 

 Value: 4

### functionReturnsTable

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val functionReturnsTable: Int
```

Indicates that the function returns a table.

A possible value for column`FUNCTION_TYPE`in the`ResultSet`object returned by the method`getFunctions`. 

 Value: 2

### importedKeyCascade

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val importedKeyCascade: Int
```

For the column`UPDATE_RULE`, indicates that when the primary key is updated, the foreign key (imported key) is changed to agree with it. For the column`DELETE_RULE`, it indicates that when the primary key is deleted, rows that imported that key are deleted.

A possible value for the columns`UPDATE_RULE`and`DELETE_RULE`in the`ResultSet`objects returned by the methods`getImportedKeys`,`getExportedKeys`, and`getCrossReference`. 

 Value: 0

### importedKeyInitiallyDeferred

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val importedKeyInitiallyDeferred: Int
```

Indicates deferrability. See SQL-92 for a definition.

A possible value for the column`DEFERRABILITY`in the`ResultSet`objects returned by the methods`getImportedKeys`,`getExportedKeys`, and`getCrossReference`. 

 Value: 5

### importedKeyInitiallyImmediate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val importedKeyInitiallyImmediate: Int
```

Indicates deferrability. See SQL-92 for a definition.

A possible value for the column`DEFERRABILITY`in the`ResultSet`objects returned by the methods`getImportedKeys`,`getExportedKeys`, and`getCrossReference`. 

 Value: 6

### importedKeyNoAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val importedKeyNoAction: Int
```

For the columns`UPDATE_RULE`and`DELETE_RULE`, indicates that if the primary key has been imported, it cannot be updated or deleted.

A possible value for the columns`UPDATE_RULE`and`DELETE_RULE`in the`ResultSet`objects returned by the methods`getImportedKeys`,`getExportedKeys`, and`getCrossReference`. 

 Value: 3

### importedKeyNotDeferrable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val importedKeyNotDeferrable: Int
```

Indicates deferrability. See SQL-92 for a definition.

A possible value for the column`DEFERRABILITY`in the`ResultSet`objects returned by the methods`getImportedKeys`,`getExportedKeys`, and`getCrossReference`. 

 Value: 7

### importedKeyRestrict

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val importedKeyRestrict: Int
```

For the column`UPDATE_RULE`, indicates that a primary key may not be updated if it has been imported by another table as a foreign key. For the column`DELETE_RULE`, indicates that a primary key may not be deleted if it has been imported by another table as a foreign key.

A possible value for the columns`UPDATE_RULE`and`DELETE_RULE`in the`ResultSet`objects returned by the methods`getImportedKeys`,`getExportedKeys`, and`getCrossReference`. 

 Value: 1

### importedKeySetDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val importedKeySetDefault: Int
```

For the columns`UPDATE_RULE`and`DELETE_RULE`, indicates that if the primary key is updated or deleted, the foreign key (imported key) is set to the default value.

A possible value for the columns`UPDATE_RULE`and`DELETE_RULE`in the`ResultSet`objects returned by the methods`getImportedKeys`,`getExportedKeys`, and`getCrossReference`. 

 Value: 4

### importedKeySetNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val importedKeySetNull: Int
```

For the columns`UPDATE_RULE`and`DELETE_RULE`, indicates that when the primary key is updated or deleted, the foreign key (imported key) is changed to`NULL`.

A possible value for the columns`UPDATE_RULE`and`DELETE_RULE`in the`ResultSet`objects returned by the methods`getImportedKeys`,`getExportedKeys`, and`getCrossReference`. 

 Value: 2

### procedureColumnIn

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val procedureColumnIn: Int
```

Indicates that the column stores IN parameters.

A possible value for the column`COLUMN_TYPE`in the`ResultSet`returned by the method`getProcedureColumns`. 

 Value: 1

### procedureColumnInOut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val procedureColumnInOut: Int
```

Indicates that the column stores INOUT parameters.

A possible value for the column`COLUMN_TYPE`in the`ResultSet`returned by the method`getProcedureColumns`. 

 Value: 2

### procedureColumnOut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val procedureColumnOut: Int
```

Indicates that the column stores OUT parameters.

A possible value for the column`COLUMN_TYPE`in the`ResultSet`returned by the method`getProcedureColumns`. 

 Value: 4

### procedureColumnResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val procedureColumnResult: Int
```

Indicates that the column stores results.

A possible value for the column`COLUMN_TYPE`in the`ResultSet`returned by the method`getProcedureColumns`. 

 Value: 3

### procedureColumnReturn

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val procedureColumnReturn: Int
```

Indicates that the column stores return values.

A possible value for the column`COLUMN_TYPE`in the`ResultSet`returned by the method`getProcedureColumns`. 

 Value: 5

### procedureColumnUnknown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val procedureColumnUnknown: Int
```

Indicates that type of the column is unknown.

A possible value for the column`COLUMN_TYPE`in the`ResultSet`returned by the method`getProcedureColumns`. 

 Value: 0

### procedureNoNulls

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val procedureNoNulls: Int
```

Indicates that`NULL`values are not allowed.

A possible value for the column`NULLABLE`in the`ResultSet`object returned by the method`getProcedureColumns`. 

 Value: 0

### procedureNoResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val procedureNoResult: Int
```

Indicates that the procedure does not return a result.

A possible value for column`PROCEDURE_TYPE`in the`ResultSet`object returned by the method`getProcedures`. 

 Value: 1

### procedureNullable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val procedureNullable: Int
```

Indicates that`NULL`values are allowed.

A possible value for the column`NULLABLE`in the`ResultSet`object returned by the method`getProcedureColumns`. 

 Value: 1

### procedureNullableUnknown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val procedureNullableUnknown: Int
```

Indicates that whether`NULL`values are allowed is unknown.

A possible value for the column`NULLABLE`in the`ResultSet`object returned by the method`getProcedureColumns`. 

 Value: 2

### procedureResultUnknown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val procedureResultUnknown: Int
```

Indicates that it is not known whether the procedure returns a result.

A possible value for column`PROCEDURE_TYPE`in the`ResultSet`object returned by the method`getProcedures`. 

 Value: 0

### procedureReturnsResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val procedureReturnsResult: Int
```

Indicates that the procedure returns a result.

A possible value for column`PROCEDURE_TYPE`in the`ResultSet`object returned by the method`getProcedures`. 

 Value: 2

### sqlStateSQL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val sqlStateSQL: Int
```

A possible return value for the method`DatabaseMetaData.getSQLStateType`which is used to indicate whether the value returned by the method`SQLException.getSQLState`is an SQLSTATE value.

<br />

 Value: 2

### sqlStateSQL99

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val sqlStateSQL99: Int
```

A possible return value for the method`DatabaseMetaData.getSQLStateType`which is used to indicate whether the value returned by the method`SQLException.getSQLState`is an SQL99 SQLSTATE value.

**Note:** This constant remains only for compatibility reasons. Developers should use the constant`sqlStateSQL`instead. 

 Value: 2

### sqlStateXOpen

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val sqlStateXOpen: Int
```

A possible return value for the method`DatabaseMetaData.getSQLStateType`which is used to indicate whether the value returned by the method`SQLException.getSQLState`is an X/Open (now know as Open Group) SQL CLI SQLSTATE value.

<br />

 Value: 1

### tableIndexClustered

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val tableIndexClustered: Short
```

Indicates that this table index is a clustered index.

A possible value for column`TYPE`in the`ResultSet`object returned by the method`getIndexInfo`. 

 Value: 1

### tableIndexHashed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val tableIndexHashed: Short
```

Indicates that this table index is a hashed index.

A possible value for column`TYPE`in the`ResultSet`object returned by the method`getIndexInfo`. 

 Value: 2

### tableIndexOther

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val tableIndexOther: Short
```

Indicates that this table index is not a clustered index, a hashed index, or table statistics; it is something other than these.

A possible value for column`TYPE`in the`ResultSet`object returned by the method`getIndexInfo`. 

 Value: 3

### tableIndexStatistic

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val tableIndexStatistic: Short
```

Indicates that this column contains table statistics that are returned in conjunction with a table's index descriptions.

A possible value for column`TYPE`in the`ResultSet`object returned by the method`getIndexInfo`. 

 Value: 0

### typeNoNulls

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val typeNoNulls: Int
```

Indicates that a`NULL`value is NOT allowed for this data type.

A possible value for column`NULLABLE`in the`ResultSet`object returned by the method`getTypeInfo`. 

 Value: 0

### typeNullable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val typeNullable: Int
```

Indicates that a`NULL`value is allowed for this data type.

A possible value for column`NULLABLE`in the`ResultSet`object returned by the method`getTypeInfo`. 

 Value: 1

### typeNullableUnknown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val typeNullableUnknown: Int
```

Indicates that it is not known whether a`NULL`value is allowed for this data type.

A possible value for column`NULLABLE`in the`ResultSet`object returned by the method`getTypeInfo`. 

 Value: 2

### typePredBasic

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val typePredBasic: Int
```

Indicates that the data type can be only be used in`WHERE`search clauses that do not use`LIKE`predicates.

A possible value for column`SEARCHABLE`in the`ResultSet`object returned by the method`getTypeInfo`. 

 Value: 2

### typePredChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val typePredChar: Int
```

Indicates that the data type can be only be used in`WHERE`search clauses that use`LIKE`predicates.

A possible value for column`SEARCHABLE`in the`ResultSet`object returned by the method`getTypeInfo`. 

 Value: 1

### typePredNone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val typePredNone: Int
```

Indicates that`WHERE`search clauses are not supported for this type.

A possible value for column`SEARCHABLE`in the`ResultSet`object returned by the method`getTypeInfo`. 

 Value: 0

### typeSearchable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val typeSearchable: Int
```

Indicates that all`WHERE`search clauses can be based on this type.

A possible value for column`SEARCHABLE`in the`ResultSet`object returned by the method`getTypeInfo`. 

 Value: 3

### versionColumnNotPseudo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val versionColumnNotPseudo: Int
```

Indicates that this version column is NOT a pseudo column.

A possible value for the column`PSEUDO_COLUMN`in the`ResultSet`object returned by the method`getVersionColumns`. 

 Value: 1

### versionColumnPseudo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val versionColumnPseudo: Int
```

Indicates that this version column is a pseudo column.

A possible value for the column`PSEUDO_COLUMN`in the`ResultSet`object returned by the method`getVersionColumns`. 

 Value: 2

### versionColumnUnknown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val versionColumnUnknown: Int
```

Indicates that this version column may or may not be a pseudo column.

A possible value for the column`PSEUDO_COLUMN`in the`ResultSet`object returned by the method`getVersionColumns`. 

 Value: 0

## Public methods

### allProceduresAreCallable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun allProceduresAreCallable(): Boolean
```

Retrieves whether the current user can call all the procedures returned by the method`getProcedures`.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### allTablesAreSelectable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun allTablesAreSelectable(): Boolean
```

Retrieves whether the current user can use all the tables returned by the method`getTables`in a`SELECT`statement.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### autoCommitFailureClosesAllResultSets

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun autoCommitFailureClosesAllResultSets(): Boolean
```

Retrieves whether a`SQLException`while autoCommit is`true`inidcates that all open ResultSets are closed, even ones that are holdable. When a`SQLException`occurs while autocommit is`true`, it is vendor specific whether the JDBC driver responds with a commit operation, a rollback operation, or by doing neither a commit nor a rollback. A potential result of this difference is in whether or not holdable ResultSets are closed.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### dataDefinitionCausesTransactionCommit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun dataDefinitionCausesTransactionCommit(): Boolean
```

Retrieves whether a data definition statement within a transaction forces the transaction to commit.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### dataDefinitionIgnoredInTransactions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun dataDefinitionIgnoredInTransactions(): Boolean
```

Retrieves whether this database ignores a data definition statement within a transaction.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### deletesAreDetected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun deletesAreDetected(type: Int): Boolean
```

Retrieves whether or not a visible row delete can be detected by calling the method`ResultSet.rowDeleted`. If the method`deletesAreDetected`returns`false`, it means that deleted rows are removed from the result set.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the`ResultSet`type; one of`ResultSet.TYPE_FORWARD_ONLY`,`ResultSet.TYPE_SCROLL_INSENSITIVE`, or`ResultSet.TYPE_SCROLL_SENSITIVE` |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if deletes are detected by the given result set type;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### doesMaxRowSizeIncludeBlobs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun doesMaxRowSizeIncludeBlobs(): Boolean
```

Retrieves whether the return value for the method`getMaxRowSize`includes the SQL data types`LONGVARCHAR`and`LONGVARBINARY`.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAttributes(
    catalog: String!, 
    schemaPattern: String!, 
    typeNamePattern: String!, 
    attributeNamePattern: String!
): ResultSet!
```

Retrieves a description of the given attribute of the given type for a user-defined type (UDT) that is available in the given schema and catalog.

Descriptions are returned only for attributes of UDTs matching the catalog, schema, type, and attribute name criteria. They are ordered by`TYPE_CAT`,`TYPE_SCHEM`,`TYPE_NAME`and`ORDINAL_POSITION`. This description does not contain inherited attributes.

The`ResultSet`object that is returned has the following columns:

1. **TYPE_CAT** String =\> type catalog (may be`null`)
2. **TYPE_SCHEM** String =\> type schema (may be`null`)
3. **TYPE_NAME**String =\> type name
4. **ATTR_NAME**String =\> attribute name
5. **DATA_TYPE**int =\> attribute type SQL type from java.sql.Types
6. **ATTR_TYPE_NAME**String =\> Data source dependent type name. For a UDT, the type name is fully qualified. For a REF, the type name is fully qualified and represents the target type of the reference type.
7. **ATTR_SIZE**int =\> column size. For char or date types this is the maximum number of characters; for numeric or decimal types this is precision.
8. **DECIMAL_DIGITS**int =\> the number of fractional digits. Null is returned for data types where DECIMAL_DIGITS is not applicable.
9. **NUM_PREC_RADIX**int =\> Radix (typically either 10 or 2)
10. **NULLABLE** int =\> whether NULL is allowed
 - attributeNoNulls - might not allow NULL values
 - attributeNullable - definitely allows NULL values
 - attributeNullableUnknown - nullability unknown
11. **REMARKS** String =\> comment describing column (may be`null`)
12. **ATTR_DEF** String =\> default value (may be`null`)
13. **SQL_DATA_TYPE**int =\> unused
14. **SQL_DATETIME_SUB**int =\> unused
15. **CHAR_OCTET_LENGTH**int =\> for char types the maximum number of bytes in the column
16. **ORDINAL_POSITION**int =\> index of the attribute in the UDT (starting at 1)
17. **IS_NULLABLE** String =\> ISO rules are used to determine the nullability for a attribute.
 - YES --- if the attribute can include NULLs
 - NO --- if the attribute cannot include NULLs
 - empty string --- if the nullability for the attribute is unknown
18. **SCOPE_CATALOG** String =\> catalog of table that is the scope of a reference attribute (`null`if DATA_TYPE isn't REF)
19. **SCOPE_SCHEMA** String =\> schema of table that is the scope of a reference attribute (`null`if DATA_TYPE isn't REF)
20. **SCOPE_TABLE** String =\> table name that is the scope of a reference attribute (`null`if the DATA_TYPE isn't REF)
21. **SOURCE_DATA_TYPE** short =\> source type of a distinct type or user-generated Ref type,SQL type from java.sql.Types (`null`if DATA_TYPE isn't DISTINCT or user-generated REF)

| Parameters ||
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in the database; "" retrieves those without a catalog;`null`means that the catalog name should not be used to narrow the search |
| `schemaPattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name pattern; must match the schema name as it is stored in the database; "" retrieves those without a schema;`null`means that the schema name should not be used to narrow the search |
| `typeNamePattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a type name pattern; must match the type name as it is stored in the database |
| --- | --- |
| `attributeNamePattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an attribute name pattern; must match the attribute name as it is declared in the database |

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | a`ResultSet`object in which each row is an attribute description |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getSearchStringEscape](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSearchStringEscape()) 

### getBestRowIdentifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBestRowIdentifier(
    catalog: String!, 
    schema: String!, 
    table: String!, 
    scope: Int, 
    nullable: Boolean
): ResultSet!
```

Retrieves a description of a table's optimal set of columns that uniquely identifies a row. They are ordered by SCOPE.

Each column description has the following columns:

1. **SCOPE** short =\> actual scope of result
 - bestRowTemporary - very temporary, while using row
 - bestRowTransaction - valid for remainder of current transaction
 - bestRowSession - valid for remainder of current session
2. **COLUMN_NAME**String =\> column name
3. **DATA_TYPE**int =\> SQL data type from java.sql.Types
4. **TYPE_NAME**String =\> Data source dependent type name, for a UDT the type name is fully qualified
5. **COLUMN_SIZE**int =\> precision
6. **BUFFER_LENGTH**int =\> not used
7. **DECIMAL_DIGITS**short =\> scale - Null is returned for data types where DECIMAL_DIGITS is not applicable.
8. **PSEUDO_COLUMN** short =\> is this a pseudo column like an Oracle ROWID
 - bestRowUnknown - may or may not be pseudo column
 - bestRowNotPseudo - is NOT a pseudo column
 - bestRowPseudo - is a pseudo column

The COLUMN_SIZE column represents the specified column size for the given column. For numeric data, this is the maximum precision. For character data, this is the length in characters. For datetime datatypes, this is the length in characters of the String representation (assuming the maximum allowed precision of the fractional seconds component). For binary data, this is the length in bytes. For the ROWID datatype, this is the length in bytes. Null is returned for data types where the column size is not applicable.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in the database; "" retrieves those without a catalog;`null`means that the catalog name should not be used to narrow the search |
| `schema` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name; must match the schema name as it is stored in the database; "" retrieves those without a schema;`null`means that the schema name should not be used to narrow the search |
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a table name; must match the table name as it is stored in the database |
| --- | --- |
| `scope` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the scope of interest; use same values as SCOPE |
| `nullable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):include columns that are nullable. |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | `ResultSet`- each row is a column description |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getCatalogSeparator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCatalogSeparator(): String!
```

Retrieves the`String`that this database uses as the separator between a catalog and table name.

| Return ||
|-----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the separator string |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getCatalogTerm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCatalogTerm(): String!
```

Retrieves the database vendor's preferred term for "catalog".

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the vendor term for "catalog" |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getCatalogs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCatalogs(): ResultSet!
```

Retrieves the catalog names available in this database. The results are ordered by catalog name.

The catalog column is:

1. **TABLE_CAT**String =\> catalog name

| Return ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | a`ResultSet`object in which each row has a single`String`column that is a catalog name |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getClientInfoProperties

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getClientInfoProperties(): ResultSet!
```

Retrieves a list of the client info properties that the driver supports. The result set contains the following columns

<br />

1. **NAME** String=\> The name of the client info property 
2. **MAX_LEN** int=\> The maximum length of the value for the property 
3. **DEFAULT_VALUE** String=\> The default value of the property 
4. **DESCRIPTION**String=\> A description of the property. This will typically contain information as to where this property is stored in the database.

The`ResultSet`is sorted by the NAME column

<br />

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | A`ResultSet`object; each row is a supported client info property <br /> |

| Exceptions ||
|-------------------------|------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs <br /> |

### getColumnPrivileges

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumnPrivileges(
    catalog: String!, 
    schema: String!, 
    table: String!, 
    columnNamePattern: String!
): ResultSet!
```

Retrieves a description of the access rights for a table's columns.

Only privileges matching the column name criteria are returned. They are ordered by COLUMN_NAME and PRIVILEGE.

Each privilige description has the following columns:

1. **TABLE_CAT** String =\> table catalog (may be`null`)
2. **TABLE_SCHEM** String =\> table schema (may be`null`)
3. **TABLE_NAME**String =\> table name
4. **COLUMN_NAME**String =\> column name
5. **GRANTOR** String =\> grantor of access (may be`null`)
6. **GRANTEE**String =\> grantee of access
7. **PRIVILEGE**String =\> name of access (SELECT, INSERT, UPDATE, REFRENCES, ...)
8. **IS_GRANTABLE** String =\> "YES" if grantee is permitted to grant to others; "NO" if not;`null`if unknown

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in the database; "" retrieves those without a catalog;`null`means that the catalog name should not be used to narrow the search |
| `schema` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name; must match the schema name as it is stored in the database; "" retrieves those without a schema;`null`means that the schema name should not be used to narrow the search |
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a table name; must match the table name as it is stored in the database |
| --- | --- |
| `columnNamePattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a column name pattern; must match the column name as it is stored in the database |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | `ResultSet`- each row is a column privilege description |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getSearchStringEscape](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSearchStringEscape()) 

### getColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumns(
    catalog: String!, 
    schemaPattern: String!, 
    tableNamePattern: String!, 
    columnNamePattern: String!
): ResultSet!
```

Retrieves a description of table columns available in the specified catalog.

Only column descriptions matching the catalog, schema, table and column name criteria are returned. They are ordered by`TABLE_CAT`,`TABLE_SCHEM`,`TABLE_NAME`, and`ORDINAL_POSITION`.

Each column description has the following columns:

1. **TABLE_CAT** String =\> table catalog (may be`null`)
2. **TABLE_SCHEM** String =\> table schema (may be`null`)
3. **TABLE_NAME**String =\> table name
4. **COLUMN_NAME**String =\> column name
5. **DATA_TYPE**int =\> SQL type from java.sql.Types
6. **TYPE_NAME**String =\> Data source dependent type name, for a UDT the type name is fully qualified
7. **COLUMN_SIZE**int =\> column size.
8. **BUFFER_LENGTH**is not used.
9. **DECIMAL_DIGITS**int =\> the number of fractional digits. Null is returned for data types where DECIMAL_DIGITS is not applicable.
10. **NUM_PREC_RADIX**int =\> Radix (typically either 10 or 2)
11. **NULLABLE** int =\> is NULL allowed.
 - columnNoNulls - might not allow`NULL`values
 - columnNullable - definitely allows`NULL`values
 - columnNullableUnknown - nullability unknown
12. **REMARKS** String =\> comment describing column (may be`null`)
13. **COLUMN_DEF** String =\> default value for the column, which should be interpreted as a string when the value is enclosed in single quotes (may be`null`)
14. **SQL_DATA_TYPE**int =\> unused
15. **SQL_DATETIME_SUB**int =\> unused
16. **CHAR_OCTET_LENGTH**int =\> for char types the maximum number of bytes in the column
17. **ORDINAL_POSITION**int =\> index of column in table (starting at 1)
18. **IS_NULLABLE** String =\> ISO rules are used to determine the nullability for a column.
 - YES --- if the column can include NULLs
 - NO --- if the column cannot include NULLs
 - empty string --- if the nullability for the column is unknown
19. **SCOPE_CATALOG** String =\> catalog of table that is the scope of a reference attribute (`null`if DATA_TYPE isn't REF)
20. **SCOPE_SCHEMA** String =\> schema of table that is the scope of a reference attribute (`null`if the DATA_TYPE isn't REF)
21. **SCOPE_TABLE** String =\> table name that this the scope of a reference attribute (`null`if the DATA_TYPE isn't REF)
22. **SOURCE_DATA_TYPE** short =\> source type of a distinct type or user-generated Ref type, SQL type from java.sql.Types (`null`if DATA_TYPE isn't DISTINCT or user-generated REF)
23. **IS_AUTOINCREMENT** String =\> Indicates whether this column is auto incremented
 - YES --- if the column is auto incremented
 - NO --- if the column is not auto incremented
 - empty string --- if it cannot be determined whether the column is auto incremented
24. **IS_GENERATEDCOLUMN** String =\> Indicates whether this is a generated column
 - YES --- if this a generated column
 - NO --- if this not a generated column
 - empty string --- if it cannot be determined whether this is a generated column

The COLUMN_SIZE column specifies the column size for the given column. For numeric data, this is the maximum precision. For character data, this is the length in characters. For datetime datatypes, this is the length in characters of the String representation (assuming the maximum allowed precision of the fractional seconds component). For binary data, this is the length in bytes. For the ROWID datatype, this is the length in bytes. Null is returned for data types where the column size is not applicable.

| Parameters ||
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in the database; "" retrieves those without a catalog;`null`means that the catalog name should not be used to narrow the search |
| `schemaPattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name pattern; must match the schema name as it is stored in the database; "" retrieves those without a schema;`null`means that the schema name should not be used to narrow the search |
| `tableNamePattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a table name pattern; must match the table name as it is stored in the database |
| --- | --- |
| `columnNamePattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a column name pattern; must match the column name as it is stored in the database |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | `ResultSet`- each row is a column description |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getSearchStringEscape](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSearchStringEscape()) 

### getConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getConnection(): Connection!
```

Retrieves the connection that produced this metadata object.

<br />

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [Connection](https://developer.android.com/reference/kotlin/java/sql/Connection)! | the connection that produced this metadata object |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getCrossReference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCrossReference(
    parentCatalog: String!, 
    parentSchema: String!, 
    parentTable: String!, 
    foreignCatalog: String!, 
    foreignSchema: String!, 
    foreignTable: String!
): ResultSet!
```

Retrieves a description of the foreign key columns in the given foreign key table that reference the primary key or the columns representing a unique constraint of the parent table (could be the same or a different table). The number of columns returned from the parent table must match the number of columns that make up the foreign key. They are ordered by FKTABLE_CAT, FKTABLE_SCHEM, FKTABLE_NAME, and KEY_SEQ.

Each foreign key column description has the following columns:

1. **PKTABLE_CAT** String =\> parent key table catalog (may be`null`)
2. **PKTABLE_SCHEM** String =\> parent key table schema (may be`null`)
3. **PKTABLE_NAME**String =\> parent key table name
4. **PKCOLUMN_NAME**String =\> parent key column name
5. **FKTABLE_CAT** String =\> foreign key table catalog (may be`null`) being exported (may be`null`)
6. **FKTABLE_SCHEM** String =\> foreign key table schema (may be`null`) being exported (may be`null`)
7. **FKTABLE_NAME**String =\> foreign key table name being exported
8. **FKCOLUMN_NAME**String =\> foreign key column name being exported
9. **KEY_SEQ**short =\> sequence number within foreign key( a value of 1 represents the first column of the foreign key, a value of 2 would represent the second column within the foreign key).
10. **UPDATE_RULE** short =\> What happens to foreign key when parent key is updated:
 - importedNoAction - do not allow update of parent key if it has been imported
 - importedKeyCascade - change imported key to agree with parent key update
 - importedKeySetNull - change imported key to`NULL`if its parent key has been updated
 - importedKeySetDefault - change imported key to default values if its parent key has been updated
 - importedKeyRestrict - same as importedKeyNoAction (for ODBC 2.x compatibility)
11. **DELETE_RULE** short =\> What happens to the foreign key when parent key is deleted.
 - importedKeyNoAction - do not allow delete of parent key if it has been imported
 - importedKeyCascade - delete rows that import a deleted key
 - importedKeySetNull - change imported key to`NULL`if its primary key has been deleted
 - importedKeyRestrict - same as importedKeyNoAction (for ODBC 2.x compatibility)
 - importedKeySetDefault - change imported key to default if its parent key has been deleted
12. **FK_NAME** String =\> foreign key name (may be`null`)
13. **PK_NAME** String =\> parent key name (may be`null`)
14. **DEFERRABILITY** short =\> can the evaluation of foreign key constraints be deferred until commit
 - importedKeyInitiallyDeferred - see SQL92 for definition
 - importedKeyInitiallyImmediate - see SQL92 for definition
 - importedKeyNotDeferrable - see SQL92 for definition

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parentCatalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in the database; "" retrieves those without a catalog;`null`means drop catalog name from the selection criteria |
| `parentSchema` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name; must match the schema name as it is stored in the database; "" retrieves those without a schema;`null`means drop schema name from the selection criteria |
| `parentTable` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the table that exports the key; must match the table name as it is stored in the database |
| --- | --- |
| `foreignCatalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in the database; "" retrieves those without a catalog;`null`means drop catalog name from the selection criteria |
| `foreignSchema` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name; must match the schema name as it is stored in the database; "" retrieves those without a schema;`null`means drop schema name from the selection criteria |
| `foreignTable` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the table that imports the key; must match the table name as it is stored in the database |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | `ResultSet`- each row is a foreign key column description |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getImportedKeys](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getImportedKeys(kotlin.String,%20kotlin.String,%20kotlin.String)) 

### getDatabaseMajorVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDatabaseMajorVersion(): Int
```

Retrieves the major version number of the underlying database.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the underlying database's major version |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getDatabaseMinorVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDatabaseMinorVersion(): Int
```

Retrieves the minor version number of the underlying database.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | underlying database's minor version |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getDatabaseProductName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDatabaseProductName(): String!
```

Retrieves the name of this database product.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | database product name |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getDatabaseProductVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDatabaseProductVersion(): String!
```

Retrieves the version number of this database product.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | database version number |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getDefaultTransactionIsolation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDefaultTransactionIsolation(): Int
```

Retrieves this database's default transaction isolation level. The possible values are defined in`java.sql.Connection`.

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the default isolation level |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [java.sql.Connection](https://developer.android.com/reference/kotlin/java/sql/Connection) 

### getDriverMajorVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDriverMajorVersion(): Int
```

Retrieves this JDBC driver's major version number.

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | JDBC driver major version |

### getDriverMinorVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDriverMinorVersion(): Int
```

Retrieves this JDBC driver's minor version number.

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | JDBC driver minor version number |

### getDriverName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDriverName(): String!
```

Retrieves the name of this JDBC driver.

| Return ||
|-----------------------------------------------------------------------------------|------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | JDBC driver name |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getDriverVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDriverVersion(): String!
```

Retrieves the version number of this JDBC driver as a`String`.

| Return ||
|-----------------------------------------------------------------------------------|---------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | JDBC driver version |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getExportedKeys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getExportedKeys(
    catalog: String!, 
    schema: String!, 
    table: String!
): ResultSet!
```

Retrieves a description of the foreign key columns that reference the given table's primary key columns (the foreign keys exported by a table). They are ordered by FKTABLE_CAT, FKTABLE_SCHEM, FKTABLE_NAME, and KEY_SEQ.

Each foreign key column description has the following columns:

1. **PKTABLE_CAT** String =\> primary key table catalog (may be`null`)
2. **PKTABLE_SCHEM** String =\> primary key table schema (may be`null`)
3. **PKTABLE_NAME**String =\> primary key table name
4. **PKCOLUMN_NAME**String =\> primary key column name
5. **FKTABLE_CAT** String =\> foreign key table catalog (may be`null`) being exported (may be`null`)
6. **FKTABLE_SCHEM** String =\> foreign key table schema (may be`null`) being exported (may be`null`)
7. **FKTABLE_NAME**String =\> foreign key table name being exported
8. **FKCOLUMN_NAME**String =\> foreign key column name being exported
9. **KEY_SEQ**short =\> sequence number within foreign key( a value of 1 represents the first column of the foreign key, a value of 2 would represent the second column within the foreign key).
10. **UPDATE_RULE** short =\> What happens to foreign key when primary is updated:
 - importedNoAction - do not allow update of primary key if it has been imported
 - importedKeyCascade - change imported key to agree with primary key update
 - importedKeySetNull - change imported key to`NULL`if its primary key has been updated
 - importedKeySetDefault - change imported key to default values if its primary key has been updated
 - importedKeyRestrict - same as importedKeyNoAction (for ODBC 2.x compatibility)
11. **DELETE_RULE** short =\> What happens to the foreign key when primary is deleted.
 - importedKeyNoAction - do not allow delete of primary key if it has been imported
 - importedKeyCascade - delete rows that import a deleted key
 - importedKeySetNull - change imported key to`NULL`if its primary key has been deleted
 - importedKeyRestrict - same as importedKeyNoAction (for ODBC 2.x compatibility)
 - importedKeySetDefault - change imported key to default if its primary key has been deleted
12. **FK_NAME** String =\> foreign key name (may be`null`)
13. **PK_NAME** String =\> primary key name (may be`null`)
14. **DEFERRABILITY** short =\> can the evaluation of foreign key constraints be deferred until commit
 - importedKeyInitiallyDeferred - see SQL92 for definition
 - importedKeyInitiallyImmediate - see SQL92 for definition
 - importedKeyNotDeferrable - see SQL92 for definition

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in this database; "" retrieves those without a catalog;`null`means that the catalog name should not be used to narrow the search |
| `schema` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name; must match the schema name as it is stored in the database; "" retrieves those without a schema;`null`means that the schema name should not be used to narrow the search |
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a table name; must match the table name as it is stored in this database |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | a`ResultSet`object in which each row is a foreign key column description |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getImportedKeys](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getImportedKeys(kotlin.String,%20kotlin.String,%20kotlin.String)) 

### getExtraNameCharacters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getExtraNameCharacters(): String!
```

Retrieves all the "extra" characters that can be used in unquoted identifier names (those beyond a-z, A-Z, 0-9 and _).

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the string containing the extra characters |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getFunctionColumns

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFunctionColumns(
    catalog: String!, 
    schemaPattern: String!, 
    functionNamePattern: String!, 
    columnNamePattern: String!
): ResultSet!
```

Retrieves a description of the given catalog's system or user function parameters and return type.

Only descriptions matching the schema, function and parameter name criteria are returned. They are ordered by`FUNCTION_CAT`,`FUNCTION_SCHEM`,`FUNCTION_NAME`and`SPECIFIC_ NAME`. Within this, the return value, if any, is first. Next are the parameter descriptions in call order. The column descriptions follow in column number order.

Each row in the`ResultSet`is a parameter description, column description or return type description with the following fields:

1. **FUNCTION_CAT** String =\> function catalog (may be`null`)
2. **FUNCTION_SCHEM** String =\> function schema (may be`null`)
3. **FUNCTION_NAME**String =\> function name. This is the name used to invoke the function
4. **COLUMN_NAME**String =\> column/parameter name
5. **COLUMN_TYPE** Short =\> kind of column/parameter:
 - functionColumnUnknown - nobody knows
 - functionColumnIn - IN parameter
 - functionColumnInOut - INOUT parameter
 - functionColumnOut - OUT parameter
 - functionColumnReturn - function return value
 - functionColumnResult - Indicates that the parameter or column is a column in the`ResultSet`
6. **DATA_TYPE**int =\> SQL type from java.sql.Types
7. **TYPE_NAME**String =\> SQL type name, for a UDT type the type name is fully qualified
8. **PRECISION**int =\> precision
9. **LENGTH**int =\> length in bytes of data
10. **SCALE**short =\> scale - null is returned for data types where SCALE is not applicable.
11. **RADIX**short =\> radix
12. **NULLABLE** short =\> can it contain NULL.
 - functionNoNulls - does not allow NULL values
 - functionNullable - allows NULL values
 - functionNullableUnknown - nullability unknown
13. **REMARKS**String =\> comment describing column/parameter
14. **CHAR_OCTET_LENGTH**int =\> the maximum length of binary and character based parameters or columns. For any other datatype the returned value is a NULL
15. **ORDINAL_POSITION**int =\> the ordinal position, starting from 1, for the input and output parameters. A value of 0 is returned if this row describes the function's return value. For result set columns, it is the ordinal position of the column in the result set starting from 1.
16. **IS_NULLABLE** String =\> ISO rules are used to determine the nullability for a parameter or column.
 - YES --- if the parameter or column can include NULLs
 - NO --- if the parameter or column cannot include NULLs
 - empty string --- if the nullability for the parameter or column is unknown
17. **SPECIFIC_NAME** String =\> the name which uniquely identifies this function within its schema. This is a user specified, or DBMS generated, name that may be different then the`FUNCTION_NAME`for example with overload functions

The PRECISION column represents the specified column size for the given parameter or column. For numeric data, this is the maximum precision. For character data, this is the length in characters. For datetime datatypes, this is the length in characters of the String representation (assuming the maximum allowed precision of the fractional seconds component). For binary data, this is the length in bytes. For the ROWID datatype, this is the length in bytes. Null is returned for data types where the column size is not applicable.

| Parameters ||
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in the database; "" retrieves those without a catalog;`null`means that the catalog name should not be used to narrow the search |
| `schemaPattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name pattern; must match the schema name as it is stored in the database; "" retrieves those without a schema;`null`means that the schema name should not be used to narrow the search |
| `functionNamePattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a procedure name pattern; must match the function name as it is stored in the database |
| --- | --- |
| `columnNamePattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a parameter name pattern; must match the parameter or column name as it is stored in the database |

| Return ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | `ResultSet`- each row describes a user function parameter, column or return type |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getSearchStringEscape](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSearchStringEscape()) 

### getFunctions

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFunctions(
    catalog: String!, 
    schemaPattern: String!, 
    functionNamePattern: String!
): ResultSet!
```

Retrieves a description of the system and user functions available in the given catalog.

Only system and user function descriptions matching the schema and function name criteria are returned. They are ordered by`FUNCTION_CAT`,`FUNCTION_SCHEM`,`FUNCTION_NAME`and`SPECIFIC_ NAME`.

Each function description has the the following columns:

1. **FUNCTION_CAT** String =\> function catalog (may be`null`)
2. **FUNCTION_SCHEM** String =\> function schema (may be`null`)
3. **FUNCTION_NAME**String =\> function name. This is the name used to invoke the function
4. **REMARKS**String =\> explanatory comment on the function
5. **FUNCTION_TYPE** short =\> kind of function:
 - functionResultUnknown - Cannot determine if a return value or table will be returned
 - functionNoTable- Does not return a table
 - functionReturnsTable - Returns a table
6. **SPECIFIC_NAME** String =\> the name which uniquely identifies this function within its schema. This is a user specified, or DBMS generated, name that may be different then the`FUNCTION_NAME`for example with overload functions

A user may not have permission to execute any of the functions that are returned by`getFunctions`

| Parameters ||
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in the database; "" retrieves those without a catalog;`null`means that the catalog name should not be used to narrow the search |
| `schemaPattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name pattern; must match the schema name as it is stored in the database; "" retrieves those without a schema;`null`means that the schema name should not be used to narrow the search |
| `functionNamePattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a function name pattern; must match the function name as it is stored in the database |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | `ResultSet`- each row is a function description |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getSearchStringEscape](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSearchStringEscape()) 

### getIdentifierQuoteString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getIdentifierQuoteString(): String!
```

Retrieves the string used to quote SQL identifiers. This method returns a space " " if identifier quoting is not supported.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the quoting string or a space if quoting is not supported |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getImportedKeys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getImportedKeys(
    catalog: String!, 
    schema: String!, 
    table: String!
): ResultSet!
```

Retrieves a description of the primary key columns that are referenced by the given table's foreign key columns (the primary keys imported by a table). They are ordered by PKTABLE_CAT, PKTABLE_SCHEM, PKTABLE_NAME, and KEY_SEQ.

Each primary key column description has the following columns:

1. **PKTABLE_CAT** String =\> primary key table catalog being imported (may be`null`)
2. **PKTABLE_SCHEM** String =\> primary key table schema being imported (may be`null`)
3. **PKTABLE_NAME**String =\> primary key table name being imported
4. **PKCOLUMN_NAME**String =\> primary key column name being imported
5. **FKTABLE_CAT** String =\> foreign key table catalog (may be`null`)
6. **FKTABLE_SCHEM** String =\> foreign key table schema (may be`null`)
7. **FKTABLE_NAME**String =\> foreign key table name
8. **FKCOLUMN_NAME**String =\> foreign key column name
9. **KEY_SEQ**short =\> sequence number within a foreign key( a value of 1 represents the first column of the foreign key, a value of 2 would represent the second column within the foreign key).
10. **UPDATE_RULE** short =\> What happens to a foreign key when the primary key is updated:
 - importedNoAction - do not allow update of primary key if it has been imported
 - importedKeyCascade - change imported key to agree with primary key update
 - importedKeySetNull - change imported key to`NULL`if its primary key has been updated
 - importedKeySetDefault - change imported key to default values if its primary key has been updated
 - importedKeyRestrict - same as importedKeyNoAction (for ODBC 2.x compatibility)
11. **DELETE_RULE** short =\> What happens to the foreign key when primary is deleted.
 - importedKeyNoAction - do not allow delete of primary key if it has been imported
 - importedKeyCascade - delete rows that import a deleted key
 - importedKeySetNull - change imported key to NULL if its primary key has been deleted
 - importedKeyRestrict - same as importedKeyNoAction (for ODBC 2.x compatibility)
 - importedKeySetDefault - change imported key to default if its primary key has been deleted
12. **FK_NAME** String =\> foreign key name (may be`null`)
13. **PK_NAME** String =\> primary key name (may be`null`)
14. **DEFERRABILITY** short =\> can the evaluation of foreign key constraints be deferred until commit
 - importedKeyInitiallyDeferred - see SQL92 for definition
 - importedKeyInitiallyImmediate - see SQL92 for definition
 - importedKeyNotDeferrable - see SQL92 for definition

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in the database; "" retrieves those without a catalog;`null`means that the catalog name should not be used to narrow the search |
| `schema` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name; must match the schema name as it is stored in the database; "" retrieves those without a schema;`null`means that the schema name should not be used to narrow the search |
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a table name; must match the table name as it is stored in the database |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | `ResultSet`- each row is a primary key column description |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getExportedKeys](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getExportedKeys(kotlin.String,%20kotlin.String,%20kotlin.String)) 

### getIndexInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getIndexInfo(
    catalog: String!, 
    schema: String!, 
    table: String!, 
    unique: Boolean, 
    approximate: Boolean
): ResultSet!
```

Retrieves a description of the given table's indices and statistics. They are ordered by NON_UNIQUE, TYPE, INDEX_NAME, and ORDINAL_POSITION.

Each index column description has the following columns:

1. **TABLE_CAT** String =\> table catalog (may be`null`)
2. **TABLE_SCHEM** String =\> table schema (may be`null`)
3. **TABLE_NAME**String =\> table name
4. **NON_UNIQUE**boolean =\> Can index values be non-unique. false when TYPE is tableIndexStatistic
5. **INDEX_QUALIFIER** String =\> index catalog (may be`null`);`null`when TYPE is tableIndexStatistic
6. **INDEX_NAME** String =\> index name;`null`when TYPE is tableIndexStatistic
7. **TYPE** short =\> index type:
 - tableIndexStatistic - this identifies table statistics that are returned in conjuction with a table's index descriptions
 - tableIndexClustered - this is a clustered index
 - tableIndexHashed - this is a hashed index
 - tableIndexOther - this is some other style of index
8. **ORDINAL_POSITION**short =\> column sequence number within index; zero when TYPE is tableIndexStatistic
9. **COLUMN_NAME** String =\> column name;`null`when TYPE is tableIndexStatistic
10. **ASC_OR_DESC** String =\> column sort sequence, "A" =\> ascending, "D" =\> descending, may be`null`if sort sequence is not supported;`null`when TYPE is tableIndexStatistic
11. **CARDINALITY**int =\> When TYPE is tableIndexStatistic, then this is the number of rows in the table; otherwise, it is the number of unique values in the index.
12. **PAGES**int =\> When TYPE is tableIndexStatisic then this is the number of pages used for the table, otherwise it is the number of pages used for the current index.
13. **FILTER_CONDITION** String =\> Filter condition, if any. (may be`null`)

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in this database; "" retrieves those without a catalog;`null`means that the catalog name should not be used to narrow the search |
| `schema` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name; must match the schema name as it is stored in this database; "" retrieves those without a schema;`null`means that the schema name should not be used to narrow the search |
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a table name; must match the table name as it is stored in this database |
| --- | --- |
| `unique` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):when true, return only indices for unique values; when false, return indices regardless of whether unique or not |
| `approximate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):when true, result is allowed to reflect approximate or out of data values; when false, results are requested to be accurate |

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | `ResultSet`- each row is an index column description |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getJDBCMajorVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getJDBCMajorVersion(): Int
```

Retrieves the major JDBC version number for this driver.

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | JDBC version major number |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getJDBCMinorVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getJDBCMinorVersion(): Int
```

Retrieves the minor JDBC version number for this driver.

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | JDBC version minor number |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxBinaryLiteralLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxBinaryLiteralLength(): Int
```

Retrieves the maximum number of hex characters this database allows in an inline binary literal.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | max the maximum length (in hex characters) for a binary literal; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxCatalogNameLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxCatalogNameLength(): Int
```

Retrieves the maximum number of characters that this database allows in a catalog name.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of characters allowed in a catalog name; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxCharLiteralLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxCharLiteralLength(): Int
```

Retrieves the maximum number of characters this database allows for a character literal.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of characters allowed for a character literal; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxColumnNameLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxColumnNameLength(): Int
```

Retrieves the maximum number of characters this database allows for a column name.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of characters allowed for a column name; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxColumnsInGroupBy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxColumnsInGroupBy(): Int
```

Retrieves the maximum number of columns this database allows in a`GROUP BY`clause.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of columns allowed; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxColumnsInIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxColumnsInIndex(): Int
```

Retrieves the maximum number of columns this database allows in an index.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of columns allowed; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxColumnsInOrderBy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxColumnsInOrderBy(): Int
```

Retrieves the maximum number of columns this database allows in an`ORDER BY`clause.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of columns allowed; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxColumnsInSelect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxColumnsInSelect(): Int
```

Retrieves the maximum number of columns this database allows in a`SELECT`list.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of columns allowed; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxColumnsInTable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxColumnsInTable(): Int
```

Retrieves the maximum number of columns this database allows in a table.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of columns allowed; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxConnections

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxConnections(): Int
```

Retrieves the maximum number of concurrent connections to this database that are possible.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of active connections possible at one time; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxCursorNameLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxCursorNameLength(): Int
```

Retrieves the maximum number of characters that this database allows in a cursor name.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of characters allowed in a cursor name; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxIndexLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxIndexLength(): Int
```

Retrieves the maximum number of bytes this database allows for an index, including all of the parts of the index.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of bytes allowed; this limit includes the composite of all the constituent parts of the index; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxProcedureNameLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxProcedureNameLength(): Int
```

Retrieves the maximum number of characters that this database allows in a procedure name.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of characters allowed in a procedure name; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxRowSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxRowSize(): Int
```

Retrieves the maximum number of bytes this database allows in a single row.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of bytes allowed for a row; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxSchemaNameLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxSchemaNameLength(): Int
```

Retrieves the maximum number of characters that this database allows in a schema name.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of characters allowed in a schema name; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxStatementLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxStatementLength(): Int
```

Retrieves the maximum number of characters this database allows in an SQL statement.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of characters allowed for an SQL statement; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxStatements

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxStatements(): Int
```

Retrieves the maximum number of active statements to this database that can be open at the same time.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of statements that can be open at one time; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxTableNameLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxTableNameLength(): Int
```

Retrieves the maximum number of characters this database allows in a table name.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of characters allowed for a table name; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxTablesInSelect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxTablesInSelect(): Int
```

Retrieves the maximum number of tables this database allows in a`SELECT`statement.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of tables allowed in a`SELECT`statement; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getMaxUserNameLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxUserNameLength(): Int
```

Retrieves the maximum number of characters this database allows in a user name.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of characters allowed for a user name; a result of zero means that there is no limit or the limit is not known |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getNumericFunctions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNumericFunctions(): String!
```

Retrieves a comma-separated list of math functions available with this database. These are the Open /Open CLI math function names used in the JDBC function escape clause.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the list of math functions supported by this database |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getPrimaryKeys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrimaryKeys(
    catalog: String!, 
    schema: String!, 
    table: String!
): ResultSet!
```

Retrieves a description of the given table's primary key columns. They are ordered by COLUMN_NAME.

Each primary key column description has the following columns:

1. **TABLE_CAT** String =\> table catalog (may be`null`)
2. **TABLE_SCHEM** String =\> table schema (may be`null`)
3. **TABLE_NAME**String =\> table name
4. **COLUMN_NAME**String =\> column name
5. **KEY_SEQ**short =\> sequence number within primary key( a value of 1 represents the first column of the primary key, a value of 2 would represent the second column within the primary key).
6. **PK_NAME** String =\> primary key name (may be`null`)

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in the database; "" retrieves those without a catalog;`null`means that the catalog name should not be used to narrow the search |
| `schema` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name; must match the schema name as it is stored in the database; "" retrieves those without a schema;`null`means that the schema name should not be used to narrow the search |
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a table name; must match the table name as it is stored in the database |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | `ResultSet`- each row is a primary key column description |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getProcedureColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getProcedureColumns(
    catalog: String!, 
    schemaPattern: String!, 
    procedureNamePattern: String!, 
    columnNamePattern: String!
): ResultSet!
```

Retrieves a description of the given catalog's stored procedure parameter and result columns.

Only descriptions matching the schema, procedure and parameter name criteria are returned. They are ordered by PROCEDURE_CAT, PROCEDURE_SCHEM, PROCEDURE_NAME and SPECIFIC_NAME. Within this, the return value, if any, is first. Next are the parameter descriptions in call order. The column descriptions follow in column number order.

Each row in the`ResultSet`is a parameter description or column description with the following fields:

1. **PROCEDURE_CAT** String =\> procedure catalog (may be`null`)
2. **PROCEDURE_SCHEM** String =\> procedure schema (may be`null`)
3. **PROCEDURE_NAME**String =\> procedure name
4. **COLUMN_NAME**String =\> column/parameter name
5. **COLUMN_TYPE** Short =\> kind of column/parameter:
 - procedureColumnUnknown - nobody knows
 - procedureColumnIn - IN parameter
 - procedureColumnInOut - INOUT parameter
 - procedureColumnOut - OUT parameter
 - procedureColumnReturn - procedure return value
 - procedureColumnResult - result column in`ResultSet`
6. **DATA_TYPE**int =\> SQL type from java.sql.Types
7. **TYPE_NAME**String =\> SQL type name, for a UDT type the type name is fully qualified
8. **PRECISION**int =\> precision
9. **LENGTH**int =\> length in bytes of data
10. **SCALE**short =\> scale - null is returned for data types where SCALE is not applicable.
11. **RADIX**short =\> radix
12. **NULLABLE** short =\> can it contain NULL.
 - procedureNoNulls - does not allow NULL values
 - procedureNullable - allows NULL values
 - procedureNullableUnknown - nullability unknown
13. **REMARKS**String =\> comment describing parameter/column
14. **COLUMN_DEF** String =\> default value for the column, which should be interpreted as a string when the value is enclosed in single quotes (may be`null`)
 - The string NULL (not enclosed in quotes) - if NULL was specified as the default value
 - TRUNCATE (not enclosed in quotes) - if the specified default value cannot be represented without truncation
 - NULL - if a default value was not specified
15. **SQL_DATA_TYPE**int =\> reserved for future use
16. **SQL_DATETIME_SUB**int =\> reserved for future use
17. **CHAR_OCTET_LENGTH**int =\> the maximum length of binary and character based columns. For any other datatype the returned value is a NULL
18. **ORDINAL_POSITION**int =\> the ordinal position, starting from 1, for the input and output parameters for a procedure. A value of 0 is returned if this row describes the procedure's return value. For result set columns, it is the ordinal position of the column in the result set starting from 1. If there are multiple result sets, the column ordinal positions are implementation defined.
19. **IS_NULLABLE** String =\> ISO rules are used to determine the nullability for a column.
 - YES --- if the column can include NULLs
 - NO --- if the column cannot include NULLs
 - empty string --- if the nullability for the column is unknown
20. **SPECIFIC_NAME**String =\> the name which uniquely identifies this procedure within its schema.

**Note:**Some databases may not return the column descriptions for a procedure.

The PRECISION column represents the specified column size for the given column. For numeric data, this is the maximum precision. For character data, this is the length in characters. For datetime datatypes, this is the length in characters of the String representation (assuming the maximum allowed precision of the fractional seconds component). For binary data, this is the length in bytes. For the ROWID datatype, this is the length in bytes. Null is returned for data types where the column size is not applicable.

| Parameters ||
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in the database; "" retrieves those without a catalog;`null`means that the catalog name should not be used to narrow the search |
| `schemaPattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name pattern; must match the schema name as it is stored in the database; "" retrieves those without a schema;`null`means that the schema name should not be used to narrow the search |
| `procedureNamePattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a procedure name pattern; must match the procedure name as it is stored in the database |
| --- | --- |
| `columnNamePattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a column name pattern; must match the column name as it is stored in the database |

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | `ResultSet`- each row describes a stored procedure parameter or column |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getSearchStringEscape](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSearchStringEscape()) 

### getProcedureTerm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getProcedureTerm(): String!
```

Retrieves the database vendor's preferred term for "procedure".

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the vendor term for "procedure" |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getProcedures

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getProcedures(
    catalog: String!, 
    schemaPattern: String!, 
    procedureNamePattern: String!
): ResultSet!
```

Retrieves a description of the stored procedures available in the given catalog.

Only procedure descriptions matching the schema and procedure name criteria are returned. They are ordered by`PROCEDURE_CAT`,`PROCEDURE_SCHEM`,`PROCEDURE_NAME`and`SPECIFIC_ NAME`.

Each procedure description has the the following columns:

1. **PROCEDURE_CAT** String =\> procedure catalog (may be`null`)
2. **PROCEDURE_SCHEM** String =\> procedure schema (may be`null`)
3. **PROCEDURE_NAME**String =\> procedure name
4. reserved for future use
5. reserved for future use
6. reserved for future use
7. **REMARKS**String =\> explanatory comment on the procedure
8. **PROCEDURE_TYPE** short =\> kind of procedure:
 - procedureResultUnknown - Cannot determine if a return value will be returned
 - procedureNoResult - Does not return a return value
 - procedureReturnsResult - Returns a return value
9. **SPECIFIC_NAME**String =\> The name which uniquely identifies this procedure within its schema.

A user may not have permissions to execute any of the procedures that are returned by`getProcedures`

| Parameters ||
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in the database; "" retrieves those without a catalog;`null`means that the catalog name should not be used to narrow the search |
| `schemaPattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name pattern; must match the schema name as it is stored in the database; "" retrieves those without a schema;`null`means that the schema name should not be used to narrow the search |
| `procedureNamePattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a procedure name pattern; must match the procedure name as it is stored in the database |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | `ResultSet`- each row is a procedure description |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getSearchStringEscape](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSearchStringEscape()) 

### getResultSetHoldability

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getResultSetHoldability(): Int
```

Retrieves this database's default holdability for`ResultSet`objects.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the default holdability; either`ResultSet.HOLD_CURSORS_OVER_COMMIT`or`ResultSet.CLOSE_CURSORS_AT_COMMIT` |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getRowIdLifetime

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRowIdLifetime(): RowIdLifetime!
```

Indicates whether or not this data source supports the SQL`ROWID`type, and if so the lifetime for which a`RowId`object remains valid.

The returned int values have the following relationship: 

```kotlin
ROWID_UNSUPPORTED < ROWID_VALID_OTHER < ROWID_VALID_TRANSACTION
          < ROWID_VALID_SESSION < ROWID_VALID_FOREVER
  
```
so conditional logic such as 

```kotlin
if (metadata.getRowIdLifetime() > DatabaseMetaData.ROWID_VALID_TRANSACTION)
  
```
can be used. Valid Forever means valid across all Sessions, and valid for a Session means valid across all its contained Transactions.

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------|
| [RowIdLifetime](https://developer.android.com/reference/kotlin/java/sql/RowIdLifetime)! | the status indicating the lifetime of a`RowId` |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getSQLKeywords

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSQLKeywords(): String!
```

Retrieves a comma-separated list of all of this database's SQL keywords that are NOT also SQL:2003 keywords.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the list of this database's keywords that are not also SQL:2003 keywords |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getSQLStateType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSQLStateType(): Int
```

Indicates whether the SQLSTATE returned by`SQLException.getSQLState`is X/Open (now known as Open Group) SQL CLI or SQL:2003.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the type of SQLSTATE; one of: sqlStateXOpen or sqlStateSQL |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getSchemaTerm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSchemaTerm(): String!
```

Retrieves the database vendor's preferred term for "schema".

| Return ||
|-----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the vendor term for "schema" |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getSchemas

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSchemas(): ResultSet!
```

Retrieves the schema names available in this database. The results are ordered by`TABLE_CATALOG`and`TABLE_SCHEM`.

The schema columns are:

1. **TABLE_SCHEM**String =\> schema name
2. **TABLE_CATALOG** String =\> catalog name (may be`null`)

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | a`ResultSet`object in which each row is a schema description |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getSchemas

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSchemas(
    catalog: String!, 
    schemaPattern: String!
): ResultSet!
```

Retrieves the schema names available in this database. The results are ordered by`TABLE_CATALOG`and`TABLE_SCHEM`.

The schema columns are:

1. **TABLE_SCHEM**String =\> schema name
2. **TABLE_CATALOG** String =\> catalog name (may be`null`)

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in the database;"" retrieves those without a catalog; null means catalog name should not be used to narrow down the search. |
| `schemaPattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name; must match the schema name as it is stored in the database; null means schema name should not be used to narrow down the search. |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | a`ResultSet`object in which each row is a schema description |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getSearchStringEscape](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSearchStringEscape()) 

### getSearchStringEscape

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSearchStringEscape(): String!
```

Retrieves the string that can be used to escape wildcard characters. This is the string that can be used to escape '_' or '%' in the catalog search parameters that are a pattern (and therefore use one of the wildcard characters).

The '_' character represents any single character; the '%' character represents any sequence of zero or more characters.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the string used to escape wildcard characters |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getStringFunctions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getStringFunctions(): String!
```

Retrieves a comma-separated list of string functions available with this database. These are the Open Group CLI string function names used in the JDBC function escape clause.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the list of string functions supported by this database |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getSuperTables

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSuperTables(
    catalog: String!, 
    schemaPattern: String!, 
    tableNamePattern: String!
): ResultSet!
```

Retrieves a description of the table hierarchies defined in a particular schema in this database.

Only supertable information for tables matching the catalog, schema and table name are returned. The table name parameter may be a fully- qualified name, in which case, the catalog and schemaPattern parameters are ignored. If a table does not have a super table, it is not listed here. Supertables have to be defined in the same catalog and schema as the sub tables. Therefore, the type description does not need to include this information for the supertable.

Each type description has the following columns:

1. **TABLE_CAT** String =\> the type's catalog (may be`null`)
2. **TABLE_SCHEM** String =\> type's schema (may be`null`)
3. **TABLE_NAME**String =\> type name
4. **SUPERTABLE_NAME**String =\> the direct super type's name

**Note:**If the driver does not support type hierarchies, an empty result set is returned.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; "" retrieves those without a catalog;`null`means drop catalog name from the selection criteria |
| `schemaPattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name pattern; "" retrieves those without a schema |
| `tableNamePattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a table name pattern; may be a fully-qualified name |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | a`ResultSet`object in which each row is a type description |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getSearchStringEscape](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSearchStringEscape()) 

### getSuperTypes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSuperTypes(
    catalog: String!, 
    schemaPattern: String!, 
    typeNamePattern: String!
): ResultSet!
```

Retrieves a description of the user-defined type (UDT) hierarchies defined in a particular schema in this database. Only the immediate super type/ sub type relationship is modeled.

Only supertype information for UDTs matching the catalog, schema, and type name is returned. The type name parameter may be a fully-qualified name. When the UDT name supplied is a fully-qualified name, the catalog and schemaPattern parameters are ignored.

If a UDT does not have a direct super type, it is not listed here. A row of the`ResultSet`object returned by this method describes the designated UDT and a direct supertype. A row has the following columns:

1. **TYPE_CAT** String =\> the UDT's catalog (may be`null`)
2. **TYPE_SCHEM** String =\> UDT's schema (may be`null`)
3. **TYPE_NAME**String =\> type name of the UDT
4. **SUPERTYPE_CAT** String =\> the direct super type's catalog (may be`null`)
5. **SUPERTYPE_SCHEM** String =\> the direct super type's schema (may be`null`)
6. **SUPERTYPE_NAME**String =\> the direct super type's name

**Note:**If the driver does not support type hierarchies, an empty result set is returned.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; "" retrieves those without a catalog;`null`means drop catalog name from the selection criteria |
| `schemaPattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name pattern; "" retrieves those without a schema |
| `typeNamePattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a UDT name pattern; may be a fully-qualified name |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | a`ResultSet`object in which a row gives information about the designated UDT |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getSearchStringEscape](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSearchStringEscape()) 

### getSystemFunctions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSystemFunctions(): String!
```

Retrieves a comma-separated list of system functions available with this database. These are the Open Group CLI system function names used in the JDBC function escape clause.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a list of system functions supported by this database |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getTablePrivileges

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTablePrivileges(
    catalog: String!, 
    schemaPattern: String!, 
    tableNamePattern: String!
): ResultSet!
```

Retrieves a description of the access rights for each table available in a catalog. Note that a table privilege applies to one or more columns in the table. It would be wrong to assume that this privilege applies to all columns (this may be true for some systems but is not true for all.)

Only privileges matching the schema and table name criteria are returned. They are ordered by`TABLE_CAT`,`TABLE_SCHEM`,`TABLE_NAME`, and`PRIVILEGE`.

Each privilige description has the following columns:

1. **TABLE_CAT** String =\> table catalog (may be`null`)
2. **TABLE_SCHEM** String =\> table schema (may be`null`)
3. **TABLE_NAME**String =\> table name
4. **GRANTOR** String =\> grantor of access (may be`null`)
5. **GRANTEE**String =\> grantee of access
6. **PRIVILEGE**String =\> name of access (SELECT, INSERT, UPDATE, REFRENCES, ...)
7. **IS_GRANTABLE** String =\> "YES" if grantee is permitted to grant to others; "NO" if not;`null`if unknown

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in the database; "" retrieves those without a catalog;`null`means that the catalog name should not be used to narrow the search |
| `schemaPattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name pattern; must match the schema name as it is stored in the database; "" retrieves those without a schema;`null`means that the schema name should not be used to narrow the search |
| `tableNamePattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a table name pattern; must match the table name as it is stored in the database |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | `ResultSet`- each row is a table privilege description |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getSearchStringEscape](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSearchStringEscape()) 

### getTableTypes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTableTypes(): ResultSet!
```

Retrieves the table types available in this database. The results are ordered by table type.

The table type is:

1. **TABLE_TYPE**String =\> table type. Typical types are "TABLE", "VIEW", "SYSTEM TABLE", "GLOBAL TEMPORARY", "LOCAL TEMPORARY", "ALIAS", "SYNONYM".

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | a`ResultSet`object in which each row has a single`String`column that is a table type |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getTables

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTables(
    catalog: String!, 
    schemaPattern: String!, 
    tableNamePattern: String!, 
    types: Array<String!>!
): ResultSet!
```

Retrieves a description of the tables available in the given catalog. Only table descriptions matching the catalog, schema, table name and type criteria are returned. They are ordered by`TABLE_TYPE`,`TABLE_CAT`,`TABLE_SCHEM`and`TABLE_NAME`.

Each table description has the following columns:

1. **TABLE_CAT** String =\> table catalog (may be`null`)
2. **TABLE_SCHEM** String =\> table schema (may be`null`)
3. **TABLE_NAME**String =\> table name
4. **TABLE_TYPE**String =\> table type. Typical types are "TABLE", "VIEW", "SYSTEM TABLE", "GLOBAL TEMPORARY", "LOCAL TEMPORARY", "ALIAS", "SYNONYM".
5. **REMARKS**String =\> explanatory comment on the table
6. **TYPE_CAT** String =\> the types catalog (may be`null`)
7. **TYPE_SCHEM** String =\> the types schema (may be`null`)
8. **TYPE_NAME** String =\> type name (may be`null`)
9. **SELF_REFERENCING_COL_NAME** String =\> name of the designated "identifier" column of a typed table (may be`null`)
10. **REF_GENERATION** String =\> specifies how values in SELF_REFERENCING_COL_NAME are created. Values are "SYSTEM", "USER", "DERIVED". (may be`null`)

**Note:**Some databases may not return information for all tables.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in the database; "" retrieves those without a catalog;`null`means that the catalog name should not be used to narrow the search |
| `schemaPattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name pattern; must match the schema name as it is stored in the database; "" retrieves those without a schema;`null`means that the schema name should not be used to narrow the search |
| `tableNamePattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a table name pattern; must match the table name as it is stored in the database |
| --- | --- |
| `types` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:a list of table types, which must be from the list of table types returned from [getTableTypes](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getTableTypes()),to include;`null`returns all types |

| Return ||
|---------------------------------------------------------------------------------|----------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | `ResultSet`- each row is a table description |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getSearchStringEscape](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSearchStringEscape()) 

### getTimeDateFunctions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTimeDateFunctions(): String!
```

Retrieves a comma-separated list of the time and date functions available with this database.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the list of time and date functions supported by this database |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getTypeInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTypeInfo(): ResultSet!
```

Retrieves a description of all the data types supported by this database. They are ordered by DATA_TYPE and then by how closely the data type maps to the corresponding JDBC SQL type.

If the database supports SQL distinct types, then getTypeInfo() will return a single row with a TYPE_NAME of DISTINCT and a DATA_TYPE of Types.DISTINCT. If the database supports SQL structured types, then getTypeInfo() will return a single row with a TYPE_NAME of STRUCT and a DATA_TYPE of Types.STRUCT.

If SQL distinct or structured types are supported, then information on the individual types may be obtained from the getUDTs() method.

Each type description has the following columns:

1. **TYPE_NAME**String =\> Type name
2. **DATA_TYPE**int =\> SQL data type from java.sql.Types
3. **PRECISION**int =\> maximum precision
4. **LITERAL_PREFIX** String =\> prefix used to quote a literal (may be`null`)
5. **LITERAL_SUFFIX** String =\> suffix used to quote a literal (may be`null`)
6. **CREATE_PARAMS** String =\> parameters used in creating the type (may be`null`)
7. **NULLABLE** short =\> can you use NULL for this type.
 - typeNoNulls - does not allow NULL values
 - typeNullable - allows NULL values
 - typeNullableUnknown - nullability unknown
8. **CASE_SENSITIVE**boolean=\> is it case sensitive.
9. **SEARCHABLE** short =\> can you use "WHERE" based on this type:
 - typePredNone - No support
 - typePredChar - Only supported with WHERE .. LIKE
 - typePredBasic - Supported except for WHERE .. LIKE
 - typeSearchable - Supported for all WHERE ..
10. **UNSIGNED_ATTRIBUTE**boolean =\> is it unsigned.
11. **FIXED_PREC_SCALE**boolean =\> can it be a money value.
12. **AUTO_INCREMENT**boolean =\> can it be used for an auto-increment value.
13. **LOCAL_TYPE_NAME** String =\> localized version of type name (may be`null`)
14. **MINIMUM_SCALE**short =\> minimum scale supported
15. **MAXIMUM_SCALE**short =\> maximum scale supported
16. **SQL_DATA_TYPE**int =\> unused
17. **SQL_DATETIME_SUB**int =\> unused
18. **NUM_PREC_RADIX**int =\> usually 2 or 10

The PRECISION column represents the maximum column size that the server supports for the given datatype. For numeric data, this is the maximum precision. For character data, this is the length in characters. For datetime datatypes, this is the length in characters of the String representation (assuming the maximum allowed precision of the fractional seconds component). For binary data, this is the length in bytes. For the ROWID datatype, this is the length in bytes. Null is returned for data types where the column size is not applicable.

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | a`ResultSet`object in which each row is an SQL type description |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getUDTs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUDTs(
    catalog: String!, 
    schemaPattern: String!, 
    typeNamePattern: String!, 
    types: IntArray!
): ResultSet!
```

Retrieves a description of the user-defined types (UDTs) defined in a particular schema. Schema-specific UDTs may have type`JAVA_OBJECT`,`STRUCT`, or`DISTINCT`.

Only types matching the catalog, schema, type name and type criteria are returned. They are ordered by`DATA_TYPE`,`TYPE_CAT`,`TYPE_SCHEM`and`TYPE_NAME`. The type name parameter may be a fully-qualified name. In this case, the catalog and schemaPattern parameters are ignored.

Each type description has the following columns:

1. **TYPE_CAT** String =\> the type's catalog (may be`null`)
2. **TYPE_SCHEM** String =\> type's schema (may be`null`)
3. **TYPE_NAME**String =\> type name
4. **CLASS_NAME**String =\> Java class name
5. **DATA_TYPE**int =\> type value defined in java.sql.Types. One of JAVA_OBJECT, STRUCT, or DISTINCT
6. **REMARKS**String =\> explanatory comment on the type
7. **BASE_TYPE** short =\> type code of the source type of a DISTINCT type or the type that implements the user-generated reference type of the SELF_REFERENCING_COLUMN of a structured type as defined in java.sql.Types (`null`if DATA_TYPE is not DISTINCT or not STRUCT with REFERENCE_GENERATION = USER_DEFINED)

**Note:**If the driver does not support UDTs, an empty result set is returned.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in the database; "" retrieves those without a catalog;`null`means that the catalog name should not be used to narrow the search |
| `schemaPattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema pattern name; must match the schema name as it is stored in the database; "" retrieves those without a schema;`null`means that the schema name should not be used to narrow the search |
| `typeNamePattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a type name pattern; must match the type name as it is stored in the database; may be a fully qualified name |
| --- | --- |
| `types` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:a list of user-defined types (JAVA_OBJECT, STRUCT, or DISTINCT) to include;`null`returns all types |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | `ResultSet`object in which each row describes a UDT |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getSearchStringEscape](https://developer.android.com/reference/kotlin/java/sql/DatabaseMetaData#getSearchStringEscape()) 

### getURL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getURL(): String!
```

Retrieves the URL for this DBMS.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the URL for this DBMS or`null`if it cannot be generated |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getUserName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUserName(): String!
```

Retrieves the user name as known to this database.

| Return ||
|-----------------------------------------------------------------------------------|------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the database user name |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getVersionColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getVersionColumns(
    catalog: String!, 
    schema: String!, 
    table: String!
): ResultSet!
```

Retrieves a description of a table's columns that are automatically updated when any value in a row is updated. They are unordered.

Each column description has the following columns:

1. **SCOPE**short =\> is not used
2. **COLUMN_NAME**String =\> column name
3. **DATA_TYPE** int =\> SQL data type from`java.sql.Types`
4. **TYPE_NAME**String =\> Data source-dependent type name
5. **COLUMN_SIZE**int =\> precision
6. **BUFFER_LENGTH**int =\> length of column value in bytes
7. **DECIMAL_DIGITS**short =\> scale - Null is returned for data types where DECIMAL_DIGITS is not applicable.
8. **PSEUDO_COLUMN** short =\> whether this is pseudo column like an Oracle ROWID
 - versionColumnUnknown - may or may not be pseudo column
 - versionColumnNotPseudo - is NOT a pseudo column
 - versionColumnPseudo - is a pseudo column

The COLUMN_SIZE column represents the specified column size for the given column. For numeric data, this is the maximum precision. For character data, this is the length in characters. For datetime datatypes, this is the length in characters of the String representation (assuming the maximum allowed precision of the fractional seconds component). For binary data, this is the length in bytes. For the ROWID datatype, this is the length in bytes. Null is returned for data types where the column size is not applicable.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a catalog name; must match the catalog name as it is stored in the database; "" retrieves those without a catalog;`null`means that the catalog name should not be used to narrow the search |
| `schema` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a schema name; must match the schema name as it is stored in the database; "" retrieves those without a schema;`null`means that the schema name should not be used to narrow the search |
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a table name; must match the table name as it is stored in the database |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | a`ResultSet`object in which each row is a column description |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### insertsAreDetected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun insertsAreDetected(type: Int): Boolean
```

Retrieves whether or not a visible row insert can be detected by calling the method`ResultSet.rowInserted`.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the`ResultSet`type; one of`ResultSet.TYPE_FORWARD_ONLY`,`ResultSet.TYPE_SCROLL_INSENSITIVE`, or`ResultSet.TYPE_SCROLL_SENSITIVE` |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if changes are detected by the specified result set type;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### isCatalogAtStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isCatalogAtStart(): Boolean
```

Retrieves whether a catalog appears at the start of a fully qualified table name. If not, the catalog appears at the end.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the catalog name appears at the beginning of a fully qualified table name;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### isReadOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isReadOnly(): Boolean
```

Retrieves whether this database is in read-only mode.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### locatorsUpdateCopy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun locatorsUpdateCopy(): Boolean
```

Indicates whether updates made to a LOB are made on a copy or directly to the LOB.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if updates are made to a copy of the LOB;`false`if updates are made directly to the LOB |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### nullPlusNonNullIsNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun nullPlusNonNullIsNull(): Boolean
```

Retrieves whether this database supports concatenations between`NULL`and non-`NULL`values being`NULL`.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### nullsAreSortedAtEnd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun nullsAreSortedAtEnd(): Boolean
```

Retrieves whether`NULL`values are sorted at the end regardless of sort order.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### nullsAreSortedAtStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun nullsAreSortedAtStart(): Boolean
```

Retrieves whether`NULL`values are sorted at the start regardless of sort order.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### nullsAreSortedHigh

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun nullsAreSortedHigh(): Boolean
```

Retrieves whether`NULL`values are sorted high. Sorted high means that`NULL`values sort higher than any other value in a domain. In an ascending order, if this method returns`true`,`NULL`values will appear at the end. By contrast, the method`nullsAreSortedAtEnd`indicates whether`NULL`values are sorted at the end regardless of sort order.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### nullsAreSortedLow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun nullsAreSortedLow(): Boolean
```

Retrieves whether`NULL`values are sorted low. Sorted low means that`NULL`values sort lower than any other value in a domain. In an ascending order, if this method returns`true`,`NULL`values will appear at the beginning. By contrast, the method`nullsAreSortedAtStart`indicates whether`NULL`values are sorted at the beginning regardless of sort order.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### othersDeletesAreVisible

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun othersDeletesAreVisible(type: Int): Boolean
```

Retrieves whether deletes made by others are visible.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the`ResultSet`type; one of`ResultSet.TYPE_FORWARD_ONLY`,`ResultSet.TYPE_SCROLL_INSENSITIVE`, or`ResultSet.TYPE_SCROLL_SENSITIVE` |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if deletes made by others are visible for the given result set type;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### othersInsertsAreVisible

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun othersInsertsAreVisible(type: Int): Boolean
```

Retrieves whether inserts made by others are visible.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the`ResultSet`type; one of`ResultSet.TYPE_FORWARD_ONLY`,`ResultSet.TYPE_SCROLL_INSENSITIVE`, or`ResultSet.TYPE_SCROLL_SENSITIVE` |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if inserts made by others are visible for the given result set type;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### othersUpdatesAreVisible

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun othersUpdatesAreVisible(type: Int): Boolean
```

Retrieves whether updates made by others are visible.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the`ResultSet`type; one of`ResultSet.TYPE_FORWARD_ONLY`,`ResultSet.TYPE_SCROLL_INSENSITIVE`, or`ResultSet.TYPE_SCROLL_SENSITIVE` |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if updates made by others are visible for the given result set type;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### ownDeletesAreVisible

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun ownDeletesAreVisible(type: Int): Boolean
```

Retrieves whether a result set's own deletes are visible.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the`ResultSet`type; one of`ResultSet.TYPE_FORWARD_ONLY`,`ResultSet.TYPE_SCROLL_INSENSITIVE`, or`ResultSet.TYPE_SCROLL_SENSITIVE` |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if deletes are visible for the given result set type;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### ownInsertsAreVisible

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun ownInsertsAreVisible(type: Int): Boolean
```

Retrieves whether a result set's own inserts are visible.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the`ResultSet`type; one of`ResultSet.TYPE_FORWARD_ONLY`,`ResultSet.TYPE_SCROLL_INSENSITIVE`, or`ResultSet.TYPE_SCROLL_SENSITIVE` |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if inserts are visible for the given result set type;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### ownUpdatesAreVisible

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun ownUpdatesAreVisible(type: Int): Boolean
```

Retrieves whether for the given type of`ResultSet`object, the result set's own updates are visible.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the`ResultSet`type; one of`ResultSet.TYPE_FORWARD_ONLY`,`ResultSet.TYPE_SCROLL_INSENSITIVE`, or`ResultSet.TYPE_SCROLL_SENSITIVE` |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if updates are visible for the given result set type;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### storesLowerCaseIdentifiers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun storesLowerCaseIdentifiers(): Boolean
```

Retrieves whether this database treats mixed case unquoted SQL identifiers as case insensitive and stores them in lower case.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### storesLowerCaseQuotedIdentifiers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun storesLowerCaseQuotedIdentifiers(): Boolean
```

Retrieves whether this database treats mixed case quoted SQL identifiers as case insensitive and stores them in lower case.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### storesMixedCaseIdentifiers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun storesMixedCaseIdentifiers(): Boolean
```

Retrieves whether this database treats mixed case unquoted SQL identifiers as case insensitive and stores them in mixed case.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### storesMixedCaseQuotedIdentifiers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun storesMixedCaseQuotedIdentifiers(): Boolean
```

Retrieves whether this database treats mixed case quoted SQL identifiers as case insensitive and stores them in mixed case.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### storesUpperCaseIdentifiers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun storesUpperCaseIdentifiers(): Boolean
```

Retrieves whether this database treats mixed case unquoted SQL identifiers as case insensitive and stores them in upper case.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### storesUpperCaseQuotedIdentifiers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun storesUpperCaseQuotedIdentifiers(): Boolean
```

Retrieves whether this database treats mixed case quoted SQL identifiers as case insensitive and stores them in upper case.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsANSI92EntryLevelSQL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsANSI92EntryLevelSQL(): Boolean
```

Retrieves whether this database supports the ANSI92 entry level SQL grammar.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsANSI92FullSQL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsANSI92FullSQL(): Boolean
```

Retrieves whether this database supports the ANSI92 full SQL grammar supported.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsANSI92IntermediateSQL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsANSI92IntermediateSQL(): Boolean
```

Retrieves whether this database supports the ANSI92 intermediate SQL grammar supported.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsAlterTableWithAddColumn

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsAlterTableWithAddColumn(): Boolean
```

Retrieves whether this database supports`ALTER TABLE`with add column.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsAlterTableWithDropColumn

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsAlterTableWithDropColumn(): Boolean
```

Retrieves whether this database supports`ALTER TABLE`with drop column.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsBatchUpdates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsBatchUpdates(): Boolean
```

Retrieves whether this database supports batch updates.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this database supports batch upcates;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsCatalogsInDataManipulation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsCatalogsInDataManipulation(): Boolean
```

Retrieves whether a catalog name can be used in a data manipulation statement.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsCatalogsInIndexDefinitions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsCatalogsInIndexDefinitions(): Boolean
```

Retrieves whether a catalog name can be used in an index definition statement.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsCatalogsInPrivilegeDefinitions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsCatalogsInPrivilegeDefinitions(): Boolean
```

Retrieves whether a catalog name can be used in a privilege definition statement.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsCatalogsInProcedureCalls

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsCatalogsInProcedureCalls(): Boolean
```

Retrieves whether a catalog name can be used in a procedure call statement.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsCatalogsInTableDefinitions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsCatalogsInTableDefinitions(): Boolean
```

Retrieves whether a catalog name can be used in a table definition statement.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsColumnAliasing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsColumnAliasing(): Boolean
```

Retrieves whether this database supports column aliasing.

If so, the SQL AS clause can be used to provide names for computed columns or to provide alias names for columns as required.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsConvert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsConvert(): Boolean
```

Retrieves whether this database supports the JDBC scalar function`CONVERT`for the conversion of one JDBC type to another. The JDBC types are the generic SQL data types defined in`java.sql.Types`.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsConvert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsConvert(
    fromType: Int, 
    toType: Int
): Boolean
```

Retrieves whether this database supports the JDBC scalar function`CONVERT`for conversions between the JDBC types*fromType* and*toType* . The JDBC types are the generic SQL data types defined in`java.sql.Types`.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fromType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the type to convert from; one of the type codes from the class`java.sql.Types` |
| `toType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the type to convert to; one of the type codes from the class`java.sql.Types` |

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [java.sql.Types](https://developer.android.com/reference/kotlin/java/sql/Types) 

### supportsCoreSQLGrammar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsCoreSQLGrammar(): Boolean
```

Retrieves whether this database supports the ODBC Core SQL grammar.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsCorrelatedSubqueries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsCorrelatedSubqueries(): Boolean
```

Retrieves whether this database supports correlated subqueries.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsDataDefinitionAndDataManipulationTransactions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsDataDefinitionAndDataManipulationTransactions(): Boolean
```

Retrieves whether this database supports both data definition and data manipulation statements within a transaction.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsDataManipulationTransactionsOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsDataManipulationTransactionsOnly(): Boolean
```

Retrieves whether this database supports only data manipulation statements within a transaction.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsDifferentTableCorrelationNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsDifferentTableCorrelationNames(): Boolean
```

Retrieves whether, when table correlation names are supported, they are restricted to being different from the names of the tables.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsExpressionsInOrderBy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsExpressionsInOrderBy(): Boolean
```

Retrieves whether this database supports expressions in`ORDER BY`lists.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsExtendedSQLGrammar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsExtendedSQLGrammar(): Boolean
```

Retrieves whether this database supports the ODBC Extended SQL grammar.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsFullOuterJoins

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsFullOuterJoins(): Boolean
```

Retrieves whether this database supports full nested outer joins.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsGetGeneratedKeys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsGetGeneratedKeys(): Boolean
```

Retrieves whether auto-generated keys can be retrieved after a statement has been executed

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if auto-generated keys can be retrieved after a statement has executed;`false`otherwise If`true`is returned, the JDBC driver must support the returning of auto-generated keys for at least SQL INSERT statements <br /> |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsGroupBy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsGroupBy(): Boolean
```

Retrieves whether this database supports some form of`GROUP BY`clause.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsGroupByBeyondSelect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsGroupByBeyondSelect(): Boolean
```

Retrieves whether this database supports using columns not included in the`SELECT`statement in a`GROUP BY`clause provided that all of the columns in the`SELECT`statement are included in the`GROUP BY`clause.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsGroupByUnrelated

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsGroupByUnrelated(): Boolean
```

Retrieves whether this database supports using a column that is not in the`SELECT`statement in a`GROUP BY`clause.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsIntegrityEnhancementFacility

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsIntegrityEnhancementFacility(): Boolean
```

Retrieves whether this database supports the SQL Integrity Enhancement Facility.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsLikeEscapeClause

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsLikeEscapeClause(): Boolean
```

Retrieves whether this database supports specifying a`LIKE`escape clause.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsLimitedOuterJoins

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsLimitedOuterJoins(): Boolean
```

Retrieves whether this database provides limited support for outer joins. (This will be`true`if the method`supportsFullOuterJoins`returns`true`).

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsMinimumSQLGrammar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsMinimumSQLGrammar(): Boolean
```

Retrieves whether this database supports the ODBC Minimum SQL grammar.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsMixedCaseIdentifiers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsMixedCaseIdentifiers(): Boolean
```

Retrieves whether this database treats mixed case unquoted SQL identifiers as case sensitive and as a result stores them in mixed case.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsMixedCaseQuotedIdentifiers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsMixedCaseQuotedIdentifiers(): Boolean
```

Retrieves whether this database treats mixed case quoted SQL identifiers as case sensitive and as a result stores them in mixed case.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsMultipleOpenResults

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsMultipleOpenResults(): Boolean
```

Retrieves whether it is possible to have multiple`ResultSet`objects returned from a`CallableStatement`object simultaneously.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if a`CallableStatement`object can return multiple`ResultSet`objects simultaneously;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a datanase access error occurs |

### supportsMultipleResultSets

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsMultipleResultSets(): Boolean
```

Retrieves whether this database supports getting multiple`ResultSet`objects from a single call to the method`execute`.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsMultipleTransactions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsMultipleTransactions(): Boolean
```

Retrieves whether this database allows having multiple transactions open at once (on different connections).

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsNamedParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsNamedParameters(): Boolean
```

Retrieves whether this database supports named parameters to callable statements.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if named parameters are supported;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsNonNullableColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsNonNullableColumns(): Boolean
```

Retrieves whether columns in this database may be defined as non-nullable.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsOpenCursorsAcrossCommit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsOpenCursorsAcrossCommit(): Boolean
```

Retrieves whether this database supports keeping cursors open across commits.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if cursors always remain open;`false`if they might not remain open |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsOpenCursorsAcrossRollback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsOpenCursorsAcrossRollback(): Boolean
```

Retrieves whether this database supports keeping cursors open across rollbacks.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if cursors always remain open;`false`if they might not remain open |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsOpenStatementsAcrossCommit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsOpenStatementsAcrossCommit(): Boolean
```

Retrieves whether this database supports keeping statements open across commits.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if statements always remain open;`false`if they might not remain open |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsOpenStatementsAcrossRollback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsOpenStatementsAcrossRollback(): Boolean
```

Retrieves whether this database supports keeping statements open across rollbacks.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if statements always remain open;`false`if they might not remain open |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsOrderByUnrelated

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsOrderByUnrelated(): Boolean
```

Retrieves whether this database supports using a column that is not in the`SELECT`statement in an`ORDER BY`clause.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsOuterJoins

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsOuterJoins(): Boolean
```

Retrieves whether this database supports some form of outer join.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsPositionedDelete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsPositionedDelete(): Boolean
```

Retrieves whether this database supports positioned`DELETE`statements.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsPositionedUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsPositionedUpdate(): Boolean
```

Retrieves whether this database supports positioned`UPDATE`statements.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsResultSetConcurrency

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsResultSetConcurrency(
    type: Int, 
    concurrency: Int
): Boolean
```

Retrieves whether this database supports the given concurrency type in combination with the given result set type.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):defined in`java.sql.ResultSet` |
| `concurrency` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):type defined in`java.sql.ResultSet` |

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [java.sql.Connection](https://developer.android.com/reference/kotlin/java/sql/Connection) 

### supportsResultSetHoldability

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsResultSetHoldability(holdability: Int): Boolean
```

Retrieves whether this database supports the given result set holdability.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `holdability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the following constants:`ResultSet.HOLD_CURSORS_OVER_COMMIT`or`ResultSet.CLOSE_CURSORS_AT_COMMIT` |

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [java.sql.Connection](https://developer.android.com/reference/kotlin/java/sql/Connection) 

### supportsResultSetType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsResultSetType(type: Int): Boolean
```

Retrieves whether this database supports the given result set type.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):defined in`java.sql.ResultSet` |

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [java.sql.Connection](https://developer.android.com/reference/kotlin/java/sql/Connection) 

### supportsSavepoints

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsSavepoints(): Boolean
```

Retrieves whether this database supports savepoints.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if savepoints are supported;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsSchemasInDataManipulation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsSchemasInDataManipulation(): Boolean
```

Retrieves whether a schema name can be used in a data manipulation statement.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsSchemasInIndexDefinitions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsSchemasInIndexDefinitions(): Boolean
```

Retrieves whether a schema name can be used in an index definition statement.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsSchemasInPrivilegeDefinitions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsSchemasInPrivilegeDefinitions(): Boolean
```

Retrieves whether a schema name can be used in a privilege definition statement.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsSchemasInProcedureCalls

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsSchemasInProcedureCalls(): Boolean
```

Retrieves whether a schema name can be used in a procedure call statement.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsSchemasInTableDefinitions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsSchemasInTableDefinitions(): Boolean
```

Retrieves whether a schema name can be used in a table definition statement.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsSelectForUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsSelectForUpdate(): Boolean
```

Retrieves whether this database supports`SELECT FOR UPDATE`statements.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsStatementPooling

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsStatementPooling(): Boolean
```

Retrieves whether this database supports statement pooling.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsStoredFunctionsUsingCallSyntax

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsStoredFunctionsUsingCallSyntax(): Boolean
```

Retrieves whether this database supports invoking user-defined or vendor functions using the stored procedure escape syntax.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsStoredProcedures

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsStoredProcedures(): Boolean
```

Retrieves whether this database supports stored procedure calls that use the stored procedure escape syntax.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsSubqueriesInComparisons

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsSubqueriesInComparisons(): Boolean
```

Retrieves whether this database supports subqueries in comparison expressions.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsSubqueriesInExists

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsSubqueriesInExists(): Boolean
```

Retrieves whether this database supports subqueries in`EXISTS`expressions.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsSubqueriesInIns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsSubqueriesInIns(): Boolean
```

Retrieves whether this database supports subqueries in`IN`expressions.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsSubqueriesInQuantifieds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsSubqueriesInQuantifieds(): Boolean
```

Retrieves whether this database supports subqueries in quantified expressions.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsTableCorrelationNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsTableCorrelationNames(): Boolean
```

Retrieves whether this database supports table correlation names.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsTransactionIsolationLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsTransactionIsolationLevel(level: Int): Boolean
```

Retrieves whether this database supports the given transaction isolation level.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the transaction isolation levels defined in`java.sql.Connection` |

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [java.sql.Connection](https://developer.android.com/reference/kotlin/java/sql/Connection) 

### supportsTransactions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsTransactions(): Boolean
```

Retrieves whether this database supports transactions. If not, invoking the method`commit`is a noop, and the isolation level is`TRANSACTION_NONE`.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if transactions are supported;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsUnion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsUnion(): Boolean
```

Retrieves whether this database supports SQL`UNION`.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### supportsUnionAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supportsUnionAll(): Boolean
```

Retrieves whether this database supports SQL`UNION ALL`.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### updatesAreDetected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun updatesAreDetected(type: Int): Boolean
```

Retrieves whether or not a visible row update can be detected by calling the method`ResultSet.rowUpdated`.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the`ResultSet`type; one of`ResultSet.TYPE_FORWARD_ONLY`,`ResultSet.TYPE_SCROLL_INSENSITIVE`, or`ResultSet.TYPE_SCROLL_SENSITIVE` |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if changes are detected by the result set type;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### usesLocalFilePerTable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun usesLocalFilePerTable(): Boolean
```

Retrieves whether this database uses a file for each table.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this database uses a local file for each table;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### usesLocalFiles

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun usesLocalFiles(): Boolean
```

Retrieves whether this database stores tables in a local file.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
