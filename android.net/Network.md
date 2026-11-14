# Network

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Network

Kotlin| [Java](https://developer.android.com/reference/android/net/Network "View this page in Java") 

```
open class Network : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.Network](https://developer.android.com/reference/kotlin/android/net/Network#) |

Identifies a`Network`. This is supplied to applications via [ConnectivityManager.NetworkCallback](https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback) in response to the active android.net.ConnectivityManager#requestNetwork or passive android.net.ConnectivityManager#registerNetworkCallback calls. It is used to direct traffic to the given`Network`, either on a [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) basis through a targeted [SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#) or process-wide via [ConnectivityManager.bindProcessToNetwork](https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#bindProcessToNetwork(android.net.Network)).

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindSocket](https://developer.android.com/reference/kotlin/android/net/Network#bindSocket(java.io.FileDescriptor))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!`)` Binds the specified [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#) to this`Network`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindSocket](https://developer.android.com/reference/kotlin/android/net/Network#bindSocket(java.net.DatagramSocket))`(`socket:` ` [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#)!`)` Binds the specified [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#) to this`Network`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindSocket](https://developer.android.com/reference/kotlin/android/net/Network#bindSocket(java.net.Socket))`(`socket:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`)` Binds the specified [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) to this`Network`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/Network#describeContents())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/Network#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| openstatic [Network](https://developer.android.com/reference/kotlin/android/net/Network#)! | [fromNetworkHandle](https://developer.android.com/reference/kotlin/android/net/Network#fromNetworkHandle(kotlin.Long))`(`networkHandle:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a [Network](https://developer.android.com/reference/kotlin/android/net/Network#) object given a handle returned from [getNetworkHandle](https://developer.android.com/reference/kotlin/android/net/Network#getNetworkHandle()). |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!\>! | [getAllByName](https://developer.android.com/reference/kotlin/android/net/Network#getAllByName(kotlin.String))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Operates the same as`InetAddress.getAllByName`except that host resolution is done on this network. |
| open [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)! | [getByName](https://developer.android.com/reference/kotlin/android/net/Network#getByName(kotlin.String))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Operates the same as`InetAddress.getByName`except that host resolution is done on this network. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getNetworkHandle](https://developer.android.com/reference/kotlin/android/net/Network#getNetworkHandle())`()` Returns a handle representing this`Network`, for use with the NDK API. |
| open [SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#)! | [getSocketFactory](https://developer.android.com/reference/kotlin/android/net/Network#getSocketFactory())`()` Returns a [SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#) bound to this network. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/Network#hashCode())`()` <br /> |
| open [URLConnection](https://developer.android.com/reference/kotlin/java/net/URLConnection.html#)! | [openConnection](https://developer.android.com/reference/kotlin/android/net/Network#openConnection(java.net.URL))`(`url:` ` [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)!`)` Opens the specified [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#) on this`Network`, such that all traffic will be sent on this Network. |
| open [URLConnection](https://developer.android.com/reference/kotlin/java/net/URLConnection.html#)! | [openConnection](https://developer.android.com/reference/kotlin/android/net/Network#openConnection(java.net.URL,%20java.net.Proxy))`(`url:` ` [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)!`, `proxy:` ` [Proxy](https://developer.android.com/reference/kotlin/java/net/Proxy.html#)!`)` Opens the specified [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#) on this`Network`, such that all traffic will be sent on this Network. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/Network#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/Network#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [Network](https://developer.android.com/reference/kotlin/android/net/Network#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/Network#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### bindSocket

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bindSocket(fd: FileDescriptor!): Unit
```

Binds the specified [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#) to this`Network`. All data traffic on the socket represented by this file descriptor will be sent on this`Network`, irrespective of any process-wide network binding set by [ConnectivityManager.bindProcessToNetwork](https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#bindProcessToNetwork(android.net.Network)). The socket must not be connected. 

### bindSocket

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bindSocket(socket: DatagramSocket!): Unit
```

Binds the specified [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#) to this`Network`. All data traffic on the socket will be sent on this`Network`, irrespective of any process-wide network binding set by [ConnectivityManager.bindProcessToNetwork](https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#bindProcessToNetwork(android.net.Network)). The socket must not be connected. 

### bindSocket

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bindSocket(socket: Socket!): Unit
```

Binds the specified [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) to this`Network`. All data traffic on the socket will be sent on this`Network`, irrespective of any process-wide network binding set by [ConnectivityManager.bindProcessToNetwork](https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#bindProcessToNetwork(android.net.Network)). The socket must not be connected. 

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### fromNetworkHandle

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fromNetworkHandle(networkHandle: Long): Network!
```

Returns a [Network](https://developer.android.com/reference/kotlin/android/net/Network#) object given a handle returned from [getNetworkHandle](https://developer.android.com/reference/kotlin/android/net/Network#getNetworkHandle()).

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `networkHandle` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a handle returned from [getNetworkHandle](https://developer.android.com/reference/kotlin/android/net/Network#getNetworkHandle()). |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Network](https://developer.android.com/reference/kotlin/android/net/Network#)! | A [Network](https://developer.android.com/reference/kotlin/android/net/Network#) object derived from`networkHandle`. |

### getAllByName

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAllByName(host: String!): Array<InetAddress!>!
```

Operates the same as`InetAddress.getAllByName`except that host resolution is done on this network.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the hostname or literal IP string to be resolved. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!>! | the array of addresses associated with the specified host. |

| Exceptions ||
|---------------------------------|------------------------------|
| `java.net.UnknownHostException` | if the address lookup fails. |

### getByName

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getByName(host: String!): InetAddress!
```

Operates the same as`InetAddress.getByName`except that host resolution is done on this network.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the hostname to be resolved to an address or`null`. |

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)! | the`InetAddress`instance representing the host. |

| Exceptions ||
|---------------------------------|------------------------------|
| `java.net.UnknownHostException` | if the address lookup fails. |

### getNetworkHandle

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNetworkHandle(): Long
```

Returns a handle representing this`Network`, for use with the NDK API. 

### getSocketFactory

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSocketFactory(): SocketFactory!
```

Returns a [SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#) bound to this network. Any [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) created by this factory will have its traffic sent over this`Network`. Note that if this`Network`ever disconnects, this factory and any [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) it produced in the past or future will cease to work.

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#)! | a [SocketFactory](https://developer.android.com/reference/kotlin/javax/net/SocketFactory.html#) which produces [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) instances bound to this`Network`. |

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### openConnection

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openConnection(url: URL!): URLConnection!
```

Opens the specified [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#) on this`Network`, such that all traffic will be sent on this Network. The URL protocol must be`HTTP`or`HTTPS`.

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [URLConnection](https://developer.android.com/reference/kotlin/java/net/URLConnection.html#)! | a`URLConnection`to the resource referred to by this URL. |

| Exceptions ||
|----------------------------------|--------------------------------------------------|
| `java.net.MalformedURLException` | if the URL protocol is not HTTP or HTTPS. |
| `java.io.IOException` | if an error occurs while opening the connection. |

**See Also**

- [java.net.URL#openConnection()](https://developer.android.com/reference/kotlin/java/net/URL.html#openConnection()) 

### openConnection

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openConnection(
    url: URL!, 
    proxy: Proxy!
): URLConnection!
```

Opens the specified [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#) on this`Network`, such that all traffic will be sent on this Network. The URL protocol must be`HTTP`or`HTTPS`.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `proxy` | [Proxy](https://developer.android.com/reference/kotlin/java/net/Proxy.html#)!:the proxy through which the connection will be established. |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [URLConnection](https://developer.android.com/reference/kotlin/java/net/URLConnection.html#)! | a`URLConnection`to the resource referred to by this URL. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------|
| `java.net.MalformedURLException` | if the URL protocol is not HTTP or HTTPS. |
| `java.lang.IllegalArgumentException` | if the argument proxy is null. |
| `java.io.IOException` | if an error occurs while opening the connection. |

**See Also**

- [java.net.URL#openConnection()](https://developer.android.com/reference/kotlin/java/net/URL.html#openConnection()) 

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Network!>
```
