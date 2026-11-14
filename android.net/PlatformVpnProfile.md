# PlatformVpnProfile

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PlatformVpnProfile

Kotlin| [Java](https://developer.android.com/reference/android/net/PlatformVpnProfile "View this page in Java") 
| --- | --- |

```
abstract class PlatformVpnProfile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.PlatformVpnProfile](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile#) |

| Known Direct Subclasses [Ikev2VpnProfile](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile) |-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------| | [Ikev2VpnProfile](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile) | The Ikev2VpnProfile is a configuration for the platform setup of IKEv2/IPsec VPNs. | |
| --- | --- | --- | --- | --- | --- | --- |

PlatformVpnProfile represents a configuration for a platform-based VPN implementation.

Platform-based VPNs allow VPN applications to provide configuration and authentication options to leverage the Android OS' implementations of well-defined control plane (authentication, key negotiation) and data plane (per-packet encryption) protocols to simplify the creation of VPN tunnels. In contrast, [VpnService](https://developer.android.com/reference/kotlin/android/net/VpnService) based VPNs must implement both the control and data planes on a per-app basis.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_IKEV2_IPSEC_PSK](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile#TYPE_IKEV2_IPSEC_PSK:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_IKEV2_IPSEC_RSA](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile#TYPE_IKEV2_IPSEC_RSA:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_IKEV2_IPSEC_USER_PASS](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile#TYPE_IKEV2_IPSEC_USER_PASS:kotlin.Int) <br /> |
| --- | --- |

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areLocalRoutesExcluded](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile#areLocalRoutesExcluded())`()` Returns whether the local traffic is exempted from the VPN. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile#getType())`()` Returns the profile integer type. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTypeString](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile#getTypeString())`()` Returns a type string describing the VPN profile type |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInternetValidationRequired](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile#isInternetValidationRequired())`()` Returns whether this VPN should undergo Internet validation. |

## Constants

### TYPE_IKEV2_IPSEC_PSK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_IKEV2_IPSEC_PSK: Int
```  

 Value: 7

### TYPE_IKEV2_IPSEC_RSA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_IKEV2_IPSEC_RSA: Int
```  

 Value: 8

### TYPE_IKEV2_IPSEC_USER_PASS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_IKEV2_IPSEC_USER_PASS: Int
```  

 Value: 6

## Public methods

### areLocalRoutesExcluded

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun areLocalRoutesExcluded(): Boolean
```

Returns whether the local traffic is exempted from the VPN. 

### getType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Returns the profile integer type.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.PlatformVpnProfile#TYPE_IKEV2_IPSEC_USER_PASS](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile#TYPE_IKEV2_IPSEC_USER_PASS:kotlin.Int), [android.net.PlatformVpnProfile#TYPE_IKEV2_IPSEC_PSK](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile#TYPE_IKEV2_IPSEC_PSK:kotlin.Int), or [android.net.PlatformVpnProfile#TYPE_IKEV2_IPSEC_RSA](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile#TYPE_IKEV2_IPSEC_RSA:kotlin.Int) |

### getTypeString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTypeString(): String
```

Returns a type string describing the VPN profile type

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### isInternetValidationRequired

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isInternetValidationRequired(): Boolean
```

Returns whether this VPN should undergo Internet validation. If this is true, the platform will perform basic validation checks for Internet connectivity over this VPN. If and when they succeed, the VPN network capabilities will reflect this by gaining the [NetworkCapabilities.NET_CAPABILITY_VALIDATED](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_VALIDATED:kotlin.Int) capability. If this is false, the platform assumes the VPN either is always capable of reaching the Internet or intends not to. In this case, the VPN network capabilities will always gain the [NetworkCapabilities.NET_CAPABILITY_VALIDATED](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#NET_CAPABILITY_VALIDATED:kotlin.Int) capability immediately after it connects, whether it can reach public Internet destinations or not.
