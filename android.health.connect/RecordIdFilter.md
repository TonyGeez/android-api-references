# RecordIdFilter

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RecordIdFilter

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/RecordIdFilter "View this page in Java") 

```
open class RecordIdFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.health.connect.RecordIdFilter](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter#) |

A class to represent filtering based on record ID or client ID.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [RecordIdFilter](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter#) | [fromClientRecordId](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter#fromClientRecordId(java.lang.Class,%20kotlin.String))`(`recordType:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<out` ` [Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record)!>`, `clientRecordId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Creates an instance of Record id filter based on client record id. |
| openstatic [RecordIdFilter](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter#) | [fromId](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter#fromId(java.lang.Class,%20kotlin.String))`(`recordType:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<out` ` [Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record)!>`, `id:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Creates an instance of Record id filter based on record id. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getClientRecordId](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter#getClientRecordId())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getId](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter#getId())`()` <br /> |
| open [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<out [Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record)!\> | [getRecordType](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter#getRecordType())`()` <br /> |

## Public methods

### fromClientRecordId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fromClientRecordId(
    recordType: Class<out Record!>, 
    clientRecordId: String
): RecordIdFilter
```

Creates an instance of Record id filter based on client record id.

Note: this only works when reading own records, using client record ids to read records inserted by another app will return no result.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `recordType` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<out [Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record)!\>:Record class for which the client record id must be set. This value cannot be`null`. |
| `clientRecordId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):Client identifier that was set while inserting the record. This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [RecordIdFilter](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter#) | Object of [RecordIdFilter](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter#) This value cannot be`null`. |

### fromId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fromId(
    recordType: Class<out Record!>, 
    id: String
): RecordIdFilter
```

Creates an instance of Record id filter based on record id.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `recordType` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<out [Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record)!\>:Record class for which the id must be set. This value cannot be`null`. |
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):Identifier generated by the platform and returned by [android.health.connect.HealthConnectManager#insertRecords](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#insertRecords(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [RecordIdFilter](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter#) | Object of [RecordIdFilter](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter#) This value cannot be`null`. |

### getClientRecordId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getClientRecordId(): String?
```

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | Client record identifier This value may be`null`. |

### getId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getId(): String?
```

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | Identifier given by the platform This value may be`null`. |

### getRecordType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRecordType(): Class<out Record!>
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<out` ` [Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record)!> | Record class for this identifier This value cannot be`null`. |
