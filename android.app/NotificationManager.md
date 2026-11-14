Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NotificationManager

```
open class NotificationManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.NotificationManager](NotificationManager.md) |

Class to notify the user of events that happen. This is how you tell the user that something has happened in the background.

Notifications can take different forms:

- A persistent icon that goes in the status bar and is accessible through the launcher, (when the user selects it, a designated Intent can be launched),
- Turning on or flashing LEDs on the device, or
- Alerting the user by flashing the backlight, playing a sound, or vibrating.

Each of the notify methods takes an int id parameter and optionally a `https://developer.android.com/reference/kotlin/java/lang/String.html#` tag parameter, which may be `null`. These parameters are used to form a pair (tag, id), or (`null`, id) if tag is unspecified. This pair identifies this notification from your app to the system, so that pair should be unique within your app. If you call one of the notify methods with a (tag, id) pair that is currently active and a new set of notification parameters, it will be updated. For example, if you pass a new status bar icon, the old icon in the status bar will be replaced with the new one. This is also the same tag and id you pass to the cancel or cancel method to clear this notification.

> [!NOTE]
>
> ### Developer Guides
>
> For a guide to creating notifications, read the [Status Bar Notifications](https://developer.android.com/guide/topics/ui/notifiers/notifications.html) developer guide.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/app/NotificationManager.Policy` Notification policy configuration. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_APP_BLOCK_STATE_CHANGED:kotlin.String` Intent that is broadcast when an application is blocked or unblocked. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_AUTOMATIC_ZEN_RULE:kotlin.String` Activity Action: Launch an Automatic Zen Rule configuration screen |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_AUTOMATIC_ZEN_RULE_STATUS_CHANGED:kotlin.String` Intent that is broadcast when the status of an AutomaticZenRule has changed. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_CONSOLIDATED_NOTIFICATION_POLICY_CHANGED:kotlin.String` Intent that is broadcast when the state of getConsolidatedNotificationPolicy changes. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_INTERRUPTION_FILTER_CHANGED:kotlin.String` Intent that is broadcast when the state of getCurrentInterruptionFilter() changes. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_NOTIFICATION_CHANNEL_BLOCK_STATE_CHANGED:kotlin.String` Intent that is broadcast when a NotificationChannel is blocked (when getImportance is `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_NONE:kotlin.Int`) or unblocked (when getImportance is anything other than `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_NONE:kotlin.Int`). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_NOTIFICATION_CHANNEL_GROUP_BLOCK_STATE_CHANGED:kotlin.String` Intent that is broadcast when a NotificationChannelGroup is isBlocked or unblocked. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_NOTIFICATION_POLICY_ACCESS_GRANTED_CHANGED:kotlin.String` Intent that is broadcast when the state of isNotificationPolicyAccessGranted changes. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_NOTIFICATION_POLICY_CHANGED:kotlin.String` Intent that is broadcast when the state of getNotificationPolicy changes. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#AUTOMATIC_RULE_STATUS_ACTIVATED:kotlin.Int` Constant value for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_AUTOMATIC_ZEN_RULE_STATUS:kotlin.String` - the given rule has been activated by the user or cross device sync. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#AUTOMATIC_RULE_STATUS_DEACTIVATED:kotlin.Int` Constant value for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_AUTOMATIC_ZEN_RULE_STATUS:kotlin.String` - the given rule has been deactivated ("snoozed") by the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#AUTOMATIC_RULE_STATUS_DISABLED:kotlin.Int` Constant value for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_AUTOMATIC_ZEN_RULE_STATUS:kotlin.String` - the given rule currently exists but is disabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#AUTOMATIC_RULE_STATUS_ENABLED:kotlin.Int` Constant value for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_AUTOMATIC_ZEN_RULE_STATUS:kotlin.String` - the given rule currently exists and is enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#AUTOMATIC_RULE_STATUS_REMOVED:kotlin.Int` Constant value for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_AUTOMATIC_ZEN_RULE_STATUS:kotlin.String` - the given rule has been deleted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#AUTOMATIC_RULE_STATUS_UNKNOWN:kotlin.Int` Constant value for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_AUTOMATIC_ZEN_RULE_STATUS:kotlin.String` - the current status of the rule is unknown at your target sdk version, and you should continue to provide state changes via setAutomaticZenRuleState. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#BUBBLE_PREFERENCE_ALL:kotlin.Int` Indicates that all bubbles are allowed from the app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#BUBBLE_PREFERENCE_NONE:kotlin.Int` Indicates that the no bubbles are allowed from the app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#BUBBLE_PREFERENCE_SELECTED:kotlin.Int` Indicates that only notifications selected by the user will appear as bubbles. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_AUTOMATIC_RULE_ID:kotlin.String` Used as an optional string extra on `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_AUTOMATIC_ZEN_RULE:kotlin.String` intents. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_AUTOMATIC_ZEN_RULE_ID:kotlin.String` String extra for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_AUTOMATIC_ZEN_RULE_STATUS_CHANGED:kotlin.String` containing the id of the AutomaticZenRule (see addAutomaticZenRule) that has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_AUTOMATIC_ZEN_RULE_STATUS:kotlin.String` Integer extra for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_AUTOMATIC_ZEN_RULE_STATUS_CHANGED:kotlin.String` containing the state of the AutomaticZenRule. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_BLOCKED_STATE:kotlin.String` Extra for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_NOTIFICATION_CHANNEL_BLOCK_STATE_CHANGED:kotlin.String` or `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_NOTIFICATION_CHANNEL_GROUP_BLOCK_STATE_CHANGED:kotlin.String` containing the new blocked state as a boolean. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_NOTIFICATION_CHANNEL_GROUP_ID:kotlin.String` Extra for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_NOTIFICATION_CHANNEL_GROUP_BLOCK_STATE_CHANGED:kotlin.String` containing the id of the NotificationChannelGroup which has a new blocked state. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_NOTIFICATION_CHANNEL_ID:kotlin.String` Extra for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_NOTIFICATION_CHANNEL_BLOCK_STATE_CHANGED:kotlin.String` containing the id of the NotificationChannel which has a new blocked state. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_NOTIFICATION_POLICY:kotlin.String` Extra for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_NOTIFICATION_POLICY_CHANGED:kotlin.String` and `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_CONSOLIDATED_NOTIFICATION_POLICY_CHANGED:kotlin.String` containing the new `https://developer.android.com/reference/kotlin/android/app/NotificationManager.Policy` value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_DEFAULT:kotlin.Int` Default notification importance: shows everywhere, makes noise, but does not visually intrude. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_HIGH:kotlin.Int` Higher notification importance: shows everywhere, makes noise and peeks. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_LOW:kotlin.Int` Low notification importance: Shows in the shade, and potentially in the status bar (see shouldHideSilentStatusBarIcons), but is not audibly intrusive. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_MAX:kotlin.Int` Higher notification importance: shows everywhere, makes noise and peeks. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_MIN:kotlin.Int` Min notification importance: only shows in the shade, below the fold. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_NONE:kotlin.Int` A notification with no importance: does not show in the shade. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_UNSPECIFIED:kotlin.Int` Value signifying that the user has not expressed an importance. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_ALARMS:kotlin.Int` getCurrentInterruptionFilter constant - Alarms only interruption filter - all notifications except those of category `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_ALARM:kotlin.String` are suppressed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_ALL:kotlin.Int` getCurrentInterruptionFilter constant - Normal interruption filter - no notifications are suppressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_NONE:kotlin.Int` getCurrentInterruptionFilter constant - No interruptions filter - all notifications are suppressed and all audio streams (except those used for phone calls) and vibrations are muted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_PRIORITY:kotlin.Int` getCurrentInterruptionFilter constant - Priority interruption filter - all notifications are suppressed except those that match the priority criteria. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_UNKNOWN:kotlin.Int` getCurrentInterruptionFilter constant - returned when the value is unavailable for any reason. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#META_DATA_AUTOMATIC_RULE_TYPE:kotlin.String` A required `meta-data` tag for activities that handle `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_AUTOMATIC_ZEN_RULE:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/NotificationManager#META_DATA_RULE_INSTANCE_LIMIT:kotlin.String` An optional `meta-data` tag for activities that handle `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_AUTOMATIC_ZEN_RULE:kotlin.String`. |
| --- | --- |

| Public methods ||
|---|---|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | addAutomaticZenRule Creates the given zen rule. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | areAutomaticZenRulesUserManaged Returns true if users can independently and fully manage AutomaticZenRule rules. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | areBubblesAllowed Gets whether all notifications posted by this app can appear outside of the notification shade, floating over other apps' content. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | areBubblesEnabled Returns whether bubbles are enabled at the feature level for the current user. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | areNotificationsEnabled Returns whether notifications from the calling package are enabled. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | areNotificationsPaused Returns whether notifications from this package are temporarily hidden. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canNotifyAsPackage Returns whether you are allowed to post notifications on behalf of a given package, with notifyAsPackage. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canPostPromotedNotifications Returns whether the calling app's properly formatted notifications can appear in a promoted format, which may result in higher ranking, appearances on additional surfaces, and richer presentation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canUseFullScreenIntent Returns whether the calling app can send fullscreen intents. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | cancel Cancels a previously posted notification. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | cancel Cancels a previously posted notification. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | cancelAll Cancel all previously shown notifications. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | cancelAsPackage Cancels a previously posted notification. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | createNotificationChannel Creates a notification channel that notifications can be posted to. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | createNotificationChannelGroup Creates a group container for NotificationChannel objects. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | createNotificationChannelGroups Creates multiple notification channel groups. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | createNotificationChannels Creates multiple notification channels that different notifications can be posted to. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | deleteNotificationChannel Deletes the given notification channel. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | deleteNotificationChannelGroup Deletes the given notification channel group, and all notification channels that belong to it. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [StatusBarNotification](../android.service.notification/StatusBarNotification.md)!\>! | getActiveNotifications Recover a list of active notifications: ones that have been posted by the calling app that have not yet been dismissed by the user or canceled by the app. |
| open [AutomaticZenRule](AutomaticZenRule.md)! | getAutomaticZenRule Returns the AutomaticZenRule with the given id, if it exists and the caller has access. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAutomaticZenRuleState Returns the current activation state of an AutomaticZenRule. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [AutomaticZenRule](AutomaticZenRule.md)!\>! | getAutomaticZenRules Returns AutomaticZenRules owned by the caller. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getBubblePreference Gets the bubble preference for the app. |
| --- | --- |
| open [NotificationManager.Policy](../android/app/NotificationManager.Policy.md) | getConsolidatedNotificationPolicy Returns the currently applied notification policy. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getCurrentInterruptionFilter Gets the current notification interruption filter. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getImportance Returns the user specified importance for notifications from the calling package. |
| --- | --- |
| open [NotificationChannel](NotificationChannel.md)! | getNotificationChannel Returns the notification channel settings for a given channel id. |
| open [NotificationChannel](NotificationChannel.md)? | getNotificationChannel Returns the notification channel settings for a given channel and getId. |
| open [NotificationChannelGroup](NotificationChannelGroup.md)! | getNotificationChannelGroup Returns the notification channel group settings for a given channel group id. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [NotificationChannelGroup](NotificationChannelGroup.md)!\>! | getNotificationChannelGroups Returns all notification channel groups belonging to the calling app. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [NotificationChannel](NotificationChannel.md)!\>! | getNotificationChannels Returns all notification channels belonging to the calling package. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getNotificationDelegate Returns the setNotificationDelegate that can post notifications on your behalf, if there currently is one. |
| --- | --- |
| open [NotificationManager.Policy](../android/app/NotificationManager.Policy.md)! | getNotificationPolicy Gets the current user-specified default notification policy. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isNotificationListenerAccessGranted Checks whether the user has approved a given `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isNotificationPolicyAccessGranted Checks the ability to modify Notification Policy for the calling package. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | matchesCallFilter Returns whether a call from the provided URI is permitted to notify the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | notify Post a notification to be shown in the status bar. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | notify Posts a notification to be shown in the status bar. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | notifyAsPackage Posts a notification as a specified package to be shown in the status bar. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | removeAutomaticZenRule Deletes the automatic zen rule with the given id. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAutomaticZenRuleState Informs the notification manager that the state of an AutomaticZenRule has changed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setInterruptionFilter Sets the current notification interruption filter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setNotificationDelegate Allows a package to post notifications on your behalf using notifyAsPackage. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setNotificationPolicy Sets the current notification policy (which applies when setInterruptionFilter is called with the `https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_PRIORITY:kotlin.Int` value). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | shouldHideSilentStatusBarIcons Returns whether the user wants silent notifications (see `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_LOW:kotlin.Int` to appear in the status bar. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | updateAutomaticZenRule Updates the given zen rule. |

## Constants

### ACTION_APP_BLOCK_STATE_CHANGED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APP_BLOCK_STATE_CHANGED: String
```

Intent that is broadcast when an application is blocked or unblocked. This broadcast is only sent to the app whose block state has changed. Input: nothing Output: `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_BLOCKED_STATE:kotlin.String`

 Value: "android.app.action.APP_BLOCK_STATE_CHANGED"

### ACTION_AUTOMATIC_ZEN_RULE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_AUTOMATIC_ZEN_RULE: String
```

Activity Action: Launch an Automatic Zen Rule configuration screen

Input: Optionally, `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_AUTOMATIC_RULE_ID:kotlin.String`, if the configuration screen for an existing rule should be displayed. If the rule id is missing or null, apps should display a configuration screen where users can create a new instance of the rule.

Output: Nothing

You can have multiple activities handling this intent, if you support multiple AutomaticZenRule. In order for the system to properly display all of your rule types so that users can create new instances or configure existing ones, you need to add some extra metadata (`https://developer.android.com/reference/kotlin/android/app/NotificationManager#META_DATA_AUTOMATIC_RULE_TYPE:kotlin.String`) to your activity tag in your manifest. If you'd like to limit the number of rules a user can create from this flow, you can additionally optionally include `https://developer.android.com/reference/kotlin/android/app/NotificationManager#META_DATA_RULE_INSTANCE_LIMIT:kotlin.String`. For example,

```kotlin
<code>&lt;meta-data
          android:name="android.service.zen.automatic.ruleType"
          android:value="@string/my_condition_rule" /&gt;
      &lt;meta-data
          android:name="android.service.zen.automatic.ruleInstanceLimit"
          android:value="1" /&gt;
      </code>
```

 Value: "android.app.action.AUTOMATIC_ZEN_RULE"

**See Also**

- addAutomaticZenRule

### ACTION_AUTOMATIC_ZEN_RULE_STATUS_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_AUTOMATIC_ZEN_RULE_STATUS_CHANGED: String
```

Intent that is broadcast when the status of an AutomaticZenRule has changed.

Use this to know whether you need to continue monitor to device state in order to provide up-to-date states (with setAutomaticZenRuleState) for this rule.
Input: nothing Output: `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_AUTOMATIC_ZEN_RULE_ID:kotlin.String` Output: `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_AUTOMATIC_ZEN_RULE_STATUS:kotlin.String`

 Value: "android.app.action.AUTOMATIC_ZEN_RULE_STATUS_CHANGED"

### ACTION_CONSOLIDATED_NOTIFICATION_POLICY_CHANGED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CONSOLIDATED_NOTIFICATION_POLICY_CHANGED: String
```

Intent that is broadcast when the state of getConsolidatedNotificationPolicy changes.

This broadcast is only sent to registered receivers and receivers in packages that have been granted Notification Policy access (see isNotificationPolicyAccessGranted).

 Value: "android.app.action.CONSOLIDATED_NOTIFICATION_POLICY_CHANGED"

### ACTION_INTERRUPTION_FILTER_CHANGED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_INTERRUPTION_FILTER_CHANGED: String
```

Intent that is broadcast when the state of getCurrentInterruptionFilter() changes.

This broadcast is only sent to registered receivers and (starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int`) receivers in packages that have been granted Do Not Disturb access (see isNotificationPolicyAccessGranted).

 Value: "android.app.action.INTERRUPTION_FILTER_CHANGED"

