Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# HealthPermissions

```
class HealthPermissions
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.HealthPermissions](../android/health/connect/HealthPermissions.md) |

Permissions for accessing the HealthConnect APIs.

Apps must support `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW_PERMISSION_USAGE:kotlin.String` with `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#CATEGORY_HEALTH_PERMISSIONS:kotlin.String` category to be granted read/write health data permissions.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_ACTIVE_CALORIES_BURNED:kotlin.String` Allows an application to read the user's active calories burned data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_ACTIVITY_INTENSITY:kotlin.String` Allows an application to read the user's activity intensity data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_ALCOHOL_CONSUMPTION:kotlin.String` Allows an application to write user's alcohol consumption data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_BASAL_BODY_TEMPERATURE:kotlin.String` Allows an application to read the user's body temperature data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_BASAL_METABOLIC_RATE:kotlin.String` Allows an application to read the user's basal metabolic rate data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_BLOOD_GLUCOSE:kotlin.String` Allows an application to read the user's blood glucose data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_BLOOD_PRESSURE:kotlin.String` Allows an application to read the user's blood pressure data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_BODY_FAT:kotlin.String` Allows an application to read the user's body fat data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_BODY_TEMPERATURE:kotlin.String` Allows an application to read the user's body temperature data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_BODY_WATER_MASS:kotlin.String` Allows an application to read the user's body water mass data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_BONE_MASS:kotlin.String` Allows an application to read the user's bone mass data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_CERVICAL_MUCUS:kotlin.String` Allows an application to read the user's cervical mucus data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_DISTANCE:kotlin.String` Allows an application to read the user's distance data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_ELEVATION_GAINED:kotlin.String` Allows an application to read the user's elevation gained data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_EXERCISE:kotlin.String` Allows an application to read the user's exercise data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_EXERCISE_ROUTES:kotlin.String` Allows an application to read `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseRoute`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_FLOORS_CLIMBED:kotlin.String` Allows an application to read the user's floors climbed data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_HEALTH_DATA_HISTORY:kotlin.String` Allows an application to read the entire history of health data (of any type). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_HEALTH_DATA_IN_BACKGROUND:kotlin.String` Allows an application to read health data (of any type) in background. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_HEART_RATE:kotlin.String` Allows an application to read the user's heart rate data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_HEART_RATE_VARIABILITY:kotlin.String` Allows an application to read the user's heart rate variability data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_HEIGHT:kotlin.String` Allows an application to read the user's height data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_HYDRATION:kotlin.String` Allows an application to read the user's hydration data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_INTERMENSTRUAL_BLEEDING:kotlin.String` Allows an application to read the user's intermenstrual bleeding data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_LEAN_BODY_MASS:kotlin.String` Allows an application to read the user's lean body mass data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_MEDICAL_DATA_ALLERGIES_INTOLERANCES:kotlin.String` Allows an application to read the user's data about allergies and intolerances. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_MEDICAL_DATA_CONDITIONS:kotlin.String` Allows an application to read the user's data about medical conditions. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_MEDICAL_DATA_LABORATORY_RESULTS:kotlin.String` Allows an application to read the user's laboratory result data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_MEDICAL_DATA_MEDICATIONS:kotlin.String` Allows an application to read the user's medication data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_MEDICAL_DATA_PERSONAL_DETAILS:kotlin.String` Allows an application to read the user's personal details. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_MEDICAL_DATA_PRACTITIONER_DETAILS:kotlin.String` Allows an application to read the user's data about the practitioners who have interacted with them in their medical record. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_MEDICAL_DATA_PREGNANCY:kotlin.String` Allows an application to read the user's pregnancy data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_MEDICAL_DATA_PROCEDURES:kotlin.String` Allows an application to read the user's data about medical procedures. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_MEDICAL_DATA_SOCIAL_HISTORY:kotlin.String` Allows an application to read the user's social history data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_MEDICAL_DATA_VACCINES:kotlin.String` Allows an application to read the user's data about immunizations and vaccinations. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_MEDICAL_DATA_VISITS:kotlin.String` Allows an application to read the user's information about their encounters with health care practitioners, including things like location, time of appointment, and name of organization the visit was with. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_MEDICAL_DATA_VITAL_SIGNS:kotlin.String` Allows an application to read the user's vital signs data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_MENSTRUAL_CYCLE_PHASE:kotlin.String` Allows an application to read the user's cycle phases data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_MENSTRUATION:kotlin.String` Allows an application to read the user's menstruation data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_MINDFULNESS:kotlin.String` Allows an application to read user's mindfulness data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_NUTRITION:kotlin.String` Allows an application to read the user's nutrition data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_OVULATION_TEST:kotlin.String` Allows an application to read the user's ovulation test data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_OXYGEN_SATURATION:kotlin.String` Allows an application to read the user's oxygen saturation data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_PLANNED_EXERCISE:kotlin.String` Allows an application to read the user's training plan data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_POWER:kotlin.String` Allows an application to read the user's power data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_RESPIRATORY_RATE:kotlin.String` Allows an application to read the user's respiratory rate data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_RESTING_HEART_RATE:kotlin.String` Allows an application to read the user's resting heart rate data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SEXUAL_ACTIVITY:kotlin.String` Allows an application to read the user's sexual activity data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SKIN_TEMPERATURE:kotlin.String` Allows an application to read the user's skin temperature data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SLEEP:kotlin.String` Allows an application to read the user's sleep data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SPEED:kotlin.String` Allows an application to read the user's speed data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_STEPS:kotlin.String` Allows an application to read the user's steps data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_ABDOMINAL_PAIN:kotlin.String` Allows an application to read the user's abdominal pain data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_ACNE:kotlin.String` Allows an application to read the user's acne data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_BACK_PAIN:kotlin.String` Allows an application to read the user's back pain data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_BLOATING:kotlin.String` Allows an application to read the user's bloating data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_BRAIN_FOG:kotlin.String` Allows an application to read the user's brain fog data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_BREAST_TENDERNESS:kotlin.String` Allows an application to read the user's breast tenderness data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_BRITTLE_NAILS:kotlin.String` Allows an application to read the user's brittle nails data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_BURNING_MOUTH:kotlin.String` Allows an application to read the user's burning mouth data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_CHEST_PAIN:kotlin.String` Allows an application to read the user's chest pain data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_CHEST_TIGHTNESS:kotlin.String` Allows an application to read the user's chest tightness data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_CHILLS:kotlin.String` Allows an application to read the user's chills data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_CONSTIPATION:kotlin.String` Allows an application to read the user's constipation data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_COUGH:kotlin.String` Allows an application to read the user's cough symptom data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_CRAMPS:kotlin.String` Allows an application to read the user's cramps data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_CRAVINGS:kotlin.String` Allows an application to read the user's cravings data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_DEHYDRATION:kotlin.String` Allows an application to read the user's dehydration data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_DIARRHEA:kotlin.String` Allows an application to read the user's diarrhea data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_DIFFICULTY_SWALLOWING:kotlin.String` Allows an application to read the user's difficulty swallowing data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_DIZZINESS:kotlin.String` Allows an application to read the user's dizziness data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_DRY_SKIN:kotlin.String` Allows an application to read the user's dry skin data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_EARACHES:kotlin.String` Allows an application to read the user's earaches data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_FATIGUE:kotlin.String` Allows an application to read the user's fatigue data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_FEVER:kotlin.String` Allows an application to read the user's fever data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_GENERALIZED_BODY_ACHE:kotlin.String` Allows an application to read the user's generalized body ache data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_HAIR_LOSS:kotlin.String` Allows an application to read the user's hair loss data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_HEADACHE:kotlin.String` Allows an application to read the user's headache data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_HEARTBURN:kotlin.String` Allows an application to read the user's heartburn data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_HEART_PALPITATIONS:kotlin.String` Allows an application to read the user's heart palpitations data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_HOT_FLASHES:kotlin.String` Allows an application to read the user's hot flashes data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_INSOMNIA:kotlin.String` Allows an application to read the user's insomnia data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_JOINT_PAIN:kotlin.String` Allows an application to read the user's joint pain data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_JOINT_STIFFNESS:kotlin.String` Allows an application to read the user's joint stiffness data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_LOSS_OF_APPETITE:kotlin.String` Allows an application to read the user's loss of appetite data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_LOSS_OF_CONSCIOUSNESS:kotlin.String` Allows an application to read the user's loss of consciousness data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_LOWER_BACK_PAIN:kotlin.String` Allows an application to read the user's lower back pain data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_MEMORY_LAPSE:kotlin.String` Allows an application to read the user's memory lapse data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_MOOD_CHANGE:kotlin.String` Allows an application to read the user's mood change data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_MUSCLE_PAIN:kotlin.String` Allows an application to read the user's muscle pain data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_NAUSEA:kotlin.String` Allows an application to read the user's nausea data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_NIGHT_SWEATS:kotlin.String` Allows an application to read the user's night sweats data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_PELVIC_PAIN:kotlin.String` Allows an application to read the user's pelvic pain data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_RAPID_POUNDING_OR_FLUTTERING_HEARTBEAT:kotlin.String` Allows an application to read the user's rapid, pounding, or fluttering heartbeat data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_REDUCED_CAPACITY_FOR_EXERCISE:kotlin.String` Allows an application to read the user's reduced capacity for exercise data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_RUNNY_NOSE:kotlin.String` Allows an application to read the user's runny nose data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_SHORTNESS_OF_BREATH:kotlin.String` Allows an application to read the user's shortness of breath data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_SKIPPED_HEARTBEAT:kotlin.String` Allows an application to read the user's skipped heartbeat data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_SLEEPINESS:kotlin.String` Allows an application to read the user's sleepiness data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_SLEEP_CHANGES:kotlin.String` Allows an application to read the user's sleep changes data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_SNEEZING:kotlin.String` Allows an application to read the user's sneezing data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_SNORE:kotlin.String` Allows an application to read the user's snore data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_SORE_THROAT:kotlin.String` Allows an application to read the user's sore throat data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_STOMACH_ACHE:kotlin.String` Allows an application to read the user's stomach ache data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_STUFFY_NOSE:kotlin.String` Allows an application to read the user's stuffy nose data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_UNEXPLAINED_WEIGHT_CHANGES:kotlin.String` Allows an application to read the user's unexplained weight changes data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_VAGINAL_DRYNESS:kotlin.String` Allows an application to read the user's vaginal dryness data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_VAGINAL_ITCHINESS:kotlin.String` Allows an application to read the user's vaginal itchiness data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_VOMITING:kotlin.String` Allows an application to read the user's vomiting data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_WATER_RETENTION:kotlin.String` Allows an application to read the user's water retention data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_SYMPTOM_WHEEZING:kotlin.String` Allows an application to read the user's wheezing data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_TOTAL_CALORIES_BURNED:kotlin.String` Allows an application to read the user's total calories burned data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_VO2_MAX:kotlin.String` Allows an application to read the user's vo2 maximum data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_WEIGHT:kotlin.String` Allows an application to read the user's weight data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_WHEELCHAIR_PUSHES:kotlin.String` Allows an application to read the user's wheelchair pushes data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#START_ONBOARDING:kotlin.String` Allows an application to launch client onboarding activities responsible for connecting to Health Connect. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_ACTIVE_CALORIES_BURNED:kotlin.String` Allows an application to write the user's calories burned data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_ACTIVITY_INTENSITY:kotlin.String` Allows an application to write the user's activity intensity data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_ALCOHOL_CONSUMPTION:kotlin.String` Allows an application to write user's alcohol consumption data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_BASAL_BODY_TEMPERATURE:kotlin.String` Allows an application to write the user's basal body temperature data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_BASAL_METABOLIC_RATE:kotlin.String` Allows an application to write the user's basal metabolic rate data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_BLOOD_GLUCOSE:kotlin.String` Allows an application to write the user's blood glucose data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_BLOOD_PRESSURE:kotlin.String` Allows an application to write the user's blood pressure data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_BODY_FAT:kotlin.String` Allows an application to write the user's body fat data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_BODY_TEMPERATURE:kotlin.String` Allows an application to write the user's body temperature data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_BODY_WATER_MASS:kotlin.String` Allows an application to write the user's body water mass data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_BONE_MASS:kotlin.String` Allows an application to write the user's bone mass data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_CERVICAL_MUCUS:kotlin.String` Allows an application to write the user's cervical mucus data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_DEVICE_UDI:kotlin.String` Allows an application to write the device's unique device identifier (UDI). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_DISTANCE:kotlin.String` Allows an application to write the user's distance data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_ELEVATION_GAINED:kotlin.String` Allows an application to write the user's elevation gained data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_EXERCISE:kotlin.String` Allows an application to write the user's exercise data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_EXERCISE_ROUTE:kotlin.String` Allows an application to write the user's exercise route. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_FLOORS_CLIMBED:kotlin.String` Allows an application to write the user's floors climbed data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_HEART_RATE:kotlin.String` Allows an application to write the user's heart rate data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_HEART_RATE_VARIABILITY:kotlin.String` Allows an application to write the user's heart rate variability data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_HEIGHT:kotlin.String` Allows an application to write the user's height data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_HYDRATION:kotlin.String` Allows an application to write the user's hydration data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_INTERMENSTRUAL_BLEEDING:kotlin.String` Allows an application to write the user's intermenstrual bleeding data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_LEAN_BODY_MASS:kotlin.String` Allows an application to write the user's lean body mass data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_MEDICAL_DATA:kotlin.String` Allows an application to write the user's medical data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_MENSTRUAL_CYCLE_PHASE:kotlin.String` Allows an application to write the user's cycle phases data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_MENSTRUATION:kotlin.String` Allows an application to write the user's menstruation data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_MINDFULNESS:kotlin.String` Allows an application to write user's mindfulness data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_NUTRITION:kotlin.String` Allows an application to write the user's nutrition data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_OVULATION_TEST:kotlin.String` Allows an application to write the user's ovulation test data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_OXYGEN_SATURATION:kotlin.String` Allows an application to write the user's oxygen saturation data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_PLANNED_EXERCISE:kotlin.String` Allows an application to write the user's training plan data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_POWER:kotlin.String` Allows an application to write the user's power data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_RESPIRATORY_RATE:kotlin.String` Allows an application to write the user's respiratory rate data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_RESTING_HEART_RATE:kotlin.String` Allows an application to write the user's resting heart rate data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SEXUAL_ACTIVITY:kotlin.String` Allows an application to write the user's sexual activity data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SKIN_TEMPERATURE:kotlin.String` Allows an application to write the user's skin temperature data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SLEEP:kotlin.String` Allows an application to write the user's sleep data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SPEED:kotlin.String` Allows an application to write the user's speed data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_STEPS:kotlin.String` Allows an application to write the user's steps data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_ABDOMINAL_PAIN:kotlin.String` Allows an application to write the user's abdominal pain data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_ACNE:kotlin.String` Allows an application to write the user's acne data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_BACK_PAIN:kotlin.String` Allows an application to write the user's back pain data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_BLOATING:kotlin.String` Allows an application to write the user's bloating data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_BRAIN_FOG:kotlin.String` Allows an application to write the user's brain fog data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_BREAST_TENDERNESS:kotlin.String` Allows an application to write the user's breast tenderness data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_BRITTLE_NAILS:kotlin.String` Allows an application to write the user's brittle nails data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_BURNING_MOUTH:kotlin.String` Allows an application to write the user's burning mouth data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_CHEST_PAIN:kotlin.String` Allows an application to write the user's chest pain data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_CHEST_TIGHTNESS:kotlin.String` Allows an application to write the user's chest tightness data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_CHILLS:kotlin.String` Allows an application to write the user's chills data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_CONSTIPATION:kotlin.String` Allows an application to write the user's constipation data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_COUGH:kotlin.String` Allows an application to write the user's cough symptom data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_CRAMPS:kotlin.String` Allows an application to write the user's cramps data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_CRAVINGS:kotlin.String` Allows an application to write the user's cravings data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_DEHYDRATION:kotlin.String` Allows an application to write the user's dehydration data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_DIARRHEA:kotlin.String` Allows an application to write the user's diarrhea data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_DIFFICULTY_SWALLOWING:kotlin.String` Allows an application to write the user's difficulty swallowing data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_DIZZINESS:kotlin.String` Allows an application to write the user's dizziness data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_DRY_SKIN:kotlin.String` Allows an application to write the user's dry skin data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_EARACHES:kotlin.String` Allows an application to write the user's earaches data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_FATIGUE:kotlin.String` Allows an application to write the user's fatigue data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_FEVER:kotlin.String` Allows an application to write the user's fever data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_GENERALIZED_BODY_ACHE:kotlin.String` Allows an application to write the user's generalized body ache data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_HAIR_LOSS:kotlin.String` Allows an application to write the user's hair loss data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_HEADACHE:kotlin.String` Allows an application to write the user's headache data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_HEARTBURN:kotlin.String` Allows an application to write the user's heartburn data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_HEART_PALPITATIONS:kotlin.String` Allows an application to write the user's heart palpitations data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_HOT_FLASHES:kotlin.String` Allows an application to write the user's hot flashes data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_INSOMNIA:kotlin.String` Allows an application to write the user's insomnia data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_JOINT_PAIN:kotlin.String` Allows an application to write the user's joint pain data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_JOINT_STIFFNESS:kotlin.String` Allows an application to write the user's joint stiffness data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_LOSS_OF_APPETITE:kotlin.String` Allows an application to write the user's loss of appetite data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_LOSS_OF_CONSCIOUSNESS:kotlin.String` Allows an application to write the user's loss of consciousness data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_LOWER_BACK_PAIN:kotlin.String` Allows an application to write the user's lower back pain data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_MEMORY_LAPSE:kotlin.String` Allows an application to write the user's memory lapse data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_MOOD_CHANGE:kotlin.String` Allows an application to write the user's mood change data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_MUSCLE_PAIN:kotlin.String` Allows an application to write the user's muscle pain data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_NAUSEA:kotlin.String` Allows an application to write the user's nausea data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_NIGHT_SWEATS:kotlin.String` Allows an application to write the user's night sweats data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_PELVIC_PAIN:kotlin.String` Allows an application to write the user's pelvic pain data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_RAPID_POUNDING_OR_FLUTTERING_HEARTBEAT:kotlin.String` Allows an application to write the user's rapid, pounding, or fluttering heartbeat data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_REDUCED_CAPACITY_FOR_EXERCISE:kotlin.String` Allows an application to write the user's reduced capacity for exercise data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_RUNNY_NOSE:kotlin.String` Allows an application to write the user's runny nose data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_SHORTNESS_OF_BREATH:kotlin.String` Allows an application to write the user's shortness of breath data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_SKIPPED_HEARTBEAT:kotlin.String` Allows an application to write the user's skipped heartbeat data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_SLEEPINESS:kotlin.String` Allows an application to write the user's sleepiness data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_SLEEP_CHANGES:kotlin.String` Allows an application to write the user's sleep changes data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_SNEEZING:kotlin.String` Allows an application to write the user's sneezing data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_SNORE:kotlin.String` Allows an application to write the user's snore data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_SORE_THROAT:kotlin.String` Allows an application to write the user's sore throat data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_STOMACH_ACHE:kotlin.String` Allows an application to write the user's stomach ache data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_STUFFY_NOSE:kotlin.String` Allows an application to write the user's stuffy nose data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_UNEXPLAINED_WEIGHT_CHANGES:kotlin.String` Allows an application to write the user's unexplained weight changes data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_VAGINAL_DRYNESS:kotlin.String` Allows an application to write the user's vaginal dryness data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_VAGINAL_ITCHINESS:kotlin.String` Allows an application to write the user's vaginal itchiness data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_VOMITING:kotlin.String` Allows an application to write the user's vomiting data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_WATER_RETENTION:kotlin.String` Allows an application to write the user's water retention data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_SYMPTOM_WHEEZING:kotlin.String` Allows an application to write the user's wheezing data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_TOTAL_CALORIES_BURNED:kotlin.String` Allows an application to write the user's total calories burned data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_VO2_MAX:kotlin.String` Allows an application to write the user's vo2 maximum data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_WEIGHT:kotlin.String` Allows an application to write the user's weight data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_WHEELCHAIR_PUSHES:kotlin.String` Allows an application to write the user's wheelchair pushes data. |
| --- | --- |

