# E2eeContactKeysManager

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# E2eeContactKeysManager

Kotlin| [Java](../android/provider/E2eeContactKeysManager.md) 
| --- | --- |

```
class E2eeContactKeysManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.E2eeContactKeysManager](../android/provider/E2eeContactKeysManager.md) |

E2eeContactKeysManager provides access to the provider of end-to-end encryption contact keys. It manages two types of keys - [E2eeContactKey](../android/provider/E2eeContactKeysManager.E2eeContactKey.md) and [E2eeSelfKey](../android/provider/E2eeContactKeysManager.E2eeSelfKey.md).

- A [E2eeContactKey](../android/provider/E2eeContactKeysManager.E2eeContactKey.md) is a public key associated with a contact. It's used to end-to-end encrypt the communications between a user and the contact. This API allows operations on [E2eeContactKey](../android/provider/E2eeContactKeysManager.E2eeContactKey.md) s to insert/update, remove, change the verification state, and retrieving keys (either created by or visible to the caller app).
- A [E2eeSelfKey](../android/provider/E2eeContactKeysManager.E2eeSelfKey.md) is a key for this device, so the key represents the owner of the device. This API allows operations on [E2eeSelfKey](../android/provider/E2eeContactKeysManager.E2eeSelfKey.md) s to insert/update, remove, and retrieving self keys (either created by or visible to the caller app).

Keys are uniquely identified by:

<!-- -->

- ownerPackageName - package name of an app that the key belongs to.
- deviceId - an app-specified identifier for the device, defined by the app. Within that app, the deviceID should be unique among devices belonging to that user.
- accountId - the app-specified identifier for the account for which the contact key can be used. Using different account IDs allows for multiple key entries representing the same user. For most apps this would be a phone number.

Contact keys also use lookupKey which is an opaque value used to identify a contact in ContactsProvider.

<br />

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [E2eeContactKey](../android/provider/E2eeContactKeysManager.E2eeContactKey.md) A parcelable class encapsulating other users' end to end encrypted contact key. |
| | [E2eeSelfKey](../android/provider/E2eeContactKeysManager.E2eeSelfKey.md) A parcelable class encapsulating self end to end encrypted contact key. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VERIFICATION_STATE_UNVERIFIED](../android/provider/E2eeContactKeysManager.md) Unverified state of a contact end to end encrypted key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VERIFICATION_STATE_VERIFICATION_FAILED](../android/provider/E2eeContactKeysManager.md) Failed verification state of a contact end to end encrypted key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VERIFICATION_STATE_VERIFIED](../android/provider/E2eeContactKeysManager.md) Verified state of a contact end to end encrypted key. |
| --- | --- |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [E2eeContactKeysManager.E2eeContactKey](../android/provider/E2eeContactKeysManager.E2eeContactKey.md)!\> | [getAllE2eeContactKeys](../android/provider/E2eeContactKeysManager.md))`(`lookupKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Retrieves all end-to-end encryption contact key entries that belong to apps visible to the caller. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [E2eeContactKeysManager.E2eeSelfKey](../android/provider/E2eeContactKeysManager.E2eeSelfKey.md)!\> | [getAllE2eeSelfKeys](../android/provider/E2eeContactKeysManager.md))`()` Returns all end-to-end encryption self key entries that belong to apps visible to the caller. |
| [E2eeContactKeysManager.E2eeContactKey](../android/provider/E2eeContactKeysManager.E2eeContactKey.md)? | [getE2eeContactKey](../android/provider/E2eeContactKeysManager.md))`(`lookupKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `deviceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `accountId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Retrieves an end-to-end encryption contact key entry given the lookup key, device ID, accountId and inferred caller package name. |
| --- | --- |
| [E2eeContactKeysManager.E2eeSelfKey](../android/provider/E2eeContactKeysManager.E2eeSelfKey.md)? | [getE2eeSelfKey](../android/provider/E2eeContactKeysManager.md))`(`deviceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `accountId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns an end-to-end encryption self key entry given the deviceId and the inferred package name of the caller. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxKeySizeBytes](../android/provider/E2eeContactKeysManager.md))`()` Maximum size of an end-to-end encryption contact key. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [E2eeContactKeysManager.E2eeContactKey](../android/provider/E2eeContactKeysManager.E2eeContactKey.md)!\> | [getOwnerE2eeContactKeys](../android/provider/E2eeContactKeysManager.md))`(`lookupKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Retrieves all end-to-end encryption contact key entries for a given lookupKey that belong to the caller app. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [E2eeContactKeysManager.E2eeSelfKey](../android/provider/E2eeContactKeysManager.E2eeSelfKey.md)!\> | [getOwnerE2eeSelfKeys](../android/provider/E2eeContactKeysManager.md))`()` Returns all end-to-end encryption self key entries that are owned by the caller app. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeE2eeContactKey](../android/provider/E2eeContactKeysManager.md))`(`lookupKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `deviceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `accountId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Removes an end-to-end encryption contact key entry that belongs to the caller app. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeE2eeSelfKey](../android/provider/E2eeContactKeysManager.md))`(`deviceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `accountId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Removes an end-to-end encryption self key entry given the deviceId and the inferred package name of the caller. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [updateE2eeContactKeyLocalVerificationState](../android/provider/E2eeContactKeysManager.md))`(`lookupKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `deviceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `accountId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `localVerificationState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates an end-to-end encryption contact key entry's local verification state that belongs to the caller app. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [updateE2eeContactKeyRemoteVerificationState](../android/provider/E2eeContactKeysManager.md))`(`lookupKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `deviceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `accountId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `remoteVerificationState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates an end-to-end encryption contact key entry's remote verification state that belongs to the caller app. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [updateE2eeSelfKeyRemoteVerificationState](../android/provider/E2eeContactKeysManager.md))`(`deviceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `accountId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `remoteVerificationState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates an end-to-end encryption self key entry's remote verification state. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateOrInsertE2eeContactKey](../android/provider/E2eeContactKeysManager.md))`(`lookupKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `deviceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `accountId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `keyValue:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Inserts a new entry into the end-to-end encryption contact keys table or updates one if it already exists. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [updateOrInsertE2eeSelfKey](../android/provider/E2eeContactKeysManager.md))`(`deviceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `accountId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `keyValue:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Inserts a new entry into the end-to-end encryption self keys table or updates one if it already exists. |

