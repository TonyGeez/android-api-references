# Ikev2VpnProfile

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Ikev2VpnProfile

Kotlin| [Java](../android/net/Ikev2VpnProfile.md) 
| --- | --- |

```
class Ikev2VpnProfile : PlatformVpnProfile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.net.PlatformVpnProfile](../android/net/PlatformVpnProfile.md) ||
| | ↳ | [android.net.Ikev2VpnProfile](../android/net/Ikev2VpnProfile.md) |

The Ikev2VpnProfile is a configuration for the platform setup of IKEv2/IPsec VPNs.

Together with VpnManager, this allows apps to provision IKEv2/IPsec VPNs that do not require the VPN app to constantly run in the background.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/net/Ikev2VpnProfile.Builder.md) A incremental builder for IKEv2 VPN profiles |

| Inherited constants ||
|---|---|
| From class [PlatformVpnProfile](../android/net/PlatformVpnProfile.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_IKEV2_IPSEC_PSK](../android/net/PlatformVpnProfile.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_IKEV2_IPSEC_RSA](../android/net/PlatformVpnProfile.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_IKEV2_IPSEC_USER_PASS](../android/net/PlatformVpnProfile.md) <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/net/Ikev2VpnProfile.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getAllowedAlgorithms](../android/net/Ikev2VpnProfile.md))`()` Returns all the algorithms allowed by this VPN profile. |
| [IkeTunnelConnectionParams](../android/net/ipsec/ike/IkeTunnelConnectionParams.md)? | [getIkeTunnelConnectionParams](../android/net/Ikev2VpnProfile.md))`()` Retrieves the ikeTunnelConnectionParams contains IKEv2 configurations, if any was set. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxMtu](../android/net/Ikev2VpnProfile.md))`()` Retrieves the maximum MTU set for this VPN profile. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPassword](../android/net/Ikev2VpnProfile.md))`()` Retrieves the password. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getPresharedKey](../android/net/Ikev2VpnProfile.md))`()` Retrieves the pre-shared key. |
| --- | --- |
| [ProxyInfo](../android/net/ProxyInfo.md)? | [getProxyInfo](../android/net/Ikev2VpnProfile.md))`()` Retrieves the proxy information if any was set |
| [PrivateKey](../java/security/PrivateKey.md)? | [getRsaPrivateKey](../android/net/Ikev2VpnProfile.md))`()` Retrieves the RSA private key. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getServerAddr](../android/net/Ikev2VpnProfile.md))`()` Retrieves the server address string. |
| --- | --- |
| [X509Certificate](../java/security/cert/X509Certificate.md)? | [getServerRootCaCert](../android/net/Ikev2VpnProfile.md))`()` Retrieves the certificate for the server's root CA. |
| [X509Certificate](../java/security/cert/X509Certificate.md)? | [getUserCert](../android/net/Ikev2VpnProfile.md))`()` Retrieves the user certificate, if any was set. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getUserIdentity](../android/net/Ikev2VpnProfile.md))`()` Retrieves the user identity. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getUsername](../android/net/Ikev2VpnProfile.md))`()` Retrieves the username. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/net/Ikev2VpnProfile.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutomaticIpVersionSelectionEnabled](../android/net/Ikev2VpnProfile.md))`()` Returns whether automatic IP version selection is enabled. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutomaticNattKeepaliveTimerEnabled](../android/net/Ikev2VpnProfile.md))`()` Returns whether automatic NAT-T keepalive timers are enabled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBypassable](../android/net/Ikev2VpnProfile.md))`()` Returns whether or not the VPN profile should be bypassable. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMetered](../android/net/Ikev2VpnProfile.md))`()` Returns whether or not the VPN profile should be always considered metered. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/net/Ikev2VpnProfile.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [PlatformVpnProfile](../android/net/PlatformVpnProfile.md) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areLocalRoutesExcluded](../android/net/PlatformVpnProfile.md))`()` <br /> Returns whether the local traffic is exempted from the VPN. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](../android/net/PlatformVpnProfile.md))`()` <br /> Returns the profile integer type. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTypeString](../android/net/PlatformVpnProfile.md))`()` <br /> Returns a type string describing the VPN profile type <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInternetValidationRequired](../android/net/PlatformVpnProfile.md))`()` <br /> Returns whether this VPN should undergo Internet validation. If this is true, the platform will perform basic validation checks for Internet connectivity over this VPN. If and when they succeed, the VPN network capabilities will reflect this by gaining the [NetworkCapabilities.NET_CAPABILITY_VALIDATED](../android/net/NetworkCapabilities.md) capability. If this is false, the platform assumes the VPN either is always capable of reaching the Internet or intends not to. In this case, the VPN network capabilities will always gain the [NetworkCapabilities.NET_CAPABILITY_VALIDATED](../android/net/NetworkCapabilities.md) capability immediately after it connects, whether it can reach public Internet destinations or not. <br /> | ||

## Public methods

### equals

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAllowedAlgorithms

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAllowedAlgorithms(): MutableList<String!>
```

