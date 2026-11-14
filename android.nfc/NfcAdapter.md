Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NfcAdapter

```
class NfcAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.nfc.NfcAdapter](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#) |

Represents the local NFC adapter.

Use the helper `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#getDefaultAdapter(android.content.Context)` to get the default NFC adapter for this Android device.

> [!NOTE]
>
> ### Developer Guides
>
> For more information about using NFC, read the [Near Field Communication](https://developer.android.com/guide/topics/nfc/index.html) developer guide.
>
> To perform basic file sharing between devices, read [Sharing Files with NFC](https://developer.android.com/training/beam-files/index.html).

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.CreateBeamUrisCallback` <br /> |
| abstract | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.CreateNdefMessageCallback` A callback to be invoked when another NFC device capable of NDEF push (Android Beam) is within range. |
| abstract | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.OnNdefPushCompleteCallback` A callback to be invoked when the system successfully delivers your `https://developer.android.com/reference/kotlin/android/nfc/NdefMessage` to another device. |
| abstract | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.OnTagRemovedListener` A callback that is invoked when a tag is removed from the field. |
| abstract | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.ReaderCallback` A callback to be invoked when the system finds a tag while the foreground activity is operating in reader mode. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_ADAPTER_STATE_CHANGED:kotlin.String` Broadcast Action: The state of the local NFC adapter has been changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_CHANGE_TAG_INTENT_PREFERENCE:kotlin.String` Activity action: Bring up the settings page that allows the user to enable or disable tag intent reception for apps. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_NDEF_DISCOVERED:kotlin.String` Intent to start an activity when a tag with NDEF payload is discovered. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_PREFERRED_PAYMENT_CHANGED:kotlin.String` Broadcast Action: Intent to notify if the preferred payment service changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TAG_DISCOVERED:kotlin.String` Intent to start an activity when a tag is discovered. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TECH_DISCOVERED:kotlin.String` Intent to start an activity when a tag is discovered and activities are registered for the specific technologies on the tag. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TRANSACTION_DETECTED:kotlin.String` Broadcast Action: Intent to notify an application that a transaction event has occurred on the Secure Element. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#EXTRA_ADAPTER_STATE:kotlin.String` Used as an int extra field in `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_ADAPTER_STATE_CHANGED:kotlin.String` intents to request the current power state. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#EXTRA_AID:kotlin.String` Mandatory byte\[\] extra field in `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TRANSACTION_DETECTED:kotlin.String` |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#EXTRA_DATA:kotlin.String` Optional byte\[\] extra field in `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TRANSACTION_DETECTED:kotlin.String` |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#EXTRA_ID:kotlin.String` Optional extra containing a byte array containing the ID of the discovered tag for the `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_NDEF_DISCOVERED:kotlin.String`, `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TECH_DISCOVERED:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TAG_DISCOVERED:kotlin.String` intents. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#EXTRA_NDEF_MESSAGES:kotlin.String` Extra containing an array of `https://developer.android.com/reference/kotlin/android/nfc/NdefMessage` present on the discovered tag. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#EXTRA_PREFERRED_PAYMENT_CHANGED_REASON:kotlin.String` Mandatory String extra field in `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_PREFERRED_PAYMENT_CHANGED:kotlin.String` Indicates the condition when trigger this event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#EXTRA_READER_PRESENCE_CHECK_DELAY:kotlin.String` Int Extra for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#EXTRA_READER_TECH_A_POLLING_LOOP_ANNOTATION:kotlin.String` Key to specify an NFC-A polling loop annotation (as a byte array) in the extras Bundle when calling `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#EXTRA_SECURE_ELEMENT_NAME:kotlin.String` Mandatory String extra field in `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TRANSACTION_DETECTED:kotlin.String` Indicates the Secure Element on which the transaction occurred. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#EXTRA_TAG:kotlin.String` Mandatory extra containing the `https://developer.android.com/reference/kotlin/android/nfc/Tag` that was discovered for the `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_NDEF_DISCOVERED:kotlin.String`, `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TECH_DISCOVERED:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TAG_DISCOVERED:kotlin.String` intents. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_LISTEN_DISABLE:kotlin.Int` Flags for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setDiscoveryTechnology(android.app.Activity,%20kotlin.Int,%20kotlin.Int)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_LISTEN_KEEP:kotlin.Int` Flags for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setDiscoveryTechnology(android.app.Activity,%20kotlin.Int,%20kotlin.Int)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_LISTEN_NFC_PASSIVE_A:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setDiscoveryTechnology(android.app.Activity,%20kotlin.Int,%20kotlin.Int)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_LISTEN_NFC_PASSIVE_B:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setDiscoveryTechnology(android.app.Activity,%20kotlin.Int,%20kotlin.Int)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_LISTEN_NFC_PASSIVE_F:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setDiscoveryTechnology(android.app.Activity,%20kotlin.Int,%20kotlin.Int)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_DISABLE:kotlin.Int` Flags for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setDiscoveryTechnology(android.app.Activity,%20kotlin.Int,%20kotlin.Int)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_KEEP:kotlin.Int` Flags for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setDiscoveryTechnology(android.app.Activity,%20kotlin.Int,%20kotlin.Int)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_NFC_A:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_NFC_B:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_NFC_BARCODE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_NFC_F:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_NFC_V:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_NO_PLATFORM_SOUNDS:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_SKIP_NDEF_CHECK:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#PREFERRED_PAYMENT_CHANGED:kotlin.Int` User selected another payment application as the preferred payment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#PREFERRED_PAYMENT_LOADED:kotlin.Int` Nfc is enabled and the preferred payment aids are registered. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#PREFERRED_PAYMENT_UPDATED:kotlin.Int` Current preferred payment has issued an update (registered/unregistered new aids or has been updated itself). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#STATE_OFF:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#STATE_ON:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#STATE_TURNING_OFF:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#STATE_TURNING_ON:kotlin.Int` <br /> |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#allowOneTransaction()()` Temporarily disables observe mode to allow a single Host Card Emulation (HCE) transaction to proceed. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#disable()()` Disable NFC hardware. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#disableForegroundDispatch(android.app.Activity)(activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#!)` Disable foreground dispatch to the given activity. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#disableReaderMode(android.app.Activity)(activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#!)` Restore the NFC adapter to normal mode of operation: supporting peer-to-peer (Android Beam), card emulation, and polling for all supported tag technologies. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enable()()` Enable NFC hardware. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableForegroundDispatch(android.app.Activity,%20android.app.PendingIntent,%20kotlin.Array,%20kotlin.Array)(activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#!, intent: https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#!, filters: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#!>!, techLists: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!>!)` Enable foreground dispatch to the given Activity. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)(activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#!, callback: https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.ReaderCallback!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Limit the NFC controller to reader mode while this Activity is in the foreground. |
| static [NfcAdapter](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#)! | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#getDefaultAdapter(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` Helper to get the default NFC Adapter. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#getGestureExchangeAid()()` Get the AID for Tap to Share functionality. |
| [NfcAntennaInfo](https://developer.android.com/reference/kotlin/android/nfc/NfcAntennaInfo)? | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#getNfcAntennaInfo()()` Returns information regarding Nfc antennas on the device such as their relative positioning on the device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ignore(android.nfc.Tag,%20kotlin.Int,%20android.nfc.NfcAdapter.OnTagRemovedListener,%20android.os.Handler)(tag: https://developer.android.com/reference/kotlin/android/nfc/Tag!, debounceMs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, tagRemovedListener: https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.OnTagRemovedListener!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Signals that you are no longer interested in communicating with an NFC tag for as long as it remains in range. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#isEnabled()()` Return true if this NFC Adapter has any features enabled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#isExitFramesSupported()()` Returns whether the device supports exit frames or not. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#isObserveModeEnabled()()` Returns whether Observe Mode is currently enabled or not. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#isObserveModeSupported()()` Returns whether the device supports observe mode or not. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#isPowerSavingModeEnabled()()` Returns whether power-saving mode is currently enabled or not. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#isPowerSavingModeSupported()()` Returns whether the device supports power-saving mode or not. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#isReaderModeAnnotationSupported()()` Returns whether the device supports setting annotation frames when enabling reader mode by passing an extras bundle that includes a `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#EXTRA_READER_TECH_A_POLLING_LOOP_ANNOTATION:kotlin.String` key to `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#isReaderOptionEnabled()()` Checks NFC Reader option feature is enabled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#isReaderOptionSupported()()` Checks if the device supports NFC Reader option functionality. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#isSecureNfcEnabled()()` Checks Secure NFC feature is enabled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#isSecureNfcSupported()()` Checks if the device supports Secure NFC functionality. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#isTagIntentAllowed()()` Checks whether the user has disabled the calling app from receiving NFC tag intents. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#isTagIntentAppPreferenceSupported()()` Checks if the device supports Tag Intent App Preference functionality. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#resetDiscoveryTechnology(android.app.Activity)(activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#?)` Restore the poll/listen technologies of NFC controller to its default state, which were changed by `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setDiscoveryTechnology(android.app.Activity,%20kotlin.Int,%20kotlin.Int)` |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setDiscoveryTechnology(android.app.Activity,%20kotlin.Int,%20kotlin.Int)(activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#?, pollTechnology: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, listenTechnology: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the NFC controller to enable specific poll/listen technologies, as specified in parameters, while this Activity is in the foreground. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setObserveModeEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Controls whether the NFC adapter will allow transactions to proceed or be in observe mode and simply observe and notify the APDU service of polling loop frames. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setPowerSavingMode(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether or not the NFC chip should be in power-saving mode next time it is disabled with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#disable()`. |

## Constants

### ACTION_ADAPTER_STATE_CHANGED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ADAPTER_STATE_CHANGED: String
```

Broadcast Action: The state of the local NFC adapter has been changed.

For example, NFC has been turned on or off.

Always contains the extra field `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#EXTRA_ADAPTER_STATE:kotlin.String`

 Value: "android.nfc.action.ADAPTER_STATE_CHANGED"

### ACTION_CHANGE_TAG_INTENT_PREFERENCE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CHANGE_TAG_INTENT_PREFERENCE: String
```

Activity action: Bring up the settings page that allows the user to enable or disable tag intent reception for apps.

This will direct user to the settings page shows a list that asks users whether they want to allow or disallow the package to start an activity when a tag is discovered.

 Value: "android.nfc.action.CHANGE_TAG_INTENT_PREFERENCE"

### ACTION_NDEF_DISCOVERED

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NDEF_DISCOVERED: String
```

Intent to start an activity when a tag with NDEF payload is discovered.

The system inspects the first `https://developer.android.com/reference/kotlin/android/nfc/NdefRecord` in the first `https://developer.android.com/reference/kotlin/android/nfc/NdefMessage` and looks for a URI, SmartPoster, or MIME record. If a URI or SmartPoster record is found the intent will contain the URI in its data field. If a MIME record is found the intent will contain the MIME type in its type field. This allows activities to register `https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#`s targeting specific content on tags. Activities should register the most specific intent filters possible to avoid the activity chooser dialog, which can disrupt the interaction with the tag as the user interacts with the screen.

If the tag has an NDEF payload this intent is started before `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TECH_DISCOVERED:kotlin.String`. If any activities respond to this intent neither `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TECH_DISCOVERED:kotlin.String` or `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TAG_DISCOVERED:kotlin.String` will be started.

The MIME type or data URI of this intent are normalized before dispatch - so that MIME, URI scheme and URI host are always lower-case.

 Value: "android.nfc.action.NDEF_DISCOVERED"

### ACTION_PREFERRED_PAYMENT_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PREFERRED_PAYMENT_CHANGED: String
```

Broadcast Action: Intent to notify if the preferred payment service changed.

This intent will only be sent to the application has requested permission for `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC_PREFERRED_PAYMENT_INFO:kotlin.String` and if the application has the necessary access to Secure Element which witnessed the particular event. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC_PREFERRED_PAYMENT_INFO:kotlin.String`

 Value: "android.nfc.action.PREFERRED_PAYMENT_CHANGED"

### ACTION_TAG_DISCOVERED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_TAG_DISCOVERED: String
```

**Deprecated:** *This intent action is deprecated. Please use `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_NDEF_DISCOVERED:kotlin.String` or `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TECH_DISCOVERED:kotlin.String` instead.*

*To achieve the same behavior as `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TAG_DISCOVERED:kotlin.String` (listening for all types of tags), use `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TECH_DISCOVERED:kotlin.String` and include all available NFC technologies in the meta-data.*

<br />

Intent to start an activity when a tag is discovered.

This intent will not be started when a tag is discovered if any activities respond to `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_NDEF_DISCOVERED:kotlin.String` or `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TECH_DISCOVERED:kotlin.String` for the current tag.

 Value: "android.nfc.action.TAG_DISCOVERED"

### ACTION_TECH_DISCOVERED

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_TECH_DISCOVERED: String
```

Intent to start an activity when a tag is discovered and activities are registered for the specific technologies on the tag.

To receive this intent an activity must include an intent filter for this action and specify the desired tech types in a manifest `meta-data` entry. Here is an example manfiest entry:

```kotlin
<activity android:name=".nfc.TechFilter" android:label="NFC/TechFilter">
      <!-- Add a technology filter -->
      <intent-filter>
          <action android:name="android.nfc.action.TECH_DISCOVERED" />
      </intent-filter>
 
      <meta-data android:name="android.nfc.action.TECH_DISCOVERED"
          android:resource="@xml/filter_nfc"
      />
  </activity>
```

The meta-data XML file should contain one or more `tech-list` entries each consisting or one or more `tech` entries. The `tech` entries refer to the qualified class name implementing the technology, for example "android.nfc.tech.NfcA".

A tag matches if any of the `tech-list` sets is a subset of `https://developer.android.com/reference/kotlin/android/nfc/Tag#getTechList()`. Each of the `tech-list`s is considered independently and the activity is considered a match is any single `tech-list` matches the tag that was discovered. This provides AND and OR semantics for filtering desired techs. Here is an example that will match any tag using `https://developer.android.com/reference/kotlin/android/nfc/tech/NfcF` or any tag using `https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA`, `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic`, and `https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef`:

```kotlin
<resources xmlns:xliff="urn:oasis:names:tc:xliff:document:1.2">
      <!-- capture anything using NfcF -->
      <tech-list>
          <tech>android.nfc.tech.NfcF</tech>
      </tech-list>
 
      <!-- OR -->
 
      <!-- capture all MIFARE Classics with NDEF payloads -->
      <tech-list>
          <tech>android.nfc.tech.NfcA</tech>
          <tech>android.nfc.tech.MifareClassic</tech>
          <tech>android.nfc.tech.Ndef</tech>
      </tech-list>
  </resources>
```

This intent is started after `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_NDEF_DISCOVERED:kotlin.String` and before `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TAG_DISCOVERED:kotlin.String`. If any activities respond to `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_NDEF_DISCOVERED:kotlin.String` this intent will not be started. If any activities respond to this intent `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TAG_DISCOVERED:kotlin.String` will not be started.

 Value: "android.nfc.action.TECH_DISCOVERED"

### ACTION_TRANSACTION_DETECTED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_TRANSACTION_DETECTED: String
```

Broadcast Action: Intent to notify an application that a transaction event has occurred on the Secure Element.

This intent will only be sent if the application has requested permission for `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC_TRANSACTION_EVENT:kotlin.String` and if the application has the necessary access to Secure Element which witnessed the particular event. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC_TRANSACTION_EVENT:kotlin.String`

 Value: "android.nfc.action.TRANSACTION_DETECTED"

### EXTRA_ADAPTER_STATE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ADAPTER_STATE: String
```

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_ADAPTER_STATE_CHANGED:kotlin.String` intents to request the current power state. Possible values are: `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#STATE_OFF:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#STATE_TURNING_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#STATE_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#STATE_TURNING_OFF:kotlin.Int`,

 Value: "android.nfc.extra.ADAPTER_STATE"

### EXTRA_AID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_AID: String
```

Mandatory byte\[\] extra field in `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TRANSACTION_DETECTED:kotlin.String`

 Value: "android.nfc.extra.AID"

### EXTRA_DATA

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DATA: String
```

Optional byte\[\] extra field in `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TRANSACTION_DETECTED:kotlin.String`

 Value: "android.nfc.extra.DATA"

### EXTRA_ID

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ID: String
```

Optional extra containing a byte array containing the ID of the discovered tag for the `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_NDEF_DISCOVERED:kotlin.String`, `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TECH_DISCOVERED:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TAG_DISCOVERED:kotlin.String` intents.

 Value: "android.nfc.extra.ID"

### EXTRA_NDEF_MESSAGES

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NDEF_MESSAGES: String
```

Extra containing an array of `https://developer.android.com/reference/kotlin/android/nfc/NdefMessage` present on the discovered tag.

This extra is mandatory for `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_NDEF_DISCOVERED:kotlin.String` intents, and optional for `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TECH_DISCOVERED:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TAG_DISCOVERED:kotlin.String` intents.

When this extra is present there will always be at least one `https://developer.android.com/reference/kotlin/android/nfc/NdefMessage` element. Most NDEF tags have only one NDEF message, but we use an array for future compatibility.

 Value: "android.nfc.extra.NDEF_MESSAGES"

### EXTRA_PREFERRED_PAYMENT_CHANGED_REASON

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PREFERRED_PAYMENT_CHANGED_REASON: String
```

Mandatory String extra field in `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_PREFERRED_PAYMENT_CHANGED:kotlin.String` Indicates the condition when trigger this event. Possible values are: `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#PREFERRED_PAYMENT_LOADED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#PREFERRED_PAYMENT_CHANGED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#PREFERRED_PAYMENT_UPDATED:kotlin.Int`,

 Value: "android.nfc.extra.PREFERRED_PAYMENT_CHANGED_REASON"

### EXTRA_READER_PRESENCE_CHECK_DELAY

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_READER_PRESENCE_CHECK_DELAY: String
```

Int Extra for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`.

Setting this integer extra allows the calling application to specify the delay that the platform will use for performing presence checks on any discovered tag.

 Value: "presence"

### EXTRA_READER_TECH_A_POLLING_LOOP_ANNOTATION

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_READER_TECH_A_POLLING_LOOP_ANNOTATION: String
```

Key to specify an NFC-A polling loop annotation (as a byte array) in the extras Bundle when calling `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`. This polling loop annotation will be included as a non-standard polling frame which will be reported to via `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/HostApduService#processPollingFrames(kotlin.collections.MutableList)`. If there is no explicit value set by the app, the device will emit the default annotation. Use `new byte[0]` as annotation in the extra to override the default and don't emit any annotation.

 Value: "android.nfc.extra.READER_TECH_A_POLLING_LOOP_ANNOTATION"

### EXTRA_SECURE_ELEMENT_NAME

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SECURE_ELEMENT_NAME: String
```

Mandatory String extra field in `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TRANSACTION_DETECTED:kotlin.String` Indicates the Secure Element on which the transaction occurred. eSE1...eSEn for Embedded Secure Elements, SIM1...SIMn for UICC/EUICC, etc.

 Value: "android.nfc.extra.SECURE_ELEMENT_NAME"

### EXTRA_TAG

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_TAG: String
```

Mandatory extra containing the `https://developer.android.com/reference/kotlin/android/nfc/Tag` that was discovered for the `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_NDEF_DISCOVERED:kotlin.String`, `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TECH_DISCOVERED:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TAG_DISCOVERED:kotlin.String` intents.

 Value: "android.nfc.extra.TAG"

### FLAG_LISTEN_DISABLE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_LISTEN_DISABLE: Int
```

Flags for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setDiscoveryTechnology(android.app.Activity,%20kotlin.Int,%20kotlin.Int)`.

Setting this flag disables listening.

 Value: 0

### FLAG_LISTEN_KEEP

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_LISTEN_KEEP: Int
```

Flags for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setDiscoveryTechnology(android.app.Activity,%20kotlin.Int,%20kotlin.Int)`.

Setting this flag makes listening to be set to the current stored default technology configuration.

 Value: -2147483648

### FLAG_LISTEN_NFC_PASSIVE_A

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_LISTEN_NFC_PASSIVE_A: Int
```

Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setDiscoveryTechnology(android.app.Activity,%20kotlin.Int,%20kotlin.Int)`.

Setting this flag enables listening for Nfc-A technology.

 Value: 1

### FLAG_LISTEN_NFC_PASSIVE_B

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_LISTEN_NFC_PASSIVE_B: Int
```

Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setDiscoveryTechnology(android.app.Activity,%20kotlin.Int,%20kotlin.Int)`.

Setting this flag enables listening for Nfc-B technology.

 Value: 2

### FLAG_LISTEN_NFC_PASSIVE_F

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_LISTEN_NFC_PASSIVE_F: Int
```

Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setDiscoveryTechnology(android.app.Activity,%20kotlin.Int,%20kotlin.Int)`.

Setting this flag enables listening for Nfc-F technology.

 Value: 4

### FLAG_READER_DISABLE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_READER_DISABLE: Int
```

Flags for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setDiscoveryTechnology(android.app.Activity,%20kotlin.Int,%20kotlin.Int)`.

Setting this flag disables polling.

 Value: 0

### FLAG_READER_KEEP

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_READER_KEEP: Int
```

Flags for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setDiscoveryTechnology(android.app.Activity,%20kotlin.Int,%20kotlin.Int)`.

Setting this flag makes polling to be set to the current stored default technology configuration.

 Value: -2147483648

### FLAG_READER_NFC_A

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_READER_NFC_A: Int
```

Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`.

Setting this flag enables polling for Nfc-A technology.

 Value: 1

### FLAG_READER_NFC_B

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_READER_NFC_B: Int
```

Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`.

Setting this flag enables polling for Nfc-B technology.

 Value: 2

### FLAG_READER_NFC_BARCODE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_READER_NFC_BARCODE: Int
```

Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`.

Setting this flag enables polling for NfcBarcode technology.

 Value: 16

### FLAG_READER_NFC_F

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_READER_NFC_F: Int
```

Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`.

Setting this flag enables polling for Nfc-F technology.

 Value: 4

### FLAG_READER_NFC_V

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_READER_NFC_V: Int
```

Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`.

Setting this flag enables polling for Nfc-V (ISO15693) technology.

 Value: 8

### FLAG_READER_NO_PLATFORM_SOUNDS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_READER_NO_PLATFORM_SOUNDS: Int
```

Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`.

Setting this flag allows the caller to prevent the platform from playing sounds when it discovers a tag.

 Value: 256

### FLAG_READER_SKIP_NDEF_CHECK

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_READER_SKIP_NDEF_CHECK: Int
```

Flag for use with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`.

Setting this flag allows the caller to prevent the platform from performing an NDEF check on the tags it finds.

 Value: 128

### PREFERRED_PAYMENT_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PREFERRED_PAYMENT_CHANGED: Int
```

User selected another payment application as the preferred payment.

 Value: 2

### PREFERRED_PAYMENT_LOADED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PREFERRED_PAYMENT_LOADED: Int
```

Nfc is enabled and the preferred payment aids are registered.

 Value: 1

### PREFERRED_PAYMENT_UPDATED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PREFERRED_PAYMENT_UPDATED: Int
```

Current preferred payment has issued an update (registered/unregistered new aids or has been updated itself).

 Value: 3

### STATE_OFF

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_OFF: Int
```

 Value: 1

### STATE_ON

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_ON: Int
```

 Value: 3

### STATE_TURNING_OFF

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_TURNING_OFF: Int
```

 Value: 4

### STATE_TURNING_ON

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_TURNING_ON: Int
```

 Value: 2

## Public methods

### allowOneTransaction

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun allowOneTransaction(): Unit
```

Temporarily disables observe mode to allow a single Host Card Emulation (HCE) transaction to proceed.

This is typically used in scenarios where an application, such as a digital wallet, needs to perform a tap-to-pay transaction while observe mode is active. After calling this method, observe mode will be disabled, allowing the HCE service to be selected by the reader. Observe mode will be automatically re-enabled after the transaction is complete or if the NFC field is lost.

### disable

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun disable(): Boolean
```

Disable NFC hardware.

No NFC features will work after this call, and the hardware will not perform or respond to any NFC communication.

This call is asynchronous. Listen for `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_ADAPTER_STATE_CHANGED:kotlin.String` broadcasts to find out when the operation is complete.

This API is only allowed to be called by system apps or apps which are Device Owner or Profile Owner.

If this returns true, then either NFC is already off, or a `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_ADAPTER_STATE_CHANGED:kotlin.String` broadcast will be sent to indicate a state transition. If this returns false, then there is some problem that prevents an attempt to turn NFC off. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_SECURE_SETTINGS:kotlin.String`

### disableForegroundDispatch

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun disableForegroundDispatch(activity: Activity!): Unit
```

Disable foreground dispatch to the given activity.

After calling `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableForegroundDispatch(android.app.Activity,%20android.app.PendingIntent,%20kotlin.Array,%20kotlin.Array)`, an activity must call this method before its `https://developer.android.com/reference/kotlin/android/app/Activity.html#onPause()` callback completes.

This method must be called from the main thread.

Requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String` permission.

| Parameters ||
|---|---|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!: the Activity to disable dispatch to |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the Activity has already been paused |
| `java.lang.UnsupportedOperationException` | if FEATURE_NFC is unavailable. |

### disableReaderMode

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun disableReaderMode(activity: Activity!): Unit
```

Restore the NFC adapter to normal mode of operation: supporting peer-to-peer (Android Beam), card emulation, and polling for all supported tag technologies.

| Parameters ||
|---|---|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!: the Activity that currently has reader mode enabled |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if FEATURE_NFC is unavailable. |

### enable

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun enable(): Boolean
```

Enable NFC hardware.

This call is asynchronous. Listen for `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_ADAPTER_STATE_CHANGED:kotlin.String` broadcasts to find out when the operation is complete.

This API is only allowed to be called by system apps or apps which are Device Owner or Profile Owner.

If this returns true, then either NFC is already on, or a `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_ADAPTER_STATE_CHANGED:kotlin.String` broadcast will be sent to indicate a state transition. If this returns false, then there is some problem that prevents an attempt to turn NFC on (for example we are in airplane mode and NFC is not toggleable in airplane mode on this platform). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_SECURE_SETTINGS:kotlin.String`

### enableForegroundDispatch

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun enableForegroundDispatch(
    activity: Activity!, 
    intent: PendingIntent!, 
    filters: Array<IntentFilter!>!, 
    techLists: Array<Array<String!>!>!
): Unit
```

Enable foreground dispatch to the given Activity.

This will give priority to the foreground activity when dispatching a discovered `https://developer.android.com/reference/kotlin/android/nfc/Tag` to an application.

If any IntentFilters are provided to this method they are used to match dispatch Intents for both the `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_NDEF_DISCOVERED:kotlin.String` and `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TAG_DISCOVERED:kotlin.String`. Since `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TECH_DISCOVERED:kotlin.String` relies on meta data outside of the IntentFilter matching for that dispatch Intent is handled by passing in the tech lists separately. Each first level entry in the tech list represents an array of technologies that must all be present to match. If any of the first level sets match then the dispatch is routed through the given PendingIntent. In other words, the second level is ANDed together and the first level entries are ORed together.

If you pass `null` for both the `filters` and `techLists` parameters that acts a wild card and will cause the foreground activity to receive all tags via the `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TAG_DISCOVERED:kotlin.String` intent.

This method must be called from the main thread, and only when the activity is in the foreground (resumed). Also, activities must call `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#disableForegroundDispatch(android.app.Activity)` before the completion of their `https://developer.android.com/reference/kotlin/android/app/Activity.html#onPause()` callback to disable foreground dispatch after it has been enabled.

Requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String` permission.

| Parameters ||
|---|---|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!: the Activity to dispatch to |
| `intent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)!: the PendingIntent to start for the dispatch |
| `filters` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [IntentFilter](https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#)!\>!: the IntentFilters to override dispatching for, or null to always dispatch |
| `techLists` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>!: the tech lists used to perform matching for dispatching of the `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TECH_DISCOVERED:kotlin.String` intent |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the Activity is not currently in the foreground |
| `java.lang.UnsupportedOperationException` | if FEATURE_NFC is unavailable. |

### enableReaderMode

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun enableReaderMode(
    activity: Activity!, 
    callback: NfcAdapter.ReaderCallback!, 
    flags: Int, 
    extras: Bundle!
): Unit
```

Limit the NFC controller to reader mode while this Activity is in the foreground.

In this mode the NFC controller will only act as an NFC tag reader/writer, thus disabling any peer-to-peer (Android Beam) and card-emulation modes of the NFC adapter on this device.

Use `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_SKIP_NDEF_CHECK:kotlin.Int` to prevent the platform from performing any NDEF checks in reader mode. Note that this will prevent the `https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef` tag technology from being enumerated on the tag, and that NDEF-based tag dispatch will not be functional.

For interacting with tags that are emulated on another Android device using Android's host-based card-emulation, the recommended flags are `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_NFC_A:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_SKIP_NDEF_CHECK:kotlin.Int`.

| Parameters ||
|---|---|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!: the Activity that requests the adapter to be in reader mode |
| `callback` | [NfcAdapter.ReaderCallback](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.ReaderCallback)!: the callback to be called when a tag is discovered |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags indicating poll technologies and other optional parameters |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: Additional extras for configuring reader mode. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if FEATURE_NFC is unavailable. |

### getDefaultAdapter

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDefaultAdapter(context: Context!): NfcAdapter!
```

Helper to get the default NFC Adapter.

Most Android devices will only have one NFC Adapter (NFC Controller).

This helper is the equivalent of:

```kotlin
NfcManager manager = (NfcManager) context.getSystemService(Context.NFC_SERVICE);
  NfcAdapter adapter = manager.getDefaultAdapter();
```

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: the calling application's context |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#!` | the default NFC adapter, or null if no NFC adapter exists |

### getGestureExchangeAid

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getGestureExchangeAid(): String?
```

Get the AID for Tap to Share functionality. 
Requires android.Manifest.permission#PERFORM_GESTURE_EXCHANGE

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### getNfcAntennaInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNfcAntennaInfo(): NfcAntennaInfo?
```

Returns information regarding Nfc antennas on the device such as their relative positioning on the device.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/nfc/NfcAntennaInfo?` | Information on the nfc antenna(s) on the device. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if FEATURE_NFC, FEATURE_NFC_HOST_CARD_EMULATION, FEATURE_NFC_HOST_CARD_EMULATION_NFCF, FEATURE_NFC_OFF_HOST_CARD_EMULATION_UICC and FEATURE_NFC_OFF_HOST_CARD_EMULATION_ESE are unavailable |

### ignore

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ignore(
    tag: Tag!, 
    debounceMs: Int, 
    tagRemovedListener: NfcAdapter.OnTagRemovedListener!, 
    handler: Handler!
): Boolean
```

Signals that you are no longer interested in communicating with an NFC tag for as long as it remains in range. All future attempted communication to this tag will fail with IOException. The NFC controller will be put in a low-power polling mode, allowing the device to save power in cases where it's "attached" to a tag all the time (e.g. a tag in car dock). Additionally the debounceMs parameter allows you to specify for how long the tag needs to have gone out of range, before it will be dispatched again. Note: the NFC controller typically polls at a pretty slow interval (100 - 500 ms). This means that if the tag repeatedly goes in and out of range (for example, in case of a flaky connection), and the controller happens to poll every time the tag is out of range, it \*will\* re-dispatch the tag after debounceMs, despite the tag having been "in range" during the interval. Note 2: if a tag with another UID is detected after this API is called, its effect will be cancelled; if this tag shows up before the amount of time specified in debounceMs, it will be dispatched again. Note 3: some tags have a random UID, in which case this API won't work reliably.

| Parameters ||
|---|---|
| `tag` | [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag)!: the `https://developer.android.com/reference/kotlin/android/nfc/Tag` to ignore. |
| `debounceMs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): minimum amount of time the tag needs to be out of range before being dispatched again. |
| `tagRemovedListener` | [NfcAdapter.OnTagRemovedListener](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.OnTagRemovedListener)!: listener to be called when the tag is removed from the field. Note that this will only be called if the tag has been out of range for at least debounceMs, or if another tag came into range before debounceMs. May be null in case you don't want a callback. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: the `https://developer.android.com/reference/kotlin/android/os/Handler.html#` that will be used for delivering the callback. if the handler is null, then the thread used for delivering the callback is unspecified. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | false if the tag couldn't be found (or has already gone out of range), true otherwise |

### isEnabled

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isEnabled(): Boolean
```

Return true if this NFC Adapter has any features enabled.

If this method returns false, the NFC hardware is guaranteed not to generate or respond to any NFC communication over its NFC radio.

Applications can use this to check if NFC is enabled. Applications can request Settings UI allowing the user to toggle NFC using:

<br />

```kotlin
startActivity(new Intent(Settings.ACTION_NFC_SETTINGS))
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this NFC Adapter has any features enabled |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/Settings.html#ACTION_NFC_SETTINGS:kotlin.String`

### isExitFramesSupported

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isExitFramesSupported(): Boolean
```

Returns whether the device supports exit frames or not. Exit frames allow device firmware to handle the transition out of observe mode for certain auto-transacting [polling loop filters](https://developer.android.com//develop/connectivity/nfc/hce#polling-loop-filters). Polling loop filters set by the default wallet role holder (`https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_WALLET:kotlin.String`) will be prioritized for use with exit frames.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the device supports exit frames, false otherwise. |

### isObserveModeEnabled

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isObserveModeEnabled(): Boolean
```

Returns whether Observe Mode is currently enabled or not.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if observe mode is enabled, false otherwise. |

### isObserveModeSupported

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isObserveModeSupported(): Boolean
```

Returns whether the device supports observe mode or not. When observe mode is enabled, the NFC hardware will listen to NFC readers, but not respond to them. While enabled, observed polling frames will be sent to the APDU service (see `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setObserveModeEnabled(kotlin.Boolean)`. When observe mode is disabled (or if it's not supported), the NFC hardware will automatically respond to the reader and proceed with the transaction.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the mode is supported, false otherwise. |

### isPowerSavingModeEnabled

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isPowerSavingModeEnabled(): Boolean
```

Returns whether power-saving mode is currently enabled or not.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if power saving mode is enabled, false otherwise |

### isPowerSavingModeSupported

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isPowerSavingModeSupported(): Boolean
```

Returns whether the device supports power-saving mode or not.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the device supports power-saving mode, false otherwise |

### isReaderModeAnnotationSupported

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isReaderModeAnnotationSupported(): Boolean
```

Returns whether the device supports setting annotation frames when enabling reader mode by passing an extras bundle that includes a `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#EXTRA_READER_TECH_A_POLLING_LOOP_ANNOTATION:kotlin.String` key to `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#enableReaderMode(android.app.Activity,%20android.nfc.NfcAdapter.ReaderCallback,%20kotlin.Int,%20android.os.Bundle)`. These annotations frames will be reported as unknown frames via `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/HostApduService#processPollingFrames(kotlin.collections.MutableList)` on another Android device that has set enabled observe mode by passing true to `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setObserveModeEnabled(kotlin.Boolean)` .

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the mode is supported, false otherwise. |

### isReaderOptionEnabled

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isReaderOptionEnabled(): Boolean
```

Checks NFC Reader option feature is enabled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if NFC Reader option is enabled, false otherwise |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if device doesn't support NFC Reader option functionality. `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#isReaderOptionSupported()` |

### isReaderOptionSupported

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isReaderOptionSupported(): Boolean
```

Checks if the device supports NFC Reader option functionality.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if device supports NFC Reader option, false otherwise |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if FEATURE_NFC is unavailable. |

### isSecureNfcEnabled

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSecureNfcEnabled(): Boolean
```

Checks Secure NFC feature is enabled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if Secure NFC is enabled, false otherwise |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if device doesn't support Secure NFC functionality. `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#isSecureNfcSupported()` |

### isSecureNfcSupported

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSecureNfcSupported(): Boolean
```

Checks if the device supports Secure NFC functionality.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if device supports Secure NFC, false otherwise |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if FEATURE_NFC, FEATURE_NFC_HOST_CARD_EMULATION, FEATURE_NFC_HOST_CARD_EMULATION_NFCF, FEATURE_NFC_OFF_HOST_CARD_EMULATION_UICC and FEATURE_NFC_OFF_HOST_CARD_EMULATION_ESE are unavailable |

### isTagIntentAllowed

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isTagIntentAllowed(): Boolean
```

Checks whether the user has disabled the calling app from receiving NFC tag intents.

This method checks whether the caller package name is either not present in the user disabled list or is explicitly allowed by the user.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if an app is either not present in the list or is added to the list with the flag set to `true`. Otherwise, it returns `false`. It also returns `true` if isTagIntentAppPreferenceSupported returns `false`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if FEATURE_NFC is unavailable. |

### isTagIntentAppPreferenceSupported

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isTagIntentAppPreferenceSupported(): Boolean
```

Checks if the device supports Tag Intent App Preference functionality. When supported, `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_NDEF_DISCOVERED:kotlin.String`, `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TECH_DISCOVERED:kotlin.String` or `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#ACTION_TAG_DISCOVERED:kotlin.String` will not be dispatched to an Activity if isTagIntentAllowed returns `false`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the device supports Tag application preference, `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if FEATURE_NFC is unavailable |

### resetDiscoveryTechnology

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun resetDiscoveryTechnology(activity: Activity?): Unit
```

Restore the poll/listen technologies of NFC controller to its default state, which were changed by `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#setDiscoveryTechnology(android.app.Activity,%20kotlin.Int,%20kotlin.Int)`

| Parameters ||
|---|---|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)?: The Activity that requested to change technologies. This value may be `null`. |

### setDiscoveryTechnology

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDiscoveryTechnology(
    activity: Activity?, 
    pollTechnology: Int, 
    listenTechnology: Int
): Unit
```

Set the NFC controller to enable specific poll/listen technologies, as specified in parameters, while this Activity is in the foreground. Use `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_KEEP:kotlin.Int` to keep current polling technology. Use `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_LISTEN_KEEP:kotlin.Int` to keep current listenig technology. (if the _KEEP flag is specified the other technology flags shouldn't be set and are quietly ignored otherwise). Use `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_DISABLE:kotlin.Int` to disable polling. Use `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_LISTEN_DISABLE:kotlin.Int` to disable listening. Also refer to `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#resetDiscoveryTechnology(android.app.Activity)` to restore these changes.

<br />

The pollTechnology, listenTechnology parameters can be one or several of below list.

```kotlin
Poll                    Listen
   Passive A         0x01   (NFC_A)           0x01  (NFC_PASSIVE_A)
   Passive B         0x02   (NFC_B)           0x02  (NFC_PASSIVE_B)
   Passive F         0x04   (NFC_F)           0x04  (NFC_PASSIVE_F)
   ISO 15693         0x08   (NFC_V)             -
   Kovio             0x10   (NFC_BARCODE)       -
  
```

Example usage in an Activity that requires to disable poll, keep current listen technologies:

```kotlin
protected void onResume() {
      mNfcAdapter = NfcAdapter.getDefaultAdapter(getApplicationContext());
      mNfcAdapter.setDiscoveryTechnology(this,
          NfcAdapter.FLAG_READER_DISABLE, NfcAdapter.FLAG_LISTEN_KEEP);
  }
```

<br />

| Parameters ||
|---|---|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)?: The Activity that requests NFC controller to enable specific technologies. This can be null for privileged apps. |
| `pollTechnology` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags indicating poll technologies. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_KEEP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_DISABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_NFC_A:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_NFC_B:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_NFC_F:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_NFC_V:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_READER_NFC_BARCODE:kotlin.Int` |
| `listenTechnology` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags indicating listen technologies. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_LISTEN_KEEP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_LISTEN_DISABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_LISTEN_NFC_PASSIVE_A:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_LISTEN_NFC_PASSIVE_B:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#FLAG_LISTEN_NFC_PASSIVE_F:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if FEATURE_NFC, FEATURE_NFC_HOST_CARD_EMULATION, FEATURE_NFC_HOST_CARD_EMULATION_NFCF are unavailable. NOTE: This API overrides all technology flags regardless of the current device state, it is incompatible with enableReaderMode() API and the others that either update or assume any techlology flag set by the OS. Please use with care. |

### setObserveModeEnabled

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setObserveModeEnabled(enabled: Boolean): Boolean
```

Controls whether the NFC adapter will allow transactions to proceed or be in observe mode and simply observe and notify the APDU service of polling loop frames. See `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#isObserveModeSupported()` for a description of observe mode. Only the package of the currently preferred service (the service set as preferred by the current foreground application via `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/CardEmulation#setPreferredService(android.app.Activity,%20android.content.ComponentName)` or the current Default Wallet Role Holder `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_WALLET:kotlin.String`), otherwise a call to this method will fail and return false.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): false disables observe mode to allow the transaction to proceed while true enables observe mode and does not allow transactions to proceed. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | boolean indicating success or failure. |

### setPowerSavingMode

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPowerSavingMode(enabled: Boolean): Unit
```

Sets whether or not the NFC chip should be in power-saving mode next time it is disabled with `https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter#disable()`. If the chip is already disabled, power-saving mode will take effect immediately.

This mode puts the NFC chip in a very low power mode, but not fully turned off. This mode limits communication between the NFC chip and the host processor to conserve power, although the exact implementation may depend on the device's underlying hardware. Other NFC APIs are disabled while this mode is active. 
Requires android.Manifest.permission#NFC_SET_CONTROLLER_ALWAYS_ON

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If a transient failure related to current device state prevented power-saving mode from being set. |
| `java.lang.UnsupportedOperationException` | If the device does not support power-saving mode. |
