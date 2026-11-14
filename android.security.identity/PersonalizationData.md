Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PersonalizationData

```
open class PersonalizationData
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.security.identity.PersonalizationData](https://developer.android.com/reference/kotlin/android/security/identity/PersonalizationData#) |

> [!CAUTION]
> **This class was deprecated in API level 37.2.**
>
> Use `java.security.KeyStore` with the Android hardware-backed keystore instead.

An object that holds personalization data. This data includes access control profiles and a set of data entries and values, grouped by namespace. This is used to provision data into a `https://developer.android.com/reference/kotlin/android/security/identity/WritableIdentityCredential`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/security/identity/PersonalizationData.Builder` A builder for `https://developer.android.com/reference/kotlin/android/security/identity/PersonalizationData#`. |
