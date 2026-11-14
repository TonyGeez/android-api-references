# WifiEnterpriseConfig

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiEnterpriseConfig

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/WifiEnterpriseConfig "View this page in Java") 
| --- | --- |

```
open class WifiEnterpriseConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.WifiEnterpriseConfig](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#) |

Enterprise configuration details for Wi-Fi. Stores details about the EAP method and any associated credentials.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Eap](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig.Eap) The Extensible Authentication Protocol method used |
| | [Phase2](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig.Phase2) The inner authentication method used |

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_WAPI_AS_CERTIFICATE_DATA](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#EXTRA_WAPI_AS_CERTIFICATE_DATA:kotlin.String) Intent extra: data for WAPI AS certificates |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_WAPI_AS_CERTIFICATE_NAME](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#EXTRA_WAPI_AS_CERTIFICATE_NAME:kotlin.String) Intent extra: name for WAPI AS certificates |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_WAPI_USER_CERTIFICATE_DATA](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#EXTRA_WAPI_USER_CERTIFICATE_DATA:kotlin.String) Intent extra: data for WAPI USER certificates |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_WAPI_USER_CERTIFICATE_NAME](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#EXTRA_WAPI_USER_CERTIFICATE_NAME:kotlin.String) Intent extra: name for WAPI USER certificates |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TLS_V1_0](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#TLS_V1_0:kotlin.Int) Constant definition for TLS v1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TLS_V1_1](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#TLS_V1_1:kotlin.Int) Constant definition for TLS v1. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TLS_V1_2](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#TLS_V1_2:kotlin.Int) Constant definition for TLS v1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TLS_V1_3](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#TLS_V1_3:kotlin.Int) Constant definition for TLS v1. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WAPI_AS_CERTIFICATE](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#WAPI_AS_CERTIFICATE:kotlin.String) Key prefix for WAPI AS certificates. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WAPI_USER_CERTIFICATE](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#WAPI_USER_CERTIFICATE:kotlin.String) Key prefix for WAPI user certificates. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WifiEnterpriseConfig](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#WifiEnterpriseConfig())`()` <br /> |
| [WifiEnterpriseConfig](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#WifiEnterpriseConfig(android.net.wifi.WifiEnterpriseConfig))`(`source:` ` [WifiEnterpriseConfig](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#)!`)` Copy constructor. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#describeContents())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [enableTrustOnFirstUse](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#enableTrustOnFirstUse(kotlin.Boolean))`(`enable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable Trust On First Use. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAltSubjectMatch](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#getAltSubjectMatch())`()` Get alternate subject match |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAnonymousIdentity](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#getAnonymousIdentity())`()` Get the anonymous identity |
| open [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)? | [getCaCertificate](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#getCaCertificate())`()` Get CA certificate. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!\>? | [getCaCertificates](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#getCaCertificates())`()` Get CA certificates. |
| --- | --- |
| open [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)! | [getClientCertificate](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#getClientCertificate())`()` Get client certificate |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!\>? | [getClientCertificateChain](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#getClientCertificateChain())`()` Get the complete client certificate chain in the same order as it was last supplied. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getClientKeyPairAlias](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#getClientKeyPairAlias())`()` Get KeyChain alias to use for client authentication. |
| --- | --- |
| open [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)? | [getClientPrivateKey](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#getClientPrivateKey())`()` Get the client private key as supplied in [setClientKeyEntryWithCertificateChain](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setClientKeyEntryWithCertificateChain(java.security.PrivateKey,%20kotlin.Array)), or null if unset. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getDecoratedIdentityPrefix](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#getDecoratedIdentityPrefix())`()` Get the decorated identity prefix. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDomainSuffixMatch](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#getDomainSuffixMatch())`()` Get the domain_suffix_match value. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEapMethod](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#getEapMethod())`()` Get the eap method. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getIdentity](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#getIdentity())`()` Get the identity |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumTlsVersion](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#getMinimumTlsVersion())`()` Get the minimum TLS version for TLS-based EAP methods. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPassword](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#getPassword())`()` Get the password. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPhase2Method](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#getPhase2Method())`()` Get the phase 2 authentication method. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPlmn](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#getPlmn())`()` Get plmn (Public Land Mobile Network) for Passpoint credential; see [(java.lang.String)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setPlmn(kotlin.String))for more information |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getRealm](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#getRealm())`()` Get realm for Passpoint credential; see [setRealm(java.lang.String)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setRealm(kotlin.String))for more information |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSubjectMatch](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#getSubjectMatch())`()` Get subject match (deprecated) |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasCaCertificate](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#hasCaCertificate())`()` Indicates whether or not this enterprise config has a CA certificate configured. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAuthenticationSimBased](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#isAuthenticationSimBased())`()` Utility method to determine whether the configuration's authentication method is SIM-based. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEapMethodServerCertUsed](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#isEapMethodServerCertUsed())`()` Determines whether an Enterprise configuration's EAP method requires a Root CA certification to validate the authentication server i. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isServerCertValidationEnabled](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#isServerCertValidationEnabled())`()` Determines whether an Enterprise configuration enables server certificate validation. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTrustOnFirstUseEnabled](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#isTrustOnFirstUseEnabled())`()` Indicates whether or not Trust On First Use (TOFU) is enabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAltSubjectMatch](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setAltSubjectMatch(kotlin.String))`(`altSubjectMatch:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set alternate subject match. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAnonymousIdentity](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setAnonymousIdentity(kotlin.String))`(`anonymousIdentity:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set anonymous identity. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCaCertificate](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setCaCertificate(java.security.cert.X509Certificate))`(`cert:` ` [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)?`)` Specify a X. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCaCertificates](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setCaCertificates(kotlin.Array))`(`certs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!>?`)` Specify a list of X. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClientKeyEntry](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setClientKeyEntry(java.security.PrivateKey,%20java.security.cert.X509Certificate))`(`privateKey:` ` [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)!`, `clientCertificate:` ` [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!`)` Specify a private key and client certificate for client authorization. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClientKeyEntryWithCertificateChain](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setClientKeyEntryWithCertificateChain(java.security.PrivateKey,%20kotlin.Array))`(`privateKey:` ` [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)!`, `clientCertificateChain:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!>!`)` Specify a private key and client certificate chain for client authorization. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClientKeyPairAlias](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setClientKeyPairAlias(kotlin.String))`(`alias:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Specify a key pair via KeyChain alias for client authentication. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDecoratedIdentityPrefix](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setDecoratedIdentityPrefix(kotlin.String))`(`decoratedIdentityPrefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Set a prefix for a decorated identity as per RFC 7542. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDomainSuffixMatch](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setDomainSuffixMatch(kotlin.String))`(`domain:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the domain_suffix_match directive on wpa_supplicant. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEapMethod](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setEapMethod(kotlin.Int))`(`eapMethod:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the EAP authentication method. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIdentity](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setIdentity(kotlin.String))`(`identity:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the identity |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumTlsVersion](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setMinimumTlsVersion(kotlin.Int))`(`tlsVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the minimum TLS version for TLS-based EAP methods. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPassword](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setPassword(kotlin.String))`(`password:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the password. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPhase2Method](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setPhase2Method(kotlin.Int))`(`phase2Method:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set Phase 2 authentication method. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlmn](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setPlmn(kotlin.String))`(`plmn:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set plmn (Public Land Mobile Network) of the provider of Passpoint credential |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRealm](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setRealm(kotlin.String))`(`realm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set realm for Passpoint credential; realm identifies a set of networks where your Passpoint credential can be used |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSubjectMatch](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setSubjectMatch(kotlin.String))`(`subjectMatch:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set subject match (deprecated). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [WifiEnterpriseConfig](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### EXTRA_WAPI_AS_CERTIFICATE_DATA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_WAPI_AS_CERTIFICATE_DATA: String
```

Intent extra: data for WAPI AS certificates 

 Value: "android.net.wifi.extra.WAPI_AS_CERTIFICATE_DATA"

### EXTRA_WAPI_AS_CERTIFICATE_NAME

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_WAPI_AS_CERTIFICATE_NAME: String
```

Intent extra: name for WAPI AS certificates 

 Value: "android.net.wifi.extra.WAPI_AS_CERTIFICATE_NAME"

### EXTRA_WAPI_USER_CERTIFICATE_DATA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_WAPI_USER_CERTIFICATE_DATA: String
```

Intent extra: data for WAPI USER certificates 

 Value: "android.net.wifi.extra.WAPI_USER_CERTIFICATE_DATA"

### EXTRA_WAPI_USER_CERTIFICATE_NAME

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_WAPI_USER_CERTIFICATE_NAME: String
```

Intent extra: name for WAPI USER certificates 

 Value: "android.net.wifi.extra.WAPI_USER_CERTIFICATE_NAME"

### TLS_V1_0

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TLS_V1_0: Int
```

Constant definition for TLS v1.0 which is used in [setMinimumTlsVersion(int)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setMinimumTlsVersion(kotlin.Int)) 

 Value: 0

### TLS_V1_1

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TLS_V1_1: Int
```

Constant definition for TLS v1.1 which is used in [setMinimumTlsVersion(int)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setMinimumTlsVersion(kotlin.Int)) 

 Value: 1

### TLS_V1_2

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TLS_V1_2: Int
```

Constant definition for TLS v1.2 which is used in [setMinimumTlsVersion(int)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setMinimumTlsVersion(kotlin.Int)) 

 Value: 2

### TLS_V1_3

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TLS_V1_3: Int
```

Constant definition for TLS v1.3 which is used in [setMinimumTlsVersion(int)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setMinimumTlsVersion(kotlin.Int)) 

 Value: 3

### WAPI_AS_CERTIFICATE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WAPI_AS_CERTIFICATE: String
```

Key prefix for WAPI AS certificates. 

 Value: "WAPIAS_"

### WAPI_USER_CERTIFICATE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WAPI_USER_CERTIFICATE: String
```

Key prefix for WAPI user certificates. 

 Value: "WAPIUSR_"

## Public constructors

### WifiEnterpriseConfig

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WifiEnterpriseConfig()
```  

### WifiEnterpriseConfig

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WifiEnterpriseConfig(source: WifiEnterpriseConfig!)
```

Copy constructor. This copies over all the fields verbatim (does not ignore masked password fields).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [WifiEnterpriseConfig](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#)!:Source WifiEnterpriseConfig object. |

## Public methods

### describeContents

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### enableTrustOnFirstUse

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun enableTrustOnFirstUse(enable: Boolean): Unit
```

Enable Trust On First Use. Trust On First Use (TOFU) simplifies manual or partial configurations of TLS-based EAP networks. TOFU operates by installing the Root CA cert which is received from the server during an initial connection to a new network. Such installation is gated by user approval. Use only when it is not possible to configure the Root CA cert for the server. 
Note: If a Root CA cert is already configured, this option is ignored, e.g. if [setCaCertificate(java.security.cert.X509Certificate)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setCaCertificate(java.security.cert.X509Certificate)), or[setCaCertificates(java.security.cert.X509Certificate[])](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setCaCertificates(kotlin.Array))is called.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true to enable; false otherwise (the default if the method is not called). |

### getAltSubjectMatch

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAltSubjectMatch(): String!
```

Get alternate subject match

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the alternate subject match string |

### getAnonymousIdentity

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAnonymousIdentity(): String!
```

Get the anonymous identity

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | anonymous identity |

### getCaCertificate

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCaCertificate(): X509Certificate?
```

Get CA certificate. If multiple CA certificates are configured previously, return the first one.

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)? | X.509 CA certificate This value may be`null`. |

### getCaCertificates

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCaCertificates(): Array<X509Certificate!>?
```

Get CA certificates.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!>? | This value may be`null`. |

### getClientCertificate

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getClientCertificate(): X509Certificate!
```

Get client certificate

| Return ||
|-------------------------------------------------------------------------------------------------------------|--------------------------|
| [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)! | X.509 client certificate |

### getClientCertificateChain

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getClientCertificateChain(): Array<X509Certificate!>?
```

Get the complete client certificate chain in the same order as it was last supplied.

If the chain was last supplied by a call to [setClientKeyEntry(java.security.PrivateKey,java.security.cert.X509Certificate)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setClientKeyEntry(java.security.PrivateKey,%20java.security.cert.X509Certificate))with a non-null \* certificate instance, a single-element array containing the certificate will be \* returned. If[setClientKeyEntryWithCertificateChain(java.security.PrivateKey,java.security.cert.X509Certificate[])](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setClientKeyEntryWithCertificateChain(java.security.PrivateKey,%20kotlin.Array))was last called with a non-empty array, this array will be returned in the same order as it was supplied. Otherwise,`null`will be returned.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!>? | X.509 client certificates |

### getClientKeyPairAlias

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getClientKeyPairAlias(): String?
```

Get KeyChain alias to use for client authentication.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getClientPrivateKey

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getClientPrivateKey(): PrivateKey?
```

Get the client private key as supplied in [setClientKeyEntryWithCertificateChain](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setClientKeyEntryWithCertificateChain(java.security.PrivateKey,%20kotlin.Array)), or null if unset. 

### getDecoratedIdentityPrefix

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDecoratedIdentityPrefix(): String?
```

Get the decorated identity prefix.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The decorated identity prefix This value may be`null`. |

### getDomainSuffixMatch

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDomainSuffixMatch(): String!
```

Get the domain_suffix_match value. See setDomSuffixMatch.

| Return ||
|-----------------------------------------------------------------------------------|-------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The domain value. |

### getEapMethod

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEapMethod(): Int
```

Get the eap method.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | eap method configured |

### getIdentity

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIdentity(): String!
```

Get the identity

| Return ||
|-----------------------------------------------------------------------------------|--------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the identity |

### getMinimumTlsVersion

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinimumTlsVersion(): Int
```

Get the minimum TLS version for TLS-based EAP methods.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the TLS version Value is [android.net.wifi.WifiEnterpriseConfig#TLS_V1_0](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#TLS_V1_0:kotlin.Int), [android.net.wifi.WifiEnterpriseConfig#TLS_V1_1](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#TLS_V1_1:kotlin.Int), [android.net.wifi.WifiEnterpriseConfig#TLS_V1_2](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#TLS_V1_2:kotlin.Int), or [android.net.wifi.WifiEnterpriseConfig#TLS_V1_3](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#TLS_V1_3:kotlin.Int) |

### getPassword

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPassword(): String!
```

Get the password. Returns locally set password value. For networks fetched from framework, returns "\*". 

### getPhase2Method

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPhase2Method(): Int
```

Get the phase 2 authentication method.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a phase 2 method defined at [Phase2](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig.Phase2) |

### getPlmn

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPlmn(): String!
```

Get plmn (Public Land Mobile Network) for Passpoint credential; see [(java.lang.String)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setPlmn(kotlin.String))for more information

| Return ||
|-----------------------------------------------------------------------------------|----------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the plmn |

### getRealm

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRealm(): String!
```

Get realm for Passpoint credential; see [setRealm(java.lang.String)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setRealm(kotlin.String))for more information

| Return ||
|-----------------------------------------------------------------------------------|-----------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the realm |

### getSubjectMatch

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSubjectMatch(): String!
```

**Deprecated:** *in favor of altSubjectMatch*

Get subject match (deprecated)

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the subject match string |

### hasCaCertificate

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasCaCertificate(): Boolean
```

Indicates whether or not this enterprise config has a CA certificate configured. 

### isAuthenticationSimBased

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAuthenticationSimBased(): Boolean
```

Utility method to determine whether the configuration's authentication method is SIM-based.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the credential information requires SIM card for current authentication method, otherwise it returns false. |

### isEapMethodServerCertUsed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEapMethodServerCertUsed(): Boolean
```

Determines whether an Enterprise configuration's EAP method requires a Root CA certification to validate the authentication server i.e. PEAP, TLS, UNAUTH_TLS, or TTLS.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if configuration requires a CA certification, false otherwise. |

### isServerCertValidationEnabled

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isServerCertValidationEnabled(): Boolean
```

Determines whether an Enterprise configuration enables server certificate validation.

The caller can determine, along with [isEapMethodServerCertUsed()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#isEapMethodServerCertUsed()), if an Enterprise configuration enables server certificate validation, which is a mandatory requirement for networks that use TLS based EAP methods. A configuration that does not enable server certificate validation will be ignored and will not be considered for network selection. A network suggestion with such a configuration will cause an IllegalArgumentException to be thrown when suggested. Server validation is achieved by the following: - Either certificate or CA path is configured. - Either alternative subject match or domain suffix match is set.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True for server certificate validation is enabled, false otherwise. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------|
| `java.lang.IllegalStateException` | on configuration which doesn't use server certificate. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#isEapMethodServerCertUsed()> 

### isTrustOnFirstUseEnabled

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isTrustOnFirstUseEnabled(): Boolean
```

Indicates whether or not Trust On First Use (TOFU) is enabled.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Trust On First Use is enabled or not. |

### setAltSubjectMatch

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAltSubjectMatch(altSubjectMatch: String!): Unit
```

Set alternate subject match. This is the substring to be matched against the alternate subject of the authentication server certificate. Note: If no alternate subject is set for an Enterprise configuration, either by not calling this API, or by calling it with null, or not setting domain suffix match using the [setDomainSuffixMatch(java.lang.String)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setDomainSuffixMatch(kotlin.String)), then the server certificate validation is incomplete - which means that the connection is not secure.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `altSubjectMatch` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:substring to be matched, for example DNS:server.example.com;EMAIL:server@example.com |

### setAnonymousIdentity

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAnonymousIdentity(anonymousIdentity: String!): Unit
```

Set anonymous identity. This is used as the unencrypted identity with certain EAP types

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------|
| `anonymousIdentity` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the anonymous identity |

### setCaCertificate

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCaCertificate(cert: X509Certificate?): Unit
```

Specify a X.509 certificate that identifies the server.

A default name is automatically assigned to the certificate and used with this configuration. The framework takes care of installing the certificate when the config is saved and removing the certificate when the config is removed. Note: If no certificate is set for an Enterprise configuration, either by not calling this API (or the[setCaCertificates(java.security.cert.X509Certificate[])](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setCaCertificates(kotlin.Array)), or by calling it with null, then the server certificate validation is skipped - which means that the connection is not secure.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cert` | [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)?:X.509 CA certificate This value may be`null`. |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | if not a CA certificate |

### setCaCertificates

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCaCertificates(certs: Array<X509Certificate!>?): Unit
```

Specify a list of X.509 certificates that identifies the server. The validation passes if the CA of server certificate matches one of the given certificates.

Default names are automatically assigned to the certificates and used with this configuration. The framework takes care of installing the certificates when the config is saved and removing the certificates when the config is removed. Note: If no certificates are set for an Enterprise configuration, either by not calling this API (or the [setCaCertificate(java.security.cert.X509Certificate)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setCaCertificate(java.security.cert.X509Certificate)), or by calling it with null, then the server certificate validation is skipped - which means that the connection is not secure.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `certs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!\>?:X.509 CA certificates This value may be`null`. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if any of the provided certificates is not a CA certificate, or if too many CA certificates are provided |

### setClientKeyEntry

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setClientKeyEntry(
    privateKey: PrivateKey!, 
    clientCertificate: X509Certificate!
): Unit
```

Specify a private key and client certificate for client authorization.

A default name is automatically assigned to the key entry and used with this configuration. The framework takes care of installing the key entry when the config is saved and removing the key entry when the config is removed.

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `privateKey` | [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)!:a PrivateKey instance for the end certificate. |
| `clientCertificate` | [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!:an X509Certificate representing the end certificate. |

| Exceptions ||
|--------------------------------------|------------------------------------|
| `java.lang.IllegalArgumentException` | for an invalid key or certificate. |

### setClientKeyEntryWithCertificateChain

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setClientKeyEntryWithCertificateChain(
    privateKey: PrivateKey!, 
    clientCertificateChain: Array<X509Certificate!>!
): Unit
```

Specify a private key and client certificate chain for client authorization.

A default name is automatically assigned to the key entry and used with this configuration. The framework takes care of installing the key entry when the config is saved and removing the key entry when the config is removed.

| Parameters ||
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `privateKey` | [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey.html#)!:a PrivateKey instance for the end certificate. |
| `clientCertificateChain` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!\>!:an array of X509Certificate instances which starts with end certificate and continues with additional CA certificates necessary to link the end certificate with some root certificate known by the authenticator. |

| Exceptions ||
|--------------------------------------|------------------------------------|
| `java.lang.IllegalArgumentException` | for an invalid key or certificate. |

### setClientKeyPairAlias

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setClientKeyPairAlias(alias: String): Unit
```

Specify a key pair via KeyChain alias for client authentication. The alias should refer to a key pair in KeyChain that is allowed for WiFi authentication.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):key pair alias This value cannot be`null`. |

**See Also**

- [android.app.admin.DevicePolicyManager#grantKeyPairToWifiAuth(String)](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#grantKeyPairToWifiAuth(kotlin.String)) 

### setDecoratedIdentityPrefix

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDecoratedIdentityPrefix(decoratedIdentityPrefix: String?): Unit
```

Set a prefix for a decorated identity as per RFC 7542. This prefix must contain a list of realms (could be a list of 1) delimited by a '!' character. e.g. homerealm.example.org! or proxyrealm.example.net!homerealm.example.org! A prefix of "homerealm.example.org!" will generate a decorated identity that looks like: homerealm.example.org!user@otherrealm.example.net Calling with a null parameter will clear the decorated prefix. Note: Caller must verify that the device supports this feature by calling [WifiManager.isDecoratedIdentitySupported()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isDecoratedIdentitySupported())

| Parameters ||
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `decoratedIdentityPrefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The prefix to add to the outer/anonymous identity This value may be`null`. |

### setDomainSuffixMatch

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDomainSuffixMatch(domain: String!): Unit
```

Set the domain_suffix_match directive on wpa_supplicant. This is the parameter to use for Hotspot 2.0 defined matching of AAA server certs per WFA HS2.0 spec, section 7.3.3.2, second paragraph.

From wpa_supplicant documentation:

Constraint for server domain name. If set, this FQDN is used as a suffix match requirement for the AAAserver certificate in SubjectAltName dNSName element(s). If a matching dNSName is found, this constraint is met.

Suffix match here means that the host/domain name is compared one label at a time starting from the top-level domain and all the labels in domain_suffix_match shall be included in the certificate. The certificate may include additional sub-level labels in addition to the required labels.

More than one match string can be provided by using semicolons to separate the strings (e.g., example.org;example.com). When multiple strings are specified, a match with any one of the values is considered a sufficient match for the certificate, i.e., the conditions are ORed ogether.

For example, domain_suffix_match=example.com would match test.example.com but would not match test-example.com. Note: If no domain suffix is set for an Enterprise configuration, either by not calling this API, or by calling it with null, or not setting alternate subject match using the [setAltSubjectMatch(java.lang.String)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#setAltSubjectMatch(kotlin.String)), then the server certificate validation is incomplete - which means that the connection is not secure.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------|
| `domain` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The domain value |

### setEapMethod

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEapMethod(eapMethod: Int): Unit
```

Set the EAP authentication method.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `eapMethod` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is one of [Eap](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig.Eap), except for [Eap.NONE](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig.Eap#NONE:kotlin.Int) |

| Exceptions ||
|--------------------------------------|--------------------------|
| `java.lang.IllegalArgumentException` | on an invalid eap method |

### setIdentity

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIdentity(identity: String!): Unit
```

Set the identity

| Parameters ||
|------------|------------------------------------------------------------------------------------|
| `identity` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: |

### setMinimumTlsVersion

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMinimumTlsVersion(tlsVersion: Int): Unit
```

Set the minimum TLS version for TLS-based EAP methods. [WifiManager.isTlsMinimumVersionSupported()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isTlsMinimumVersionSupported())indicates whether or not a minimum TLS version can be set. If not supported, the minimum TLS version is always TLS v1.0.

[WifiManager.isTlsV13Supported()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isTlsV13Supported())indicates whether or not TLS v1.3 is supported. If requested minimum is not supported, it will default to the maximum supported version.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tlsVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the TLS version Value is [android.net.wifi.WifiEnterpriseConfig#TLS_V1_0](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#TLS_V1_0:kotlin.Int), [android.net.wifi.WifiEnterpriseConfig#TLS_V1_1](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#TLS_V1_1:kotlin.Int), [android.net.wifi.WifiEnterpriseConfig#TLS_V1_2](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#TLS_V1_2:kotlin.Int), or [android.net.wifi.WifiEnterpriseConfig#TLS_V1_3](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig#TLS_V1_3:kotlin.Int) |

| Exceptions ||
|--------------------------------------|--------------------------------|
| `java.lang.IllegalArgumentException` | if the TLS version is invalid. |

### setPassword

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPassword(password: String!): Unit
```

Set the password.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------|
| `password` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the password |

### setPhase2Method

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPhase2Method(phase2Method: Int): Unit
```

Set Phase 2 authentication method. Sets the inner authentication method to be used in phase 2 after setting up a secure channel

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `phase2Method` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the inner authentication method and can be one of [Phase2](https://developer.android.com/reference/kotlin/android/net/wifi/WifiEnterpriseConfig.Phase2) |

| Exceptions ||
|--------------------------------------|-----------------------------|
| `java.lang.IllegalArgumentException` | on an invalid phase2 method |

### setPlmn

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPlmn(plmn: String!): Unit
```

Set plmn (Public Land Mobile Network) of the provider of Passpoint credential

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `plmn` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the plmn value derived from mcc (mobile country code) \& mnc (mobile network code) |

### setRealm

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRealm(realm: String!): Unit
```

Set realm for Passpoint credential; realm identifies a set of networks where your Passpoint credential can be used

| Parameters ||
|---------|---------------------------------------------------------------------------------------------|
| `realm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the realm |

### setSubjectMatch

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSubjectMatch(subjectMatch: String!): Unit
```

**Deprecated:** *in favor of altSubjectMatch*

Set subject match (deprecated). This is the substring to be matched against the subject of the authentication server certificate.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------|
| `subjectMatch` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:substring to be matched |

### toString

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WifiEnterpriseConfig!>
```
