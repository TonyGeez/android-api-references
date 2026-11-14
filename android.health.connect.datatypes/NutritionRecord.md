Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# NutritionRecord

```
class NutritionRecord : IntervalRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.health.connect.datatypes.Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record) |||
| | ↳ | [android.health.connect.datatypes.IntervalRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord) ||
| | | ↳ | [android.health.connect.datatypes.NutritionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#) |
| --- | --- | --- | --- |

Captures what nutrients were consumed as part of a meal or a food item.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#` |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getBiotin()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getCaffeine()()` <br /> |
| --- | --- |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getCalcium()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getChloride()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getCholesterol()()` <br /> |
| --- | --- |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getChromium()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getCopper()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getDietaryFiber()()` <br /> |
| --- | --- |
| [Energy](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getEnergy()()` <br /> |
| [Energy](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getEnergyFromFat()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getFolate()()` <br /> |
| --- | --- |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getFolicAcid()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getIodine()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getIron()()` <br /> |
| --- | --- |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getMagnesium()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getManganese()()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getMealName()()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getMealType()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getMolybdenum()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getMonounsaturatedFat()()` <br /> |
| --- | --- |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getNiacin()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getPantothenicAcid()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getPhosphorus()()` <br /> |
| --- | --- |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getPolyunsaturatedFat()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getPotassium()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getProtein()()` <br /> |
| --- | --- |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getRiboflavin()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getSaturatedFat()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getSelenium()()` <br /> |
| --- | --- |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getSodium()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getSugar()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getThiamin()()` <br /> |
| --- | --- |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getTotalCarbohydrate()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getTotalFat()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getTransFat()()` <br /> |
| --- | --- |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getUnsaturatedFat()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getVitaminA()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getVitaminB12()()` <br /> |
| --- | --- |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getVitaminB6()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getVitaminC()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getVitaminD()()` <br /> |
| --- | --- |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getVitaminE()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getVitaminK()()` <br /> |
| [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#getZinc()()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#hashCode()()` <br /> |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord` |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndZoneOffset()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartZoneOffset()()` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Metadata` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#getMetadata()()` <br /> | ||

| Properties ||
|---|---|
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#BIOTIN_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total biotin using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#CAFFEINE_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total caffeine using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#CALCIUM_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total calcium using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#CHLORIDE_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total chloride using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#CHOLESTEROL_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total cholesterol using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#CHROMIUM_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total chromium using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#COPPER_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total copper using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#DIETARY_FIBER_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total dietary fibre using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Energy](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#ENERGY_FROM_FAT_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total energy from fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Energy](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#ENERGY_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total energy using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#FOLATE_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total folate using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#FOLIC_ACID_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total folic acid using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#IODINE_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total iodine using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#IRON_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total iron using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#MAGNESIUM_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total magnesium using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#MANGANESE_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total manganese using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#MOLYBDENUM_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total molybdenum using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#MONOUNSATURATED_FAT_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total monounsaturated fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#NIACIN_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total niacin using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#PANTOTHENIC_ACID_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total pantothenic acid fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#PHOSPHORUS_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total phosphorus fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#POLYUNSATURATED_FAT_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total polyunsaturated fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#POTASSIUM_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total potassium using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#PROTEIN_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total protein using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#RIBOFLAVIN_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total riboflavin using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#SATURATED_FAT_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total saturated fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#SELENIUM_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total selenium using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#SODIUM_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total sodium using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#SUGAR_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total sugar using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#THIAMIN_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total thiamin using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#TOTAL_CARBOHYDRATE_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total carbohydrate using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#TOTAL_FAT_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#TRANS_FAT_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total trans fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#UNSATURATED_FAT_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total unsaturated fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#VITAMIN_A_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total Vitamin A using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#VITAMIN_B12_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total Vitamin B12 using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#VITAMIN_B6_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total Vitamin B6 using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#VITAMIN_C_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total Vitamin C using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#VITAMIN_D_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total Vitamin D using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#VITAMIN_E_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total Vitamin E using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#VITAMIN_K_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total Vitamin K using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Mass](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#ZINC_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total Zinc using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `object` | the reference object with which to compare. This value may be `null`. |
| `o` | the reference object with which to compare. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj |

### getBiotin

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getBiotin(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | biotin in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getCaffeine

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getCaffeine(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | caffeine in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getCalcium

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getCalcium(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | calcium in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getChloride

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getChloride(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | chloride in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getCholesterol

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getCholesterol(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | cholesterol in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getChromium

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getChromium(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | chromium in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getCopper

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getCopper(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | copper in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getDietaryFiber

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getDietaryFiber(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | dietaryFiber in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getEnergy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getEnergy(): Energy?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy?` | energy in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy` unit. This value may be `null`. |

### getEnergyFromFat

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getEnergyFromFat(): Energy?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy?` | energyFromFat in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy` unit. This value may be `null`. |

### getFolate

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getFolate(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | folate in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getFolicAcid

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getFolicAcid(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | folicAcid in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getIodine

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getIodine(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | iodine in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getIron

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getIron(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | iron in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getMagnesium

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getMagnesium(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | magnesium in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getManganese

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getManganese(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | manganese in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getMealName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getMealName(): String?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the meal name. This value may be `null`. |

### getMealType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getMealType(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | mealType. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MealType#MEAL_TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MealType#MEAL_TYPE_BREAKFAST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MealType#MEAL_TYPE_LUNCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MealType#MEAL_TYPE_DINNER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MealType#MEAL_TYPE_SNACK:kotlin.Int` |

### getMolybdenum

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getMolybdenum(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | molybdenum in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getMonounsaturatedFat

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getMonounsaturatedFat(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | monounsaturatedFat in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getNiacin

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getNiacin(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | niacin in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getPantothenicAcid

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getPantothenicAcid(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | pantothenicAcid in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getPhosphorus

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getPhosphorus(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | phosphorus in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getPolyunsaturatedFat

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getPolyunsaturatedFat(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | polyunsaturatedFat in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getPotassium

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getPotassium(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | potassium. This value may be `null`. |

### getProtein

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getProtein(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | protein in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getRiboflavin

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getRiboflavin(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | riboflavin in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getSaturatedFat

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getSaturatedFat(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | saturatedFat in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getSelenium

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getSelenium(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | selenium in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getSodium

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getSodium(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | sodium in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getSugar

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getSugar(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | sugar in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getThiamin

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getThiamin(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | thiamin. This value may be `null`. |

### getTotalCarbohydrate

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getTotalCarbohydrate(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | totalCarbohydrate in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getTotalFat

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getTotalFat(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | totalFat in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getTransFat

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getTransFat(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | transFat in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getUnsaturatedFat

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getUnsaturatedFat(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | unsaturatedFat. This value may be `null`. |

### getVitaminA

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getVitaminA(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | vitaminA in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getVitaminB12

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getVitaminB12(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | vitaminB12 in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getVitaminB6

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getVitaminB6(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | vitaminB6 in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getVitaminC

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getVitaminC(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | vitaminC in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getVitaminD

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getVitaminD(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | vitaminD in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getVitaminE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getVitaminE(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | vitaminE in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getVitaminK

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getVitaminK(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | vitaminK in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### getZinc

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getZinc(): Mass?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass?` | zinc in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Mass` unit. This value may be `null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

## Properties

### BIOTIN_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val BIOTIN_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total biotin using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### CAFFEINE_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val CAFFEINE_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total caffeine using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### CALCIUM_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val CALCIUM_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total calcium using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### CHLORIDE_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val CHLORIDE_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total chloride using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### CHOLESTEROL_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val CHOLESTEROL_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total cholesterol using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### CHROMIUM_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val CHROMIUM_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total chromium using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### COPPER_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val COPPER_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total copper using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### DIETARY_FIBER_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val DIETARY_FIBER_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total dietary fibre using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### ENERGY_FROM_FAT_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val ENERGY_FROM_FAT_TOTAL: AggregationType<Energy!>
```

Metric identifier to get total energy from fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### ENERGY_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val ENERGY_TOTAL: AggregationType<Energy!>
```

Metric identifier to get total energy using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### FOLATE_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val FOLATE_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total folate using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### FOLIC_ACID_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val FOLIC_ACID_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total folic acid using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### IODINE_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val IODINE_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total iodine using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### IRON_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val IRON_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total iron using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### MAGNESIUM_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val MAGNESIUM_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total magnesium using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### MANGANESE_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val MANGANESE_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total manganese using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### MOLYBDENUM_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val MOLYBDENUM_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total molybdenum using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### MONOUNSATURATED_FAT_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val MONOUNSATURATED_FAT_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total monounsaturated fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### NIACIN_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val NIACIN_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total niacin using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### PANTOTHENIC_ACID_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val PANTOTHENIC_ACID_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total pantothenic acid fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### PHOSPHORUS_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val PHOSPHORUS_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total phosphorus fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### POLYUNSATURATED_FAT_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val POLYUNSATURATED_FAT_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total polyunsaturated fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### POTASSIUM_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val POTASSIUM_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total potassium using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### PROTEIN_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val PROTEIN_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total protein using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### RIBOFLAVIN_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val RIBOFLAVIN_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total riboflavin using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### SATURATED_FAT_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val SATURATED_FAT_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total saturated fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### SELENIUM_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val SELENIUM_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total selenium using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### SODIUM_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val SODIUM_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total sodium using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### SUGAR_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val SUGAR_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total sugar using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### THIAMIN_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val THIAMIN_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total thiamin using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### TOTAL_CARBOHYDRATE_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val TOTAL_CARBOHYDRATE_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total carbohydrate using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### TOTAL_FAT_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val TOTAL_FAT_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### TRANS_FAT_TOTAL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 10](https://developer.android.com/sdkExtensions)

```
static val TRANS_FAT_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total trans fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### UNSATURATED_FAT_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val UNSATURATED_FAT_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total unsaturated fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### VITAMIN_A_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val VITAMIN_A_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total Vitamin A using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### VITAMIN_B12_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val VITAMIN_B12_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total Vitamin B12 using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### VITAMIN_B6_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val VITAMIN_B6_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total Vitamin B6 using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### VITAMIN_C_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val VITAMIN_C_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total Vitamin C using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### VITAMIN_D_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val VITAMIN_D_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total Vitamin D using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### VITAMIN_E_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val VITAMIN_E_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total Vitamin E using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### VITAMIN_K_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val VITAMIN_K_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total Vitamin K using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### ZINC_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val ZINC_TOTAL: AggregationType<Mass!>
```

Metric identifier to get total Zinc using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`
