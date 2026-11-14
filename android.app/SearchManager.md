# SearchManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SearchManager

Kotlin| [Java](https://developer.android.com/reference/android/app/SearchManager "View this page in Java") 
| --- | --- |

```
open class SearchManager : DialogInterface.OnCancelListener, DialogInterface.OnDismissListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.SearchManager](https://developer.android.com/reference/kotlin/android/app/SearchManager#) |

This class provides access to the system search services.

In practice, you won't interact with this class directly, as search services are provided through methods in [Activity](https://developer.android.com/reference/kotlin/android/app/Activity) and the [ACTION_SEARCH](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEARCH:kotlin.String) [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#).

[Configuration.UI_MODE_TYPE_WATCH](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_TYPE_WATCH:kotlin.Int) does not support this system service.
|
| ### Developer Guides
|
| For more information about using the search dialog and adding search suggestions in your application, read the [Search](https://developer.android.com/guide/topics/search/index.html) developer guide.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnCancelListener](https://developer.android.com/reference/kotlin/android/app/SearchManager.OnCancelListener) See [SearchManager.setOnCancelListener](https://developer.android.com/reference/kotlin/android/app/SearchManager#setOnCancelListener(android.app.SearchManager.OnCancelListener))for configuring your activity to monitor search UI state. |
| abstract | [OnDismissListener](https://developer.android.com/reference/kotlin/android/app/SearchManager.OnDismissListener) See [SearchManager.setOnDismissListener](https://developer.android.com/reference/kotlin/android/app/SearchManager#setOnDismissListener(android.app.SearchManager.OnDismissListener))for configuring your activity to monitor search UI state. |

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_KEY](https://developer.android.com/reference/kotlin/android/app/SearchManager#ACTION_KEY:kotlin.String) Intent extra data key: Use this key with Intent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_MSG](https://developer.android.com/reference/kotlin/android/app/SearchManager#ACTION_MSG:kotlin.String) Intent extra data key: Use this key with Intent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [APP_DATA](https://developer.android.com/reference/kotlin/android/app/SearchManager#APP_DATA:kotlin.String) Intent extra data key: Use this key with Intent. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CURSOR_EXTRA_KEY_IN_PROGRESS](https://developer.android.com/reference/kotlin/android/app/SearchManager#CURSOR_EXTRA_KEY_IN_PROGRESS:kotlin.String) Boolean extra data key for a suggestion provider to return in [Cursor.getExtras](https://developer.android.com/reference/kotlin/android/database/Cursor.html#getExtras())to indicate that the search is not complete yet. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DATA_KEY](https://developer.android.com/reference/kotlin/android/app/SearchManager#EXTRA_DATA_KEY:kotlin.String) Intent extra data key: This key will be used for the extra populated by the [SUGGEST_COLUMN_INTENT_EXTRA_DATA](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_INTENT_EXTRA_DATA:kotlin.String) column. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_NEW_SEARCH](https://developer.android.com/reference/kotlin/android/app/SearchManager#EXTRA_NEW_SEARCH:kotlin.String) Boolean extra data key for [Intent.ACTION_WEB_SEARCH](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_WEB_SEARCH:kotlin.String) intents. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SELECT_QUERY](https://developer.android.com/reference/kotlin/android/app/SearchManager#EXTRA_SELECT_QUERY:kotlin.String) Boolean extra data key for [INTENT_ACTION_GLOBAL_SEARCH](https://developer.android.com/reference/kotlin/android/app/SearchManager#INTENT_ACTION_GLOBAL_SEARCH:kotlin.String) intents. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_WEB_SEARCH_PENDINGINTENT](https://developer.android.com/reference/kotlin/android/app/SearchManager#EXTRA_WEB_SEARCH_PENDINGINTENT:kotlin.String) Extra data key for [Intent.ACTION_WEB_SEARCH](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_WEB_SEARCH:kotlin.String). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_QUERY_REFINEMENT](https://developer.android.com/reference/kotlin/android/app/SearchManager#FLAG_QUERY_REFINEMENT:kotlin.Int) Flag to specify that the entry can be used for query refinement, i. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_ACTION_GLOBAL_SEARCH](https://developer.android.com/reference/kotlin/android/app/SearchManager#INTENT_ACTION_GLOBAL_SEARCH:kotlin.String) Intent action for starting the global search activity. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_ACTION_SEARCHABLES_CHANGED](https://developer.android.com/reference/kotlin/android/app/SearchManager#INTENT_ACTION_SEARCHABLES_CHANGED:kotlin.String) Intent action broadcasted to inform that the searchables list or default have changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_ACTION_SEARCH_SETTINGS](https://developer.android.com/reference/kotlin/android/app/SearchManager#INTENT_ACTION_SEARCH_SETTINGS:kotlin.String) Intent action for starting the global search settings activity. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_ACTION_SEARCH_SETTINGS_CHANGED](https://developer.android.com/reference/kotlin/android/app/SearchManager#INTENT_ACTION_SEARCH_SETTINGS_CHANGED:kotlin.String) Intent action broadcasted to inform that the search settings have changed in some way. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_ACTION_WEB_SEARCH_SETTINGS](https://developer.android.com/reference/kotlin/android/app/SearchManager#INTENT_ACTION_WEB_SEARCH_SETTINGS:kotlin.String) Intent action for starting a web search provider's settings activity. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_GLOBAL_SEARCH_ACTIVITY_CHANGED](https://developer.android.com/reference/kotlin/android/app/SearchManager#INTENT_GLOBAL_SEARCH_ACTIVITY_CHANGED:kotlin.String) Intent action to be broadcast to inform that the global search provider has changed. |
| --- | --- |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [MENU_KEY](https://developer.android.com/reference/kotlin/android/app/SearchManager#MENU_KEY:kotlin.Char) This is a shortcut definition for the default menu key to use for invoking search. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MENU_KEYCODE](https://developer.android.com/reference/kotlin/android/app/SearchManager#MENU_KEYCODE:kotlin.Int) This is a shortcut definition for the default menu key to use for invoking search. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [QUERY](https://developer.android.com/reference/kotlin/android/app/SearchManager#QUERY:kotlin.String) Intent extra data key: Use this key with [content.Intent.getStringExtra()](https://developer.android.com/reference/kotlin/android/content/Intent.html#getStringExtra(kotlin.String))to obtain the query string from Intent. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SHORTCUT_MIME_TYPE](https://developer.android.com/reference/kotlin/android/app/SearchManager#SHORTCUT_MIME_TYPE:kotlin.String) MIME type for shortcut validation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_AUDIO_CHANNEL_CONFIG](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_AUDIO_CHANNEL_CONFIG:kotlin.String) Column name for suggestions cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_CONTENT_TYPE:kotlin.String) Column name for suggestions cursor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_DURATION](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_DURATION:kotlin.String) Column name for suggestions cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_FLAGS](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_FLAGS:kotlin.String) Column name for suggestions cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_FORMAT](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_FORMAT:kotlin.String) Column name for suggestions cursor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_ICON_1](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_ICON_1:kotlin.String) Column name for suggestions cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_ICON_2](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_ICON_2:kotlin.String) Column name for suggestions cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_INTENT_ACTION](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_INTENT_ACTION:kotlin.String) Column name for suggestions cursor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_INTENT_DATA](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_INTENT_DATA:kotlin.String) Column name for suggestions cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_INTENT_DATA_ID](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_INTENT_DATA_ID:kotlin.String) Column name for suggestions cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_INTENT_EXTRA_DATA](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_INTENT_EXTRA_DATA:kotlin.String) Column name for suggestions cursor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_IS_LIVE](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_IS_LIVE:kotlin.String) Column name for suggestions cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_LAST_ACCESS_HINT](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_LAST_ACCESS_HINT:kotlin.String) Column name for suggestions cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_PRODUCTION_YEAR](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_PRODUCTION_YEAR:kotlin.String) Column name for suggestions cursor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_PURCHASE_PRICE](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_PURCHASE_PRICE:kotlin.String) Column name for suggestions cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_QUERY](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_QUERY:kotlin.String) Column name for suggestions cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_RATING_SCORE](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_RATING_SCORE:kotlin.String) Column name for suggestions cursor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_RATING_STYLE](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_RATING_STYLE:kotlin.String) Column name for suggestions cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_RENTAL_PRICE](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_RENTAL_PRICE:kotlin.String) Column name for suggestions cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_RESULT_CARD_IMAGE](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_RESULT_CARD_IMAGE:kotlin.String) Column name for suggestions cursor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_SHORTCUT_ID](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_SHORTCUT_ID:kotlin.String) Column name for suggestions cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_SPINNER_WHILE_REFRESHING](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_SPINNER_WHILE_REFRESHING:kotlin.String) Column name for suggestions cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_TEXT_1](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_TEXT_1:kotlin.String) Column name for suggestions cursor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_TEXT_2](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_TEXT_2:kotlin.String) Column name for suggestions cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_TEXT_2_URL](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_TEXT_2_URL:kotlin.String) Column name for suggestions cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_VIDEO_HEIGHT](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_VIDEO_HEIGHT:kotlin.String) Column name for suggestions cursor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_COLUMN_VIDEO_WIDTH](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_VIDEO_WIDTH:kotlin.String) Column name for suggestions cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_MIME_TYPE](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_MIME_TYPE:kotlin.String) MIME type for suggestions data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_NEVER_MAKE_SHORTCUT](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_NEVER_MAKE_SHORTCUT:kotlin.String) Column value for suggestion column [SUGGEST_COLUMN_SHORTCUT_ID](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_SHORTCUT_ID:kotlin.String) when a suggestion should not be stored as a shortcut in global search. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_PARAMETER_LIMIT](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_PARAMETER_LIMIT:kotlin.String) Query parameter added to suggestion queries to limit the number of suggestions returned. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_URI_PATH_QUERY](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_URI_PATH_QUERY:kotlin.String) Uri path for queried suggestions data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGEST_URI_PATH_SHORTCUT](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_URI_PATH_SHORTCUT:kotlin.String) Uri path for shortcut validation. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [USER_QUERY](https://developer.android.com/reference/kotlin/android/app/SearchManager#USER_QUERY:kotlin.String) Intent extra data key: Use this key with [content.Intent.getStringExtra()](https://developer.android.com/reference/kotlin/android/content/Intent.html#getStringExtra(kotlin.String))to obtain the query string typed in by the user. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)! | [getGlobalSearchActivity](https://developer.android.com/reference/kotlin/android/app/SearchManager#getGlobalSearchActivity())`()` Gets the name of the global search activity. |
| open [SearchableInfo](https://developer.android.com/reference/kotlin/android/app/SearchableInfo)! | [getSearchableInfo](https://developer.android.com/reference/kotlin/android/app/SearchManager#getSearchableInfo(android.content.ComponentName))`(`componentName:` ` [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!`)` Gets information about a searchable activity. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SearchableInfo](https://developer.android.com/reference/kotlin/android/app/SearchableInfo)!\>! | [getSearchablesInGlobalSearch](https://developer.android.com/reference/kotlin/android/app/SearchManager#getSearchablesInGlobalSearch())`()` Returns a list of the searchable activities that can be included in global search. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCancel](https://developer.android.com/reference/kotlin/android/app/SearchManager#onCancel(android.content.DialogInterface))`(`dialog:` ` [DialogInterface](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDismiss](https://developer.android.com/reference/kotlin/android/app/SearchManager#onDismiss(android.content.DialogInterface))`(`dialog:` ` [DialogInterface](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnCancelListener](https://developer.android.com/reference/kotlin/android/app/SearchManager#setOnCancelListener(android.app.SearchManager.OnCancelListener))`(`listener:` ` [SearchManager.OnCancelListener](https://developer.android.com/reference/kotlin/android/app/SearchManager.OnCancelListener)!`)` Set or clear the callback that will be invoked whenever the search UI is canceled. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnDismissListener](https://developer.android.com/reference/kotlin/android/app/SearchManager#setOnDismissListener(android.app.SearchManager.OnDismissListener))`(`listener:` ` [SearchManager.OnDismissListener](https://developer.android.com/reference/kotlin/android/app/SearchManager.OnDismissListener)!`)` Set or clear the callback that will be invoked whenever the search UI is dismissed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startSearch](https://developer.android.com/reference/kotlin/android/app/SearchManager#startSearch(kotlin.String,%20kotlin.Boolean,%20android.content.ComponentName,%20android.os.Bundle,%20kotlin.Boolean))`(`initialQuery:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `selectInitialQuery:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `launchActivity:` ` [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!`, `appSearchData:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`, `globalSearch:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Launch search UI. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopSearch](https://developer.android.com/reference/kotlin/android/app/SearchManager#stopSearch())`()` Terminate search UI. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [triggerSearch](https://developer.android.com/reference/kotlin/android/app/SearchManager#triggerSearch(kotlin.String,%20android.content.ComponentName,%20android.os.Bundle))`(`query:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `launchActivity:` ` [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!`, `appSearchData:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Similar to [startSearch](https://developer.android.com/reference/kotlin/android/app/SearchManager#startSearch(kotlin.String,%20kotlin.Boolean,%20android.content.ComponentName,%20android.os.Bundle,%20kotlin.Boolean))but actually fires off the search query after invoking the search dialog. |

## Constants

### ACTION_KEY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_KEY: String
```

Intent extra data key: Use this key with Intent.ACTION_SEARCH and [content.Intent.getIntExtra()](https://developer.android.com/reference/kotlin/android/content/Intent.html#getIntExtra(kotlin.String,%20kotlin.Int))to obtain the keycode that the user used to trigger this query. It will be zero if the user simply pressed the "GO" button on the search UI. This is primarily used in conjunction with the keycode attribute in the actionkey element of your searchable.xml configuration file. 

 Value: "action_key"

### ACTION_MSG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_MSG: String
```

Intent extra data key: Use this key with Intent.ACTION_SEARCH and [content.Intent.getStringExtra()](https://developer.android.com/reference/kotlin/android/content/Intent.html#getStringExtra(kotlin.String))to obtain the action message that was defined for a particular search action key and/or suggestion. It will be null if the search was launched by typing "enter", touching the "GO" button, or other means not involving any action key. 

 Value: "action_msg"

### APP_DATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_DATA: String
```

Intent extra data key: Use this key with Intent.ACTION_SEARCH and [content.Intent.getBundleExtra()](https://developer.android.com/reference/kotlin/android/content/Intent.html#getBundleExtra(kotlin.String))to obtain any additional app-specific data that was inserted by the activity that launched the search. 

 Value: "app_data"

### CURSOR_EXTRA_KEY_IN_PROGRESS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CURSOR_EXTRA_KEY_IN_PROGRESS: String
```

Boolean extra data key for a suggestion provider to return in [Cursor.getExtras](https://developer.android.com/reference/kotlin/android/database/Cursor.html#getExtras())to indicate that the search is not complete yet. This can be used by the search UI to indicate that a search is in progress. The suggestion provider can return partial results this way and send a change notification on the cursor when more results are available. 

 Value: "in_progress"

### EXTRA_DATA_KEY

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_DATA_KEY: String
```

Intent extra data key: This key will be used for the extra populated by the [SUGGEST_COLUMN_INTENT_EXTRA_DATA](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_INTENT_EXTRA_DATA:kotlin.String) column. 

 Value: "intent_extra_data_key"

### EXTRA_NEW_SEARCH

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_NEW_SEARCH: String
```

Boolean extra data key for [Intent.ACTION_WEB_SEARCH](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_WEB_SEARCH:kotlin.String) intents. If`true`, this search should open a new browser window, rather than using an existing one. 

 Value: "new_search"

### EXTRA_SELECT_QUERY

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SELECT_QUERY: String
```

Boolean extra data key for [INTENT_ACTION_GLOBAL_SEARCH](https://developer.android.com/reference/kotlin/android/app/SearchManager#INTENT_ACTION_GLOBAL_SEARCH:kotlin.String) intents. If`true`, the initial query should be selected when the global search activity is started, so that the user can easily replace it with another query. 

 Value: "select_query"

### EXTRA_WEB_SEARCH_PENDINGINTENT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_WEB_SEARCH_PENDINGINTENT: String
```

Extra data key for [Intent.ACTION_WEB_SEARCH](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_WEB_SEARCH:kotlin.String). If set, the value must be a [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent). The search activity handling the [Intent.ACTION_WEB_SEARCH](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_WEB_SEARCH:kotlin.String) intent will fill in and launch the pending intent. The data URI will be filled in with an http or https URI, and [android.provider.Browser#EXTRA_HEADERS](https://developer.android.com/reference/kotlin/android/provider/Browser.html#EXTRA_HEADERS:kotlin.String) may be filled in. 

 Value: "web_search_pendingintent"

### FLAG_QUERY_REFINEMENT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_QUERY_REFINEMENT: Int
```

Flag to specify that the entry can be used for query refinement, i.e., the query text in the search field can be replaced with the text in this entry, when a query refinement icon is clicked. The suggestion list should show such a clickable icon beside the entry.

Use this flag as a bit-field for [SUGGEST_COLUMN_FLAGS](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_FLAGS:kotlin.String). 

 Value: 1

### INTENT_ACTION_GLOBAL_SEARCH

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_ACTION_GLOBAL_SEARCH: String
```

Intent action for starting the global search activity. The global search provider should handle this intent. Supported extra data keys: [QUERY](https://developer.android.com/reference/kotlin/android/app/SearchManager#QUERY:kotlin.String), [EXTRA_SELECT_QUERY](https://developer.android.com/reference/kotlin/android/app/SearchManager#EXTRA_SELECT_QUERY:kotlin.String), [APP_DATA](https://developer.android.com/reference/kotlin/android/app/SearchManager#APP_DATA:kotlin.String). 

 Value: "android.search.action.GLOBAL_SEARCH"

### INTENT_ACTION_SEARCHABLES_CHANGED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_ACTION_SEARCHABLES_CHANGED: String
```

Intent action broadcasted to inform that the searchables list or default have changed. Components should handle this intent if they cache any searchable data and wish to stay up to date on changes. 

 Value: "android.search.action.SEARCHABLES_CHANGED"

### INTENT_ACTION_SEARCH_SETTINGS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_ACTION_SEARCH_SETTINGS: String
```

Intent action for starting the global search settings activity. The global search provider should handle this intent. 

 Value: "android.search.action.SEARCH_SETTINGS"

### INTENT_ACTION_SEARCH_SETTINGS_CHANGED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_ACTION_SEARCH_SETTINGS_CHANGED: String
```

Intent action broadcasted to inform that the search settings have changed in some way. Either searchables have been enabled or disabled, or a different web search provider has been chosen. 

 Value: "android.search.action.SETTINGS_CHANGED"

### INTENT_ACTION_WEB_SEARCH_SETTINGS

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_ACTION_WEB_SEARCH_SETTINGS: String
```

Intent action for starting a web search provider's settings activity. Web search providers should handle this intent if they have provider-specific settings to implement. 

 Value: "android.search.action.WEB_SEARCH_SETTINGS"

### INTENT_GLOBAL_SEARCH_ACTIVITY_CHANGED

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_GLOBAL_SEARCH_ACTIVITY_CHANGED: String
```

Intent action to be broadcast to inform that the global search provider has changed. 

 Value: "android.search.action.GLOBAL_SEARCH_ACTIVITY_CHANGED"

### MENU_KEY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MENU_KEY: Char
```

This is a shortcut definition for the default menu key to use for invoking search. See Menu.Item.setAlphabeticShortcut() for more information. 

 Value: 's'

### MENU_KEYCODE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MENU_KEYCODE: Int
```

This is a shortcut definition for the default menu key to use for invoking search. See Menu.Item.setAlphabeticShortcut() for more information. 

 Value: 47

### QUERY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERY: String
```

Intent extra data key: Use this key with [content.Intent.getStringExtra()](https://developer.android.com/reference/kotlin/android/content/Intent.html#getStringExtra(kotlin.String))to obtain the query string from Intent.ACTION_SEARCH. 

 Value: "query"

### SHORTCUT_MIME_TYPE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHORTCUT_MIME_TYPE: String
```

MIME type for shortcut validation. You'll use this in your suggestions content provider in the getType() function. 

 Value: "vnd.android.cursor.item/vnd.android.search.suggest"

### SUGGEST_COLUMN_AUDIO_CHANNEL_CONFIG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_AUDIO_CHANNEL_CONFIG: String
```

Column name for suggestions cursor.*Optional.*If your content contains audio, you should provide this column to specify the audio channel configuration. The data in the column is string with format like "channels.subchannels" such as "1.0" or "5.1". 

 Value: "suggest_audio_channel_config"

### SUGGEST_COLUMN_CONTENT_TYPE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_CONTENT_TYPE: String
```

Column name for suggestions cursor.*Optional.*If your content is media type, you should provide this column so search app could understand more about your content. The data in the column must specify the MIME type of the content. 

 Value: "suggest_content_type"

### SUGGEST_COLUMN_DURATION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_DURATION: String
```

Column name for suggestions cursor.*Optional.*If your content is video or audio, you should provide this column to specify the duration of your content in milliseconds. The data in the column is of long type. 

 Value: "suggest_duration"

### SUGGEST_COLUMN_FLAGS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_FLAGS: String
```

Column name for suggestions cursor.*Optional.*This column is used to specify additional flags per item. Multiple flags can be specified.

Must be one of [FLAG_QUERY_REFINEMENT](https://developer.android.com/reference/kotlin/android/app/SearchManager#FLAG_QUERY_REFINEMENT:kotlin.Int) or 0 to indicate no flags. 

 Value: "suggest_flags"

### SUGGEST_COLUMN_FORMAT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_FORMAT: String
```

Column name for suggestions cursor.*Unused - can be null or column can be omitted.* 

 Value: "suggest_format"

### SUGGEST_COLUMN_ICON_1

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_ICON_1: String
```

Column name for suggestions cursor.*Optional.*If your cursor includes this column, then all suggestions will be provided in a format that includes space for two small icons, one at the left and one at the right of each suggestion. The data in the column must be a resource ID of a drawable, or a URI in one of the following formats:

- content ([android.content.ContentResolver#SCHEME_CONTENT](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_CONTENT:kotlin.String))
- android.resource ([android.content.ContentResolver#SCHEME_ANDROID_RESOURCE](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_ANDROID_RESOURCE:kotlin.String))
- file ([android.content.ContentResolver#SCHEME_FILE](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_FILE:kotlin.String))

See [android.content.ContentResolver#openAssetFileDescriptor(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openAssetFileDescriptor(android.net.Uri,%20kotlin.String))for more information on these schemes.

<br />

 Value: "suggest_icon_1"

### SUGGEST_COLUMN_ICON_2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_ICON_2: String
```

Column name for suggestions cursor.*Optional.*If your cursor includes this column, then all suggestions will be provided in a format that includes space for two small icons, one at the left and one at the right of each suggestion. The data in the column must be a resource ID of a drawable, or a URI in one of the following formats:

- content ([android.content.ContentResolver#SCHEME_CONTENT](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_CONTENT:kotlin.String))
- android.resource ([android.content.ContentResolver#SCHEME_ANDROID_RESOURCE](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_ANDROID_RESOURCE:kotlin.String))
- file ([android.content.ContentResolver#SCHEME_FILE](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_FILE:kotlin.String))

See [android.content.ContentResolver#openAssetFileDescriptor(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openAssetFileDescriptor(android.net.Uri,%20kotlin.String))for more information on these schemes.

<br />

 Value: "suggest_icon_2"

### SUGGEST_COLUMN_INTENT_ACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_INTENT_ACTION: String
```

Column name for suggestions cursor.*Optional.* If this column exists*and* this element exists at the given row, this is the action that will be used when forming the suggestion's intent. If the element is not provided, the action will be taken from the android:searchSuggestIntentAction field in your XML metadata.*At least one of these must be present for the suggestion to generate an intent.*Note: If your action is the same for all suggestions, it is more efficient to specify it using XML metadata and omit it from the cursor. 

 Value: "suggest_intent_action"

### SUGGEST_COLUMN_INTENT_DATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_INTENT_DATA: String
```

Column name for suggestions cursor.*Optional.* If this column exists*and*this element exists at the given row, this is the data that will be used when forming the suggestion's intent. If the element is not provided, the data will be taken from the android:searchSuggestIntentData field in your XML metadata. If neither source is provided, the Intent's data field will be null. Note: If your data is the same for all suggestions, or can be described using a constant part and a specific ID, it is more efficient to specify it using XML metadata and omit it from the cursor. 

 Value: "suggest_intent_data"

### SUGGEST_COLUMN_INTENT_DATA_ID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_INTENT_DATA_ID: String
```

Column name for suggestions cursor.*Optional.* If this column exists*and*this element exists at the given row, then "/" and this value will be appended to the data field in the Intent. This should only be used if the data field has already been set to an appropriate base string. 

 Value: "suggest_intent_data_id"

### SUGGEST_COLUMN_INTENT_EXTRA_DATA

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_INTENT_EXTRA_DATA: String
```

Column name for suggestions cursor.*Optional.* If this column exists*and* this element exists at the given row, this is the data that will be used when forming the suggestion's intent. If not provided, the Intent's extra data field will be null. This column allows suggestions to provide additional arbitrary data which will be included as an extra under the key [EXTRA_DATA_KEY](https://developer.android.com/reference/kotlin/android/app/SearchManager#EXTRA_DATA_KEY:kotlin.String). 

 Value: "suggest_intent_extra_data"

### SUGGEST_COLUMN_IS_LIVE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_IS_LIVE: String
```

Column name for suggestions cursor.*Optional.*If your content is media type, you should provide this column to specify whether your content is live media such as live video or live audio. The value in the column is of integer type with value of either 0 indicating non-live content or 1 indicating live content. 

 Value: "suggest_is_live"

### SUGGEST_COLUMN_LAST_ACCESS_HINT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_LAST_ACCESS_HINT: String
```

Column name for suggestions cursor.*Optional.* This column may be used to specify the time in [System.currentTImeMillis()](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis())(wall time in UTC) when an item was last accessed within the results-providing application. If set, this may be used to show more-recently-used items first. 

 Value: "suggest_last_access_hint"

### SUGGEST_COLUMN_PRODUCTION_YEAR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_PRODUCTION_YEAR: String
```

Column name for suggestions cursor.*Optional.*If your content is video or audio and has a known production year, you should provide this column to specify the production year of your content. The data in the column is of integer type. 

 Value: "suggest_production_year"

### SUGGEST_COLUMN_PURCHASE_PRICE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_PURCHASE_PRICE: String
```

Column name for suggestions cursor.*Optional.*If your content is purchasable, you should provide this column to specify the displayable string representation of the purchase price of your content including the currency and the amount. If it's free, you should provide localized string to specify that it's free. This column can be omitted if the content is not applicable to purchase. 

 Value: "suggest_purchase_price"

### SUGGEST_COLUMN_QUERY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_QUERY: String
```

Column name for suggestions cursor.*Required if action is [ACTION_SEARCH](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEARCH:kotlin.String), optional otherwise.* If this column exists*and*this element exists at the given row, this is the data that will be used when forming the suggestion's query. 

 Value: "suggest_intent_query"

### SUGGEST_COLUMN_RATING_SCORE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_RATING_SCORE: String
```

Column name for suggestions cursor.*Optional.* If your content has a rating, you should provide this column to specify the rating score of your content. The data in the column is of float type. See [android.media.Rating](https://developer.android.com/reference/kotlin/android/media/Rating.html#) about valid rating scores for each rating style. 

 Value: "suggest_rating_score"

### SUGGEST_COLUMN_RATING_STYLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_RATING_STYLE: String
```

Column name for suggestions cursor.*Optional.* If your content has a rating, you should provide this column to specify the rating style of your content. The data in the column must be one of the constant values specified in [android.media.Rating](https://developer.android.com/reference/kotlin/android/media/Rating.html#) 

 Value: "suggest_rating_style"

### SUGGEST_COLUMN_RENTAL_PRICE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_RENTAL_PRICE: String
```

Column name for suggestions cursor.*Optional.*If your content is rentable, you should provide this column to specify the displayable string representation of the rental price of your content including the currency and the amount. If it's free, you should provide localized string to specify that it's free. This column can be omitted if the content is not applicable to rent. 

 Value: "suggest_rental_price"

### SUGGEST_COLUMN_RESULT_CARD_IMAGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_RESULT_CARD_IMAGE: String
```

Column name for suggestions cursor.*Optional.*If your cursor includes this column, then the image will be displayed when forming the suggestion. The suggested dimension for the image is 270x400 px for portrait mode and 400x225 px for landscape mode. The data in the column must be a resource ID of a drawable, or a URI in one of the following formats:

- content ([android.content.ContentResolver#SCHEME_CONTENT](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_CONTENT:kotlin.String))
- android.resource ([android.content.ContentResolver#SCHEME_ANDROID_RESOURCE](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_ANDROID_RESOURCE:kotlin.String))
- file ([android.content.ContentResolver#SCHEME_FILE](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#SCHEME_FILE:kotlin.String))

See [android.content.ContentResolver#openAssetFileDescriptor(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openAssetFileDescriptor(android.net.Uri,%20kotlin.String))for more information on these schemes.

<br />

 Value: "suggest_result_card_image"

### SUGGEST_COLUMN_SHORTCUT_ID

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_SHORTCUT_ID: String
```

Column name for suggestions cursor.*Optional.* This column is used to indicate whether a search suggestion should be stored as a shortcut, and whether it should be refreshed. If missing, the result will be stored as a shortcut and never validated. If set to [SUGGEST_NEVER_MAKE_SHORTCUT](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_NEVER_MAKE_SHORTCUT:kotlin.String), the result will not be stored as a shortcut. Otherwise, the shortcut id will be used to check back for an up to date suggestion using [SUGGEST_URI_PATH_SHORTCUT](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_URI_PATH_SHORTCUT:kotlin.String). 

 Value: "suggest_shortcut_id"

### SUGGEST_COLUMN_SPINNER_WHILE_REFRESHING

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_SPINNER_WHILE_REFRESHING: String
```

Column name for suggestions cursor.*Optional.*This column is used to specify that a spinner should be shown in lieu of an icon2 while the shortcut of this suggestion is being refreshed. 

 Value: "suggest_spinner_while_refreshing"

### SUGGEST_COLUMN_TEXT_1

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_TEXT_1: String
```

Column name for suggestions cursor.*Required.*This is the primary line of text that will be presented to the user as the suggestion. 

 Value: "suggest_text_1"

### SUGGEST_COLUMN_TEXT_2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_TEXT_2: String
```

Column name for suggestions cursor.*Optional.*If your cursor includes this column, then all suggestions will be provided in a two-line format. The second line of text is in a much smaller appearance. 

 Value: "suggest_text_2"

### SUGGEST_COLUMN_TEXT_2_URL

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_TEXT_2_URL: String
```

Column name for suggestions cursor.*Optional.* This is a URL that will be shown as the second line of text instead of [SUGGEST_COLUMN_TEXT_2](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_TEXT_2:kotlin.String). This is a separate column so that the search UI knows to display the text as a URL, e.g. by using a different color. If this column is absent, or has the value`null`, [SUGGEST_COLUMN_TEXT_2](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_TEXT_2:kotlin.String) will be used instead. 

 Value: "suggest_text_2_url"

### SUGGEST_COLUMN_VIDEO_HEIGHT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_VIDEO_HEIGHT: String
```

Column name for suggestions cursor.*Optional.*If your content is video, you should provide this column to specify the number of horizontal lines. The data in the column is of integer type. 

 Value: "suggest_video_height"

### SUGGEST_COLUMN_VIDEO_WIDTH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_COLUMN_VIDEO_WIDTH: String
```

Column name for suggestions cursor.*Optional.*If your content is video, you should provide this column to specify the number of vertical lines. The data in the column is of integer type. 

 Value: "suggest_video_width"

### SUGGEST_MIME_TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_MIME_TYPE: String
```

MIME type for suggestions data. You'll use this in your suggestions content provider in the getType() function. 

 Value: "vnd.android.cursor.dir/vnd.android.search.suggest"

### SUGGEST_NEVER_MAKE_SHORTCUT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_NEVER_MAKE_SHORTCUT: String
```

Column value for suggestion column [SUGGEST_COLUMN_SHORTCUT_ID](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_SHORTCUT_ID:kotlin.String) when a suggestion should not be stored as a shortcut in global search. 

 Value: "_-1"

### SUGGEST_PARAMETER_LIMIT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_PARAMETER_LIMIT: String
```

Query parameter added to suggestion queries to limit the number of suggestions returned. This limit is only advisory and suggestion providers may chose to ignore it. 

 Value: "limit"

### SUGGEST_URI_PATH_QUERY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_URI_PATH_QUERY: String
```

Uri path for queried suggestions data. This is the path that the search manager will use when querying your content provider for suggestions data based on user input (e.g. looking for partial matches). Typically you'll use this with a URI matcher. 

 Value: "search_suggest_query"

### SUGGEST_URI_PATH_SHORTCUT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGEST_URI_PATH_SHORTCUT: String
```

Uri path for shortcut validation. This is the path that the search manager will use when querying your content provider to refresh a shortcutted suggestion result and to check if it is still valid. When asked, a source may return an up to date result, or no result. No result indicates the shortcut refers to a no longer valid sugggestion. 

 Value: "search_suggest_shortcut"

**See Also**

- [#SUGGEST_COLUMN_SHORTCUT_ID](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_SHORTCUT_ID:kotlin.String) 

### USER_QUERY

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USER_QUERY: String
```

Intent extra data key: Use this key with [content.Intent.getStringExtra()](https://developer.android.com/reference/kotlin/android/content/Intent.html#getStringExtra(kotlin.String))to obtain the query string typed in by the user. This may be different from the value of [QUERY](https://developer.android.com/reference/kotlin/android/app/SearchManager#QUERY:kotlin.String) if the intent is the result of selecting a suggestion. In that case, [QUERY](https://developer.android.com/reference/kotlin/android/app/SearchManager#QUERY:kotlin.String) will contain the value of [SUGGEST_COLUMN_QUERY](https://developer.android.com/reference/kotlin/android/app/SearchManager#SUGGEST_COLUMN_QUERY:kotlin.String) for the suggestion, and [USER_QUERY](https://developer.android.com/reference/kotlin/android/app/SearchManager#USER_QUERY:kotlin.String) will contain the string typed by the user. 

 Value: "user_query"

## Public methods

### getGlobalSearchActivity

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGlobalSearchActivity(): ComponentName!
```

Gets the name of the global search activity. 

### getSearchableInfo

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSearchableInfo(componentName: ComponentName!): SearchableInfo!
```

Gets information about a searchable activity.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `componentName` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!:The activity to get searchable information for. |

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [SearchableInfo](https://developer.android.com/reference/kotlin/android/app/SearchableInfo)! | Searchable information, or`null`if the activity does not exist, or is not searchable. |

### getSearchablesInGlobalSearch

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSearchablesInGlobalSearch(): MutableList<SearchableInfo!>!
```

Returns a list of the searchable activities that can be included in global search.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [SearchableInfo](https://developer.android.com/reference/kotlin/android/app/SearchableInfo)!>! | a list containing searchable information for all searchable activities that have the`android:includeInGlobalSearch`attribute set in their searchable meta-data. |

### onCancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCancel(dialog: DialogInterface!): Unit
```

**Deprecated:** *This method is an obsolete internal implementation detail. Do not use.*

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dialog` | [DialogInterface](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#)!:the dialog that was canceled will be passed into the method |

### onDismiss

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDismiss(dialog: DialogInterface!): Unit
```

**Deprecated:** *This method is an obsolete internal implementation detail. Do not use.*

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dialog` | [DialogInterface](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#)!:the dialog that was dismissed will be passed into the method |

### setOnCancelListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnCancelListener(listener: SearchManager.OnCancelListener!): Unit
```

Set or clear the callback that will be invoked whenever the search UI is canceled.

[Configuration.UI_MODE_TYPE_TELEVISION](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_TYPE_TELEVISION:kotlin.Int) does not support this method.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SearchManager.OnCancelListener](https://developer.android.com/reference/kotlin/android/app/SearchManager.OnCancelListener)!:The [OnCancelListener](https://developer.android.com/reference/kotlin/android/app/SearchManager.OnCancelListener) to use, or null. |

### setOnDismissListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnDismissListener(listener: SearchManager.OnDismissListener!): Unit
```

Set or clear the callback that will be invoked whenever the search UI is dismissed.

[Configuration.UI_MODE_TYPE_TELEVISION](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_TYPE_TELEVISION:kotlin.Int) does not support this method.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [SearchManager.OnDismissListener](https://developer.android.com/reference/kotlin/android/app/SearchManager.OnDismissListener)!:The [OnDismissListener](https://developer.android.com/reference/kotlin/android/app/SearchManager.OnDismissListener) to use, or null. |

### startSearch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startSearch(
    initialQuery: String!, 
    selectInitialQuery: Boolean, 
    launchActivity: ComponentName!, 
    appSearchData: Bundle!, 
    globalSearch: Boolean
): Unit
```

Launch search UI.

The search manager will open a search widget in an overlapping window, and the underlying activity may be obscured. The search entry state will remain in effect until one of the following events:

- The user completes the search. In most cases this will launch a search intent.
- The user uses the back, home, or other keys to exit the search.
- The application calls the [stopSearch](https://developer.android.com/reference/kotlin/android/app/SearchManager#stopSearch())method, which will hide the search window and return focus to the activity from which it was launched.
- Most applications will*not* use this interface to invoke search. The primary method for invoking search is to call android.app.Activity#onSearchRequested or [Activity.startSearch()](https://developer.android.com/reference/kotlin/android/app/Activity#startSearch(kotlin.String,%20kotlin.Boolean,%20android.os.Bundle,%20kotlin.Boolean)).

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `initialQuery` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A search string can be pre-entered here, but this is typically null or empty. |
| `selectInitialQuery` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true, the initial query will be preselected, which means that any further typing will replace it. This is useful for cases where an entire pre-formed query is being inserted. If false, the selection point will be placed at the end of the inserted query. This is useful when the inserted query is text that the user entered, and the user would expect to be able to keep typing.*This parameter is only meaningful if initialQuery is a non-empty string.* |
| `launchActivity` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!:The ComponentName of the activity that has launched this search. |
| --- | --- |
| `appSearchData` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:An application can insert application-specific context here, in order to improve quality or specificity of its own searches. This data will be returned with SEARCH intent(s). Null if no extra data is required. |
| `globalSearch` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If false, this will only launch the search that has been specifically defined by the application (which is usually defined as a local search). If no default search is defined in the current application or activity, global search will be launched. If true, this will always launch a platform-global (e.g. web-based) search instead. |

**See Also**

- [#stopSearch](https://developer.android.com/reference/kotlin/android/app/SearchManager#stopSearch()) 

### stopSearch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stopSearch(): Unit
```

Terminate search UI.

Typically the user will terminate the search UI by launching a search or by canceling. This function allows the underlying application or activity to cancel the search prematurely (for any reason).

This function can be safely called at any time (even if no search is active.)

[Configuration.UI_MODE_TYPE_TELEVISION](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#UI_MODE_TYPE_TELEVISION:kotlin.Int) does not support this method. 
**See Also**

- [#startSearch](https://developer.android.com/reference/kotlin/android/app/SearchManager#startSearch(kotlin.String,%20kotlin.Boolean,%20android.content.ComponentName,%20android.os.Bundle,%20kotlin.Boolean)) 

### triggerSearch

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun triggerSearch(
    query: String!, 
    launchActivity: ComponentName!, 
    appSearchData: Bundle!
): Unit
```

Similar to [startSearch](https://developer.android.com/reference/kotlin/android/app/SearchManager#startSearch(kotlin.String,%20kotlin.Boolean,%20android.content.ComponentName,%20android.os.Bundle,%20kotlin.Boolean))but actually fires off the search query after invoking the search dialog. Made available for testing purposes.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `query` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The query to trigger. If empty, request will be ignored. |
| `launchActivity` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!:The ComponentName of the activity that has launched this search. |
| `appSearchData` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:An application can insert application-specific context here, in order to improve quality or specificity of its own searches. This data will be returned with SEARCH intent(s). Null if no extra data is required. |
| --- | --- |

**See Also**

- [#startSearch](https://developer.android.com/reference/kotlin/android/app/SearchManager#startSearch(kotlin.String,%20kotlin.Boolean,%20android.content.ComponentName,%20android.os.Bundle,%20kotlin.Boolean))
