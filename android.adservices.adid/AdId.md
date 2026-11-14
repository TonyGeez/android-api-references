Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# AdId

Kotlin | [Java](../android/adservices/adid/AdId.md)
| --- | --- |

```
open class AdId
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adid.AdId](../android/adservices/adid/AdId.md) |

A unique, user-resettable, device-wide, per-profile ID for advertising.

Ad networks may use `AdId` to monetize for Interest Based Advertising (IBA), i.e. targeting and remarketing ads. The user may limit availability of this identifier.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adid/AdId#ZERO_OUT:kotlin.String` A zeroed-out `https://developer.android.com/reference/kotlin/android/adservices/adid/AdId#getAdId()` that is returned when the user has `https://developer.android.com/reference/kotlin/android/adservices/adid/AdId#isLimitAdTrackingEnabled()`. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/adid/AdId#AdId(kotlin.String,%20kotlin.Boolean)(adId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, limitAdTrackingEnabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Creates an instance of `https://developer.android.com/reference/kotlin/android/adservices/adid/AdId#` |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adid/AdId#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adid/AdId#getAdId()()` The advertising ID. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adid/AdId#hashCode()()` Returns a hash code value for the object. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adid/AdId#isLimitAdTrackingEnabled()()` Retrieves the limit ad tracking enabled setting. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adid/AdId#toString()()` Returns a string representation of the object. |

## Constants

### ZERO_OUT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

```
static val ZERO_OUT: String
```

A zeroed-out `https://developer.android.com/reference/kotlin/android/adservices/adid/AdId#getAdId()` that is returned when the user has `https://developer.android.com/reference/kotlin/android/adservices/adid/AdId#isLimitAdTrackingEnabled()`.

 Value: "00000000-0000-0000-0000-000000000000"

## Public constructors

### AdId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

```
AdId(
    adId: String, 
    limitAdTrackingEnabled: Boolean)
```

Creates an instance of `https://developer.android.com/reference/kotlin/android/adservices/adid/AdId#`

| Parameters ||
|---|---|
| `adId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): obtained from the provider service. This value cannot be `null`. |
| `limitAdTrackingEnabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): value from the provider service which determines the value of adId. |

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getAdId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

```
open fun getAdId(): String
```

The advertising ID.

The value of advertising Id depends on a combination of `https://developer.android.com/reference/kotlin/android/adservices/adid/AdId#isLimitAdTrackingEnabled()` and `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_AD_ID:kotlin.String`.

When the user is `https://developer.android.com/reference/kotlin/android/adservices/adid/AdId#isLimitAdTrackingEnabled()`, the API returns `https://developer.android.com/reference/kotlin/android/adservices/adid/AdId#ZERO_OUT:kotlin.String`. This disallows a caller to track the user for monetization purposes.

Otherwise, a string unique to the device and user is returned, which can be used to track users for advertising.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isLimitAdTrackingEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

```
open fun isLimitAdTrackingEnabled(): Boolean
```

Retrieves the limit ad tracking enabled setting.

This value is true if user has limit ad tracking enabled, `false` otherwise.

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
