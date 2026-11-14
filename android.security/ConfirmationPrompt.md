# ConfirmationPrompt

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConfirmationPrompt

Kotlin| [Java](ConfirmationPrompt.md) 
| --- | --- |

```
open class ConfirmationPrompt
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.ConfirmationPrompt](ConfirmationPrompt.md) |

Class used for displaying confirmation prompts.

Confirmation prompts are prompts shown to the user to confirm a given text and are implemented in a way that a positive response indicates with high confidence that the user has seen the given text, even if the Android framework (including the kernel) was compromised. Implementing confirmation prompts with these guarantees requires dedicated hardware-support and may not always be available.

Confirmation prompts are typically used with an external entity - the*Relying Party*- in the following way. The setup steps are as follows:

- Before first use, the application generates a key-pair with the [CONFIRMATION tag](../android/security/keystore/KeyGenParameterSpec.Builder.md))set. AndroidKeyStore key attestation, e.g.,[android.security.keystore.KeyGenParameterSpec.Builder#setAttestationChallenge(byte[])](https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder#setAttestationChallenge(kotlin.ByteArray))is used to generate a certificate chain that includes the public key (`Kpub`in the following) of the newly generated key.
- The application sends`Kpub`and the certificate chain resulting from device attestation to the*Relying Party*.
- The*Relying Party* validates the certificate chain which involves checking the root certificate is what is expected (e.g. a certificate from Google), each certificate signs the next one in the chain, ending with`Kpub`, and that the attestation certificate asserts that`Kpub`has the [CONFIRMATION tag](../android/security/keystore/KeyGenParameterSpec.Builder.md))set. Additionally the relying party stores`Kpub`and associates it with the device it was received from.

The*Relying Party*is typically an external device (for example connected via Bluetooth) or application server.

Before executing a transaction which requires a high assurance of user content, the application does the following:

- The application gets a cryptographic nonce from the*Relying Party* and passes this as the`extraData`(via the Builder helper class) to the [presentPrompt()](ConfirmationPrompt.md))method. The*Relying Party*stores the nonce locally since it'll use it in a later step.
- If the user approves the prompt a*Confirmation Response* is returned in the[onConfirmed(byte[])](https://developer.android.com/reference/kotlin/android/security/ConfirmationCallback#onConfirmed(kotlin.ByteArray))callback as the`dataThatWasConfirmed`parameter. This blob contains the text that was shown to the user, the`extraData`parameter, and possibly other data.
- The application signs the*Confirmation Response* with the previously created key and sends the blob and the signature to the*Relying Party*.
- The*Relying Party* checks that the signature was made with`Kpub`and then extracts`promptText`matches what is expected and`extraData`matches the previously created nonce. If all checks passes, the transaction is executed.

Note: It is vital to check the`promptText`because this is the only part that the user has approved. To avoid writing parsers for all of the possible locales, it is recommended that the*Relying Party*uses the same string generator as used on the device and performs a simple string comparison.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/security/ConfirmationPrompt.Builder.md) A builder that collects arguments, to be shown on the system-provided confirmation prompt. |

| Public methods ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancelPrompt](ConfirmationPrompt.md))`()` Cancels a prompt currently being displayed. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](ConfirmationPrompt.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Checks if the device supports confirmation prompts. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [presentPrompt](ConfirmationPrompt.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [ConfirmationCallback](ConfirmationCallback.md)`)` Requests a confirmation prompt to be presented to the user. |
| --- | --- |

## Public methods

### cancelPrompt

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancelPrompt(): Unit
```

Cancels a prompt currently being displayed. On success, the [onCanceled()](ConfirmationCallback.md))method on the supplied callback object will be called asynchronously.

| Exceptions ||
|-----------------------------------|--------------------------------------------|
| `java.lang.IllegalStateException` | if no prompt is currently being presented. |

### isSupported

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isSupported(context: Context!): Boolean
```

Checks if the device supports confirmation prompts.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:the application context. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if confirmation prompts are supported by the device. |

### presentPrompt

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun presentPrompt(
    executor: Executor, 
    callback: ConfirmationCallback
): Unit
```

Requests a confirmation prompt to be presented to the user. When the prompt is no longer being presented, one of the methods in [ConfirmationCallback](ConfirmationCallback.md) is called on the supplied callback object. Confirmation prompts may not be available when accessibility services are running so this may fail with a [ConfirmationNotAvailableException](ConfirmationNotAvailableException.md) exception even if [isSupported](ConfirmationPrompt.md))returns`true`.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java.util.concurrent/Executor.md):the executor identifying the thread that will receive the callback. This value cannot be`null`. |
| `callback` | [ConfirmationCallback](ConfirmationCallback.md):the callback to use when the prompt is done showing. This value cannot be`null`. |

| Exceptions ||
|-----------------------------------------------------------|---------------------------------------------|
| `java.lang.IllegalArgumentException` | if the prompt text is too long or malfomed. |
| `android.security.ConfirmationAlreadyPresentingException` | if another prompt is being presented. |
| `android.security.ConfirmationNotAvailableException` | if confirmation prompts are not supported. |
| --- | --- |