### ACTION_NOTIFICATION_CHANNEL_BLOCK_STATE_CHANGED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NOTIFICATION_CHANNEL_BLOCK_STATE_CHANGED: String
```

Intent that is broadcast when a NotificationChannel is blocked (when getImportance is `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_NONE:kotlin.Int`) or unblocked (when getImportance is anything other than `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_NONE:kotlin.Int`). This broadcast is only sent to the app that owns the channel that has changed. Input: nothing Output: `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_NOTIFICATION_CHANNEL_ID:kotlin.String` Output: `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_BLOCKED_STATE:kotlin.String`

 Value: "android.app.action.NOTIFICATION_CHANNEL_BLOCK_STATE_CHANGED"

### ACTION_NOTIFICATION_CHANNEL_GROUP_BLOCK_STATE_CHANGED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NOTIFICATION_CHANNEL_GROUP_BLOCK_STATE_CHANGED: String
```

Intent that is broadcast when a NotificationChannelGroup is isBlocked or unblocked. This broadcast is only sent to the app that owns the channel group that has changed. Input: nothing Output: `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_NOTIFICATION_CHANNEL_GROUP_ID:kotlin.String` Output: `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_BLOCKED_STATE:kotlin.String`

 Value: "android.app.action.NOTIFICATION_CHANNEL_GROUP_BLOCK_STATE_CHANGED"

