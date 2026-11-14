Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyChain

```
class KeyChain
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.security.KeyChain](https://developer.android.com/reference/kotlin/android/security/KeyChain#) |

The `KeyChain` class provides access to private keys and their corresponding certificate chains in credential storage.

Applications accessing the `KeyChain` normally go through these steps:

1. Receive a callback from an `https://developer.android.com/reference/kotlin/javax/net/ssl/X509KeyManager.html#` that a private key is requested.
2. Call #choosePrivateKeyAlias to allow the user to select from a list of currently available private keys and corresponding certificate chains. The chosen alias will be returned by the callback `https://developer.android.com/reference/kotlin/android/security/KeyChainAliasCallback#alias(kotlin.String)`, or null if no private key is available or the user cancels the request.
3. Call `https://developer.android.com/reference/kotlin/android/security/KeyChain#getPrivateKey(android.content.Context,%20kotlin.String)` and `https://developer.android.com/reference/kotlin/android/security/KeyChain#getCertificateChain(android.content.Context,%20kotlin.String)` to retrieve the credentials to return to the corresponding `https://developer.android.com/reference/kotlin/javax/net/ssl/X509KeyManager.html#` callbacks.

An application may remember the value of a selected alias to avoid prompting the user with #choosePrivateKeyAlias on subsequent connections. If the alias is no longer valid, null will be returned on lookups using that value

An application can request the installation of private keys and certificates via the `Intent` provided by `https://developer.android.com/reference/kotlin/android/security/KeyChain#createInstallIntent()`. Private keys installed via this `Intent` will be accessible via #choosePrivateKeyAlias while Certificate Authority (CA) certificates will be trusted by all applications through the default `X509TrustManager`.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#ACTION_KEYCHAIN_CHANGED:kotlin.String` Broadcast Action: Indicates the contents of the keychain has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#ACTION_KEY_ACCESS_CHANGED:kotlin.String` Broadcast Action: Indicates that the access permissions for a private key have changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#ACTION_STORAGE_CHANGED:kotlin.String` Broadcast Action: Indicates the trusted storage has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#ACTION_TRUST_STORE_CHANGED:kotlin.String` Broadcast Action: Indicates the contents of the trusted certificate store has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#EXTRA_CERTIFICATE:kotlin.String` Optional extra to specify an X. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#EXTRA_KEY_ACCESSIBLE:kotlin.String` Used as a boolean extra field in `https://developer.android.com/reference/kotlin/android/security/KeyChain#ACTION_KEY_ACCESS_CHANGED:kotlin.String` to supply if the key is accessible to the application. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#EXTRA_KEY_ALIAS:kotlin.String` Used as a String extra field in `https://developer.android.com/reference/kotlin/android/security/KeyChain#ACTION_KEY_ACCESS_CHANGED:kotlin.String` to supply the alias of the key. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#EXTRA_NAME:kotlin.String` Optional extra to specify a `String` credential name on the `Intent` returned by `https://developer.android.com/reference/kotlin/android/security/KeyChain#createInstallIntent()`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#EXTRA_PKCS12:kotlin.String` Optional extra for use with the `Intent` returned by `https://developer.android.com/reference/kotlin/android/security/KeyChain#createInstallIntent()` to specify a PKCS#12 key store to install. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#KEY_ALIAS_SELECTION_DENIED:kotlin.String` Used by DPC or delegated app in `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver.html#onChoosePrivateKeyAlias(android.content.Context,%20android.content.Intent,%20kotlin.Int,%20android.net.Uri,%20kotlin.String)` or `https://developer.android.com/reference/kotlin/android/app/admin/DelegatedAdminReceiver.html#onChoosePrivateKeyAlias(android.content.Context,%20android.content.Intent,%20kotlin.Int,%20android.net.Uri,%20kotlin.String)` to identify that the requesting app is not granted access to any key, and nor will the user be able to grant access manually. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/security/KeyChain#KeyChain()()` <br /> |

