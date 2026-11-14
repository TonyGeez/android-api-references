# TabHost.TabContentFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TabContentFactory

Kotlin| [Java](https://developer.android.com/reference/android/widget/TabHost.TabContentFactory "View this page in Java") 
| --- | --- |

```
interface TabContentFactory
```

| [android.widget.TabHost.TabContentFactory](https://developer.android.com/reference/kotlin/android/widget/TabHost.TabContentFactory#) |

| **This interface was deprecated in API level 30.**
|
| Deprecated in Java.

Makes the content of a tab when it is selected. Use this if your tab content needs to be created on demand, i.e. you are not showing an existing view or starting an activity.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [createTabContent](https://developer.android.com/reference/kotlin/android/widget/TabHost.TabContentFactory#createTabContent(kotlin.String))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Callback to make the tab contents |

## Public methods

### createTabContent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createTabContent(tag: String!): View!
```

**Deprecated:** *Deprecated in Java.*

Callback to make the tab contents

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Which tab was selected. |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | The view to display the contents of the selected tab. |
