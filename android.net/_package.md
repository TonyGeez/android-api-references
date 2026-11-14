# android.net

# android.net

Kotlin| [Java](../android/net/_package.md)
| --- | --- |

## Interfaces

| [OnNetworkActiveListener](../android/net/ConnectivityManager.OnNetworkActiveListener.md) | Callback for use with [ConnectivityManager.addDefaultNetworkActiveListener](../android/net/ConnectivityManager.md))to find out when the system default network has gone in to a high power state. |
| --- | --- |
| [Callback](../android/net/DnsResolver.Callback.md) | Base interface for answer callbacks |
| [StartTetheringCallback](../android/net/TetheringManager.StartTetheringCallback.md) | Callback for use with [startTethering](../android/net/TetheringManager.md))to find out whether tethering succeeded. |
| [StopTetheringCallback](../android/net/TetheringManager.StopTetheringCallback.md) | Callback for use with [stopTethering](../android/net/TetheringManager.md))to find out whether stop tethering succeeded. |
| --- | --- |
| [TetheringEventCallback](../android/net/TetheringManager.TetheringEventCallback.md) | Callback for use with registerTetheringEventCallback to find out tethering upstream status. |
| [TransportInfo](../android/net/TransportInfo.md) | A container for transport-specific capabilities which is returned by [NetworkCapabilities.getTransportInfo()](../android/net/NetworkCapabilities.md)). |
| [ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md) | A functor used to sanitize a single query value. |
| --- | --- |

## Classes

