# java.net

# java.net

## Interfaces

| [ContentHandlerFactory](ContentHandlerFactory.md) | This interface defines a factory for content handlers. |
| --- | --- |
| [CookiePolicy](CookiePolicy.md) | CookiePolicy implementations decide which cookies should be accepted and which should be rejected. |
| [CookieStore](CookieStore.md) | A CookieStore object represents a storage for cookie. |
| [DatagramSocketImplFactory](DatagramSocketImplFactory.md) | This interface defines a factory for datagram socket implementations. |
| --- | --- |
| [FileNameMap](FileNameMap.md) | A simple interface which provides a mechanism to map between a file name and a MIME type string. |
| [ProtocolFamily](ProtocolFamily.md) | Represents a family of communication protocols. |
| [SocketImplFactory](SocketImplFactory.md) | This interface defines a factory for socket implementations. |
| --- | --- |
| [SocketOption](SocketOption.md) | A socket option associated with a socket. |
| [SocketOptions](SocketOptions.md) | Interface of methods to get/set socket options. |
| [URLStreamHandlerFactory](URLStreamHandlerFactory.md) | This interface defines a factory for`URL`stream protocol handlers. |
| --- | --- |

## Classes

| [Authenticator](Authenticator.md) | The class Authenticator represents an object that knows how to obtain authentication for a network connection. |
| --- | --- |
| [CacheRequest](CacheRequest.md) | Represents channels for storing resources in the ResponseCache. |
| [CacheResponse](CacheResponse.md) | Represent channels for retrieving resources from the ResponseCache. |
| [ContentHandler](ContentHandler.md) | The abstract class`ContentHandler`is the superclass of all classes that read an`Object`from a`URLConnection`. |
| --- | --- |
| [CookieHandler](CookieHandler.md) | A CookieHandler object provides a callback mechanism to hook up a HTTP state management policy implementation into the HTTP protocol handler. |
| [CookieManager](CookieManager.md) | CookieManager provides a concrete implementation of [CookieHandler](CookieHandler.md), which separates the storage of cookies from the policy surrounding accepting and rejecting cookies. |
| [DatagramPacket](DatagramPacket.md) | This class represents a datagram packet. |
| --- | --- |
| [DatagramSocket](DatagramSocket.md) | This class represents a socket for sending and receiving datagram packets. |
| [DatagramSocketImpl](DatagramSocketImpl.md) | Abstract datagram and multicast socket implementation base class. |
| [HttpCookie](HttpCookie.md) | An HttpCookie object represents an HTTP cookie, which carries state information between server and user agent. |
| --- | --- |
| [HttpURLConnection](HttpURLConnection.md) | A URLConnection with support for HTTP-specific features. |
| [IDN](IDN.md) | Provides methods to convert internationalized domain names (IDNs) between a normal Unicode representation and an ASCII Compatible Encoding (ACE) representation. |
| [Inet4Address](Inet4Address.md) | This class represents an Internet Protocol version 4 (IPv4) address. |
| --- | --- |
| [Inet6Address](Inet6Address.md) | This class represents an Internet Protocol version 6 (IPv6) address. |
| [InetAddress](InetAddress.md) | This class represents an Internet Protocol (IP) address. |
| [InetSocketAddress](InetSocketAddress.md) | This class implements an IP Socket Address (IP address + port number) It can also be a pair (hostname + port number), in which case an attempt will be made to resolve the hostname. |
| --- | --- |
| [InterfaceAddress](InterfaceAddress.md) | This class represents a Network Interface address. |
| [JarURLConnection](JarURLConnection.md) | A URL Connection to a Java ARchive (JAR) file or an entry in a JAR file. |
| [MulticastSocket](MulticastSocket.md) | The multicast datagram socket class is useful for sending and receiving IP multicast packets. |
| --- | --- |
| [NetPermission](NetPermission.md) | Legacy security code; do not use. |
| [NetworkInterface](NetworkInterface.md) | This class represents a Network Interface made up of a name, and a list of IP addresses assigned to this interface. |
| [PasswordAuthentication](PasswordAuthentication.md) | The class PasswordAuthentication is a data holder that is used by Authenticator. |
| --- | --- |
| [Proxy](Proxy.md) | This class represents a proxy setting, typically a type (http, socks) and a socket address. |
| [ProxySelector](ProxySelector.md) | Selects the proxy server to use, if any, when connecting to the network resource referenced by a URL. |
| [ResponseCache](ResponseCache.md) | Represents implementations of URLConnection caches. |
| --- | --- |
| [SecureCacheResponse](SecureCacheResponse.md) | Represents a cache response originally retrieved through secure means, such as TLS. |
| [ServerSocket](ServerSocket.md) | This class implements server sockets. |
| [Socket](Socket.md) | This class implements client sockets (also called just "sockets"). |
| --- | --- |
| [SocketAddress](SocketAddress.md) | This class represents a Socket Address with no protocol attachment. |
| [SocketImpl](SocketImpl.md) | The abstract class`SocketImpl`is a common superclass of all classes that actually implement sockets. |
| [SocketPermission](SocketPermission.md) | Legacy security code; do not use. |
| --- | --- |
| [StandardSocketOptions](StandardSocketOptions.md) | Defines the*standard*socket options. |
| [URI](URI.md) | Represents a Uniform Resource Identifier (URI) reference. |
| [URL](URL.md) | Class`URL`represents a Uniform Resource Locator, a pointer to a "resource" on the World Wide Web. |
| --- | --- |
| [URLClassLoader](URLClassLoader.md) | This class loader is used to load classes and resources from a search path of URLs referring to both JAR files and directories. |
| [URLConnection](URLConnection.md) | The abstract class is the superclass of all classes that represent a communications link between the application and a URL. |
| [URLDecoder](URLDecoder.md) | Utility class for HTML form decoding. |
| --- | --- |
| [URLEncoder](URLEncoder.md) | Utility class for HTML form encoding. |
| [URLStreamHandler](URLStreamHandler.md) | The abstract class`URLStreamHandler`is the common superclass for all stream protocol handlers. |

