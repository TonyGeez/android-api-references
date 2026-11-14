# ChildSessionParams

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChildSessionParams

Kotlin| [Java](../android/net/ipsec/ike/ChildSessionParams.md) 
| --- | --- |

```
abstract class ChildSessionParams
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.ipsec.ike.ChildSessionParams](../android/net/ipsec/ike/ChildSessionParams.md) |

| Known Direct Subclasses [TransportModeChildSessionParams](../android/net/ipsec/ike/TransportModeChildSessionParams.md), [TunnelModeChildSessionParams](../android/net/ipsec/ike/TunnelModeChildSessionParams.md) |-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------| | [TransportModeChildSessionParams](../android/net/ipsec/ike/TransportModeChildSessionParams.md) | TransportModeChildSessionParams represents proposed configurations for negotiating a transport mode Child Session. | | [TunnelModeChildSessionParams](../android/net/ipsec/ike/TunnelModeChildSessionParams.md) | TunnelModeChildSessionParams represents proposed configurations for negotiating a tunnel mode Child Session. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

ChildSessionParams is an abstract class that represents proposed configurations for negotiating a Child Session.

Note that references to negotiated configurations will be held, and the same parameters will be reused during rekey. This includes SA Proposals, lifetimes and traffic selectors.

IKE library will send out KE payload only if user has configured one or more DH groups. The KE payload in a request will use the first DH group from the first user provided SA proposal (or the peer selected SA proposal if it's a rekey request). The KE payload in a response will depend on the SA proposal negotiation result.

When requesting the first Child Session in IKE AUTH, IKE library will not propose any DH group even if user has configured it, as per RFC 7296. When rekeying this child session, IKE library will accept DH groups that are configured in its ChildSessionParams. If after rekeying user needs to have the same DH group as that of the IKE Session, then they need to explicitly set the same DH Group in ChildSessionParams.

@see [TunnelModeChildSessionParams](../android/net/ipsec/ike/TunnelModeChildSessionParams.md) and [TransportModeChildSessionParams](../android/net/ipsec/ike/TransportModeChildSessionParams.md)

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/net/ipsec/ike/ChildSessionParams.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ChildSaProposal](../android/net/ipsec/ike/ChildSaProposal.md)!\> | [getChildSaProposals](../android/net/ipsec/ike/ChildSessionParams.md))`()` Retrieves all ChildSaProposals configured |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHardLifetimeSeconds](../android/net/ipsec/ike/ChildSessionParams.md))`()` Retrieves hard lifetime in seconds |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [IkeTrafficSelector](../android/net/ipsec/ike/IkeTrafficSelector.md)!\> | [getInboundTrafficSelectors](../android/net/ipsec/ike/ChildSessionParams.md))`()` Retrieves configured inbound traffic selectors |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [IkeTrafficSelector](../android/net/ipsec/ike/IkeTrafficSelector.md)!\> | [getOutboundTrafficSelectors](../android/net/ipsec/ike/ChildSessionParams.md))`()` Retrieves configured outbound traffic selectors |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSoftLifetimeSeconds](../android/net/ipsec/ike/ChildSessionParams.md))`()` Retrieves soft lifetime in seconds |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/net/ipsec/ike/ChildSessionParams.md))`()` <br /> |

## Public methods

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getChildSaProposals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChildSaProposals(): MutableList<ChildSaProposal!>
```

Retrieves all ChildSaProposals configured

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ChildSaProposal](../android/net/ipsec/ike/ChildSaProposal.md)!> | This value cannot be`null`. |

### getHardLifetimeSeconds

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHardLifetimeSeconds(): Int
```

Retrieves hard lifetime in seconds

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between android.net.ipsec.ike.ChildSessionParams#CHILD_HARD_LIFETIME_SEC_MINIMUM and android.net.ipsec.ike.ChildSessionParams#CHILD_HARD_LIFETIME_SEC_MAXIMUM inclusive |

### getInboundTrafficSelectors

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInboundTrafficSelectors(): MutableList<IkeTrafficSelector!>
```

Retrieves configured inbound traffic selectors

@see [android.net.ipsec.ike.TunnelModeChildSessionParams.Builder#addInboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector)](../android/net/ipsec/ike/TunnelModeChildSessionParams.Builder.md))or [android.net.ipsec.ike.TransportModeChildSessionParams.Builder#addInboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector)](../android/net/ipsec/ike/TransportModeChildSessionParams.Builder.md))

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [IkeTrafficSelector](../android/net/ipsec/ike/IkeTrafficSelector.md)!> | This value cannot be`null`. |

### getOutboundTrafficSelectors

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutboundTrafficSelectors(): MutableList<IkeTrafficSelector!>
```

Retrieves configured outbound traffic selectors

@see [android.net.ipsec.ike.TunnelModeChildSessionParams.Builder#addOutboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector)](../android/net/ipsec/ike/TunnelModeChildSessionParams.Builder.md))or [android.net.ipsec.ike.TransportModeChildSessionParams.Builder#addOutboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector)](../android/net/ipsec/ike/TransportModeChildSessionParams.Builder.md))

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [IkeTrafficSelector](../android/net/ipsec/ike/IkeTrafficSelector.md)!> | This value cannot be`null`. |

### getSoftLifetimeSeconds

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSoftLifetimeSeconds(): Int
```

Retrieves soft lifetime in seconds

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between android.net.ipsec.ike.ChildSessionParams#CHILD_SOFT_LIFETIME_SEC_MINIMUM and android.net.ipsec.ike.ChildSessionParams#CHILD_HARD_LIFETIME_SEC_MAXIMUM inclusive |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
