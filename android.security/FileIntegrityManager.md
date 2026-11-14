# FileIntegrityManager

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileIntegrityManager

Kotlin| [Java](FileIntegrityManager.md) 
| --- | --- |

```
class FileIntegrityManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.FileIntegrityManager](FileIntegrityManager.md) |

This class provides access to file integrity related operations. 
Restricted for SDK Runtime environment in API level 34.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isApkVeritySupported](FileIntegrityManager.md))`()` Returns whether fs-verity is supported on the device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAppSourceCertificateTrusted](FileIntegrityManager.md))`(`certificate:` ` [X509Certificate](../java.security.cert/X509Certificate.md)`)` Returns whether the given certificate can be used to prove app's install source. |

## Public methods

### isApkVeritySupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isApkVeritySupported(): Boolean
```

Returns whether fs-verity is supported on the device. fs-verity provides on-access verification, although the app APIs are only made available to apps in a later SDK version. Only when this method returns true, the other fs-verity APIs in the same class can succeed.

The app may not need this method and just call the other APIs normally and handle any failure. If some app feature really depends on fs-verity (e.g. protecting integrity of a large file download), an early check of support status may avoid any cost if it is to fail late.

Note: for historical reasons this is named`isApkVeritySupported()`instead of`isFsVeritySupported()`. It has also been available since API level 30, predating the other fs-verity APIs. 

### isAppSourceCertificateTrusted

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAppSourceCertificateTrusted(certificate: X509Certificate): Boolean
```

**Deprecated:** *The feature is no longer supported, and this API now always returns false.*

Returns whether the given certificate can be used to prove app's install source. Always return false if the feature is not supported.

A store can use this API to decide if a signature file needs to be downloaded. Also, if a store has shipped different certificates before (e.g. with stronger and weaker key), it can also use this API to download the best signature on the running device. 
Requires [android.Manifest.permission#INSTALL_PACKAGES](../android/Manifest.permission.md) or [android.Manifest.permission#REQUEST_INSTALL_PACKAGES](../android/Manifest.permission.md)

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `certificate` | [X509Certificate](../java.security.cert/X509Certificate.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the certificate is trusted in the system |
