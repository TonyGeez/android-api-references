# VcnCellUnderlyingNetworkTemplate

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VcnCellUnderlyingNetworkTemplate

Kotlin | [Java](https://developer.android.com/reference/android/net/vcn/VcnCellUnderlyingNetworkTemplate "View this page in Java") 
| --- | --- |

```
class VcnCellUnderlyingNetworkTemplate : VcnUnderlyingNetworkTemplate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.net.vcn.VcnUnderlyingNetworkTemplate](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate) ||
| | ↳ | [android.net.vcn.VcnCellUnderlyingNetworkTemplate](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate#) |

This class represents a configuration for a network template class of underlying cellular networks.

See [VcnUnderlyingNetworkTemplate](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate)

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder) This class is used to incrementally build VcnCellUnderlyingNetworkTemplate objects. |

| Inherited constants ||
|---|---|
| From class [VcnUnderlyingNetworkTemplate](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_ANY](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_ANY:kotlin.Int) Used to configure the matching criteria of a network characteristic. This may include network capabilities, or cellular subscription information. Denotes that networks with or without the characteristic are both acceptable to match this template. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_FORBIDDEN](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN:kotlin.Int) Used to configure the matching criteria of a network characteristic. This may include network capabilities, or cellular subscription information. Denotes that a network MUST NOT have the capability in order to match this template. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_REQUIRED](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_REQUIRED:kotlin.Int) Used to configure the matching criteria of a network characteristic. This may include network capabilities, or cellular subscription information. Denotes that a network MUST have the capability in order to match this template. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCbs](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate#getCbs())`()` Returns the matching criteria for CBS networks. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDun](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate#getDun())`()` Returns the matching criteria for DUN networks. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIms](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate#getIms())`()` Returns the matching criteria for IMS networks. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInternet](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate#getInternet())`()` Returns the matching criteria for INTERNET networks. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMms](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate#getMms())`()` Returns the matching criteria for MMS networks. |
| --- | --- |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getOperatorPlmnIds](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate#getOperatorPlmnIds())`()` Retrieve the matching operator PLMN IDs, or an empty set if any PLMN ID is acceptable. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpportunistic](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate#getOpportunistic())`()` Return the matching criteria for opportunistic cellular subscriptions. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRcs](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate#getRcs())`()` Returns the matching criteria for RCS networks. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRoaming](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate#getRoaming())`()` Return the matching criteria for roaming networks. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | [getSimSpecificCarrierIds](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate#getSimSpecificCarrierIds())`()` Retrieve the matching sim specific carrier IDs, or an empty set if any sim specific carrier ID is acceptable. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate#hashCode())`()` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [VcnUnderlyingNetworkTemplate](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetered](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#getMetered())`()` Return the matching criteria for metered networks. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinEntryDownstreamBandwidthKbps](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#getMinEntryDownstreamBandwidthKbps())`()` Returns the minimum entry downstream bandwidth allowed by this template. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinEntryUpstreamBandwidthKbps](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#getMinEntryUpstreamBandwidthKbps())`()` Returns the minimum entry upstream bandwidth allowed by this template. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinExitDownstreamBandwidthKbps](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#getMinExitDownstreamBandwidthKbps())`()` Returns the minimum exit downstream bandwidth allowed by this template. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinExitUpstreamBandwidthKbps](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#getMinExitUpstreamBandwidthKbps())`()` Returns the minimum exit upstream bandwidth allowed by this template. <br /> | ||

## Public methods

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
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
|---------|--------------------------------------------------------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: This value may be `null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this object is the same as the obj argument; `false` otherwise. |

### getCbs

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCbs(): Int
```

Returns the matching criteria for CBS networks.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_ANY](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_ANY:kotlin.Int), [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_REQUIRED](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_REQUIRED:kotlin.Int), or [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN:kotlin.Int) |

**See Also**

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setCbs(int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder#setCbs(kotlin.Int)) 

### getDun

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDun(): Int
```

Returns the matching criteria for DUN networks.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_ANY](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_ANY:kotlin.Int), [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_REQUIRED](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_REQUIRED:kotlin.Int), or [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN:kotlin.Int) |

**See Also**

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setDun(int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder#setDun(kotlin.Int)) 

### getIms

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIms(): Int
```

Returns the matching criteria for IMS networks.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_ANY](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_ANY:kotlin.Int), [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_REQUIRED](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_REQUIRED:kotlin.Int), or [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN:kotlin.Int) |

**See Also**

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setIms(int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder#setIms(kotlin.Int)) 

### getInternet

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInternet(): Int
```

Returns the matching criteria for INTERNET networks.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_ANY](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_ANY:kotlin.Int), [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_REQUIRED](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_REQUIRED:kotlin.Int), or [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN:kotlin.Int) |

**See Also**

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setInternet(int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder#setInternet(kotlin.Int)) 

### getMms

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMms(): Int
```

Returns the matching criteria for MMS networks.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_ANY](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_ANY:kotlin.Int), [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_REQUIRED](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_REQUIRED:kotlin.Int), or [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN:kotlin.Int) |

**See Also**

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setMms(int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder#setMms(kotlin.Int)) 

### getOperatorPlmnIds

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOperatorPlmnIds(): MutableSet<String!>
```

Retrieve the matching operator PLMN IDs, or an empty set if any PLMN ID is acceptable.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be `null`. |

**See Also**

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setOperatorPlmnIds(Set)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder#setOperatorPlmnIds(kotlin.collections.MutableSet)) 

### getOpportunistic

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOpportunistic(): Int
```

Return the matching criteria for opportunistic cellular subscriptions.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_ANY](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_ANY:kotlin.Int), [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_REQUIRED](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_REQUIRED:kotlin.Int), or [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN:kotlin.Int) |

**See Also**

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setOpportunistic(int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder#setOpportunistic(kotlin.Int)) 

### getRcs

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRcs(): Int
```

Returns the matching criteria for RCS networks.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_ANY](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_ANY:kotlin.Int), [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_REQUIRED](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_REQUIRED:kotlin.Int), or [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN:kotlin.Int) |

**See Also**

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setRcs(int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder#setRcs(kotlin.Int)) 

### getRoaming

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRoaming(): Int
```

Return the matching criteria for roaming networks.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_ANY](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_ANY:kotlin.Int), [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_REQUIRED](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_REQUIRED:kotlin.Int), or [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN:kotlin.Int) |

**See Also**

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setRoaming(int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder#setRoaming(kotlin.Int)) 

### getSimSpecificCarrierIds

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSimSpecificCarrierIds(): MutableSet<Int!>
```

Retrieve the matching sim specific carrier IDs, or an empty set if any sim specific carrier ID is acceptable.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!> | This value cannot be `null`. |

**See Also**

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setSimSpecificCarrierIds(Set)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder#setSimSpecificCarrierIds(kotlin.collections.MutableSet)) 

### hashCode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
