# java.net

# java.net

## Interfaces

| [ContentHandlerFactory](../java/net/ContentHandlerFactory.md) | This interface defines a factory for content handlers. |
| --- | --- |
| [CookiePolicy](../java/net/CookiePolicy.md) | CookiePolicy implementations decide which cookies should be accepted and which should be rejected. |
| [CookieStore](../java/net/CookieStore.md) | A CookieStore object represents a storage for cookie. |
| [DatagramSocketImplFactory](../java/net/DatagramSocketImplFactory.md) | This interface defines a factory for datagram socket implementations. |
| --- | --- |
| [FileNameMap](../java/net/FileNameMap.md) | A simple interface which provides a mechanism to map between a file name and a MIME type string. |
| [ProtocolFamily](../java/net/ProtocolFamily.md) | Represents a family of communication protocols. |
| [SocketImplFactory](../java/net/SocketImplFactory.md) | This interface defines a factory for socket implementations. |
| --- | --- |
| [SocketOption](../java/net/SocketOption.md) | A socket option associated with a socket. |
| [SocketOptions](../java/net/SocketOptions.md) | Interface of methods to get/set socket options. |
| [URLStreamHandlerFactory](../java/net/URLStreamHandlerFactory.md) | This interface defines a factory for`URL`stream protocol handlers. |
| --- | --- |

## Classes

| [Authenticator](../java/net/Authenticator.md) | The class Authenticator represents an object that knows how to obtain authentication for a network connection. |
| --- | --- |
| [CacheRequest](../java/net/CacheRequest.md) | Represents channels for storing resources in the ResponseCache. |
| [CacheResponse](../java/net/CacheResponse.md) | Represent channels for retrieving resources from the ResponseCache. |
| [ContentHandler](../java/net/ContentHandler.md) | The abstract class`ContentHandler`is the superclass of all classes that read an`Object`from a`URLConnection`. |
| --- | --- |
| [CookieHandler](../java/net/CookieHandler.md) | A CookieHandler object provides a callback mechanism to hook up a HTTP state management policy implementation into the HTTP protocol handler. |
| [CookieManager](../java/net/CookieManager.md) | CookieManager provides a concrete implementation of [CookieHandler](../java/net/CookieHandler.md), which separates the storage of cookies from the policy surrounding accepting and rejecting cookies. |
| [DatagramPacket](../java/net/DatagramPacket.md) | This class represents a datagram packet. |
| --- | --- |
| [DatagramSocket](../java/net/DatagramSocket.md) | This class represents a socket for sending and receiving datagram packets. |
| [DatagramSocketImpl](../java/net/DatagramSocketImpl.md) | Abstract datagram and multicast socket implementation base class. |
| [HttpCookie](../java/net/HttpCookie.md) | An HttpCookie object represents an HTTP cookie, which carries state information between server and user agent. |
| --- | --- |
| [HttpURLConnection](../java/net/HttpURLConnection.md) | A URLConnection with support for HTTP-specific features. |
| [IDN](../java/net/IDN.md) | Provides methods to convert internationalized domain names (IDNs) between a normal Unicode representation and an ASCII Compatible Encoding (ACE) representation. |
| [Inet4Address](../java/net/Inet4Address.md) | This class represents an Internet Protocol version 4 (IPv4) address. |
| --- | --- |
| [Inet6Address](../java/net/Inet6Address.md) | This class represents an Internet Protocol version 6 (IPv6) address. |
| [InetAddress](../java/net/InetAddress.md) | This class represents an Internet Protocol (IP) address. |
| [InetSocketAddress](../java/net/InetSocketAddress.md) | This class implements an IP Socket Address (IP address + port number) It can also be a pair (hostname + port number), in which case an attempt will be made to resolve the hostname. |
| --- | --- |
| [InterfaceAddress](../java/net/InterfaceAddress.md) | This class represents a Network Interface address. |
| [JarURLConnection](../java/net/JarURLConnection.md) | A URL Connection to a Java ARchive (JAR) file or an entry in a JAR file. |
| [MulticastSocket](../java/net/MulticastSocket.md) | The multicast datagram socket class is useful for sending and receiving IP multicast packets. |
| --- | --- |
| [NetPermission](../java/net/NetPermission.md) | Legacy security code; do not use. |
| [NetworkInterface](../java/net/NetworkInterface.md) | This class represents a Network Interface made up of a name, and a list of IP addresses assigned to this interface. |
| [PasswordAuthentication](../java/net/PasswordAuthentication.md) | The class PasswordAuthentication is a data holder that is used by Authenticator. |
| --- | --- |
| [Proxy](../java/net/Proxy.md) | This class represents a proxy setting, typically a type (http, socks) and a socket address. |
| [ProxySelector](../java/net/ProxySelector.md) | Selects the proxy server to use, if any, when connecting to the network resource referenced by a URL. |
| [ResponseCache](../java/net/ResponseCache.md) | Represents implementations of URLConnection caches. |
| --- | --- |
| [SecureCacheResponse](../java/net/SecureCacheResponse.md) | Represents a cache response originally retrieved through secure means, such as TLS. |
| [ServerSocket](../java/net/ServerSocket.md) | This class implements server sockets. |
| [Socket](../java/net/Socket.md) | This class implements client sockets (also called just "sockets"). |
| --- | --- |
| [SocketAddress](../java/net/SocketAddress.md) | This class represents a Socket Address with no protocol attachment. |
| [SocketImpl](../java/net/SocketImpl.md) | The abstract class`SocketImpl`is a common superclass of all classes that actually implement sockets. |
| [SocketPermission](../java/net/SocketPermission.md) | Legacy security code; do not use. |
| --- | --- |
| [StandardSocketOptions](../java/net/StandardSocketOptions.md) | Defines the*standard*socket options. |
| [URI](../java/net/URI.md) | Represents a Uniform Resource Identifier (URI) reference. |
| [URL](../java/net/URL.md) | Class`URL`represents a Uniform Resource Locator, a pointer to a "resource" on the World Wide Web. |
| --- | --- |
| [URLClassLoader](../java/net/URLClassLoader.md) | This class loader is used to load classes and resources from a search path of URLs referring to both JAR files and directories. |
| [URLConnection](../java/net/URLConnection.md) | The abstract class is the superclass of all classes that represent a communications link between the application and a URL. |
| [URLDecoder](../java/net/URLDecoder.md) | Utility class for HTML form decoding. |
| --- | --- |
| [URLEncoder](../java/net/URLEncoder.md) | Utility class for HTML form encoding. |
| [URLStreamHandler](../java/net/URLStreamHandler.md) | The abstract class`URLStreamHandler`is the common superclass for all stream protocol handlers. |

