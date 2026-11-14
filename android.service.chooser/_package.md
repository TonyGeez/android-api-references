# android.service.chooser

# android.service.chooser

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [AdditionalContentContract](AdditionalContentContract.md) | Specifies constants used by Chooser when interacting with the additional content provider, see [android.content.Intent#EXTRA_CHOOSER_ADDITIONAL_CONTENT_URI](../android.content/Intent.md). |
| --- | --- |
| [StateListener](../android/service/chooser/ChooserSession.StateListener.md) | A callback interface for Chooser session state updates. |

## Classes

| [ChooserAction](ChooserAction.md) | A ChooserAction is an app-defined action that can be provided to the Android Sharesheet to be shown to the user when [android.content.Intent#ACTION_CHOOSER](../android.content/Intent.md) is invoked. |
| --- | --- |
| [ChooserManager](ChooserManager.md) | Manages the creation, tracking, and retrieval of chooser sessions. |
| [ChooserResult](ChooserResult.md) | An event reported to a supplied \[IntentSender\] by the system chooser when an activity is selected or other actions are taken to complete the session. |
| [ChooserSession](ChooserSession.md) | A class that represents an interactive Chooser session. |
| --- | --- |
| [ChooserSessionToken](ChooserSessionToken.md) | An opaque token that serves as a Chooser session identifier. |
| [ChooserTarget](ChooserTarget.md) | A ChooserTarget represents a deep-link into an application as returned by a [android.service.chooser.ChooserTargetService](ChooserTargetService.md). |
| [ChooserTargetService](ChooserTargetService.md) | A service that receives calls from the system when the user is asked to choose a target for an intent explicitly by another app. |
| --- | --- |
