# StandardConstants

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StandardConstants

```
class StandardConstants
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.StandardConstants](../javax/net/ssl/StandardConstants.md) |

Standard constants definitions

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SNI_HOST_NAME](../javax/net/ssl/StandardConstants.md) The "host_name" type representing of a DNS hostname (see [SNIHostName](../javax/net/ssl/SNIHostName.md)) in a Server Name Indication (SNI) extension. |

## Constants

### SNI_HOST_NAME

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SNI_HOST_NAME: Int
```

The "host_name" type representing of a DNS hostname (see [SNIHostName](../javax/net/ssl/SNIHostName.md)) in a Server Name Indication (SNI) extension.

The SNI extension is a feature that extends the SSL/TLS protocols to indicate what server name the client is attempting to connect to during handshaking. See section 3, "Server Name Indication", of [TLS Extensions (RFC 6066)](http://www.ietf.org/rfc/rfc6066.txt).

The value of this constant is`0x00`. 

 Value: 0

**See Also**

- [javax.net.ssl.SNIServerName](../javax/net/ssl/SNIServerName.md)
- [javax.net.ssl.SNIHostName](../javax/net/ssl/SNIHostName.md)
