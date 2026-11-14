Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# NutritionRecord

```
class NutritionRecord : IntervalRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.health.connect.datatypes.Record](Record.md) |||
| | ↳ | [android.health.connect.datatypes.IntervalRecord](IntervalRecord.md) ||
| | | ↳ | [android.health.connect.datatypes.NutritionRecord](NutritionRecord.md) |
| --- | --- | --- | --- |

Captures what nutrients were consumed as part of a meal or a food item.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord.Builder` Builder class for NutritionRecord |

| Inherited constants ||
|---|---|
| From class Record |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getBiotin <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getCaffeine <br /> |
| --- | --- |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getCalcium <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getChloride <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getCholesterol <br /> |
| --- | --- |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getChromium <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getCopper <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getDietaryFiber <br /> |
| --- | --- |
| [Energy](../android.health.connect.datatypes.units/Energy.md)? | getEnergy <br /> |
| [Energy](../android.health.connect.datatypes.units/Energy.md)? | getEnergyFromFat <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getFolate <br /> |
| --- | --- |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getFolicAcid <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getIodine <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getIron <br /> |
| --- | --- |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getMagnesium <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getManganese <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getMealName <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMealType <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getMolybdenum <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getMonounsaturatedFat <br /> |
| --- | --- |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getNiacin <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getPantothenicAcid <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getPhosphorus <br /> |
| --- | --- |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getPolyunsaturatedFat <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getPotassium <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getProtein <br /> |
| --- | --- |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getRiboflavin <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getSaturatedFat <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getSelenium <br /> |
| --- | --- |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getSodium <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getSugar <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getThiamin <br /> |
| --- | --- |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getTotalCarbohydrate <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getTotalFat <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getTransFat <br /> |
| --- | --- |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getUnsaturatedFat <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getVitaminA <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getVitaminB12 <br /> |
| --- | --- |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getVitaminB6 <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getVitaminC <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getVitaminD <br /> |
| --- | --- |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getVitaminE <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getVitaminK <br /> |
| [Mass](../android.health.connect.datatypes.units/Mass.md)? | getZinc <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode <br /> |

| Inherited functions ||
|---|---|
| From class IntervalRecord |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | getEndTime <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | getEndZoneOffset <br /> | | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | getStartTime <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | getStartZoneOffset <br /> | ||
| From class Record |---|---| | Metadata | getMetadata <br /> | ||

| Properties ||
|---|---|
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#BIOTIN_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total biotin using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#CAFFEINE_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total caffeine using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#CALCIUM_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total calcium using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#CHLORIDE_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total chloride using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#CHOLESTEROL_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total cholesterol using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#CHROMIUM_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total chromium using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#COPPER_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total copper using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#DIETARY_FIBER_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total dietary fibre using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Energy](../android.health.connect.datatypes.units/Energy.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#ENERGY_FROM_FAT_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total energy from fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](AggregationType.md)\< [Energy](../android.health.connect.datatypes.units/Energy.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#ENERGY_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total energy using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#FOLATE_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total folate using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#FOLIC_ACID_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total folic acid using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#IODINE_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total iodine using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#IRON_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total iron using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#MAGNESIUM_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total magnesium using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#MANGANESE_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total manganese using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#MOLYBDENUM_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total molybdenum using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#MONOUNSATURATED_FAT_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total monounsaturated fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#NIACIN_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total niacin using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#PANTOTHENIC_ACID_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total pantothenic acid fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#PHOSPHORUS_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total phosphorus fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#POLYUNSATURATED_FAT_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total polyunsaturated fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#POTASSIUM_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total potassium using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#PROTEIN_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total protein using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#RIBOFLAVIN_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total riboflavin using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#SATURATED_FAT_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total saturated fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#SELENIUM_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total selenium using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#SODIUM_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total sodium using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#SUGAR_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total sugar using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#THIAMIN_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total thiamin using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#TOTAL_CARBOHYDRATE_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total carbohydrate using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#TOTAL_FAT_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#TRANS_FAT_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total trans fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#UNSATURATED_FAT_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total unsaturated fat using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#VITAMIN_A_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total Vitamin A using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#VITAMIN_B12_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total Vitamin B12 using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#VITAMIN_B6_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total Vitamin B6 using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#VITAMIN_C_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total Vitamin C using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#VITAMIN_D_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total Vitamin D using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#VITAMIN_E_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total Vitamin E using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#VITAMIN_K_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total Vitamin K using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord#ZINC_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total Zinc using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
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
| Mass | biotin in Mass unit. This value may be `null`. |

### getCaffeine

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getCaffeine(): Mass?
```

| Return ||
|---|---|
| Mass | caffeine in Mass unit. This value may be `null`. |

### getCalcium

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getCalcium(): Mass?
```

| Return ||
|---|---|
| Mass | calcium in Mass unit. This value may be `null`. |

### getChloride

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getChloride(): Mass?
```

| Return ||
|---|---|
| Mass | chloride in Mass unit. This value may be `null`. |

### getCholesterol

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getCholesterol(): Mass?
```

| Return ||
|---|---|
| Mass | cholesterol in Mass unit. This value may be `null`. |

### getChromium

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getChromium(): Mass?
```

| Return ||
|---|---|
| Mass | chromium in Mass unit. This value may be `null`. |

### getCopper

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getCopper(): Mass?
```

| Return ||
|---|---|
| Mass | copper in Mass unit. This value may be `null`. |

