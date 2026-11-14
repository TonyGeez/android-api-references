# Ikev2VpnProfile

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Ikev2VpnProfile

Kotlin| [Java](https://developer.android.com/reference/android/net/Ikev2VpnProfile "View this page in Java") 

```
class Ikev2VpnProfile : PlatformVpnProfile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.net.PlatformVpnProfile](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile) ||
| | ↳ | [android.net.Ikev2VpnProfile](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#) |

The Ikev2VpnProfile is a configuration for the platform setup of IKEv2/IPsec VPNs.

Together with VpnManager, this allows apps to provision IKEv2/IPsec VPNs that do not require the VPN app to constantly run in the background.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile.Builder) A incremental builder for IKEv2 VPN profiles |

| Inherited constants ||
|---|---|
| From class [PlatformVpnProfile](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_IKEV2_IPSEC_PSK](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile#TYPE_IKEV2_IPSEC_PSK:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_IKEV2_IPSEC_RSA](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile#TYPE_IKEV2_IPSEC_RSA:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_IKEV2_IPSEC_USER_PASS](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile#TYPE_IKEV2_IPSEC_USER_PASS:kotlin.Int) <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getAllowedAlgorithms](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#getAllowedAlgorithms())`()` Returns all the algorithms allowed by this VPN profile. |
| [IkeTunnelConnectionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeTunnelConnectionParams)? | [getIkeTunnelConnectionParams](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#getIkeTunnelConnectionParams())`()` Retrieves the ikeTunnelConnectionParams contains IKEv2 configurations, if any was set. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxMtu](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#getMaxMtu())`()` Retrieves the maximum MTU set for this VPN profile. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPassword](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#getPassword())`()` Retrieves the password. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getPresharedKey](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#getPresharedKey())`()` Retrieves the pre-shared key. |
| [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo)? | [getProxyInfo](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#getProxyInfo())`()` Retrieves the proxy information if any was set |
| [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)? | [getRsaPrivateKey](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#getRsaPrivateKey())`()` Retrieves the RSA private key. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getServerAddr](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#getServerAddr())`()` Retrieves the server address string. |
| [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)? | [getServerRootCaCert](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#getServerRootCaCert())`()` Retrieves the certificate for the server's root CA. |
| [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)? | [getUserCert](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#getUserCert())`()` Retrieves the user certificate, if any was set. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getUserIdentity](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#getUserIdentity())`()` Retrieves the user identity. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getUsername](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#getUsername())`()` Retrieves the username. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutomaticIpVersionSelectionEnabled](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#isAutomaticIpVersionSelectionEnabled())`()` Returns whether automatic IP version selection is enabled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutomaticNattKeepaliveTimerEnabled](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#isAutomaticNattKeepaliveTimerEnabled())`()` Returns whether automatic NAT-T keepalive timers are enabled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBypassable](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#isBypassable())`()` Returns whether or not the VPN profile should be bypassable. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMetered](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#isMetered())`()` Returns whether or not the VPN profile should be always considered metered. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile#toString())`()` <br /> |

| Inherited functions ||
|---|---|
| From class [PlatformVpnProfile](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areLocalRoutesExcluded](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile#areLocalRoutesExcluded())`()` <br /> Returns whether the local traffic is exempted from the VPN. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile#getType())`()` <br /> Returns the profile integer type. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTypeString](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile#getTypeString())`()` <br /> Returns a type string describing the VPN profile type <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInternetValidationRequired](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile#isInternetValidationRequired())`()` <br /> Returns whether this VPN should undergo Internet validation. If this is true, the platform will perform basic validation checks for Internet connectivity over this VPN. If and when they succeed, the VPN network capabilities will reflect this by gaining the [NetworkCapabilities.NET_CAPABILITY_VALIDATED](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_VALIDATED:kotlin.Int) capability. If this is false, the platform assumes the VPN either is always capable of reaching the Internet or intends not to. In this case, the VPN network capabilities will always gain the [NetworkCapabilities.NET_CAPABILITY_VALIDATED](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_VALIDATED:kotlin.Int) capability immediately after it connects, whether it can reach public Internet destinations or not. <br /> | ||

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

May be an empty list if the profile is built from an [IkeTunnelConnectionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeTunnelConnectionParams).

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
| [IkeTunnelConnectionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeTunnelConnectionParams)? | This value may be`null`. |

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

May be null if the profile is not using Username/Password authentication, or the profile is built from an [IkeTunnelConnectionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeTunnelConnectionParams). 

### getPresharedKey

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPresharedKey(): ByteArray?
```

Retrieves the pre-shared key.

May be null if the profile is not using Pre-shared key authentication, or the profile is built from an [IkeTunnelConnectionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeTunnelConnectionParams). 

### getProxyInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProxyInfo(): ProxyInfo?
```

Retrieves the proxy information if any was set

| Return ||
|------------------------------------------------------------------------------------|--------------------------|
| [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo)? | This value may be`null`. |

### getRsaPrivateKey

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRsaPrivateKey(): PrivateKey?
```

Retrieves the RSA private key.

May be null if the profile is not using RSA Digital Signature authentication, or the profile is built from an [IkeTunnelConnectionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeTunnelConnectionParams). 

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

May be null if the profile is not using RSA Digital Signature Authentication or Username/Password authentication, or the profile is built from an [IkeTunnelConnectionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeTunnelConnectionParams). 

### getUserCert

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserCert(): X509Certificate?
```

Retrieves the user certificate, if any was set.

May be null if the profile is built from an [IkeTunnelConnectionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeTunnelConnectionParams). 

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

May be null if the profile is not using Username/Password authentication, or the profile is built from an [IkeTunnelConnectionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeTunnelConnectionParams). 

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
