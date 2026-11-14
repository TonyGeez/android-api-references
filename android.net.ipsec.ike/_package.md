# android.net.ipsec.ike

# android.net.ipsec.ike

Kotlin| [Java](../android/net/ipsec/ike/_package.md)
| --- | --- |

## Interfaces

| [ChildSessionCallback](../android/net/ipsec/ike/ChildSessionCallback.md) | Callback interface for receiving state changes of a Child Session. |
| --- | --- |
| [IkeSessionCallback](../android/net/ipsec/ike/IkeSessionCallback.md) | Callback interface for receiving state changes of an [IkeSession](../android/net/ipsec/ike/IkeSession.md). |
| [ConfigRequestIpv4Address](../android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv4Address.md) | Represents an IPv4 Internal Address request |
| [ConfigRequestIpv4DhcpServer](../android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv4DhcpServer.md) | Represents an IPv4 DHCP server request |
| --- | --- |
| [ConfigRequestIpv4DnsServer](../android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv4DnsServer.md) | Represents an IPv4 DNS Server request |
| [ConfigRequestIpv4Netmask](../android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv4Netmask.md) | Represents an IPv4 Netmask request |
| [ConfigRequestIpv6Address](../android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv6Address.md) | Represents an IPv6 Internal Address request |
| --- | --- |
| [ConfigRequestIpv6DnsServer](../android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv6DnsServer.md) | Represents an IPv6 DNS Server request |
| [TunnelModeChildConfigRequest](../android/net/ipsec/ike/TunnelModeChildSessionParams.TunnelModeChildConfigRequest.md) | Represents a tunnel mode child session configuration request type |

## Classes

| [ChildSaProposal](../android/net/ipsec/ike/ChildSaProposal.md) | ChildSaProposal represents a proposed configuration to negotiate a Child SA. |
| --- | --- |
| [ChildSessionConfiguration](../android/net/ipsec/ike/ChildSessionConfiguration.md) | ChildSessionConfiguration represents the negotiated configuration for a Child Session. |
| [ChildSessionParams](../android/net/ipsec/ike/ChildSessionParams.md) | ChildSessionParams is an abstract class that represents proposed configurations for negotiating a Child Session. |
| [IkeDerAsn1DnIdentification](../android/net/ipsec/ike/IkeDerAsn1DnIdentification.md) | This class represents an IKE entity ID based on a DER encoded ASN. |
| --- | --- |
| [IkeFqdnIdentification](../android/net/ipsec/ike/IkeFqdnIdentification.md) | IkeFqdnIdentification represents an IKE entity identification based on a fully-qualified domain name (FQDN). |
| [IkeIdentification](../android/net/ipsec/ike/IkeIdentification.md) | IkeIdentification is abstract base class that represents the common information for all types of IKE entity identification. |
| [IkeIpv4AddrIdentification](../android/net/ipsec/ike/IkeIpv4AddrIdentification.md) | IkeIpv4AddrIdentification represents an IKE entity identification based on IPv4 address. |
| --- | --- |
| [IkeIpv6AddrIdentification](../android/net/ipsec/ike/IkeIpv6AddrIdentification.md) | IkeIpv6AddrIdentification represents an IKE entity identification based on IPv6 address. |
| [IkeKeyIdIdentification](../android/net/ipsec/ike/IkeKeyIdIdentification.md) | IkeKeyIdIdentification represents an IKE entity identification based on a Key ID. |
| [IkeRfc822AddrIdentification](../android/net/ipsec/ike/IkeRfc822AddrIdentification.md) | IkeRfc822AddrIdentification represents an IKE entity identification based on a fully-qualified RFC 822 email address ID (e.g. ike@android.com). |
| --- | --- |
| [IkeSaProposal](../android/net/ipsec/ike/IkeSaProposal.md) | IkeSaProposal represents a proposed configuration to negotiate an IKE SA. |
| [IkeSession](../android/net/ipsec/ike/IkeSession.md) | This class represents an IKE Session management object that allows for keying and management of [android.net.IpSecTransform](../android/net/IpSecTransform.md) s. |
| [IkeSessionConfiguration](../android/net/ipsec/ike/IkeSessionConfiguration.md) | IkeSessionConfiguration represents the negotiated configuration for a [IkeSession](../android/net/ipsec/ike/IkeSession.md). |
| --- | --- |
| [IkeSessionConnectionInfo](../android/net/ipsec/ike/IkeSessionConnectionInfo.md) | IkeSessionConnectionInfo represents the connection information of an [IkeSession](../android/net/ipsec/ike/IkeSession.md). |
| [IkeSessionParams](../android/net/ipsec/ike/IkeSessionParams.md) | IkeSessionParams contains all user provided configurations for negotiating an [IkeSession](../android/net/ipsec/ike/IkeSession.md). |
| [IkeTrafficSelector](../android/net/ipsec/ike/IkeTrafficSelector.md) | IkeTrafficSelector represents a Traffic Selector of a Child Session. |
| --- | --- |
| [IkeTunnelConnectionParams](../android/net/ipsec/ike/IkeTunnelConnectionParams.md) | IkeTunnelConnectionParams contains IKEv2 configurations to establish an IKE/IPsec tunnel. |
| [SaProposal](../android/net/ipsec/ike/SaProposal.md) | SaProposal represents a proposed configuration to negotiate an IKE or Child SA. |
| [TransportModeChildSessionParams](../android/net/ipsec/ike/TransportModeChildSessionParams.md) | TransportModeChildSessionParams represents proposed configurations for negotiating a transport mode Child Session. |
| --- | --- |
| [TunnelModeChildSessionParams](../android/net/ipsec/ike/TunnelModeChildSessionParams.md) | TunnelModeChildSessionParams represents proposed configurations for negotiating a tunnel mode Child Session. |
