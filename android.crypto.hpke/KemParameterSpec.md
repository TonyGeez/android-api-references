# KemParameterSpec

Kotlin | [Java](https://developer.android.com/reference/android/crypto/hpke/KemParameterSpec "View this page in Java")
| --- | --- |

```
open class KemParameterSpec : NamedParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.spec.NamedParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#) ||
| | ↳ | [android.crypto.hpke.KemParameterSpec](https://developer.android.com/reference/kotlin/android/crypto/hpke/KemParameterSpec#) |

Specifies algorithm parameters for the KEM component of an HPKE suite which are determined by standard names as per RFC 9180.

These parameters can be composed into a full HKPE suite name using `https://developer.android.com/reference/kotlin/android/crypto/hpke/Hpke#getSuiteName(android.crypto.hpke.KemParameterSpec,%20android.crypto.hpke.KdfParameterSpec,%20android.crypto.hpke.AeadParameterSpec)`.

Note that currently only `DHKEM_X25519_HKDF_SHA256` is implemented.

## Summary

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#getName()()` Returns the standard name that determines the algorithm parameters. <br /> | ||

| Properties ||
|---|---|
| static [KemParameterSpec](https://developer.android.com/reference/kotlin/android/crypto/hpke/KemParameterSpec#)! | `https://developer.android.com/reference/kotlin/android/crypto/hpke/KemParameterSpec#DHKEM_P256_HKDF_SHA256:android.crypto.hpke.KemParameterSpec` <br /> |
| static [KemParameterSpec](https://developer.android.com/reference/kotlin/android/crypto/hpke/KemParameterSpec#)! | `https://developer.android.com/reference/kotlin/android/crypto/hpke/KemParameterSpec#DHKEM_P384_HKDF_SHA384:android.crypto.hpke.KemParameterSpec` <br /> |
| static [KemParameterSpec](https://developer.android.com/reference/kotlin/android/crypto/hpke/KemParameterSpec#)! | `https://developer.android.com/reference/kotlin/android/crypto/hpke/KemParameterSpec#DHKEM_P521_HKDF_SHA256:android.crypto.hpke.KemParameterSpec` <br /> |
| --- | --- |
| static [KemParameterSpec](https://developer.android.com/reference/kotlin/android/crypto/hpke/KemParameterSpec#)! | `https://developer.android.com/reference/kotlin/android/crypto/hpke/KemParameterSpec#DHKEM_X25519_HKDF_SHA256:android.crypto.hpke.KemParameterSpec` <br /> |
| static [KemParameterSpec](https://developer.android.com/reference/kotlin/android/crypto/hpke/KemParameterSpec#)! | `https://developer.android.com/reference/kotlin/android/crypto/hpke/KemParameterSpec#DHKEM_X448_HKDF_SHA512:android.crypto.hpke.KemParameterSpec` <br /> |

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#` |---|---| | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#!` | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#ED25519:java.security.spec.NamedParameterSpec` The Ed25519 parameters <br /> | | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#!` | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#ED448:java.security.spec.NamedParameterSpec` The Ed448 parameters <br /> | | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#!` | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#X25519:java.security.spec.NamedParameterSpec` The X25519 parameters <br /> | | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#!` | `https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec.html#X448:java.security.spec.NamedParameterSpec` The X448 parameters <br /> | ||

## Properties

### DHKEM_P256_HKDF_SHA256

```
static val DHKEM_P256_HKDF_SHA256: KemParameterSpec!
```

### DHKEM_P384_HKDF_SHA384

```
static val DHKEM_P384_HKDF_SHA384: KemParameterSpec!
```

### DHKEM_P521_HKDF_SHA256

```
static val DHKEM_P521_HKDF_SHA256: KemParameterSpec!
```

### DHKEM_X25519_HKDF_SHA256

```
static val DHKEM_X25519_HKDF_SHA256: KemParameterSpec!
```

### DHKEM_X448_HKDF_SHA512

```
static val DHKEM_X448_HKDF_SHA512: KemParameterSpec!
```
