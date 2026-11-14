Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyChainManager

```
class KeyChainManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.security.KeyChainManager](https://developer.android.com/reference/kotlin/android/security/KeyChainManager#) |

Manages KeyChain certificates and grants.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyChainManager#KEYPAIR_SCOPE_DEVICE:kotlin.Int` Scope indicating the key pair is installed device-wide and is visible to all affiliated users on the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyChainManager#KEYPAIR_SCOPE_USER:kotlin.Int` Scope indicating the key pair is installed for the current user only. |

| Public methods ||
|---|---|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!\> | `https://developer.android.com/reference/kotlin/android/security/KeyChainManager#getCertificateChain(kotlin.String,%20kotlin.Int)(alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, scope: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the certificate chain of the given scoped certificate. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [GrantedKeyInfo](https://developer.android.com/reference/kotlin/android/security/GrantedKeyInfo)!\> | `https://developer.android.com/reference/kotlin/android/security/KeyChainManager#getGrantedKeyPairs(kotlin.Int)(scope: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a list of granted keys that the calling app has access to for the specified scope. |
| [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)? | `https://developer.android.com/reference/kotlin/android/security/KeyChainManager#getPrivateKey(kotlin.String,%20kotlin.Int)(alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, scope: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the private key for the given alias and scope. |

## Constants

### KEYPAIR_SCOPE_DEVICE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYPAIR_SCOPE_DEVICE: Int
```

Scope indicating the key pair is installed device-wide and is visible to all affiliated users on the device.

 Value: 1

### KEYPAIR_SCOPE_USER

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEYPAIR_SCOPE_USER: Int
```

Scope indicating the key pair is installed for the current user only. This is the default scope for existing KeyChain credentials.

 Value: 2

## Public methods

### getCertificateChain

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCertificateChain(
    alias: String, 
    scope: Int
): MutableList<X509Certificate!>
```

Returns the certificate chain of the given scoped certificate. Callable by the application that installed the certificate, any app that has been granted access to the given alias, as well as DPCs and their delegates.

| Parameters ||
|---|---|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The alias of the desired certificate chain. This value cannot be `null`. |
| `scope` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The scope to search (`https://developer.android.com/reference/kotlin/android/security/KeyChainManager#KEYPAIR_SCOPE_USER:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/security/KeyChainManager#KEYPAIR_SCOPE_DEVICE:kotlin.Int`). Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/KeyChainManager#KEYPAIR_SCOPE_USER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/KeyChainManager#KEYPAIR_SCOPE_DEVICE:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#!>` | The list of `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#`s representing the chain, or an empty list if no certificate exists for the given alias/scope or if access to the key is not granted. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `scope` is invalid. |

### getGrantedKeyPairs

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getGrantedKeyPairs(scope: Int): MutableList<GrantedKeyInfo!>
```

Returns a list of granted keys that the calling app has access to for the specified scope.

| Parameters ||
|---|---|
| `scope` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The scope of the key pair: `https://developer.android.com/reference/kotlin/android/security/KeyChainManager#KEYPAIR_SCOPE_USER:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/security/KeyChainManager#KEYPAIR_SCOPE_DEVICE:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/KeyChainManager#KEYPAIR_SCOPE_USER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/KeyChainManager#KEYPAIR_SCOPE_DEVICE:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/security/GrantedKeyInfo!>` | A non-null list of `https://developer.android.com/reference/kotlin/android/security/GrantedKeyInfo` objects. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `scope` is invalid. |

### getPrivateKey

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPrivateKey(
    alias: String, 
    scope: Int
): PrivateKey?
```

Returns the private key for the given alias and scope. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The alias of the desired key pair. This value cannot be `null`. |
| `scope` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The scope to search (`https://developer.android.com/reference/kotlin/android/security/KeyChainManager#KEYPAIR_SCOPE_USER:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/security/KeyChainManager#KEYPAIR_SCOPE_DEVICE:kotlin.Int`). Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/KeyChainManager#KEYPAIR_SCOPE_USER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/KeyChainManager#KEYPAIR_SCOPE_DEVICE:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#?` | The `https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#`, or `null` if no key exists for the given alias/scope or if access to the key is not granted. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `scope` is invalid. |
