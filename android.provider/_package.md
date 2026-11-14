# android.provider

## Interfaces

| [BaseColumns](../android/provider/BaseColumns.md) | <br /> |
| --- | --- |
| [AttendeesColumns](../android/provider/CalendarContract.AttendeesColumns.md) | Columns from the Attendees table that other tables join into themselves. |
| [CalendarAlertsColumns](../android/provider/CalendarContract.CalendarAlertsColumns.md) | <br /> |
| [CalendarCacheColumns](../android/provider/CalendarContract.CalendarCacheColumns.md) | <br /> |
| --- | --- |
| [CalendarColumns](../android/provider/CalendarContract.CalendarColumns.md) | Columns specific to the Calendars Uri that other Uris can query. |
| [CalendarSyncColumns](../android/provider/CalendarContract.CalendarSyncColumns.md) | Generic columns for use by sync adapters. |
| [ColorsColumns](../android/provider/CalendarContract.ColorsColumns.md) | <br /> |
| --- | --- |
| [EventDaysColumns](../android/provider/CalendarContract.EventDaysColumns.md) | <br /> |
| [EventsColumns](../android/provider/CalendarContract.EventsColumns.md) | Columns from the Events table that other tables join into themselves. |
| [ExtendedPropertiesColumns](../android/provider/CalendarContract.ExtendedPropertiesColumns.md) | <br /> |
| --- | --- |
| [RemindersColumns](../android/provider/CalendarContract.RemindersColumns.md) | <br /> |
| [SyncColumns](../android/provider/CalendarContract.SyncColumns.md) | Columns for Sync information used by Calendars and Events tables. |
| [ContactMethodsColumns](../android/provider/Contacts.ContactMethodsColumns.md) | Columns from the ContactMethods table that other tables join into themseleves. |
| --- | --- |
| [ExtensionsColumns](../android/provider/Contacts.ExtensionsColumns.md) | <br /> |
| [GroupsColumns](../android/provider/Contacts.GroupsColumns.md) | Columns from the groups table. |
| [OrganizationColumns](../android/provider/Contacts.OrganizationColumns.md) | Columns from the Organizations table that other columns join into themselves. |
| --- | --- |
| [PeopleColumns](../android/provider/Contacts.PeopleColumns.md) | Columns from the People table that other tables join into themselves. |
| [PhonesColumns](../android/provider/Contacts.PhonesColumns.md) | Columns from the Phones table that other columns join into themselves. |
| [PhotosColumns](../android/provider/Contacts.PhotosColumns.md) | Columns from the Photos table that other columns join into themselves. |
| --- | --- |
| [PresenceColumns](../android/provider/Contacts.PresenceColumns.md) | The IM presence columns with some contacts specific columns mixed in. |
| [SettingsColumns](../android/provider/Contacts.SettingsColumns.md) | Columns from the Settings table that other columns join into themselves. |
| [BaseSyncColumns](../android/provider/ContactsContract.BaseSyncColumns.md) | Generic columns for use by sync adapters. |
| --- | --- |
| [ContactNameColumns](../android/provider/ContactsContract.ContactNameColumns.md) | Contact name and contact name metadata columns in the RawContacts table. |
| [ContactOptionsColumns](../android/provider/ContactsContract.ContactOptionsColumns.md) | Columns of `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts` that track the user's preferences for, or interactions with, the contact. |
| [ContactsColumns](../android/provider/ContactsContract.ContactsColumns.md) | Columns of `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts` that refer to intrinsic properties of the contact, as opposed to the user-specified options found in `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactOptionsColumns`. |
| --- | --- |
| [ContactStatusColumns](../android/provider/ContactsContract.ContactStatusColumns.md) | <br /> |
| [DataColumns](../android/provider/ContactsContract.DataColumns.md) | Columns in the Data table. |
| [DataColumnsWithJoins](../android/provider/ContactsContract.DataColumnsWithJoins.md) | Combines all columns returned by `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data` table queries. |
| --- | --- |
| [DataUsageStatColumns](../android/provider/ContactsContract.DataUsageStatColumns.md) | Columns in the Data_Usage_Stat table |
| [DeletedContactsColumns](../android/provider/ContactsContract.DeletedContactsColumns.md) | <br /> |
| [DisplayNameSources](../android/provider/ContactsContract.DisplayNameSources.md) | Types of data used to produce the display name for a contact. |
| --- | --- |
| [FullNameStyle](../android/provider/ContactsContract.FullNameStyle.md) | Constants for various styles of combining given name, family name etc into a full name. |
| [GroupsColumns](../android/provider/ContactsContract.GroupsColumns.md) | <br /> |
| [PhoneLookupColumns](../android/provider/ContactsContract.PhoneLookupColumns.md) | <br /> |
| --- | --- |
| [PhoneticNameStyle](../android/provider/ContactsContract.PhoneticNameStyle.md) | Constants for various styles of capturing the pronunciation of a person's name. |
| [PresenceColumns](../android/provider/ContactsContract.PresenceColumns.md) | Additional data mixed in with `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns` to link back to specific `https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String` entries. |
| [RawContactsColumns](../android/provider/ContactsContract.RawContactsColumns.md) | <br /> |
| --- | --- |
| [SettingsColumns](../android/provider/ContactsContract.SettingsColumns.md) | <br /> |
| [StatusColumns](../android/provider/ContactsContract.StatusColumns.md) | Social status update columns. |
| [SyncColumns](../android/provider/ContactsContract.SyncColumns.md) | Columns that appear when each row of a table belongs to a specific account, including sync information that an account may need. |
| --- | --- |
| [DownloadColumns](../android/provider/MediaStore.DownloadColumns.md) | Download metadata columns. |
| [MediaColumns](../android/provider/MediaStore.MediaColumns.md) | Common media metadata columns. |
| [OpenableColumns](../android/provider/OpenableColumns.md) | These are standard columns for openable URIs. |
| --- | --- |
| [Columns](../android/provider/SyncStateContract.Columns.md) | <br /> |
| [BaseMmsColumns](../android/provider/Telephony.BaseMmsColumns.md) | Base columns for tables that contain MMSs. |
| [CanonicalAddressesColumns](../android/provider/Telephony.CanonicalAddressesColumns.md) | Columns for the "canonical_addresses" table used by MMS and SMS. |
| --- | --- |
| [TextBasedSmsColumns](../android/provider/Telephony.TextBasedSmsColumns.md) | Base columns for tables that contain text-based SMSs. |
| [ThreadsColumns](../android/provider/Telephony.ThreadsColumns.md) | Columns for the "threads" table used by MMS and SMS. |

