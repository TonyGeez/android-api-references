# NfcFCardEmulation

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NfcFCardEmulation

Kotlin | [Java](../android/nfc/cardemulation/NfcFCardEmulation.md) 
| --- | --- |

```
class NfcFCardEmulation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.cardemulation.NfcFCardEmulation](../android/nfc/cardemulation/NfcFCardEmulation.md) |

This class can be used to query the state of NFC-F card emulation services. For a general introduction into NFC card emulation, please read the [NFC card emulation developer guide](https://developer.android.com/guide/topics/connectivity/nfc/hce.html).

<br />

Use of this class requires the [PackageManager.FEATURE_NFC_HOST_CARD_EMULATION_NFCF](../android/content/pm/PackageManager.md) to be present on the device.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [disableService](../android/nfc/cardemulation/NfcFCardEmulation.md))`(`activity:` ` [Activity](../android/app/Activity.md)!`)` Disables the service for the specified Activity. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [enableService](../android/nfc/cardemulation/NfcFCardEmulation.md))`(`activity:` ` [Activity](../android/app/Activity.md)!`, `service:` ` [ComponentName](../android/content/ComponentName.md)!`)` Allows a foreground application to specify which card emulation service should be enabled while a specific Activity is in the foreground. |
| static [NfcFCardEmulation](../android/nfc/cardemulation/NfcFCardEmulation.md)! | [getInstance](../android/nfc/cardemulation/NfcFCardEmulation.md))`(`adapter:` ` [NfcAdapter](../android/nfc/NfcAdapter.md)!`)` Helper to get an instance of this class. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNfcid2ForService](../android/nfc/cardemulation/NfcFCardEmulation.md))`(`service:` ` [ComponentName](../android/content/ComponentName.md)!`)` Retrieves the current NFCID2 for the specified service. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemCodeForService](../android/nfc/cardemulation/NfcFCardEmulation.md))`(`service:` ` [ComponentName](../android/content/ComponentName.md)!`)` Retrieves the current System Code for the specified service. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerSystemCodeForService](../android/nfc/cardemulation/NfcFCardEmulation.md))`(`service:` ` [ComponentName](../android/content/ComponentName.md)!`, `systemCode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Registers a System Code for the specified service. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setNfcid2ForService](../android/nfc/cardemulation/NfcFCardEmulation.md))`(`service:` ` [ComponentName](../android/content/ComponentName.md)!`, `nfcid2:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set a NFCID2 for the specified service. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [unregisterSystemCodeForService](../android/nfc/cardemulation/NfcFCardEmulation.md))`(`service:` ` [ComponentName](../android/content/ComponentName.md)!`)` Removes a registered System Code for the specified service. |

## Public methods

### disableService

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun disableService(activity: Activity!): Boolean
```

Disables the service for the specified Activity.

Note that the specified Activity must still be in resumed state at the time of this call. A good place to call this method is in your [Activity.onPause](../android/app/Activity.md)) implementation.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md)!: The activity which the service was registered for |

| Return ||
|------------------------------------------------------------------------------------|----------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true when successful |

### enableService

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun enableService(
    activity: Activity!, 
    service: ComponentName!
): Boolean
```

Allows a foreground application to specify which card emulation service should be enabled while a specific Activity is in the foreground.

The specified HCE-F service is only enabled when the corresponding application is in the foreground and this method has been called. When the application is moved to the background, [disableService(android.app.Activity)](../android/nfc/cardemulation/NfcFCardEmulation.md)) is called, or NFCID2 or System Code is replaced, the HCE-F service is disabled.

The specified Activity must currently be in resumed state. A good paradigm is to call this method in your [Activity.onResume](../android/app/Activity.md)), and to call [disableService(android.app.Activity)](../android/nfc/cardemulation/NfcFCardEmulation.md)) in your [Activity.onPause](../android/app/Activity.md)).

Note that this preference is not persisted by the OS, and hence must be called every time the Activity is resumed.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md)!: The activity which prefers this service to be invoked |
| `service` | [ComponentName](../android/content/ComponentName.md)!: The service to be preferred while this activity is in the foreground |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the registration was successful |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(adapter: NfcAdapter!): NfcFCardEmulation!
```