### ACTION_NOTIFICATION_POLICY_ACCESS_GRANTED_CHANGED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NOTIFICATION_POLICY_ACCESS_GRANTED_CHANGED: String
```

Intent that is broadcast when the state of isNotificationPolicyAccessGranted changes. This broadcast is only sent to registered receivers, and only to the apps that have changed.

 Value: "android.app.action.NOTIFICATION_POLICY_ACCESS_GRANTED_CHANGED"

### ACTION_NOTIFICATION_POLICY_CHANGED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NOTIFICATION_POLICY_CHANGED: String
```

Intent that is broadcast when the state of getNotificationPolicy changes.

This broadcast is only sent to registered receivers and (starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int`) receivers in packages that have been granted Do Not Disturb access (see isNotificationPolicyAccessGranted).

Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, most calls to setNotificationPolicy will update the app's implicit rule policy instead of the global policy, so this broadcast will be sent much less frequently.

 Value: "android.app.action.NOTIFICATION_POLICY_CHANGED"

### AUTOMATIC_RULE_STATUS_ACTIVATED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMATIC_RULE_STATUS_ACTIVATED: Int
```

Constant value for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_AUTOMATIC_ZEN_RULE_STATUS:kotlin.String` - the given rule has been activated by the user or cross device sync. Sent from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`. If the rule owner has a mode that includes a DND component, the rule owner should activate any extra behavior that's part of that mode in response to this broadcast.

 Value: 4

### AUTOMATIC_RULE_STATUS_DEACTIVATED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMATIC_RULE_STATUS_DEACTIVATED: Int
```

Constant value for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_AUTOMATIC_ZEN_RULE_STATUS:kotlin.String` - the given rule has been deactivated ("snoozed") by the user. The rule will not return to an activated state until the app calls setAutomaticZenRuleState with `https://developer.android.com/reference/kotlin/android/service/notification/Condition.html#STATE_FALSE:kotlin.Int` (either immediately or when the trigger criteria is no longer met) and then `https://developer.android.com/reference/kotlin/android/service/notification/Condition.html#STATE_TRUE:kotlin.Int` when the trigger criteria is freshly met, or when the user re-activates it.

 Value: 5

### AUTOMATIC_RULE_STATUS_DISABLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMATIC_RULE_STATUS_DISABLED: Int
```

Constant value for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_AUTOMATIC_ZEN_RULE_STATUS:kotlin.String` - the given rule currently exists but is disabled. You do not need to continue to provide state changes via setAutomaticZenRuleState until the rule is reenabled.

 Value: 2

### AUTOMATIC_RULE_STATUS_ENABLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMATIC_RULE_STATUS_ENABLED: Int
```

Constant value for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_AUTOMATIC_ZEN_RULE_STATUS:kotlin.String` - the given rule currently exists and is enabled. You should continue to provide state changes via setAutomaticZenRuleState.

 Value: 1

### AUTOMATIC_RULE_STATUS_REMOVED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMATIC_RULE_STATUS_REMOVED: Int
```

Constant value for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_AUTOMATIC_ZEN_RULE_STATUS:kotlin.String` - the given rule has been deleted. Further calls to setAutomaticZenRuleState will be ignored.

 Value: 3

### AUTOMATIC_RULE_STATUS_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMATIC_RULE_STATUS_UNKNOWN: Int
```

Constant value for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#EXTRA_AUTOMATIC_ZEN_RULE_STATUS:kotlin.String` - the current status of the rule is unknown at your target sdk version, and you should continue to provide state changes via setAutomaticZenRuleState.

 Value: -1

### BUBBLE_PREFERENCE_ALL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUBBLE_PREFERENCE_ALL: Int
```

Indicates that all bubbles are allowed from the app. If the app sends bubbles, the bubble will appear along with the notification.

 Value: 1

### BUBBLE_PREFERENCE_NONE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUBBLE_PREFERENCE_NONE: Int
```

Indicates that the no bubbles are allowed from the app. If the app sends bubbles, only the notification will appear. The notification will have an affordance allowing the user to bubble it. If the user selects this affordance, that notification is approved to bubble and the apps' bubble preference will be upgraded to `https://developer.android.com/reference/kotlin/android/app/NotificationManager#BUBBLE_PREFERENCE_SELECTED:kotlin.Int`.

 Value: 0

### BUBBLE_PREFERENCE_SELECTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUBBLE_PREFERENCE_SELECTED: Int
```

Indicates that only notifications selected by the user will appear as bubbles. If the app sends bubbles that haven't been selected, only the notification appear. If the bubble has been approved by the user, it will appear along with the notification.

 Value: 2

### EXTRA_AUTOMATIC_RULE_ID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_AUTOMATIC_RULE_ID: String
```

Used as an optional string extra on `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_AUTOMATIC_ZEN_RULE:kotlin.String` intents. If provided, contains the id of the AutomaticZenRule (as returned from addAutomaticZenRule) for which configuration settings should be displayed.

 Value: "android.app.extra.AUTOMATIC_RULE_ID"

### EXTRA_AUTOMATIC_ZEN_RULE_ID

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_AUTOMATIC_ZEN_RULE_ID: String
```

String extra for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_AUTOMATIC_ZEN_RULE_STATUS_CHANGED:kotlin.String` containing the id of the AutomaticZenRule (see addAutomaticZenRule) that has changed.

 Value: "android.app.extra.AUTOMATIC_ZEN_RULE_ID"

### EXTRA_AUTOMATIC_ZEN_RULE_STATUS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_AUTOMATIC_ZEN_RULE_STATUS: String
```

Integer extra for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_AUTOMATIC_ZEN_RULE_STATUS_CHANGED:kotlin.String` containing the state of the AutomaticZenRule.

The value will be one of `https://developer.android.com/reference/kotlin/android/app/NotificationManager#AUTOMATIC_RULE_STATUS_ENABLED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/NotificationManager#AUTOMATIC_RULE_STATUS_DISABLED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/NotificationManager#AUTOMATIC_RULE_STATUS_REMOVED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/NotificationManager#AUTOMATIC_RULE_STATUS_ACTIVATED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/NotificationManager#AUTOMATIC_RULE_STATUS_DEACTIVATED:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/app/NotificationManager#AUTOMATIC_RULE_STATUS_UNKNOWN:kotlin.Int`.

Note that the `https://developer.android.com/reference/kotlin/android/app/NotificationManager#AUTOMATIC_RULE_STATUS_ACTIVATED:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/app/NotificationManager#AUTOMATIC_RULE_STATUS_DEACTIVATED:kotlin.Int` statuses are only sent to packages targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` and above; apps targeting a lower SDK version will be sent `https://developer.android.com/reference/kotlin/android/app/NotificationManager#AUTOMATIC_RULE_STATUS_UNKNOWN:kotlin.Int` in their place instead.

 Value: "android.app.extra.AUTOMATIC_ZEN_RULE_STATUS"

### EXTRA_BLOCKED_STATE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_BLOCKED_STATE: String
```

Extra for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_NOTIFICATION_CHANNEL_BLOCK_STATE_CHANGED:kotlin.String` or `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_NOTIFICATION_CHANNEL_GROUP_BLOCK_STATE_CHANGED:kotlin.String` containing the new blocked state as a boolean. The value will be `true` if this channel or group is now blocked and `false` if this channel or group is now unblocked.

 Value: "android.app.extra.BLOCKED_STATE"

### EXTRA_NOTIFICATION_CHANNEL_GROUP_ID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NOTIFICATION_CHANNEL_GROUP_ID: String
```

Extra for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_NOTIFICATION_CHANNEL_GROUP_BLOCK_STATE_CHANGED:kotlin.String` containing the id of the NotificationChannelGroup which has a new blocked state. The value will be the getId of the group.

 Value: "android.app.extra.NOTIFICATION_CHANNEL_GROUP_ID"

### EXTRA_NOTIFICATION_CHANNEL_ID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NOTIFICATION_CHANNEL_ID: String
```

Extra for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_NOTIFICATION_CHANNEL_BLOCK_STATE_CHANGED:kotlin.String` containing the id of the NotificationChannel which has a new blocked state. The value will be the getId of the channel.

 Value: "android.app.extra.NOTIFICATION_CHANNEL_ID"

### EXTRA_NOTIFICATION_POLICY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NOTIFICATION_POLICY: String
```

Extra for `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_NOTIFICATION_POLICY_CHANGED:kotlin.String` and `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_CONSOLIDATED_NOTIFICATION_POLICY_CHANGED:kotlin.String` containing the new `https://developer.android.com/reference/kotlin/android/app/NotificationManager.Policy` value.

 Value: "android.app.extra.NOTIFICATION_POLICY"

### IMPORTANCE_DEFAULT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANCE_DEFAULT: Int
```

Default notification importance: shows everywhere, makes noise, but does not visually intrude.

 Value: 3

### IMPORTANCE_HIGH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANCE_HIGH: Int
```

Higher notification importance: shows everywhere, makes noise and peeks. May use full screen intents.

 Value: 4

### IMPORTANCE_LOW

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANCE_LOW: Int
```

Low notification importance: Shows in the shade, and potentially in the status bar (see shouldHideSilentStatusBarIcons), but is not audibly intrusive.

 Value: 2

### IMPORTANCE_MAX

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANCE_MAX: Int
```

Higher notification importance: shows everywhere, makes noise and peeks. May use full screen intents. May have elevated prominence in appearance or shade ranking. Usage is reserved by OS; app usage is capped at `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_HIGH:kotlin.Int`.

 Value: 5

### IMPORTANCE_MIN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANCE_MIN: Int
```

Min notification importance: only shows in the shade, below the fold. This should not be used with startForeground since a foreground service is supposed to be something the user cares about so it does not make semantic sense to mark its notification as minimum importance. If you do this as of Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int`, the system will show a higher-priority notification about your app running in the background.

 Value: 1

### IMPORTANCE_NONE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANCE_NONE: Int
```

A notification with no importance: does not show in the shade.

 Value: 0

### IMPORTANCE_UNSPECIFIED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPORTANCE_UNSPECIFIED: Int
```

Value signifying that the user has not expressed an importance. This value is for persisting preferences, and should never be associated with an actual notification.

 Value: -1000

### INTERRUPTION_FILTER_ALARMS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERRUPTION_FILTER_ALARMS: Int
```

getCurrentInterruptionFilter constant - Alarms only interruption filter - all notifications except those of category `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_ALARM:kotlin.String` are suppressed. Some audio streams are muted.

 Value: 4

### INTERRUPTION_FILTER_ALL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERRUPTION_FILTER_ALL: Int
```

getCurrentInterruptionFilter constant - Normal interruption filter - no notifications are suppressed.

 Value: 1

### INTERRUPTION_FILTER_NONE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERRUPTION_FILTER_NONE: Int
```

getCurrentInterruptionFilter constant - No interruptions filter - all notifications are suppressed and all audio streams (except those used for phone calls) and vibrations are muted.

 Value: 3

### INTERRUPTION_FILTER_PRIORITY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERRUPTION_FILTER_PRIORITY: Int
```

getCurrentInterruptionFilter constant - Priority interruption filter - all notifications are suppressed except those that match the priority criteria. Some audio streams are muted. See `https://developer.android.com/reference/kotlin/android/app/NotificationManager.Policy#priorityCallSenders:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/NotificationManager.Policy#priorityCategories:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/NotificationManager.Policy#priorityMessageSenders:kotlin.Int` to define or query this criteria. Users can additionally specify packages that can bypass this interruption filter.

 Value: 2

### INTERRUPTION_FILTER_UNKNOWN

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERRUPTION_FILTER_UNKNOWN: Int
```

getCurrentInterruptionFilter constant - returned when the value is unavailable for any reason.

 Value: 0

### META_DATA_AUTOMATIC_RULE_TYPE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_DATA_AUTOMATIC_RULE_TYPE: String
```

A required `meta-data` tag for activities that handle `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_AUTOMATIC_ZEN_RULE:kotlin.String`. This tag should contain a localized name of the type of the zen rule provided by the activity.

 Value: "android.service.zen.automatic.ruleType"

### META_DATA_RULE_INSTANCE_LIMIT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_DATA_RULE_INSTANCE_LIMIT: String
```

An optional `meta-data` tag for activities that handle `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_AUTOMATIC_ZEN_RULE:kotlin.String`. This tag should contain the maximum number of rule instances that can be created for this rule type. Omit or enter a value \<= 0 to allow unlimited instances.

 Value: "android.service.zen.automatic.ruleInstanceLimit"

## Public methods

### addAutomaticZenRule

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addAutomaticZenRule(automaticZenRule: AutomaticZenRule!): String!
```

Creates the given zen rule.

Throws a SecurityException if policy access is not granted to this package. See isNotificationPolicyAccessGranted.

| Parameters ||
|---|---|
| `automaticZenRule` | [AutomaticZenRule](AutomaticZenRule.md)!: the rule to create. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The id of the newly created rule; null if the rule could not be created. |

### areAutomaticZenRulesUserManaged

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun areAutomaticZenRulesUserManaged(): Boolean
```

Returns true if users can independently and fully manage AutomaticZenRule rules. This includes the ability to independently activate/deactivate rules and overwrite/freeze the behavior (policy) of the rule when activated.

If this method returns true, calls to updateAutomaticZenRule may fail and apps should defer rule management to system settings/uis via `https://developer.android.com/reference/kotlin/android/provider/Settings.html#ACTION_AUTOMATIC_ZEN_RULE_SETTINGS:kotlin.String`.

### areBubblesAllowed

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun areBubblesAllowed(): Boolean
```

**Deprecated:** *use getBubblePreference instead.*

Gets whether all notifications posted by this app can appear outside of the notification shade, floating over other apps' content.

This value will be ignored for notifications that are posted to channels that do not allow bubbles (canBubble).
**See Also**

- getBubbleMetadata

### areBubblesEnabled

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun areBubblesEnabled(): Boolean
```

Returns whether bubbles are enabled at the feature level for the current user. When enabled, notifications able to bubble will display an affordance allowing the user to bubble them.
**See Also**

- setBubbleMetadata

### areNotificationsEnabled

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun areNotificationsEnabled(): Boolean
```

Returns whether notifications from the calling package are enabled.

### areNotificationsPaused

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun areNotificationsPaused(): Boolean
```

Returns whether notifications from this package are temporarily hidden. This could be done because the package was marked as distracting to the user via `PackageManager#setDistractingPackageRestrictions(String[], int)` or because the package is `PackageManager#setPackagesSuspended(String[], boolean, PersistableBundle, PersistableBundle, SuspendDialogInfo) suspended`.

### canNotifyAsPackage

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canNotifyAsPackage(pkg: String): Boolean
```

Returns whether you are allowed to post notifications on behalf of a given package, with notifyAsPackage. See setNotificationDelegate.

| Parameters ||
|---|---|
| `pkg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### canPostPromotedNotifications

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canPostPromotedNotifications(): Boolean
```

Returns whether the calling app's properly formatted notifications can appear in a promoted format, which may result in higher ranking, appearances on additional surfaces, and richer presentation. Apps can request this permission by sending the user to the activity that matches the system intent action `https://developer.android.com/reference/kotlin/android/provider/Settings.html#ACTION_APP_NOTIFICATION_PROMOTION_SETTINGS:kotlin.String`.

### canUseFullScreenIntent

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canUseFullScreenIntent(): Boolean
```

Returns whether the calling app can send fullscreen intents.

From Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, apps may not have permission to use `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#USE_FULL_SCREEN_INTENT:kotlin.String`. If permission is denied, notification will show up as an expanded heads up notification on lockscreen.

To request access, add the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#USE_FULL_SCREEN_INTENT:kotlin.String` permission to your manifest, and use `https://developer.android.com/reference/kotlin/android/provider/Settings.html#ACTION_MANAGE_APP_USE_FULL_SCREEN_INTENT:kotlin.String`.

### cancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancel(id: Int): Unit
```

Cancels a previously posted notification.

If the notification does not currently represent a startForeground or a setUserInitiated, it will be removed from the UI and live `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` will be informed so they can remove the notification from their UIs.

### cancel

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancel(
    tag: String?, 
    id: Int
): Unit
```

Cancels a previously posted notification.

If the notification does not currently represent a startForeground or a setUserInitiated, it will be removed from the UI and live `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` will be informed so they can remove the notification from their UIs.

| Parameters ||
|---|---|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

### cancelAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancelAll(): Unit
```

Cancel all previously shown notifications. See #cancel for the detailed behavior.

### cancelAsPackage

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancelAsPackage(
    targetPackage: String, 
    tag: String?, 
    id: Int
): Unit
```

Cancels a previously posted notification.

If the notification does not currently represent a startForeground or a setUserInitiated, it will be removed from the UI and live `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` will be informed so they can remove the notification from their UIs.

This method may be used by getNotificationDelegate to cancel notifications that they have posted via notifyAsPackage.

| Parameters ||
|---|---|
| `targetPackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package to cancel the notification as. If this package is not your package, you can only cancel notifications you posted with notifyAsPackage. This value cannot be `null`. |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A string identifier for this notification. May be `null`. |
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An identifier for this notification. |
| --- | --- |

### createNotificationChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createNotificationChannel(channel: NotificationChannel): Unit
```

Creates a notification channel that notifications can be posted to. This can also be used to restore a deleted channel and to update an existing channel's name, description, group, and/or importance.

The name and description should only be changed if the locale changes or in response to the user renaming this channel. For example, if a user has a channel named 'Messages' and the user changes their locale, this channel's name should be updated with the translation of 'Messages' in the new locale.

The importance of an existing channel will only be changed if the new importance is lower than the current value and the user has not altered any settings on this channel.

The group an existing channel will only be changed if the channel does not already belong to a group. All other fields are ignored for channels that already exist.

| Parameters ||
|---|---|
| `channel` | [NotificationChannel](NotificationChannel.md): the channel to create. Note that the created channel may differ from this value. If the provided channel is malformed, a RemoteException will be thrown. This value cannot be `null`. |

### createNotificationChannelGroup

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createNotificationChannelGroup(group: NotificationChannelGroup): Unit
```

Creates a group container for NotificationChannel objects. This can be used to rename an existing group.

Group information is only used for presentation, not for behavior. Groups are optional for channels, and you can have a mix of channels that belong to groups and channels that do not.

For example, if your application supports multiple accounts, and those accounts will have similar channels, you can create a group for each account with account specific labels instead of appending account information to each channel's label.

| Parameters ||
|---|---|
| `group` | [NotificationChannelGroup](NotificationChannelGroup.md): The group to create. This value cannot be `null`. |

### createNotificationChannelGroups

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createNotificationChannelGroups(groups: MutableList<NotificationChannelGroup!>): Unit
```

Creates multiple notification channel groups.

| Parameters ||
|---|---|
| `groups` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [NotificationChannelGroup](NotificationChannelGroup.md)!\>: The list of groups to create. This value cannot be `null`. |

### createNotificationChannels

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createNotificationChannels(channels: MutableList<NotificationChannel!>): Unit
```

Creates multiple notification channels that different notifications can be posted to. See createNotificationChannel.

| Parameters ||
|---|---|
| `channels` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [NotificationChannel](NotificationChannel.md)!\>: the list of channels to attempt to create. This value cannot be `null`. |

### deleteNotificationChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun deleteNotificationChannel(channelId: String!): Unit
```

Deletes the given notification channel.

If you createNotificationChannel a new channel with this same id, the deleted channel will be un-deleted with all of the same settings it had before it was deleted.

### deleteNotificationChannelGroup

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun deleteNotificationChannelGroup(groupId: String!): Unit
```

Deletes the given notification channel group, and all notification channels that belong to it.

### getActiveNotifications

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActiveNotifications(): Array<StatusBarNotification!>!
```

Recover a list of active notifications: ones that have been posted by the calling app that have not yet been dismissed by the user or canceled by the app.

[StatusBarNotification](../android.service.notification/StatusBarNotification.md) object, including the original `tag` and `id` supplied to notify (via getTag and getId) as well as a copy of the original Notification object (via getNotification).

From `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int`, will also return notifications you've posted as an app's notification delegate via notifyAsPackage.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification.html#!>!` | An array of `https://developer.android.com/reference/kotlin/android/service/notification/StatusBarNotification.html#`. |

### getAutomaticZenRule

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAutomaticZenRule(id: String!): AutomaticZenRule!
```

Returns the AutomaticZenRule with the given id, if it exists and the caller has access.

Throws a SecurityException if policy access is not granted to this package. See isNotificationPolicyAccessGranted.

Returns null if there are no zen rules that match the given id, or if the calling package doesn't own the matching rule. See getOwner.

### getAutomaticZenRuleState

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAutomaticZenRuleState(id: String): Int
```

Returns the current activation state of an AutomaticZenRule.

Returns `https://developer.android.com/reference/kotlin/android/service/notification/Condition.html#STATE_UNKNOWN:kotlin.Int` if the rule does not exist or the calling package doesn't have access to it.

| Parameters ||
|---|---|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The id of the rule. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the state of the rule. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/service/notification/Condition.html#STATE_FALSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/notification/Condition.html#STATE_TRUE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/notification/Condition.html#STATE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/notification/Condition.html#STATE_ERROR:kotlin.Int` |

### getAutomaticZenRules

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAutomaticZenRules(): MutableMap<String!, AutomaticZenRule!>!
```

Returns AutomaticZenRules owned by the caller.

Throws a SecurityException if policy access is not granted to this package. See isNotificationPolicyAccessGranted.

### getBubblePreference

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBubblePreference(): Int
```

Gets the bubble preference for the app. This preference only applies to notifications that have been properly configured to bubble.

If `https://developer.android.com/reference/kotlin/android/app/NotificationManager#BUBBLE_PREFERENCE_ALL:kotlin.Int`, then any bubble notification will appear as a bubble, as long as the user hasn't excluded it (canBubble).

If `https://developer.android.com/reference/kotlin/android/app/NotificationManager#BUBBLE_PREFERENCE_SELECTED:kotlin.Int`, then any bubble notification will appear as a bubble, as long as the user has selected it.

If `https://developer.android.com/reference/kotlin/android/app/NotificationManager#BUBBLE_PREFERENCE_NONE:kotlin.Int`, then no notification may appear as a bubble from the app.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the users' bubble preference for the app. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#BUBBLE_PREFERENCE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#BUBBLE_PREFERENCE_SELECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#BUBBLE_PREFERENCE_ALL:kotlin.Int` |

**See Also**

- getBubbleMetadata

### getConsolidatedNotificationPolicy

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getConsolidatedNotificationPolicy(): NotificationManager.Policy
```

Returns the currently applied notification policy.

If getCurrentInterruptionFilter is equal to `https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_ALL:kotlin.Int`, then the consolidated notification policy will match the default notification policy returned by getNotificationPolicy.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/NotificationManager.Policy` | This value cannot be `null`. |

### getCurrentInterruptionFilter

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCurrentInterruptionFilter(): Int
```

Gets the current notification interruption filter.

The interruption filter defines which notifications are allowed to interrupt the user (e.g. via sound \& vibration) and is applied globally.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_PRIORITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_ALARMS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_ALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_UNKNOWN:kotlin.Int` |

### getImportance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getImportance(): Int
```

Returns the user specified importance for notifications from the calling package.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_MIN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_LOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_HIGH:kotlin.Int` |

### getNotificationChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNotificationChannel(channelId: String!): NotificationChannel!
```

Returns the notification channel settings for a given channel id.

The channel must belong to your package, or to a package you are an approved notification delegate for (see canNotifyAsPackage), or it will not be returned. To query a channel as a notification delegate, call this method from a context created for that package (see createPackageContext).

### getNotificationChannel

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNotificationChannel(
    channelId: String, 
    conversationId: String
): NotificationChannel?
```

Returns the notification channel settings for a given channel and getId.

The channel must belong to your package, or to a package you are an approved notification delegate for (see canNotifyAsPackage), or it will not be returned. To query a channel as a notification delegate, call this method from a context created for that package (see createPackageContext).

If a conversation channel with the given conversation id is not found, this method will instead return the parent channel with the given channel ID, or `null` if neither exists.

| Parameters ||
|---|---|
| `channelId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `conversationId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### getNotificationChannelGroup

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNotificationChannelGroup(channelGroupId: String!): NotificationChannelGroup!
```

Returns the notification channel group settings for a given channel group id. The channel group must belong to your package, or null will be returned.

### getNotificationChannelGroups

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNotificationChannelGroups(): MutableList<NotificationChannelGroup!>!
```

Returns all notification channel groups belonging to the calling app.

### getNotificationChannels

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNotificationChannels(): MutableList<NotificationChannel!>!
```

Returns all notification channels belonging to the calling package.

Approved notification delegates (see canNotifyAsPackage) can query notification channels belonging to packages they are the delegate for. To do so, call this method from a context created for that package (see createPackageContext).

### getNotificationDelegate

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNotificationDelegate(): String?
```

Returns the setNotificationDelegate that can post notifications on your behalf, if there currently is one.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### getNotificationPolicy

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNotificationPolicy(): NotificationManager.Policy!
```

Gets the current user-specified default notification policy.

For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` and above (with some exceptions, such as companion device managers) this method will return the policy associated to their implicit AutomaticZenRule instead, if it exists. See setNotificationPolicy.

### isNotificationListenerAccessGranted

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isNotificationListenerAccessGranted(listener: ComponentName!): Boolean
```

Checks whether the user has approved a given `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#`.

The listener service must belong to the calling app.

Apps can request notification listener access by sending the user to the activity that matches the system intent action `https://developer.android.com/reference/kotlin/android/provider/Settings.html#ACTION_NOTIFICATION_LISTENER_SETTINGS:kotlin.String`.

### isNotificationPolicyAccessGranted

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isNotificationPolicyAccessGranted(): Boolean
```

Checks the ability to modify Notification Policy for the calling package.

Returns true if the calling package can modify notification policy.

Apps can request policy access by sending the user to the activity that matches the system intent action `https://developer.android.com/reference/kotlin/android/provider/Settings.html#ACTION_NOTIFICATION_POLICY_ACCESS_SETTINGS:kotlin.String`.

Use `https://developer.android.com/reference/kotlin/android/app/NotificationManager#ACTION_NOTIFICATION_POLICY_ACCESS_GRANTED_CHANGED:kotlin.String` to listen for user grant or denial of this access.

### matchesCallFilter

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun matchesCallFilter(uri: Uri): Boolean
```

Returns whether a call from the provided URI is permitted to notify the user.

A true return value indicates one of the following: Do Not Disturb is not currently active; or the caller is a repeat caller and the current policy allows interruptions from repeat callers; or the caller is in the user's set of contacts whose calls are allowed to interrupt Do Not Disturb.

If Do Not Disturb is enabled and either no interruptions or only alarms are allowed, this method will return false regardless of input.

The provided URI should be a `tel:` or `mailto:` schema URI indicating the source of the call. For an accurate answer regarding whether the caller matches the user's permitted contacts, the path part of the URI must match an entry the Contacts database in the appropriate column.

Passing in a `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.html#CONTENT_LOOKUP_URI:android.net.Uri` is also permissible, but should only be used for priority contact interruptions and may not provide accurate results in the case of repeat callers.

See also setUri and `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.html#CONTENT_LOOKUP_URI:android.net.Uri` for more information.

Callers of this method must have notification listener access, permission to read contacts, or have system permissions.

NOTE: This method calls into Contacts, which may take some time, and should not be called on the main thread.
. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `uri` | [Uri](../android.net/Uri.md): A URI representing a caller. Must not be null. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | A boolean indicating whether a call from the URI provided would be allowed to interrupt the user given the current filter. |

### notify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun notify(
    id: Int, 
    notification: Notification!
): Unit
```

Post a notification to be shown in the status bar. If a notification with the same id has already been posted by your application and has not yet been canceled, it will be replaced by the updated information.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An identifier for this notification unique within your application. |
| `notification` | [Notification](Notification.md)!: A Notification object describing what to show the user. Must not be null. |

### notify

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun notify(
    tag: String!, 
    id: Int, 
    notification: Notification!
): Unit
```

