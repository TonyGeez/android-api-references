# IkeIdentification

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeIdentification

Kotlin| [Java](../android/net/ipsec/ike/IkeIdentification.md) 
| --- | --- |

```
abstract class IkeIdentification
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.ipsec.ike.IkeIdentification](../android/net/ipsec/ike/IkeIdentification.md) |

| Known Direct Subclasses [IkeDerAsn1DnIdentification](../android/net/ipsec/ike/IkeDerAsn1DnIdentification.md), [IkeFqdnIdentification](../android/net/ipsec/ike/IkeFqdnIdentification.md), [IkeIpv4AddrIdentification](../android/net/ipsec/ike/IkeIpv4AddrIdentification.md), [IkeIpv6AddrIdentification](../android/net/ipsec/ike/IkeIpv6AddrIdentification.md), [IkeKeyIdIdentification](../android/net/ipsec/ike/IkeKeyIdIdentification.md), [IkeRfc822AddrIdentification](../android/net/ipsec/ike/IkeRfc822AddrIdentification.md) |---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------| | [IkeDerAsn1DnIdentification](../android/net/ipsec/ike/IkeDerAsn1DnIdentification.md) | This class represents an IKE entity ID based on a DER encoded ASN. | | [IkeFqdnIdentification](../android/net/ipsec/ike/IkeFqdnIdentification.md) | IkeFqdnIdentification represents an IKE entity identification based on a fully-qualified domain name (FQDN). | | [IkeIpv4AddrIdentification](../android/net/ipsec/ike/IkeIpv4AddrIdentification.md) | IkeIpv4AddrIdentification represents an IKE entity identification based on IPv4 address. | | [IkeIpv6AddrIdentification](../android/net/ipsec/ike/IkeIpv6AddrIdentification.md) | IkeIpv6AddrIdentification represents an IKE entity identification based on IPv6 address. | | [IkeKeyIdIdentification](../android/net/ipsec/ike/IkeKeyIdIdentification.md) | IkeKeyIdIdentification represents an IKE entity identification based on a Key ID. | | [IkeRfc822AddrIdentification](../android/net/ipsec/ike/IkeRfc822AddrIdentification.md) | IkeRfc822AddrIdentification represents an IKE entity identification based on a fully-qualified RFC 822 email address ID (e.g. ike@android.com). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

IkeIdentification is abstract base class that represents the common information for all types of IKE entity identification.

[IkeIdentification](../android/net/ipsec/ike/IkeIdentification.md) is used in IKE authentication.

## Summary
