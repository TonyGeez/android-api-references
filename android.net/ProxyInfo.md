# ProxyInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProxyInfo

Kotlin| [Java](ProxyInfo.md) 
| --- | --- |

```
open class ProxyInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.ProxyInfo](ProxyInfo.md) |

Describes a proxy configuration. Proxy configurations are already integrated within the`java.net`and Apache HTTP stack. So [URLConnection](../java.net/URLConnection.md) and Apache's`HttpClient`will use them automatically. Other HTTP stacks will need to obtain the proxy info by watching for the [Proxy.PROXY_CHANGE_ACTION](Proxy.md) broadcast and calling methods such as [android.net.ConnectivityManager#getDefaultProxy](ConnectivityManager.md)).

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ProxyInfo](ProxyInfo.md))`(`source:` ` [ProxyInfo](ProxyInfo.md)?`)` A copy constructor to hold proxy properties. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [ProxyInfo](ProxyInfo.md)! | [buildDirectProxy](ProxyInfo.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a [ProxyInfo](ProxyInfo.md) object that points at a Direct proxy on the specified host and port. |
| openstatic [ProxyInfo](ProxyInfo.md)! | [buildDirectProxy](ProxyInfo.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `exclList:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Constructs a [ProxyInfo](ProxyInfo.md) object that points at a Direct proxy on the specified host and port. |
| openstatic [ProxyInfo](ProxyInfo.md)! | [buildPacProxy](ProxyInfo.md))`(`pacUri:` ` [Uri](Uri.md)!`)` Construct a [ProxyInfo](ProxyInfo.md) that will download and run the PAC script at the specified URL. |
| --- | --- |
| openstatic [ProxyInfo](ProxyInfo.md) | [buildPacProxy](ProxyInfo.md))`(`pacUrl:` ` [Uri](Uri.md)`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Construct a [ProxyInfo](ProxyInfo.md) object that will download and run the PAC script at the specified URL and port. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](ProxyInfo.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getExclusionList](ProxyInfo.md))`()` When configured to use a Direct Proxy this returns the list of hosts for which the proxy is ignored. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getHost](ProxyInfo.md))`()` When configured to use a Direct Proxy this returns the host of the proxy. |
| open [Uri](Uri.md)! | [getPacFileUrl](ProxyInfo.md))`()` Returns the URL of the current PAC script or null if there is no PAC script. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPort](ProxyInfo.md))`()` When configured to use a Direct Proxy this returns the port of the proxy |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](ProxyInfo.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValid](ProxyInfo.md))`()` Return true if the pattern of proxy is valid, otherwise return false. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](ProxyInfo.md))`()` <br /> |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ProxyInfo](ProxyInfo.md)!\> | [CREATOR](ProxyInfo.md) <br /> |

## Public constructors

### ProxyInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProxyInfo(source: ProxyInfo?)
```

A copy constructor to hold proxy properties.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `source` | [ProxyInfo](ProxyInfo.md)?:This value may be`null`. |

## Public methods

### buildDirectProxy

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun buildDirectProxy(
    host: String!, 
    port: Int
): ProxyInfo!
```

Constructs a [ProxyInfo](ProxyInfo.md) object that points at a Direct proxy on the specified host and port. 

### buildDirectProxy

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun buildDirectProxy(
    host: String!, 
    port: Int, 
    exclList: MutableList<String!>!
): ProxyInfo!
```

Constructs a [ProxyInfo](ProxyInfo.md) object that points at a Direct proxy on the specified host and port. The proxy will not be used to access any host in exclusion list, exclList.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exclList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Hosts to exclude using the proxy on connections for. These hosts can use wildcards such as \*.example.com. |

### buildPacProxy

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun buildPacProxy(pacUri: Uri!): ProxyInfo!
```

Construct a [ProxyInfo](ProxyInfo.md) that will download and run the PAC script at the specified URL. 

### buildPacProxy

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun buildPacProxy(
    pacUrl: Uri, 
    port: Int
): ProxyInfo
```

Construct a [ProxyInfo](ProxyInfo.md) object that will download and run the PAC script at the specified URL and port.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------|
| `pacUrl` | [Uri](Uri.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [ProxyInfo](ProxyInfo.md) | This value cannot be`null`. |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getExclusionList

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExclusionList(): Array<String!>!
```

When configured to use a Direct Proxy this returns the list of hosts for which the proxy is ignored. 

### getHost

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHost(): String!
```

When configured to use a Direct Proxy this returns the host of the proxy. 

### getPacFileUrl

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPacFileUrl(): Uri!
```

Returns the URL of the current PAC script or null if there is no PAC script. 

### getPort

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPort(): Int
```

When configured to use a Direct Proxy this returns the port of the proxy 

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isValid

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isValid(): Boolean
```

Return true if the pattern of proxy is valid, otherwise return false. 

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ProxyInfo!>
```
