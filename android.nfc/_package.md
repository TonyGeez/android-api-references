# android.nfc

# android.nfc

Kotlin| [Java](../android/nfc/_package.md)
| --- | --- |

## Interfaces

| [CreateBeamUrisCallback](../android/nfc/NfcAdapter.CreateBeamUrisCallback.md) | <br /> |
| --- | --- |
| [CreateNdefMessageCallback](../android/nfc/NfcAdapter.CreateNdefMessageCallback.md) | A callback to be invoked when another NFC device capable of NDEF push (Android Beam) is within range. |
| [OnNdefPushCompleteCallback](../android/nfc/NfcAdapter.OnNdefPushCompleteCallback.md) | A callback to be invoked when the system successfully delivers your [NdefMessage](../android/nfc/NdefMessage.md) to another device. |
| [OnTagRemovedListener](../android/nfc/NfcAdapter.OnTagRemovedListener.md) | A callback that is invoked when a tag is removed from the field. |
| --- | --- |
| [ReaderCallback](../android/nfc/NfcAdapter.ReaderCallback.md) | A callback to be invoked when the system finds a tag while the foreground activity is operating in reader mode. |

## Classes

| [AvailableNfcAntenna](../android/nfc/AvailableNfcAntenna.md) | Represents a single available Nfc antenna on an Android device. |
| --- | --- |
| [NdefMessage](../android/nfc/NdefMessage.md) | Represents an immutable NDEF Message. |
| [NdefRecord](../android/nfc/NdefRecord.md) | Represents an immutable NDEF Record. |
| [NfcAdapter](../android/nfc/NfcAdapter.md) | Represents the local NFC adapter. |
| --- | --- |
| [NfcAntennaInfo](../android/nfc/NfcAntennaInfo.md) | Contains information on all available Nfc antennas on an Android device as well as information on the device itself in relation positioning of the antennas. |
| [NfcEvent](../android/nfc/NfcEvent.md) | Wraps information associated with any NFC event. |
| [NfcManager](../android/nfc/NfcManager.md) | High level manager used to obtain an instance of an [NfcAdapter](../android/nfc/NfcAdapter.md). |
| --- | --- |
| [Tag](../android/nfc/Tag.md) | Represents an NFC tag that has been discovered. |

## Exceptions

| [FormatException](../android/nfc/FormatException.md) | <br /> |
| --- | --- |
| [TagLostException](../android/nfc/TagLostException.md) | <br /> |
