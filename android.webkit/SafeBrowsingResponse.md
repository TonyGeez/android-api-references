# SafeBrowsingResponse

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SafeBrowsingResponse

Kotlin | [Java](SafeBrowsingResponse.md) 
| --- | --- |

```
abstract class SafeBrowsingResponse
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.SafeBrowsingResponse](SafeBrowsingResponse.md) |

Used to indicate an action to take when hitting a malicious URL. Instances of this class are created by the WebView and passed to [android.webkit.WebViewClient#onSafeBrowsingHit](WebViewClient.md)). The host application must call [showInterstitial(boolean)](SafeBrowsingResponse.md)), [proceed(boolean)](SafeBrowsingResponse.md)), or [backToSafety(boolean)](SafeBrowsingResponse.md)) to set the WebView's response to the Safe Browsing hit.

If reporting is enabled, all reports will be sent according to the privacy policy referenced by [android.webkit.WebView#getSafeBrowsingPrivacyPolicyUrl()](WebView.md)).

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SafeBrowsingResponse](SafeBrowsingResponse.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [backToSafety](SafeBrowsingResponse.md))`(`report:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Act as if the user clicked the "back to safety" button. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [proceed](SafeBrowsingResponse.md))`(`report:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Act as if the user clicked the "visit this unsafe site" button. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [showInterstitial](SafeBrowsingResponse.md))`(`allowReporting:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Display the default interstitial. |
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
