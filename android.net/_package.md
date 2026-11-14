# android.net

# android.net

Kotlin| [Java](https://developer.android.com/reference/android/net/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [OnNetworkActiveListener](https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.OnNetworkActiveListener) | Callback for use with [ConnectivityManager.addDefaultNetworkActiveListener](https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#addDefaultNetworkActiveListener(android.net.ConnectivityManager.OnNetworkActiveListener))to find out when the system default network has gone in to a high power state. |
| --- | --- |
| [Callback](https://developer.android.com/reference/kotlin/android/net/DnsResolver.Callback) | Base interface for answer callbacks |
| [StartTetheringCallback](https://developer.android.com/reference/kotlin/android/net/TetheringManager.StartTetheringCallback) | Callback for use with [startTethering](https://developer.android.com/reference/kotlin/android/net/TetheringManager#startTethering(android.net.TetheringManager.TetheringRequest,%20java.util.concurrent.Executor,%20android.net.TetheringManager.StartTetheringCallback))to find out whether tethering succeeded. |
| [StopTetheringCallback](https://developer.android.com/reference/kotlin/android/net/TetheringManager.StopTetheringCallback) | Callback for use with [stopTethering](https://developer.android.com/reference/kotlin/android/net/TetheringManager#stopTethering(android.net.TetheringManager.TetheringRequest,%20java.util.concurrent.Executor,%20android.net.TetheringManager.StopTetheringCallback))to find out whether stop tethering succeeded. |
| --- | --- |
| [TetheringEventCallback](https://developer.android.com/reference/kotlin/android/net/TetheringManager.TetheringEventCallback) | Callback for use with registerTetheringEventCallback to find out tethering upstream status. |
| [TransportInfo](https://developer.android.com/reference/kotlin/android/net/TransportInfo) | A container for transport-specific capabilities which is returned by [NetworkCapabilities.getTransportInfo()](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#getTransportInfo()). |
| [ValueSanitizer](https://developer.android.com/reference/kotlin/android/net/UrlQuerySanitizer.ValueSanitizer) | A functor used to sanitize a single query value. |
| --- | --- |

## Classes

| [CaptivePortal](https://developer.android.com/reference/kotlin/android/net/CaptivePortal) | A class allowing apps handling the [ConnectivityManager.ACTION_CAPTIVE_PORTAL_SIGN_IN](https://developer.android.com/reference/kotlin/android/net/ConnectivityManager#ACTION_CAPTIVE_PORTAL_SIGN_IN:kotlin.String) activity to indicate to the system different outcomes of captive portal sign in. |
| --- | --- |
| [ConnectivityDiagnosticsManager](https://developer.android.com/reference/kotlin/android/net/ConnectivityDiagnosticsManager) | Class that provides utilities for collecting network connectivity diagnostics information. |
| [ConnectivityManager](https://developer.android.com/reference/kotlin/android/net/ConnectivityManager) | Class that answers queries about the state of network connectivity. |
| [Credentials](https://developer.android.com/reference/kotlin/android/net/Credentials) | A class for representing UNIX credentials passed via ancillary data on UNIX domain sockets. |
| --- | --- |
| [DhcpInfo](https://developer.android.com/reference/kotlin/android/net/DhcpInfo) | A simple object for retrieving the results of a DHCP request. |
| [DnsResolver](https://developer.android.com/reference/kotlin/android/net/DnsResolver) | Dns resolver class for asynchronous dns querying Note that if a client sends a query with more than 1 record in the question section but the remote dns server does not support this, it may not respond at all, leading to a timeout. |
| [EthernetNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/EthernetNetworkSpecifier) | A [NetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier) used to identify ethernet interfaces. |
| --- | --- |
| [Ikev2VpnProfile](https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile) | The Ikev2VpnProfile is a configuration for the platform setup of IKEv2/IPsec VPNs. |
| [InetAddresses](https://developer.android.com/reference/kotlin/android/net/InetAddresses) | Utility methods for [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#) implementations. |
| [IpConfiguration](https://developer.android.com/reference/kotlin/android/net/IpConfiguration) | A class representing the IP configuration of a network. |
| --- | --- |
| [IpPrefix](https://developer.android.com/reference/kotlin/android/net/IpPrefix) | This class represents an IP prefix, i. |
| [IpSecAlgorithm](https://developer.android.com/reference/kotlin/android/net/IpSecAlgorithm) | This class represents a single algorithm that can be used by an [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform). |
| [IpSecManager](https://developer.android.com/reference/kotlin/android/net/IpSecManager) | This class contains methods for managing IPsec sessions. |
| --- | --- |
| [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform) | This class represents a transform, which roughly corresponds to an IPsec Security Association. |
| [IpSecTransformState](https://developer.android.com/reference/kotlin/android/net/IpSecTransformState) | This class represents a snapshot of the state of an IpSecTransform |
| [L2capNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/L2capNetworkSpecifier) | A [NetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier) used to identify an L2CAP network over BLE. |
| --- | --- |
| [LinkAddress](https://developer.android.com/reference/kotlin/android/net/LinkAddress) | Identifies an IP address on a network link. |
| [LinkProperties](https://developer.android.com/reference/kotlin/android/net/LinkProperties) | Describes the properties of a network link. |
| [LocalServerSocket](https://developer.android.com/reference/kotlin/android/net/LocalServerSocket) | Non-standard class for creating an inbound UNIX-domain socket in the Linux abstract namespace. |
| --- | --- |
| [LocalSocket](https://developer.android.com/reference/kotlin/android/net/LocalSocket) | Creates a (non-server) socket in the UNIX-domain namespace. |
| [LocalSocketAddress](https://developer.android.com/reference/kotlin/android/net/LocalSocketAddress) | A UNIX-domain (AF_LOCAL) socket address. |
| [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress) | Representation of a MAC address. |
| --- | --- |
| [MailTo](https://developer.android.com/reference/kotlin/android/net/MailTo) | MailTo URL parser This class parses a mailto scheme URL and then can be queried for the parsed parameters. |
| [Network](https://developer.android.com/reference/kotlin/android/net/Network) | Identifies a`Network`. |
| [NetworkCapabilities](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities) | Representation of the capabilities of an active network. |
| --- | --- |
| [NetworkInfo](https://developer.android.com/reference/kotlin/android/net/NetworkInfo) | Describes the status of a network interface. |
| [NetworkRequest](https://developer.android.com/reference/kotlin/android/net/NetworkRequest) | An object describing a network that the application is interested in. |
| [NetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier) | Describes specific properties of a requested network for use in a [NetworkRequest](https://developer.android.com/reference/kotlin/android/net/NetworkRequest). |
| --- | --- |
| [PlatformVpnProfile](https://developer.android.com/reference/kotlin/android/net/PlatformVpnProfile) | PlatformVpnProfile represents a configuration for a platform-based VPN implementation. |
| [Proxy](https://developer.android.com/reference/kotlin/android/net/Proxy) | A convenience class for accessing the user and default proxy settings. |
| [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo) | Describes a proxy configuration. |
| --- | --- |
| [RouteInfo](https://developer.android.com/reference/kotlin/android/net/RouteInfo) | Represents a network route. |
| [SocketKeepalive](https://developer.android.com/reference/kotlin/android/net/SocketKeepalive) | Allows applications to request that the system periodically send specific packets on their behalf, using hardware offload to save battery power. |
| [SSLCertificateSocketFactory](https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory) | SSLSocketFactory implementation with several extra features: - Timeout specification for SSL handshake operations - Hostname verification in most cases (see WARNINGs below) - Optional SSL session caching with [SSLSessionCache](https://developer.android.com/reference/kotlin/android/net/SSLSessionCache) - Optionally bypass all SSL certificate checks The handshake timeout does not apply to actual TCP socket connection. <br /> |
| --- | --- |
| [SSLSessionCache](https://developer.android.com/reference/kotlin/android/net/SSLSessionCache) | File-based cache of established SSL sessions. |
| [StaticIpConfiguration](https://developer.android.com/reference/kotlin/android/net/StaticIpConfiguration) | Class that describes static IP configuration. |
| [TelephonyNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/TelephonyNetworkSpecifier) | NetworkSpecifier object for cellular network request. |
| --- | --- |
| [TetheringInterface](https://developer.android.com/reference/kotlin/android/net/TetheringInterface) | The mapping of tethering interface and type. |
| [TetheringManager](https://developer.android.com/reference/kotlin/android/net/TetheringManager) | This class provides the APIs to control the tethering service. |
| [TrafficStats](https://developer.android.com/reference/kotlin/android/net/TrafficStats) | Class that provides network traffic statistics. |
| --- | --- |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri) | Immutable URI reference. |
| [UrlQuerySanitizer](https://developer.android.com/reference/kotlin/android/net/UrlQuerySanitizer) | Sanitizes the Query portion of a URL. |
| [VpnManager](https://developer.android.com/reference/kotlin/android/net/VpnManager) | This class provides an interface for apps to manage platform VPN profiles |
| --- | --- |
| [VpnProfileState](https://developer.android.com/reference/kotlin/android/net/VpnProfileState) | Describe the state of VPN. |
| [VpnService](https://developer.android.com/reference/kotlin/android/net/VpnService) | VpnService is a base class for applications to extend and build their own VPN solutions. |

## Exceptions

| [ParseException](https://developer.android.com/reference/kotlin/android/net/ParseException) | Thrown when parsing failed. |
| --- | --- |
