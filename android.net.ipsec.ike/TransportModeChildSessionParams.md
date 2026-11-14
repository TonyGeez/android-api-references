# TransportModeChildSessionParams

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransportModeChildSessionParams

Kotlin| [Java](../android/net/ipsec/ike/TransportModeChildSessionParams.md) 
| --- | --- |

```
class TransportModeChildSessionParams : ChildSessionParams
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.net.ipsec.ike.ChildSessionParams](../android/net/ipsec/ike/ChildSessionParams.md) ||
| | ↳ | [android.net.ipsec.ike.TransportModeChildSessionParams](../android/net/ipsec/ike/TransportModeChildSessionParams.md) |

TransportModeChildSessionParams represents proposed configurations for negotiating a transport mode Child Session.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/net/ipsec/ike/TransportModeChildSessionParams.Builder.md) This class can be used to incrementally construct a [TransportModeChildSessionParams](../android/net/ipsec/ike/TransportModeChildSessionParams.md). |

| Inherited functions ||
|---|---|
| From class [ChildSessionParams](../android/net/ipsec/ike/ChildSessionParams.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/net/ipsec/ike/ChildSessionParams.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ChildSaProposal](../android/net/ipsec/ike/ChildSaProposal.md)!> | [getChildSaProposals](../android/net/ipsec/ike/ChildSessionParams.md))`()` <br /> Retrieves all ChildSaProposals configured <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHardLifetimeSeconds](../android/net/ipsec/ike/ChildSessionParams.md))`()` <br /> Retrieves hard lifetime in seconds <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [IkeTrafficSelector](../android/net/ipsec/ike/IkeTrafficSelector.md)!> | [getInboundTrafficSelectors](../android/net/ipsec/ike/ChildSessionParams.md))`()` <br /> Retrieves configured inbound traffic selectors @see [android.net.ipsec.ike.TunnelModeChildSessionParams.Builder#addInboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector)](../android/net/ipsec/ike/TunnelModeChildSessionParams.Builder.md))or [android.net.ipsec.ike.TransportModeChildSessionParams.Builder#addInboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector)](../android/net/ipsec/ike/TransportModeChildSessionParams.Builder.md)) <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [IkeTrafficSelector](../android/net/ipsec/ike/IkeTrafficSelector.md)!> | [getOutboundTrafficSelectors](../android/net/ipsec/ike/ChildSessionParams.md))`()` <br /> Retrieves configured outbound traffic selectors @see [android.net.ipsec.ike.TunnelModeChildSessionParams.Builder#addOutboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector)](../android/net/ipsec/ike/TunnelModeChildSessionParams.Builder.md))or [android.net.ipsec.ike.TransportModeChildSessionParams.Builder#addOutboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector)](../android/net/ipsec/ike/TransportModeChildSessionParams.Builder.md)) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSoftLifetimeSeconds](../android/net/ipsec/ike/ChildSessionParams.md))`()` <br /> Retrieves soft lifetime in seconds <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/net/ipsec/ike/ChildSessionParams.md))`()` <br /> | ||
