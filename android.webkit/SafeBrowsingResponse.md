# SafeBrowsingResponse

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SafeBrowsingResponse

Kotlin | [Java](https://developer.android.com/reference/android/webkit/SafeBrowsingResponse "View this page in Java") 
| --- | --- |

```
abstract class SafeBrowsingResponse
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.SafeBrowsingResponse](https://developer.android.com/reference/kotlin/android/webkit/SafeBrowsingResponse#) |

Used to indicate an action to take when hitting a malicious URL. Instances of this class are created by the WebView and passed to [android.webkit.WebViewClient#onSafeBrowsingHit](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onSafeBrowsingHit(android.webkit.WebView,%20android.webkit.WebResourceRequest,%20kotlin.Int,%20android.webkit.SafeBrowsingResponse)). The host application must call [showInterstitial(boolean)](https://developer.android.com/reference/kotlin/android/webkit/SafeBrowsingResponse#showInterstitial(kotlin.Boolean)), [proceed(boolean)](https://developer.android.com/reference/kotlin/android/webkit/SafeBrowsingResponse#proceed(kotlin.Boolean)), or [backToSafety(boolean)](https://developer.android.com/reference/kotlin/android/webkit/SafeBrowsingResponse#backToSafety(kotlin.Boolean)) to set the WebView's response to the Safe Browsing hit.

If reporting is enabled, all reports will be sent according to the privacy policy referenced by [android.webkit.WebView#getSafeBrowsingPrivacyPolicyUrl()](https://developer.android.com/reference/kotlin/android/webkit/WebView#getSafeBrowsingPrivacyPolicyUrl()).

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SafeBrowsingResponse](https://developer.android.com/reference/kotlin/android/webkit/SafeBrowsingResponse#SafeBrowsingResponse())`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [backToSafety](https://developer.android.com/reference/kotlin/android/webkit/SafeBrowsingResponse#backToSafety(kotlin.Boolean))`(`report:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Act as if the user clicked the "back to safety" button. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [proceed](https://developer.android.com/reference/kotlin/android/webkit/SafeBrowsingResponse#proceed(kotlin.Boolean))`(`report:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Act as if the user clicked the "visit this unsafe site" button. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [showInterstitial](https://developer.android.com/reference/kotlin/android/webkit/SafeBrowsingResponse#showInterstitial(kotlin.Boolean))`(`allowReporting:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Display the default interstitial. |
| --- | --- |

## Public constructors

### SafeBrowsingResponse

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SafeBrowsingResponse()
```

**Deprecated:** *This class should not be constructed by applications.*

## Public methods

### backToSafety

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun backToSafety(report: Boolean): Unit
```

Act as if the user clicked the "back to safety" button.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `report` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` to enable Safe Browsing reporting. |

### proceed

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun proceed(report: Boolean): Unit
```

Act as if the user clicked the "visit this unsafe site" button.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `report` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` to enable Safe Browsing reporting. |

### showInterstitial

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun showInterstitial(allowReporting: Boolean): Unit
```

Display the default interstitial.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `allowReporting` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the interstitial should show a reporting checkbox. |
