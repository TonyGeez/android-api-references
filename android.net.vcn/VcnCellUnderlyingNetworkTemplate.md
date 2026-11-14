# VcnCellUnderlyingNetworkTemplate

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VcnCellUnderlyingNetworkTemplate

Kotlin | [Java](VcnCellUnderlyingNetworkTemplate.md) 
| --- | --- |

```
class VcnCellUnderlyingNetworkTemplate : VcnUnderlyingNetworkTemplate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.net.vcn.VcnUnderlyingNetworkTemplate](VcnUnderlyingNetworkTemplate.md) ||
| | ↳ | [android.net.vcn.VcnCellUnderlyingNetworkTemplate](VcnCellUnderlyingNetworkTemplate.md) |

This class represents a configuration for a network template class of underlying cellular networks.

See [VcnUnderlyingNetworkTemplate](VcnUnderlyingNetworkTemplate.md)

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder.md) This class is used to incrementally build VcnCellUnderlyingNetworkTemplate objects. |

| Inherited constants ||
|---|---|
| From class [VcnUnderlyingNetworkTemplate](VcnUnderlyingNetworkTemplate.md) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_ANY](VcnUnderlyingNetworkTemplate.md) Used to configure the matching criteria of a network characteristic. This may include network capabilities, or cellular subscription information. Denotes that networks with or without the characteristic are both acceptable to match this template. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_FORBIDDEN](VcnUnderlyingNetworkTemplate.md) Used to configure the matching criteria of a network characteristic. This may include network capabilities, or cellular subscription information. Denotes that a network MUST NOT have the capability in order to match this template. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_REQUIRED](VcnUnderlyingNetworkTemplate.md) Used to configure the matching criteria of a network characteristic. This may include network capabilities, or cellular subscription information. Denotes that a network MUST have the capability in order to match this template. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](VcnCellUnderlyingNetworkTemplate.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCbs](VcnCellUnderlyingNetworkTemplate.md))`()` Returns the matching criteria for CBS networks. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDun](VcnCellUnderlyingNetworkTemplate.md))`()` Returns the matching criteria for DUN networks. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIms](VcnCellUnderlyingNetworkTemplate.md))`()` Returns the matching criteria for IMS networks. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInternet](VcnCellUnderlyingNetworkTemplate.md))`()` Returns the matching criteria for INTERNET networks. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMms](VcnCellUnderlyingNetworkTemplate.md))`()` Returns the matching criteria for MMS networks. |
| --- | --- |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getOperatorPlmnIds](VcnCellUnderlyingNetworkTemplate.md))`()` Retrieve the matching operator PLMN IDs, or an empty set if any PLMN ID is acceptable. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpportunistic](VcnCellUnderlyingNetworkTemplate.md))`()` Return the matching criteria for opportunistic cellular subscriptions. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRcs](VcnCellUnderlyingNetworkTemplate.md))`()` Returns the matching criteria for RCS networks. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRoaming](VcnCellUnderlyingNetworkTemplate.md))`()` Return the matching criteria for roaming networks. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | [getSimSpecificCarrierIds](VcnCellUnderlyingNetworkTemplate.md))`()` Retrieve the matching sim specific carrier IDs, or an empty set if any sim specific carrier ID is acceptable. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](VcnCellUnderlyingNetworkTemplate.md))`()` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [VcnUnderlyingNetworkTemplate](VcnUnderlyingNetworkTemplate.md) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetered](VcnUnderlyingNetworkTemplate.md))`()` Return the matching criteria for metered networks. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinEntryDownstreamBandwidthKbps](VcnUnderlyingNetworkTemplate.md))`()` Returns the minimum entry downstream bandwidth allowed by this template. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinEntryUpstreamBandwidthKbps](VcnUnderlyingNetworkTemplate.md))`()` Returns the minimum entry upstream bandwidth allowed by this template. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinExitDownstreamBandwidthKbps](VcnUnderlyingNetworkTemplate.md))`()` Returns the minimum exit downstream bandwidth allowed by this template. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinExitUpstreamBandwidthKbps](VcnUnderlyingNetworkTemplate.md))`()` Returns the minimum exit upstream bandwidth allowed by this template. <br /> | ||

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_ANY](VcnUnderlyingNetworkTemplate.md), [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_REQUIRED](VcnUnderlyingNetworkTemplate.md), or [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN](VcnUnderlyingNetworkTemplate.md) |

**See Also**

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setCbs(int)](../android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder.md)) 

### getDun

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDun(): Int
```

Returns the matching criteria for DUN networks.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_ANY](VcnUnderlyingNetworkTemplate.md), [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_REQUIRED](VcnUnderlyingNetworkTemplate.md), or [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN](VcnUnderlyingNetworkTemplate.md) |

**See Also**

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setDun(int)](../android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder.md)) 

### getIms

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIms(): Int
```

Returns the matching criteria for IMS networks.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_ANY](VcnUnderlyingNetworkTemplate.md), [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_REQUIRED](VcnUnderlyingNetworkTemplate.md), or [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN](VcnUnderlyingNetworkTemplate.md) |

**See Also**

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setIms(int)](../android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder.md)) 

### getInternet

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInternet(): Int
```

Returns the matching criteria for INTERNET networks.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_ANY](VcnUnderlyingNetworkTemplate.md), [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_REQUIRED](VcnUnderlyingNetworkTemplate.md), or [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN](VcnUnderlyingNetworkTemplate.md) |

**See Also**

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setInternet(int)](../android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder.md)) 

### getMms

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMms(): Int
```

Returns the matching criteria for MMS networks.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_ANY](VcnUnderlyingNetworkTemplate.md), [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_REQUIRED](VcnUnderlyingNetworkTemplate.md), or [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN](VcnUnderlyingNetworkTemplate.md) |

**See Also**

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setMms(int)](../android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder.md)) 

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

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setOperatorPlmnIds(Set)](../android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder.md)) 

### getOpportunistic

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOpportunistic(): Int
```

Return the matching criteria for opportunistic cellular subscriptions.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_ANY](VcnUnderlyingNetworkTemplate.md), [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_REQUIRED](VcnUnderlyingNetworkTemplate.md), or [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN](VcnUnderlyingNetworkTemplate.md) |

**See Also**

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setOpportunistic(int)](../android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder.md)) 

### getRcs

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRcs(): Int
```

Returns the matching criteria for RCS networks.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_ANY](VcnUnderlyingNetworkTemplate.md), [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_REQUIRED](VcnUnderlyingNetworkTemplate.md), or [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN](VcnUnderlyingNetworkTemplate.md) |

**See Also**

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setRcs(int)](../android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder.md)) 

### getRoaming

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRoaming(): Int
```

Return the matching criteria for roaming networks.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_ANY](VcnUnderlyingNetworkTemplate.md), [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_REQUIRED](VcnUnderlyingNetworkTemplate.md), or [android.net.vcn.VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN](VcnUnderlyingNetworkTemplate.md) |

**See Also**

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setRoaming(int)](../android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder.md)) 

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

- [android.net.vcn.VcnCellUnderlyingNetworkTemplate.Builder#setSimSpecificCarrierIds(Set)](../android/net/vcn/VcnCellUnderlyingNetworkTemplate.Builder.md)) 

### hashCode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