## Constants

### VERIFICATION_STATE_UNVERIFIED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VERIFICATION_STATE_UNVERIFIED: Int
```

Unverified state of a contact end to end encrypted key. 

 Value: 0

### VERIFICATION_STATE_VERIFICATION_FAILED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VERIFICATION_STATE_VERIFICATION_FAILED: Int
```

Failed verification state of a contact end to end encrypted key. 

 Value: 1

### VERIFICATION_STATE_VERIFIED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VERIFICATION_STATE_VERIFIED: Int
```

Verified state of a contact end to end encrypted key. 

 Value: 2

## Public methods

### getAllE2eeContactKeys

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAllE2eeContactKeys(lookupKey: String): MutableList<E2eeContactKeysManager.E2eeContactKey!>
```

Retrieves all end-to-end encryption contact key entries that belong to apps visible to the caller. The keys will be stripped of deviceId, timeUpdated and keyValue data. 
Requires [android.Manifest.permission#READ_CONTACTS](../android/Manifest.permission.md)

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `lookupKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the value that references the contact This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [E2eeContactKeysManager.E2eeContactKey](../android/provider/E2eeContactKeysManager.E2eeContactKey.md)!> | a list of [E2eeContactKey](../android/provider/E2eeContactKeysManager.E2eeContactKey.md) objects containing the contact key information, or an empty list if no keys are found. This value cannot be`null`. |

### getAllE2eeSelfKeys

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAllE2eeSelfKeys(): MutableList<E2eeContactKeysManager.E2eeSelfKey!>
```

Returns all end-to-end encryption self key entries that belong to apps visible to the caller. The keys will be stripped of deviceId, timeUpdated and keyValue data. 
Requires [android.Manifest.permission#READ_CONTACTS](../android/Manifest.permission.md)

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [E2eeContactKeysManager.E2eeSelfKey](../android/provider/E2eeContactKeysManager.E2eeSelfKey.md)!> | a list of [E2eeSelfKey](../android/provider/E2eeContactKeysManager.E2eeSelfKey.md) objects containing the end-to-end encryption self key information, or an empty list if no self keys are found. This value cannot be`null`. |

### getE2eeContactKey

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getE2eeContactKey(
    lookupKey: String, 
    deviceId: String, 
    accountId: String
): E2eeContactKeysManager.E2eeContactKey?
```

Retrieves an end-to-end encryption contact key entry given the lookup key, device ID, accountId and inferred caller package name. 
Requires [android.Manifest.permission#READ_CONTACTS](../android/Manifest.permission.md)

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `lookupKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the value that references the contact This value cannot be`null`. |
| `deviceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):an app-specified identifier for the device This value cannot be`null`. |
| `accountId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):an app-specified identifier for the account This value cannot be`null`. |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [E2eeContactKeysManager.E2eeContactKey](../android/provider/E2eeContactKeysManager.E2eeContactKey.md)? | a [E2eeContactKey](../android/provider/E2eeContactKeysManager.E2eeContactKey.md) object containing the contact key information, or null if no contact key is found. |

### getE2eeSelfKey

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getE2eeSelfKey(
    deviceId: String, 
    accountId: String
): E2eeContactKeysManager.E2eeSelfKey?
```

Returns an end-to-end encryption self key entry given the deviceId and the inferred package name of the caller. 
Requires [android.Manifest.permission#READ_CONTACTS](../android/Manifest.permission.md)

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):an app-specified identifier for the device This value cannot be`null`. |
| `accountId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):an app-specified identifier for the account This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [E2eeContactKeysManager.E2eeSelfKey](../android/provider/E2eeContactKeysManager.E2eeSelfKey.md)? | a [E2eeSelfKey](../android/provider/E2eeContactKeysManager.E2eeSelfKey.md) object containing the end-to-end encryption self key information, or null if no self key is found. |

