# IkeSessionConfiguration

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeSessionConfiguration

Kotlin| [Java](https://developer.android.com/reference/android/net/ipsec/ike/IkeSessionConfiguration "View this page in Java") 

```
class IkeSessionConfiguration
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.ipsec.ike.IkeSessionConfiguration](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConfiguration#) |

IkeSessionConfiguration represents the negotiated configuration for a [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession).

Configurations include remote application version and enabled IKE extensions.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConfiguration.Builder) This class can be used to incrementally construct a [IkeSessionConfiguration](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConfiguration#). |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTENSION_TYPE_FRAGMENTATION](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConfiguration#EXTENSION_TYPE_FRAGMENTATION:kotlin.Int) IKE Message Fragmentation |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTENSION_TYPE_MOBIKE](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConfiguration#EXTENSION_TYPE_MOBIKE:kotlin.Int) IKEv2 Mobility and Multihoming Protocol |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [EapInfo](https://developer.android.com/reference/kotlin/android/net/eap/EapInfo.html#)? | [getEapInfo](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConfiguration#getEapInfo())`()` Retrieves the EAP information. |
| [IkeSessionConnectionInfo](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConnectionInfo) | [getIkeSessionConnectionInfo](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConfiguration#getIkeSessionConnectionInfo())`()` Returns the connection information. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getRemoteApplicationVersion](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConfiguration#getRemoteApplicationVersion())`()` Gets remote (server) version information. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\> | [getRemoteVendorIds](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConfiguration#getRemoteVendorIds())`()` Returns remote vendor IDs received during IKE Session setup. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIkeExtensionEnabled](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConfiguration#isIkeExtensionEnabled(kotlin.Int))`(`extensionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks if an IKE extension is enabled. |

## Constants

### EXTENSION_TYPE_FRAGMENTATION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTENSION_TYPE_FRAGMENTATION: Int
```

IKE Message Fragmentation 

 Value: 1

### EXTENSION_TYPE_MOBIKE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTENSION_TYPE_MOBIKE: Int
```

IKEv2 Mobility and Multihoming Protocol 

 Value: 2

## Public methods

### getEapInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEapInfo(): EapInfo?
```

Retrieves the EAP information.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [EapInfo](https://developer.android.com/reference/kotlin/android/net/eap/EapInfo.html#)? | the EAP information provided by the server during EAP authentication (e.g. next re-authentication ID), or null if the server did not provide any information that will be useful after the authentication. |

### getIkeSessionConnectionInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIkeSessionConnectionInfo(): IkeSessionConnectionInfo
```

Returns the connection information.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [IkeSessionConnectionInfo](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConnectionInfo) | the IKE Session connection information. This value cannot be`null`. |

### getRemoteApplicationVersion

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRemoteApplicationVersion(): String
```

Gets remote (server) version information.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | application version of the remote server, or an empty string if the remote server did not provide the application version. This value cannot be`null`. |

### getRemoteVendorIds

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRemoteVendorIds(): MutableList<ByteArray!>
```

Returns remote vendor IDs received during IKE Session setup.

According to the IKEv2 specification (RFC 7296), a vendor ID may indicate the sender is capable of accepting certain extensions to the protocol, or it may simply identify the implementation as an aid in debugging.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!> | the vendor IDs of the remote server, or an empty list if no vendor ID is received during IKE Session setup. This value cannot be`null`. |

### isIkeExtensionEnabled

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isIkeExtensionEnabled(extensionType: Int): Boolean
```

Checks if an IKE extension is enabled.

An IKE extension is enabled when both sides can support it. This negotiation always happens in IKE initial exchanges (IKE INIT and IKE AUTH).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `extensionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the extension type. Value is [android.net.ipsec.ike.IkeSessionConfiguration#EXTENSION_TYPE_FRAGMENTATION](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConfiguration#EXTENSION_TYPE_FRAGMENTATION:kotlin.Int), or [android.net.ipsec.ike.IkeSessionConfiguration#EXTENSION_TYPE_MOBIKE](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConfiguration#EXTENSION_TYPE_MOBIKE:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this extension is enabled. |
