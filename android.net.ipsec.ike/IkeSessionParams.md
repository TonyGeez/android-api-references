Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeSessionParams

```
class IkeSessionParams
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.ipsec.ike.IkeSessionParams](../android/net/ipsec/ike/IkeSessionParams.md) |

IkeSessionParams contains all user provided configurations for negotiating an `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession`.

Note that all negotiated configurations will be reused during rekey including SA Proposal and lifetime.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams.Builder` This class can be used to incrementally construct a `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#`. |
| abstract | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams.IkeAuthConfig` This class contains common information of an IKEv2 authentication configuration. |
| | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams.IkeAuthDigitalSignLocalConfig` This class represents the configuration to support IKEv2 public-key-signature-based authentication of the local side. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams.IkeAuthDigitalSignRemoteConfig` This class represents the configuration to support IKEv2 public-key-signature-based authentication of the remote side. |
| | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams.IkeAuthEapConfig` This class represents the configuration to support EAP authentication of the local side. |
| | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams.IkeAuthPskConfig` This class represents the configuration to support IKEv2 pre-shared-key-based authentication of local or remote side. |
| --- | --- |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#IKE_DPD_DELAY_SEC_DISABLED:kotlin.Int` Setting timer to this value will disable the Dead Peer Detection(DPD). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#IKE_OPTION_ACCEPT_ANY_REMOTE_ID:kotlin.Int` If set, the IKE library will accept any remote (server) identity, even if it does not match the configured remote identity |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#IKE_OPTION_EAP_ONLY_AUTH:kotlin.Int` If set, and EAP has been configured as the authentication method, the IKE library will request that the remote (also) use an EAP-only authentication flow. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#IKE_OPTION_FORCE_PORT_4500:kotlin.Int` Configures the IKE session to always send to port 4500. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#IKE_OPTION_INITIAL_CONTACT:kotlin.Int` If set, the IKE library will send INITIAL_CONTACT notification to the peers. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#IKE_OPTION_MOBIKE:kotlin.Int` If set, the IKE Session will attempt to handle IP address changes using RFC4555 MOBIKE. |
| --- | --- |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#getDpdDelaySeconds()()` Retrieves the Dead Peer Detection(DPD) delay in seconds |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#getHardLifetimeSeconds()()` Retrieves hard lifetime in seconds |
| --- | --- |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#getIkeOptions()()` Return all the enabled IKE Options |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [IkeSaProposal](../android/net/ipsec/ike/IkeSaProposal.md)!\> | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#getIkeSaProposals()()` Retrieves all IkeSaProposals configured |
| [IkeSessionParams.IkeAuthConfig](../android/net/ipsec/ike/IkeSessionParams.IkeAuthConfig.md) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#getLocalAuthConfig()()` Retrieves the local (client) authentication configuration |
| --- | --- |
| [IkeIdentification](../android/net/ipsec/ike/IkeIdentification.md) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#getLocalIdentification()()` Retrieves the local (client) identity |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#getNattKeepAliveDelaySeconds()()` Retrieves the Network Address Translation Traversal (NATT) keepalive delay in seconds |
| [Network](../android/net/Network.md)? | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#getNetwork()()` Retrieves the configured `https://developer.android.com/reference/kotlin/android/net/Network.html#`, or null if was not set. |
| --- | --- |
| [IkeSessionParams.IkeAuthConfig](../android/net/ipsec/ike/IkeSessionParams.IkeAuthConfig.md) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#getRemoteAuthConfig()()` Retrieves the remote (server) authentication configuration |
| [IkeIdentification](../android/net/ipsec/ike/IkeIdentification.md) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#getRemoteIdentification()()` Retrieves the required remote (server) identity |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#getRetransmissionTimeoutsMillis()()` Retrieves the relative retransmission timeout list in milliseconds |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#getServerHostname()()` Retrieves the configured server hostname |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#getSoftLifetimeSeconds()()` Retrieves soft lifetime in seconds |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#hasIkeOption(kotlin.Int)(ikeOption: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Checks if the given IKE Session negotiation option is set |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#hashCode()()` Returns a hash code value for the object. |

## Constants

### IKE_DPD_DELAY_SEC_DISABLED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IKE_DPD_DELAY_SEC_DISABLED: Int
```

Setting timer to this value will disable the Dead Peer Detection(DPD).

@see `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams.Builder#setDpdDelaySeconds(kotlin.Int)`

 Value: 2147483647

### IKE_OPTION_ACCEPT_ANY_REMOTE_ID

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IKE_OPTION_ACCEPT_ANY_REMOTE_ID: Int
```

If set, the IKE library will accept any remote (server) identity, even if it does not match the configured remote identity

See `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams.Builder#setRemoteIdentification(android.net.ipsec.ike.IkeIdentification)`

 Value: 0

### IKE_OPTION_EAP_ONLY_AUTH

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IKE_OPTION_EAP_ONLY_AUTH: Int
```

If set, and EAP has been configured as the authentication method, the IKE library will request that the remote (also) use an EAP-only authentication flow.

@see `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams.Builder#setAuthEap(java.security.cert.X509Certificate,%20android.net.eap.EapSessionConfig)`

 Value: 1

### IKE_OPTION_FORCE_PORT_4500

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IKE_OPTION_FORCE_PORT_4500: Int
```

Configures the IKE session to always send to port 4500.

If set, the IKE Session will be initiated and maintained exclusively using destination port 4500, regardless of the presence of NAT. Otherwise, the IKE Session will be initiated on destination port 500; then, if either a NAT is detected or both MOBIKE and NAT-T are supported by the peer, it will proceed on port 4500.

 Value: 3

### IKE_OPTION_INITIAL_CONTACT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IKE_OPTION_INITIAL_CONTACT: Int
```

