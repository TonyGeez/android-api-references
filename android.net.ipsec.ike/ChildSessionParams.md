# ChildSessionParams

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChildSessionParams

Kotlin| [Java](https://developer.android.com/reference/android/net/ipsec/ike/ChildSessionParams "View this page in Java") 

```
abstract class ChildSessionParams
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.ipsec.ike.ChildSessionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams#) |

| Known Direct Subclasses [TransportModeChildSessionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TransportModeChildSessionParams), [TunnelModeChildSessionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams) |-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------| | [TransportModeChildSessionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TransportModeChildSessionParams) | TransportModeChildSessionParams represents proposed configurations for negotiating a transport mode Child Session. | | [TunnelModeChildSessionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams) | TunnelModeChildSessionParams represents proposed configurations for negotiating a tunnel mode Child Session. | |

ChildSessionParams is an abstract class that represents proposed configurations for negotiating a Child Session.

Note that references to negotiated configurations will be held, and the same parameters will be reused during rekey. This includes SA Proposals, lifetimes and traffic selectors.

IKE library will send out KE payload only if user has configured one or more DH groups. The KE payload in a request will use the first DH group from the first user provided SA proposal (or the peer selected SA proposal if it's a rekey request). The KE payload in a response will depend on the SA proposal negotiation result.

When requesting the first Child Session in IKE AUTH, IKE library will not propose any DH group even if user has configured it, as per RFC 7296. When rekeying this child session, IKE library will accept DH groups that are configured in its ChildSessionParams. If after rekeying user needs to have the same DH group as that of the IKE Session, then they need to explicitly set the same DH Group in ChildSessionParams.

@see [TunnelModeChildSessionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams) and [TransportModeChildSessionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TransportModeChildSessionParams)

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ChildSaProposal](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSaProposal)!\> | [getChildSaProposals](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams#getChildSaProposals())`()` Retrieves all ChildSaProposals configured |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHardLifetimeSeconds](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams#getHardLifetimeSeconds())`()` Retrieves hard lifetime in seconds |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [IkeTrafficSelector](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeTrafficSelector)!\> | [getInboundTrafficSelectors](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams#getInboundTrafficSelectors())`()` Retrieves configured inbound traffic selectors |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [IkeTrafficSelector](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeTrafficSelector)!\> | [getOutboundTrafficSelectors](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams#getOutboundTrafficSelectors())`()` Retrieves configured outbound traffic selectors |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSoftLifetimeSeconds](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams#getSoftLifetimeSeconds())`()` Retrieves soft lifetime in seconds |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams#hashCode())`()` <br /> |

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
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ChildSaProposal](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSaProposal)!> | This value cannot be`null`. |

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

@see [android.net.ipsec.ike.TunnelModeChildSessionParams.Builder#addInboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector)](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.Builder#addInboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector))or [android.net.ipsec.ike.TransportModeChildSessionParams.Builder#addInboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector)](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TransportModeChildSessionParams.Builder#addInboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector))

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [IkeTrafficSelector](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeTrafficSelector)!> | This value cannot be`null`. |

### getOutboundTrafficSelectors

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutboundTrafficSelectors(): MutableList<IkeTrafficSelector!>
```

Retrieves configured outbound traffic selectors

@see [android.net.ipsec.ike.TunnelModeChildSessionParams.Builder#addOutboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector)](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.Builder#addOutboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector))or [android.net.ipsec.ike.TransportModeChildSessionParams.Builder#addOutboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector)](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TransportModeChildSessionParams.Builder#addOutboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector))

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [IkeTrafficSelector](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeTrafficSelector)!> | This value cannot be`null`. |

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
