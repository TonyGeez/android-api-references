# PpsMoParser

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PpsMoParser

Kotlin| [Java](PpsMoParser.md) 
| --- | --- |

```
class PpsMoParser
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.hotspot2.omadm.PpsMoParser](PpsMoParser.md) |

Utility class for converting OMA-DM (Open Mobile Alliance's Device Management) PPS-MO (PerProviderSubscription Management Object) XML tree to a [PasspointConfiguration](../android.net.wifi.hotspot2/PasspointConfiguration.md) object. Currently this only supports PerProviderSubscription/HomeSP and PerProviderSubscription/Credential subtree for Hotspot 2.0 Release 1 support. For more info, refer to Hotspot 2.0 PPS MO defined in section 9.1 of the Hotspot 2.0 Release 2 Technical Specification. Below is a sample XML string for a Release 1 PPS MO tree: 1.2 PerProviderSubscription urn:wfa:mo:hotspot2dot0perprovidersubscription:1.0 i001 HomeSP FriendlyName Century House FQDN mi6.co.uk RoamingConsortiumOI 112233,445566 Credential Realm shaken.stirred.com UsernamePassword Username james Password Ym9uZDAwNw== EAPMethod EAPType 21 InnerMethod MS-CHAP-V2

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [PasspointConfiguration](../android.net.wifi.hotspot2/PasspointConfiguration.md)! | [parseMoText](PpsMoParser.md))`(`xmlString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Convert a XML string representation of a PPS MO (PerProviderSubscription Management Object) tree to a [PasspointConfiguration](../android.net.wifi.hotspot2/PasspointConfiguration.md) object. |

## Public methods

### parseMoText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseMoText(xmlString: String!): PasspointConfiguration!
```

Convert a XML string representation of a PPS MO (PerProviderSubscription Management Object) tree to a [PasspointConfiguration](../android.net.wifi.hotspot2/PasspointConfiguration.md) object.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------|
| `xmlString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:XML string representation of a PPS MO tree |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [PasspointConfiguration](../android.net.wifi.hotspot2/PasspointConfiguration.md)! | [PasspointConfiguration](../android.net.wifi.hotspot2/PasspointConfiguration.md) or null |
