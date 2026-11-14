# ChildSessionConfiguration

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChildSessionConfiguration

Kotlin | [Java](../android/net/ipsec/ike/ChildSessionConfiguration.md) 
| --- | --- |

```
class ChildSessionConfiguration
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.ipsec.ike.ChildSessionConfiguration](../android/net/ipsec/ike/ChildSessionConfiguration.md) |

ChildSessionConfiguration represents the negotiated configuration for a Child Session.

Configurations include traffic selectors and internal network information.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/net/ipsec/ike/ChildSessionConfiguration.Builder.md) This class can be used to incrementally construct a [ChildSessionConfiguration](../android/net/ipsec/ike/ChildSessionConfiguration.md). |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [IkeTrafficSelector](../android/net/ipsec/ike/IkeTrafficSelector.md)!\> | [getInboundTrafficSelectors](../android/net/ipsec/ike/ChildSessionConfiguration.md))`()` Returns the negotiated inbound traffic selectors. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [IkeTrafficSelector](../android/net/ipsec/ike/IkeTrafficSelector.md)!\> | [getOutboundTrafficSelectors](../android/net/ipsec/ike/ChildSessionConfiguration.md))`()` Returns the negotiated outbound traffic selectors. |

## Public methods

### getInboundTrafficSelectors

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInboundTrafficSelectors(): MutableList<IkeTrafficSelector!>
```

Returns the negotiated inbound traffic selectors.

Only inbound traffic within the range is acceptable to the Child Session.

The Android platform does not support port-based routing. Port ranges of traffic selectors are only informational.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [IkeTrafficSelector](../android/net/ipsec/ike/IkeTrafficSelector.md)!> | the inbound traffic selectors. This value cannot be `null`. |

### getOutboundTrafficSelectors

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOutboundTrafficSelectors(): MutableList<IkeTrafficSelector!>
```

Returns the negotiated outbound traffic selectors.

Only outbound traffic within the range is acceptable to the Child Session.

The Android platform does not support port-based routing. Port ranges of traffic selectors are only informational.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [IkeTrafficSelector](../android/net/ipsec/ike/IkeTrafficSelector.md)!> | the outbound traffic selectors. This value cannot be `null`. |
