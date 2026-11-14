Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecurityStateManager

```
open class SecurityStateManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.SecurityStateManager](SecurityStateManager.md) |

SecurityStateManager provides the functionality to query the security status of the system and platform components. For example, this includes the system and vendor security patch level.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/SecurityStateManager#KEY_KERNEL_VERSION:kotlin.String` The kernel version key returned as part of the `Bundle` from `getGlobalSecurityState`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/SecurityStateManager#KEY_SYSTEM_SPL:kotlin.String` The system SPL key returned as part of the `Bundle` from `getGlobalSecurityState`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/SecurityStateManager#KEY_SYSTEM_SUPPLEMENTAL_PATCHES:kotlin.String` The system supplemental patches key returned as part of the `Bundle` from `getGlobalSecurityState`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/SecurityStateManager#KEY_VENDOR_SPL:kotlin.String` The vendor SPL key returned as part of the `Bundle` from `getGlobalSecurityState`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/SecurityStateManager#KEY_VENDOR_SUPPLEMENTAL_PATCHES:kotlin.String` The vendor supplemental patches key returned as part of the `Bundle` from `getGlobalSecurityState`. |

| Public methods ||
|---|---|
| open [Bundle](Bundle.md) | `https://developer.android.com/reference/kotlin/android/os/SecurityStateManager#getGlobalSecurityState()()` Returns the current global security state. |

## Constants

### KEY_KERNEL_VERSION

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_KERNEL_VERSION: String
```

The kernel version key returned as part of the `Bundle` from `getGlobalSecurityState`.

 Value: "kernel_version"

### KEY_SYSTEM_SPL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SYSTEM_SPL: String
```

The system SPL key returned as part of the `Bundle` from `getGlobalSecurityState`.

 Value: "system_spl"

### KEY_SYSTEM_SUPPLEMENTAL_PATCHES

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SYSTEM_SUPPLEMENTAL_PATCHES: String
```

The system supplemental patches key returned as part of the `Bundle` from `getGlobalSecurityState`.

The value is a `String[]` of CVE IDs (e.g., "CVE-2026-12345") that are affirmed to be fully mitigated in the system image, supplemental to the declared `https://developer.android.com/reference/kotlin/android/os/SecurityStateManager#KEY_SYSTEM_SPL:kotlin.String`.

 Value: "system_supplemental_security_patches"

### KEY_VENDOR_SPL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VENDOR_SPL: String
```

The vendor SPL key returned as part of the `Bundle` from `getGlobalSecurityState`.

 Value: "vendor_spl"

### KEY_VENDOR_SUPPLEMENTAL_PATCHES

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VENDOR_SUPPLEMENTAL_PATCHES: String
```

The vendor supplemental patches key returned as part of the `Bundle` from `getGlobalSecurityState`.

The value is a `String[]` listing CVEs (e.g., "CVE-2026-12345") that are affirmed to be fully mitigated in the vendor image, supplemental to the declared `https://developer.android.com/reference/kotlin/android/os/SecurityStateManager#KEY_VENDOR_SPL:kotlin.String`.

 Value: "vendor_supplemental_security_patches"

## Public methods

### getGlobalSecurityState

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGlobalSecurityState(): Bundle
```

Returns the current global security state. Each key-value pair is a mapping of a component of the global security state to its current version/SPL (security patch level). For example, the `KEY_SYSTEM_SPL` key will map to the SPL of the system as defined in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION`. The bundle will also include mappings from WebView packages and packages listed under config `config_securityStatePackages` to their respective versions as defined in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#versionName:kotlin.String`.

The bundle will also include lists of CVEs that are affirmed to be patched in the source code, supplemental to the declared Security Patch Level (SPL). These lists are associated with `https://developer.android.com/reference/kotlin/android/os/SecurityStateManager#KEY_SYSTEM_SUPPLEMENTAL_PATCHES:kotlin.String` and `https://developer.android.com/reference/kotlin/android/os/SecurityStateManager#KEY_VENDOR_SUPPLEMENTAL_PATCHES:kotlin.String`.

The presence of a CVE in these lists indicates that the device implementation has fully mitigated the vulnerability. The accuracy of this information is critical, as it is used to determine the device's security posture.

The CVE data is aggregated from `supplemental_security_patches.xml` files located across multiple device partitions (e.g., `/system`, `/vendor`, `/product`), ensuring that patches from both the framework and hardware-specific components are accounted for.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle` | A `Bundle` that contains the global security state information as string-to-string key-value pairs. This value cannot be `null`. |
