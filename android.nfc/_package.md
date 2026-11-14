# android.nfc

# android.nfc

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [CreateBeamUrisCallback](../android/nfc/NfcAdapter.CreateBeamUrisCallback.md) | <br /> |
| --- | --- |
| [CreateNdefMessageCallback](../android/nfc/NfcAdapter.CreateNdefMessageCallback.md) | A callback to be invoked when another NFC device capable of NDEF push (Android Beam) is within range. |
| [OnNdefPushCompleteCallback](../android/nfc/NfcAdapter.OnNdefPushCompleteCallback.md) | A callback to be invoked when the system successfully delivers your [NdefMessage](NdefMessage.md) to another device. |
| [OnTagRemovedListener](../android/nfc/NfcAdapter.OnTagRemovedListener.md) | A callback that is invoked when a tag is removed from the field. |
| --- | --- |
| [ReaderCallback](../android/nfc/NfcAdapter.ReaderCallback.md) | A callback to be invoked when the system finds a tag while the foreground activity is operating in reader mode. |

## Classes

| [AvailableNfcAntenna](AvailableNfcAntenna.md) | Represents a single available Nfc antenna on an Android device. |
| --- | --- |
| [NdefMessage](NdefMessage.md) | Represents an immutable NDEF Message. |
| [NdefRecord](NdefRecord.md) | Represents an immutable NDEF Record. |
| [NfcAdapter](NfcAdapter.md) | Represents the local NFC adapter. |
| --- | --- |
| [NfcAntennaInfo](NfcAntennaInfo.md) | Contains information on all available Nfc antennas on an Android device as well as information on the device itself in relation positioning of the antennas. |
| [NfcEvent](NfcEvent.md) | Wraps information associated with any NFC event. |
| [NfcManager](NfcManager.md) | High level manager used to obtain an instance of an [NfcAdapter](NfcAdapter.md). |
| --- | --- |
| [Tag](Tag.md) | Represents an NFC tag that has been discovered. |

## Exceptions

| [FormatException](FormatException.md) | <br /> |
| --- | --- |
| [TagLostException](TagLostException.md) | <br /> |
