# org.apache.http.conn.ssl

# org.apache.http.conn.ssl

## Interfaces

| [X509HostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier) | Interface for checking if a hostname matches the names stored inside the server's X. |

## Classes

| [AbstractVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier) | Abstract base class for all standard [X509HostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier) implementations. |
| [AllowAllHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AllowAllHostnameVerifier) | The ALLOW_ALL HostnameVerifier essentially turns hostname verification off. |
| [BrowserCompatHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/BrowserCompatHostnameVerifier) | The HostnameVerifier that works the same way as Curl and Firefox. |
| [SSLSocketFactory](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/SSLSocketFactory) | Layered socket factory for TLS/SSL connections, based on JSSE. |
| [StrictHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/StrictHostnameVerifier) | The Strict HostnameVerifier works the same way as Sun Java 1. |
