# android.net.ipsec.ike

# android.net.ipsec.ike

Kotlin| [Java](https://developer.android.com/reference/android/net/ipsec/ike/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [ChildSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback) | Callback interface for receiving state changes of a Child Session. |
| --- | --- |
| [IkeSessionCallback](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback) | Callback interface for receiving state changes of an [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession). |
| [ConfigRequestIpv4Address](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv4Address) | Represents an IPv4 Internal Address request |
| [ConfigRequestIpv4DhcpServer](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv4DhcpServer) | Represents an IPv4 DHCP server request |
| --- | --- |
| [ConfigRequestIpv4DnsServer](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv4DnsServer) | Represents an IPv4 DNS Server request |
| [ConfigRequestIpv4Netmask](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv4Netmask) | Represents an IPv4 Netmask request |
| [ConfigRequestIpv6Address](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv6Address) | Represents an IPv6 Internal Address request |
| --- | --- |
| [ConfigRequestIpv6DnsServer](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv6DnsServer) | Represents an IPv6 DNS Server request |
| [TunnelModeChildConfigRequest](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.TunnelModeChildConfigRequest) | Represents a tunnel mode child session configuration request type |

## Classes

| [ChildSaProposal](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSaProposal) | ChildSaProposal represents a proposed configuration to negotiate a Child SA. |
| --- | --- |
| [ChildSessionConfiguration](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionConfiguration) | ChildSessionConfiguration represents the negotiated configuration for a Child Session. |
| [ChildSessionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams) | ChildSessionParams is an abstract class that represents proposed configurations for negotiating a Child Session. |
| [IkeDerAsn1DnIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeDerAsn1DnIdentification) | This class represents an IKE entity ID based on a DER encoded ASN. |
| --- | --- |
| [IkeFqdnIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeFqdnIdentification) | IkeFqdnIdentification represents an IKE entity identification based on a fully-qualified domain name (FQDN). |
| [IkeIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIdentification) | IkeIdentification is abstract base class that represents the common information for all types of IKE entity identification. |
| [IkeIpv4AddrIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIpv4AddrIdentification) | IkeIpv4AddrIdentification represents an IKE entity identification based on IPv4 address. |
| --- | --- |
| [IkeIpv6AddrIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIpv6AddrIdentification) | IkeIpv6AddrIdentification represents an IKE entity identification based on IPv6 address. |
| [IkeKeyIdIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeKeyIdIdentification) | IkeKeyIdIdentification represents an IKE entity identification based on a Key ID. |
| [IkeRfc822AddrIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeRfc822AddrIdentification) | IkeRfc822AddrIdentification represents an IKE entity identification based on a fully-qualified RFC 822 email address ID (e.g. ike@android.com). |
| --- | --- |
| [IkeSaProposal](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSaProposal) | IkeSaProposal represents a proposed configuration to negotiate an IKE SA. |
| [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession) | This class represents an IKE Session management object that allows for keying and management of [android.net.IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#) s. |
| [IkeSessionConfiguration](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConfiguration) | IkeSessionConfiguration represents the negotiated configuration for a [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession). |
| --- | --- |
| [IkeSessionConnectionInfo](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionConnectionInfo) | IkeSessionConnectionInfo represents the connection information of an [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession). |
| [IkeSessionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams) | IkeSessionParams contains all user provided configurations for negotiating an [IkeSession](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession). |
| [IkeTrafficSelector](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeTrafficSelector) | IkeTrafficSelector represents a Traffic Selector of a Child Session. |
| --- | --- |
| [IkeTunnelConnectionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeTunnelConnectionParams) | IkeTunnelConnectionParams contains IKEv2 configurations to establish an IKE/IPsec tunnel. |
| [SaProposal](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/SaProposal) | SaProposal represents a proposed configuration to negotiate an IKE or Child SA. |
| [TransportModeChildSessionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TransportModeChildSessionParams) | TransportModeChildSessionParams represents proposed configurations for negotiating a transport mode Child Session. |
| --- | --- |
| [TunnelModeChildSessionParams](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams) | TunnelModeChildSessionParams represents proposed configurations for negotiating a tunnel mode Child Session. |
