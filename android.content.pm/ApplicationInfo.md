Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ApplicationInfo

```
open class ApplicationInfo : PackageItemInfo, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.content.pm.PackageItemInfo](PackageItemInfo.md) ||
| | ↳ | [android.content.pm.ApplicationInfo](ApplicationInfo.md) |

Information you can retrieve about a particular application. This corresponds to information collected from the AndroidManifest.xml's \<application\> tag.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.DisplayNameComparator` <br /> |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_ACCESSIBILITY:kotlin.Int` Category for apps which are primarily accessibility apps, such as screen-readers. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_AUDIO:kotlin.Int` Category for apps which primarily work with audio or music, such as music players. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_GAME:kotlin.Int` Category for apps which are primarily games. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_IMAGE:kotlin.Int` Category for apps which primarily work with images or photos, such as camera or gallery apps. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_MAPS:kotlin.Int` Category for apps which are primarily maps apps, such as navigation apps. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_NEWS:kotlin.Int` Category for apps which are primarily news apps, such as newspapers, magazines, or sports apps. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_PRODUCTIVITY:kotlin.Int` Category for apps which are primarily productivity apps, such as cloud storage or workplace apps. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_SOCIAL:kotlin.Int` Category for apps which are primarily social apps, such as messaging, communication, email, or social network apps. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_UNDEFINED:kotlin.Int` Value when category is undefined. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_VIDEO:kotlin.Int` Category for apps which primarily work with video or movies, such as streaming video apps. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_ALLOW_BACKUP:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: set to `false` if the application does not wish to permit any OS-driven backups of its data; `true` otherwise. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_ALLOW_CLEAR_USER_DATA:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: default value for the corresponding ActivityInfo flag. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_ALLOW_TASK_REPARENTING:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: default value for the corresponding ActivityInfo flag. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_DEBUGGABLE:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: set to true if this application would like to allow debugging of its code, even when installed on a non-development system. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_EXTERNAL_STORAGE:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: Set to true if the application is currently installed on external/removable/unprotected storage. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_EXTRACT_NATIVE_LIBS:kotlin.Int` When set installer extracts native libs from . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_FACTORY_TEST:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: set to true if this application holds the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#FACTORY_TEST:kotlin.String` permission and the device is running in factory test mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_FULL_BACKUP_ONLY:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: `true` if the application asks that only full-data streaming backups of its data be performed even though it defines a `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent.html#`, which normally indicates that the app will manage its backed-up data via incremental key/value updates. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_HARDWARE_ACCELERATED:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: `true` when the application's rendering should be hardware accelerated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_HAS_CODE:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: set to true if this application has code associated with it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_INSTALLED:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true if the application is currently installed for the calling user. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_IS_DATA_ONLY:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true if the application only has its data installed; the application package itself does not currently exist on the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_IS_GAME:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true if the application was declared to be a game, or false if it is a non-game application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_KILL_AFTER_RESTORE:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: set to `false` if the application must be kept in memory following a full-system restore operation; `true` otherwise. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_LARGE_HEAP:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true when the application has requested a large heap for its processes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_MULTIARCH:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true if code from this application will need to be loaded into other applications' processes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_PERSISTENT:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: set to true if this application is persistent. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_RESIZEABLE_FOR_SCREENS:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true when the application knows how to adjust its UI for different screen sizes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_RESTORE_ANY_VERSION:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: Set to `true` if the application's backup agent claims to be able to handle restore data even "from the future," i. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_STOPPED:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true if this application's package is in the stopped state. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_SUPPORTS_LARGE_SCREENS:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true when the application's window can be increased in size for larger screens. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_SUPPORTS_NORMAL_SCREENS:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true when the application's window can be displayed on normal screens. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_SUPPORTS_RTL:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true when the application is willing to support RTL (right to left). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_SUPPORTS_SCREEN_DENSITIES:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true when the application knows how to accommodate different screen densities. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_SUPPORTS_SMALL_SCREENS:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true when the application's window can be reduced in size for smaller screens. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_SUPPORTS_XLARGE_SCREENS:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true when the application's window can be increased in size for extra large screens. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_SUSPENDED:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true if this application's package is in the suspended state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_SYSTEM:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: if set, this application is installed in the device's system image. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_TEST_ONLY:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: this is set if the application has specified `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_testOnly:kotlin.Int` to be true. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_UPDATED_SYSTEM_APP:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: this is set if this application has been installed as an update to a built-in system application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_USES_CLEARTEXT_TRAFFIC:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: `true` if the application may use cleartext network traffic (e.g., HTTP rather than HTTPS; WebSockets rather than WebSockets Secure; XMPP, IMAP, SMTP without STARTTLS or TLS). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_VM_SAFE_MODE:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: set to true if this application would like to request the VM to operate under the safe mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#GWP_ASAN_ALWAYS:kotlin.Int` Always enable GWP-ASan in this application or process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#GWP_ASAN_DEFAULT:kotlin.Int` Default (unspecified) setting of GWP-ASan. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#GWP_ASAN_NEVER:kotlin.Int` Never enable GWP-ASan in this application or process. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#MEMTAG_ASYNC:kotlin.Int` Enable Memtag in Async mode in this application or process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#MEMTAG_DEFAULT:kotlin.Int` Default (unspecified) setting of Memtag. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#MEMTAG_OFF:kotlin.Int` Do not enable Memtag in this application or process. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#MEMTAG_SYNC:kotlin.Int` Enable Memtag in Sync mode in this application or process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#RAW_EXTERNAL_STORAGE_ACCESS_DEFAULT:kotlin.Int` Use default value for `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_requestRawExternalStorageAccess:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#RAW_EXTERNAL_STORAGE_ACCESS_NOT_REQUESTED:kotlin.Int` Raw external storage was not requested by this app. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#RAW_EXTERNAL_STORAGE_ACCESS_REQUESTED:kotlin.Int` Raw external storage was requested by this app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#ZEROINIT_DEFAULT:kotlin.Int` Default (unspecified) setting of nativeHeapZeroInitialized. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#ZEROINIT_DISABLED:kotlin.Int` Disable zero-initialization of the native heap in this application or process. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#ZEROINIT_ENABLED:kotlin.Int` Enable zero-initialization of the native heap in this application or process. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#ApplicationInfo()()` <br /> |
| `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#ApplicationInfo(android.content.pm.ApplicationInfo)(orig: https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#!)` <br /> |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#areAttributionsUserVisible()()` Returns whether attributions provided by the application are meant to be user-visible. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#dump(android.util.Printer,%20kotlin.String)(pw: https://developer.android.com/reference/kotlin/android/util/Printer.html#!, prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> |
| --- | --- |
| open static [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#getCategoryTitle(android.content.Context,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, category: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return a concise, localized title for the given `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#category:kotlin.Int` value, or `null` for unknown values such as `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_UNDEFINED:kotlin.Int`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#getGwpAsanMode()()` <br /> |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#getKnownActivityEmbeddingCerts()()` Gets the trusted host certificate digests of apps that are allowed to embed activities of this application. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#getMemtagMode()()` Returns whether the application has requested Memtag to be enabled, disabled, or left unspecified. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#getNativeHeapZeroInitialized()()` Returns whether the application has requested automatic zero-initialization of native heap memory allocations to be enabled or disabled. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#getRequestRawExternalStorageAccess()()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#isProfileable()()` Returns whether this application can be profiled, either by the shell user or the system. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#isProfileableByShell()()` Returns whether or not this application can be profiled by the shell user, even when running on a device that is running in user mode. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#isResourceOverlay()()` Returns true if the package has declared in its manifest that it is a runtime resource overlay. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#isVirtualPreload()()` Returns whether or not this application was installed as a virtual preload. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#loadDescription(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)` Retrieve the textual description of the application. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#toString()()` Returns a string representation of the object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, parcelableFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#dumpBack(android.util.Printer,%20kotlin.String)(pw: https://developer.android.com/reference/kotlin/android/util/Printer.html#!, prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#dumpFront(android.util.Printer,%20kotlin.String)(pw: https://developer.android.com/reference/kotlin/android/util/Printer.html#!, prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadBanner(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)`

Retrieve the current graphical banner associated with this item. This will call back on the given PackageManager to load the banner from the application.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadIcon(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)`

Retrieve the current graphical icon associated with this item. This will call back on the given PackageManager to load the icon from the application.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadLabel(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager)`

Retrieve the current textual label associated with this item. This will call back on the given PackageManager to load the label from the application.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadLogo(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)`

Retrieve the current graphical logo associated with this item. This will call back on the given PackageManager to load the logo from the application.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadUnbadgedIcon(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!)`

Retrieve the current graphical icon associated with this item without the addition of a work badge if applicable. This will call back on the given PackageManager to load the icon from the application.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#loadXmlMetaData(android.content.pm.PackageManager,%20kotlin.String)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager!, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Load an XML resource attached to the meta-data of this item. This will retrieved the name meta-data entry, and if defined call back on the given PackageManager to load its XML file from the application.

<br />

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ApplicationInfo](ApplicationInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CREATOR:android.os.Parcelable.Creator` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#appComponentFactory:kotlin.String` The factory of this package, as specified by the \<manifest\> tag's `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_appComponentFactory:kotlin.Int` attribute. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#backupAgentName:kotlin.String` Class implementing the Application's backup functionality. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#category:kotlin.Int` The category of this app. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#className:kotlin.String` Class implementing the Application object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#compatibleWidthLimitDp:kotlin.Int` The maximum smallest screen width the application is designed for. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#compileSdkVersion:kotlin.Int` The user-visible SDK version (ex. 26) of the framework against which the application claims to have been compiled, or |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#compileSdkVersionCodename:kotlin.String` The development codename (ex. "S", "REL") of the framework against which the application claims to have been compiled, or |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#dataDir:kotlin.String` Full path to the default directory assigned to the package for its persistent data. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#descriptionRes:kotlin.Int` A style resource identifier (in the package's resources) of the description of an application. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#deviceProtectedDataDir:kotlin.String` Full path to the device-protected directory assigned to the package for its persistent data. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#enabled:kotlin.Boolean` When false, indicates that all components within this application are considered disabled, regardless of their individually set enabled status. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int` Flags associated with the application. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#isAppLockEnabled:kotlin.Boolean` App lock enablement state of an application. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#isAppLockSupported:kotlin.Boolean` If `true` this app supports App Lock. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#largestWidthLimitDp:kotlin.Int` The maximum smallest screen width the application will work on. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#manageSpaceActivityName:kotlin.String` Class implementing the Application's manage space functionality. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#minSdkVersion:kotlin.Int` The minimum SDK version this application can run on. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#nativeLibraryDir:kotlin.String` Full path to the directory where native JNI libraries are stored. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#permission:kotlin.String` Optional name of a permission required to be able to access this application's components. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#processName:kotlin.String` The name of the process this application should run in. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#publicSourceDir:kotlin.String` Full path to the publicly available parts of `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#sourceDir:kotlin.String`, including resources and manifest. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#requiresSmallestWidthDp:kotlin.Int` The required smallest screen width the application can run on. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#sharedLibraryFiles:kotlin.Array` Paths to all shared libraries this application is linked against. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#sourceDir:kotlin.String` Full path to the base APK for this application. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#splitNames:kotlin.Array` The names of all installed split APKs, ordered lexicographically. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#splitPublicSourceDirs:kotlin.Array` Full path to the publicly available parts of `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#splitSourceDirs:kotlin.Array`, including resources and manifest. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#splitSourceDirs:kotlin.Array` Full paths to split APKs, indexed by the same order as `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#splitNames:kotlin.Array`. |
| [UUID](../java.util/UUID.md)! | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#storageUuid:java.util.UUID` UUID of the storage volume on which this application is being hosted. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#targetSdkVersion:kotlin.Int` The minimum SDK version this application targets. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#taskAffinity:kotlin.String` Default task affinity of all activities in this application. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#theme:kotlin.Int` A style resource identifier (in the package's resources) of the default visual theme of the application. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#uiOptions:kotlin.Int` The default extra UI options for activities in this application. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#uid:kotlin.Int` The kernel user-ID that has been assigned to this application; currently this is not a unique ID (multiple applications can have the same uid). |

Inherited properties From class `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#banner:kotlin.Int`

A drawable resource identifier (in the package's resources) of this component's banner. From the "banner" attribute or, if not set, 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#icon:kotlin.Int`

A drawable resource identifier (in the package's resources) of this component's icon. From the "icon" attribute or, if not set, 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#isArchived:kotlin.Boolean`

Whether the package is currently in an archived state.

Packages can be archived through `https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller#requestArchive(kotlin.String,%20android.content.IntentSender)` and do not have any APKs stored on the device, but do keep the data directory.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#labelRes:kotlin.Int`

A string resource identifier (in the package's resources) of this component's label. From the "label" attribute or, if not set, 0.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#logo:kotlin.Int`

A drawable resource identifier (in the package's resources) of this component's logo. Logos may be larger/wider than icons and are displayed by certain UI elements in place of a name or name/icon combination. From the "logo" attribute or, if not set, 0.

<br />

`https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#metaData:android.os.Bundle`

Additional meta-data associated with this component. This field will only be filled in if you set the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_META_DATA:kotlin.Int` flag when requesting the info.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#name:kotlin.String`

Public name of this item. From the "android:name" attribute.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#nonLocalizedLabel:kotlin.CharSequence`

The string provided in the AndroidManifest file, if any. You probably don't want to use this. You probably want `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationLabel(android.content.pm.ApplicationInfo)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#packageName:kotlin.String`

Name of the package that this item is in.

<br />

## Constants

### CATEGORY_ACCESSIBILITY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_ACCESSIBILITY: Int
```

Category for apps which are primarily accessibility apps, such as screen-readers.

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#category:kotlin.Int`

### CATEGORY_AUDIO

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_AUDIO: Int
```

Category for apps which primarily work with audio or music, such as music players.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#category:kotlin.Int`

### CATEGORY_GAME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_GAME: Int
```

Category for apps which are primarily games.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#category:kotlin.Int`

### CATEGORY_IMAGE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_IMAGE: Int
```

Category for apps which primarily work with images or photos, such as camera or gallery apps.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#category:kotlin.Int`

### CATEGORY_MAPS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_MAPS: Int
```

Category for apps which are primarily maps apps, such as navigation apps.

 Value: 6

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#category:kotlin.Int`

### CATEGORY_NEWS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_NEWS: Int
```

Category for apps which are primarily news apps, such as newspapers, magazines, or sports apps.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#category:kotlin.Int`

### CATEGORY_PRODUCTIVITY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_PRODUCTIVITY: Int
```

Category for apps which are primarily productivity apps, such as cloud storage or workplace apps.

 Value: 7

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#category:kotlin.Int`

### CATEGORY_SOCIAL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_SOCIAL: Int
```

Category for apps which are primarily social apps, such as messaging, communication, email, or social network apps.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#category:kotlin.Int`

### CATEGORY_UNDEFINED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_UNDEFINED: Int
```

Value when category is undefined.

 Value: -1

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#category:kotlin.Int`

### CATEGORY_VIDEO

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_VIDEO: Int
```

Category for apps which primarily work with video or movies, such as streaming video apps.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#category:kotlin.Int`

### FLAG_ALLOW_BACKUP

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_ALLOW_BACKUP: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: set to `false` if the application does not wish to permit any OS-driven backups of its data; `true` otherwise.

Comes from the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_allowBackup:kotlin.Int` attribute of the \<application\> tag.

 Value: 32768

### FLAG_ALLOW_CLEAR_USER_DATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_ALLOW_CLEAR_USER_DATA: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: default value for the corresponding ActivityInfo flag. Comes from `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_allowClearUserData:kotlin.Int` of the \<application\> tag.

 Value: 64

### FLAG_ALLOW_TASK_REPARENTING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_ALLOW_TASK_REPARENTING: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: default value for the corresponding ActivityInfo flag. Comes from `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_allowTaskReparenting:kotlin.Int` of the \<application\> tag.

 Value: 32

### FLAG_DEBUGGABLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_DEBUGGABLE: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: set to true if this application would like to allow debugging of its code, even when installed on a non-development system. Comes from `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_debuggable:kotlin.Int` of the \<application\> tag.

 Value: 2

### FLAG_EXTERNAL_STORAGE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_EXTERNAL_STORAGE: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: Set to true if the application is currently installed on external/removable/unprotected storage. Such applications may not be available if their storage is not currently mounted. When the storage it is on is not available, it will look like the application has been uninstalled (its .apk is no longer available) but its persistent data is not removed.

 Value: 262144

### FLAG_EXTRACT_NATIVE_LIBS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_EXTRACT_NATIVE_LIBS: Int
```

When set installer extracts native libs from .apk files.

 Value: 268435456

### FLAG_FACTORY_TEST

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_FACTORY_TEST: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: set to true if this application holds the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#FACTORY_TEST:kotlin.String` permission and the device is running in factory test mode.

 Value: 16

### FLAG_FULL_BACKUP_ONLY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_FULL_BACKUP_ONLY: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: `true` if the application asks that only full-data streaming backups of its data be performed even though it defines a `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent.html#`, which normally indicates that the app will manage its backed-up data via incremental key/value updates.

 Value: 67108864

### FLAG_HARDWARE_ACCELERATED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_HARDWARE_ACCELERATED: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: `true` when the application's rendering should be hardware accelerated.

 Value: 536870912

### FLAG_HAS_CODE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_HAS_CODE: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: set to true if this application has code associated with it. Comes from `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_hasCode:kotlin.Int` of the \<application\> tag.

 Value: 4

### FLAG_INSTALLED

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_INSTALLED: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true if the application is currently installed for the calling user.

 Value: 8388608

### FLAG_IS_DATA_ONLY

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_IS_DATA_ONLY: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true if the application only has its data installed; the application package itself does not currently exist on the device.

 Value: 16777216

### FLAG_IS_GAME

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_IS_GAME: Int
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_GAME:kotlin.Int` instead.*

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true if the application was declared to be a game, or false if it is a non-game application.

 Value: 33554432

### FLAG_KILL_AFTER_RESTORE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_KILL_AFTER_RESTORE: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: set to `false` if the application must be kept in memory following a full-system restore operation; `true` otherwise. Ordinarily, during a full system restore operation each application is shut down following execution of its agent's onRestore() method. Setting this attribute to `false` prevents this. Most applications will not need to set this attribute.

If `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_allowBackup:kotlin.Int` is set to `false` or no `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_backupAgent:kotlin.Int` is specified, this flag will be ignored.

Comes from the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_killAfterRestore:kotlin.Int` attribute of the \<application\> tag.

 Value: 65536

### FLAG_LARGE_HEAP

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_LARGE_HEAP: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true when the application has requested a large heap for its processes. Corresponds to `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_largeHeap:kotlin.Int`.

 Value: 1048576

### FLAG_MULTIARCH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_MULTIARCH: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true if code from this application will need to be loaded into other applications' processes. On devices that support multiple instruction sets, this implies the code might be loaded into a process that's using any of the devices supported instruction sets.

The system might treat such applications specially, for eg., by extracting the application's native libraries for all supported instruction sets or by compiling the application's dex code for all supported instruction sets.

 Value: -2147483648

### FLAG_PERSISTENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_PERSISTENT: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: set to true if this application is persistent. Comes from `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_persistent:kotlin.Int` of the \<application\> tag.

 Value: 8

### FLAG_RESIZEABLE_FOR_SCREENS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_RESIZEABLE_FOR_SCREENS: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true when the application knows how to adjust its UI for different screen sizes. Corresponds to `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestSupportsScreens_resizeable:kotlin.Int`.

 Value: 4096

### FLAG_RESTORE_ANY_VERSION

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_RESTORE_ANY_VERSION: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: Set to `true` if the application's backup agent claims to be able to handle restore data even "from the future," i.e. from versions of the application with a versionCode greater than the one currently installed on the device. *Use with caution!* By default this attribute is `false` and the Backup Manager will ensure that data from "future" versions of the application are never supplied during a restore operation.

If `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_allowBackup:kotlin.Int` is set to `false` or no `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_backupAgent:kotlin.Int` is specified, this flag will be ignored.

Comes from the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_restoreAnyVersion:kotlin.Int` attribute of the \<application\> tag.

 Value: 131072

### FLAG_STOPPED

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_STOPPED: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true if this application's package is in the stopped state.

Stopped is the initial state after an app is installed, before it is launched or otherwise directly interacted with by the user. The system tries not to start it unless initiated by a user interaction (typically launching its icon from the launcher, could also include user actions like adding it as an app widget, selecting it as a live wallpaper, selecting it as a keyboard, etc). Stopped applications will not receive implicit broadcasts unless the sender specifies `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_INCLUDE_STOPPED_PACKAGES:kotlin.Int`.

Applications should avoid launching activities, binding to or starting services, or otherwise causing a stopped application to run unless initiated by the user.

An app can also return to the stopped state by a "force stop".

 Value: 2097152

### FLAG_SUPPORTS_LARGE_SCREENS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SUPPORTS_LARGE_SCREENS: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true when the application's window can be increased in size for larger screens. Corresponds to `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestSupportsScreens_largeScreens:kotlin.Int`.

 Value: 2048

### FLAG_SUPPORTS_NORMAL_SCREENS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SUPPORTS_NORMAL_SCREENS: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true when the application's window can be displayed on normal screens. Corresponds to `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestSupportsScreens_normalScreens:kotlin.Int`.

 Value: 1024

### FLAG_SUPPORTS_RTL

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SUPPORTS_RTL: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true when the application is willing to support RTL (right to left). All activities will inherit this value. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#supportsRtl:kotlin.Int` attribute in the activity's manifest. Default value is false (no support for RTL).

 Value: 4194304

### FLAG_SUPPORTS_SCREEN_DENSITIES

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SUPPORTS_SCREEN_DENSITIES: Int
```

**Deprecated:** *Set by default when targeting API 4 or higher and apps should not set this to false.*

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true when the application knows how to accommodate different screen densities. Corresponds to `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestSupportsScreens_anyDensity:kotlin.Int`.

 Value: 8192

### FLAG_SUPPORTS_SMALL_SCREENS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SUPPORTS_SMALL_SCREENS: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true when the application's window can be reduced in size for smaller screens. Corresponds to `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestSupportsScreens_smallScreens:kotlin.Int`.

 Value: 512

### FLAG_SUPPORTS_XLARGE_SCREENS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SUPPORTS_XLARGE_SCREENS: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true when the application's window can be increased in size for extra large screens. Corresponds to `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestSupportsScreens_xlargeScreens:kotlin.Int`.

 Value: 524288

### FLAG_SUSPENDED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SUSPENDED: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: true if this application's package is in the suspended state.

 Value: 1073741824

### FLAG_SYSTEM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SYSTEM: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: if set, this application is installed in the device's system image. This should not be used to make security decisions. Instead, rely on [signature checks](PackageManager.md)) or [permissions](https://developer.android.com/training/articles/security-tips#Permissions).

**Warning:** Note that this flag does not behave the same as `https://developer.android.com/reference/kotlin/android/R.attr.html#protectionLevel:kotlin.Int` `system` or `signatureOrSystem`.

 Value: 1

### FLAG_TEST_ONLY

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_TEST_ONLY: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: this is set if the application has specified `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_testOnly:kotlin.Int` to be true.

 Value: 256

### FLAG_UPDATED_SYSTEM_APP

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_UPDATED_SYSTEM_APP: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: this is set if this application has been installed as an update to a built-in system application.

 Value: 128

### FLAG_USES_CLEARTEXT_TRAFFIC

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_USES_CLEARTEXT_TRAFFIC: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: `true` if the application may use cleartext network traffic (e.g., HTTP rather than HTTPS; WebSockets rather than WebSockets Secure; XMPP, IMAP, SMTP without STARTTLS or TLS). If `false`, the app declares that it does not intend to use cleartext network traffic, in which case platform components (e.g., HTTP stacks, `DownloadManager`, `MediaPlayer`) will refuse app's requests to use cleartext traffic. Third-party libraries are encouraged to honor this flag as well.

NOTE: `WebView` honors this flag for applications targeting API level 26 and up.

This flag is ignored on Android N and above if an Android Network Security Config is present.

This flag comes from `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_usesCleartextTraffic:kotlin.Int` of the \<application\> tag.

 Value: 134217728

### FLAG_VM_SAFE_MODE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_VM_SAFE_MODE: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#flags:kotlin.Int`: set to true if this application would like to request the VM to operate under the safe mode. Comes from `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_vmSafeMode:kotlin.Int` of the \<application\> tag.

 Value: 16384

### GWP_ASAN_ALWAYS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GWP_ASAN_ALWAYS: Int
```

Always enable GWP-ASan in this application or process.

 Value: 1

### GWP_ASAN_DEFAULT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GWP_ASAN_DEFAULT: Int
```

Default (unspecified) setting of GWP-ASan.

 Value: -1

### GWP_ASAN_NEVER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GWP_ASAN_NEVER: Int
```

Never enable GWP-ASan in this application or process.

 Value: 0

### MEMTAG_ASYNC

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEMTAG_ASYNC: Int
```

Enable Memtag in Async mode in this application or process.

 Value: 1

### MEMTAG_DEFAULT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEMTAG_DEFAULT: Int
```

Default (unspecified) setting of Memtag.

 Value: -1

### MEMTAG_OFF

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEMTAG_OFF: Int
```

Do not enable Memtag in this application or process.

 Value: 0

### MEMTAG_SYNC

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEMTAG_SYNC: Int
```

Enable Memtag in Sync mode in this application or process.

 Value: 2

### RAW_EXTERNAL_STORAGE_ACCESS_DEFAULT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RAW_EXTERNAL_STORAGE_ACCESS_DEFAULT: Int
```

Use default value for `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_requestRawExternalStorageAccess:kotlin.Int`.

 Value: 0

### RAW_EXTERNAL_STORAGE_ACCESS_NOT_REQUESTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RAW_EXTERNAL_STORAGE_ACCESS_NOT_REQUESTED: Int
```

Raw external storage was not requested by this app.

 Value: 2

### RAW_EXTERNAL_STORAGE_ACCESS_REQUESTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RAW_EXTERNAL_STORAGE_ACCESS_REQUESTED: Int
```

Raw external storage was requested by this app.

 Value: 1

### ZEROINIT_DEFAULT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ZEROINIT_DEFAULT: Int
```

Default (unspecified) setting of nativeHeapZeroInitialized.

 Value: -1

### ZEROINIT_DISABLED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ZEROINIT_DISABLED: Int
```

Disable zero-initialization of the native heap in this application or process.

 Value: 0

### ZEROINIT_ENABLED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ZEROINIT_ENABLED: Int
```

Enable zero-initialization of the native heap in this application or process.

 Value: 1

## Public constructors

### ApplicationInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ApplicationInfo()
```

### ApplicationInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ApplicationInfo(orig: ApplicationInfo!)
```

## Public methods

### areAttributionsUserVisible

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun areAttributionsUserVisible(): Boolean
```

Returns whether attributions provided by the application are meant to be user-visible. Defaults to false if application info is retrieved without `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_ATTRIBUTIONS_LONG:kotlin.Long`.

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### dump

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dump(
    pw: Printer!, 
    prefix: String!
): Unit
```

### getCategoryTitle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getCategoryTitle(
    context: Context!, 
    category: Int
): CharSequence!
```

Return a concise, localized title for the given `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#category:kotlin.Int` value, or `null` for unknown values such as `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_UNDEFINED:kotlin.Int`.

| Parameters ||
|---|---|
| `category` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_UNDEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_GAME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_AUDIO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_VIDEO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_IMAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_SOCIAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_NEWS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_MAPS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_PRODUCTIVITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_ACCESSIBILITY:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#category:kotlin.Int`

### getGwpAsanMode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGwpAsanMode(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#GWP_ASAN_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#GWP_ASAN_NEVER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#GWP_ASAN_ALWAYS:kotlin.Int` |

### getKnownActivityEmbeddingCerts

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getKnownActivityEmbeddingCerts(): MutableSet<String!>
```

Gets the trusted host certificate digests of apps that are allowed to embed activities of this application. The digests are computed using the SHA-256 digest algorithm.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.attr.html#knownActivityEmbeddingCerts:kotlin.Int`

### getMemtagMode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMemtagMode(): Int
```

Returns whether the application has requested Memtag to be enabled, disabled, or left unspecified. Processes can override this setting.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#MEMTAG_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#MEMTAG_OFF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#MEMTAG_ASYNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#MEMTAG_SYNC:kotlin.Int` |

### getNativeHeapZeroInitialized

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNativeHeapZeroInitialized(): Int
```

Returns whether the application has requested automatic zero-initialization of native heap memory allocations to be enabled or disabled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#ZEROINIT_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#ZEROINIT_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#ZEROINIT_ENABLED:kotlin.Int` |

### getRequestRawExternalStorageAccess

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRequestRawExternalStorageAccess(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#RAW_EXTERNAL_STORAGE_ACCESS_DEFAULT:kotlin.Int` if app didn't specify `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_requestRawExternalStorageAccess:kotlin.Int` attribute in the manifest. - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#RAW_EXTERNAL_STORAGE_ACCESS_REQUESTED:kotlin.Int` if this app requested raw external storage access. - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#RAW_EXTERNAL_STORAGE_ACCESS_NOT_REQUESTED:kotlin.Int` if this app requests to disable raw external storage access Note that this doesn't give any hints on whether the app gets raw external storage access or not. Also, apps may get raw external storage access by default in some cases, see `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_requestRawExternalStorageAccess:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#RAW_EXTERNAL_STORAGE_ACCESS_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#RAW_EXTERNAL_STORAGE_ACCESS_REQUESTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#RAW_EXTERNAL_STORAGE_ACCESS_NOT_REQUESTED:kotlin.Int` |

### isProfileable

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isProfileable(): Boolean
```

Returns whether this application can be profiled, either by the shell user or the system.

### isProfileableByShell

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isProfileableByShell(): Boolean
```

Returns whether or not this application can be profiled by the shell user, even when running on a device that is running in user mode.

### isResourceOverlay

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isResourceOverlay(): Boolean
```

Returns true if the package has declared in its manifest that it is a runtime resource overlay.

### isVirtualPreload

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isVirtualPreload(): Boolean
```

Returns whether or not this application was installed as a virtual preload.

### loadDescription

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadDescription(pm: PackageManager!): CharSequence!
```

Retrieve the textual description of the application. This will call back on the given PackageManager to load the description from the application.

| Parameters ||
|---|---|
| `pm` | [PackageManager](PackageManager.md)!: A PackageManager from which the label can be loaded; usually the PackageManager from which you originally retrieved this item. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | Returns a CharSequence containing the application's description. If there is no description, null is returned. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel, 
    parcelableFlags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ApplicationInfo!>
```

### appComponentFactory

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var appComponentFactory: String!
```

The factory of this package, as specified by the \<manifest\> tag's `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_appComponentFactory:kotlin.Int` attribute.

### backupAgentName

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var backupAgentName: String!
```

Class implementing the Application's backup functionality. From the "backupAgent" attribute. This is an optional attribute and will be null if the application does not specify it in its manifest.

If android:allowBackup is set to false, this attribute is ignored.

### category

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var category: Int
```

The category of this app. Categories are used to cluster multiple apps together into meaningful groups, such as when summarizing battery, network, or disk usage. Apps should only define this value when they fit well into one of the specific categories.

Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#appCategory:kotlin.Int` attribute in the manifest. If the manifest doesn't define a category, this value may have been provided by the installer via `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#setApplicationCategoryHint(kotlin.String,%20kotlin.Int)`. 
Value is one of the following:

- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_UNDEFINED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_GAME:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_AUDIO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_VIDEO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_IMAGE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_SOCIAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_NEWS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_MAPS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_PRODUCTIVITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_ACCESSIBILITY:kotlin.Int`

### className

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var className: String!
```

Class implementing the Application object. From the "class" attribute.

### compatibleWidthLimitDp

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var compatibleWidthLimitDp: Int
```

The maximum smallest screen width the application is designed for. If 0, nothing has been specified. Comes from `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestSupportsScreens_compatibleWidthLimitDp:kotlin.Int` attribute of the \<supports-screens\> tag.

### compileSdkVersion

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var compileSdkVersion: Int
```

The user-visible SDK version (ex. 26) of the framework against which the application claims to have been compiled, or `0` if not specified.

This property is the compile-time equivalent of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION.html#CODENAME:kotlin.String`.

### compileSdkVersionCodename

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var compileSdkVersionCodename: String?
```

The development codename (ex. "S", "REL") of the framework against which the application claims to have been compiled, or `null` if not specified.

This property is the compile-time equivalent of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION.html#CODENAME:kotlin.String`.

### dataDir

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var dataDir: String!
```

Full path to the default directory assigned to the package for its persistent data.

### descriptionRes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var descriptionRes: Int
```

A style resource identifier (in the package's resources) of the description of an application. From the "description" attribute or, if not set, 0.

### deviceProtectedDataDir

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var deviceProtectedDataDir: String!
```

Full path to the device-protected directory assigned to the package for its persistent data.
**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Context.html#createDeviceProtectedStorageContext()`

### enabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var enabled: Boolean
```

When false, indicates that all components within this application are considered disabled, regardless of their individually set enabled status.

### flags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var flags: Int
```

Flags associated with the application. Any combination of `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_SYSTEM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_DEBUGGABLE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_HAS_CODE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_PERSISTENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_FACTORY_TEST:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_ALLOW_TASK_REPARENTING:kotlin.Int` `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_ALLOW_CLEAR_USER_DATA:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_UPDATED_SYSTEM_APP:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_TEST_ONLY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_SUPPORTS_SMALL_SCREENS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_SUPPORTS_NORMAL_SCREENS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_SUPPORTS_LARGE_SCREENS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_SUPPORTS_XLARGE_SCREENS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_RESIZEABLE_FOR_SCREENS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_SUPPORTS_SCREEN_DENSITIES:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_VM_SAFE_MODE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_ALLOW_BACKUP:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_KILL_AFTER_RESTORE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_RESTORE_ANY_VERSION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_EXTERNAL_STORAGE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_LARGE_HEAP:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_STOPPED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_SUPPORTS_RTL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_INSTALLED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_IS_DATA_ONLY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_IS_GAME:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_FULL_BACKUP_ONLY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_USES_CLEARTEXT_TRAFFIC:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_MULTIARCH:kotlin.Int`.

### isAppLockEnabled

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var isAppLockEnabled: Boolean
```

App lock enablement state of an application. This field is only set if the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_APP_LOCK_INFO:kotlin.Long` was used when retrieving the application info and the caller has the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#LOCK_APPS:kotlin.String` permission and will default to `false`. To enable App Lock for a package, call `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getEnableAppLockIntentForPackage(kotlin.String,%20kotlin.Boolean)`.

### isAppLockSupported

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var isAppLockSupported: Boolean
```

If `true` this app supports App Lock. This field is only set if the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_APP_LOCK_INFO:kotlin.Long` was used when retrieving the application info and the caller has the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#LOCK_APPS:kotlin.String` permission, and will default to `false`. To enable App Lock for a package, call `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getEnableAppLockIntentForPackage(kotlin.String,%20kotlin.Boolean)`.

### largestWidthLimitDp

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var largestWidthLimitDp: Int
```

The maximum smallest screen width the application will work on. If 0, nothing has been specified. Comes from `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestSupportsScreens_largestWidthLimitDp:kotlin.Int` attribute of the \<supports-screens\> tag.

### manageSpaceActivityName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var manageSpaceActivityName: String!
```

Class implementing the Application's manage space functionality. From the "manageSpaceActivity" attribute. This is an optional attribute and will be null if applications don't specify it in their manifest

### minSdkVersion

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var minSdkVersion: Int
```

The minimum SDK version this application can run on. It will not run on earlier versions.

### nativeLibraryDir

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var nativeLibraryDir: String!
```

Full path to the directory where native JNI libraries are stored.

### permission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var permission: String!
```

Optional name of a permission required to be able to access this application's components. From the "permission" attribute.

### processName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var processName: String!
```

The name of the process this application should run in. From the "process" attribute or, if not set, the same as packageName.

### publicSourceDir

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var publicSourceDir: String!
```

Full path to the publicly available parts of `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#sourceDir:kotlin.String`, including resources and manifest. This may be different from `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#sourceDir:kotlin.String` if an application is forward locked.

### requiresSmallestWidthDp

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var requiresSmallestWidthDp: Int
```

The required smallest screen width the application can run on. If 0, nothing has been specified. Comes from `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestSupportsScreens_requiresSmallestWidthDp:kotlin.Int` attribute of the \<supports-screens\> tag.

### sharedLibraryFiles

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var sharedLibraryFiles: Array<String!>!
```

Paths to all shared libraries this application is linked against. This field is only set if the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_SHARED_LIBRARY_FILES:kotlin.Int` flag was used when retrieving the structure.

### sourceDir

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var sourceDir: String!
```

Full path to the base APK for this application.

### splitNames

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var splitNames: Array<String!>?
```

The names of all installed split APKs, ordered lexicographically. May be null if no splits are installed.

### splitPublicSourceDirs

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var splitPublicSourceDirs: Array<String!>?
```

Full path to the publicly available parts of `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#splitSourceDirs:kotlin.Array`, including resources and manifest. This may be different from `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#splitSourceDirs:kotlin.Array` if an application is forward locked. May be null if no splits are installed.
**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#splitSourceDirs:kotlin.Array`

### splitSourceDirs

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var splitSourceDirs: Array<String!>?
```

Full paths to split APKs, indexed by the same order as `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#splitNames:kotlin.Array`. May be null if no splits are installed.

### storageUuid

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var storageUuid: UUID!
```

UUID of the storage volume on which this application is being hosted. For apps hosted on the default internal storage at `https://developer.android.com/reference/kotlin/android/os/Environment.html#getDataDirectory()`, the UUID value is `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#UUID_DEFAULT:java.util.UUID`.

### targetSdkVersion

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var targetSdkVersion: Int
```

The minimum SDK version this application targets. It may run on earlier versions, but it knows how to work with any new behavior added at this version. Will be `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CUR_DEVELOPMENT:kotlin.Int` if this is a development build and the app is targeting that. You should compare that this number is \>= the SDK version number at which your behavior was introduced.

### taskAffinity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var taskAffinity: String!
```

Default task affinity of all activities in this application. See `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo#taskAffinity:kotlin.String` for more information. This comes from the "taskAffinity" attribute.

### theme

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var theme: Int
```

A style resource identifier (in the package's resources) of the default visual theme of the application. From the "theme" attribute or, if not set, 0.

### uiOptions

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var uiOptions: Int
```

The default extra UI options for activities in this application. Set from the `https://developer.android.com/reference/kotlin/android/R.attr.html#uiOptions:kotlin.Int` attribute in the activity's manifest.

### uid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var uid: Int
```

The kernel user-ID that has been assigned to this application; currently this is not a unique ID (multiple applications can have the same uid).