Helper to get an instance of this class.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------|
| `adapter` | [NfcAdapter](../android/nfc/NfcAdapter.md)!: A reference to an NfcAdapter object. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------|---|
| [NfcFCardEmulation](../android/nfc/cardemulation/NfcFCardEmulation.md)! | |

### getNfcid2ForService

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNfcid2ForService(service: ComponentName!): String!
```

Retrieves the current NFCID2 for the specified service.

Before calling [setNfcid2ForService(android.content.ComponentName,java.lang.String)](../android/nfc/cardemulation/NfcFCardEmulation.md)), the NFCID2 contained in the Manifest file is returned. If "random" is specified in the Manifest file, a random number assigned by the system at installation time is returned. After setting an NFCID2 with [setNfcid2ForService(android.content.ComponentName,java.lang.String)](../android/nfc/cardemulation/NfcFCardEmulation.md)), this NFCID2 is returned.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `service` | [ComponentName](../android/content/ComponentName.md)!: The component name of the service |

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the current NFCID2 |

### getSystemCodeForService

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSystemCodeForService(service: ComponentName!): String!
```

Retrieves the current System Code for the specified service.

Before calling [registerSystemCodeForService(android.content.ComponentName,java.lang.String)](../android/nfc/cardemulation/NfcFCardEmulation.md)), the System Code contained in the Manifest file is returned. After calling [registerSystemCodeForService(android.content.ComponentName,java.lang.String)](../android/nfc/cardemulation/NfcFCardEmulation.md)), the System Code registered there is returned. After calling [unregisterSystemCodeForService(android.content.ComponentName)](../android/nfc/cardemulation/NfcFCardEmulation.md)), "null" is returned.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `service` | [ComponentName](../android/content/ComponentName.md)!: The component name of the service |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the current System Code |

### registerSystemCodeForService

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerSystemCodeForService(
    service: ComponentName!, 
    systemCode: String!
): Boolean
```

Registers a System Code for the specified service.

The System Code must be in range from "4000" to "4FFF" (excluding "4\*FF").

If a System Code was previously registered for this service (either statically through the manifest, or dynamically by using this API), it will be replaced with this one.

Even if the same System Code is already registered for another service, this method succeeds in registering the System Code.

Note that you can only register a System Code for a service that is running under the same UID as the caller of this API. Typically this means you need to call this from the same package as the service itself, though UIDs can also be shared between packages using shared UIDs.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `service` | [ComponentName](../android/content/ComponentName.md)!: The component name of the service |
| `systemCode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The System Code to be registered |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the registration was successful. |

### setNfcid2ForService

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setNfcid2ForService(
    service: ComponentName!, 
    nfcid2: String!
): Boolean
```

Set a NFCID2 for the specified service.

The NFCID2 must be in range from "02FE000000000000" to "02FEFFFFFFFFFFFF".

If a NFCID2 was previously set for this service (either statically through the manifest, or dynamically by using this API), it will be replaced.

Note that you can only set the NFCID2 for a service that is running under the same UID as the caller of this API. Typically this means you need to call this from the same package as the service itself, though UIDs can also be shared between packages using shared UIDs.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `service` | [ComponentName](../android/content/ComponentName.md)!: The component name of the service |
| `nfcid2` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The NFCID2 to be registered |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the setting was successful. |

### unregisterSystemCodeForService

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterSystemCodeForService(service: ComponentName!): Boolean
```

Removes a registered System Code for the specified service.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `service` | [ComponentName](../android/content/ComponentName.md)!: The component name of the service |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the System Code was successfully removed. |
