Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Notification

```
open class Notification : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.Notification](https://developer.android.com/reference/kotlin/android/app/Notification#) |

A class that represents how a persistent notification is to be presented to the user using the `https://developer.android.com/reference/kotlin/android/app/NotificationManager`.

The `https://developer.android.com/reference/kotlin/android/app/Notification.Builder` has been added to make it easier to construct Notifications.

> [!NOTE]
>
> ### Developer Guides
>
> For a guide to creating notifications, read the [Status Bar Notifications](https://developer.android.com/guide/topics/ui/notifiers/notifications.html) developer guide.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/app/Notification.Action` Structure to encapsulate a named action that can be shown as part of this notification. |
| open | `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle` Helper class for generating large-format notifications that include a large image attachment. |
| open | `https://developer.android.com/reference/kotlin/android/app/Notification.BigTextStyle` Helper class for generating large-format notifications that include a lot of text. |
| | `https://developer.android.com/reference/kotlin/android/app/Notification.BridgedNotificationMetadata` Encapsulates the information needed to display a notification as a bridged notification. |
| | `https://developer.android.com/reference/kotlin/android/app/Notification.BubbleMetadata` Encapsulates the information needed to display a notification as a bubble. |
| open | `https://developer.android.com/reference/kotlin/android/app/Notification.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/app/Notification#` objects. |
| open | `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` Helper class for generating large-format notifications that include a caller and required actions, such as an incoming call with answer / decline. |
| | `https://developer.android.com/reference/kotlin/android/app/Notification.CarExtender` Helper class to add Android Auto extensions to notifications. |
| open | `https://developer.android.com/reference/kotlin/android/app/Notification.DecoratedCustomViewStyle` Notification style for custom views that are decorated by the system |
| open | `https://developer.android.com/reference/kotlin/android/app/Notification.DecoratedMediaCustomViewStyle` Notification style for media custom views that are decorated by the system |
| abstract | `https://developer.android.com/reference/kotlin/android/app/Notification.Extender` Extender interface for use with `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#extend(android.app.Notification.Extender)`. |
| open | `https://developer.android.com/reference/kotlin/android/app/Notification.InboxStyle` Helper class for generating large-format notifications that include a list of (up to 5) strings. |
| open | `https://developer.android.com/reference/kotlin/android/app/Notification.MediaStyle` Notification style for media playback notifications. |
| open | `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle` Helper class for generating large-format notifications that include multiple back-and-forth messages of varying types between any number of people. |
| | `https://developer.android.com/reference/kotlin/android/app/Notification.Metric` A metric, used with `https://developer.android.com/reference/kotlin/android/app/Notification.MetricStyle`, and which has a value and a label. |
| | `https://developer.android.com/reference/kotlin/android/app/Notification.MetricStyle` A notification style which shows up to 3 metrics when expanded. |
| open | `https://developer.android.com/reference/kotlin/android/app/Notification.ProgressStyle` A Notification Style used to define a notification whose expanded state includes a highly customizable progress bar with segments, points, a custom tracker icon, and custom icons at the start and end of the progress bar. |
| | `https://developer.android.com/reference/kotlin/android/app/Notification.ProjectedExtender` Helper class to add projection-specific extensions to a notification. |
| abstract | `https://developer.android.com/reference/kotlin/android/app/Notification.Style` An object that can apply a rich notification style to a `https://developer.android.com/reference/kotlin/android/app/Notification.Builder` object. |
| | `https://developer.android.com/reference/kotlin/android/app/Notification.TvExtender` Helper class to add Android TV extensions to notifications. |
| | `https://developer.android.com/reference/kotlin/android/app/Notification.WearableExtender` Helper class to add wearable extensions to notifications. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#ACTION_BRIDGED_NOTIFICATION_PREFERENCES:kotlin.String` An activity that provides a user interface for adjusting notification preferences for its bridged notification which originated on another device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#BADGE_ICON_LARGE:kotlin.Int` If this notification is being shown as a badge, use the `https://developer.android.com/reference/kotlin/android/app/Notification#getLargeIcon()` to represent this notification. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#BADGE_ICON_NONE:kotlin.Int` If this notification is being shown as a badge, always show as a number. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#BADGE_ICON_SMALL:kotlin.Int` If this notification is being shown as a badge, use the `https://developer.android.com/reference/kotlin/android/app/Notification#getSmallIcon()` to represent this notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_ALARM:kotlin.String` Notification category: alarm or timer. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_CALL:kotlin.String` Notification category: incoming call (voice or video) or similar synchronous communication request. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_EMAIL:kotlin.String` Notification category: asynchronous bulk message (email). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_ERROR:kotlin.String` Notification category: error in background operation or authentication status. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_EVENT:kotlin.String` Notification category: calendar event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_LOCATION_SHARING:kotlin.String` Notification category: temporarily sharing location. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_MESSAGE:kotlin.String` Notification category: incoming direct message (SMS, instant message, etc.). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_MISSED_CALL:kotlin.String` Notification category: missed call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_NAVIGATION:kotlin.String` Notification category: map turn-by-turn navigation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_PROGRESS:kotlin.String` Notification category: progress of a long-running background operation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_PROMO:kotlin.String` Notification category: promotion or advertisement. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_RECOMMENDATION:kotlin.String` Notification category: a specific, timely recommendation for a single thing. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_REMINDER:kotlin.String` Notification category: user-scheduled reminder. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_SERVICE:kotlin.String` Notification category: indication of running background service. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_SOCIAL:kotlin.String` Notification category: social network or sharing update. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_STATUS:kotlin.String` Notification category: ongoing information about device or contextual status. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_STOPWATCH:kotlin.String` Notification category: running stopwatch. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_SYSTEM:kotlin.String` Notification category: system or device status update. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_TRANSPORT:kotlin.String` Notification category: media transport control for playback. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_VOICEMAIL:kotlin.String` Notification category: voicemail. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#CATEGORY_WORKOUT:kotlin.String` Notification category: tracking a user's workout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#COLOR_DEFAULT:kotlin.Int` Special value of `https://developer.android.com/reference/kotlin/android/app/Notification#color:kotlin.Int` telling the system not to decorate this element with any special color (but instead use default system colors). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#DEFAULT_ALL:kotlin.Int` Use all default values (where applicable). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#DEFAULT_LIGHTS:kotlin.Int` Use the default notification lights. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#DEFAULT_SOUND:kotlin.Int` Use the default notification sound. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#DEFAULT_VIBRATE:kotlin.Int` Use the default notification vibrate. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_ANSWER_COLOR:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the color used as a hint for the Answer action button of a `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_ANSWER_INTENT:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the intent to be sent when the users answers a `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_AUDIO_CONTENTS_URI:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the audio contents of this notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_BACKGROUND_IMAGE_URI:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: flat `https://developer.android.com/reference/kotlin/java/lang/String.html#` representation of a `https://developer.android.com/reference/kotlin/android/content/ContentUris.html#` pointing to an image that can be displayed in the background when the notification is selected. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_BIG_TEXT:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is the longer text shown in the expanded form of a `https://developer.android.com/reference/kotlin/android/app/Notification.BigTextStyle` notification, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.BigTextStyle#bigText(kotlin.CharSequence)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_CALL_IS_VIDEO:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: whether the `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification is for a call that will activate video when answered. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_CALL_PERSON:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the person to be displayed as calling for the `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_CALL_TYPE:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the type of call represented by the `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_CHANNEL_GROUP_ID:kotlin.String` Optional extra for `https://developer.android.com/reference/kotlin/android/app/Notification#INTENT_CATEGORY_NOTIFICATION_PREFERENCES:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_CHANNEL_ID:kotlin.String` Optional extra for `https://developer.android.com/reference/kotlin/android/app/Notification#INTENT_CATEGORY_NOTIFICATION_PREFERENCES:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_CHRONOMETER_COUNT_DOWN:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: whether the chronometer set on the notification should count down instead of counting up. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_COLORIZED:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: whether the notification should be colorized as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setColorized(kotlin.Boolean)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_COMPACT_ACTIONS:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the indices of actions to be shown in the compact view, as supplied to (e.g.) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_CONVERSATION_TITLE:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: a `https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#` to be displayed as the title to a conversation represented by a `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle` |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_DECLINE_COLOR:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the color used as a hint for the Decline or Hang Up action button of a `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_DECLINE_INTENT:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the intent to be sent when the users declines a `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_HANG_UP_INTENT:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the intent to be sent when the users hangs up a `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_HISTORIC_MESSAGES:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: an array of `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle#addHistoricMessage(android.app.Notification.MessagingStyle.Message)` `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle.Message` bundles provided by a `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle` notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_INFO_TEXT:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is a small piece of additional text as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setContentInfo(kotlin.CharSequence)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_IS_GROUP_CONVERSATION:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: whether the `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle` notification represents a group conversation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_LARGE_ICON:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is a bitmap to be used instead of the small icon when showing the notification payload, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setLargeIcon(android.graphics.Bitmap)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_LARGE_ICON_BIG:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is a bitmap to be used instead of the one from `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setLargeIcon(android.graphics.Bitmap)` when the notification is shown in its expanded form, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle#bigLargeIcon(android.graphics.Bitmap)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_MEDIA_SESSION:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: A `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token.html#` associated with a `https://developer.android.com/reference/kotlin/android/app/Notification.MediaStyle` notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_MESSAGES:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: an array of `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle.Message` bundles provided by a `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle` notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_MESSAGING_PERSON:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the person to be displayed for all messages sent by the user including direct replies `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle` notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_NOTIFICATION_ID:kotlin.String` Optional extra for `https://developer.android.com/reference/kotlin/android/app/Notification#INTENT_CATEGORY_NOTIFICATION_PREFERENCES:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_NOTIFICATION_TAG:kotlin.String` Optional extra for `https://developer.android.com/reference/kotlin/android/app/Notification#INTENT_CATEGORY_NOTIFICATION_PREFERENCES:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_PEOPLE:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: A String array containing the people that this notification relates to, each of which was supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#addPerson(kotlin.String)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_PEOPLE_LIST:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: An arrayList of `https://developer.android.com/reference/kotlin/android/app/Person` objects containing the people that this notification relates to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_PICTURE:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is a bitmap to be shown in `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle` expanded notifications, supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle#bigPicture(android.graphics.Bitmap)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_PICTURE_CONTENT_DESCRIPTION:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is a content description of the big picture supplied from `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle#bigPicture(android.graphics.Bitmap)`, supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle#setContentDescription(kotlin.CharSequence)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_PICTURE_ICON:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is an `https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#` of an image to be shown in `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle` expanded notifications, supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle#bigPicture(android.graphics.drawable.Icon)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_PREFER_SMALL_ICON:kotlin.String` A boolean for `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` requesting that the notification card show the small icon instead of the launcher app icon. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_PROGRESS:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is the progress value supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setProgress(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_PROGRESS_INDETERMINATE:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: whether the progress bar is indeterminate, supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setProgress(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_PROGRESS_MAX:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is the maximum value supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setProgress(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_REMOTE_INPUT_DRAFT:kotlin.String` If the notification contained an unsent draft for a RemoteInput when the user clicked on it, we're adding the draft as a String extra to the `https://developer.android.com/reference/kotlin/android/app/Notification#contentIntent:android.app.PendingIntent` using this key. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_REMOTE_INPUT_HISTORY:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is the remote input history, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setRemoteInputHistory(kotlin.Array)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_REQUEST_PROMOTED_ONGOING:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: If provided, should contain a boolean indicating whether the notification is requesting promoted treatment. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_SELF_DISPLAY_NAME:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the username to be displayed for all messages sent by the user including direct replies `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle` notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_SHOW_BIG_PICTURE_WHEN_COLLAPSED:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is a boolean to indicate that the `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle#bigPicture(android.graphics.Bitmap)` is to be shown in the collapsed state of a `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle` notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_SHOW_CHRONOMETER:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: whether `https://developer.android.com/reference/kotlin/android/app/Notification#when:kotlin.Long` should be shown as a count-up timer (specifically a `https://developer.android.com/reference/kotlin/android/widget/Chronometer.html#`) instead of a timestamp, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setUsesChronometer(kotlin.Boolean)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_SHOW_WHEN:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: whether `https://developer.android.com/reference/kotlin/android/app/Notification#when:kotlin.Long` should be shown, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setShowWhen(kotlin.Boolean)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_SMALL_ICON:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is the resource ID of the notification's main small icon, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setSmallIcon(kotlin.Int)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_SUB_TEXT:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is a third line of text, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setSubText(kotlin.CharSequence)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_SUMMARY_TEXT:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is a line of summary information intended to be shown alongside expanded notifications, as supplied to (e.g.) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_TEMPLATE:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: A string representing the name of the specific `https://developer.android.com/reference/kotlin/android/app/Notification.Style` used to create this notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_TEXT:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is the main text payload, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setContentText(kotlin.CharSequence)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_TEXT_LINES:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: An array of CharSequences to show in `https://developer.android.com/reference/kotlin/android/app/Notification.InboxStyle` expanded notifications, each of which was supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.InboxStyle#addLine(kotlin.CharSequence)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_TITLE:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is the title of the notification, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setContentTitle(kotlin.CharSequence)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_TITLE_BIG:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is the title of the notification when shown in expanded form, e. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_VERIFICATION_ICON:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the icon to be displayed as a verification status of the caller on a `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_VERIFICATION_TEXT:kotlin.String` `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the text to be displayed as a verification status of the caller on a `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_AUTO_CANCEL:kotlin.Int` Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set if the notification should be canceled when it is clicked by the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_BUBBLE:kotlin.Int` Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set by the system if this notification is showing as a bubble. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_FOREGROUND_SERVICE:kotlin.Int` Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set if this notification represents a currently running service. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_GROUP_SUMMARY:kotlin.Int` Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set if this notification is the group summary for a group of notifications. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_HIGH_PRIORITY:kotlin.Int` Obsolete flag indicating high-priority notifications; use the priority field instead. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_INSISTENT:kotlin.Int` Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that if set, the audio will be repeated until the notification is cancelled or the notification window is opened. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_LOCAL_ONLY:kotlin.Int` Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set if this notification is relevant to the current device only and it is not recommended that it bridge to other devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_NO_CLEAR:kotlin.Int` Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set if the notification should not be canceled when the user clicks the Clear all button. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_ONGOING_EVENT:kotlin.Int` Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set if this notification is in reference to something that is ongoing, like a phone call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_ONLY_ALERT_ONCE:kotlin.Int` Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set if you would only like the sound, vibrate and ticker to be played if the notification was not already showing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_PROMOTED_ONGOING:kotlin.Int` Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set by the system if this notification is a promoted ongoing notification, both because it `https://developer.android.com/reference/kotlin/android/app/Notification#hasPromotableCharacteristics()` and the user has not disabled the feature for this app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_SHOW_LIGHTS:kotlin.Int` Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set if you want the LED on for this notification. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#FOREGROUND_SERVICE_DEFAULT:kotlin.Int` If the Notification associated with starting a foreground service has been built using `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setForegroundServiceBehavior(kotlin.Int)` with this behavior, display of the notification will usually be suppressed for a short time to avoid visual disturbances to the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#FOREGROUND_SERVICE_DEFERRED:kotlin.Int` If the Notification associated with starting a foreground service has been built using `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setForegroundServiceBehavior(kotlin.Int)` with this behavior, display of the notification will usually be suppressed for a short time to avoid visual disturbances to the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#FOREGROUND_SERVICE_IMMEDIATE:kotlin.Int` If the Notification associated with starting a foreground service has been built using `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setForegroundServiceBehavior(kotlin.Int)` with this behavior, display of the notification will be immediate even if the default behavior would be to defer visibility for a short time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#GROUP_ALERT_ALL:kotlin.Int` Constant for `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setGroupAlertBehavior(kotlin.Int)`, meaning that all notifications in a group with sound or vibration ought to make sound or vibrate (respectively), so this notification will not be muted when it is in a group. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#GROUP_ALERT_CHILDREN:kotlin.Int` Constant for `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setGroupAlertBehavior(kotlin.Int)`, meaning that the summary notification in a group should be silenced (no sound or vibration) even if they are posted to a `https://developer.android.com/reference/kotlin/android/app/NotificationChannel` that has sound and/or vibration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#GROUP_ALERT_SUMMARY:kotlin.Int` Constant for `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setGroupAlertBehavior(kotlin.Int)`, meaning that all children notification in a group should be silenced (no sound or vibration) even if they are posted to a `https://developer.android.com/reference/kotlin/android/app/NotificationChannel` that has sound and/or vibration. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#INTENT_CATEGORY_NOTIFICATION_PREFERENCES:kotlin.String` An activity that provides a user interface for adjusting notification preferences for its containing application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#PRIORITY_DEFAULT:kotlin.Int` Default notification `https://developer.android.com/reference/kotlin/android/app/Notification#priority:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#PRIORITY_HIGH:kotlin.Int` Higher `https://developer.android.com/reference/kotlin/android/app/Notification#priority:kotlin.Int`, for more important notifications or alerts. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#PRIORITY_LOW:kotlin.Int` Lower `https://developer.android.com/reference/kotlin/android/app/Notification#priority:kotlin.Int`, for items that are less important. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#PRIORITY_MAX:kotlin.Int` Highest `https://developer.android.com/reference/kotlin/android/app/Notification#priority:kotlin.Int`, for your application's most important items that require the user's prompt attention or input. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#PRIORITY_MIN:kotlin.Int` Lowest `https://developer.android.com/reference/kotlin/android/app/Notification#priority:kotlin.Int`; these items might not be shown to the user except under special circumstances, such as detailed notification logs. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#SEMANTIC_STYLE_CAUTION:kotlin.Int` This value is used to annotate an element as indicating caution, moderate urgency, tardiness, or another "intermediate" value on the semantic hierarchy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#SEMANTIC_STYLE_DANGER:kotlin.Int` This value is used to annotate an element as indicating danger, extreme urgency or lateness, or another "extreme" value on the semantic hierarchy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#SEMANTIC_STYLE_INFO:kotlin.Int` This value is used to annotate an element as indicating information that should stand out from other content, but which doesn't fall on a scale or hierarchy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#SEMANTIC_STYLE_SAFE:kotlin.Int` This value is used to annotate an element as indicating safety, non-urgency, timeliness, or another "mild" value on the semantic hierarchy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#SEMANTIC_STYLE_UNSPECIFIED:kotlin.Int` This is the default value for semantic style, signaling no particular semantics. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#STREAM_DEFAULT:kotlin.Int` Use this constant as the value for audioStreamType to request that the default stream type for notifications be used. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#VISIBILITY_PRIVATE:kotlin.Int` Notification visibility: Show this notification on all lockscreens, but conceal sensitive or private information on secure lockscreens. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#VISIBILITY_PUBLIC:kotlin.Int` Notification visibility: Show this notification in its entirety on all lockscreens and while screen sharing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#VISIBILITY_SECRET:kotlin.Int` Notification visibility: Do not reveal any part of this notification on a secure lockscreen or while screen sharing. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/Notification#Notification()()` Constructs a Notification object with default values. |
| `https://developer.android.com/reference/kotlin/android/app/Notification#Notification(android.os.Parcel)(parcel: https://developer.android.com/reference/kotlin/android/os/Parcel.html#!)` Unflatten the notification from a parcel. |
| `https://developer.android.com/reference/kotlin/android/app/Notification#Notification(kotlin.Int,%20kotlin.CharSequence,%20kotlin.Long)(icon: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, tickerText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, when: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Constructs a Notification object with the information needed to have a status bar icon without the standard expanded view. |

| Public methods ||
|---|---|
| open [Notification](https://developer.android.com/reference/kotlin/android/app/Notification#)! | `https://developer.android.com/reference/kotlin/android/app/Notification#clone()()` Creates and returns a copy of this object. |
| open static [Annotation](https://developer.android.com/reference/kotlin/android/text/Annotation.html#) | `https://developer.android.com/reference/kotlin/android/app/Notification#createSemanticStyleAnnotation(kotlin.Int)(semanticStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs an `https://developer.android.com/reference/kotlin/android/text/Annotation.html#` that can be used to span text in a `https://developer.android.com/reference/kotlin/android/text/Spanned.html#` `https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#` in some Notification text fields, and which may then be converted into styling of that section of text in order to indicate the semantic style. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Pair](https://developer.android.com/reference/kotlin/android/util/Pair.html#)\< [RemoteInput](https://developer.android.com/reference/kotlin/android/app/RemoteInput)!, [Notification.Action](https://developer.android.com/reference/kotlin/android/app/Notification.Action)!\>? | `https://developer.android.com/reference/kotlin/android/app/Notification#findRemoteInputActionPair(kotlin.Boolean)(requiresFreeform: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Finds and returns a remote input and its corresponding action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#getAllowSystemGeneratedContextualActions()()` Returns whether the platform is allowed (by the app developer) to generate contextual actions for this notification. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#getBadgeIconType()()` Returns what icon should be shown for this notification if it is being displayed in a Launcher that supports badging. |
| open [Notification.BridgedNotificationMetadata](https://developer.android.com/reference/kotlin/android/app/Notification.BridgedNotificationMetadata)? | `https://developer.android.com/reference/kotlin/android/app/Notification#getBridgedNotificationMetadata()()` Returns the metadata associated with a notification originating on another device. |
| open [Notification.BubbleMetadata](https://developer.android.com/reference/kotlin/android/app/Notification.BubbleMetadata)? | `https://developer.android.com/reference/kotlin/android/app/Notification#getBubbleMetadata()()` Returns the bubble metadata that will be used to display app content in a floating window over the existing foreground activity. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/app/Notification#getChannelId()()` Returns the id of the channel this notification posts to. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Notification.Action](https://developer.android.com/reference/kotlin/android/app/Notification.Action)!\> | `https://developer.android.com/reference/kotlin/android/app/Notification#getContextualActions()()` Returns the actions that are contextual (that is, suggested because of the content of the notification) out of the actions in this notification. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/app/Notification#getGroup()()` Get the key used to group this notification into a cluster or stack with other notifications on devices which support such rendering. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#getGroupAlertBehavior()()` Returns which type of notifications in a group are responsible for audibly alerting the user. |
| open [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)! | `https://developer.android.com/reference/kotlin/android/app/Notification#getLargeIcon()()` The large icon shown in this notification's content view. |
| open [LocusId](https://developer.android.com/reference/kotlin/android/content/LocusId.html#)? | `https://developer.android.com/reference/kotlin/android/app/Notification#getLocusId()()` Gets the `https://developer.android.com/reference/kotlin/android/content/LocusId.html#` associated with this notification. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/app/Notification#getSettingsText()()` Returns the settings text provided to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setSettingsText(kotlin.CharSequence)`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/app/Notification#getShortCriticalText()()` Returns the very short text summarizing the most critical information contained in the notification, or `null` if this field was not set. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/app/Notification#getShortcutId()()` Returns the `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.html#getId()` that this notification supersedes, if any. |
| open [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)! | `https://developer.android.com/reference/kotlin/android/app/Notification#getSmallIcon()()` The small icon representing this notification in the status bar. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/app/Notification#getSortKey()()` Get a sort key that orders this notification among other notifications from the same package. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#getTimeoutAfter()()` Returns the duration from posting after which this notification should be canceled by the system, if it's not canceled already. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#hasImage()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#hasPromotableCharacteristics()()` Returns whether the notification has all the characteristics that make it eligible for `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_PROMOTED_ONGOING:kotlin.Int`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#hasSummarizedContent()()` Returns whether this notification contains computationally summarized text. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#isRequestPromotedOngoing()()` Returns whether this notification has requested to be a promoted ongoing notification. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#writeToParcel(android.os.Parcel,%20kotlin.Int)(parcel: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this notification into a parcel. |

| Properties ||
|---|---|
| static [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes.html#)! | `https://developer.android.com/reference/kotlin/android/app/Notification#AUDIO_ATTRIBUTES_DEFAULT:android.media.AudioAttributes` The default value of `https://developer.android.com/reference/kotlin/android/app/Notification#audioAttributes:android.media.AudioAttributes`. |
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [Notification](https://developer.android.com/reference/kotlin/android/app/Notification#)!\> | `https://developer.android.com/reference/kotlin/android/app/Notification#CREATOR:android.os.Parcelable.Creator` Parcelable. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Notification.Action](https://developer.android.com/reference/kotlin/android/app/Notification.Action)!\>! | `https://developer.android.com/reference/kotlin/android/app/Notification#actions:kotlin.Array` Array of all `https://developer.android.com/reference/kotlin/android/app/Notification.Action` structures attached to this notification by `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#addAction(kotlin.Int,%20kotlin.CharSequence,%20android.app.PendingIntent)`. |
| [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes.html#)! | `https://developer.android.com/reference/kotlin/android/app/Notification#audioAttributes:android.media.AudioAttributes` The `https://developer.android.com/reference/kotlin/android/media/AudioAttributes.html#` to use when playing the sound. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#audioStreamType:kotlin.Int` The audio stream type to use when playing the sound. |
| [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#)! | `https://developer.android.com/reference/kotlin/android/app/Notification#bigContentView:android.widget.RemoteViews` A large-format version of `https://developer.android.com/reference/kotlin/android/app/Notification#contentView:android.widget.RemoteViews`, giving the Notification an opportunity to show more detail when expanded. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/app/Notification#category:kotlin.String` One of the predefined notification categories (see the `CATEGORY_*` constants) that best describes this Notification. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#color:kotlin.Int` Accent color (an ARGB integer like the constants in `https://developer.android.com/reference/kotlin/android/graphics/Color.html#`) to be applied by the standard Style templates when presenting this notification. |
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent)! | `https://developer.android.com/reference/kotlin/android/app/Notification#contentIntent:android.app.PendingIntent` The intent to execute when the expanded status entry is clicked. |
| [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#)! | `https://developer.android.com/reference/kotlin/android/app/Notification#contentView:android.widget.RemoteViews` The view that will represent this notification in the notification list (which is pulled down from the status bar). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#defaults:kotlin.Int` Specifies which values should be taken from the defaults. |
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent)! | `https://developer.android.com/reference/kotlin/android/app/Notification#deleteIntent:android.app.PendingIntent` The intent to execute when the notification is explicitly dismissed by the user, either with the "Clear All" button or by swiping it away individually. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` Additional semantic data to be carried around with this Notification. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` <br /> |
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent)! | `https://developer.android.com/reference/kotlin/android/app/Notification#fullScreenIntent:android.app.PendingIntent` An intent to launch instead of posting the notification to the status bar. |
| [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#)! | `https://developer.android.com/reference/kotlin/android/app/Notification#headsUpContentView:android.widget.RemoteViews` A medium-format version of `https://developer.android.com/reference/kotlin/android/app/Notification#contentView:android.widget.RemoteViews`, providing the Notification an opportunity to add action buttons to contentView. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#icon:kotlin.Int` The resource id of a drawable to use as the icon in the status bar. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#iconLevel:kotlin.Int` If the icon in the status bar is to have more than one level, you can set this. |
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)! | `https://developer.android.com/reference/kotlin/android/app/Notification#largeIcon:android.graphics.Bitmap` A large bitmap to be shown in the notification content area. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#ledARGB:kotlin.Int` The color of the led. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#ledOffMS:kotlin.Int` The number of milliseconds for the LED to be off while it's flashing. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#ledOnMS:kotlin.Int` The number of milliseconds for the LED to be on while it's flashing. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#number:kotlin.Int` The number of events that this notification represents. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#priority:kotlin.Int` Relative priority for this notification. |
| [Notification](https://developer.android.com/reference/kotlin/android/app/Notification#)! | `https://developer.android.com/reference/kotlin/android/app/Notification#publicVersion:android.app.Notification` Replacement version of this notification whose content will be shown in an insecure context such as atop a secure keyguard. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | `https://developer.android.com/reference/kotlin/android/app/Notification#sound:android.net.Uri` The sound to play. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/app/Notification#tickerText:kotlin.CharSequence` Text that summarizes this notification for accessibility services. |
| [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#)! | `https://developer.android.com/reference/kotlin/android/app/Notification#tickerView:android.widget.RemoteViews` Formerly, a view showing the `https://developer.android.com/reference/kotlin/android/app/Notification#tickerText:kotlin.CharSequence`. |
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)! | `https://developer.android.com/reference/kotlin/android/app/Notification#vibrate:kotlin.LongArray` The pattern with which to vibrate. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#visibility:kotlin.Int` Sphere of visibility of this notification, which affects how and when the SystemUI reveals the notification's presence and contents in untrusted situations (namely, on the secure lockscreen and during screen sharing). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/Notification#when:kotlin.Long` A timestamp related to this notification, in milliseconds since the epoch. |

## Constants

### ACTION_BRIDGED_NOTIFICATION_PREFERENCES

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_BRIDGED_NOTIFICATION_PREFERENCES: String
```

An activity that provides a user interface for adjusting notification preferences for its bridged notification which originated on another device.

 Value: "android.app.action.BRIDGED_NOTIFICATION_PREFERENCES"

### BADGE_ICON_LARGE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BADGE_ICON_LARGE: Int
```

If this notification is being shown as a badge, use the `https://developer.android.com/reference/kotlin/android/app/Notification#getLargeIcon()` to represent this notification.

 Value: 2

### BADGE_ICON_NONE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BADGE_ICON_NONE: Int
```

If this notification is being shown as a badge, always show as a number.

 Value: 0

### BADGE_ICON_SMALL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BADGE_ICON_SMALL: Int
```

If this notification is being shown as a badge, use the `https://developer.android.com/reference/kotlin/android/app/Notification#getSmallIcon()` to represent this notification.

 Value: 1

### CATEGORY_ALARM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_ALARM: String
```

Notification category: alarm or timer.

 Value: "alarm"

### CATEGORY_CALL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_CALL: String
```

Notification category: incoming call (voice or video) or similar synchronous communication request.

 Value: "call"

### CATEGORY_EMAIL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_EMAIL: String
```

Notification category: asynchronous bulk message (email).

 Value: "email"

### CATEGORY_ERROR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_ERROR: String
```

Notification category: error in background operation or authentication status.

 Value: "err"

### CATEGORY_EVENT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_EVENT: String
```

Notification category: calendar event.

 Value: "event"

### CATEGORY_LOCATION_SHARING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_LOCATION_SHARING: String
```

Notification category: temporarily sharing location.

 Value: "location_sharing"

### CATEGORY_MESSAGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_MESSAGE: String
```

Notification category: incoming direct message (SMS, instant message, etc.).

 Value: "msg"

### CATEGORY_MISSED_CALL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_MISSED_CALL: String
```

Notification category: missed call.

 Value: "missed_call"

### CATEGORY_NAVIGATION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_NAVIGATION: String
```

Notification category: map turn-by-turn navigation.

 Value: "navigation"

### CATEGORY_PROGRESS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_PROGRESS: String
```

Notification category: progress of a long-running background operation.

 Value: "progress"

### CATEGORY_PROMO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_PROMO: String
```

Notification category: promotion or advertisement.

 Value: "promo"

### CATEGORY_RECOMMENDATION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_RECOMMENDATION: String
```

Notification category: a specific, timely recommendation for a single thing. For example, a news app might want to recommend a news story it believes the user will want to read next.

 Value: "recommendation"

### CATEGORY_REMINDER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_REMINDER: String
```

Notification category: user-scheduled reminder.

 Value: "reminder"

### CATEGORY_SERVICE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_SERVICE: String
```

Notification category: indication of running background service.

 Value: "service"

### CATEGORY_SOCIAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_SOCIAL: String
```

Notification category: social network or sharing update.

 Value: "social"

### CATEGORY_STATUS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_STATUS: String
```

Notification category: ongoing information about device or contextual status.

 Value: "status"

### CATEGORY_STOPWATCH

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_STOPWATCH: String
```

Notification category: running stopwatch.

 Value: "stopwatch"

### CATEGORY_SYSTEM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_SYSTEM: String
```

Notification category: system or device status update. Reserved for system use.

 Value: "sys"

### CATEGORY_TRANSPORT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_TRANSPORT: String
```

Notification category: media transport control for playback.

 Value: "transport"

### CATEGORY_VOICEMAIL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_VOICEMAIL: String
```

Notification category: voicemail.

 Value: "voicemail"

### CATEGORY_WORKOUT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_WORKOUT: String
```

Notification category: tracking a user's workout.

 Value: "workout"

### COLOR_DEFAULT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_DEFAULT: Int
```

Special value of `https://developer.android.com/reference/kotlin/android/app/Notification#color:kotlin.Int` telling the system not to decorate this element with any special color (but instead use default system colors).

 Value: 0

### DEFAULT_ALL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEFAULT_ALL: Int
```

Use all default values (where applicable).

 Value: -1

### DEFAULT_LIGHTS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEFAULT_LIGHTS: Int
```

Use the default notification lights. This will ignore the `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_SHOW_LIGHTS:kotlin.Int` bit, and `https://developer.android.com/reference/kotlin/android/app/Notification#ledARGB:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/Notification#ledOffMS:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/app/Notification#ledOnMS:kotlin.Int`.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Notification#defaults:kotlin.Int`

### DEFAULT_SOUND

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEFAULT_SOUND: Int
```

Use the default notification sound. This will ignore any given `https://developer.android.com/reference/kotlin/android/app/Notification#sound:android.net.Uri`.

A notification that is noisy is more likely to be presented as a heads-up notification.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Notification#defaults:kotlin.Int`

### DEFAULT_VIBRATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEFAULT_VIBRATE: Int
```

Use the default notification vibrate. This will ignore any given `https://developer.android.com/reference/kotlin/android/app/Notification#vibrate:kotlin.LongArray`. Using phone vibration requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#VIBRATE:kotlin.String` permission.

A notification that vibrates is more likely to be presented as a heads-up notification.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Notification#defaults:kotlin.Int`

### EXTRA_ANSWER_COLOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ANSWER_COLOR: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the color used as a hint for the Answer action button of a `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification. This extra is a `ColorInt`.

 Value: "android.answerColor"

### EXTRA_ANSWER_INTENT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ANSWER_INTENT: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the intent to be sent when the users answers a `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification. This extra is a `https://developer.android.com/reference/kotlin/android/app/PendingIntent`.

 Value: "android.answerIntent"

### EXTRA_AUDIO_CONTENTS_URI

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_AUDIO_CONTENTS_URI: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the audio contents of this notification.

This is for use when rendering the notification on an audio-focused interface; the audio contents are a complete sound sample that contains the contents/body of the notification. This may be used in substitute of a Text-to-Speech reading of the notification. For example if the notification represents a voice message this should point to the audio of that message.

The data stored under this key should be a String representation of a Uri that contains the audio contents in one of the following formats: WAV, PCM 16-bit, AMR-WB.

This extra is unnecessary if you are using `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle` since each `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle.Message` has a field for holding data URI. That field can be used for audio. See `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle.Message#setData(kotlin.String,%20android.net.Uri)`.

Example usage:

```kotlin
<code>Notification.Builder myBuilder = (build your Notification as normal);
  myBuilder.getExtras().putString(EXTRA_AUDIO_CONTENTS_URI, myAudioUri.toString());
  </code>
```

 Value: "android.audioContents"

### EXTRA_BACKGROUND_IMAGE_URI

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_BACKGROUND_IMAGE_URI: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: flat `https://developer.android.com/reference/kotlin/java/lang/String.html#` representation of a `https://developer.android.com/reference/kotlin/android/content/ContentUris.html#` pointing to an image that can be displayed in the background when the notification is selected. Used on television platforms. The URI must point to an image stream suitable for passing into `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.html#decodeStream(java.io.InputStream)`; all other content types will be ignored.

 Value: "android.backgroundImageUri"

### EXTRA_BIG_TEXT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_BIG_TEXT: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is the longer text shown in the expanded form of a `https://developer.android.com/reference/kotlin/android/app/Notification.BigTextStyle` notification, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.BigTextStyle#bigText(kotlin.CharSequence)`.

 Value: "android.bigText"

### EXTRA_CALL_IS_VIDEO

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CALL_IS_VIDEO: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: whether the `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification is for a call that will activate video when answered. This extra is a boolean.

 Value: "android.callIsVideo"

### EXTRA_CALL_PERSON

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CALL_PERSON: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the person to be displayed as calling for the `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification. This extra is a `https://developer.android.com/reference/kotlin/android/app/Person`.

 Value: "android.callPerson"

### EXTRA_CALL_TYPE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CALL_TYPE: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the type of call represented by the `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification. This extra is an int.

 Value: "android.callType"

### EXTRA_CHANNEL_GROUP_ID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CHANNEL_GROUP_ID: String
```

Optional extra for `https://developer.android.com/reference/kotlin/android/app/Notification#INTENT_CATEGORY_NOTIFICATION_PREFERENCES:kotlin.String`. If provided, will contain a `https://developer.android.com/reference/kotlin/android/app/NotificationChannelGroup#getId()` that can be used to narrow down what settings should be shown in the target app.

 Value: "android.intent.extra.CHANNEL_GROUP_ID"

### EXTRA_CHANNEL_ID

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CHANNEL_ID: String
```

Optional extra for `https://developer.android.com/reference/kotlin/android/app/Notification#INTENT_CATEGORY_NOTIFICATION_PREFERENCES:kotlin.String`. If provided, will contain a `https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getId()` that can be used to narrow down what settings should be shown in the target app.

 Value: "android.intent.extra.CHANNEL_ID"

### EXTRA_CHRONOMETER_COUNT_DOWN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CHRONOMETER_COUNT_DOWN: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: whether the chronometer set on the notification should count down instead of counting up. Is only relevant if key `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_SHOW_CHRONOMETER:kotlin.String` is present. This extra is a boolean. The default is `false`.

 Value: "android.chronometerCountDown"

### EXTRA_COLORIZED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_COLORIZED: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: whether the notification should be colorized as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setColorized(kotlin.Boolean)`.

 Value: "android.colorized"

### EXTRA_COMPACT_ACTIONS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_COMPACT_ACTIONS: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the indices of actions to be shown in the compact view, as supplied to (e.g.) `https://developer.android.com/reference/kotlin/android/app/Notification.MediaStyle#setShowActionsInCompactView(kotlin.Int)`.

 Value: "android.compactActions"

### EXTRA_CONVERSATION_TITLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CONVERSATION_TITLE: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: a `https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#` to be displayed as the title to a conversation represented by a `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle`

 Value: "android.conversationTitle"

### EXTRA_DECLINE_COLOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DECLINE_COLOR: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the color used as a hint for the Decline or Hang Up action button of a `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification. This extra is a `ColorInt`.

 Value: "android.declineColor"

### EXTRA_DECLINE_INTENT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DECLINE_INTENT: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the intent to be sent when the users declines a `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification. This extra is a `https://developer.android.com/reference/kotlin/android/app/PendingIntent`.

 Value: "android.declineIntent"

### EXTRA_HANG_UP_INTENT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_HANG_UP_INTENT: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the intent to be sent when the users hangs up a `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification. This extra is a `https://developer.android.com/reference/kotlin/android/app/PendingIntent`.

 Value: "android.hangUpIntent"

### EXTRA_HISTORIC_MESSAGES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_HISTORIC_MESSAGES: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: an array of `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle#addHistoricMessage(android.app.Notification.MessagingStyle.Message)` `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle.Message` bundles provided by a `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle` notification. This extra is a parcelable array of bundles.

 Value: "android.messages.historic"

### EXTRA_INFO_TEXT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_INFO_TEXT: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is a small piece of additional text as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setContentInfo(kotlin.CharSequence)`.

 Value: "android.infoText"

### EXTRA_IS_GROUP_CONVERSATION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_IS_GROUP_CONVERSATION: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: whether the `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle` notification represents a group conversation.

 Value: "android.isGroupConversation"

### EXTRA_LARGE_ICON

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_LARGE_ICON: String
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/Notification#getLargeIcon()`, which supports a wider variety of icon sources.*

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is a bitmap to be used instead of the small icon when showing the notification payload, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setLargeIcon(android.graphics.Bitmap)`.

 Value: "android.largeIcon"

### EXTRA_LARGE_ICON_BIG

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_LARGE_ICON_BIG: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is a bitmap to be used instead of the one from `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setLargeIcon(android.graphics.Bitmap)` when the notification is shown in its expanded form, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle#bigLargeIcon(android.graphics.Bitmap)`.

 Value: "android.largeIcon.big"

### EXTRA_MEDIA_SESSION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MEDIA_SESSION: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: A `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token.html#` associated with a `https://developer.android.com/reference/kotlin/android/app/Notification.MediaStyle` notification.

 Value: "android.mediaSession"

### EXTRA_MESSAGES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MESSAGES: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: an array of `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle.Message` bundles provided by a `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle` notification. This extra is a parcelable array of bundles.

 Value: "android.messages"

### EXTRA_MESSAGING_PERSON

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MESSAGING_PERSON: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the person to be displayed for all messages sent by the user including direct replies `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle` notification. This extra is a `https://developer.android.com/reference/kotlin/android/app/Person`.

 Value: "android.messagingUser"

### EXTRA_NOTIFICATION_ID

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NOTIFICATION_ID: String
```

Optional extra for `https://developer.android.com/reference/kotlin/android/app/Notification#INTENT_CATEGORY_NOTIFICATION_PREFERENCES:kotlin.String`. If provided, will contain the id provided to `https://developer.android.com/reference/kotlin/android/app/NotificationManager#notify(kotlin.String,%20kotlin.Int,%20android.app.Notification)` that can be used to narrow down what settings should be shown in the target app.

 Value: "android.intent.extra.NOTIFICATION_ID"

### EXTRA_NOTIFICATION_TAG

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NOTIFICATION_TAG: String
```

Optional extra for `https://developer.android.com/reference/kotlin/android/app/Notification#INTENT_CATEGORY_NOTIFICATION_PREFERENCES:kotlin.String`. If provided, will contain the tag provided to `https://developer.android.com/reference/kotlin/android/app/NotificationManager#notify(kotlin.String,%20kotlin.Int,%20android.app.Notification)` that can be used to narrow down what settings should be shown in the target app.

 Value: "android.intent.extra.NOTIFICATION_TAG"

### EXTRA_PEOPLE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PEOPLE: String
```

**Deprecated:** *the actual objects are now in `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_PEOPLE_LIST:kotlin.String`*

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: A String array containing the people that this notification relates to, each of which was supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#addPerson(kotlin.String)`.

 Value: "android.people"

### EXTRA_PEOPLE_LIST

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PEOPLE_LIST: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: An arrayList of `https://developer.android.com/reference/kotlin/android/app/Person` objects containing the people that this notification relates to.

 Value: "android.people.list"

### EXTRA_PICTURE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PICTURE: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is a bitmap to be shown in `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle` expanded notifications, supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle#bigPicture(android.graphics.Bitmap)`.

 Value: "android.picture"

### EXTRA_PICTURE_CONTENT_DESCRIPTION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PICTURE_CONTENT_DESCRIPTION: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is a content description of the big picture supplied from `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle#bigPicture(android.graphics.Bitmap)`, supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle#setContentDescription(kotlin.CharSequence)`.

 Value: "android.pictureContentDescription"

### EXTRA_PICTURE_ICON

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PICTURE_ICON: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is an `https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#` of an image to be shown in `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle` expanded notifications, supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle#bigPicture(android.graphics.drawable.Icon)`.

 Value: "android.pictureIcon"

### EXTRA_PREFER_SMALL_ICON

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PREFER_SMALL_ICON: String
```

A boolean for `https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` requesting that the notification card show the small icon instead of the launcher app icon.

 Value: "android.app.preferSmallIcon"

### EXTRA_PROGRESS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PROGRESS: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is the progress value supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setProgress(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean)`.

 Value: "android.progress"

### EXTRA_PROGRESS_INDETERMINATE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PROGRESS_INDETERMINATE: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: whether the progress bar is indeterminate, supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setProgress(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean)`.

 Value: "android.progressIndeterminate"

### EXTRA_PROGRESS_MAX

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PROGRESS_MAX: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is the maximum value supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setProgress(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean)`.

 Value: "android.progressMax"

### EXTRA_REMOTE_INPUT_DRAFT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_REMOTE_INPUT_DRAFT: String
```

If the notification contained an unsent draft for a RemoteInput when the user clicked on it, we're adding the draft as a String extra to the `https://developer.android.com/reference/kotlin/android/app/Notification#contentIntent:android.app.PendingIntent` using this key.

Apps may use this extra to prepopulate text fields in the app, where the user usually sends messages.

 Value: "android.remoteInputDraft"

### EXTRA_REMOTE_INPUT_HISTORY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_REMOTE_INPUT_HISTORY: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is the remote input history, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setRemoteInputHistory(kotlin.Array)`.

Apps can fill this through `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setRemoteInputHistory(kotlin.Array)` with the most recent inputs that have been sent through a `https://developer.android.com/reference/kotlin/android/app/RemoteInput` of this Notification and are expected to clear it once the it is no longer relevant (e.g. for chat notifications once the other party has responded).

The extra with this key is of type `CharSequence[]` and contains the most recent entry at the 0 index, the second most recent at the 1 index, etc.

 Value: "android.remoteInputHistory"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setRemoteInputHistory(kotlin.Array)`

### EXTRA_REQUEST_PROMOTED_ONGOING

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_REQUEST_PROMOTED_ONGOING: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: If provided, should contain a boolean indicating whether the notification is requesting promoted treatment.

 Value: "android.requestPromotedOngoing"

### EXTRA_SELF_DISPLAY_NAME

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SELF_DISPLAY_NAME: String
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_MESSAGING_PERSON:kotlin.String`*

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the username to be displayed for all messages sent by the user including direct replies `https://developer.android.com/reference/kotlin/android/app/Notification.MessagingStyle` notification. This extra is a `https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#`.

 Value: "android.selfDisplayName"

### EXTRA_SHOW_BIG_PICTURE_WHEN_COLLAPSED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SHOW_BIG_PICTURE_WHEN_COLLAPSED: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is a boolean to indicate that the `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle#bigPicture(android.graphics.Bitmap)` is to be shown in the collapsed state of a `https://developer.android.com/reference/kotlin/android/app/Notification.BigPictureStyle` notification. This will replace a `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setLargeIcon(android.graphics.drawable.Icon)` in that state if one was provided.

 Value: "android.showBigPictureWhenCollapsed"

### EXTRA_SHOW_CHRONOMETER

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SHOW_CHRONOMETER: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: whether `https://developer.android.com/reference/kotlin/android/app/Notification#when:kotlin.Long` should be shown as a count-up timer (specifically a `https://developer.android.com/reference/kotlin/android/widget/Chronometer.html#`) instead of a timestamp, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setUsesChronometer(kotlin.Boolean)`.

 Value: "android.showChronometer"

### EXTRA_SHOW_WHEN

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SHOW_WHEN: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: whether `https://developer.android.com/reference/kotlin/android/app/Notification#when:kotlin.Long` should be shown, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setShowWhen(kotlin.Boolean)`.

 Value: "android.showWhen"

### EXTRA_SMALL_ICON

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SMALL_ICON: String
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/Notification#getSmallIcon()`, which supports a wider variety of icon sources.*

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is the resource ID of the notification's main small icon, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setSmallIcon(kotlin.Int)`.

 Value: "android.icon"

### EXTRA_SUB_TEXT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SUB_TEXT: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is a third line of text, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setSubText(kotlin.CharSequence)`.

 Value: "android.subText"

### EXTRA_SUMMARY_TEXT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SUMMARY_TEXT: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is a line of summary information intended to be shown alongside expanded notifications, as supplied to (e.g.) `https://developer.android.com/reference/kotlin/android/app/Notification.BigTextStyle#setSummaryText(kotlin.CharSequence)`.

 Value: "android.summaryText"

### EXTRA_TEMPLATE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_TEMPLATE: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: A string representing the name of the specific `https://developer.android.com/reference/kotlin/android/app/Notification.Style` used to create this notification.

 Value: "android.template"

### EXTRA_TEXT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_TEXT: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is the main text payload, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setContentText(kotlin.CharSequence)`.

 Value: "android.text"

### EXTRA_TEXT_LINES

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_TEXT_LINES: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: An array of CharSequences to show in `https://developer.android.com/reference/kotlin/android/app/Notification.InboxStyle` expanded notifications, each of which was supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.InboxStyle#addLine(kotlin.CharSequence)`.

 Value: "android.textLines"

### EXTRA_TITLE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_TITLE: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is the title of the notification, as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setContentTitle(kotlin.CharSequence)`.

 Value: "android.title"

### EXTRA_TITLE_BIG

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_TITLE_BIG: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: this is the title of the notification when shown in expanded form, e.g. as supplied to `https://developer.android.com/reference/kotlin/android/app/Notification.BigTextStyle#setBigContentTitle(kotlin.CharSequence)`.

 Value: "android.title.big"

### EXTRA_VERIFICATION_ICON

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_VERIFICATION_ICON: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the icon to be displayed as a verification status of the caller on a `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification. This extra is an `https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#`.

 Value: "android.verificationIcon"

### EXTRA_VERIFICATION_TEXT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_VERIFICATION_TEXT: String
```

`https://developer.android.com/reference/kotlin/android/app/Notification#extras:android.os.Bundle` key: the text to be displayed as a verification status of the caller on a `https://developer.android.com/reference/kotlin/android/app/Notification.CallStyle` notification. This extra is a `https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#`.

 Value: "android.verificationText"

### FLAG_AUTO_CANCEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_AUTO_CANCEL: Int
```

Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set if the notification should be canceled when it is clicked by the user.

 Value: 16

### FLAG_BUBBLE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_BUBBLE: Int
```

Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set by the system if this notification is showing as a bubble.

Applications cannot set this flag directly; they should instead call `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setBubbleMetadata(android.app.Notification.BubbleMetadata)` to request that a notification be displayed as a bubble, and then check this flag to see whether that request was honored by the system.

 Value: 4096

### FLAG_FOREGROUND_SERVICE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_FOREGROUND_SERVICE: Int
```

Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set if this notification represents a currently running service. This will normally be set for you by android.app.Service#startForeground.

 Value: 64

### FLAG_GROUP_SUMMARY

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_GROUP_SUMMARY: Int
```

Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set if this notification is the group summary for a group of notifications. Grouped notifications may display in a cluster or stack on devices which support such rendering. Requires a group key also be set using `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setGroup(kotlin.String)`.

 Value: 512

### FLAG_HIGH_PRIORITY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_HIGH_PRIORITY: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/Notification#priority:kotlin.Int` with a positive value.*

Obsolete flag indicating high-priority notifications; use the priority field instead.

 Value: 128

### FLAG_INSISTENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_INSISTENT: Int
```

Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that if set, the audio will be repeated until the notification is cancelled or the notification window is opened.

 Value: 4

### FLAG_LOCAL_ONLY

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_LOCAL_ONLY: Int
```

Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set if this notification is relevant to the current device only and it is not recommended that it bridge to other devices.

 Value: 256

### FLAG_NO_CLEAR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_NO_CLEAR: Int
```

Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set if the notification should not be canceled when the user clicks the Clear all button.

 Value: 32

### FLAG_ONGOING_EVENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_ONGOING_EVENT: Int
```

Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set if this notification is in reference to something that is ongoing, like a phone call. It should not be set if this notification is in reference to something that happened at a particular point in time, like a missed phone call.

 Value: 2

### FLAG_ONLY_ALERT_ONCE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_ONLY_ALERT_ONCE: Int
```

Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set if you would only like the sound, vibrate and ticker to be played if the notification was not already showing.

Note that using this flag will stop any ongoing alerting behaviour such as sound, vibration or blinking notification LED.

 Value: 8

### FLAG_PROMOTED_ONGOING

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_PROMOTED_ONGOING: Int
```

Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set by the system if this notification is a promoted ongoing notification, both because it `https://developer.android.com/reference/kotlin/android/app/Notification#hasPromotableCharacteristics()` and the user has not disabled the feature for this app.

Applications cannot set this flag directly, but the posting app and `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` can read it.

 Value: 262144

### FLAG_SHOW_LIGHTS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SHOW_LIGHTS: Int
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/app/NotificationChannel#shouldShowLights()`.*

Bit to be bitwise-ORed into the `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int` field that should be set if you want the LED on for this notification.

- To turn the LED off, pass 0 in the alpha channel for colorARGB or 0 for both ledOnMS and ledOffMS.
- To turn the LED on, pass 1 for ledOnMS and 0 for ledOffMS.
- To flash the LED, pass the number of milliseconds that it should be on and off to ledOnMS and ledOffMS.

<br />

Since hardware varies, you are not guaranteed that any of the values you pass are honored exactly. Use the system defaults if possible because they will be set to values that work on any given hardware.

The alpha channel must be set for forward compatibility.

 Value: 1

### FOREGROUND_SERVICE_DEFAULT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_DEFAULT: Int
```

If the Notification associated with starting a foreground service has been built using `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setForegroundServiceBehavior(kotlin.Int)` with this behavior, display of the notification will usually be suppressed for a short time to avoid visual disturbances to the user. 
Value is one of the following:

- `https://developer.android.com/reference/kotlin/android/app/Notification#FOREGROUND_SERVICE_DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/Notification#FOREGROUND_SERVICE_IMMEDIATE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/Notification#FOREGROUND_SERVICE_DEFERRED:kotlin.Int`

<br />

 Value: 0

### FOREGROUND_SERVICE_DEFERRED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_DEFERRED: Int
```

If the Notification associated with starting a foreground service has been built using `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setForegroundServiceBehavior(kotlin.Int)` with this behavior, display of the notification will usually be suppressed for a short time to avoid visual disturbances to the user. 
Value is one of the following:

- `https://developer.android.com/reference/kotlin/android/app/Notification#FOREGROUND_SERVICE_DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/Notification#FOREGROUND_SERVICE_IMMEDIATE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/Notification#FOREGROUND_SERVICE_DEFERRED:kotlin.Int`

<br />

 Value: 2

### FOREGROUND_SERVICE_IMMEDIATE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOREGROUND_SERVICE_IMMEDIATE: Int
```

If the Notification associated with starting a foreground service has been built using `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setForegroundServiceBehavior(kotlin.Int)` with this behavior, display of the notification will be immediate even if the default behavior would be to defer visibility for a short time. 
Value is one of the following:

- `https://developer.android.com/reference/kotlin/android/app/Notification#FOREGROUND_SERVICE_DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/Notification#FOREGROUND_SERVICE_IMMEDIATE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/Notification#FOREGROUND_SERVICE_DEFERRED:kotlin.Int`

<br />

 Value: 1

### GROUP_ALERT_ALL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUP_ALERT_ALL: Int
```

Constant for `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setGroupAlertBehavior(kotlin.Int)`, meaning that all notifications in a group with sound or vibration ought to make sound or vibrate (respectively), so this notification will not be muted when it is in a group.

 Value: 0

### GROUP_ALERT_CHILDREN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUP_ALERT_CHILDREN: Int
```

Constant for `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setGroupAlertBehavior(kotlin.Int)`, meaning that the summary notification in a group should be silenced (no sound or vibration) even if they are posted to a `https://developer.android.com/reference/kotlin/android/app/NotificationChannel` that has sound and/or vibration. Use this constant to mute this notification if this notification is a group summary.

For example, you might want to use this constant if only the children notifications in your group have content and the summary is only used to visually group notifications rather than to alert the user that new information is available.

 Value: 2

### GROUP_ALERT_SUMMARY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GROUP_ALERT_SUMMARY: Int
```

Constant for `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setGroupAlertBehavior(kotlin.Int)`, meaning that all children notification in a group should be silenced (no sound or vibration) even if they are posted to a `https://developer.android.com/reference/kotlin/android/app/NotificationChannel` that has sound and/or vibration. Use this constant to mute this notification if this notification is a group child. This must be applied to all children notifications you want to mute.

For example, you might want to use this constant if you post a number of children notifications at once (say, after a periodic sync), and only need to notify the user audibly once.

 Value: 1

### INTENT_CATEGORY_NOTIFICATION_PREFERENCES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTENT_CATEGORY_NOTIFICATION_PREFERENCES: String
```

An activity that provides a user interface for adjusting notification preferences for its containing application.

 Value: "android.intent.category.NOTIFICATION_PREFERENCES"

### PRIORITY_DEFAULT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRIORITY_DEFAULT: Int
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_DEFAULT:kotlin.Int` instead.*

Default notification `https://developer.android.com/reference/kotlin/android/app/Notification#priority:kotlin.Int`. If your application does not prioritize its own notifications, use this value for all notifications.

 Value: 0

### PRIORITY_HIGH

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRIORITY_HIGH: Int
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_HIGH:kotlin.Int` instead.*

Higher `https://developer.android.com/reference/kotlin/android/app/Notification#priority:kotlin.Int`, for more important notifications or alerts. The UI may choose to show these items larger, or at a different position in notification lists, compared with your app's `https://developer.android.com/reference/kotlin/android/app/Notification#PRIORITY_DEFAULT:kotlin.Int` items.

 Value: 1

### PRIORITY_LOW

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRIORITY_LOW: Int
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_LOW:kotlin.Int` instead.*

Lower `https://developer.android.com/reference/kotlin/android/app/Notification#priority:kotlin.Int`, for items that are less important. The UI may choose to show these items smaller, or at a different position in the list, compared with your app's `https://developer.android.com/reference/kotlin/android/app/Notification#PRIORITY_DEFAULT:kotlin.Int` items.

 Value: -1

### PRIORITY_MAX

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRIORITY_MAX: Int
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_HIGH:kotlin.Int` instead.*

Highest `https://developer.android.com/reference/kotlin/android/app/Notification#priority:kotlin.Int`, for your application's most important items that require the user's prompt attention or input.

 Value: 2

### PRIORITY_MIN

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRIORITY_MIN: Int
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/app/NotificationManager#IMPORTANCE_MIN:kotlin.Int` instead.*

Lowest `https://developer.android.com/reference/kotlin/android/app/Notification#priority:kotlin.Int`; these items might not be shown to the user except under special circumstances, such as detailed notification logs.

 Value: -2

### SEMANTIC_STYLE_CAUTION

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SEMANTIC_STYLE_CAUTION: Int
```

This value is used to annotate an element as indicating caution, moderate urgency, tardiness, or another "intermediate" value on the semantic hierarchy.

Caution is generally represented to users by styling the element with a yellow or orange color.

 Value: 3

### SEMANTIC_STYLE_DANGER

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SEMANTIC_STYLE_DANGER: Int
```

This value is used to annotate an element as indicating danger, extreme urgency or lateness, or another "extreme" value on the semantic hierarchy.

Danger is generally represented to users by styling the element with a red color.

 Value: 4

### SEMANTIC_STYLE_INFO

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SEMANTIC_STYLE_INFO: Int
```

This value is used to annotate an element as indicating information that should stand out from other content, but which doesn't fall on a scale or hierarchy. This can be thought of as a more neutral value that may be used in cases where the element is intended to stand out against elements with the other semantic styles -- for example if a `https://developer.android.com/reference/kotlin/android/app/Notification.ProgressStyle` bar uses semantic style to color segments, this style would be appropriate for segments where the semantic hierarchy is unhelpful to the user.

Info is generally represented to users by styling the element with a color (like blue) that is clearly distinct from the colors used for other styles.

 Value: 1

### SEMANTIC_STYLE_SAFE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SEMANTIC_STYLE_SAFE: Int
```

This value is used to annotate an element as indicating safety, non-urgency, timeliness, or another "mild" value on the semantic hierarchy.

Safety is generally represented to users by styling the element with a green color.

 Value: 2

### SEMANTIC_STYLE_UNSPECIFIED

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SEMANTIC_STYLE_UNSPECIFIED: Int
```

This is the default value for semantic style, signaling no particular semantics. An `https://developer.android.com/reference/kotlin/android/text/Annotation.html#` with this style has no effect.

 Value: 0

### STREAM_DEFAULT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STREAM_DEFAULT: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getAudioAttributes()` instead.*

Use this constant as the value for audioStreamType to request that the default stream type for notifications be used. Currently the default stream type is `https://developer.android.com/reference/kotlin/android/media/AudioManager.html#STREAM_NOTIFICATION:kotlin.Int`.

 Value: -1

### VISIBILITY_PRIVATE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VISIBILITY_PRIVATE: Int
```

Notification visibility: Show this notification on all lockscreens, but conceal sensitive or private information on secure lockscreens. Conceal sensitive or private information while screen sharing.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Notification#visibility:kotlin.Int`

### VISIBILITY_PUBLIC

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VISIBILITY_PUBLIC: Int
```

Notification visibility: Show this notification in its entirety on all lockscreens and while screen sharing.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Notification#visibility:kotlin.Int`

### VISIBILITY_SECRET

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VISIBILITY_SECRET: Int
```

Notification visibility: Do not reveal any part of this notification on a secure lockscreen or while screen sharing.

 Value: -1

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Notification#visibility:kotlin.Int`

## Public constructors

### Notification

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Notification()
```

Constructs a Notification object with default values. You should use `https://developer.android.com/reference/kotlin/android/app/Notification.Builder` instead.

### Notification

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Notification(parcel: Parcel!)
```

Unflatten the notification from a parcel.

### Notification

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Notification(
    icon: Int, 
    tickerText: CharSequence!, 
    when: Long)
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/Notification.Builder` instead.*

Constructs a Notification object with the information needed to have a status bar icon without the standard expanded view.

| Parameters ||
|---|---|
| `icon` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the resource id of the icon to put in the status bar |
| `tickerText` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text that flows by in the status bar when the notification first activates |
| `when` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the time to show in the time field, in the `System.currentTimeMillis` timebase |

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Notification!
```

Creates and returns a copy of this object. The precise meaning of "copy" may depend on the class of the object. The general intent is that, for any object `x`, the expression:

```kotlin
x.clone() != x
```
will be true, and that the expression:

```kotlin
x.clone().getClass() == x.getClass()
```
will be `true`, but these are not absolute requirements. While it is typically the case that:

```kotlin
x.clone().equals(x)
```
will be `true`, this is not an absolute requirement.

<br />

By convention, the returned object should be obtained by calling `super.clone`. If a class and all of its superclasses (except `Object`) obey this convention, it will be the case that `x.clone().getClass() == x.getClass()`.

By convention, the object returned by this method should be independent of this object (which is being cloned). To achieve this independence, it may be necessary to modify one or more fields of the object returned by `super.clone` before returning it. Typically, this means copying any mutable objects that comprise the internal "deep structure" of the object being cloned and replacing the references to these objects with references to the copies. If a class contains only primitive fields or references to immutable objects, then it is usually the case that no fields in the object returned by `super.clone` need to be modified.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/Notification#!` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### createSemanticStyleAnnotation

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createSemanticStyleAnnotation(semanticStyle: Int): Annotation
```

Constructs an `https://developer.android.com/reference/kotlin/android/text/Annotation.html#` that can be used to span text in a `https://developer.android.com/reference/kotlin/android/text/Spanned.html#` `https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#` in some Notification text fields, and which may then be converted into styling of that section of text in order to indicate the semantic style. Since Notifications may strip styling, even for semantic styles, it's important that stripping these styles should not distort the meaning of the text.

Semantic style will only be applied to text appearance in notifications that are eligible (e.g. `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_PROMOTED_ONGOING:kotlin.Int` notifications).

| Parameters ||
|---|---|
| `semanticStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/Notification#SEMANTIC_STYLE_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/Notification#SEMANTIC_STYLE_INFO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/Notification#SEMANTIC_STYLE_SAFE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/Notification#SEMANTIC_STYLE_CAUTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/Notification#SEMANTIC_STYLE_DANGER:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/Annotation.html#` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/text/Spannable.html#setSpan(kotlin.Any,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### findRemoteInputActionPair

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun findRemoteInputActionPair(requiresFreeform: Boolean): Pair<RemoteInput!, Notification.Action!>?
```

Finds and returns a remote input and its corresponding action.

| Parameters ||
|---|---|
| `requiresFreeform` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): requires the remoteinput to allow freeform or not |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Pair.html#<https://developer.android.com/reference/kotlin/android/app/RemoteInput!, https://developer.android.com/reference/kotlin/android/app/Notification.Action!>?` | the result pair, `null` if no result is found |

### getAllowSystemGeneratedContextualActions

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAllowSystemGeneratedContextualActions(): Boolean
```

Returns whether the platform is allowed (by the app developer) to generate contextual actions for this notification.

### getBadgeIconType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBadgeIconType(): Int
```

Returns what icon should be shown for this notification if it is being displayed in a Launcher that supports badging. Will be one of `https://developer.android.com/reference/kotlin/android/app/Notification#BADGE_ICON_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/Notification#BADGE_ICON_SMALL:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/app/Notification#BADGE_ICON_LARGE:kotlin.Int`.

### getBridgedNotificationMetadata

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBridgedNotificationMetadata(): Notification.BridgedNotificationMetadata?
```

Returns the metadata associated with a notification originating on another device. A copy of the original notification is sent to this device by a bridging app. This metadata is used for displaying the notification as a bridged notification to the user.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/Notification.BridgedNotificationMetadata?` | the metadata associated with the notification. This value may be `null`. |

### getBubbleMetadata

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBubbleMetadata(): Notification.BubbleMetadata?
```

Returns the bubble metadata that will be used to display app content in a floating window over the existing foreground activity.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/Notification.BubbleMetadata?` | This value may be `null`. |

### getChannelId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChannelId(): String!
```

Returns the id of the channel this notification posts to.

### getContextualActions

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getContextualActions(): MutableList<Notification.Action!>
```

Returns the actions that are contextual (that is, suggested because of the content of the notification) out of the actions in this notification.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/Notification.Action!>` | This value cannot be `null`. |

### getGroup

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGroup(): String!
```

Get the key used to group this notification into a cluster or stack with other notifications on devices which support such rendering.

### getGroupAlertBehavior

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGroupAlertBehavior(): Int
```

Returns which type of notifications in a group are responsible for audibly alerting the user.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/Notification#GROUP_ALERT_ALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/Notification#GROUP_ALERT_CHILDREN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/Notification#GROUP_ALERT_SUMMARY:kotlin.Int` |

### getLargeIcon

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLargeIcon(): Icon!
```

The large icon shown in this notification's content view.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Notification#getLargeIcon()`
- `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setLargeIcon(android.graphics.drawable.Icon)`

### getLocusId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLocusId(): LocusId?
```

Gets the `https://developer.android.com/reference/kotlin/android/content/LocusId.html#` associated with this notification.

Used by the device's intelligence services to correlate objects (such as `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.html#` and `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureContext.html#`) that are correlated.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/LocusId.html#?` | This value may be `null`. |

### getSettingsText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSettingsText(): CharSequence!
```

Returns the settings text provided to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setSettingsText(kotlin.CharSequence)`.

### getShortCriticalText

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShortCriticalText(): String?
```

Returns the very short text summarizing the most critical information contained in the notification, or `null` if this field was not set.

### getShortcutId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShortcutId(): String!
```

Returns the `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo.html#getId()` that this notification supersedes, if any.

Used by some Launchers that display notification content to hide shortcuts that duplicate notifications.

### getSmallIcon

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSmallIcon(): Icon!
```

The small icon representing this notification in the status bar.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#!` | the small icon representing this notification |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Notification#getSmallIcon()`
- `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setSmallIcon(android.graphics.drawable.Icon)`

### getSortKey

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSortKey(): String!
```

Get a sort key that orders this notification among other notifications from the same package. This can be useful if an external sort was already applied and an app would like to preserve this. Notifications will be sorted lexicographically using this value, although providing different priorities in addition to providing sort key may cause this value to be ignored.

This sort key can also be used to order members of a notification group. See `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setGroup(kotlin.String)`.
**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/String.html#compareTo(kotlin.String)`

### getTimeoutAfter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTimeoutAfter(): Long
```

Returns the duration from posting after which this notification should be canceled by the system, if it's not canceled already.

### hasImage

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasImage(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the notification has an image |

### hasPromotableCharacteristics

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasPromotableCharacteristics(): Boolean
```

Returns whether the notification has all the characteristics that make it eligible for `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_PROMOTED_ONGOING:kotlin.Int`. This method does not factor in other criteria such user preferences for the app or channel. If this returns `true`, it does not guarantee that the notification will be assigned `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_PROMOTED_ONGOING:kotlin.Int` by the system, but if this returns `false`, it will not.

### hasSummarizedContent

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasSummarizedContent(): Boolean
```

Returns whether this notification contains computationally summarized text. The OS may choose to display this content instead of the original notification content on some surfaces and may add styling to indicate to the user that this was computationally generated.

### isRequestPromotedOngoing

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isRequestPromotedOngoing(): Boolean
```

Returns whether this notification has requested to be a promoted ongoing notification.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Notification#EXTRA_REQUEST_PROMOTED_ONGOING:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setRequestPromotedOngoing(kotlin.Boolean)`

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
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this notification into a parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### AUDIO_ATTRIBUTES_DEFAULT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_ATTRIBUTES_DEFAULT: AudioAttributes!
```

The default value of `https://developer.android.com/reference/kotlin/android/app/Notification#audioAttributes:android.media.AudioAttributes`.

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<Notification!>
```

Parcelable.Creator that instantiates Notification objects

### actions

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var actions: Array<Notification.Action!>!
```

Array of all `https://developer.android.com/reference/kotlin/android/app/Notification.Action` structures attached to this notification by `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#addAction(kotlin.Int,%20kotlin.CharSequence,%20android.app.PendingIntent)`. Mostly useful for instances of `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` that provide an alternative interface for invoking actions.

### audioAttributes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var audioAttributes: AudioAttributes!
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getAudioAttributes()` instead.*

The `https://developer.android.com/reference/kotlin/android/media/AudioAttributes.html#` to use when playing the sound.

### audioStreamType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var audioStreamType: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/Notification#audioAttributes:android.media.AudioAttributes` instead.*

The audio stream type to use when playing the sound. Should be one of the STREAM_ constants from `https://developer.android.com/reference/kotlin/android/media/AudioManager.html#`.

### bigContentView

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var bigContentView: RemoteViews!
```

**Deprecated:** *Deprecated in Java.*

A large-format version of `https://developer.android.com/reference/kotlin/android/app/Notification#contentView:android.widget.RemoteViews`, giving the Notification an opportunity to show more detail when expanded. The system UI may choose to show this instead of the normal content view at its discretion.

As of N, this field may be null. The expanded notification view is determined by the inputs to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder`; a custom RemoteViews can optionally be supplied with `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setCustomBigContentView(android.widget.RemoteViews)`.

### category

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var category: String!
```

One of the predefined notification categories (see the `CATEGORY_*` constants) that best describes this Notification. May be used by the system for ranking and filtering.

### color

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var color: Int
```

Accent color (an ARGB integer like the constants in `https://developer.android.com/reference/kotlin/android/graphics/Color.html#`) to be applied by the standard Style templates when presenting this notification.

The current template design constructs a colorful header image by overlaying the `https://developer.android.com/reference/kotlin/android/app/Notification#icon:kotlin.Int` image (stenciled in white) atop a field of this color. Alpha components are ignored.

### contentIntent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var contentIntent: PendingIntent!
```

The intent to execute when the expanded status entry is clicked. If this is an activity, it must include the `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` flag, which requires that you take care of task management as described in the [Tasks and Back Stack](https://developer.android.com/guide/topics/fundamentals/tasks-and-back-stack.html) document. In particular, make sure to read the [Start an Activity from a Notification](https://developer.android.com/training/notify-user/navigation) page for the correct ways to launch an application from a notification.

### contentView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var contentView: RemoteViews!
```

**Deprecated:** *Deprecated in Java.*

The view that will represent this notification in the notification list (which is pulled down from the status bar).

As of N, this field may be null. The notification view is determined by the inputs to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder`; a custom RemoteViews can optionally be supplied with `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setCustomContentView(android.widget.RemoteViews)`.

### defaults

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var defaults: Int
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getSound()` and `https://developer.android.com/reference/kotlin/android/app/NotificationChannel#shouldShowLights()` and `https://developer.android.com/reference/kotlin/android/app/NotificationChannel#shouldVibrate()`.*

Specifies which values should be taken from the defaults.

To set, OR the desired from `https://developer.android.com/reference/kotlin/android/app/Notification#DEFAULT_SOUND:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/Notification#DEFAULT_VIBRATE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/Notification#DEFAULT_LIGHTS:kotlin.Int`. For all default values, use `https://developer.android.com/reference/kotlin/android/app/Notification#DEFAULT_ALL:kotlin.Int`.

### deleteIntent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var deleteIntent: PendingIntent!
```

The intent to execute when the notification is explicitly dismissed by the user, either with the "Clear All" button or by swiping it away individually.

This probably shouldn't be launching an activity since several of those will be sent at the same time.

### extras

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var extras: Bundle!
```

Additional semantic data to be carried around with this Notification.

The extras keys defined here are intended to capture the original inputs to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder` APIs, and are intended to be used by `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` implementations to extract detailed information from notification objects.

### flags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var flags: Int
```

### fullScreenIntent

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var fullScreenIntent: PendingIntent!
```

An intent to launch instead of posting the notification to the status bar.

The system UI may choose to display a heads-up notification, instead of launching this intent, while the user is using the device.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setFullScreenIntent(android.app.PendingIntent,%20kotlin.Boolean)`

### headsUpContentView

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var headsUpContentView: RemoteViews!
```

**Deprecated:** *Deprecated in Java.*

A medium-format version of `https://developer.android.com/reference/kotlin/android/app/Notification#contentView:android.widget.RemoteViews`, providing the Notification an opportunity to add action buttons to contentView. At its discretion, the system UI may choose to show this as a heads-up notification, which will pop up so the user can see it without leaving their current activity.

As of N, this field may be null. The heads-up notification view is determined by the inputs to `https://developer.android.com/reference/kotlin/android/app/Notification.Builder`; a custom RemoteViews can optionally be supplied with `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setCustomHeadsUpContentView(android.widget.RemoteViews)`.

### icon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var icon: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setSmallIcon(android.graphics.drawable.Icon)` instead.*

The resource id of a drawable to use as the icon in the status bar.

### iconLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var iconLevel: Int
```

If the icon in the status bar is to have more than one level, you can set this. Otherwise, leave it at its default value of 0.
**See Also**

- `https://developer.android.com/reference/kotlin/android/widget/ImageView.html#setImageLevel(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#setLevel(kotlin.Int)`

### largeIcon

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var largeIcon: Bitmap!
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setLargeIcon(android.graphics.drawable.Icon)` instead.*

A large bitmap to be shown in the notification content area.

### ledARGB

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var ledARGB: Int
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/app/NotificationChannel#shouldShowLights()`.*

The color of the led. The hardware will do its best approximation.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_SHOW_LIGHTS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int`

### ledOffMS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var ledOffMS: Int
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/app/NotificationChannel#shouldShowLights()`.*

The number of milliseconds for the LED to be off while it's flashing. The hardware will do its best approximation.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_SHOW_LIGHTS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int`

### ledOnMS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var ledOnMS: Int
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/app/NotificationChannel#shouldShowLights()`.*

The number of milliseconds for the LED to be on while it's flashing. The hardware will do its best approximation.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Notification#FLAG_SHOW_LIGHTS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/Notification#flags:kotlin.Int`

### number

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var number: Int
```

The number of events that this notification represents. For example, in a new mail notification, this could be the number of unread messages.

The system may or may not use this field to modify the appearance of the notification. Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int`, the number may be displayed as a badge icon in Launchers that support badging.

### priority

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var priority: Int
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getImportance()` instead.*

Relative priority for this notification.

Priority is an indication of how much of the user's valuable attention should be consumed by this notification. Low-priority notifications may be hidden from the user in certain situations, while the user might be interrupted for a higher-priority notification. The system will make a determination about how to interpret this priority when presenting the notification.

A notification that is at least `https://developer.android.com/reference/kotlin/android/app/Notification#PRIORITY_HIGH:kotlin.Int` is more likely to be presented as a heads-up notification.
. 
Value is one of the following:

- `https://developer.android.com/reference/kotlin/android/app/Notification#PRIORITY_DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/Notification#PRIORITY_LOW:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/Notification#PRIORITY_MIN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/Notification#PRIORITY_HIGH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/Notification#PRIORITY_MAX:kotlin.Int`

### publicVersion

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var publicVersion: Notification!
```

Replacement version of this notification whose content will be shown in an insecure context such as atop a secure keyguard. See `https://developer.android.com/reference/kotlin/android/app/Notification#visibility:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/app/Notification#VISIBILITY_PUBLIC:kotlin.Int`.

### sound

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var sound: Uri!
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getSound()`.*

The sound to play.

A notification that is noisy is more likely to be presented as a heads-up notification.

To play the default notification sound, see `https://developer.android.com/reference/kotlin/android/app/Notification#defaults:kotlin.Int`.

### tickerText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var tickerText: CharSequence!
```

Text that summarizes this notification for accessibility services.

As of the L release, this text is no longer shown on screen, but it is still useful to accessibility services (where it serves as an audible announcement of the notification's appearance).
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Notification#tickerView:android.widget.RemoteViews`

### tickerView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var tickerView: RemoteViews!
```

**Deprecated:** *Deprecated in Java.*

Formerly, a view showing the `https://developer.android.com/reference/kotlin/android/app/Notification#tickerText:kotlin.CharSequence`.

No longer displayed in the status bar as of API 21.

### vibrate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var vibrate: LongArray!
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/app/NotificationChannel#getVibrationPattern()`.*

The pattern with which to vibrate.

To vibrate the default pattern, see `https://developer.android.com/reference/kotlin/android/app/Notification#defaults:kotlin.Int`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Vibrator.html#vibrate(kotlin.LongArray,%20kotlin.Int)`

### visibility

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var visibility: Int
```

Sphere of visibility of this notification, which affects how and when the SystemUI reveals the notification's presence and contents in untrusted situations (namely, on the secure lockscreen and during screen sharing).

The default level, `https://developer.android.com/reference/kotlin/android/app/Notification#VISIBILITY_PRIVATE:kotlin.Int`, behaves exactly as notifications have always done on Android: The notification's `https://developer.android.com/reference/kotlin/android/app/Notification#icon:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/app/Notification#tickerText:kotlin.CharSequence` (if available) are shown in all situations, but the contents are only available if the device is unlocked for the appropriate user and there is no active screen sharing session.

A more permissive policy can be expressed by `https://developer.android.com/reference/kotlin/android/app/Notification#VISIBILITY_PUBLIC:kotlin.Int`; such a notification can be read even in an "insecure" context (that is, above a secure lockscreen or while screen sharing with a remote viewer). To modify the public version of this notification---for example, to redact some portions---see `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setPublicVersion(android.app.Notification)`.

Finally, a notification can be made `https://developer.android.com/reference/kotlin/android/app/Notification#VISIBILITY_SECRET:kotlin.Int`, which will suppress its icon and ticker until the user has bypassed the lockscreen. 
Value is one of the following:

- `https://developer.android.com/reference/kotlin/android/app/Notification#VISIBILITY_PUBLIC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/Notification#VISIBILITY_PRIVATE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/Notification#VISIBILITY_SECRET:kotlin.Int`

### when

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var when: Long
```

A timestamp related to this notification, in milliseconds since the epoch.

Default value: `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`.

Choose a timestamp that will be most relevant to the user. For most finite events, this corresponds to the time the event happened (or will happen, in the case of events that have yet to occur but about which the user is being informed). Indefinite events should be timestamped according to when the activity began.

Some examples:

- Notification of a new chat message should be stamped when the message was received.
- Notification of an ongoing file download (with a progress bar, for example) should be stamped when the download started.
- Notification of a completed file download should be stamped when the download finished.
- Notification of an upcoming meeting should be stamped with the time the meeting will begin (that is, in the future).
- Notification of an ongoing stopwatch (increasing timer) should be stamped with the watch's start time.
- Notification of an ongoing countdown timer should be stamped with the timer's end time.

For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` and above, this time is not shown anymore by default and must be opted into by using `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#setShowWhen(kotlin.Boolean)`
