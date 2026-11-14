# ServiceInfo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceInfo

Kotlin| [Java](../android/telephony/mbms/ServiceInfo.md) 
| --- | --- |

```
open class ServiceInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.mbms.ServiceInfo](../android/telephony/mbms/ServiceInfo.md) |

| Known Direct Subclasses [FileServiceInfo](../android/telephony/mbms/FileServiceInfo.md), [StreamingServiceInfo](../android/telephony/mbms/StreamingServiceInfo.md) |--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------| | [FileServiceInfo](../android/telephony/mbms/FileServiceInfo.md) | Describes a file service available from the carrier from which files can be downloaded via cell-broadcast. | | [StreamingServiceInfo](../android/telephony/mbms/StreamingServiceInfo.md) | Describes a single MBMS streaming service. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Describes a cell-broadcast service. This class should not be instantiated directly -- use [StreamingServiceInfo](../android/telephony/mbms/StreamingServiceInfo.md) or [FileServiceInfo](../android/telephony/mbms/FileServiceInfo.md)

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/telephony/mbms/ServiceInfo.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Locale](../java/util/Locale.md)!\>! | [getLocales](../android/telephony/mbms/ServiceInfo.md))`()` The languages available for this service content |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getNameForLocale](../android/telephony/mbms/ServiceInfo.md))`(`locale:` ` [Locale](../java/util/Locale.md)`)` Get the user-displayable name for this cell-broadcast service corresponding to the provided [Locale](../java/util/Locale.md). |
| --- | --- |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Locale](../java/util/Locale.md)!\> | [getNamedContentLocales](../android/telephony/mbms/ServiceInfo.md))`()` Return an unmodifiable set of the current [Locale](../java/util/Locale.md) s that have a user-displayable name associated with them. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getServiceClassName](../android/telephony/mbms/ServiceInfo.md))`()` The class name for this service - used to categorize and filter |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getServiceId](../android/telephony/mbms/ServiceInfo.md))`()` The carrier's identifier for the service. |
| --- | --- |
| open [Date](../java/util/Date.md)! | [getSessionEndTime](../android/telephony/mbms/ServiceInfo.md))`()` The end time indicating when this session stops being available. |
| open [Date](../java/util/Date.md)! | [getSessionStartTime](../android/telephony/mbms/ServiceInfo.md))`()` The start time indicating when this service will be available. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/telephony/mbms/ServiceInfo.md))`()` <br /> |
| --- | --- |

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

Get the user-displayable name for this cell-broadcast service corresponding to the provided [Locale](../java/util/Locale.md).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md):The [Locale](../java/util/Locale.md) in which you want the name of the service. This must be a value from the set returned by [getNamedContentLocales()](../android/telephony/mbms/ServiceInfo.md))-- an [java.util.NoSuchElementException](../java/util/NoSuchElementException.md) may be thrown otherwise. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | The [CharSequence](../java/lang/CharSequence.md) providing the name of the service in the given [Locale](../java/util/Locale.md) This value cannot be`null`. |

### getNamedContentLocales

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNamedContentLocales(): MutableSet<Locale!>
```

Return an unmodifiable set of the current [Locale](../java/util/Locale.md) s that have a user-displayable name associated with them. The user-displayable name associated with any [Locale](../java/util/Locale.md) in this set can be retrieved with [getNameForLocale(java.util.Locale)](../android/telephony/mbms/ServiceInfo.md)).

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Locale](../java/util/Locale.md)!> | An unmodifiable set of [Locale](../java/util/Locale.md) objects corresponding to a user-displayable content name in that locale. This value cannot be`null`. |

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
