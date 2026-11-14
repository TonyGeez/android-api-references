# android.net

# android.net

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [OnNetworkActiveListener](../android/net/ConnectivityManager.OnNetworkActiveListener.md) | Callback for use with [ConnectivityManager.addDefaultNetworkActiveListener](ConnectivityManager.md))to find out when the system default network has gone in to a high power state. |
| --- | --- |
| [Callback](../android/net/DnsResolver.Callback.md) | Base interface for answer callbacks |
| [StartTetheringCallback](../android/net/TetheringManager.StartTetheringCallback.md) | Callback for use with [startTethering](TetheringManager.md))to find out whether tethering succeeded. |
| [StopTetheringCallback](../android/net/TetheringManager.StopTetheringCallback.md) | Callback for use with [stopTethering](TetheringManager.md))to find out whether stop tethering succeeded. |
| --- | --- |
| [TetheringEventCallback](../android/net/TetheringManager.TetheringEventCallback.md) | Callback for use with registerTetheringEventCallback to find out tethering upstream status. |
| [TransportInfo](TransportInfo.md) | A container for transport-specific capabilities which is returned by [NetworkCapabilities.getTransportInfo()](NetworkCapabilities.md)). |
| [ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md) | A functor used to sanitize a single query value. |
| --- | --- |

## Classes

| [CaptivePortal](CaptivePortal.md) | A class allowing apps handling the [ConnectivityManager.ACTION_CAPTIVE_PORTAL_SIGN_IN](ConnectivityManager.md) activity to indicate to the system different outcomes of captive portal sign in. |
| --- | --- |
| [ConnectivityDiagnosticsManager](ConnectivityDiagnosticsManager.md) | Class that provides utilities for collecting network connectivity diagnostics information. |
| [ConnectivityManager](ConnectivityManager.md) | Class that answers queries about the state of network connectivity. |
| [Credentials](Credentials.md) | A class for representing UNIX credentials passed via ancillary data on UNIX domain sockets. |
| --- | --- |
| [DhcpInfo](DhcpInfo.md) | A simple object for retrieving the results of a DHCP request. |
| [DnsResolver](DnsResolver.md) | Dns resolver class for asynchronous dns querying Note that if a client sends a query with more than 1 record in the question section but the remote dns server does not support this, it may not respond at all, leading to a timeout. |
| [EthernetNetworkSpecifier](EthernetNetworkSpecifier.md) | A [NetworkSpecifier](NetworkSpecifier.md) used to identify ethernet interfaces. |
| --- | --- |
| [Ikev2VpnProfile](Ikev2VpnProfile.md) | The Ikev2VpnProfile is a configuration for the platform setup of IKEv2/IPsec VPNs. |
| [InetAddresses](InetAddresses.md) | Utility methods for [InetAddress](../java.net/InetAddress.md) implementations. |
| [IpConfiguration](IpConfiguration.md) | A class representing the IP configuration of a network. |
| --- | --- |
| [IpPrefix](IpPrefix.md) | This class represents an IP prefix, i. |
| [IpSecAlgorithm](IpSecAlgorithm.md) | This class represents a single algorithm that can be used by an [IpSecTransform](IpSecTransform.md). |
| [IpSecManager](IpSecManager.md) | This class contains methods for managing IPsec sessions. |
| --- | --- |
| [IpSecTransform](IpSecTransform.md) | This class represents a transform, which roughly corresponds to an IPsec Security Association. |
| [IpSecTransformState](IpSecTransformState.md) | This class represents a snapshot of the state of an IpSecTransform |
| [L2capNetworkSpecifier](L2capNetworkSpecifier.md) | A [NetworkSpecifier](NetworkSpecifier.md) used to identify an L2CAP network over BLE. |
| --- | --- |
| [LinkAddress](LinkAddress.md) | Identifies an IP address on a network link. |
| [LinkProperties](LinkProperties.md) | Describes the properties of a network link. |
| [LocalServerSocket](LocalServerSocket.md) | Non-standard class for creating an inbound UNIX-domain socket in the Linux abstract namespace. |
| --- | --- |
| [LocalSocket](LocalSocket.md) | Creates a (non-server) socket in the UNIX-domain namespace. |
| [LocalSocketAddress](LocalSocketAddress.md) | A UNIX-domain (AF_LOCAL) socket address. |
| [MacAddress](MacAddress.md) | Representation of a MAC address. |
| --- | --- |
| [MailTo](MailTo.md) | MailTo URL parser This class parses a mailto scheme URL and then can be queried for the parsed parameters. |
| [Network](Network.md) | Identifies a`Network`. |
| [NetworkCapabilities](NetworkCapabilities.md) | Representation of the capabilities of an active network. |
| --- | --- |
| [NetworkInfo](NetworkInfo.md) | Describes the status of a network interface. |
| [NetworkRequest](NetworkRequest.md) | An object describing a network that the application is interested in. |
| [NetworkSpecifier](NetworkSpecifier.md) | Describes specific properties of a requested network for use in a [NetworkRequest](NetworkRequest.md). |
| --- | --- |
| [PlatformVpnProfile](PlatformVpnProfile.md) | PlatformVpnProfile represents a configuration for a platform-based VPN implementation. |
| [Proxy](Proxy.md) | A convenience class for accessing the user and default proxy settings. |
| [ProxyInfo](ProxyInfo.md) | Describes a proxy configuration. |
| --- | --- |
| [RouteInfo](RouteInfo.md) | Represents a network route. |
| [SocketKeepalive](SocketKeepalive.md) | Allows applications to request that the system periodically send specific packets on their behalf, using hardware offload to save battery power. |
| [SSLCertificateSocketFactory](SSLCertificateSocketFactory.md) | SSLSocketFactory implementation with several extra features: - Timeout specification for SSL handshake operations - Hostname verification in most cases (see WARNINGs below) - Optional SSL session caching with [SSLSessionCache](SSLSessionCache.md) - Optionally bypass all SSL certificate checks The handshake timeout does not apply to actual TCP socket connection. <br /> |
| --- | --- |
| [SSLSessionCache](SSLSessionCache.md) | File-based cache of established SSL sessions. |
| [StaticIpConfiguration](StaticIpConfiguration.md) | Class that describes static IP configuration. |
| [TelephonyNetworkSpecifier](TelephonyNetworkSpecifier.md) | NetworkSpecifier object for cellular network request. |
| --- | --- |
| [TetheringInterface](TetheringInterface.md) | The mapping of tethering interface and type. |
| [TetheringManager](TetheringManager.md) | This class provides the APIs to control the tethering service. |
| [TrafficStats](TrafficStats.md) | Class that provides network traffic statistics. |
| --- | --- |
| [Uri](Uri.md) | Immutable URI reference. |
| [UrlQuerySanitizer](UrlQuerySanitizer.md) | Sanitizes the Query portion of a URL. |
| [VpnManager](VpnManager.md) | This class provides an interface for apps to manage platform VPN profiles |
| --- | --- |
| [VpnProfileState](VpnProfileState.md) | Describe the state of VPN. |
| [VpnService](VpnService.md) | VpnService is a base class for applications to extend and build their own VPN solutions. |

## Exceptions

| [ParseException](ParseException.md) | Thrown when parsing failed. |
| --- | --- |
