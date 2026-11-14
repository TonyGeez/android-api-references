# Security

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Security

```
class Security
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.Security](https://developer.android.com/reference/kotlin/java/security/Security#) |

This class centralizes all security properties and common security methods. One of its primary uses is to manage providers.

The default values of security properties are read from an implementation-specific location, which is typically the properties file`lib/security/java.security`in the Java installation directory.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [addProvider](https://developer.android.com/reference/kotlin/java/security/Security#addProvider(java.security.Provider))`(`provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!`)` Adds a provider to the next position available. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithmProperty](https://developer.android.com/reference/kotlin/java/security/Security#getAlgorithmProperty(kotlin.String,%20kotlin.String))`(`algName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `propName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets a specified property for an algorithm. |
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getAlgorithms](https://developer.android.com/reference/kotlin/java/security/Security#getAlgorithms(kotlin.String))`(`serviceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a Set of Strings containing the names of all available algorithms or types for the specified Java cryptographic service (e.g., Signature, MessageDigest, Cipher, Mac, KeyStore). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getProperty](https://developer.android.com/reference/kotlin/java/security/Security#getProperty(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets a security property value. |
| static [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)! | [getProvider](https://developer.android.com/reference/kotlin/java/security/Security#getProvider(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the provider installed with the specified name, if any. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!\>! | [getProviders](https://developer.android.com/reference/kotlin/java/security/Security#getProviders())`()` Returns an array containing all the installed providers. |
| --- | --- |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!\>! | [getProviders](https://developer.android.com/reference/kotlin/java/security/Security#getProviders(kotlin.String))`(`filter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns an array containing all installed providers that satisfy the specified selection criterion, or null if no such providers have been installed. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!\>! | [getProviders](https://developer.android.com/reference/kotlin/java/security/Security#getProviders(kotlin.collections.MutableMap))`(`filter:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Returns an array containing all installed providers that satisfy the specified\* selection criteria, or null if no such providers have been installed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [insertProviderAt](https://developer.android.com/reference/kotlin/java/security/Security#insertProviderAt(java.security.Provider,%20kotlin.Int))`(`provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!`, `position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adds a new provider, at a specified position. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeProvider](https://developer.android.com/reference/kotlin/java/security/Security#removeProvider(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Removes the provider with the specified name. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperty](https://developer.android.com/reference/kotlin/java/security/Security#setProperty(kotlin.String,%20kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `datum:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets a security property value. |

## Public methods

### addProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun addProvider(provider: Provider!): Int
```

Adds a provider to the next position available.

If there is a security manager, the [java.lang.SecurityManager#checkSecurityAccess](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String))method is called with the`"insertProvider"`permission target name to see if it's ok to add a new provider. If this permission check is denied,`checkSecurityAccess`is called again with the`"insertProvider."+provider.getName()`permission target name. If both checks are denied, a`SecurityException`is thrown.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!:the provider to be added. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the preference position in which the provider was added, or -1 if the provider was not added because it is already installed. |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if provider is null |
| `java.lang.SecurityException` | if a security manager exists and its [java.lang.SecurityManager#checkSecurityAccess](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String))method denies access to add a new provider |

**See Also**

- [#getProvider](https://developer.android.com/reference/kotlin/java/security/Security#getProvider(kotlin.String))
- [#removeProvider](https://developer.android.com/reference/kotlin/java/security/Security#removeProvider(kotlin.String))
- [java.security.SecurityPermission](https://developer.android.com/reference/kotlin/java/security/SecurityPermission) 

### getAlgorithmProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAlgorithmProperty(
    algName: String!, 
    propName: String!
): String!
```

**Deprecated:** *This method used to return the value of a proprietary property in the master file of the "SUN" Cryptographic Service Provider in order to determine how to parse algorithm-specific parameters. Use the new provider-based and algorithm-independent`AlgorithmParameters`and`KeyFactory`engine classes (introduced in the J2SE version 1.2 platform) instead.*

Gets a specified property for an algorithm. The algorithm name should be a standard name. See the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html) for information about standard algorithm names. One possible use is by specialized algorithm parsers, which may map classes to algorithms which they understand (much like Key parsers do).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------|
| `algName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm name. |
| `propName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the property to get. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the value of the specified property. |

### getAlgorithms

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAlgorithms(serviceName: String!): MutableSet<String!>!
```

Returns a Set of Strings containing the names of all available algorithms or types for the specified Java cryptographic service (e.g., Signature, MessageDigest, Cipher, Mac, KeyStore). Returns an empty Set if there is no provider that supports the specified service or if serviceName is null. For a complete list of Java cryptographic services, please see the [Java Cryptography Architecture API Specification \& Reference](https://docs.oracle.com/javase/8/docs/technotes/guides/security/crypto/CryptoSpec.html). Note: the returned set is immutable.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `serviceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the Java cryptographic service (e.g., Signature, MessageDigest, Cipher, Mac, KeyStore). Note: this parameter is case-insensitive. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | a Set of Strings containing the names of all available algorithms or types for the specified Java cryptographic service or an empty set if no provider supports the specified service. |

### getProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getProperty(key: String!): String!
```

Gets a security property value.

First, if there is a security manager, its`checkPermission`method is called with a`java.security.SecurityPermission("getProperty."+key)`permission to see if it's ok to retrieve the specified security property value..

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the key of the property being retrieved. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the value of the security property corresponding to key. |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its java.lang.SecurityManager#checkPermission method denies access to retrieve the specified security property value |
| `java.lang.NullPointerException` | is key is null |

**See Also**

- [#setProperty](https://developer.android.com/reference/kotlin/java/security/Security#setProperty(kotlin.String,%20kotlin.String))
- [java.security.SecurityPermission](https://developer.android.com/reference/kotlin/java/security/SecurityPermission) 

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getProvider(name: String!): Provider!
```

Returns the provider installed with the specified name, if any. Returns null if no provider with the specified name is installed or if name is null.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider to get. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)! | the provider of the specified name. |

**See Also**

- [#removeProvider](https://developer.android.com/reference/kotlin/java/security/Security#removeProvider(kotlin.String))
- [#addProvider](https://developer.android.com/reference/kotlin/java/security/Security#addProvider(java.security.Provider)) 

### getProviders

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getProviders(): Array<Provider!>!
```

Returns an array containing all the installed providers. The order of the providers in the array is their preference order.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!>! | an array of all the installed providers. |

### getProviders

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getProviders(filter: String!): Array<Provider!>!
```

Returns an array containing all installed providers that satisfy the specified selection criterion, or null if no such providers have been installed. The returned providers are ordered according to their [preference order](https://developer.android.com/reference/kotlin/java/security/Security#insertProviderAt(java.security.Provider,%20kotlin.Int)).

A cryptographic service is always associated with a particular algorithm or type. For example, a digital signature service is always associated with a particular algorithm (e.g., DSA), and a CertificateFactory service is always associated with a particular certificate type (e.g., X.509).

The selection criterion must be specified in one of the following two formats:

- *\<crypto_service\>.\<algorithm_or_type\>*

 The cryptographic service name must not contain any dots.

 A provider satisfies the specified selection criterion iff the provider implements the specified algorithm or type for the specified cryptographic service.

 For example, "CertificateFactory.X.509" would be satisfied by any provider that supplied a CertificateFactory implementation for X.509 certificates.
- *\<crypto_service\>.\<algorithm_or_type\> \<attribute_name\>:\<attribute_value\>*

 The cryptographic service name must not contain any dots. There must be one or more space characters between the*\<algorithm_or_type\>* and the*\<attribute_name\>*.

 A provider satisfies this selection criterion iff the provider implements the specified algorithm or type for the specified cryptographic service and its implementation meets the constraint expressed by the specified attribute name/value pair.

 For example, "Signature.SHA1withDSA KeySize:1024" would be satisfied by any provider that implemented the SHA1withDSA signature algorithm with a keysize of 1024 (or larger).

See the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html) for information about standard cryptographic service names, standard algorithm names and standard attribute names.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the criterion for selecting providers. The filter is case-insensitive. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!>! | all the installed providers that satisfy the selection criterion, or null if no such providers have been installed. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------|
| `java.security.InvalidParameterException` | if the filter is not in the required format |
| `java.lang.NullPointerException` | if filter is null |

**See Also**

- [#getProviders(java.util.Map)](https://developer.android.com/reference/kotlin/java/security/Security#getProviders(kotlin.collections.MutableMap)) 

### getProviders

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getProviders(filter: MutableMap<String!, String!>!): Array<Provider!>!
```

Returns an array containing all installed providers that satisfy the specified\* selection criteria, or null if no such providers have been installed. The returned providers are ordered according to their [preference order](https://developer.android.com/reference/kotlin/java/security/Security#insertProviderAt(java.security.Provider,%20kotlin.Int)).

The selection criteria are represented by a map. Each map entry represents a selection criterion. A provider is selected iff it satisfies all selection criteria. The key for any entry in such a map must be in one of the following two formats:

- *\<crypto_service\>.\<algorithm_or_type\>*

 The cryptographic service name must not contain any dots.

 The value associated with the key must be an empty string.

 A provider satisfies this selection criterion iff the provider implements the specified algorithm or type for the specified cryptographic service.
- *\<crypto_service\>. \<algorithm_or_type\> \<attribute_name\>*

 The cryptographic service name must not contain any dots. There must be one or more space characters between the*\<algorithm_or_type\>* and the*\<attribute_name\>*.

 The value associated with the key must be a non-empty string. A provider satisfies this selection criterion iff the provider implements the specified algorithm or type for the specified cryptographic service and its implementation meets the constraint expressed by the specified attribute name/value pair.

See the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html) for information about standard cryptographic service names, standard algorithm names and standard attribute names.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filter` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the criteria for selecting providers. The filter is case-insensitive. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!>! | all the installed providers that satisfy the selection criteria, or null if no such providers have been installed. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------|
| `java.security.InvalidParameterException` | if the filter is not in the required format |
| `java.lang.NullPointerException` | if filter is null |

**See Also**

- [#getProviders(java.lang.String)](https://developer.android.com/reference/kotlin/java/security/Security#getProviders(kotlin.String)) 

### insertProviderAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun insertProviderAt(
    provider: Provider!, 
    position: Int
): Int
```

Adds a new provider, at a specified position. The position is the preference order in which providers are searched for requested algorithms. The position is 1-based, that is, 1 is most preferred, followed by 2, and so on.

If the given provider is installed at the requested position, the provider that used to be at that position, and all providers with a position greater than`position`, are shifted up one position (towards the end of the list of installed providers).

A provider cannot be added if it is already installed.

If there is a security manager, the [java.lang.SecurityManager#checkSecurityAccess](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String))method is called with the`"insertProvider"`permission target name to see if it's ok to add a new provider. If this permission check is denied,`checkSecurityAccess`is called again with the`"insertProvider."+provider.getName()`permission target name. If both checks are denied, a`SecurityException`is thrown.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!:the provider to be added. |
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the preference position that the caller would like for this provider. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the actual preference position in which the provider was added, or -1 if the provider was not added because it is already installed. |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if provider is null |
| `java.lang.SecurityException` | if a security manager exists and its [java.lang.SecurityManager#checkSecurityAccess](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String))method denies access to add a new provider |

**See Also**

- [#getProvider](https://developer.android.com/reference/kotlin/java/security/Security#getProvider(kotlin.String))
- [#removeProvider](https://developer.android.com/reference/kotlin/java/security/Security#removeProvider(kotlin.String))
- [java.security.SecurityPermission](https://developer.android.com/reference/kotlin/java/security/SecurityPermission) 

### removeProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun removeProvider(name: String!): Unit
```

Removes the provider with the specified name.

When the specified provider is removed, all providers located at a position greater than where the specified provider was are shifted down one position (towards the head of the list of installed providers).

This method returns silently if the provider is not installed or if name is null.

First, if there is a security manager, its`checkSecurityAccess`method is called with the string`"removeProvider."+name`to see if it's ok to remove the provider. If the default implementation of`checkSecurityAccess`is used (i.e., that method is not overriden), then this will result in a call to the security manager's`checkPermission`method with a`SecurityPermission("removeProvider."+name)`permission.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider to remove. |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its [java.lang.SecurityManager#checkSecurityAccess](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String))method denies access to remove the provider |

**See Also**

- [#getProvider](https://developer.android.com/reference/kotlin/java/security/Security#getProvider(kotlin.String))
- [#addProvider](https://developer.android.com/reference/kotlin/java/security/Security#addProvider(java.security.Provider)) 

### setProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setProperty(
    key: String!, 
    datum: String!
): Unit
```

Sets a security property value.

First, if there is a security manager, its`checkPermission`method is called with a`java.security.SecurityPermission("setProperty."+key)`permission to see if it's ok to set the specified security property value.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the property to be set. |
| `datum` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the value of the property to be set. |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its java.lang.SecurityManager#checkPermission method denies access to set the specified security property value |
| `java.lang.NullPointerException` | if key or datum is null |

**See Also**

- [#getProperty](https://developer.android.com/reference/kotlin/java/security/Security#getProperty(kotlin.String))
- [java.security.SecurityPermission](https://developer.android.com/reference/kotlin/java/security/SecurityPermission)