### getDietaryFiber

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getDietaryFiber(): Mass?
```

| Return ||
|---|---|
| Mass | dietaryFiber in Mass unit. This value may be `null`. |

### getEnergy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getEnergy(): Energy?
```

| Return ||
|---|---|
| Energy | energy in Energy unit. This value may be `null`. |

### getEnergyFromFat

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getEnergyFromFat(): Energy?
```

| Return ||
|---|---|
| Energy | energyFromFat in Energy unit. This value may be `null`. |

### getFolate

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getFolate(): Mass?
```

| Return ||
|---|---|
| Mass | folate in Mass unit. This value may be `null`. |

### getFolicAcid

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getFolicAcid(): Mass?
```

| Return ||
|---|---|
| Mass | folicAcid in Mass unit. This value may be `null`. |

### getIodine

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getIodine(): Mass?
```

| Return ||
|---|---|
| Mass | iodine in Mass unit. This value may be `null`. |

### getIron

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getIron(): Mass?
```

| Return ||
|---|---|
| Mass | iron in Mass unit. This value may be `null`. |

### getMagnesium

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getMagnesium(): Mass?
```

| Return ||
|---|---|
| Mass | magnesium in Mass unit. This value may be `null`. |

### getManganese

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getManganese(): Mass?
```

| Return ||
|---|---|
| Mass | manganese in Mass unit. This value may be `null`. |

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
| Mass | molybdenum in Mass unit. This value may be `null`. |

### getMonounsaturatedFat

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getMonounsaturatedFat(): Mass?
```

| Return ||
|---|---|
| Mass | monounsaturatedFat in Mass unit. This value may be `null`. |

### getNiacin

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getNiacin(): Mass?
```

| Return ||
|---|---|
| Mass | niacin in Mass unit. This value may be `null`. |

### getPantothenicAcid

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getPantothenicAcid(): Mass?
```

| Return ||
|---|---|
| Mass | pantothenicAcid in Mass unit. This value may be `null`. |

### getPhosphorus

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getPhosphorus(): Mass?
```

| Return ||
|---|---|
| Mass | phosphorus in Mass unit. This value may be `null`. |

### getPolyunsaturatedFat

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getPolyunsaturatedFat(): Mass?
```

| Return ||
|---|---|
| Mass | polyunsaturatedFat in Mass unit. This value may be `null`. |

### getPotassium

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getPotassium(): Mass?
```

| Return ||
|---|---|
| Mass | potassium. This value may be `null`. |

### getProtein

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getProtein(): Mass?
```

| Return ||
|---|---|
| Mass | protein in Mass unit. This value may be `null`. |

### getRiboflavin

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getRiboflavin(): Mass?
```

| Return ||
|---|---|
| Mass | riboflavin in Mass unit. This value may be `null`. |

### getSaturatedFat

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getSaturatedFat(): Mass?
```

| Return ||
|---|---|
| Mass | saturatedFat in Mass unit. This value may be `null`. |

### getSelenium

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getSelenium(): Mass?
```

| Return ||
|---|---|
| Mass | selenium in Mass unit. This value may be `null`. |

### getSodium

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getSodium(): Mass?
```

| Return ||
|---|---|
| Mass | sodium in Mass unit. This value may be `null`. |

### getSugar

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getSugar(): Mass?
```

| Return ||
|---|---|
| Mass | sugar in Mass unit. This value may be `null`. |

### getThiamin

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getThiamin(): Mass?
```

| Return ||
|---|---|
| Mass | thiamin. This value may be `null`. |

### getTotalCarbohydrate

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getTotalCarbohydrate(): Mass?
```

| Return ||
|---|---|
| Mass | totalCarbohydrate in Mass unit. This value may be `null`. |

### getTotalFat

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getTotalFat(): Mass?
```

| Return ||
|---|---|
| Mass | totalFat in Mass unit. This value may be `null`. |

### getTransFat

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getTransFat(): Mass?
```

| Return ||
|---|---|
| Mass | transFat in Mass unit. This value may be `null`. |

### getUnsaturatedFat

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getUnsaturatedFat(): Mass?
```

| Return ||
|---|---|
| Mass | unsaturatedFat. This value may be `null`. |

### getVitaminA

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getVitaminA(): Mass?
```

| Return ||
|---|---|
| Mass | vitaminA in Mass unit. This value may be `null`. |

### getVitaminB12

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getVitaminB12(): Mass?
```

| Return ||
|---|---|
| Mass | vitaminB12 in Mass unit. This value may be `null`. |

### getVitaminB6

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getVitaminB6(): Mass?
```

| Return ||
|---|---|
| Mass | vitaminB6 in Mass unit. This value may be `null`. |

### getVitaminC

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getVitaminC(): Mass?
```

| Return ||
|---|---|
| Mass | vitaminC in Mass unit. This value may be `null`. |

### getVitaminD

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getVitaminD(): Mass?
```

| Return ||
|---|---|
| Mass | vitaminD in Mass unit. This value may be `null`. |

### getVitaminE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getVitaminE(): Mass?
```

| Return ||
|---|---|
| Mass | vitaminE in Mass unit. This value may be `null`. |

### getVitaminK

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getVitaminK(): Mass?
```

| Return ||
|---|---|
| Mass | vitaminK in Mass unit. This value may be `null`. |

### getZinc

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getZinc(): Mass?
```

| Return ||
|---|---|
| Mass | zinc in Mass unit. This value may be `null`. |

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