| [CaptivePortal](../android/net/CaptivePortal.md) | A class allowing apps handling the [ConnectivityManager.ACTION_CAPTIVE_PORTAL_SIGN_IN](../android/net/ConnectivityManager.md) activity to indicate to the system different outcomes of captive portal sign in. |
| --- | --- |
| [ConnectivityDiagnosticsManager](../android/net/ConnectivityDiagnosticsManager.md) | Class that provides utilities for collecting network connectivity diagnostics information. |
| [ConnectivityManager](../android/net/ConnectivityManager.md) | Class that answers queries about the state of network connectivity. |
| [Credentials](../android/net/Credentials.md) | A class for representing UNIX credentials passed via ancillary data on UNIX domain sockets. |
| --- | --- |
| [DhcpInfo](../android/net/DhcpInfo.md) | A simple object for retrieving the results of a DHCP request. |
| [DnsResolver](../android/net/DnsResolver.md) | Dns resolver class for asynchronous dns querying Note that if a client sends a query with more than 1 record in the question section but the remote dns server does not support this, it may not respond at all, leading to a timeout. |
| [EthernetNetworkSpecifier](../android/net/EthernetNetworkSpecifier.md) | A [NetworkSpecifier](../android/net/NetworkSpecifier.md) used to identify ethernet interfaces. |
| --- | --- |
| [Ikev2VpnProfile](../android/net/Ikev2VpnProfile.md) | The Ikev2VpnProfile is a configuration for the platform setup of IKEv2/IPsec VPNs. |
| [InetAddresses](../android/net/InetAddresses.md) | Utility methods for [InetAddress](../java/net/InetAddress.md) implementations. |
| [IpConfiguration](../android/net/IpConfiguration.md) | A class representing the IP configuration of a network. |
| --- | --- |
| [IpPrefix](../android/net/IpPrefix.md) | This class represents an IP prefix, i. |
| [IpSecAlgorithm](../android/net/IpSecAlgorithm.md) | This class represents a single algorithm that can be used by an [IpSecTransform](../android/net/IpSecTransform.md). |
| [IpSecManager](../android/net/IpSecManager.md) | This class contains methods for managing IPsec sessions. |
| --- | --- |
| [IpSecTransform](../android/net/IpSecTransform.md) | This class represents a transform, which roughly corresponds to an IPsec Security Association. |
| [IpSecTransformState](../android/net/IpSecTransformState.md) | This class represents a snapshot of the state of an IpSecTransform |
| [L2capNetworkSpecifier](../android/net/L2capNetworkSpecifier.md) | A [NetworkSpecifier](../android/net/NetworkSpecifier.md) used to identify an L2CAP network over BLE. |
| --- | --- |
| [LinkAddress](../android/net/LinkAddress.md) | Identifies an IP address on a network link. |
| [LinkProperties](../android/net/LinkProperties.md) | Describes the properties of a network link. |
| [LocalServerSocket](../android/net/LocalServerSocket.md) | Non-standard class for creating an inbound UNIX-domain socket in the Linux abstract namespace. |
| --- | --- |
| [LocalSocket](../android/net/LocalSocket.md) | Creates a (non-server) socket in the UNIX-domain namespace. |
| [LocalSocketAddress](../android/net/LocalSocketAddress.md) | A UNIX-domain (AF_LOCAL) socket address. |
| [MacAddress](../android/net/MacAddress.md) | Representation of a MAC address. |
| --- | --- |
| [MailTo](../android/net/MailTo.md) | MailTo URL parser This class parses a mailto scheme URL and then can be queried for the parsed parameters. |
| [Network](../android/net/Network.md) | Identifies a`Network`. |
| [NetworkCapabilities](../android/net/NetworkCapabilities.md) | Representation of the capabilities of an active network. |
| --- | --- |
| [NetworkInfo](../android/net/NetworkInfo.md) | Describes the status of a network interface. |
| [NetworkRequest](../android/net/NetworkRequest.md) | An object describing a network that the application is interested in. |
| [NetworkSpecifier](../android/net/NetworkSpecifier.md) | Describes specific properties of a requested network for use in a [NetworkRequest](../android/net/NetworkRequest.md). |
| --- | --- |
| [PlatformVpnProfile](../android/net/PlatformVpnProfile.md) | PlatformVpnProfile represents a configuration for a platform-based VPN implementation. |
| [Proxy](../android/net/Proxy.md) | A convenience class for accessing the user and default proxy settings. |
| [ProxyInfo](../android/net/ProxyInfo.md) | Describes a proxy configuration. |
| --- | --- |
| [RouteInfo](../android/net/RouteInfo.md) | Represents a network route. |
| [SocketKeepalive](../android/net/SocketKeepalive.md) | Allows applications to request that the system periodically send specific packets on their behalf, using hardware offload to save battery power. |
| [SSLCertificateSocketFactory](../android/net/SSLCertificateSocketFactory.md) | SSLSocketFactory implementation with several extra features: - Timeout specification for SSL handshake operations - Hostname verification in most cases (see WARNINGs below) - Optional SSL session caching with [SSLSessionCache](../android/net/SSLSessionCache.md) - Optionally bypass all SSL certificate checks The handshake timeout does not apply to actual TCP socket connection. <br /> |
| --- | --- |
| [SSLSessionCache](../android/net/SSLSessionCache.md) | File-based cache of established SSL sessions. |
| [StaticIpConfiguration](../android/net/StaticIpConfiguration.md) | Class that describes static IP configuration. |
| [TelephonyNetworkSpecifier](../android/net/TelephonyNetworkSpecifier.md) | NetworkSpecifier object for cellular network request. |
| --- | --- |
| [TetheringInterface](../android/net/TetheringInterface.md) | The mapping of tethering interface and type. |
| [TetheringManager](../android/net/TetheringManager.md) | This class provides the APIs to control the tethering service. |
| [TrafficStats](../android/net/TrafficStats.md) | Class that provides network traffic statistics. |
| --- | --- |
| [Uri](../android/net/Uri.md) | Immutable URI reference. |
| [UrlQuerySanitizer](../android/net/UrlQuerySanitizer.md) | Sanitizes the Query portion of a URL. |
| [VpnManager](../android/net/VpnManager.md) | This class provides an interface for apps to manage platform VPN profiles |
| --- | --- |
| [VpnProfileState](../android/net/VpnProfileState.md) | Describe the state of VPN. |
| [VpnService](../android/net/VpnService.md) | VpnService is a base class for applications to extend and build their own VPN solutions. |

## Exceptions

| [ParseException](../android/net/ParseException.md) | Thrown when parsing failed. |
| --- | --- |
