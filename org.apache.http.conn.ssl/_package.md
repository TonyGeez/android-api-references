# org.apache.http.conn.ssl

# org.apache.http.conn.ssl

## Interfaces

| [X509HostnameVerifier](X509HostnameVerifier.md) | Interface for checking if a hostname matches the names stored inside the server's X. |
| --- | --- |

## Classes

| [AbstractVerifier](AbstractVerifier.md) | Abstract base class for all standard [X509HostnameVerifier](X509HostnameVerifier.md) implementations. |
| --- | --- |
| [AllowAllHostnameVerifier](AllowAllHostnameVerifier.md) | The ALLOW_ALL HostnameVerifier essentially turns hostname verification off. |
| [BrowserCompatHostnameVerifier](BrowserCompatHostnameVerifier.md) | The HostnameVerifier that works the same way as Curl and Firefox. |
| [SSLSocketFactory](SSLSocketFactory.md) | Layered socket factory for TLS/SSL connections, based on JSSE. |
| --- | --- |
| [StrictHostnameVerifier](StrictHostnameVerifier.md) | The Strict HostnameVerifier works the same way as Sun Java 1. |
