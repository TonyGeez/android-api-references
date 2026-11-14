# ConfigParser

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConfigParser

Kotlin| [Java](../android/net/wifi/hotspot2/ConfigParser.md) 
| --- | --- |

```
class ConfigParser
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.hotspot2.ConfigParser](../android/net/wifi/hotspot2/ConfigParser.md) |

Utility class for building PasspointConfiguration from an installation file.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [PasspointConfiguration](../android/net/wifi/hotspot2/PasspointConfiguration.md)! | [parsePasspointConfig](../android/net/wifi/hotspot2/ConfigParser.md))`(`mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Parse the Hotspot 2. |

## Public methods

### parsePasspointConfig

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parsePasspointConfig(
    mimeType: String!, 
    data: ByteArray!
): PasspointConfiguration!
```

Parse the Hotspot 2.0 Release 1 configuration data into a [PasspointConfiguration](../android/net/wifi/hotspot2/PasspointConfiguration.md) object. The configuration data is a base64 encoded MIME multipart data. Below is the format of the decoded message: Content-Type: multipart/mixed; boundary={boundary} Content-Transfer-Encoding: base64 \[Skip uninterested headers\] --{boundary} Content-Type: application/x-passpoint-profile Content-Transfer-Encoding: base64 \[base64 encoded Passpoint profile data\] --{boundary} Content-Type: application/x-x509-ca-cert Content-Transfer-Encoding: base64 \[base64 encoded X509 CA certificate data\] --{boundary} Content-Type: application/x-pkcs12 Content-Transfer-Encoding: base64 \[base64 encoded PKCS#12 ASN.1 structure containing client certificate chain\] --{boundary}

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:MIME type of the encoded data. |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:A base64 encoded MIME multipart message containing the Passpoint profile (required), CA (Certificate Authority) certificate (optional), and client certificate chain (optional). |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [PasspointConfiguration](../android/net/wifi/hotspot2/PasspointConfiguration.md)! | [PasspointConfiguration](../android/net/wifi/hotspot2/PasspointConfiguration.md) |
