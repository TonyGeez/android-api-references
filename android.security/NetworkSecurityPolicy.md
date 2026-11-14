Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkSecurityPolicy

```
open class NetworkSecurityPolicy
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.NetworkSecurityPolicy](../android/security/NetworkSecurityPolicy.md) |

Network security policy.

Network stacks/components should honor this policy to make it possible to centrally control the relevant aspects of network security behavior.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy.Builder` A builder for a `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#DOMAIN_ENCRYPTION_MODE_DISABLED:kotlin.Int` Domain encryption is disabled for the app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#DOMAIN_ENCRYPTION_MODE_ENABLED:kotlin.Int` Domain encryption is in fully enabled mode for the app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#DOMAIN_ENCRYPTION_MODE_OPPORTUNISTIC:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#DOMAIN_ENCRYPTION_MODE_REQUIRED:kotlin.Int` Domain encryption is required for the app and should fail closed (i.e. if ECH cannot be enabled for any reason, the connection will fail). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#DOMAIN_ENCRYPTION_MODE_UNKNOWN:kotlin.Int` Unknown setting for domain encryption in the app. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#getDomainEncryptionMode(kotlin.String)(hostname: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns the domain encryption mode the app has chosen for the given `hostname`, including the setting for Encrypted Client Hello. |
| open static [NetworkSecurityPolicy](../android/security/NetworkSecurityPolicy.md) | `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#getInstance()()` Gets the policy for this process. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#isCertificateTransparencyVerificationRequired(kotlin.String)(hostname: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns `true` if Certificate Transparency information is required to be verified by the client in TLS connections to `hostname`. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#isCleartextTrafficPermitted()()` Returns whether cleartext network traffic (e.g. HTTP, FTP, WebSockets, XMPP, IMAP, SMTP -- without TLS or STARTTLS) is permitted for all network communication from this process. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#isCleartextTrafficPermitted(kotlin.String)(hostname: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns whether cleartext network traffic (e.g. HTTP, FTP, XMPP, IMAP, SMTP -- without TLS or STARTTLS) is permitted for communicating with |

## Constants

### DOMAIN_ENCRYPTION_MODE_DISABLED

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [C Extensions 22](https://developer.android.com/sdkExtensions)

```
static val DOMAIN_ENCRYPTION_MODE_DISABLED: Int
```

Domain encryption is disabled for the app. ECH and GREASE should not be used.

 Value: 1

### DOMAIN_ENCRYPTION_MODE_ENABLED

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [C Extensions 22](https://developer.android.com/sdkExtensions)

```
static val DOMAIN_ENCRYPTION_MODE_ENABLED: Int
```

Domain encryption is in fully enabled mode for the app. ECH will be enabled when there is server support, otherwise GREASE will be used.

 Value: 3

### DOMAIN_ENCRYPTION_MODE_OPPORTUNISTIC

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [C Extensions 22](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DOMAIN_ENCRYPTION_MODE_OPPORTUNISTIC: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#DOMAIN_ENCRYPTION_MODE_ENABLED:kotlin.Int` instead.*

 Value: 2

### DOMAIN_ENCRYPTION_MODE_REQUIRED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [C Extensions 24](https://developer.android.com/sdkExtensions)

```
static val DOMAIN_ENCRYPTION_MODE_REQUIRED: Int
```

Domain encryption is required for the app and should fail closed (i.e. if ECH cannot be enabled for any reason, the connection will fail).

If a valid ECH configuration is not available (e.g. because the DNS server does not return ECHConfigList in a SVCB/HTTPS record), connections will fail.

 Value: 4

### DOMAIN_ENCRYPTION_MODE_UNKNOWN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [C Extensions 22](https://developer.android.com/sdkExtensions)

```
static val DOMAIN_ENCRYPTION_MODE_UNKNOWN: Int
```

Unknown setting for domain encryption in the app.

This is the default value returned by `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#getDomainEncryptionMode(kotlin.String)` when not overridden. Network libraries should avoid performing any domain encryption and perform a standard TLS handshake, equivalent to `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#DOMAIN_ENCRYPTION_MODE_DISABLED:kotlin.Int`.

 Value: 0

## Public methods

### getDomainEncryptionMode

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [C Extensions 22](https://developer.android.com/sdkExtensions)

```
open fun getDomainEncryptionMode(hostname: String): Int
```

Returns the domain encryption mode the app has chosen for the given `hostname`, including the setting for Encrypted Client Hello.

| Parameters ||
|---|---|
| `hostname` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): hostname to check what domain encryption mode has been chosen by the app. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int representing the domain encryption mode. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#DOMAIN_ENCRYPTION_MODE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#DOMAIN_ENCRYPTION_MODE_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#DOMAIN_ENCRYPTION_MODE_OPPORTUNISTIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#DOMAIN_ENCRYPTION_MODE_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#DOMAIN_ENCRYPTION_MODE_REQUIRED:kotlin.Int` |

### getInstance

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(): NetworkSecurityPolicy
```

Gets the policy for this process.

It's fine to cache this reference. Any changes to the policy will be immediately visible through the reference.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#` | This value cannot be `null`. |

### isCertificateTransparencyVerificationRequired

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isCertificateTransparencyVerificationRequired(hostname: String): Boolean
```

Returns `true` if Certificate Transparency information is required to be verified by the client in TLS connections to `hostname`.

See RFC6962 section 3.3 for more details.

| Parameters ||
|---|---|
| `hostname` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): hostname to check whether certificate transparency verification is required. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if certificate transparency verification is required and `false` otherwise |

### isCleartextTrafficPermitted

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isCleartextTrafficPermitted(): Boolean
```

Returns whether cleartext network traffic (e.g. HTTP, FTP, WebSockets, XMPP, IMAP, SMTP -- without TLS or STARTTLS) is permitted for all network communication from this process.

When cleartext network traffic is not permitted, the platform's components (e.g. HTTP and FTP stacks, `https://developer.android.com/reference/kotlin/android/app/DownloadManager.html#`, `https://developer.android.com/reference/kotlin/android/media/MediaPlayer.html#`) will refuse this process's requests to use cleartext traffic. Third-party libraries are strongly encouraged to honor this setting as well.

This flag is honored on a best effort basis because it's impossible to prevent all cleartext traffic from Android applications given the level of access provided to them. For example, there's no expectation that the `https://developer.android.com/reference/kotlin/java/net/Socket.html#` API will honor this flag because it cannot determine whether its traffic is in cleartext. However, most network traffic from applications is handled by higher-level network stacks/components which can honor this aspect of the policy.

NOTE: `https://developer.android.com/reference/kotlin/android/webkit/WebView.html#` honors this flag for applications targeting API level 26 and up.

### isCleartextTrafficPermitted

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isCleartextTrafficPermitted(hostname: String?): Boolean
```

Returns whether cleartext network traffic (e.g. HTTP, FTP, XMPP, IMAP, SMTP -- without TLS or STARTTLS) is permitted for communicating with `hostname` for this process.

| Parameters ||
|---|---|
| `hostname` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/security/NetworkSecurityPolicy#isCleartextTrafficPermitted()`
