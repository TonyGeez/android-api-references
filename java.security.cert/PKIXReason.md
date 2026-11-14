# PKIXReason

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PKIXReason

```
class PKIXReason : CertPathValidatorException.Reason
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.security.cert.PKIXReason](../java/security/cert/PKIXReason.md)\> ||
| | ↳ | [java.security.cert.PKIXReason](../java/security/cert/PKIXReason.md) |

| Known Direct Subclasses [PKIXReason.INVALID_KEY_USAGE](../java/security/cert/PKIXReason.md), [PKIXReason.INVALID_NAME](../java/security/cert/PKIXReason.md), [PKIXReason.INVALID_POLICY](../java/security/cert/PKIXReason.md), [PKIXReason.NAME_CHAINING](../java/security/cert/PKIXReason.md), [PKIXReason.NOT_CA_CERT](../java/security/cert/PKIXReason.md), [PKIXReason.NO_TRUST_ANCHOR](../java/security/cert/PKIXReason.md), [PKIXReason.PATH_TOO_LONG](../java/security/cert/PKIXReason.md), [PKIXReason.UNRECOGNIZED_CRIT_EXT](../java/security/cert/PKIXReason.md) |---------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------| | [PKIXReason.INVALID_KEY_USAGE](../java/security/cert/PKIXReason.md) | The certificate's key usage is invalid. | | [PKIXReason.INVALID_NAME](../java/security/cert/PKIXReason.md) | The name constraints have been violated. | | [PKIXReason.INVALID_POLICY](../java/security/cert/PKIXReason.md) | The policy constraints have been violated. | | [PKIXReason.NAME_CHAINING](../java/security/cert/PKIXReason.md) | The certificate does not chain correctly. | | [PKIXReason.NOT_CA_CERT](../java/security/cert/PKIXReason.md) | The certificate is not a CA certificate. | | [PKIXReason.NO_TRUST_ANCHOR](../java/security/cert/PKIXReason.md) | No acceptable trust anchor found. | | [PKIXReason.PATH_TOO_LONG](../java/security/cert/PKIXReason.md) | The path length constraint has been violated. | | [PKIXReason.UNRECOGNIZED_CRIT_EXT](../java/security/cert/PKIXReason.md) | The certificate contains one or more unrecognized critical extensions. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The`PKIXReason`enumerates the potential PKIX-specific reasons that an X.509 certification path may be invalid according to the PKIX (RFC 5280) standard. These reasons are in addition to those of the`CertPathValidatorException.BasicReason`enumeration.

## Summary

| Enum values ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [INVALID_KEY_USAGE](../java/security/cert/PKIXReason.md) The certificate's key usage is invalid. |
| [INVALID_NAME](../java/security/cert/PKIXReason.md) The name constraints have been violated. |
| [INVALID_POLICY](../java/security/cert/PKIXReason.md) The policy constraints have been violated. |
| [NAME_CHAINING](../java/security/cert/PKIXReason.md) The certificate does not chain correctly. |
| [NOT_CA_CERT](../java/security/cert/PKIXReason.md) The certificate is not a CA certificate. |
| [NO_TRUST_ANCHOR](../java/security/cert/PKIXReason.md) No acceptable trust anchor found. |
| [PATH_TOO_LONG](../java/security/cert/PKIXReason.md) The path length constraint has been violated. |
| [UNRECOGNIZED_CRIT_EXT](../java/security/cert/PKIXReason.md) The certificate contains one or more unrecognized critical extensions. |

## Enum values

### INVALID_KEY_USAGE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val INVALID_KEY_USAGE : PKIXReason
```

The certificate's key usage is invalid. 

### INVALID_NAME

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val INVALID_NAME : PKIXReason
```

The name constraints have been violated. 

### INVALID_POLICY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val INVALID_POLICY : PKIXReason
```

The policy constraints have been violated. 

### NAME_CHAINING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val NAME_CHAINING : PKIXReason
```

The certificate does not chain correctly. 

### NOT_CA_CERT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val NOT_CA_CERT : PKIXReason
```

The certificate is not a CA certificate. 

### NO_TRUST_ANCHOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val NO_TRUST_ANCHOR : PKIXReason
```

No acceptable trust anchor found. 

### PATH_TOO_LONG

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val PATH_TOO_LONG : PKIXReason
```

The path length constraint has been violated. 

### UNRECOGNIZED_CRIT_EXT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val UNRECOGNIZED_CRIT_EXT : PKIXReason
```

The certificate contains one or more unrecognized critical extensions.