## Exceptions

| [BindException](BindException.md) | Signals that an error occurred while attempting to bind a socket to a local address and port. |
| --- | --- |
| [ConnectException](ConnectException.md) | Signals that an error occurred while attempting to connect a socket to a remote address and port. |
| [HttpRetryException](HttpRetryException.md) | Thrown to indicate that a HTTP request needs to be retried but cannot be retried automatically, due to streaming mode being enabled. |
| [MalformedURLException](MalformedURLException.md) | Thrown to indicate that a malformed URL has occurred. |
| --- | --- |
| [NoRouteToHostException](NoRouteToHostException.md) | Signals that an error occurred while attempting to connect a socket to a remote address and port. |
| [PortUnreachableException](PortUnreachableException.md) | Signals that an ICMP Port Unreachable message has been received on a connected datagram. |
| [ProtocolException](ProtocolException.md) | Thrown to indicate that there is an error in the underlying protocol, such as a TCP error. |
| --- | --- |
| [SocketException](SocketException.md) | Thrown to indicate that there is an error creating or accessing a Socket. |
| [SocketTimeoutException](SocketTimeoutException.md) | Signals that a timeout has occurred on a socket read or accept. |
| [UnknownHostException](UnknownHostException.md) | Thrown to indicate that the IP address of a host could not be determined. |
| --- | --- |
| [UnknownServiceException](UnknownServiceException.md) | Thrown to indicate that an unknown service exception has occurred. |
| [URISyntaxException](URISyntaxException.md) | Checked exception thrown to indicate that a string could not be parsed as a URI reference. |

## Enums

| [StandardProtocolFamily](StandardProtocolFamily.md) | Defines the standard families of communication protocols. |
| --- | --- |