## Constants

### READ_ACTIVE_CALORIES_BURNED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_ACTIVE_CALORIES_BURNED: String
```

Allows an application to read the user's active calories burned data.

Protection level: dangerous.

 Value: "android.permission.health.READ_ACTIVE_CALORIES_BURNED"

### READ_ACTIVITY_INTENSITY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val READ_ACTIVITY_INTENSITY: String
```

Allows an application to read the user's activity intensity data.

Protection level: dangerous.

 Value: "android.permission.health.READ_ACTIVITY_INTENSITY"

### READ_ALCOHOL_CONSUMPTION

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_ALCOHOL_CONSUMPTION: String
```

Allows an application to write user's alcohol consumption data.

Protection level: dangerous.

 Value: "android.permission.health.READ_ALCOHOL_CONSUMPTION"

### READ_BASAL_BODY_TEMPERATURE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_BASAL_BODY_TEMPERATURE: String
```

Allows an application to read the user's body temperature data.

Protection level: dangerous.

 Value: "android.permission.health.READ_BASAL_BODY_TEMPERATURE"

### READ_BASAL_METABOLIC_RATE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_BASAL_METABOLIC_RATE: String
```

Allows an application to read the user's basal metabolic rate data.

Protection level: dangerous.

 Value: "android.permission.health.READ_BASAL_METABOLIC_RATE"

### READ_BLOOD_GLUCOSE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_BLOOD_GLUCOSE: String
```

