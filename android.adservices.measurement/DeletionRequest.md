Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeletionRequest

```
open class DeletionRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.measurement.DeletionRequest](../android/adservices/measurement/DeletionRequest.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The Rubidium (Rb) Measurement APIs, including those in android.adservices.measurement, are being deprecated. There are no direct replacement APIs for the Measurement APIs. Developers currently using these APIs should cease integration, as calls to these APIs will be rejected in upcoming Android releases as part of a soft removal process. Please refer to the official Privacy Sandbox developer documentation and announcements for more details on this deprecation and the future roadmap of Privacy Sandbox on Android: https://privacysandbox.com/news/update-on-plans-for-privacy-sandbox-technologies/

Deletion Request.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/adservices/measurement/DeletionRequest.Builder` Builder for `https://developer.android.com/reference/kotlin/android/adservices/measurement/DeletionRequest#` objects. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/DeletionRequest#DELETION_MODE_ALL:kotlin.Int` Deletion mode to delete all data associated with the selected records. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/DeletionRequest#DELETION_MODE_EXCLUDE_INTERNAL_DATA:kotlin.Int` Deletion mode to delete all data except the internal data (e.g. rate limits) for the selected records. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/DeletionRequest#MATCH_BEHAVIOR_DELETE:kotlin.Int` Match behavior option to delete the supplied params (Origin/Domains). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/DeletionRequest#MATCH_BEHAVIOR_PRESERVE:kotlin.Int` Match behavior option to preserve the supplied params (Origin/Domains) and delete everything else. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/DeletionRequest#getDeletionMode()()` Get the deletion mode. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](../android/net/Uri.md)!\> | `https://developer.android.com/reference/kotlin/android/adservices/measurement/DeletionRequest#getDomainUris()()` Get the list of domain URIs. |
| open [Instant](../java/time/Instant.md) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/DeletionRequest#getEnd()()` Get the end of the deletion range. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/DeletionRequest#getMatchBehavior()()` Get the match behavior. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](../android/net/Uri.md)!\> | `https://developer.android.com/reference/kotlin/android/adservices/measurement/DeletionRequest#getOriginUris()()` Get the list of origin URIs. |
| open [Instant](../java/time/Instant.md) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/DeletionRequest#getStart()()` Get the start of the deletion range. |
| --- | --- |

## Constants

### DELETION_MODE_ALL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DELETION_MODE_ALL: Int
```

**Deprecated:** *Deprecated in Java.*

Deletion mode to delete all data associated with the selected records.

 Value: 0

### DELETION_MODE_EXCLUDE_INTERNAL_DATA

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DELETION_MODE_EXCLUDE_INTERNAL_DATA: Int
```

**Deprecated:** *Deprecated in Java.*

Deletion mode to delete all data except the internal data (e.g. rate limits) for the selected records.

 Value: 1

### MATCH_BEHAVIOR_DELETE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_BEHAVIOR_DELETE: Int
```

**Deprecated:** *Deprecated in Java.*

Match behavior option to delete the supplied params (Origin/Domains).

 Value: 0

### MATCH_BEHAVIOR_PRESERVE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_BEHAVIOR_PRESERVE: Int
```

**Deprecated:** *Deprecated in Java.*

Match behavior option to preserve the supplied params (Origin/Domains) and delete everything else.

 Value: 1

## Public methods

### getDeletionMode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDeletionMode(): Int
```

**Deprecated:** *Deprecated in Java.*

Get the deletion mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/adservices/measurement/DeletionRequest#DELETION_MODE_ALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/adservices/measurement/DeletionRequest#DELETION_MODE_EXCLUDE_INTERNAL_DATA:kotlin.Int` |

### getDomainUris

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDomainUris(): MutableList<Uri!>
```

**Deprecated:** *Deprecated in Java.*

Get the list of domain URIs.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>` | This value cannot be `null`. |

### getEnd

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEnd(): Instant
```

**Deprecated:** *Deprecated in Java.*

Get the end of the deletion range.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | This value cannot be `null`. |

### getMatchBehavior

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMatchBehavior(): Int
```

**Deprecated:** *Deprecated in Java.*

Get the match behavior.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/adservices/measurement/DeletionRequest#MATCH_BEHAVIOR_DELETE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/adservices/measurement/DeletionRequest#MATCH_BEHAVIOR_PRESERVE:kotlin.Int` |

### getOriginUris

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOriginUris(): MutableList<Uri!>
```

**Deprecated:** *Deprecated in Java.*

Get the list of origin URIs.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>` | This value cannot be `null`. |

### getStart

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStart(): Instant
```

**Deprecated:** *Deprecated in Java.*

Get the start of the deletion range.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | This value cannot be `null`. |
