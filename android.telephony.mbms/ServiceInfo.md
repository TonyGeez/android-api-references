# ServiceInfo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceInfo

Kotlin| [Java](https://developer.android.com/reference/android/telephony/mbms/ServiceInfo "View this page in Java") 

```
open class ServiceInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.mbms.ServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#) |

| Known Direct Subclasses [FileServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileServiceInfo), [StreamingServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceInfo) |--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------| | [FileServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileServiceInfo) | Describes a file service available from the carrier from which files can be downloaded via cell-broadcast. | | [StreamingServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceInfo) | Describes a single MBMS streaming service. | |

Describes a cell-broadcast service. This class should not be instantiated directly -- use [StreamingServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceInfo) or [FileServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileServiceInfo)

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!\>! | [getLocales](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#getLocales())`()` The languages available for this service content |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getNameForLocale](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#getNameForLocale(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)`)` Get the user-displayable name for this cell-broadcast service corresponding to the provided [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#). |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!\> | [getNamedContentLocales](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#getNamedContentLocales())`()` Return an unmodifiable set of the current [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) s that have a user-displayable name associated with them. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getServiceClassName](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#getServiceClassName())`()` The class name for this service - used to categorize and filter |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getServiceId](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#getServiceId())`()` The carrier's identifier for the service. |
| open [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | [getSessionEndTime](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#getSessionEndTime())`()` The end time indicating when this session stops being available. |
| open [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | [getSessionStartTime](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#getSessionStartTime())`()` The start time indicating when this service will be available. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#hashCode())`()` <br /> |

## Public methods

### equals

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getLocales

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocales(): MutableList<Locale!>!
```

The languages available for this service content 

### getNameForLocale

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNameForLocale(locale: Locale): CharSequence
```

Get the user-displayable name for this cell-broadcast service corresponding to the provided [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#):The [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) in which you want the name of the service. This must be a value from the set returned by [getNamedContentLocales()](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#getNamedContentLocales())-- an [java.util.NoSuchElementException](https://developer.android.com/reference/kotlin/java/util/NoSuchElementException.html#) may be thrown otherwise. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | The [CharSequence](https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#) providing the name of the service in the given [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) This value cannot be`null`. |

### getNamedContentLocales

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNamedContentLocales(): MutableSet<Locale!>
```

Return an unmodifiable set of the current [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) s that have a user-displayable name associated with them. The user-displayable name associated with any [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) in this set can be retrieved with [getNameForLocale(java.util.Locale)](https://developer.android.com/reference/kotlin/android/telephony/mbms/ServiceInfo#getNameForLocale(java.util.Locale)).

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!> | An unmodifiable set of [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) objects corresponding to a user-displayable content name in that locale. This value cannot be`null`. |

### getServiceClassName

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getServiceClassName(): String!
```

The class name for this service - used to categorize and filter 

### getServiceId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getServiceId(): String!
```

The carrier's identifier for the service. 

### getSessionEndTime

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSessionEndTime(): Date!
```

The end time indicating when this session stops being available. 

### getSessionStartTime

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSessionStartTime(): Date!
```

The start time indicating when this service will be available. 

### hashCode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