Allows an application to read the user's blood glucose data.

Protection level: dangerous.

 Value: "android.permission.health.READ_BLOOD_GLUCOSE"

### READ_BLOOD_PRESSURE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_BLOOD_PRESSURE: String
```

Allows an application to read the user's blood pressure data.

Protection level: dangerous.

 Value: "android.permission.health.READ_BLOOD_PRESSURE"

### READ_BODY_FAT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_BODY_FAT: String
```

Allows an application to read the user's body fat data.

Protection level: dangerous.

 Value: "android.permission.health.READ_BODY_FAT"

### READ_BODY_TEMPERATURE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_BODY_TEMPERATURE: String
```

Allows an application to read the user's body temperature data.

Protection level: dangerous.

 Value: "android.permission.health.READ_BODY_TEMPERATURE"

### READ_BODY_WATER_MASS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_BODY_WATER_MASS: String
```

Allows an application to read the user's body water mass data.

Protection level: dangerous.

 Value: "android.permission.health.READ_BODY_WATER_MASS"

### READ_BONE_MASS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_BONE_MASS: String
```

Allows an application to read the user's bone mass data.

Protection level: dangerous.

 Value: "android.permission.health.READ_BONE_MASS"

### READ_CERVICAL_MUCUS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_CERVICAL_MUCUS: String
```

Allows an application to read the user's cervical mucus data.

Protection level: dangerous.

 Value: "android.permission.health.READ_CERVICAL_MUCUS"

### READ_DISTANCE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_DISTANCE: String
```

Allows an application to read the user's distance data.

Protection level: dangerous.

 Value: "android.permission.health.READ_DISTANCE"

### READ_ELEVATION_GAINED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_ELEVATION_GAINED: String
```

Allows an application to read the user's elevation gained data.

Protection level: dangerous.

 Value: "android.permission.health.READ_ELEVATION_GAINED"

