# BlockedNumberContract

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BlockedNumberContract

Kotlin| [Java](../android/provider/BlockedNumberContract.md) 
| --- | --- |

```
open class BlockedNumberContract
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.BlockedNumberContract](../android/provider/BlockedNumberContract.md) |

The contract between the blockednumber provider and applications. Contains definitions for the supported URIs and columns.

### Overview

The content provider exposes a table containing blocked numbers. The columns and URIs for accessing this table are defined by the [BlockedNumbers](../android/provider/BlockedNumberContract.BlockedNumbers.md) class. Messages, and calls from blocked numbers are discarded by the platform. Notifications upon provider changes can be received using a [android.database.ContentObserver](../android/database/ContentObserver.md).

The platform will not block messages, and calls from emergency numbers as defined by [android.telephony.PhoneNumberUtils#isEmergencyNumber(String)](../android/telephony/PhoneNumberUtils.md)). If the user contacts emergency services, number blocking is disabled by the platform for a duration defined by [android.telephony.CarrierConfigManager#KEY_DURATION_BLOCKING_DISABLED_AFTER_EMERGENCY_INT](../android/telephony/CarrierConfigManager.md).

### Permissions

Only the system, the default SMS application, and the default phone app (See [android.telecom.TelecomManager#getDefaultDialerPackage()](../android/telecom/TelecomManager.md))), and carrier apps (See [android.service.carrier.CarrierService](../android/service/carrier/CarrierService.md)) can read, and write to the blockednumber provider. However, [canCurrentUserBlockNumbers(android.content.Context)](../android/provider/BlockedNumberContract.md))can be accessed by any application.

### Data

Other than regular phone numbers, the blocked number provider can also store addresses (such as email) from which a user can receive messages, and calls. The blocked numbers are stored in the [BlockedNumbers.COLUMN_ORIGINAL_NUMBER](../android/provider/BlockedNumberContract.BlockedNumbers.md) column. A normalized version of phone numbers (if normalization is possible) is stored in [BlockedNumbers.COLUMN_E164_NUMBER](../android/provider/BlockedNumberContract.BlockedNumbers.md) column. The platform blocks calls, and messages from an address if it is present in in the [BlockedNumbers.COLUMN_ORIGINAL_NUMBER](../android/provider/BlockedNumberContract.BlockedNumbers.md) column or if the E164 version of the address matches the [BlockedNumbers.COLUMN_E164_NUMBER](../android/provider/BlockedNumberContract.BlockedNumbers.md) column.

### Operations

**Insert**

: [BlockedNumbers.COLUMN_ORIGINAL_NUMBER](../android/provider/BlockedNumberContract.BlockedNumbers.md) is a required column that needs to be populated. Apps can optionally provide the [BlockedNumbers.COLUMN_E164_NUMBER](../android/provider/BlockedNumberContract.BlockedNumbers.md) which is the phone number's E164 representation. The provider automatically populates this column if the app does not provide it. Note that this column is not populated if normalization fails or if the address is not a phone number (eg: email).

 Attempting to insert an existing blocked number (same [BlockedNumbers.COLUMN_ORIGINAL_NUMBER](../android/provider/BlockedNumberContract.BlockedNumbers.md) column) will result in replacing the existing blocked number.

 Examples: 

    ```kotlin
    ContentValues values = new ContentValues();
      values.put(BlockedNumbers.COLUMN_ORIGINAL_NUMBER, "1234567890");
      Uri uri = getContentResolver().insert(BlockedNumbers.CONTENT_URI, values);
      
    ```  

    ```kotlin
    ContentValues values = new ContentValues();
      values.put(BlockedNumbers.COLUMN_ORIGINAL_NUMBER, "1234567890");
      values.put(BlockedNumbers.COLUMN_E164_NUMBER, "+11234567890");
      Uri uri = getContentResolver().insert(BlockedNumbers.CONTENT_URI, values);
      
    ```  

    ```kotlin
    ContentValues values = new ContentValues();
      values.put(BlockedNumbers.COLUMN_ORIGINAL_NUMBER, "12345@abdcde.com");
      Uri uri = getContentResolver().insert(BlockedNumbers.CONTENT_URI, values);
      
    ```

 <br />

**Update**

: Updates are not supported. Use Delete, and Insert instead.

**Delete**

: Deletions can be performed as follows:

    ```kotlin
    ContentValues values = new ContentValues();
      values.put(BlockedNumbers.COLUMN_ORIGINAL_NUMBER, "1234567890");
      Uri uri = getContentResolver().insert(BlockedNumbers.CONTENT_URI, values);
      getContentResolver().delete(uri, null, null);
      
    ```
 To check if a particular number is blocked, use the method [isBlocked(android.content.Context,java.lang.String)](../android/provider/BlockedNumberContract.md)).

 <br />

**Query**

: All blocked numbers can be enumerated as follows:

    ```kotlin
    Cursor c = getContentResolver().query(BlockedNumbers.CONTENT_URI,
               new String[]{BlockedNumbers.COLUMN_ID, BlockedNumbers.COLUMN_ORIGINAL_NUMBER,
               BlockedNumbers.COLUMN_E164_NUMBER}, null, null, null);
      
    ```

 <br />

**Unblock**

: Use the method [unblock(android.content.Context,java.lang.String)](../android/provider/BlockedNumberContract.md))to unblock numbers.

## Summary

| Nested classes ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [BlockedNumbers](../android/provider/BlockedNumberContract.BlockedNumbers.md) Constants to interact with the blocked numbers list. |

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AUTHORITY](../android/provider/BlockedNumberContract.md) The authority for the blocked number provider |

| Public methods ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canCurrentUserBlockNumbers](../android/provider/BlockedNumberContract.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Checks if blocking numbers is supported for the current user. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBlocked](../android/provider/BlockedNumberContract.md))`(`context:` ` [Context](../android/content/Context.md)!`, `phoneNumber:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns whether a given number is in the blocked list. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [unblock](../android/provider/BlockedNumberContract.md))`(`context:` ` [Context](../android/content/Context.md)!`, `phoneNumber:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Unblocks the`phoneNumber`if it is blocked. |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Uri](../android/net/Uri.md)! | [AUTHORITY_URI](../android/provider/BlockedNumberContract.md) A content:// style uri to the authority for the blocked number provider |

## Constants

### AUTHORITY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUTHORITY: String
```

The authority for the blocked number provider 

 Value: "com.android.blockednumber"

## Public methods

### canCurrentUserBlockNumbers

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun canCurrentUserBlockNumbers(context: Context!): Boolean
```

Checks if blocking numbers is supported for the current user.

Typically, blocking numbers is only supported for one user at a time.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the current user can block numbers. |

### isBlocked

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isBlocked(
    context: Context!, 
    phoneNumber: String!
): Boolean
```

Returns whether a given number is in the blocked list.

This matches the`phoneNumber`against the [BlockedNumbers.COLUMN_ORIGINAL_NUMBER](../android/provider/BlockedNumberContract.BlockedNumbers.md) column, and the E164 representation of the`phoneNumber`with the [BlockedNumbers.COLUMN_E164_NUMBER](../android/provider/BlockedNumberContract.BlockedNumbers.md) column.

Note that if the [canCurrentUserBlockNumbers](../android/provider/BlockedNumberContract.md))is`false`for the user context`context`, this method will throw a [SecurityException](../java/lang/SecurityException.md). 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the`phoneNumber`is blocked. |

### unblock

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun unblock(
    context: Context!, 
    phoneNumber: String!
): Int
```

Unblocks the`phoneNumber`if it is blocked.

This deletes all rows where the`phoneNumber`matches the [BlockedNumbers.COLUMN_ORIGINAL_NUMBER](../android/provider/BlockedNumberContract.BlockedNumbers.md) column or the E164 representation of the`phoneNumber`matches the [BlockedNumbers.COLUMN_E164_NUMBER](../android/provider/BlockedNumberContract.BlockedNumbers.md) column.

To delete rows based on exact match with specific columns such as [BlockedNumbers.COLUMN_ID](../android/provider/BlockedNumberContract.BlockedNumbers.md) use[android.content.ContentProvider#delete(Uri, String, String[])](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#delete(android.net.Uri,%20kotlin.String,%20kotlin.Array))with [BlockedNumbers.CONTENT_URI](../android/provider/BlockedNumberContract.BlockedNumbers.md) URI.

Note that if the [canCurrentUserBlockNumbers](../android/provider/BlockedNumberContract.md))is`false`for the user context`context`, this method will throw a [SecurityException](../java/lang/SecurityException.md). 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of rows deleted in the blocked number provider as a result of unblock. |

## Properties

### AUTHORITY_URI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUTHORITY_URI: Uri!
```

A content:// style uri to the authority for the blocked number provider