Posts a notification to be shown in the status bar. If a notification with the same tag and id has already been posted by your application and has not yet been canceled, it will be replaced by the updated information. All `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` will be granted `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` access to any `https://developer.android.com/reference/kotlin/android/net/Uri.html#` provided on this notification or the NotificationChannel this notification is posted to using grantUriPermission. Permission will be revoked when the notification is canceled, or you can revoke permissions with revokeUriPermission.

| Parameters ||
|---|---|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A string identifier for this notification. May be `null`. |
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An identifier for this notification. The pair (tag, id) must be unique within your application. |
| `notification` | [Notification](Notification.md)!: A Notification object describing what to show the user. Must not be null. |
| --- | --- |

### notifyAsPackage

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun notifyAsPackage(
    targetPackage: String, 
    tag: String?, 
    id: Int, 
    notification: Notification
): Unit
```

Posts a notification as a specified package to be shown in the status bar. If a notification with the same tag and id has already been posted for that package and has not yet been canceled, it will be replaced by the updated information. All `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` will be granted `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` access to any `https://developer.android.com/reference/kotlin/android/net/Uri.html#` provided on this notification or the NotificationChannel this notification is posted to using grantUriPermission. Permission will be revoked when the notification is canceled, or you can revoke permissions with revokeUriPermission.