## Exceptions

| [BindException](../java/net/BindException.md) | Signals that an error occurred while attempting to bind a socket to a local address and port. |
| --- | --- |
| [ConnectException](../java/net/ConnectException.md) | Signals that an error occurred while attempting to connect a socket to a remote address and port. |
| [HttpRetryException](../java/net/HttpRetryException.md) | Thrown to indicate that a HTTP request needs to be retried but cannot be retried automatically, due to streaming mode being enabled. |
| [MalformedURLException](../java/net/MalformedURLException.md) | Thrown to indicate that a malformed URL has occurred. |
| --- | --- |
| [NoRouteToHostException](../java/net/NoRouteToHostException.md) | Signals that an error occurred while attempting to connect a socket to a remote address and port. |
| [PortUnreachableException](../java/net/PortUnreachableException.md) | Signals that an ICMP Port Unreachable message has been received on a connected datagram. |
| [ProtocolException](../java/net/ProtocolException.md) | Thrown to indicate that there is an error in the underlying protocol, such as a TCP error. |
| --- | --- |
| [SocketException](../java/net/SocketException.md) | Thrown to indicate that there is an error creating or accessing a Socket. |
| [SocketTimeoutException](../java/net/SocketTimeoutException.md) | Signals that a timeout has occurred on a socket read or accept. |
| [UnknownHostException](../java/net/UnknownHostException.md) | Thrown to indicate that the IP address of a host could not be determined. |
| --- | --- |
| [UnknownServiceException](../java/net/UnknownServiceException.md) | Thrown to indicate that an unknown service exception has occurred. |
| [URISyntaxException](../java/net/URISyntaxException.md) | Checked exception thrown to indicate that a string could not be parsed as a URI reference. |

## Enums

| [StandardProtocolFamily](../java/net/StandardProtocolFamily.md) | Defines the standard families of communication protocols. |
| --- | --- |
