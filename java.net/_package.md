# java.net

# java.net

## Interfaces

| [ContentHandlerFactory](https://developer.android.com/reference/kotlin/java/net/ContentHandlerFactory) | This interface defines a factory for content handlers. |
| [CookiePolicy](https://developer.android.com/reference/kotlin/java/net/CookiePolicy) | CookiePolicy implementations decide which cookies should be accepted and which should be rejected. |
| [CookieStore](https://developer.android.com/reference/kotlin/java/net/CookieStore) | A CookieStore object represents a storage for cookie. |
| [DatagramSocketImplFactory](https://developer.android.com/reference/kotlin/java/net/DatagramSocketImplFactory) | This interface defines a factory for datagram socket implementations. |
| [FileNameMap](https://developer.android.com/reference/kotlin/java/net/FileNameMap) | A simple interface which provides a mechanism to map between a file name and a MIME type string. |
| [ProtocolFamily](https://developer.android.com/reference/kotlin/java/net/ProtocolFamily) | Represents a family of communication protocols. |
| [SocketImplFactory](https://developer.android.com/reference/kotlin/java/net/SocketImplFactory) | This interface defines a factory for socket implementations. |
| [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption) | A socket option associated with a socket. |
| [SocketOptions](https://developer.android.com/reference/kotlin/java/net/SocketOptions) | Interface of methods to get/set socket options. |
| [URLStreamHandlerFactory](https://developer.android.com/reference/kotlin/java/net/URLStreamHandlerFactory) | This interface defines a factory for`URL`stream protocol handlers. |

## Classes

| [Authenticator](https://developer.android.com/reference/kotlin/java/net/Authenticator) | The class Authenticator represents an object that knows how to obtain authentication for a network connection. |
| [CacheRequest](https://developer.android.com/reference/kotlin/java/net/CacheRequest) | Represents channels for storing resources in the ResponseCache. |
| [CacheResponse](https://developer.android.com/reference/kotlin/java/net/CacheResponse) | Represent channels for retrieving resources from the ResponseCache. |
| [ContentHandler](https://developer.android.com/reference/kotlin/java/net/ContentHandler) | The abstract class`ContentHandler`is the superclass of all classes that read an`Object`from a`URLConnection`. |
| [CookieHandler](https://developer.android.com/reference/kotlin/java/net/CookieHandler) | A CookieHandler object provides a callback mechanism to hook up a HTTP state management policy implementation into the HTTP protocol handler. |
| [CookieManager](https://developer.android.com/reference/kotlin/java/net/CookieManager) | CookieManager provides a concrete implementation of [CookieHandler](https://developer.android.com/reference/kotlin/java/net/CookieHandler), which separates the storage of cookies from the policy surrounding accepting and rejecting cookies. |
| [DatagramPacket](https://developer.android.com/reference/kotlin/java/net/DatagramPacket) | This class represents a datagram packet. |
| [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket) | This class represents a socket for sending and receiving datagram packets. |
| [DatagramSocketImpl](https://developer.android.com/reference/kotlin/java/net/DatagramSocketImpl) | Abstract datagram and multicast socket implementation base class. |
| [HttpCookie](https://developer.android.com/reference/kotlin/java/net/HttpCookie) | An HttpCookie object represents an HTTP cookie, which carries state information between server and user agent. |
| [HttpURLConnection](https://developer.android.com/reference/kotlin/java/net/HttpURLConnection) | A URLConnection with support for HTTP-specific features. |
| [IDN](https://developer.android.com/reference/kotlin/java/net/IDN) | Provides methods to convert internationalized domain names (IDNs) between a normal Unicode representation and an ASCII Compatible Encoding (ACE) representation. |
| [Inet4Address](https://developer.android.com/reference/kotlin/java/net/Inet4Address) | This class represents an Internet Protocol version 4 (IPv4) address. |
| [Inet6Address](https://developer.android.com/reference/kotlin/java/net/Inet6Address) | This class represents an Internet Protocol version 6 (IPv6) address. |
| [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress) | This class represents an Internet Protocol (IP) address. |
| [InetSocketAddress](https://developer.android.com/reference/kotlin/java/net/InetSocketAddress) | This class implements an IP Socket Address (IP address + port number) It can also be a pair (hostname + port number), in which case an attempt will be made to resolve the hostname. |
| [InterfaceAddress](https://developer.android.com/reference/kotlin/java/net/InterfaceAddress) | This class represents a Network Interface address. |
| [JarURLConnection](https://developer.android.com/reference/kotlin/java/net/JarURLConnection) | A URL Connection to a Java ARchive (JAR) file or an entry in a JAR file. |
| [MulticastSocket](https://developer.android.com/reference/kotlin/java/net/MulticastSocket) | The multicast datagram socket class is useful for sending and receiving IP multicast packets. |
| [NetPermission](https://developer.android.com/reference/kotlin/java/net/NetPermission) | Legacy security code; do not use. |
| [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface) | This class represents a Network Interface made up of a name, and a list of IP addresses assigned to this interface. |
| [PasswordAuthentication](https://developer.android.com/reference/kotlin/java/net/PasswordAuthentication) | The class PasswordAuthentication is a data holder that is used by Authenticator. |
| [Proxy](https://developer.android.com/reference/kotlin/java/net/Proxy) | This class represents a proxy setting, typically a type (http, socks) and a socket address. |
| [ProxySelector](https://developer.android.com/reference/kotlin/java/net/ProxySelector) | Selects the proxy server to use, if any, when connecting to the network resource referenced by a URL. |
| [ResponseCache](https://developer.android.com/reference/kotlin/java/net/ResponseCache) | Represents implementations of URLConnection caches. |
| [SecureCacheResponse](https://developer.android.com/reference/kotlin/java/net/SecureCacheResponse) | Represents a cache response originally retrieved through secure means, such as TLS. |
| [ServerSocket](https://developer.android.com/reference/kotlin/java/net/ServerSocket) | This class implements server sockets. |
| [Socket](https://developer.android.com/reference/kotlin/java/net/Socket) | This class implements client sockets (also called just "sockets"). |
| [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress) | This class represents a Socket Address with no protocol attachment. |
| [SocketImpl](https://developer.android.com/reference/kotlin/java/net/SocketImpl) | The abstract class`SocketImpl`is a common superclass of all classes that actually implement sockets. |
| [SocketPermission](https://developer.android.com/reference/kotlin/java/net/SocketPermission) | Legacy security code; do not use. |
| [StandardSocketOptions](https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions) | Defines the*standard*socket options. |
| [URI](https://developer.android.com/reference/kotlin/java/net/URI) | Represents a Uniform Resource Identifier (URI) reference. |
| [URL](https://developer.android.com/reference/kotlin/java/net/URL) | Class`URL`represents a Uniform Resource Locator, a pointer to a "resource" on the World Wide Web. |
| [URLClassLoader](https://developer.android.com/reference/kotlin/java/net/URLClassLoader) | This class loader is used to load classes and resources from a search path of URLs referring to both JAR files and directories. |
| [URLConnection](https://developer.android.com/reference/kotlin/java/net/URLConnection) | The abstract class is the superclass of all classes that represent a communications link between the application and a URL. |
| [URLDecoder](https://developer.android.com/reference/kotlin/java/net/URLDecoder) | Utility class for HTML form decoding. |
| [URLEncoder](https://developer.android.com/reference/kotlin/java/net/URLEncoder) | Utility class for HTML form encoding. |
| [URLStreamHandler](https://developer.android.com/reference/kotlin/java/net/URLStreamHandler) | The abstract class`URLStreamHandler`is the common superclass for all stream protocol handlers. |

## Exceptions

| [BindException](https://developer.android.com/reference/kotlin/java/net/BindException) | Signals that an error occurred while attempting to bind a socket to a local address and port. |
| [ConnectException](https://developer.android.com/reference/kotlin/java/net/ConnectException) | Signals that an error occurred while attempting to connect a socket to a remote address and port. |
| [HttpRetryException](https://developer.android.com/reference/kotlin/java/net/HttpRetryException) | Thrown to indicate that a HTTP request needs to be retried but cannot be retried automatically, due to streaming mode being enabled. |
| [MalformedURLException](https://developer.android.com/reference/kotlin/java/net/MalformedURLException) | Thrown to indicate that a malformed URL has occurred. |
| [NoRouteToHostException](https://developer.android.com/reference/kotlin/java/net/NoRouteToHostException) | Signals that an error occurred while attempting to connect a socket to a remote address and port. |
| [PortUnreachableException](https://developer.android.com/reference/kotlin/java/net/PortUnreachableException) | Signals that an ICMP Port Unreachable message has been received on a connected datagram. |
| [ProtocolException](https://developer.android.com/reference/kotlin/java/net/ProtocolException) | Thrown to indicate that there is an error in the underlying protocol, such as a TCP error. |
| [SocketException](https://developer.android.com/reference/kotlin/java/net/SocketException) | Thrown to indicate that there is an error creating or accessing a Socket. |
| [SocketTimeoutException](https://developer.android.com/reference/kotlin/java/net/SocketTimeoutException) | Signals that a timeout has occurred on a socket read or accept. |
| [UnknownHostException](https://developer.android.com/reference/kotlin/java/net/UnknownHostException) | Thrown to indicate that the IP address of a host could not be determined. |
| [UnknownServiceException](https://developer.android.com/reference/kotlin/java/net/UnknownServiceException) | Thrown to indicate that an unknown service exception has occurred. |
| [URISyntaxException](https://developer.android.com/reference/kotlin/java/net/URISyntaxException) | Checked exception thrown to indicate that a string could not be parsed as a URI reference. |

## Enums

| [StandardProtocolFamily](https://developer.android.com/reference/kotlin/java/net/StandardProtocolFamily) | Defines the standard families of communication protocols. |
