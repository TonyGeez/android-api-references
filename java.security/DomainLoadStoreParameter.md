# DomainLoadStoreParameter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DomainLoadStoreParameter

```
class DomainLoadStoreParameter : KeyStore.LoadStoreParameter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.DomainLoadStoreParameter](DomainLoadStoreParameter.md) |

Configuration data that specifies the keystores in a keystore domain. A keystore domain is a collection of keystores that are presented as a single logical keystore. The configuration data is used during`KeyStore` [load](KeyStore.md)) [store](KeyStore.md))operations.

The following syntax is supported for configuration data: 

```kotlin
<code>domain &lt;domainName&gt; [&lt;property&gt; ...] {
          keystore &lt;keystoreName&gt; [&lt;property&gt; ...] ;
          ...
      };
      ...
  </code>
```
where`domainName`and`keystoreName`are identifiers and`property`is a key/value pairing. The key and value are separated by an 'equals' symbol and the value is enclosed in double quotes. A property value may be either a printable string or a binary string of colon-separated pairs of hexadecimal digits. Multi-valued properties are represented as a comma-separated list of values, enclosed in square brackets. See[Arrays.toString(java.lang.Object[])](https://developer.android.com/reference/kotlin/java/util/Arrays.html#toString(kotlin.Array)).

To ensure that keystore entries are uniquely identified, each entry's alias is prefixed by its`keystoreName`followed by the entry name separator and each`keystoreName`must be unique within its domain. Entry name prefixes are omitted when storing a keystore.

Properties are context-sensitive: properties that apply to all the keystores in a domain are located in the domain clause, and properties that apply only to a specific keystore are located in that keystore's clause. Unless otherwise specified, a property in a keystore clause overrides a property of the same name in the domain clause. All property names are case-insensitive. The following properties are supported:

`keystoreType="<type>"`
: The keystore type.

`keystoreURI="<url>"`
: The keystore location.

`keystoreProviderName="<name>"`
: The name of the keystore's JCE provider.

`keystorePasswordEnv="<environment-variable>"`
: The environment variable that stores a keystore password. Alternatively, passwords may be supplied to the constructor method in a`Map<String, ProtectionParameter>`.

`entryNameSeparator="<separator>"`
: The separator between a keystore name prefix and an entry name. When specified, it applies to all the entries in a domain. Its default value is a space.

For example, configuration data for a simple keystore domain comprising three keystores is shown below: 

```kotlin
domain app1 {
      keystore app1-truststore
          keystoreURI="file:///app1/etc/truststore.jks";
 
      keystore system-truststore
          keystoreURI="${java.home}/lib/security/cacerts";
 
      keystore app1-keystore
          keystoreType="PKCS12"
          keystoreURI="file:///app1/etc/keystore.p12";
  };
 
  
```

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DomainLoadStoreParameter](DomainLoadStoreParameter.md))`(`configuration:` ` [URI](../java.net/URI.md)!`, `protectionParams:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [KeyStore.ProtectionParameter](../java/security/KeyStore.ProtectionParameter.md)!>!`)` Constructs a DomainLoadStoreParameter for a keystore domain with the parameters used to protect keystore data. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [URI](../java.net/URI.md)! | [getConfiguration](DomainLoadStoreParameter.md))`()` Gets the identifier for the domain configuration data. |
| [KeyStore.ProtectionParameter](../java/security/KeyStore.ProtectionParameter.md)! | [getProtectionParameter](DomainLoadStoreParameter.md))`()` Gets the keystore protection parameters for this domain. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [KeyStore.ProtectionParameter](../java/security/KeyStore.ProtectionParameter.md)!\>! | [getProtectionParams](DomainLoadStoreParameter.md))`()` Gets the keystore protection parameters for keystores in this domain. |
| --- | --- |

## Public constructors

### DomainLoadStoreParameter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DomainLoadStoreParameter(
    configuration: URI!, 
    protectionParams: MutableMap<String!, KeyStore.ProtectionParameter!>!)
```

Constructs a DomainLoadStoreParameter for a keystore domain with the parameters used to protect keystore data.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `configuration` | [URI](../java.net/URI.md)!:identifier for the domain configuration data. The name of the target domain should be specified in the`java.net.URI`fragment component when it is necessary to distinguish between several domain configurations at the same location. |
| `protectionParams` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [KeyStore.ProtectionParameter](../java/security/KeyStore.ProtectionParameter.md)!\>!:the map from keystore name to the parameter used to protect keystore data. A`java.util.Collections.EMPTY_MAP`should be used when protection parameters are not required or when they have been specified by properties in the domain configuration data. It is cloned to prevent subsequent modification. |

| Exceptions ||
|----------------------------------|-----------------------------------------------|
| `java.lang.NullPointerException` | if`configuration`or`protectionParams`is`null` |

## Public methods

### getConfiguration

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConfiguration(): URI!
```

Gets the identifier for the domain configuration data.

| Return ||
|---------------------------------------------------------------------------|-------------------------------------------|
| [URI](../java.net/URI.md)! | the identifier for the configuration data |

### getProtectionParameter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProtectionParameter(): KeyStore.ProtectionParameter!
```

Gets the keystore protection parameters for this domain. Keystore domains do not support a protection parameter.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|----------------------|
| [KeyStore.ProtectionParameter](../java/security/KeyStore.ProtectionParameter.md)! | always returns`null` |

### getProtectionParams

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProtectionParams(): MutableMap<String!, KeyStore.ProtectionParameter!>!
```

Gets the keystore protection parameters for keystores in this domain.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [KeyStore.ProtectionParameter](../java/security/KeyStore.ProtectionParameter.md)!>! | an unmodifiable map of keystore names to protection parameters |
