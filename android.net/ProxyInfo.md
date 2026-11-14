# ProxyInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProxyInfo

Kotlin| [Java](https://developer.android.com/reference/android/net/ProxyInfo "View this page in Java") 
| --- | --- |

```
open class ProxyInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#) |

Describes a proxy configuration. Proxy configurations are already integrated within the`java.net`and Apache HTTP stack. So [URLConnection](https://developer.android.com/reference/kotlin/java/net/URLConnection.html#) and Apache's`HttpClient`will use them automatically. Other HTTP stacks will need to obtain the proxy info by watching for the [Proxy.PROXY_CHANGE_ACTION](https://developer.android.com/reference/kotlin/android/net/Proxy#PROXY_CHANGE_ACTION:kotlin.String) broadcast and calling methods such as [android.net.ConnectivityManager#getDefaultProxy](https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#getDefaultProxy()).

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#ProxyInfo(android.net.ProxyInfo))`(`source:` ` [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#)?`)` A copy constructor to hold proxy properties. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#)! | [buildDirectProxy](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#buildDirectProxy(kotlin.String,%20kotlin.Int))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#) object that points at a Direct proxy on the specified host and port. |
| openstatic [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#)! | [buildDirectProxy](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#buildDirectProxy(kotlin.String,%20kotlin.Int,%20kotlin.collections.MutableList))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `exclList:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Constructs a [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#) object that points at a Direct proxy on the specified host and port. |
| openstatic [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#)! | [buildPacProxy](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#buildPacProxy(android.net.Uri))`(`pacUri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri)!`)` Construct a [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#) that will download and run the PAC script at the specified URL. |
| --- | --- |
| openstatic [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#) | [buildPacProxy](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#buildPacProxy(android.net.Uri,%20kotlin.Int))`(`pacUrl:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri)`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Construct a [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#) object that will download and run the PAC script at the specified URL and port. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getExclusionList](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#getExclusionList())`()` When configured to use a Direct Proxy this returns the list of hosts for which the proxy is ignored. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getHost](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#getHost())`()` When configured to use a Direct Proxy this returns the host of the proxy. |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri)! | [getPacFileUrl](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#getPacFileUrl())`()` Returns the URL of the current PAC script or null if there is no PAC script. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPort](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#getPort())`()` When configured to use a Direct Proxy this returns the port of the proxy |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#hashCode())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValid](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#isValid())`()` Return true if the pattern of proxy is valid, otherwise return false. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#toString())`()` <br /> |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### ProxyInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProxyInfo(source: ProxyInfo?)
```

A copy constructor to hold proxy properties.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `source` | [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#)?:This value may be`null`. |

## Public methods

### buildDirectProxy

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun buildDirectProxy(
    host: String!, 
    port: Int
): ProxyInfo!
```

Constructs a [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#) object that points at a Direct proxy on the specified host and port. 

### buildDirectProxy

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun buildDirectProxy(
    host: String!, 
    port: Int, 
    exclList: MutableList<String!>!
): ProxyInfo!
```

Constructs a [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#) object that points at a Direct proxy on the specified host and port. The proxy will not be used to access any host in exclusion list, exclList.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exclList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Hosts to exclude using the proxy on connections for. These hosts can use wildcards such as \*.example.com. |

### buildPacProxy

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun buildPacProxy(pacUri: Uri!): ProxyInfo!
```

Construct a [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#) that will download and run the PAC script at the specified URL. 

### buildPacProxy

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun buildPacProxy(
    pacUrl: Uri, 
    port: Int
): ProxyInfo
```

Construct a [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#) object that will download and run the PAC script at the specified URL and port.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------|
| `pacUrl` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo#) | This value cannot be`null`. |

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
