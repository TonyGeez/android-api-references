# HostNameResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HostNameResolver

```
interface HostNameResolver
```

| [org.apache.http.conn.scheme.HostNameResolver](https://developer.android.com/reference/kotlin/org/apache/http/conn/scheme/HostNameResolver#) |

| **This interface was deprecated in API level 22.**
|
| Please use java.net.URL#openConnection instead. Please visit [this webpage](http://android-developers.blogspot.com/2011/09/androids-http-clients.html) for further details.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)! | [resolve](https://developer.android.com/reference/kotlin/org/apache/http/conn/scheme/HostNameResolver#resolve(kotlin.String))`(`hostname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public methods

### resolve

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun resolve(hostname: String!): InetAddress!
```

**Deprecated:** *Deprecated in Java.*