Returns all the algorithms allowed by this VPN profile.

May be an empty list if the profile is built from an [IkeTunnelConnectionParams](../android/net/ipsec/ike/IkeTunnelConnectionParams.md).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. |

### getIkeTunnelConnectionParams

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIkeTunnelConnectionParams(): IkeTunnelConnectionParams?
```

Retrieves the ikeTunnelConnectionParams contains IKEv2 configurations, if any was set.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [IkeTunnelConnectionParams](../android/net/ipsec/ike/IkeTunnelConnectionParams.md)? | This value may be`null`. |

### getMaxMtu

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxMtu(): Int
```

Retrieves the maximum MTU set for this VPN profile. 

### getPassword

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPassword(): String?
```

Retrieves the password.

May be null if the profile is not using Username/Password authentication, or the profile is built from an [IkeTunnelConnectionParams](../android/net/ipsec/ike/IkeTunnelConnectionParams.md). 

### getPresharedKey

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPresharedKey(): ByteArray?
```

Retrieves the pre-shared key.

May be null if the profile is not using Pre-shared key authentication, or the profile is built from an [IkeTunnelConnectionParams](../android/net/ipsec/ike/IkeTunnelConnectionParams.md). 

### getProxyInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProxyInfo(): ProxyInfo?
```

Retrieves the proxy information if any was set

| Return ||
|------------------------------------------------------------------------------------|--------------------------|
| [ProxyInfo](../android/net/ProxyInfo.md)? | This value may be`null`. |

### getRsaPrivateKey

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRsaPrivateKey(): PrivateKey?
```

Retrieves the RSA private key.

May be null if the profile is not using RSA Digital Signature authentication, or the profile is built from an [IkeTunnelConnectionParams](../android/net/ipsec/ike/IkeTunnelConnectionParams.md). 

### getServerAddr

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServerAddr(): String
```

Retrieves the server address string.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getServerRootCaCert

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServerRootCaCert(): X509Certificate?
```

Retrieves the certificate for the server's root CA.

May be null if the profile is not using RSA Digital Signature Authentication or Username/Password authentication, or the profile is built from an [IkeTunnelConnectionParams](../android/net/ipsec/ike/IkeTunnelConnectionParams.md). 

### getUserCert

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserCert(): X509Certificate?
```

Retrieves the user certificate, if any was set.

May be null if the profile is built from an [IkeTunnelConnectionParams](../android/net/ipsec/ike/IkeTunnelConnectionParams.md). 

### getUserIdentity

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserIdentity(): String
```

Retrieves the user identity.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getUsername

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUsername(): String?
```

Retrieves the username.

May be null if the profile is not using Username/Password authentication, or the profile is built from an [IkeTunnelConnectionParams](../android/net/ipsec/ike/IkeTunnelConnectionParams.md). 

### hashCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isAutomaticIpVersionSelectionEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAutomaticIpVersionSelectionEnabled(): Boolean
```

Returns whether automatic IP version selection is enabled. 

### isAutomaticNattKeepaliveTimerEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAutomaticNattKeepaliveTimerEnabled(): Boolean
```

Returns whether automatic NAT-T keepalive timers are enabled. 

### isBypassable

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isBypassable(): Boolean
```

Returns whether or not the VPN profile should be bypassable. 

### isMetered

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isMetered(): Boolean
```

Returns whether or not the VPN profile should be always considered metered. 

### toString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