If set, the IKE library will send INITIAL_CONTACT notification to the peers.

If this option is set, the INITIAL_CONTACT notification payload is sent in IKE_AUTH. The client can use this option to assert to the peer that this IKE SA is the only IKE SA currently active between the authenticated identities.

@see "https://tools.ietf.org/html/rfc7296#section-2.4" RFC 7296, Internet Key Exchange Protocol Version 2 (IKEv2)

@see `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams.Builder#addIkeOption(kotlin.Int)`

 Value: 4

### IKE_OPTION_MOBIKE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IKE_OPTION_MOBIKE: Int
```

If set, the IKE Session will attempt to handle IP address changes using RFC4555 MOBIKE.

Upon IP address changes (including Network changes), the IKE session will initiate an RFC 4555 MOBIKE procedure, migrating both this IKE Session and associated IPsec Transforms to the new local and remote address pair.

The IKE library will first attempt to enable MOBIKE to handle the changes of underlying network and addresses. For callers targeting SDK `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S_V2:kotlin.Int` and earlier, this option will implicitly enable the support for rekey-based mobility, and thus if the server does not support MOBIKE, the IKE Session will try migration by rekeying all associated IPsec SAs. This rekey-based mobility feature is not best-practice and has technical issues; accordingly, it will no longer be enabled for callers targeting SDK `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` and above.

Checking whether or not MOBIKE is supported by both the IKE library and the server in an IKE Session is done via `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConfiguration#isIkeExtensionEnabled(kotlin.Int)`.

It is recommended that IKE_OPTION_MOBIKE be enabled unless precluded for compatibility reasons.

If this option is set for an IKE Session, Transport-mode SAs will not be allowed in that Session.

Callers that need to perform migration of IPsec transforms and tunnels MUST implement migration specific methods in `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback` and `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback`.

 Value: 2

## Public methods

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getDpdDelaySeconds

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDpdDelaySeconds(): Int
```

Retrieves the Dead Peer Detection(DPD) delay in seconds

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is #IKE_DPD_DELAY_SEC_MIN or greater |

### getHardLifetimeSeconds

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHardLifetimeSeconds(): Int
```

Retrieves hard lifetime in seconds

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is between #IKE_HARD_LIFETIME_SEC_MINIMUM and #IKE_HARD_LIFETIME_SEC_MAXIMUM inclusive |

### getIkeOptions

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIkeOptions(): MutableSet<Int!>
```

Return all the enabled IKE Options

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | A Set of enabled IKE options that have been added using `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams.Builder#addIkeOption(kotlin.Int)` This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#IKE_OPTION_ACCEPT_ANY_REMOTE_ID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#IKE_OPTION_EAP_ONLY_AUTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#IKE_OPTION_MOBIKE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#IKE_OPTION_FORCE_PORT_4500:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#IKE_OPTION_INITIAL_CONTACT:kotlin.Int` |

### getIkeSaProposals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIkeSaProposals(): MutableList<IkeSaProposal!>
```

Retrieves all IkeSaProposals configured

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSaProposal!>` | This value cannot be `null`. |

### getLocalAuthConfig

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLocalAuthConfig(): IkeSessionParams.IkeAuthConfig
```

Retrieves the local (client) authentication configuration

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams.IkeAuthConfig` | This value cannot be `null`. |

### getLocalIdentification

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLocalIdentification(): IkeIdentification
```

Retrieves the local (client) identity

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIdentification` | This value cannot be `null`. |

### getNattKeepAliveDelaySeconds

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNattKeepAliveDelaySeconds(): Int
```

Retrieves the Network Address Translation Traversal (NATT) keepalive delay in seconds

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is between #IKE_NATT_KEEPALIVE_DELAY_SEC_MIN and #IKE_NATT_KEEPALIVE_DELAY_SEC_MAX inclusive |

### getNetwork

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNetwork(): Network?
```

Retrieves the configured `https://developer.android.com/reference/kotlin/android/net/Network.html#`, or null if was not set.

@see `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams.Builder#setNetwork(android.net.Network)`

### getRemoteAuthConfig

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRemoteAuthConfig(): IkeSessionParams.IkeAuthConfig
```

Retrieves the remote (server) authentication configuration

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams.IkeAuthConfig` | This value cannot be `null`. |

### getRemoteIdentification

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRemoteIdentification(): IkeIdentification
```

Retrieves the required remote (server) identity

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIdentification` | This value cannot be `null`. |

### getRetransmissionTimeoutsMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRetransmissionTimeoutsMillis(): IntArray
```

Retrieves the relative retransmission timeout list in milliseconds

@see `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams.Builder#setRetransmissionTimeoutsMillis(kotlin.IntArray)`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | This value cannot be `null`. |

### getServerHostname

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getServerHostname(): String
```

Retrieves the configured server hostname

The configured server hostname will be resolved during IKE Session creation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getSoftLifetimeSeconds

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSoftLifetimeSeconds(): Int
```

Retrieves soft lifetime in seconds

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is between #IKE_SOFT_LIFETIME_SEC_MINIMUM and #IKE_HARD_LIFETIME_SEC_MAXIMUM inclusive |

### hasIkeOption

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasIkeOption(ikeOption: Int): Boolean
```

Checks if the given IKE Session negotiation option is set

| Parameters ||
|---|---|
| `ikeOption` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the option to check. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#IKE_OPTION_ACCEPT_ANY_REMOTE_ID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#IKE_OPTION_EAP_ONLY_AUTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#IKE_OPTION_MOBIKE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#IKE_OPTION_FORCE_PORT_4500:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams#IKE_OPTION_INITIAL_CONTACT:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the provided option is invalid. |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |
