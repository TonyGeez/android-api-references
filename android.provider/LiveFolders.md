# LiveFolders

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LiveFolders

Kotlin| [Java](LiveFolders.md) 
| --- | --- |

```
class LiveFolders : BaseColumns
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.LiveFolders](LiveFolders.md) |

| **This class was deprecated in API level 14.**
|
| Live folders are no longer supported by Android. These have been replaced by the new [AppWidget Collection](https://developer.android.com/guide/topics/appwidgets/index.html#collections) APIs introduced in [android.os.Build.VERSION_CODES#HONEYCOMB](../android/os/Build.VERSION_CODES.md). These provide all of the features of live folders plus many more. The use of live folders is greatly discouraged because of security issues they introduce -- publishing a live folder requires making all data show for the live folder available to all applications with no permissions protecting it.

A LiveFolder is a special folder whose content is provided by a [android.content.ContentProvider](../android.content/ContentProvider.md). To create a live folder, two components are required:

- An activity that can respond to the intent action [ACTION_CREATE_LIVE_FOLDER](LiveFolders.md). The activity is responsible for creating the live folder.
- A [android.content.ContentProvider](../android.content/ContentProvider.md) to provide the live folder items.

### Lifecycle

When a user wants to create a live folder, the system looks for all activities with the intent filter action [ACTION_CREATE_LIVE_FOLDER](LiveFolders.md) and presents the list to the user. When the user chooses one of the activities, the activity is invoked with the [ACTION_CREATE_LIVE_FOLDER](LiveFolders.md) action. The activity then creates the live folder and passes it back to the system by setting it as an [activity result](../android.app/Activity.md)). The live folder is described by a content provider URI, a name, an icon and a display mode. Finally, when the user opens the live folder, the system queries the content provider to retrieve the folder's content.

### Setting up the live folder activity

The following code sample shows how to write an activity that creates a live folder: 

```kotlin
public static class MyLiveFolder extends Activity {
      public static final Uri CONTENT_URI = Uri.parse("content://my.app/live");
 
      protected void onCreate(Bundle savedInstanceState) {
          super.onCreate(savedInstanceState);
 
          final Intent intent = getIntent();
          final String action = intent.getAction();
 
          if (LiveFolders.ACTION_CREATE_LIVE_FOLDER.equals(action)) {
              setResult(RESULT_OK, createLiveFolder(this, CONTENT_URI, "My LiveFolder",
                      R.drawable.ic_launcher_contacts_phones));
          } else {
              setResult(RESULT_CANCELED);
          }
 
          finish();
      }
 
      private static Intent createLiveFolder(Context context, Uri uri, String name,
              int icon) {
 
          final Intent intent = new Intent();
 
          intent.setData(uri);
          intent.putExtra(LiveFolders.EXTRA_LIVE_FOLDER_NAME, name);
          intent.putExtra(LiveFolders.EXTRA_LIVE_FOLDER_ICON,
                  Intent.ShortcutIconResource.fromContext(context, icon));
          intent.putExtra(LiveFolders.EXTRA_LIVE_FOLDER_DISPLAY_MODE, LiveFolders.DISPLAY_MODE_LIST);
 
          return intent;
      }
  }
  
```

The live folder is described by an [android.content.Intent](../android.content/Intent.md) as follows:

| Component | Type | Description | Required |
| --- | --- | --- | --- |
| URI | URI | The ContentProvider URI | Yes |
| [EXTRA_LIVE_FOLDER_NAME](LiveFolders.md) | Extra String | The name of the live folder | Yes |
| [EXTRA_LIVE_FOLDER_ICON](LiveFolders.md) | Extra [android.content.Intent.ShortcutIconResource](../android/content/Intent.ShortcutIconResource.md) | The icon of the live folder | Yes |
| --- | --- | --- | --- |
| [EXTRA_LIVE_FOLDER_DISPLAY_MODE](LiveFolders.md) | Extra int | The display mode of the live folder. The value must be either [DISPLAY_MODE_GRID](LiveFolders.md) or [DISPLAY_MODE_LIST](LiveFolders.md). | Yes |
| [EXTRA_LIVE_FOLDER_BASE_INTENT](LiveFolders.md) | Extra Intent | When the user clicks an item inside a live folder, the system will either fire the intent associated with that item or, if present, the live folder's base intent with the id of the item appended to the base intent's URI. | No |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|

### Setting up the content provider

The live folder's content provider must, upon query, return a [android.database.Cursor](../android.database/Cursor.md) whose columns match the following names:

| Column | Type | Description | Required |
| --- | --- | --- | --- |
| [NAME](LiveFolders.md) | String | The name of the item | Yes |
| [DESCRIPTION](LiveFolders.md) | String | The description of the item. The description is ignored when the live folder's display mode is [DISPLAY_MODE_GRID](LiveFolders.md). | No |
| [INTENT](LiveFolders.md) | [android.content.Intent](../android.content/Intent.md) | The intent to fire when the item is clicked. Ignored when the live folder defines a base intent. | No |
| --- | --- | --- | --- |
| [ICON_BITMAP](LiveFolders.md) | Bitmap | The icon for the item. When this column value is not null, the values for the columns [ICON_PACKAGE](LiveFolders.md) and [ICON_RESOURCE](LiveFolders.md) must be null. | No |
| [ICON_PACKAGE](LiveFolders.md) | String | The package of the item's icon. When this value is not null, the value for the column [ICON_RESOURCE](LiveFolders.md) must be specified and the value for the column [ICON_BITMAP](LiveFolders.md) must be null. | No |
| [ICON_RESOURCE](LiveFolders.md) | String | The resource name of the item's icon. When this value is not null, the value for the column [ICON_PACKAGE](LiveFolders.md) must be specified and the value for the column [ICON_BITMAP](LiveFolders.md) must be null. | No |
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CREATE_LIVE_FOLDER](LiveFolders.md) Activity Action: Creates a live folder. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DESCRIPTION](LiveFolders.md) Content provider column. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISPLAY_MODE_GRID](LiveFolders.md) Displays a live folder's content in a grid. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISPLAY_MODE_LIST](LiveFolders.md) Displays a live folder's content in a list. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_LIVE_FOLDER_BASE_INTENT](LiveFolders.md) The name of the extra used to define the base Intent of a live folder. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_LIVE_FOLDER_DISPLAY_MODE](LiveFolders.md) The name of the extra used to define the display mode of a live folder. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_LIVE_FOLDER_ICON](LiveFolders.md) The name of the extra used to define the icon of a live folder. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_LIVE_FOLDER_NAME](LiveFolders.md) The name of the extra used to define the name of a live folder. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ICON_BITMAP](LiveFolders.md) Content provider column. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ICON_PACKAGE](LiveFolders.md) Content provider column. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ICON_RESOURCE](LiveFolders.md) Content provider column. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT](LiveFolders.md) Content provider column. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NAME](LiveFolders.md) Content provider column. |

| Inherited constants ||
|---|---|
| From class [BaseColumns](BaseColumns.md) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_COUNT](BaseColumns.md) <br /> The count of rows in a directory. Type: INTEGER <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_ID](BaseColumns.md) <br /> The unique ID for a row. Type: INTEGER (long) <br /> | ||

## Constants

### ACTION_CREATE_LIVE_FOLDER

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_CREATE_LIVE_FOLDER: String
```

**Deprecated:** *Deprecated in Java.*

Activity Action: Creates a live folder.

Input: Nothing.

Output: An Intent representing the live folder. The intent must contain four extras: EXTRA_LIVE_FOLDER_NAME (value: String), EXTRA_LIVE_FOLDER_ICON (value: ShortcutIconResource), EXTRA_LIVE_FOLDER_URI (value: String) and EXTRA_LIVE_FOLDER_DISPLAY_MODE (value: int). The Intent can optionnally contain EXTRA_LIVE_FOLDER_BASE_INTENT (value: Intent). 

 Value: "android.intent.action.CREATE_LIVE_FOLDER"

**See Also**

- [#EXTRA_LIVE_FOLDER_NAME](LiveFolders.md)
- [#EXTRA_LIVE_FOLDER_ICON](LiveFolders.md)
- [#EXTRA_LIVE_FOLDER_DISPLAY_MODE](LiveFolders.md)
- [#EXTRA_LIVE_FOLDER_BASE_INTENT](LiveFolders.md)
- [android.content.Intent.ShortcutIconResource](../android/content/Intent.ShortcutIconResource.md) 

### DESCRIPTION

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DESCRIPTION: String
```

**Deprecated:** *Deprecated in Java.*

Content provider column.

Description of the live folder item. This value is ignored if the live folder's display mode is [LiveFolders.DISPLAY_MODE_GRID](LiveFolders.md).

Optional.

Type: String. 

 Value: "description"

**See Also**

- [android.provider.LiveFolders#EXTRA_LIVE_FOLDER_DISPLAY_MODE](LiveFolders.md) 

### DISPLAY_MODE_GRID

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_MODE_GRID: Int
```

**Deprecated:** *Deprecated in Java.*

Displays a live folder's content in a grid. 

 Value: 1

**See Also**

- [android.provider.LiveFolders#EXTRA_LIVE_FOLDER_DISPLAY_MODE](LiveFolders.md) 

### DISPLAY_MODE_LIST

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_MODE_LIST: Int
```

**Deprecated:** *Deprecated in Java.*

Displays a live folder's content in a list. 

 Value: 2

**See Also**

- [android.provider.LiveFolders#EXTRA_LIVE_FOLDER_DISPLAY_MODE](LiveFolders.md) 

### EXTRA_LIVE_FOLDER_BASE_INTENT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_LIVE_FOLDER_BASE_INTENT: String
```

**Deprecated:** *Deprecated in Java.*

The name of the extra used to define the base Intent of a live folder. 

 Value: "android.intent.extra.livefolder.BASE_INTENT"

**See Also**

- [#ACTION_CREATE_LIVE_FOLDER](LiveFolders.md) 

### EXTRA_LIVE_FOLDER_DISPLAY_MODE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_LIVE_FOLDER_DISPLAY_MODE: String
```

**Deprecated:** *Deprecated in Java.*

The name of the extra used to define the display mode of a live folder. 

 Value: "android.intent.extra.livefolder.DISPLAY_MODE"

**See Also**

- [#ACTION_CREATE_LIVE_FOLDER](LiveFolders.md)
- [#DISPLAY_MODE_GRID](LiveFolders.md)
- [#DISPLAY_MODE_LIST](LiveFolders.md) 

### EXTRA_LIVE_FOLDER_ICON

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_LIVE_FOLDER_ICON: String
```

**Deprecated:** *Deprecated in Java.*

The name of the extra used to define the icon of a live folder. 

 Value: "android.intent.extra.livefolder.ICON"

**See Also**

- [#ACTION_CREATE_LIVE_FOLDER](LiveFolders.md) 

### EXTRA_LIVE_FOLDER_NAME

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_LIVE_FOLDER_NAME: String
```

**Deprecated:** *Deprecated in Java.*

The name of the extra used to define the name of a live folder. 

 Value: "android.intent.extra.livefolder.NAME"

**See Also**

- [#ACTION_CREATE_LIVE_FOLDER](LiveFolders.md) 

### ICON_BITMAP

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ICON_BITMAP: String
```

**Deprecated:** *Deprecated in Java.*

Content provider column.

Icon of the live folder item, as a custom bitmap.

Optional.

Type: [android.graphics.Bitmap](../android.graphics/Bitmap.md). 

 Value: "icon_bitmap"

### ICON_PACKAGE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ICON_PACKAGE: String
```

**Deprecated:** *Deprecated in Java.*

Content provider column.

Package where to find the icon of the live folder item. This value can be obtained easily using [android.content.Intent.ShortcutIconResource#fromContext(android.content.Context, int)](../android/content/Intent.ShortcutIconResource.md)).

Optional.

Type: String. 

 Value: "icon_package"

**See Also**

- [#ICON_RESOURCE](LiveFolders.md)
- [android.content.Intent.ShortcutIconResource](../android/content/Intent.ShortcutIconResource.md) 

### ICON_RESOURCE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ICON_RESOURCE: String
```

**Deprecated:** *Deprecated in Java.*

Content provider column.

Resource name of the live folder item. This value can be obtained easily using [android.content.Intent.ShortcutIconResource#fromContext(android.content.Context, int)](../android/content/Intent.ShortcutIconResource.md)).

Optional.

Type: String. 

 Value: "icon_resource"

**See Also**

- [#ICON_PACKAGE](LiveFolders.md)
- [android.content.Intent.ShortcutIconResource](../android/content/Intent.ShortcutIconResource.md) 

### INTENT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT: String
```

**Deprecated:** *Deprecated in Java.*

Content provider column.

Intent of the live folder item.

Optional if the live folder has a base intent.

Type: [android.content.Intent](../android.content/Intent.md). 

 Value: "intent"

**See Also**

- [android.provider.LiveFolders#EXTRA_LIVE_FOLDER_BASE_INTENT](LiveFolders.md) 

### NAME

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAME: String
```

**Deprecated:** *Deprecated in Java.*

Content provider column.

Name of the live folder item.

Required.

Type: String. 

 Value: "name"