### READ_EXERCISE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_EXERCISE: String
```

Allows an application to read the user's exercise data.

Protection level: dangerous.

 Value: "android.permission.health.READ_EXERCISE"

### READ_EXERCISE_ROUTES

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 12](https://developer.android.com/sdkExtensions)

```
static val READ_EXERCISE_ROUTES: String
```

Allows an application to read `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseRoute`.

This permission can only be granted manually by a user in Health Connect settings or in the route request activity which can be launched using ACTION_REQUEST_EXERCISE_ROUTE. Attempts to request the permission by applications will be ignored.

Applications should check if the permission has been granted before reading `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseRoute`.

Protection level: dangerous.

 Value: "android.permission.health.READ_EXERCISE_ROUTES"

### READ_FLOORS_CLIMBED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_FLOORS_CLIMBED: String
```

Allows an application to read the user's floors climbed data.

Protection level: dangerous.

 Value: "android.permission.health.READ_FLOORS_CLIMBED"

### READ_HEALTH_DATA_HISTORY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
static val READ_HEALTH_DATA_HISTORY: String
```

Allows an application to read the entire history of health data (of any type).

Protection level: dangerous.

 Value: "android.permission.health.READ_HEALTH_DATA_HISTORY"

### READ_HEALTH_DATA_IN_BACKGROUND

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
static val READ_HEALTH_DATA_IN_BACKGROUND: String
```

Allows an application to read health data (of any type) in background.

Protection level: dangerous.

 Value: "android.permission.health.READ_HEALTH_DATA_IN_BACKGROUND"

### READ_HEART_RATE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_HEART_RATE: String
```

Allows an application to read the user's heart rate data.

Protection level: dangerous.

 Value: "android.permission.health.READ_HEART_RATE"

### READ_HEART_RATE_VARIABILITY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_HEART_RATE_VARIABILITY: String
```

Allows an application to read the user's heart rate variability data.

Protection level: dangerous.

 Value: "android.permission.health.READ_HEART_RATE_VARIABILITY"

### READ_HEIGHT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_HEIGHT: String
```

Allows an application to read the user's height data.

Protection level: dangerous.

 Value: "android.permission.health.READ_HEIGHT"

### READ_HYDRATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_HYDRATION: String
```

Allows an application to read the user's hydration data.

Protection level: dangerous.

 Value: "android.permission.health.READ_HYDRATION"

### READ_INTERMENSTRUAL_BLEEDING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_INTERMENSTRUAL_BLEEDING: String
```

Allows an application to read the user's intermenstrual bleeding data.

Protection level: dangerous.

 Value: "android.permission.health.READ_INTERMENSTRUAL_BLEEDING"

### READ_LEAN_BODY_MASS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_LEAN_BODY_MASS: String
```

Allows an application to read the user's lean body mass data.

Protection level: dangerous.

 Value: "android.permission.health.READ_LEAN_BODY_MASS"

### READ_MEDICAL_DATA_ALLERGIES_INTOLERANCES

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val READ_MEDICAL_DATA_ALLERGIES_INTOLERANCES: String
```

Allows an application to read the user's data about allergies and intolerances.

Protection level: dangerous.

 Value: "android.permission.health.READ_MEDICAL_DATA_ALLERGIES_INTOLERANCES"

### READ_MEDICAL_DATA_CONDITIONS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val READ_MEDICAL_DATA_CONDITIONS: String
```

Allows an application to read the user's data about medical conditions.

Protection level: dangerous.

 Value: "android.permission.health.READ_MEDICAL_DATA_CONDITIONS"

### READ_MEDICAL_DATA_LABORATORY_RESULTS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val READ_MEDICAL_DATA_LABORATORY_RESULTS: String
```

Allows an application to read the user's laboratory result data.

Protection level: dangerous.

 Value: "android.permission.health.READ_MEDICAL_DATA_LABORATORY_RESULTS"

### READ_MEDICAL_DATA_MEDICATIONS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val READ_MEDICAL_DATA_MEDICATIONS: String
```

Allows an application to read the user's medication data.

Protection level: dangerous.

 Value: "android.permission.health.READ_MEDICAL_DATA_MEDICATIONS"

### READ_MEDICAL_DATA_PERSONAL_DETAILS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val READ_MEDICAL_DATA_PERSONAL_DETAILS: String
```

Allows an application to read the user's personal details.

This is demographic information such as name, date of birth, contact details like address or telephone number and so on. For more examples see the [FHIR Patient resource](https://www.hl7.org/fhir/patient.html).

Protection level: dangerous.

 Value: "android.permission.health.READ_MEDICAL_DATA_PERSONAL_DETAILS"

### READ_MEDICAL_DATA_PRACTITIONER_DETAILS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val READ_MEDICAL_DATA_PRACTITIONER_DETAILS: String
```

Allows an application to read the user's data about the practitioners who have interacted with them in their medical record. This is the information about the clinicians (doctors, nurses, etc) but also other practitioners (masseurs, physiotherapists, etc) who have been involved with the patient.

Protection level: dangerous.

 Value: "android.permission.health.READ_MEDICAL_DATA_PRACTITIONER_DETAILS"

### READ_MEDICAL_DATA_PREGNANCY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val READ_MEDICAL_DATA_PREGNANCY: String
```

Allows an application to read the user's pregnancy data.

Protection level: dangerous.

 Value: "android.permission.health.READ_MEDICAL_DATA_PREGNANCY"

### READ_MEDICAL_DATA_PROCEDURES

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val READ_MEDICAL_DATA_PROCEDURES: String
```

Allows an application to read the user's data about medical procedures.

Protection level: dangerous.

 Value: "android.permission.health.READ_MEDICAL_DATA_PROCEDURES"

### READ_MEDICAL_DATA_SOCIAL_HISTORY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val READ_MEDICAL_DATA_SOCIAL_HISTORY: String
```

Allows an application to read the user's social history data.

Protection level: dangerous.

 Value: "android.permission.health.READ_MEDICAL_DATA_SOCIAL_HISTORY"

### READ_MEDICAL_DATA_VACCINES

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val READ_MEDICAL_DATA_VACCINES: String
```

Allows an application to read the user's data about immunizations and vaccinations.

Protection level: dangerous.

 Value: "android.permission.health.READ_MEDICAL_DATA_VACCINES"

### READ_MEDICAL_DATA_VISITS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val READ_MEDICAL_DATA_VISITS: String
```

Allows an application to read the user's information about their encounters with health care practitioners, including things like location, time of appointment, and name of organization the visit was with. Despite the name visit it covers remote encounters such as telephone or videoconference appointments.

Protection level: dangerous.

 Value: "android.permission.health.READ_MEDICAL_DATA_VISITS"

### READ_MEDICAL_DATA_VITAL_SIGNS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val READ_MEDICAL_DATA_VITAL_SIGNS: String
```

Allows an application to read the user's vital signs data.

Protection level: dangerous.

 Value: "android.permission.health.READ_MEDICAL_DATA_VITAL_SIGNS"

### READ_MENSTRUAL_CYCLE_PHASE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 22](https://developer.android.com/sdkExtensions)

```
static val READ_MENSTRUAL_CYCLE_PHASE: String
```

Allows an application to read the user's cycle phases data.

Protection level: dangerous.

 Value: "android.permission.health.READ_MENSTRUAL_CYCLE_PHASE"

### READ_MENSTRUATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_MENSTRUATION: String
```

Allows an application to read the user's menstruation data.

Protection level: dangerous.

 Value: "android.permission.health.READ_MENSTRUATION"

### READ_MINDFULNESS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
static val READ_MINDFULNESS: String
```

Allows an application to read user's mindfulness data.

Protection level: dangerous.

 Value: "android.permission.health.READ_MINDFULNESS"

### READ_NUTRITION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_NUTRITION: String
```

Allows an application to read the user's nutrition data.

Protection level: dangerous.

 Value: "android.permission.health.READ_NUTRITION"

### READ_OVULATION_TEST

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_OVULATION_TEST: String
```