| Parameters ||
|---|---|
| `targetPackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package to post the notification as. The package must have granted you access to post notifications on their behalf with setNotificationDelegate. This value cannot be `null`. |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: A string identifier for this notification. May be `null`. |
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An identifier for this notification. The pair (tag, id) must be unique within your application. |
| --- | --- |
| `notification` | [Notification](Notification.md): A Notification object describing what to show the user. Must not be null. |

### removeAutomaticZenRule

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAutomaticZenRule(id: String!): Boolean
```

Deletes the automatic zen rule with the given id.

Throws a SecurityException if policy access is not granted to this package. See isNotificationPolicyAccessGranted.

Callers can only delete rules that they own. See getOwner.

| Parameters ||
|---|---|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the id of the rule to delete. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the rule was successfully deleted. |

### setAutomaticZenRuleState

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAutomaticZenRuleState(
    id: String, 
    condition: Condition
): Unit
```

Informs the notification manager that the state of an AutomaticZenRule has changed. Use this method to put the system into Do Not Disturb mode or request that it exits Do Not Disturb mode. The calling app must own the provided AutomaticZenRule.

This method can be used in conjunction with or as a replacement to notifyCondition.

The condition change may be ignored if the user has activated or deactivated the rule manually -- the user can "override" the rule *this time* , with the rule resuming its normal operation for the next cycle. When this has happened, the supplied condition will be applied only once the automatic state is in agreement with the user-provided state. For example, assume that the AutomaticZenRule corresponds to a "Driving Mode" with automatic driving detection.

1. App detects driving and notifies the system that the rule should be active, calling this method with a `https://developer.android.com/reference/kotlin/android/service/notification/Condition.html#` with `https://developer.android.com/reference/kotlin/android/service/notification/Condition.html#STATE_TRUE:kotlin.Int`).
2. User deactivates ("snoozes") the rule for some reason. This overrides the app-provided condition state.
3. App is still detecting driving, so again calls with `https://developer.android.com/reference/kotlin/android/service/notification/Condition.html#STATE_TRUE:kotlin.Int`. This is ignored by the system, as the user override prevails.
4. Some time later, the app detects that driving stopped, so the rule should be inactive, and calls with `https://developer.android.com/reference/kotlin/android/service/notification/Condition.html#STATE_FALSE:kotlin.Int`). This doesn't change the actual rule state (it was already inactive due to the user's override), but clears the override.
5. Some time later, the app detects that driving has started again, and notifies that the rule should be active (calling with `https://developer.android.com/reference/kotlin/android/service/notification/Condition.html#STATE_TRUE:kotlin.Int` again). The rule is activated.