### getMaxKeySizeBytes

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMaxKeySizeBytes(): Int
```

Maximum size of an end-to-end encryption contact key. 

### getOwnerE2eeContactKeys

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOwnerE2eeContactKeys(lookupKey: String): MutableList<E2eeContactKeysManager.E2eeContactKey!>
```

Retrieves all end-to-end encryption contact key entries for a given lookupKey that belong to the caller app. 
Requires [android.Manifest.permission#READ_CONTACTS](../android/Manifest.permission.md)

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `lookupKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the value that references the contact This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [E2eeContactKeysManager.E2eeContactKey](../android/provider/E2eeContactKeysManager.E2eeContactKey.md)!> | a list of [E2eeContactKey](../android/provider/E2eeContactKeysManager.E2eeContactKey.md) objects containing the end-to-end encryption contact key information, or an empty list if no keys are found. This value cannot be`null`. |

### getOwnerE2eeSelfKeys

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOwnerE2eeSelfKeys(): MutableList<E2eeContactKeysManager.E2eeSelfKey!>
```

Returns all end-to-end encryption self key entries that are owned by the caller app. 
Requires [android.Manifest.permission#READ_CONTACTS](../android/Manifest.permission.md)

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [E2eeContactKeysManager.E2eeSelfKey](../android/provider/E2eeContactKeysManager.E2eeSelfKey.md)!> | a list of [E2eeSelfKey](../android/provider/E2eeContactKeysManager.E2eeSelfKey.md) objects containing the end-to-end encryption self key information, or an empty list if no self keys are found. This value cannot be`null`. |

### removeE2eeContactKey

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeE2eeContactKey(
    lookupKey: String, 
    deviceId: String, 
    accountId: String
): Boolean
```

Removes an end-to-end encryption contact key entry that belongs to the caller app. 
Requires [android.Manifest.permission#WRITE_CONTACTS](../android/Manifest.permission.md)

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `lookupKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the value that references the contact This value cannot be`null`. |
| `deviceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):an app-specified identifier for the device This value cannot be`null`. |
| `accountId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):an app-specified identifier for the account This value cannot be`null`. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the entry was removed, false otherwise. |

### removeE2eeSelfKey

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeE2eeSelfKey(
    deviceId: String, 
    accountId: String
): Boolean
```

Removes an end-to-end encryption self key entry given the deviceId and the inferred package name of the caller. 
Requires [android.Manifest.permission#WRITE_CONTACTS](../android/Manifest.permission.md)

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):an app-specified identifier for the device This value cannot be`null`. |
| `accountId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):an app-specified identifier for the account This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the entry was removed, false otherwise. |

