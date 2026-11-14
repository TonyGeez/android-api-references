# CRLReason

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CRLReason

```
class CRLReason
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.security.cert.CRLReason](../java/security/cert/CRLReason.md)\> ||
| | ↳ | [java.security.cert.CRLReason](../java/security/cert/CRLReason.md) |

| Known Direct Subclasses [CRLReason.AA_COMPROMISE](../java/security/cert/CRLReason.md), [CRLReason.AFFILIATION_CHANGED](../java/security/cert/CRLReason.md), [CRLReason.CA_COMPROMISE](../java/security/cert/CRLReason.md), [CRLReason.CERTIFICATE_HOLD](../java/security/cert/CRLReason.md), [CRLReason.CESSATION_OF_OPERATION](../java/security/cert/CRLReason.md), [CRLReason.KEY_COMPROMISE](../java/security/cert/CRLReason.md), [CRLReason.PRIVILEGE_WITHDRAWN](../java/security/cert/CRLReason.md), [CRLReason.REMOVE_FROM_CRL](../java/security/cert/CRLReason.md), [CRLReason.SUPERSEDED](../java/security/cert/CRLReason.md), [CRLReason.UNSPECIFIED](../java/security/cert/CRLReason.md), [CRLReason.UNUSED](../java/security/cert/CRLReason.md) |---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------| | [CRLReason.AA_COMPROMISE](../java/security/cert/CRLReason.md) | This reason indicates that it is known or suspected that the certificate subject's private key has been compromised. | | [CRLReason.AFFILIATION_CHANGED](../java/security/cert/CRLReason.md) | This reason indicates that the subject's name or other information has changed. | | [CRLReason.CA_COMPROMISE](../java/security/cert/CRLReason.md) | This reason indicates that it is known or suspected that the certificate subject's private key has been compromised. | | [CRLReason.CERTIFICATE_HOLD](../java/security/cert/CRLReason.md) | This reason indicates that the certificate has been put on hold. | | [CRLReason.CESSATION_OF_OPERATION](../java/security/cert/CRLReason.md) | This reason indicates that the certificate is no longer needed. | | [CRLReason.KEY_COMPROMISE](../java/security/cert/CRLReason.md) | This reason indicates that it is known or suspected that the certificate subject's private key has been compromised. | | [CRLReason.PRIVILEGE_WITHDRAWN](../java/security/cert/CRLReason.md) | This reason indicates that the privileges granted to the subject of the certificate have been withdrawn. | | [CRLReason.REMOVE_FROM_CRL](../java/security/cert/CRLReason.md) | This reason indicates that the certificate was previously on hold and should be removed from the CRL. | | [CRLReason.SUPERSEDED](../java/security/cert/CRLReason.md) | This reason indicates that the certificate has been superseded. | | [CRLReason.UNSPECIFIED](../java/security/cert/CRLReason.md) | This reason indicates that it is unspecified as to why the certificate has been revoked. | | [CRLReason.UNUSED](../java/security/cert/CRLReason.md) | Unused reason. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The CRLReason enumeration specifies the reason that a certificate is revoked, as defined in [RFC 5280: Internet X.509 Public Key Infrastructure Certificate and CRL Profile](http://tools.ietf.org/html/rfc5280).

## Summary

| Enum values ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AA_COMPROMISE](../java/security/cert/CRLReason.md) This reason indicates that it is known or suspected that the certificate subject's private key has been compromised. |
| [AFFILIATION_CHANGED](../java/security/cert/CRLReason.md) This reason indicates that the subject's name or other information has changed. |
| [CA_COMPROMISE](../java/security/cert/CRLReason.md) This reason indicates that it is known or suspected that the certificate subject's private key has been compromised. |
| [CERTIFICATE_HOLD](../java/security/cert/CRLReason.md) This reason indicates that the certificate has been put on hold. |
| [CESSATION_OF_OPERATION](../java/security/cert/CRLReason.md) This reason indicates that the certificate is no longer needed. |
| [KEY_COMPROMISE](../java/security/cert/CRLReason.md) This reason indicates that it is known or suspected that the certificate subject's private key has been compromised. |
| [PRIVILEGE_WITHDRAWN](../java/security/cert/CRLReason.md) This reason indicates that the privileges granted to the subject of the certificate have been withdrawn. |
| [REMOVE_FROM_CRL](../java/security/cert/CRLReason.md) This reason indicates that the certificate was previously on hold and should be removed from the CRL. |
| [SUPERSEDED](../java/security/cert/CRLReason.md) This reason indicates that the certificate has been superseded. |
| [UNSPECIFIED](../java/security/cert/CRLReason.md) This reason indicates that it is unspecified as to why the certificate has been revoked. |
| [UNUSED](../java/security/cert/CRLReason.md) Unused reason. |

## Enum values

### AA_COMPROMISE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val AA_COMPROMISE : CRLReason
```

This reason indicates that it is known or suspected that the certificate subject's private key has been compromised. It applies to authority attribute (AA) certificates only. 

### AFFILIATION_CHANGED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val AFFILIATION_CHANGED : CRLReason
```

This reason indicates that the subject's name or other information has changed. 

### CA_COMPROMISE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CA_COMPROMISE : CRLReason
```

This reason indicates that it is known or suspected that the certificate subject's private key has been compromised. It applies to certificate authority (CA) certificates only. 

### CERTIFICATE_HOLD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CERTIFICATE_HOLD : CRLReason
```

This reason indicates that the certificate has been put on hold. 

### CESSATION_OF_OPERATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CESSATION_OF_OPERATION : CRLReason
```

This reason indicates that the certificate is no longer needed. 

### KEY_COMPROMISE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val KEY_COMPROMISE : CRLReason
```

This reason indicates that it is known or suspected that the certificate subject's private key has been compromised. It applies to end-entity certificates only. 

### PRIVILEGE_WITHDRAWN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val PRIVILEGE_WITHDRAWN : CRLReason
```

This reason indicates that the privileges granted to the subject of the certificate have been withdrawn. 

### REMOVE_FROM_CRL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val REMOVE_FROM_CRL : CRLReason
```

This reason indicates that the certificate was previously on hold and should be removed from the CRL. It is for use with delta CRLs. 

### SUPERSEDED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SUPERSEDED : CRLReason
```

This reason indicates that the certificate has been superseded. 

### UNSPECIFIED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val UNSPECIFIED : CRLReason
```

This reason indicates that it is unspecified as to why the certificate has been revoked. 

### UNUSED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val UNUSED : CRLReason
```

Unused reason.