Note that the behavior at step #3 is different if the app also specifies `https://developer.android.com/reference/kotlin/android/service/notification/Condition.html#SOURCE_USER_ACTION:kotlin.Int` as the `https://developer.android.com/reference/kotlin/android/service/notification/Condition.html#source:kotlin.Int` -- rule state updates coming from user actions are not ignored.

| Parameters ||
|---|---|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The id of the rule whose state should change. This value cannot be `null`. |
| `condition` | [Condition](../android.service.notification/Condition.md): The new state of this rule. This value cannot be `null`. |

### setInterruptionFilter

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setInterruptionFilter(interruptionFilter: Int): Unit
```

Sets the current notification interruption filter.

The interruption filter defines which notifications are allowed to interrupt the user (e.g. via sound \& vibration) and is applied globally.

Apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` and above (with some exceptions, such as companion device managers) cannot modify the global interruption filter. Calling this method will instead activate or deactivate an AutomaticZenRule associated to the app, using a `https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy.html#` that corresponds to the `https://developer.android.com/reference/kotlin/android/app/NotificationManager.Policy` supplied to setNotificationPolicy (or the global policy when one wasn't provided).

Only available if policy access is granted to this package. See isNotificationPolicyAccessGranted.

| Parameters ||
|---|---|
| `interruptionFilter` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_PRIORITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_ALARMS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_ALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_UNKNOWN:kotlin.Int` |

### setNotificationDelegate

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNotificationDelegate(delegate: String?): Unit
```

Allows a package to post notifications on your behalf using notifyAsPackage. This can be used to allow persistent processes to post notifications based on messages received on your behalf from the cloud, without your process having to wake up. You can check if you have an allowed delegate with getNotificationDelegate and revoke your delegate by passing null to this method.

| Parameters ||
|---|---|
| `delegate` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: Package name of the app which can send notifications on your behalf. This value may be `null`. |

### setNotificationPolicy

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNotificationPolicy(policy: NotificationManager.Policy): Unit
```

Sets the current notification policy (which applies when setInterruptionFilter is called with the `https://developer.android.com/reference/kotlin/android/app/NotificationManager#INTERRUPTION_FILTER_PRIORITY:kotlin.Int` value).

Apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` and above (with some exceptions, such as companion device managers) cannot modify the global notification policy. Calling this method will instead create or update an AutomaticZenRule associated to the app, using a `https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy.html#` corresponding to the `https://developer.android.com/reference/kotlin/android/app/NotificationManager.Policy` supplied here, and which will be activated/deactivated by calls to setInterruptionFilter.

Only available if policy access is granted to this package. See isNotificationPolicyAccessGranted.

| Parameters ||
|---|---|
| `policy` | [NotificationManager.Policy](../android/app/NotificationManager.Policy.md): The new desired policy. This value cannot be `null`. |

### shouldHideSilentStatusBarIcons

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun shouldHideSilentStatusBarIcons(): Boolean
```

Returns whether the user wants silent notifications (see `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_LOW:kotlin.Int` to appear in the status bar.

Only available for isNotificationListenerAccessGranted.

### updateAutomaticZenRule

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateAutomaticZenRule(
    id: String!, 
    automaticZenRule: AutomaticZenRule!
): Boolean
```

Updates the given zen rule.

Before `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, updating a rule that is not backed up by a `https://developer.android.com/reference/kotlin/android/service/notification/ConditionProviderService.html#` will deactivate it if it was previously active. Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, this will only happen if the rule's definition is actually changing.

Throws a SecurityException if policy access is not granted to this package. See isNotificationPolicyAccessGranted.

Callers can only update rules that they own. See getOwner.

| Parameters ||
|---|---|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The id of the rule to update |
| `automaticZenRule` | [AutomaticZenRule](AutomaticZenRule.md)!: the rule to update. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the rule was successfully updated. |