### updateE2eeContactKeyLocalVerificationState

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun updateE2eeContactKeyLocalVerificationState(
    lookupKey: String, 
    deviceId: String, 
    accountId: String, 
    localVerificationState: Int
): Boolean
```

Updates an end-to-end encryption contact key entry's local verification state that belongs to the caller app. 
Requires [android.Manifest.permission#WRITE_CONTACTS](../android/Manifest.permission.md)

| Parameters ||
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `lookupKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the value that references the contact This value cannot be`null`. |
| `deviceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):an app-specified identifier for the device This value cannot be`null`. |
| `accountId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):an app-specified identifier for the account This value cannot be`null`. |
| --- | --- |
| `localVerificationState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new local verification state Value is [android.provider.E2eeContactKeysManager#VERIFICATION_STATE_UNVERIFIED](../android/provider/E2eeContactKeysManager.md), [android.provider.E2eeContactKeysManager#VERIFICATION_STATE_VERIFICATION_FAILED](../android/provider/E2eeContactKeysManager.md), or [android.provider.E2eeContactKeysManager#VERIFICATION_STATE_VERIFIED](../android/provider/E2eeContactKeysManager.md) |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the entry was updated, false otherwise. |

### updateE2eeContactKeyRemoteVerificationState

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun updateE2eeContactKeyRemoteVerificationState(
    lookupKey: String, 
    deviceId: String, 
    accountId: String, 
    remoteVerificationState: Int
): Boolean
```

Updates an end-to-end encryption contact key entry's remote verification state that belongs to the caller app. 
Requires [android.Manifest.permission#WRITE_CONTACTS](../android/Manifest.permission.md)

| Parameters ||
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `lookupKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the value that references the contact This value cannot be`null`. |
| `deviceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):an app-specified identifier for the device This value cannot be`null`. |
| `accountId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):an app-specified identifier for the account This value cannot be`null`. |
| --- | --- |
| `remoteVerificationState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new remote verification state Value is [android.provider.E2eeContactKeysManager#VERIFICATION_STATE_UNVERIFIED](../android/provider/E2eeContactKeysManager.md), [android.provider.E2eeContactKeysManager#VERIFICATION_STATE_VERIFICATION_FAILED](../android/provider/E2eeContactKeysManager.md), or [android.provider.E2eeContactKeysManager#VERIFICATION_STATE_VERIFIED](../android/provider/E2eeContactKeysManager.md) |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the entry was updated, false otherwise. |

### updateE2eeSelfKeyRemoteVerificationState

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun updateE2eeSelfKeyRemoteVerificationState(
    deviceId: String, 
    accountId: String, 
    remoteVerificationState: Int
): Boolean
```

Updates an end-to-end encryption self key entry's remote verification state. 
Requires [android.Manifest.permission#WRITE_CONTACTS](../android/Manifest.permission.md)

| Parameters ||
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):an app-specified identifier for the device This value cannot be`null`. |
| `accountId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):an app-specified identifier for the account This value cannot be`null`. |
| `remoteVerificationState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new remote verification state Value is [android.provider.E2eeContactKeysManager#VERIFICATION_STATE_UNVERIFIED](../android/provider/E2eeContactKeysManager.md), [android.provider.E2eeContactKeysManager#VERIFICATION_STATE_VERIFICATION_FAILED](../android/provider/E2eeContactKeysManager.md), or [android.provider.E2eeContactKeysManager#VERIFICATION_STATE_VERIFIED](../android/provider/E2eeContactKeysManager.md) |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the entry was updated, false otherwise. |

### updateOrInsertE2eeContactKey

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun updateOrInsertE2eeContactKey(
    lookupKey: String, 
    deviceId: String, 
    accountId: String, 
    keyValue: ByteArray
): Unit
```

Inserts a new entry into the end-to-end encryption contact keys table or updates one if it already exists. The inserted/updated end-to-end encryption contact key is owned by the caller app. 
Requires [android.Manifest.permission#WRITE_CONTACTS](../android/Manifest.permission.md)

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `lookupKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):value that references the contact This value cannot be`null`. |
| `deviceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):an app-specified identifier for the device This value cannot be`null`. |
| `accountId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):an app-specified identifier for the account This value cannot be`null`. |
| --- | --- |
| `keyValue` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the raw bytes for the key (max size is [getMaxKeySizeBytes](../android/provider/E2eeContactKeysManager.md))bytes) This value cannot be`null`. |

### updateOrInsertE2eeSelfKey

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun updateOrInsertE2eeSelfKey(
    deviceId: String, 
    accountId: String, 
    keyValue: ByteArray
): Boolean
```

Inserts a new entry into the end-to-end encryption self keys table or updates one if it already exists. 
Requires [android.Manifest.permission#WRITE_CONTACTS](../android/Manifest.permission.md)

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):an app-specified identifier for the device This value cannot be`null`. |
| `accountId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):an app-specified identifier for the account This value cannot be`null`. |
| `keyValue` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the raw bytes for the key (max size is [getMaxKeySizeBytes](../android/provider/E2eeContactKeysManager.md))bytes) This value cannot be`null`. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the entry was added or updated, false otherwise. |
