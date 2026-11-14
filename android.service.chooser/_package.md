# android.service.chooser

# android.service.chooser

Kotlin| [Java](https://developer.android.com/reference/android/service/chooser/package-summary "View this page in Java")

## Interfaces

| [AdditionalContentContract](https://developer.android.com/reference/kotlin/android/service/chooser/AdditionalContentContract) | Specifies constants used by Chooser when interacting with the additional content provider, see [android.content.Intent#EXTRA_CHOOSER_ADDITIONAL_CONTENT_URI](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_ADDITIONAL_CONTENT_URI:kotlin.String). |
| [StateListener](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession.StateListener) | A callback interface for Chooser session state updates. |

## Classes

| [ChooserAction](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserAction) | A ChooserAction is an app-defined action that can be provided to the Android Sharesheet to be shown to the user when [android.content.Intent#ACTION_CHOOSER](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String) is invoked. |
| [ChooserManager](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserManager) | Manages the creation, tracking, and retrieval of chooser sessions. |
| [ChooserResult](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserResult) | An event reported to a supplied \[IntentSender\] by the system chooser when an activity is selected or other actions are taken to complete the session. |
| [ChooserSession](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession) | A class that represents an interactive Chooser session. |
| [ChooserSessionToken](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSessionToken) | An opaque token that serves as a Chooser session identifier. |
| [ChooserTarget](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserTarget) | A ChooserTarget represents a deep-link into an application as returned by a [android.service.chooser.ChooserTargetService](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserTargetService). |
| [ChooserTargetService](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserTargetService) | A service that receives calls from the system when the user is asked to choose a target for an intent explicitly by another app. |