## Classes

| [AlarmClock](../android/provider/AlarmClock.md) | The AlarmClock provider contains an Intent action and extras that can be used to start an Activity to set a new alarm or timer in an alarm clock application. |
| --- | --- |
| [BlockedNumberContract](../android/provider/BlockedNumberContract.md) | The contract between the blockednumber provider and applications. |
| [Browser](../android/provider/Browser.md) | <br /> |
| [CalendarContract](../android/provider/CalendarContract.md) | The contract between the calendar provider and applications. |
| --- | --- |
| [CallLog](../android/provider/CallLog.md) | The CallLog provider contains information about placed and received calls. |
| [CloudMediaProvider](../android/provider/CloudMediaProvider.md) | Base class for a cloud media provider. |
| [CloudMediaProviderContract](../android/provider/CloudMediaProviderContract.md) | Defines the contract between a cloud media provider and the OS. |
| --- | --- |
| [Contacts](../android/provider/Contacts.md) | The Contacts provider stores all information about contacts. |
| [ContactsContract](../android/provider/ContactsContract.md) | The contract between the contacts provider and applications. |
| [ContactsPickerSessionContract](../android/provider/ContactsPickerSessionContract.md) | The contract between the Contacts Picker session provider and client applications. |
| --- | --- |
| [DocumentsContract](../android/provider/DocumentsContract.md) | Defines the contract between a documents provider and the platform. |
| [DocumentsProvider](../android/provider/DocumentsProvider.md) | Base class for a document provider. |
| [E2eeContactKeysManager](../android/provider/E2eeContactKeysManager.md) | E2eeContactKeysManager provides access to the provider of end-to-end encryption contact keys. |
| --- | --- |
| [FontRequest](../android/provider/FontRequest.md) | Information about a font request that may be sent to a Font Provider. |
| [FontsContract](../android/provider/FontsContract.md) | Utility class to deal with Font ContentProviders. |
| [LiveFolders](../android/provider/LiveFolders.md) | A LiveFolder is a special folder whose content is provided by a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#`. |
| --- | --- |
| [MediaStore](../android/provider/MediaStore.md) | The contract between the media provider and applications. |
| [PeopleContract](../android/provider/PeopleContract.md) | Defines the contract between client applications, People Directory applications (such as VoIP and messaging services), and the system's People Provider. |
| [SearchRecentSuggestions](../android/provider/SearchRecentSuggestions.md) | This is a utility class providing access to `https://developer.android.com/reference/kotlin/android/content/SearchRecentSuggestionsProvider.html#`. |
| --- | --- |
| [Settings](../android/provider/Settings.md) | The Settings provider contains global system-level device preferences. |
| [SettingsSlicesContract](../android/provider/SettingsSlicesContract.md) | Provides a contract for platform-supported Settings `https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#`. |
| [SimPhonebookContract](../android/provider/SimPhonebookContract.md) | The contract between the provider of contact records on the device's SIM cards and applications. |
| --- | --- |
| [SyncStateContract](../android/provider/SyncStateContract.md) | The ContentProvider contract for associating data with ana data array account. |
| [Telephony](../android/provider/Telephony.md) | The Telephony provider contains data related to phone operation, specifically SMS and MMS messages, access to the APN list, including the MMSC to use, and the service state. |
| [UserDictionary](../android/provider/UserDictionary.md) | A provider of user defined words for input methods to use for predictive text input. |
| --- | --- |
| [VoicemailContract](../android/provider/VoicemailContract.md) | The contract between the voicemail provider and applications. |
