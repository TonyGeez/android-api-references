# VcnUnderlyingNetworkTemplate

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VcnUnderlyingNetworkTemplate

Kotlin| [Java](https://developer.android.com/reference/android/net/vcn/VcnUnderlyingNetworkTemplate "View this page in Java") 

```
abstract class VcnUnderlyingNetworkTemplate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.vcn.VcnUnderlyingNetworkTemplate](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#) |

| Known Direct Subclasses [VcnCellUnderlyingNetworkTemplate](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate), [VcnWifiUnderlyingNetworkTemplate](https://developer.android.com/reference/kotlin/android/net/vcn/VcnWifiUnderlyingNetworkTemplate) |-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------| | [VcnCellUnderlyingNetworkTemplate](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate) | This class represents a configuration for a network template class of underlying cellular networks. | | [VcnWifiUnderlyingNetworkTemplate](https://developer.android.com/reference/kotlin/android/net/vcn/VcnWifiUnderlyingNetworkTemplate) | This class represents a configuration for a network template class of underlying Carrier WiFi networks. | |

This class represents a template containing set of underlying network requirements for doing route selection.

Apps provisioning a VCN can configure the underlying network priority for each Gateway Connection by setting a list (in priority order, most to least preferred) of the appropriate subclasses in the VcnGatewayConnectionConfig. See [android.net.vcn.VcnGatewayConnectionConfig.Builder#setVcnUnderlyingNetworkPriorities](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig.Builder#setVcnUnderlyingNetworkPriorities(kotlin.collections.MutableList))

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_ANY](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_ANY:kotlin.Int) Used to configure the matching criteria of a network characteristic. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_FORBIDDEN](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN:kotlin.Int) Used to configure the matching criteria of a network characteristic. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_REQUIRED](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_REQUIRED:kotlin.Int) Used to configure the matching criteria of a network characteristic. |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetered](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#getMetered())`()` Return the matching criteria for metered networks. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinEntryDownstreamBandwidthKbps](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#getMinEntryDownstreamBandwidthKbps())`()` Returns the minimum entry downstream bandwidth allowed by this template. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinEntryUpstreamBandwidthKbps](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#getMinEntryUpstreamBandwidthKbps())`()` Returns the minimum entry upstream bandwidth allowed by this template. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinExitDownstreamBandwidthKbps](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#getMinExitDownstreamBandwidthKbps())`()` Returns the minimum exit downstream bandwidth allowed by this template. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinExitUpstreamBandwidthKbps](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#getMinExitUpstreamBandwidthKbps())`()` Returns the minimum exit upstream bandwidth allowed by this template. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#hashCode())`()` <br /> |

## Constants

### MATCH_ANY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MATCH_ANY: Int
```

Used to configure the matching criteria of a network characteristic. This may include network capabilities, or cellular subscription information. Denotes that networks with or without the characteristic are both acceptable to match this template. 

 Value: 0

### MATCH_FORBIDDEN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MATCH_FORBIDDEN: Int
```

Used to configure the matching criteria of a network characteristic. This may include network capabilities, or cellular subscription information. Denotes that a network MUST NOT have the capability in order to match this template. 

 Value: 2

### MATCH_REQUIRED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MATCH_REQUIRED: Int
```

Used to configure the matching criteria of a network characteristic. This may include network capabilities, or cellular subscription information. Denotes that a network MUST have the capability in order to match this template. 

 Value: 1

## Public methods

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getMetered

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMetered(): Int
```

Return the matching criteria for metered networks. 
**See Also**

- [android.net.vcn.VcnWifiUnderlyingNetworkTemplate.Builder#setMetered(int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnWifiUnderlyingNetworkTemplate.Builder#setMetered(kotlin.Int))
- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setMetered(int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder#setMetered(kotlin.Int)) 

### getMinEntryDownstreamBandwidthKbps

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinEntryDownstreamBandwidthKbps(): Int
```

Returns the minimum entry downstream bandwidth allowed by this template. 
**See Also**

- [android.net.vcn.VcnWifiUnderlyingNetworkTemplate.Builder#setMinDownstreamBandwidthKbps(int, int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnWifiUnderlyingNetworkTemplate.Builder#setMinDownstreamBandwidthKbps(kotlin.Int,%20kotlin.Int))
- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setMinDownstreamBandwidthKbps(int, int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder#setMinDownstreamBandwidthKbps(kotlin.Int,%20kotlin.Int)) 

### getMinEntryUpstreamBandwidthKbps

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinEntryUpstreamBandwidthKbps(): Int
```

Returns the minimum entry upstream bandwidth allowed by this template. 
**See Also**

- [android.net.vcn.VcnWifiUnderlyingNetworkTemplate.Builder#setMinUpstreamBandwidthKbps(int, int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnWifiUnderlyingNetworkTemplate.Builder#setMinUpstreamBandwidthKbps(kotlin.Int,%20kotlin.Int))
- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setMinUpstreamBandwidthKbps(int, int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder#setMinUpstreamBandwidthKbps(kotlin.Int,%20kotlin.Int)) 

### getMinExitDownstreamBandwidthKbps

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinExitDownstreamBandwidthKbps(): Int
```

Returns the minimum exit downstream bandwidth allowed by this template. 
**See Also**

- [android.net.vcn.VcnWifiUnderlyingNetworkTemplate.Builder#setMinDownstreamBandwidthKbps(int, int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnWifiUnderlyingNetworkTemplate.Builder#setMinDownstreamBandwidthKbps(kotlin.Int,%20kotlin.Int))
- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setMinDownstreamBandwidthKbps(int, int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder#setMinDownstreamBandwidthKbps(kotlin.Int,%20kotlin.Int)) 

### getMinExitUpstreamBandwidthKbps

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinExitUpstreamBandwidthKbps(): Int
```

Returns the minimum exit upstream bandwidth allowed by this template. 
**See Also**

- [android.net.vcn.VcnWifiUnderlyingNetworkTemplate.Builder#setMinUpstreamBandwidthKbps(int, int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnWifiUnderlyingNetworkTemplate.Builder#setMinUpstreamBandwidthKbps(kotlin.Int,%20kotlin.Int))
- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setMinUpstreamBandwidthKbps(int, int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder#setMinUpstreamBandwidthKbps(kotlin.Int,%20kotlin.Int)) 

### hashCode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