Allows an application to read the user's ovulation test data.

Protection level: dangerous.

 Value: "android.permission.health.READ_OVULATION_TEST"

### READ_OXYGEN_SATURATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_OXYGEN_SATURATION: String
```

Allows an application to read the user's oxygen saturation data.

Protection level: dangerous.

 Value: "android.permission.health.READ_OXYGEN_SATURATION"

### READ_PLANNED_EXERCISE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
static val READ_PLANNED_EXERCISE: String
```

Allows an application to read the user's training plan data.

Protection level: dangerous.

 Value: "android.permission.health.READ_PLANNED_EXERCISE"

### READ_POWER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_POWER: String
```

Allows an application to read the user's power data.

Protection level: dangerous.

 Value: "android.permission.health.READ_POWER"

### READ_RESPIRATORY_RATE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_RESPIRATORY_RATE: String
```

Allows an application to read the user's respiratory rate data.

Protection level: dangerous.

 Value: "android.permission.health.READ_RESPIRATORY_RATE"

### READ_RESTING_HEART_RATE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_RESTING_HEART_RATE: String
```

Allows an application to read the user's resting heart rate data.

Protection level: dangerous.

 Value: "android.permission.health.READ_RESTING_HEART_RATE"

### READ_SEXUAL_ACTIVITY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_SEXUAL_ACTIVITY: String
```

Allows an application to read the user's sexual activity data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SEXUAL_ACTIVITY"

### READ_SKIN_TEMPERATURE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
static val READ_SKIN_TEMPERATURE: String
```

Allows an application to read the user's skin temperature data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SKIN_TEMPERATURE"

### READ_SLEEP

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_SLEEP: String
```

Allows an application to read the user's sleep data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SLEEP"

### READ_SPEED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_SPEED: String
```

Allows an application to read the user's speed data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SPEED"

### READ_STEPS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_STEPS: String
```

Allows an application to read the user's steps data.

Protection level: dangerous.

 Value: "android.permission.health.READ_STEPS"

### READ_SYMPTOM_ABDOMINAL_PAIN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_ABDOMINAL_PAIN: String
```

Allows an application to read the user's abdominal pain data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_ABDOMINAL_PAIN"

### READ_SYMPTOM_ACNE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_ACNE: String
```

Allows an application to read the user's acne data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_ACNE"

### READ_SYMPTOM_BACK_PAIN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_BACK_PAIN: String
```

Allows an application to read the user's back pain data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_BACK_PAIN"

### READ_SYMPTOM_BLOATING

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_BLOATING: String
```

Allows an application to read the user's bloating data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_BLOATING"

### READ_SYMPTOM_BRAIN_FOG

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_BRAIN_FOG: String
```

Allows an application to read the user's brain fog data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_BRAIN_FOG"

### READ_SYMPTOM_BREAST_TENDERNESS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_BREAST_TENDERNESS: String
```

Allows an application to read the user's breast tenderness data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_BREAST_TENDERNESS"

### READ_SYMPTOM_BRITTLE_NAILS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_BRITTLE_NAILS: String
```

Allows an application to read the user's brittle nails data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_BRITTLE_NAILS"

### READ_SYMPTOM_BURNING_MOUTH

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_BURNING_MOUTH: String
```

Allows an application to read the user's burning mouth data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_BURNING_MOUTH"

### READ_SYMPTOM_CHEST_PAIN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_CHEST_PAIN: String
```

Allows an application to read the user's chest pain data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_CHEST_PAIN"

### READ_SYMPTOM_CHEST_TIGHTNESS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_CHEST_TIGHTNESS: String
```

Allows an application to read the user's chest tightness data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_CHEST_TIGHTNESS"

### READ_SYMPTOM_CHILLS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_CHILLS: String
```

Allows an application to read the user's chills data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_CHILLS"

### READ_SYMPTOM_CONSTIPATION

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_CONSTIPATION: String
```

Allows an application to read the user's constipation data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_CONSTIPATION"

### READ_SYMPTOM_COUGH

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_COUGH: String
```

Allows an application to read the user's cough symptom data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_COUGH"

### READ_SYMPTOM_CRAMPS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_CRAMPS: String
```

Allows an application to read the user's cramps data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_CRAMPS"

### READ_SYMPTOM_CRAVINGS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_CRAVINGS: String
```

Allows an application to read the user's cravings data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_CRAVINGS"

### READ_SYMPTOM_DEHYDRATION

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_DEHYDRATION: String
```

Allows an application to read the user's dehydration data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_DEHYDRATION"

### READ_SYMPTOM_DIARRHEA

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_DIARRHEA: String
```

Allows an application to read the user's diarrhea data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_DIARRHEA"

### READ_SYMPTOM_DIFFICULTY_SWALLOWING

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_DIFFICULTY_SWALLOWING: String
```

Allows an application to read the user's difficulty swallowing data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_DIFFICULTY_SWALLOWING"

### READ_SYMPTOM_DIZZINESS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_DIZZINESS: String
```

Allows an application to read the user's dizziness data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_DIZZINESS"

### READ_SYMPTOM_DRY_SKIN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_DRY_SKIN: String
```

Allows an application to read the user's dry skin data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_DRY_SKIN"

### READ_SYMPTOM_EARACHES

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_EARACHES: String
```

Allows an application to read the user's earaches data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_EARACHES"

### READ_SYMPTOM_FATIGUE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_FATIGUE: String
```

Allows an application to read the user's fatigue data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_FATIGUE"

### READ_SYMPTOM_FEVER

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_FEVER: String
```

Allows an application to read the user's fever data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_FEVER"

### READ_SYMPTOM_GENERALIZED_BODY_ACHE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_GENERALIZED_BODY_ACHE: String
```

Allows an application to read the user's generalized body ache data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_GENERALIZED_BODY_ACHE"

### READ_SYMPTOM_HAIR_LOSS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_HAIR_LOSS: String
```

Allows an application to read the user's hair loss data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_HAIR_LOSS"

### READ_SYMPTOM_HEADACHE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_HEADACHE: String
```

Allows an application to read the user's headache data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_HEADACHE"

### READ_SYMPTOM_HEARTBURN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_HEARTBURN: String
```

Allows an application to read the user's heartburn data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_HEARTBURN"

### READ_SYMPTOM_HEART_PALPITATIONS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_HEART_PALPITATIONS: String
```

Allows an application to read the user's heart palpitations data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_HEART_PALPITATIONS"

### READ_SYMPTOM_HOT_FLASHES

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_HOT_FLASHES: String
```

Allows an application to read the user's hot flashes data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_HOT_FLASHES"

### READ_SYMPTOM_INSOMNIA

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_INSOMNIA: String
```

Allows an application to read the user's insomnia data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_INSOMNIA"

### READ_SYMPTOM_JOINT_PAIN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_JOINT_PAIN: String
```

Allows an application to read the user's joint pain data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_JOINT_PAIN"

### READ_SYMPTOM_JOINT_STIFFNESS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_JOINT_STIFFNESS: String
```

Allows an application to read the user's joint stiffness data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_JOINT_STIFFNESS"

### READ_SYMPTOM_LOSS_OF_APPETITE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_LOSS_OF_APPETITE: String
```

Allows an application to read the user's loss of appetite data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_LOSS_OF_APPETITE"

### READ_SYMPTOM_LOSS_OF_CONSCIOUSNESS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_LOSS_OF_CONSCIOUSNESS: String
```

Allows an application to read the user's loss of consciousness data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_LOSS_OF_CONSCIOUSNESS"

### READ_SYMPTOM_LOWER_BACK_PAIN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_LOWER_BACK_PAIN: String
```

Allows an application to read the user's lower back pain data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_LOWER_BACK_PAIN"

### READ_SYMPTOM_MEMORY_LAPSE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_MEMORY_LAPSE: String
```

Allows an application to read the user's memory lapse data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_MEMORY_LAPSE"

