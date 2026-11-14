# android.hardware.biometrics

## Interfaces

| [Authenticators](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators) | Types of authenticators, defined at a level of granularity supported by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager` and `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt`. |
| --- | --- |
| [EmbeddedContentFactory](https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt.EmbeddedContentFactory) | A factory that produces the custom embedded content view for the biometric prompt. |
| [PromptContentItem](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentItem) | An item shown on `https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentView`. |
| [PromptContentView](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentView) | Contains the information of the template of content view for Biometric Prompt. |
| --- | --- |

## Classes

| [BiometricManager](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager) | A class that contains biometric utilities. |
| --- | --- |
| [BiometricPrompt](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt) | A class that manages a system-provided biometric dialog. |
| [BiometricPromptStyleSpec](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPromptStyleSpec) | A class that describes the visual styles of the embedded BiometricPrompt UI to allow client applications to maintain visual consistency. |
| [EmbeddedBiometricPrompt](https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt) | The embedded version of `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt` that allows client apps to pass in content to display above the biometric prompt as a connected sheet. |
| --- | --- |
| [FallbackOption](https://developer.android.com/reference/kotlin/android/hardware/biometrics/FallbackOption) | Contains the information for a fallback option to be displayed within Biometric Prompt. |
| [PromptContentItemBulletedText](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentItemBulletedText) | A list item with bulleted text shown on `https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptVerticalListContentView`. |
| [PromptContentItemPlainText](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentItemPlainText) | A list item with plain text shown on `https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptVerticalListContentView`. |
| --- | --- |
| [PromptContentViewWithMoreOptionsButton](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentViewWithMoreOptionsButton) | Contains the information of the template of content view with a more options button for Biometric Prompt. |
| [PromptVerticalListContentView](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptVerticalListContentView) | Contains the information of the template of vertical list content view for Biometric Prompt. |