| Public methods ||
|---|---|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#choosePrivateKeyAlias(android.app.Activity,%20android.security.KeyChainAliasCallback,%20kotlin.Array,%20kotlin.Array,%20android.net.Uri,%20kotlin.String)(activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#, response: https://developer.android.com/reference/kotlin/android/security/KeyChainAliasCallback, keyTypes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, issuers: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/security/Principal.html#!>?, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?, alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Launches an `Activity` for the user to select the alias for a private key and certificate pair for authentication. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#choosePrivateKeyAlias(android.app.Activity,%20android.security.KeyChainAliasCallback,%20kotlin.Array,%20kotlin.Array,%20kotlin.String,%20kotlin.Int,%20kotlin.String)(activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#, response: https://developer.android.com/reference/kotlin/android/security/KeyChainAliasCallback, keyTypes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?, issuers: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/security/Principal.html#!>?, host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Launches an `Activity` for the user to select the alias for a private key and certificate pair for authentication. |
| static [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#createInstallIntent()()` Returns an `Intent` that can be used for credential installation. |
| static [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#createManageCredentialsIntent(android.security.AppUriAuthenticationPolicy)(policy: https://developer.android.com/reference/kotlin/android/security/AppUriAuthenticationPolicy)` Returns an `Intent` that should be used by an app to request to manage the user's credentials. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!\>? | `https://developer.android.com/reference/kotlin/android/security/KeyChain#getCertificateChain(android.content.Context,%20kotlin.String)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns the `X509Certificate` chain for the requested alias, or null if the alias does not exist or the caller has no permission to access it (see note on exceptions in `https://developer.android.com/reference/kotlin/android/security/KeyChain#getPrivateKey(android.content.Context,%20kotlin.String)`). |
| static [AppUriAuthenticationPolicy](https://developer.android.com/reference/kotlin/android/security/AppUriAuthenticationPolicy) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#getCredentialManagementAppPolicy(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Called by the credential management app to get the authentication policy `https://developer.android.com/reference/kotlin/android/security/AppUriAuthenticationPolicy`. |
| static [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)? | `https://developer.android.com/reference/kotlin/android/security/KeyChain#getPrivateKey(android.content.Context,%20kotlin.String)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns the `PrivateKey` for the requested alias, or null if the alias does not exist or the caller has no permission to access it (see note on exceptions below). |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#isBoundKeyAlgorithm(kotlin.String)(algorithm: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns `true` if the current device's `KeyChain` binds any `PrivateKey` of the given `algorithm` to the device once imported or generated. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#isCredentialManagementApp(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Check whether the caller is the credential management app `CredentialManagementApp`. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#isKeyAlgorithmSupported(kotlin.String)(algorithm: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns `true` if the current device's `KeyChain` supports a specific `PrivateKey` type indicated by `algorithm` (e.g., "RSA"). |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/security/KeyChain#removeCredentialManagementApp(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Called by the credential management app `CredentialManagementApp` to unregister as the credential management app and stop managing the user's credentials. |

## Constants

### ACTION_KEYCHAIN_CHANGED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_KEYCHAIN_CHANGED: String
```

Broadcast Action: Indicates the contents of the keychain has changed. Sent when a KeyChain entry is added, modified or removed.

 Value: "android.security.action.KEYCHAIN_CHANGED"

### ACTION_KEY_ACCESS_CHANGED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_KEY_ACCESS_CHANGED: String
```

Broadcast Action: Indicates that the access permissions for a private key have changed.

 Value: "android.security.action.KEY_ACCESS_CHANGED"

### ACTION_STORAGE_CHANGED

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_STORAGE_CHANGED: String
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/security/KeyChain#ACTION_KEYCHAIN_CHANGED:kotlin.String`, `https://developer.android.com/reference/kotlin/android/security/KeyChain#ACTION_TRUST_STORE_CHANGED:kotlin.String` or `https://developer.android.com/reference/kotlin/android/security/KeyChain#ACTION_KEY_ACCESS_CHANGED:kotlin.String`. Apps that target a version higher than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N_MR1:kotlin.Int` will only receive this broadcast if they register for it at runtime.*

Broadcast Action: Indicates the trusted storage has changed. Sent when one of this happens:

- a new CA is added,
- an existing CA is removed or disabled,
- a disabled CA is enabled,
- trusted storage is reset (all user certs are cleared),
- when permission to access a private key is changed.

<br />

 Value: "android.security.STORAGE_CHANGED"

### ACTION_TRUST_STORE_CHANGED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_TRUST_STORE_CHANGED: String
```

Broadcast Action: Indicates the contents of the trusted certificate store has changed. Sent when one the following occurs:

- A pre-installed CA is disabled or re-enabled
- A CA is added or removed from the trust store

<br />

 Value: "android.security.action.TRUST_STORE_CHANGED"

### EXTRA_CERTIFICATE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CERTIFICATE: String
```

Optional extra to specify an X.509 certificate to install on the `Intent` returned by `https://developer.android.com/reference/kotlin/android/security/KeyChain#createInstallIntent()`. The extra value should be a PEM or ASN.1 DER encoded `byte[]`. An `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#` can be converted to DER encoded bytes with `https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#getEncoded()`.

`https://developer.android.com/reference/kotlin/android/security/KeyChain#EXTRA_NAME:kotlin.String` may be used to provide a default alias name for the installed certificate.

 Value: "CERT"

### EXTRA_KEY_ACCESSIBLE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_KEY_ACCESSIBLE: String
```

Used as a boolean extra field in `https://developer.android.com/reference/kotlin/android/security/KeyChain#ACTION_KEY_ACCESS_CHANGED:kotlin.String` to supply if the key is accessible to the application.

 Value: "android.security.extra.KEY_ACCESSIBLE"

### EXTRA_KEY_ALIAS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_KEY_ALIAS: String
```

Used as a String extra field in `https://developer.android.com/reference/kotlin/android/security/KeyChain#ACTION_KEY_ACCESS_CHANGED:kotlin.String` to supply the alias of the key.

 Value: "android.security.extra.KEY_ALIAS"

### EXTRA_NAME

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NAME: String
```

Optional extra to specify a `String` credential name on the `Intent` returned by `https://developer.android.com/reference/kotlin/android/security/KeyChain#createInstallIntent()`.

 Value: "name"

### EXTRA_PKCS12

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PKCS12: String
```

Optional extra for use with the `Intent` returned by `https://developer.android.com/reference/kotlin/android/security/KeyChain#createInstallIntent()` to specify a PKCS#12 key store to install. The extra value should be a `byte[]`. The bytes may come from an external source or be generated with java.security.KeyStore#store on a "PKCS12" instance.

The user will be prompted for the password to load the key store.

The key store will be scanned for `https://developer.android.com/reference/kotlin/java/security/KeyStore.PrivateKeyEntry.html#` entries and both the private key and associated certificate chain will be installed.

`https://developer.android.com/reference/kotlin/android/security/KeyChain#EXTRA_NAME:kotlin.String` may be used to provide a default alias name for the installed credentials.

 Value: "PKCS12"

### KEY_ALIAS_SELECTION_DENIED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ALIAS_SELECTION_DENIED: String
```

Used by DPC or delegated app in `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver.html#onChoosePrivateKeyAlias(android.content.Context,%20android.content.Intent,%20kotlin.Int,%20android.net.Uri,%20kotlin.String)` or `https://developer.android.com/reference/kotlin/android/app/admin/DelegatedAdminReceiver.html#onChoosePrivateKeyAlias(android.content.Context,%20android.content.Intent,%20kotlin.Int,%20android.net.Uri,%20kotlin.String)` to identify that the requesting app is not granted access to any key, and nor will the user be able to grant access manually.

 Value: "android:alias-selection-denied"

## Public constructors

### KeyChain

```
KeyChain()
```

## Public methods

### choosePrivateKeyAlias

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun choosePrivateKeyAlias(
    activity: Activity, 
    response: KeyChainAliasCallback, 
    keyTypes: Array<String!>?, 
    issuers: Array<Principal!>?, 
    uri: Uri?, 
    alias: String?
): Unit
```

Launches an `Activity` for the user to select the alias for a private key and certificate pair for authentication. The selected alias or null will be returned via the KeyChainAliasCallback callback.

A device policy controller (as a device or profile owner) can intercept the request before the activity is shown, to pick a specific private key alias by implementing `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver.html#onChoosePrivateKeyAlias(android.content.Context,%20android.content.Intent,%20kotlin.Int,%20android.net.Uri,%20kotlin.String)`.

`keyTypes` and `issuers` may be used to narrow down suggested choices to the user. If either `keyTypes` or `issuers` is specified and non-empty, and there are no matching certificates in the KeyChain, then the certificate selection prompt would be suppressed entirely.

`uri` may be used to give the user more context about the server requesting the credentials.

`alias` allows the caller to preselect an existing alias which will still be subject to user confirmation.

| Parameters ||
|---|---|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#): The `https://developer.android.com/reference/kotlin/android/app/Activity.html#` context to use for launching the new sub-Activity to prompt the user to select a private key; used only to call startActivity(); must not be null. |
| `response` | [KeyChainAliasCallback](https://developer.android.com/reference/kotlin/android/security/KeyChainAliasCallback): Callback to invoke when the request completes; must not be null. |
| `keyTypes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: The acceptable types of asymmetric keys such as "RSA", "EC" or null. |
| `issuers` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!\>?: The acceptable certificate issuers for the certificate matching the private key, or null. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?: The full URI the server is requesting the certificate for, or null if unavailable. |
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The alias to preselect if available, or null if unavailable. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the specified issuers are not of type `X500Principal`. |

### choosePrivateKeyAlias

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun choosePrivateKeyAlias(
    activity: Activity, 
    response: KeyChainAliasCallback, 
    keyTypes: Array<String!>?, 
    issuers: Array<Principal!>?, 
    host: String?, 
    port: Int, 
    alias: String?
): Unit
```

Launches an `Activity` for the user to select the alias for a private key and certificate pair for authentication. The selected alias or null will be returned via the KeyChainAliasCallback callback.

A device policy controller (as a device or profile owner) can intercept the request before the activity is shown, to pick a specific private key alias by implementing `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver.html#onChoosePrivateKeyAlias(android.content.Context,%20android.content.Intent,%20kotlin.Int,%20android.net.Uri,%20kotlin.String)`.

`keyTypes` and `issuers` may be used to narrow down suggested choices to the user. If either `keyTypes` or `issuers` is specified and non-empty, and there are no matching certificates in the KeyChain, then the certificate selection prompt would be suppressed entirely.

`host` and `port` may be used to give the user more context about the server requesting the credentials.

`alias` allows the caller to preselect an existing alias which will still be subject to user confirmation.

| Parameters ||
|---|---|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#): The `https://developer.android.com/reference/kotlin/android/app/Activity.html#` context to use for launching the new sub-Activity to prompt the user to select a private key; used only to call startActivity(); must not be null. |
| `response` | [KeyChainAliasCallback](https://developer.android.com/reference/kotlin/android/security/KeyChainAliasCallback): Callback to invoke when the request completes; must not be null. |
| `keyTypes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: The acceptable types of asymmetric keys such as "RSA", "EC" or null. |
| `issuers` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!\>?: The acceptable certificate issuers for the certificate matching the private key, or null. |
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The host name of the server requesting the certificate, or null if unavailable. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The port number of the server requesting the certificate, or -1 if unavailable. |
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The alias to preselect if available, or null if unavailable. |

### createInstallIntent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createInstallIntent(): Intent
```

Returns an `Intent` that can be used for credential installation. The intent may be used without any extras, in which case the user will be able to install credentials from their own source.

Alternatively, `https://developer.android.com/reference/kotlin/android/security/KeyChain#EXTRA_CERTIFICATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/security/KeyChain#EXTRA_PKCS12:kotlin.String` maybe used to specify the bytes of an X.509 certificate or a PKCS#12 key store for installation. These extras may be combined with `https://developer.android.com/reference/kotlin/android/security/KeyChain#EXTRA_NAME:kotlin.String` to provide a default alias name for credentials being installed.

When used with android.app.Activity#startActivityForResult, `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` will be returned if a credential was successfully installed, otherwise `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int` will be returned.

Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, the intent returned by this method cannot be used for installing CA certificates. Since CA certificates can only be installed via Settings, the app should provide the user with a file containing the CA certificate. One way to do this would be to use the `https://developer.android.com/reference/kotlin/android/provider/MediaStore.html#` API to write the certificate to the `https://developer.android.com/reference/kotlin/android/provider/MediaStore.Downloads.html#` collection.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent.html#` | This value cannot be `null`. |

### createManageCredentialsIntent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createManageCredentialsIntent(policy: AppUriAuthenticationPolicy): Intent
```

Returns an `Intent` that should be used by an app to request to manage the user's credentials. This is limited to unmanaged devices. The authentication policy must be provided to be able to make this request successfully.

This intent should be started using `https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int)` to verify whether the request was successful and whether the user accepted or denied the request. If the user successfully receives and accepts the request, the result code will be `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int`, otherwise the result code will be `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int`.

`https://developer.android.com/reference/kotlin/android/security/KeyChain#isCredentialManagementApp(android.content.Context)` should be used to determine whether an app is already the credential management app.

| Parameters ||
|---|---|
| `policy` | [AppUriAuthenticationPolicy](https://developer.android.com/reference/kotlin/android/security/AppUriAuthenticationPolicy): The authentication policy determines which alias for a private key and certificate pair should be used for authentication. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent.html#` | This value cannot be `null`. |

### getCertificateChain

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getCertificateChain(
    context: Context, 
    alias: String
): Array<X509Certificate!>?
```

Returns the `X509Certificate` chain for the requested alias, or null if the alias does not exist or the caller has no permission to access it (see note on exceptions in `https://developer.android.com/reference/kotlin/android/security/KeyChain#getPrivateKey(android.content.Context,%20kotlin.String)`).

**Note:** If a certificate chain was explicitly specified when the alias was installed, this method will return that chain. If only the client certificate was specified at the installation time, this method will try to build a certificate chain using all available trust anchors (preinstalled and user-added).

This method may block while waiting for a connection to another process, and must never be called from the main thread.

As `https://developer.android.com/reference/kotlin/android/app/Activity.html#` and `https://developer.android.com/reference/kotlin/android/app/Service.html#` contexts are short-lived and can be destroyed at any time from the main thread, it is safer to rely on a long-lived context such as one returned from `https://developer.android.com/reference/kotlin/android/content/Context.html#getApplicationContext()`.

In case the caller specifies an alias for which it lacks a grant, it must call #choosePrivateKeyAlias again. See `https://developer.android.com/reference/kotlin/android/security/KeyChain#getPrivateKey(android.content.Context,%20kotlin.String)` for more details on coping with this scenario. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The alias of the desired certificate chain, typically returned via `https://developer.android.com/reference/kotlin/android/security/KeyChainAliasCallback#alias(kotlin.String)`. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.security.KeyChainException` | if the alias was valid but there was some problem accessing it. |
| `java.lang.IllegalStateException` | if called from the main thread. |

### getCredentialManagementAppPolicy

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getCredentialManagementAppPolicy(context: Context): AppUriAuthenticationPolicy
```

Called by the credential management app to get the authentication policy `https://developer.android.com/reference/kotlin/android/security/AppUriAuthenticationPolicy`. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/security/AppUriAuthenticationPolicy` | the credential management app's authentication policy. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller is not the credential management app. |

### getPrivateKey

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getPrivateKey(
    context: Context, 
    alias: String
): PrivateKey?
```

Returns the `PrivateKey` for the requested alias, or null if the alias does not exist or the caller has no permission to access it (see note on exceptions below).

This method may block while waiting for a connection to another process, and must never be called from the main thread.

As `https://developer.android.com/reference/kotlin/android/app/Activity.html#` and `https://developer.android.com/reference/kotlin/android/app/Service.html#` contexts are short-lived and can be destroyed at any time from the main thread, it is safer to rely on a long-lived context such as one returned from `https://developer.android.com/reference/kotlin/android/content/Context.html#getApplicationContext()`.

If the caller provides a valid alias to which it was not granted access, then the caller must invoke #choosePrivateKeyAlias again to get another valid alias or a grant to access the same alias.

On Android versions prior to Q, when a key associated with the specified alias is unavailable, the method will throw a `KeyChainException` rather than return null. If the exception's cause (as obtained by calling `KeyChainException.getCause()`) is a throwable of type `IllegalStateException` then the caller lacks a grant to access the key and certificates associated with this alias. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The alias of the desired private key, typically returned via `https://developer.android.com/reference/kotlin/android/security/KeyChainAliasCallback#alias(kotlin.String)`. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.security.KeyChainException` | if the alias was valid but there was some problem accessing it. |
| `java.lang.IllegalStateException` | if called from the main thread. |

### isBoundKeyAlgorithm

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isBoundKeyAlgorithm(algorithm: String): Boolean
```

**Deprecated:** *Whether the key is bound to the secure hardware is known only once the key has been imported. To find out, use:*

```kotlin
<code>PrivateKey key = ...; // private key from KeyChain
 
  KeyFactory keyFactory =
      KeyFactory.getInstance(key.getAlgorithm(), "AndroidKeyStore");
  KeyInfo keyInfo = keyFactory.getKeySpec(key, KeyInfo.class);
  if (keyInfo.isInsideSecureHardware()) {
      // The key is bound to the secure hardware of this Android
  }</code>
```

<br />

Returns `true` if the current device's `KeyChain` binds any `PrivateKey` of the given `algorithm` to the device once imported or generated. This can be used to tell if there is special hardware support that can be used to bind keys to the device in a way that makes it non-exportable.

| Parameters ||
|---|---|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### isCredentialManagementApp

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isCredentialManagementApp(context: Context): Boolean
```

Check whether the caller is the credential management app `CredentialManagementApp`. The credential management app has the ability to manage the user's KeyChain credentials on unmanaged devices.

`https://developer.android.com/reference/kotlin/android/security/KeyChain#createManageCredentialsIntent(android.security.AppUriAuthenticationPolicy)` should be used by an app to request to become the credential management app. The user must approve this request before the app can manage the user's credentials. There can only be one credential management on the device. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the caller is the credential management app. |

### isKeyAlgorithmSupported

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isKeyAlgorithmSupported(algorithm: String): Boolean
```

Returns `true` if the current device's `KeyChain` supports a specific `PrivateKey` type indicated by `algorithm` (e.g., "RSA").

| Parameters ||
|---|---|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### removeCredentialManagementApp

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun removeCredentialManagementApp(context: Context): Boolean
```

Called by the credential management app `CredentialManagementApp` to unregister as the credential management app and stop managing the user's credentials.

All credentials previously installed by the credential management app will be removed from the user's device.

An app holding `MANAGE_CREDENTIAL_MANAGEMENT_APP` permission can also call this method to remove the current credential management app, even if it's not the current credential management app itself. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the credential management app was successfully removed. |