### READ_SYMPTOM_MOOD_CHANGE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_MOOD_CHANGE: String
```

Allows an application to read the user's mood change data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_MOOD_CHANGE"

### READ_SYMPTOM_MUSCLE_PAIN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_MUSCLE_PAIN: String
```

Allows an application to read the user's muscle pain data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_MUSCLE_PAIN"

### READ_SYMPTOM_NAUSEA

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_NAUSEA: String
```

Allows an application to read the user's nausea data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_NAUSEA"

### READ_SYMPTOM_NIGHT_SWEATS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_NIGHT_SWEATS: String
```

Allows an application to read the user's night sweats data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_NIGHT_SWEATS"

### READ_SYMPTOM_PELVIC_PAIN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_PELVIC_PAIN: String
```

Allows an application to read the user's pelvic pain data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_PELVIC_PAIN"

### READ_SYMPTOM_RAPID_POUNDING_OR_FLUTTERING_HEARTBEAT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_RAPID_POUNDING_OR_FLUTTERING_HEARTBEAT: String
```

Allows an application to read the user's rapid, pounding, or fluttering heartbeat data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_RAPID_POUNDING_OR_FLUTTERING_HEARTBEAT"

### READ_SYMPTOM_REDUCED_CAPACITY_FOR_EXERCISE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_REDUCED_CAPACITY_FOR_EXERCISE: String
```

Allows an application to read the user's reduced capacity for exercise data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_REDUCED_CAPACITY_FOR_EXERCISE"

### READ_SYMPTOM_RUNNY_NOSE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_RUNNY_NOSE: String
```

Allows an application to read the user's runny nose data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_RUNNY_NOSE"

### READ_SYMPTOM_SHORTNESS_OF_BREATH

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_SHORTNESS_OF_BREATH: String
```

Allows an application to read the user's shortness of breath data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_SHORTNESS_OF_BREATH"

### READ_SYMPTOM_SKIPPED_HEARTBEAT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_SKIPPED_HEARTBEAT: String
```

Allows an application to read the user's skipped heartbeat data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_SKIPPED_HEARTBEAT"

### READ_SYMPTOM_SLEEPINESS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_SLEEPINESS: String
```

Allows an application to read the user's sleepiness data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_SLEEPINESS"

### READ_SYMPTOM_SLEEP_CHANGES

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_SLEEP_CHANGES: String
```

Allows an application to read the user's sleep changes data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_SLEEP_CHANGES"

### READ_SYMPTOM_SNEEZING

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_SNEEZING: String
```

Allows an application to read the user's sneezing data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_SNEEZING"

### READ_SYMPTOM_SNORE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_SNORE: String
```

Allows an application to read the user's snore data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_SNORE"

### READ_SYMPTOM_SORE_THROAT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_SORE_THROAT: String
```

Allows an application to read the user's sore throat data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_SORE_THROAT"

### READ_SYMPTOM_STOMACH_ACHE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_STOMACH_ACHE: String
```

Allows an application to read the user's stomach ache data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_STOMACH_ACHE"

### READ_SYMPTOM_STUFFY_NOSE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_STUFFY_NOSE: String
```

Allows an application to read the user's stuffy nose data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_STUFFY_NOSE"

### READ_SYMPTOM_UNEXPLAINED_WEIGHT_CHANGES

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_UNEXPLAINED_WEIGHT_CHANGES: String
```

Allows an application to read the user's unexplained weight changes data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_UNEXPLAINED_WEIGHT_CHANGES"

### READ_SYMPTOM_VAGINAL_DRYNESS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_VAGINAL_DRYNESS: String
```

Allows an application to read the user's vaginal dryness data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_VAGINAL_DRYNESS"

### READ_SYMPTOM_VAGINAL_ITCHINESS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_VAGINAL_ITCHINESS: String
```

Allows an application to read the user's vaginal itchiness data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_VAGINAL_ITCHINESS"

### READ_SYMPTOM_VOMITING

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_VOMITING: String
```

Allows an application to read the user's vomiting data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_VOMITING"

### READ_SYMPTOM_WATER_RETENTION

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_WATER_RETENTION: String
```

Allows an application to read the user's water retention data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_WATER_RETENTION"

### READ_SYMPTOM_WHEEZING

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val READ_SYMPTOM_WHEEZING: String
```

Allows an application to read the user's wheezing data.

Protection level: dangerous.

 Value: "android.permission.health.READ_SYMPTOM_WHEEZING"

### READ_TOTAL_CALORIES_BURNED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_TOTAL_CALORIES_BURNED: String
```

Allows an application to read the user's total calories burned data.

Protection level: dangerous.

 Value: "android.permission.health.READ_TOTAL_CALORIES_BURNED"

### READ_VO2_MAX

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_VO2_MAX: String
```

Allows an application to read the user's vo2 maximum data.

Protection level: dangerous.

 Value: "android.permission.health.READ_VO2_MAX"

### READ_WEIGHT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_WEIGHT: String
```

Allows an application to read the user's weight data.

Protection level: dangerous.

 Value: "android.permission.health.READ_WEIGHT"

### READ_WHEELCHAIR_PUSHES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val READ_WHEELCHAIR_PUSHES: String
```

Allows an application to read the user's wheelchair pushes data.

Protection level: dangerous.

 Value: "android.permission.health.READ_WHEELCHAIR_PUSHES"

### START_ONBOARDING

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 19](https://developer.android.com/sdkExtensions)

```
static val START_ONBOARDING: String
```

Allows an application to launch client onboarding activities responsible for connecting to Health Connect. This permission can only be held by the system. Client apps that choose to export an onboarding activity must guard it with this permission so that only the system can launch it.

See `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#ACTION_SHOW_ONBOARDING:kotlin.String` for the corresponding intent used by the system to launch onboarding activities.

Protection level: signature.

 Value: "android.permission.health.START_ONBOARDING"

### WRITE_ACTIVE_CALORIES_BURNED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_ACTIVE_CALORIES_BURNED: String
```

Allows an application to write the user's calories burned data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_ACTIVE_CALORIES_BURNED"

### WRITE_ACTIVITY_INTENSITY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val WRITE_ACTIVITY_INTENSITY: String
```

Allows an application to write the user's activity intensity data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_ACTIVITY_INTENSITY"

### WRITE_ALCOHOL_CONSUMPTION

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_ALCOHOL_CONSUMPTION: String
```

Allows an application to write user's alcohol consumption data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_ALCOHOL_CONSUMPTION"

### WRITE_BASAL_BODY_TEMPERATURE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_BASAL_BODY_TEMPERATURE: String
```

Allows an application to write the user's basal body temperature data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_BASAL_BODY_TEMPERATURE"

### WRITE_BASAL_METABOLIC_RATE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_BASAL_METABOLIC_RATE: String
```

Allows an application to write the user's basal metabolic rate data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_BASAL_METABOLIC_RATE"

### WRITE_BLOOD_GLUCOSE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_BLOOD_GLUCOSE: String
```

Allows an application to write the user's blood glucose data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_BLOOD_GLUCOSE"

### WRITE_BLOOD_PRESSURE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_BLOOD_PRESSURE: String
```

Allows an application to write the user's blood pressure data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_BLOOD_PRESSURE"

### WRITE_BODY_FAT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_BODY_FAT: String
```

Allows an application to write the user's body fat data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_BODY_FAT"

### WRITE_BODY_TEMPERATURE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_BODY_TEMPERATURE: String
```

Allows an application to write the user's body temperature data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_BODY_TEMPERATURE"

### WRITE_BODY_WATER_MASS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_BODY_WATER_MASS: String
```

Allows an application to write the user's body water mass data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_BODY_WATER_MASS"

### WRITE_BONE_MASS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_BONE_MASS: String
```

Allows an application to write the user's bone mass data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_BONE_MASS"

### WRITE_CERVICAL_MUCUS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_CERVICAL_MUCUS: String
```

Allows an application to write the user's cervical mucus data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_CERVICAL_MUCUS"

