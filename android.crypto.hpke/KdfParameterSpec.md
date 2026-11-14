Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KdfParameterSpec

```
open class KdfParameterSpec : NamedParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.security.spec.NamedParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#) ||
| | ↳ | [android.crypto.hpke.KdfParameterSpec](https://developer.android.com/reference/kotlin/android/crypto/hpke/KdfParameterSpec#) |

Specifies algorithm parameters for the KDF component of an HPKE suite which are determined by standard names as per RFC 9180.

These parameters can be composed into a full HKPE suite name using `https://developer.android.com/reference/kotlin/android/crypto/hpke/Hpke#getSuiteName(android.crypto.hpke.KemParameterSpec,%20android.crypto.hpke.KdfParameterSpec,%20android.crypto.hpke.AeadParameterSpec)`.

Note that currently only `HKDF_SHA256` is implemented.

## Summary

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#getName()()` Returns the standard name that determines the algorithm parameters. <br /> | ||

| Properties ||
|---|---|
| static [KdfParameterSpec](https://developer.android.com/reference/kotlin/android/crypto/hpke/KdfParameterSpec#)! | `https://developer.android.com/reference/kotlin/android/crypto/hpke/KdfParameterSpec#HKDF_SHA256:android.crypto.hpke.KdfParameterSpec` <br /> |
| static [KdfParameterSpec](https://developer.android.com/reference/kotlin/android/crypto/hpke/KdfParameterSpec#)! | `https://developer.android.com/reference/kotlin/android/crypto/hpke/KdfParameterSpec#HKDF_SHA384:android.crypto.hpke.KdfParameterSpec` <br /> |
| static [KdfParameterSpec](https://developer.android.com/reference/kotlin/android/crypto/hpke/KdfParameterSpec#)! | `https://developer.android.com/reference/kotlin/android/crypto/hpke/KdfParameterSpec#HKDF_SHA512:android.crypto.hpke.KdfParameterSpec` <br /> |

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#` |---|---| | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#!` | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#ED25519:java.security.spec.NamedParameterSpec` The Ed25519 parameters <br /> | | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#!` | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#ED448:java.security.spec.NamedParameterSpec` The Ed448 parameters <br /> | | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#!` | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#ML_DSA_65:java.security.spec.NamedParameterSpec` The ML-DSA-65 parameters <br /> | | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#!` | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#ML_DSA_87:java.security.spec.NamedParameterSpec` The ML-DSA-87 parameters <br /> | | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#!` | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#X25519:java.security.spec.NamedParameterSpec` The X25519 parameters <br /> | | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#!` | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#X448:java.security.spec.NamedParameterSpec` The X448 parameters <br /> | ||

## Properties

### HKDF_SHA256

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HKDF_SHA256: KdfParameterSpec!
```

### HKDF_SHA384

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HKDF_SHA384: KdfParameterSpec!
```

### HKDF_SHA512

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HKDF_SHA512: KdfParameterSpec!
```
