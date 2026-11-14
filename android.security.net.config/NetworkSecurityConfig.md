Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [C Extensions 24](https://developer.android.com/sdkExtensions)

# NetworkSecurityConfig

```
class NetworkSecurityConfig
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.net.config.NetworkSecurityConfig](NetworkSecurityConfig.md) |

The security configuration to use when performing network communications.

A NetworkSecurityConfig can specify security requirements for all network communications, or for communications with a specific domain or localhost connections.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/security/net/config/NetworkSecurityConfig.Builder` Builder for creating `NetworkSecurityConfig` objects. |

| Public methods ||
|---|---|
| static [NetworkSecurityConfig](NetworkSecurityConfig.md)? | createBaseConfig Returns a base NetworkSecurityConfig using the provided app's defaults. |
| static [NetworkSecurityConfig](NetworkSecurityConfig.md) | createLocalhostConfig Returns a NetworkSecurityConfig for localhost. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDomainEncryptionMode <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isCertificateTransparencyVerificationRequired <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isCleartextTrafficPermitted <br /> |

## Public methods

### createBaseConfig

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [C Extensions 24](https://developer.android.com/sdkExtensions)

```
static fun createBaseConfig(context: Context): NetworkSecurityConfig?
```

Returns a base NetworkSecurityConfig using the provided app's defaults.

An app default configuration has the following properties:

1. If the application targets API level 27 (Android O MR1) or lower, cleartext traffic is allowed by default.
2. Cleartext traffic is not permitted for ephemeral apps.
3. No certificate pinning is used.
4. The system certificate store is trusted for connections.
5. If the application targets API level 23 (Android M) or lower than the user certificate store is trusted by default as well for non-privileged applications.
6. Privileged applications do not trust the user certificate store on Android P and higher.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): of the application. Must not be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/security/net/config/NetworkSecurityConfig#?` | the application NetworkSecurityConfig, or `null` if the config cannot be found. |

### createLocalhostConfig

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [C Extensions 24](https://developer.android.com/sdkExtensions)

```
static fun createLocalhostConfig(): NetworkSecurityConfig
```

Returns a NetworkSecurityConfig for localhost.

The localhost configuration has the following properties:

1. Cleartext traffic is permitted.
2. Certificate Transparency is disabled.

| Return ||
|---|---|
| NetworkSecurityConfig | the NetworkSecurityConfig. This value cannot be `null`. |

### getDomainEncryptionMode

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [C Extensions 24](https://developer.android.com/sdkExtensions)

```
fun getDomainEncryptionMode(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the domain encryption mode. For possible values see getDomainEncryptionMode. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy.html#DOMAIN_ENCRYPTION_MODE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy.html#DOMAIN_ENCRYPTION_MODE_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy.html#DOMAIN_ENCRYPTION_MODE_OPPORTUNISTIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy.html#DOMAIN_ENCRYPTION_MODE_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy.html#DOMAIN_ENCRYPTION_MODE_REQUIRED:kotlin.Int` |

### isCertificateTransparencyVerificationRequired

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [C Extensions 24](https://developer.android.com/sdkExtensions)

```
fun isCertificateTransparencyVerificationRequired(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if Certificate Transparency is required for this NetworkSecurityConfig. |

### isCleartextTrafficPermitted

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [C Extensions 24](https://developer.android.com/sdkExtensions)

```
fun isCleartextTrafficPermitted(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if cleartext traffic is permitted for this NetworkSecurityConfig. |
