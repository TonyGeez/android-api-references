# LDAPCertStoreParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LDAPCertStoreParameters

```
open class LDAPCertStoreParameters : CertStoreParameters
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.cert.LDAPCertStoreParameters](https://developer.android.com/reference/kotlin/java/security/cert/LDAPCertStoreParameters#) |

Parameters used as input for the LDAP`CertStore`algorithm.

This class is used to provide necessary configuration parameters (server name and port number) to implementations of the LDAP`CertStore`algorithm. However, if you are retrieving certificates or CRLs from an ldap URI as specified by RFC 5280, use the [URICertStoreParameters](https://developer.android.com/reference/kotlin/java/security/cert/URICertStoreParameters) instead as the URI may contain additional information such as the distinguished name that will help the LDAP CertStore find the specific certificates and CRLs.

**Concurrent Access**

Unless otherwise specified, the methods defined in this class are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LDAPCertStoreParameters](https://developer.android.com/reference/kotlin/java/security/cert/LDAPCertStoreParameters#LDAPCertStoreParameters())`()` Creates an instance of`LDAPCertStoreParameters`with the default parameter values (server name "localhost", port 389). |
| [LDAPCertStoreParameters](https://developer.android.com/reference/kotlin/java/security/cert/LDAPCertStoreParameters#LDAPCertStoreParameters(kotlin.String))`(`serverName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an instance of`LDAPCertStoreParameters`with the specified server name and a default port of 389. |
| [LDAPCertStoreParameters](https://developer.android.com/reference/kotlin/java/security/cert/LDAPCertStoreParameters#LDAPCertStoreParameters(kotlin.String,%20kotlin.Int))`(`serverName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates an instance of`LDAPCertStoreParameters`with the specified parameter values. |

| Public methods ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/security/cert/LDAPCertStoreParameters#clone())`()` Returns a copy of this object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPort](https://developer.android.com/reference/kotlin/java/security/cert/LDAPCertStoreParameters#getPort())`()` Returns the port number of the LDAP server. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getServerName](https://developer.android.com/reference/kotlin/java/security/cert/LDAPCertStoreParameters#getServerName())`()` Returns the DNS name of the LDAP server. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/security/cert/LDAPCertStoreParameters#toString())`()` Returns a formatted string describing the parameters. |

## Public constructors

### LDAPCertStoreParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LDAPCertStoreParameters()
```

Creates an instance of`LDAPCertStoreParameters`with the default parameter values (server name "localhost", port 389). 

### LDAPCertStoreParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LDAPCertStoreParameters(serverName: String!)
```

Creates an instance of`LDAPCertStoreParameters`with the specified server name and a default port of 389.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------|
| `serverName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the DNS name of the LDAP server |

| Exceptions ||
|----------------------------------|------------------------|
| `java.lang.NullPointerException` | if`serverName`is`null` |

### LDAPCertStoreParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LDAPCertStoreParameters(
    serverName: String!, 
    port: Int)
```

Creates an instance of`LDAPCertStoreParameters`with the specified parameter values.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------|
| `serverName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the DNS name of the LDAP server |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port number of the LDAP server |

| Exceptions ||
|----------------------------------|------------------------|
| `java.lang.NullPointerException` | if`serverName`is`null` |

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Returns a copy of this object. Changes to the copy will not affect the original and vice versa.

Note: this method currently performs a shallow copy of the object (simply calls`Object.clone()`). This may be changed in a future revision to perform a deep copy if new parameters are added that should not be shared.

| Return ||
|----------------------------------------------------------------------------|----------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | the copy |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### getPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPort(): Int
```

Returns the port number of the LDAP server.

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the port number |

### getServerName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getServerName(): String!
```

Returns the DNS name of the LDAP server.

| Return ||
|-----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name (not`null`) |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a formatted string describing the parameters.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a formatted string describing the parameters |
