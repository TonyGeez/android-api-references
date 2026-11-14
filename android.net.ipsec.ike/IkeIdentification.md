# IkeIdentification

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeIdentification

Kotlin| [Java](https://developer.android.com/reference/android/net/ipsec/ike/IkeIdentification "View this page in Java") 

```
abstract class IkeIdentification
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.ipsec.ike.IkeIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIdentification#) |

| Known Direct Subclasses [IkeDerAsn1DnIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeDerAsn1DnIdentification), [IkeFqdnIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeFqdnIdentification), [IkeIpv4AddrIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIpv4AddrIdentification), [IkeIpv6AddrIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIpv6AddrIdentification), [IkeKeyIdIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeKeyIdIdentification), [IkeRfc822AddrIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeRfc822AddrIdentification) |---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------| | [IkeDerAsn1DnIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeDerAsn1DnIdentification) | This class represents an IKE entity ID based on a DER encoded ASN. | | [IkeFqdnIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeFqdnIdentification) | IkeFqdnIdentification represents an IKE entity identification based on a fully-qualified domain name (FQDN). | | [IkeIpv4AddrIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIpv4AddrIdentification) | IkeIpv4AddrIdentification represents an IKE entity identification based on IPv4 address. | | [IkeIpv6AddrIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIpv6AddrIdentification) | IkeIpv6AddrIdentification represents an IKE entity identification based on IPv6 address. | | [IkeKeyIdIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeKeyIdIdentification) | IkeKeyIdIdentification represents an IKE entity identification based on a Key ID. | | [IkeRfc822AddrIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeRfc822AddrIdentification) | IkeRfc822AddrIdentification represents an IKE entity identification based on a fully-qualified RFC 822 email address ID (e.g. ike@android.com). | |

IkeIdentification is abstract base class that represents the common information for all types of IKE entity identification.

[IkeIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIdentification#) is used in IKE authentication.

## Summary
