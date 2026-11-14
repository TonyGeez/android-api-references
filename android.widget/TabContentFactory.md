# TabHost.TabContentFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TabContentFactory

Kotlin| [Java](../android/widget/TabHost.TabContentFactory.md) 
| --- | --- |

```
interface TabContentFactory
```

| [android.widget.TabHost.TabContentFactory](../android/widget/TabHost.TabContentFactory.md) |

| **This interface was deprecated in API level 30.**
|
| Deprecated in Java.

Makes the content of a tab when it is selected. Use this if your tab content needs to be created on demand, i.e. you are not showing an existing view or starting an activity.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [View](../android/view/View.md)! | [createTabContent](../android/widget/TabHost.TabContentFactory.md))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Callback to make the tab contents |

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
| [View](../android/view/View.md)! | The view to display the contents of the selected tab. |