### WRITE_DEVICE_UDI

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 23](https://developer.android.com/sdkExtensions)

```
static val WRITE_DEVICE_UDI: String
```

Allows an application to write the device's unique device identifier (UDI).

Protection level: normal.

 Value: "android.permission.health.WRITE_DEVICE_UDI"

### WRITE_DISTANCE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_DISTANCE: String
```

Allows an application to write the user's distance data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_DISTANCE"

### WRITE_ELEVATION_GAINED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_ELEVATION_GAINED: String
```

Allows an application to write the user's elevation gained data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_ELEVATION_GAINED"

### WRITE_EXERCISE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_EXERCISE: String
```

Allows an application to write the user's exercise data. Additional permission `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_EXERCISE_ROUTE:kotlin.String` is required to write user's exercise route.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_EXERCISE"

### WRITE_EXERCISE_ROUTE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_EXERCISE_ROUTE: String
```

Allows an application to write the user's exercise route.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_EXERCISE_ROUTE"

### WRITE_FLOORS_CLIMBED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_FLOORS_CLIMBED: String
```

Allows an application to write the user's floors climbed data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_FLOORS_CLIMBED"

### WRITE_HEART_RATE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_HEART_RATE: String
```

Allows an application to write the user's heart rate data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_HEART_RATE"

### WRITE_HEART_RATE_VARIABILITY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_HEART_RATE_VARIABILITY: String
```

Allows an application to write the user's heart rate variability data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_HEART_RATE_VARIABILITY"

### WRITE_HEIGHT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_HEIGHT: String
```

Allows an application to write the user's height data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_HEIGHT"

### WRITE_HYDRATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_HYDRATION: String
```

Allows an application to write the user's hydration data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_HYDRATION"

### WRITE_INTERMENSTRUAL_BLEEDING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_INTERMENSTRUAL_BLEEDING: String
```

Allows an application to write the user's intermenstrual bleeding data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_INTERMENSTRUAL_BLEEDING"

### WRITE_LEAN_BODY_MASS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_LEAN_BODY_MASS: String
```

Allows an application to write the user's lean body mass data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_LEAN_BODY_MASS"

### WRITE_MEDICAL_DATA

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val WRITE_MEDICAL_DATA: String
```

Allows an application to write the user's medical data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_MEDICAL_DATA"

### WRITE_MENSTRUAL_CYCLE_PHASE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 22](https://developer.android.com/sdkExtensions)

```
static val WRITE_MENSTRUAL_CYCLE_PHASE: String
```

Allows an application to write the user's cycle phases data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_MENSTRUAL_CYCLE_PHASE"

### WRITE_MENSTRUATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_MENSTRUATION: String
```

Allows an application to write the user's menstruation data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_MENSTRUATION"

### WRITE_MINDFULNESS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
static val WRITE_MINDFULNESS: String
```

Allows an application to write user's mindfulness data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_MINDFULNESS"

### WRITE_NUTRITION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_NUTRITION: String
```

Allows an application to write the user's nutrition data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_NUTRITION"

### WRITE_OVULATION_TEST

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_OVULATION_TEST: String
```

Allows an application to write the user's ovulation test data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_OVULATION_TEST"

### WRITE_OXYGEN_SATURATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_OXYGEN_SATURATION: String
```

Allows an application to write the user's oxygen saturation data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_OXYGEN_SATURATION"

### WRITE_PLANNED_EXERCISE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
static val WRITE_PLANNED_EXERCISE: String
```

Allows an application to write the user's training plan data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_PLANNED_EXERCISE"

### WRITE_POWER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_POWER: String
```

Allows an application to write the user's power data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_POWER"

### WRITE_RESPIRATORY_RATE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_RESPIRATORY_RATE: String
```

Allows an application to write the user's respiratory rate data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_RESPIRATORY_RATE"

### WRITE_RESTING_HEART_RATE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_RESTING_HEART_RATE: String
```

Allows an application to write the user's resting heart rate data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_RESTING_HEART_RATE"

### WRITE_SEXUAL_ACTIVITY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_SEXUAL_ACTIVITY: String
```

Allows an application to write the user's sexual activity data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SEXUAL_ACTIVITY"

### WRITE_SKIN_TEMPERATURE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
static val WRITE_SKIN_TEMPERATURE: String
```

Allows an application to write the user's skin temperature data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SKIN_TEMPERATURE"

### WRITE_SLEEP

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_SLEEP: String
```

Allows an application to write the user's sleep data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SLEEP"

### WRITE_SPEED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_SPEED: String
```

Allows an application to write the user's speed data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SPEED"

### WRITE_STEPS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_STEPS: String
```

Allows an application to write the user's steps data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_STEPS"

### WRITE_SYMPTOM_ABDOMINAL_PAIN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_ABDOMINAL_PAIN: String
```

Allows an application to write the user's abdominal pain data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_ABDOMINAL_PAIN"

### WRITE_SYMPTOM_ACNE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_ACNE: String
```

Allows an application to write the user's acne data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_ACNE"

### WRITE_SYMPTOM_BACK_PAIN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_BACK_PAIN: String
```

Allows an application to write the user's back pain data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_BACK_PAIN"

### WRITE_SYMPTOM_BLOATING

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_BLOATING: String
```

Allows an application to write the user's bloating data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_BLOATING"

### WRITE_SYMPTOM_BRAIN_FOG

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_BRAIN_FOG: String
```

Allows an application to write the user's brain fog data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_BRAIN_FOG"

### WRITE_SYMPTOM_BREAST_TENDERNESS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_BREAST_TENDERNESS: String
```

Allows an application to write the user's breast tenderness data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_BREAST_TENDERNESS"

### WRITE_SYMPTOM_BRITTLE_NAILS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_BRITTLE_NAILS: String
```

Allows an application to write the user's brittle nails data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_BRITTLE_NAILS"

### WRITE_SYMPTOM_BURNING_MOUTH

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_BURNING_MOUTH: String
```

Allows an application to write the user's burning mouth data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_BURNING_MOUTH"

### WRITE_SYMPTOM_CHEST_PAIN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_CHEST_PAIN: String
```

Allows an application to write the user's chest pain data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_CHEST_PAIN"

### WRITE_SYMPTOM_CHEST_TIGHTNESS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_CHEST_TIGHTNESS: String
```

Allows an application to write the user's chest tightness data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_CHEST_TIGHTNESS"

### WRITE_SYMPTOM_CHILLS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_CHILLS: String
```

Allows an application to write the user's chills data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_CHILLS"

### WRITE_SYMPTOM_CONSTIPATION

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_CONSTIPATION: String
```

Allows an application to write the user's constipation data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_CONSTIPATION"

### WRITE_SYMPTOM_COUGH

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_COUGH: String
```

Allows an application to write the user's cough symptom data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_COUGH"

### WRITE_SYMPTOM_CRAMPS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_CRAMPS: String
```

Allows an application to write the user's cramps data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_CRAMPS"

### WRITE_SYMPTOM_CRAVINGS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_CRAVINGS: String
```

Allows an application to write the user's cravings data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_CRAVINGS"

### WRITE_SYMPTOM_DEHYDRATION

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_DEHYDRATION: String
```

Allows an application to write the user's dehydration data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_DEHYDRATION"

### WRITE_SYMPTOM_DIARRHEA

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_DIARRHEA: String
```

Allows an application to write the user's diarrhea data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_DIARRHEA"

### WRITE_SYMPTOM_DIFFICULTY_SWALLOWING

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_DIFFICULTY_SWALLOWING: String
```

Allows an application to write the user's difficulty swallowing data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_DIFFICULTY_SWALLOWING"

### WRITE_SYMPTOM_DIZZINESS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_DIZZINESS: String
```

Allows an application to write the user's dizziness data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_DIZZINESS"

### WRITE_SYMPTOM_DRY_SKIN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_DRY_SKIN: String
```

Allows an application to write the user's dry skin data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_DRY_SKIN"

### WRITE_SYMPTOM_EARACHES

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_EARACHES: String
```

Allows an application to write the user's earaches data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_EARACHES"

### WRITE_SYMPTOM_FATIGUE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_FATIGUE: String
```

Allows an application to write the user's fatigue data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_FATIGUE"

### WRITE_SYMPTOM_FEVER

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_FEVER: String
```

Allows an application to write the user's fever data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_FEVER"

### WRITE_SYMPTOM_GENERALIZED_BODY_ACHE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_GENERALIZED_BODY_ACHE: String
```

Allows an application to write the user's generalized body ache data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_GENERALIZED_BODY_ACHE"

### WRITE_SYMPTOM_HAIR_LOSS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_HAIR_LOSS: String
```

Allows an application to write the user's hair loss data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_HAIR_LOSS"

### WRITE_SYMPTOM_HEADACHE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_HEADACHE: String
```

Allows an application to write the user's headache data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_HEADACHE"

### WRITE_SYMPTOM_HEARTBURN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_HEARTBURN: String
```

Allows an application to write the user's heartburn data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_HEARTBURN"

### WRITE_SYMPTOM_HEART_PALPITATIONS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_HEART_PALPITATIONS: String
```

Allows an application to write the user's heart palpitations data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_HEART_PALPITATIONS"

### WRITE_SYMPTOM_HOT_FLASHES

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_HOT_FLASHES: String
```

Allows an application to write the user's hot flashes data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_HOT_FLASHES"

### WRITE_SYMPTOM_INSOMNIA

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_INSOMNIA: String
```

Allows an application to write the user's insomnia data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_INSOMNIA"

### WRITE_SYMPTOM_JOINT_PAIN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_JOINT_PAIN: String
```

Allows an application to write the user's joint pain data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_JOINT_PAIN"

### WRITE_SYMPTOM_JOINT_STIFFNESS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_JOINT_STIFFNESS: String
```

Allows an application to write the user's joint stiffness data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_JOINT_STIFFNESS"

### WRITE_SYMPTOM_LOSS_OF_APPETITE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_LOSS_OF_APPETITE: String
```

Allows an application to write the user's loss of appetite data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_LOSS_OF_APPETITE"

### WRITE_SYMPTOM_LOSS_OF_CONSCIOUSNESS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_LOSS_OF_CONSCIOUSNESS: String
```

Allows an application to write the user's loss of consciousness data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_LOSS_OF_CONSCIOUSNESS"

### WRITE_SYMPTOM_LOWER_BACK_PAIN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_LOWER_BACK_PAIN: String
```

Allows an application to write the user's lower back pain data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_LOWER_BACK_PAIN"

### WRITE_SYMPTOM_MEMORY_LAPSE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_MEMORY_LAPSE: String
```

Allows an application to write the user's memory lapse data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_MEMORY_LAPSE"

### WRITE_SYMPTOM_MOOD_CHANGE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_MOOD_CHANGE: String
```

Allows an application to write the user's mood change data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_MOOD_CHANGE"

### WRITE_SYMPTOM_MUSCLE_PAIN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_MUSCLE_PAIN: String
```

Allows an application to write the user's muscle pain data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_MUSCLE_PAIN"

### WRITE_SYMPTOM_NAUSEA

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_NAUSEA: String
```

Allows an application to write the user's nausea data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_NAUSEA"

### WRITE_SYMPTOM_NIGHT_SWEATS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_NIGHT_SWEATS: String
```

Allows an application to write the user's night sweats data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_NIGHT_SWEATS"

### WRITE_SYMPTOM_PELVIC_PAIN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_PELVIC_PAIN: String
```

Allows an application to write the user's pelvic pain data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_PELVIC_PAIN"

### WRITE_SYMPTOM_RAPID_POUNDING_OR_FLUTTERING_HEARTBEAT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_RAPID_POUNDING_OR_FLUTTERING_HEARTBEAT: String
```

Allows an application to write the user's rapid, pounding, or fluttering heartbeat data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_RAPID_POUNDING_OR_FLUTTERING_HEARTBEAT"

### WRITE_SYMPTOM_REDUCED_CAPACITY_FOR_EXERCISE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_REDUCED_CAPACITY_FOR_EXERCISE: String
```

Allows an application to write the user's reduced capacity for exercise data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_REDUCED_CAPACITY_FOR_EXERCISE"

### WRITE_SYMPTOM_RUNNY_NOSE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_RUNNY_NOSE: String
```

Allows an application to write the user's runny nose data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_RUNNY_NOSE"

### WRITE_SYMPTOM_SHORTNESS_OF_BREATH

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_SHORTNESS_OF_BREATH: String
```

Allows an application to write the user's shortness of breath data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_SHORTNESS_OF_BREATH"

### WRITE_SYMPTOM_SKIPPED_HEARTBEAT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_SKIPPED_HEARTBEAT: String
```

Allows an application to write the user's skipped heartbeat data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_SKIPPED_HEARTBEAT"

### WRITE_SYMPTOM_SLEEPINESS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_SLEEPINESS: String
```

Allows an application to write the user's sleepiness data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_SLEEPINESS"

### WRITE_SYMPTOM_SLEEP_CHANGES

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_SLEEP_CHANGES: String
```

Allows an application to write the user's sleep changes data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_SLEEP_CHANGES"

### WRITE_SYMPTOM_SNEEZING

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_SNEEZING: String
```

Allows an application to write the user's sneezing data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_SNEEZING"

### WRITE_SYMPTOM_SNORE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_SNORE: String
```

Allows an application to write the user's snore data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_SNORE"

### WRITE_SYMPTOM_SORE_THROAT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_SORE_THROAT: String
```

Allows an application to write the user's sore throat data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_SORE_THROAT"

### WRITE_SYMPTOM_STOMACH_ACHE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_STOMACH_ACHE: String
```

Allows an application to write the user's stomach ache data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_STOMACH_ACHE"

### WRITE_SYMPTOM_STUFFY_NOSE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_STUFFY_NOSE: String
```

Allows an application to write the user's stuffy nose data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_STUFFY_NOSE"

### WRITE_SYMPTOM_UNEXPLAINED_WEIGHT_CHANGES

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_UNEXPLAINED_WEIGHT_CHANGES: String
```

Allows an application to write the user's unexplained weight changes data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_UNEXPLAINED_WEIGHT_CHANGES"

### WRITE_SYMPTOM_VAGINAL_DRYNESS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_VAGINAL_DRYNESS: String
```

Allows an application to write the user's vaginal dryness data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_VAGINAL_DRYNESS"

### WRITE_SYMPTOM_VAGINAL_ITCHINESS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_VAGINAL_ITCHINESS: String
```

Allows an application to write the user's vaginal itchiness data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_VAGINAL_ITCHINESS"

### WRITE_SYMPTOM_VOMITING

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_VOMITING: String
```

Allows an application to write the user's vomiting data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_VOMITING"

### WRITE_SYMPTOM_WATER_RETENTION

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_WATER_RETENTION: String
```

Allows an application to write the user's water retention data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_WATER_RETENTION"

### WRITE_SYMPTOM_WHEEZING

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
static val WRITE_SYMPTOM_WHEEZING: String
```

Allows an application to write the user's wheezing data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_SYMPTOM_WHEEZING"

### WRITE_TOTAL_CALORIES_BURNED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_TOTAL_CALORIES_BURNED: String
```

Allows an application to write the user's total calories burned data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_TOTAL_CALORIES_BURNED"

### WRITE_VO2_MAX

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_VO2_MAX: String
```

Allows an application to write the user's vo2 maximum data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_VO2_MAX"

### WRITE_WEIGHT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_WEIGHT: String
```

Allows an application to write the user's weight data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_WEIGHT"

### WRITE_WHEELCHAIR_PUSHES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WRITE_WHEELCHAIR_PUSHES: String
```

Allows an application to write the user's wheelchair pushes data.

Protection level: dangerous.

 Value: "android.permission.health.WRITE_WHEELCHAIR_PUSHES"
