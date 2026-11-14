# org.apache.http.conn.ssl

# org.apache.http.conn.ssl

## Interfaces

| [X509HostnameVerifier](../org/apache/http/conn/ssl/X509HostnameVerifier.md) | Interface for checking if a hostname matches the names stored inside the server's X. |
| --- | --- |

## Classes

| [AbstractVerifier](../org/apache/http/conn/ssl/AbstractVerifier.md) | Abstract base class for all standard [X509HostnameVerifier](../org/apache/http/conn/ssl/X509HostnameVerifier.md) implementations. |
| --- | --- |
| [AllowAllHostnameVerifier](../org/apache/http/conn/ssl/AllowAllHostnameVerifier.md) | The ALLOW_ALL HostnameVerifier essentially turns hostname verification off. |
| [BrowserCompatHostnameVerifier](../org/apache/http/conn/ssl/BrowserCompatHostnameVerifier.md) | The HostnameVerifier that works the same way as Curl and Firefox. |
| [SSLSocketFactory](../org/apache/http/conn/ssl/SSLSocketFactory.md) | Layered socket factory for TLS/SSL connections, based on JSSE. |
| --- | --- |
| [StrictHostnameVerifier](../org/apache/http/conn/ssl/StrictHostnameVerifier.md) | The Strict HostnameVerifier works the same way as Sun Java 1. |
