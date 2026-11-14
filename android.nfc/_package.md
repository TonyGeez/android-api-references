# android.nfc

# android.nfc

Kotlin| [Java](https://developer.android.com/reference/android/nfc/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [CreateBeamUrisCallback](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.CreateBeamUrisCallback) | <br /> |
| --- | --- |
| [CreateNdefMessageCallback](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.CreateNdefMessageCallback) | A callback to be invoked when another NFC device capable of NDEF push (Android Beam) is within range. |
| [OnNdefPushCompleteCallback](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.OnNdefPushCompleteCallback) | A callback to be invoked when the system successfully delivers your [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage) to another device. |
| [OnTagRemovedListener](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.OnTagRemovedListener) | A callback that is invoked when a tag is removed from the field. |
| --- | --- |
| [ReaderCallback](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter.ReaderCallback) | A callback to be invoked when the system finds a tag while the foreground activity is operating in reader mode. |

## Classes

| [AvailableNfcAntenna](https://developer.android.com/reference/kotlin/android/nfc/AvailableNfcAntenna) | Represents a single available Nfc antenna on an Android device. |
| --- | --- |
| [NdefMessage](https://developer.android.com/reference/kotlin/android/nfc/NdefMessage) | Represents an immutable NDEF Message. |
| [NdefRecord](https://developer.android.com/reference/kotlin/android/nfc/NdefRecord) | Represents an immutable NDEF Record. |
| [NfcAdapter](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter) | Represents the local NFC adapter. |
| --- | --- |
| [NfcAntennaInfo](https://developer.android.com/reference/kotlin/android/nfc/NfcAntennaInfo) | Contains information on all available Nfc antennas on an Android device as well as information on the device itself in relation positioning of the antennas. |
| [NfcEvent](https://developer.android.com/reference/kotlin/android/nfc/NfcEvent) | Wraps information associated with any NFC event. |
| [NfcManager](https://developer.android.com/reference/kotlin/android/nfc/NfcManager) | High level manager used to obtain an instance of an [NfcAdapter](https://developer.android.com/reference/kotlin/android/nfc/NfcAdapter). |
| --- | --- |
| [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag) | Represents an NFC tag that has been discovered. |

## Exceptions

| [FormatException](https://developer.android.com/reference/kotlin/android/nfc/FormatException) | <br /> |
| --- | --- |
| [TagLostException](https://developer.android.com/reference/kotlin/android/nfc/TagLostException) | <br /> |
