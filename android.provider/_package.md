# android.provider

## Interfaces

| [BaseColumns](https://developer.android.com/reference/kotlin/android/provider/BaseColumns) | <br /> |
| --- | --- |
| [AttendeesColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns) | Columns from the Attendees table that other tables join into themselves. |
| [CalendarAlertsColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns) | <br /> |
| [CalendarCacheColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarCacheColumns) | <br /> |
| --- | --- |
| [CalendarColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns) | Columns specific to the Calendars Uri that other Uris can query. |
| [CalendarSyncColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns) | Generic columns for use by sync adapters. |
| [ColorsColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ColorsColumns) | <br /> |
| --- | --- |
| [EventDaysColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventDaysColumns) | <br /> |
| [EventsColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventsColumns) | Columns from the Events table that other tables join into themselves. |
| [ExtendedPropertiesColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ExtendedPropertiesColumns) | <br /> |
| --- | --- |
| [RemindersColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns) | <br /> |
| [SyncColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncColumns) | Columns for Sync information used by Calendars and Events tables. |
| [ContactMethodsColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethodsColumns) | Columns from the ContactMethods table that other tables join into themseleves. |
| --- | --- |
| [ExtensionsColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.ExtensionsColumns) | <br /> |
| [GroupsColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.GroupsColumns) | Columns from the groups table. |
| [OrganizationColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.OrganizationColumns) | Columns from the Organizations table that other columns join into themselves. |
| --- | --- |
| [PeopleColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.PeopleColumns) | Columns from the People table that other tables join into themselves. |
| [PhonesColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhonesColumns) | Columns from the Phones table that other columns join into themselves. |
| [PhotosColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhotosColumns) | Columns from the Photos table that other columns join into themselves. |
| --- | --- |
| [PresenceColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.PresenceColumns) | The IM presence columns with some contacts specific columns mixed in. |
| [SettingsColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.SettingsColumns) | Columns from the Settings table that other columns join into themselves. |
| [BaseSyncColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.BaseSyncColumns) | Generic columns for use by sync adapters. |
| --- | --- |
| [ContactNameColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns) | Contact name and contact name metadata columns in the RawContacts table. |
| [ContactOptionsColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactOptionsColumns) | Columns of `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts` that track the user's preferences for, or interactions with, the contact. |
| [ContactsColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns) | Columns of `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts` that refer to intrinsic properties of the contact, as opposed to the user-specified options found in `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactOptionsColumns`. |
| --- | --- |
| [ContactStatusColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactStatusColumns) | <br /> |
| [DataColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns) | Columns in the Data table. |
| [DataColumnsWithJoins](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumnsWithJoins) | Combines all columns returned by `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data` table queries. |
| --- | --- |
| [DataUsageStatColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataUsageStatColumns) | Columns in the Data_Usage_Stat table |
| [DeletedContactsColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DeletedContactsColumns) | <br /> |
| [DisplayNameSources](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayNameSources) | Types of data used to produce the display name for a contact. |
| --- | --- |
| [FullNameStyle](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.FullNameStyle) | Constants for various styles of combining given name, family name etc into a full name. |
| [GroupsColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.GroupsColumns) | <br /> |
| [PhoneLookupColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookupColumns) | <br /> |
| --- | --- |
| [PhoneticNameStyle](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneticNameStyle) | Constants for various styles of capturing the pronunciation of a person's name. |
| [PresenceColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PresenceColumns) | Additional data mixed in with `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns` to link back to specific `https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String` entries. |
| [RawContactsColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContactsColumns) | <br /> |
| --- | --- |
| [SettingsColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.SettingsColumns) | <br /> |
| [StatusColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns) | Social status update columns. |
| [SyncColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.SyncColumns) | Columns that appear when each row of a table belongs to a specific account, including sync information that an account may need. |
| --- | --- |
| [DownloadColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.DownloadColumns) | Download metadata columns. |
| [MediaColumns](https://developer.android.com/reference/kotlin/android/provider/MediaStore.MediaColumns) | Common media metadata columns. |
| [OpenableColumns](https://developer.android.com/reference/kotlin/android/provider/OpenableColumns) | These are standard columns for openable URIs. |
| --- | --- |
| [Columns](https://developer.android.com/reference/kotlin/android/provider/SyncStateContract.Columns) | <br /> |
| [BaseMmsColumns](https://developer.android.com/reference/kotlin/android/provider/Telephony.BaseMmsColumns) | Base columns for tables that contain MMSs. |
| [CanonicalAddressesColumns](https://developer.android.com/reference/kotlin/android/provider/Telephony.CanonicalAddressesColumns) | Columns for the "canonical_addresses" table used by MMS and SMS. |
| --- | --- |
| [TextBasedSmsColumns](https://developer.android.com/reference/kotlin/android/provider/Telephony.TextBasedSmsColumns) | Base columns for tables that contain text-based SMSs. |
| [ThreadsColumns](https://developer.android.com/reference/kotlin/android/provider/Telephony.ThreadsColumns) | Columns for the "threads" table used by MMS and SMS. |

## Classes

| [AlarmClock](https://developer.android.com/reference/kotlin/android/provider/AlarmClock) | The AlarmClock provider contains an Intent action and extras that can be used to start an Activity to set a new alarm or timer in an alarm clock application. |
| --- | --- |
| [BlockedNumberContract](https://developer.android.com/reference/kotlin/android/provider/BlockedNumberContract) | The contract between the blockednumber provider and applications. |
| [Browser](https://developer.android.com/reference/kotlin/android/provider/Browser) | <br /> |
| [CalendarContract](https://developer.android.com/reference/kotlin/android/provider/CalendarContract) | The contract between the calendar provider and applications. |
| --- | --- |
| [CallLog](https://developer.android.com/reference/kotlin/android/provider/CallLog) | The CallLog provider contains information about placed and received calls. |
| [CloudMediaProvider](https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider) | Base class for a cloud media provider. |
| [CloudMediaProviderContract](https://developer.android.com/reference/kotlin/android/provider/CloudMediaProviderContract) | Defines the contract between a cloud media provider and the OS. |
| --- | --- |
| [Contacts](https://developer.android.com/reference/kotlin/android/provider/Contacts) | The Contacts provider stores all information about contacts. |
| [ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract) | The contract between the contacts provider and applications. |
| [ContactsPickerSessionContract](https://developer.android.com/reference/kotlin/android/provider/ContactsPickerSessionContract) | The contract between the Contacts Picker session provider and client applications. |
| --- | --- |
| [DocumentsContract](https://developer.android.com/reference/kotlin/android/provider/DocumentsContract) | Defines the contract between a documents provider and the platform. |
| [DocumentsProvider](https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider) | Base class for a document provider. |
| [E2eeContactKeysManager](https://developer.android.com/reference/kotlin/android/provider/E2eeContactKeysManager) | E2eeContactKeysManager provides access to the provider of end-to-end encryption contact keys. |
| --- | --- |
| [FontRequest](https://developer.android.com/reference/kotlin/android/provider/FontRequest) | Information about a font request that may be sent to a Font Provider. |
| [FontsContract](https://developer.android.com/reference/kotlin/android/provider/FontsContract) | Utility class to deal with Font ContentProviders. |
| [LiveFolders](https://developer.android.com/reference/kotlin/android/provider/LiveFolders) | A LiveFolder is a special folder whose content is provided by a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#`. |
| --- | --- |
| [MediaStore](https://developer.android.com/reference/kotlin/android/provider/MediaStore) | The contract between the media provider and applications. |
| [PeopleContract](https://developer.android.com/reference/kotlin/android/provider/PeopleContract) | Defines the contract between client applications, People Directory applications (such as VoIP and messaging services), and the system's People Provider. |
| [SearchRecentSuggestions](https://developer.android.com/reference/kotlin/android/provider/SearchRecentSuggestions) | This is a utility class providing access to `https://developer.android.com/reference/kotlin/android/content/SearchRecentSuggestionsProvider.html#`. |
| --- | --- |
| [Settings](https://developer.android.com/reference/kotlin/android/provider/Settings) | The Settings provider contains global system-level device preferences. |
| [SettingsSlicesContract](https://developer.android.com/reference/kotlin/android/provider/SettingsSlicesContract) | Provides a contract for platform-supported Settings `https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#`. |
| [SimPhonebookContract](https://developer.android.com/reference/kotlin/android/provider/SimPhonebookContract) | The contract between the provider of contact records on the device's SIM cards and applications. |
| --- | --- |
| [SyncStateContract](https://developer.android.com/reference/kotlin/android/provider/SyncStateContract) | The ContentProvider contract for associating data with ana data array account. |
| [Telephony](https://developer.android.com/reference/kotlin/android/provider/Telephony) | The Telephony provider contains data related to phone operation, specifically SMS and MMS messages, access to the APN list, including the MMSC to use, and the service state. |
| [UserDictionary](https://developer.android.com/reference/kotlin/android/provider/UserDictionary) | A provider of user defined words for input methods to use for predictive text input. |
| --- | --- |
| [VoicemailContract](https://developer.android.com/reference/kotlin/android/provider/VoicemailContract) | The contract between the voicemail provider and applications. |
