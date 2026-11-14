Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LeaveCustomAudienceRequest

```
class LeaveCustomAudienceRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.customaudience.LeaveCustomAudienceRequest](LeaveCustomAudienceRequest.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The Rubidium (Rb) Relevance APIs, including those in android.adservices.customaudience, are being deprecated. Relevance APIs have no direct replacement. Developers should stop using them, as calls will be rejected in future Android releases. Please refer to official Privacy Sandbox documentation for deprecation and roadmap details: https://privacysandbox.com/news/update-on-plans-for-privacy-sandbox-technologies/

The request object is used to leave a custom audience.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/adservices/customaudience/LeaveCustomAudienceRequest.Builder` Builder for `https://developer.android.com/reference/kotlin/android/adservices/customaudience/LeaveCustomAudienceRequest#` objects. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/customaudience/LeaveCustomAudienceRequest#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Checks whether two `https://developer.android.com/reference/kotlin/android/adservices/customaudience/LeaveCustomAudienceRequest#` objects contain the same information. |
| [AdTechIdentifier](../android.adservices.common/AdTechIdentifier.md) | `https://developer.android.com/reference/kotlin/android/adservices/customaudience/LeaveCustomAudienceRequest#getBuyer()()` Gets the buyer's `https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#`, as identified by a domain in the form "buyerexample. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/customaudience/LeaveCustomAudienceRequest#getName()()` Gets the arbitrary string provided by the owner and buyer on creation of the `https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience` object that represents a single custom audience. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/customaudience/LeaveCustomAudienceRequest#hashCode()()` Returns the hash of the `https://developer.android.com/reference/kotlin/android/adservices/customaudience/LeaveCustomAudienceRequest#` object's data. |

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether two `https://developer.android.com/reference/kotlin/android/adservices/customaudience/LeaveCustomAudienceRequest#` objects contain the same information.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getBuyer

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBuyer(): AdTechIdentifier
```

**Deprecated:** *Deprecated in Java.*

Gets the buyer's `https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#`, as identified by a domain in the form "buyerexample.com".

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#` | an `https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#` containing the custom audience's buyer's domain. This value cannot be `null`. |

### getName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): String
```

**Deprecated:** *Deprecated in Java.*

Gets the arbitrary string provided by the owner and buyer on creation of the `https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience` object that represents a single custom audience.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the String name of the custom audience. This value cannot be `null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the hash of the `https://developer.android.com/reference/kotlin/android/adservices/customaudience/LeaveCustomAudienceRequest#` object's data.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |
