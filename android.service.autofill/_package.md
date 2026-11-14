# android.service.autofill

Kotlin | [Java](_package.md)
| --- | --- |

## Interfaces

| [OnClickAction](OnClickAction.md) | Class used to define an action to be performed when a child view in a `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#` is clicked. |
| --- | --- |
| [Sanitizer](Sanitizer.md) | Helper class used to sanitize user input before using it in a save request. |
| [SavedDatasetsInfoCallback](SavedDatasetsInfoCallback.md) | Handles the response to `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onSavedDatasetsInfoRequest(android.service.autofill.SavedDatasetsInfoCallback)`. |
| [Transformation](Transformation.md) | Helper class used to change a child view of a `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#` at runtime, using the values of fields contained in the screen. |
| --- | --- |
| [Validator](Validator.md) | Class used to define whether a condition is satisfied. |

## Classes

| [AutofillService](AutofillService.md) | An `AutofillService` is a service used to automatically fill the contents of the screen on behalf of a given user - for more information about autofill, read [Autofill Framework](https://developer.android.com/preview/features/autofill.html). |
| --- | --- |
| [BatchUpdates](BatchUpdates.md) | Defines actions to be applied to a `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#`. |
| [CharSequenceTransformation](CharSequenceTransformation.md) | Replaces a `https://developer.android.com/reference/kotlin/android/widget/TextView.html#` child of a `https://developer.android.com/reference/kotlin/android/service/autofill/CustomDescription` with the contents of one or more regular expressions (regexs). |
| [CustomDescription](CustomDescription.md) | Defines a custom description for the autofill save UI. |
| --- | --- |
| [Dataset](Dataset.md) | A `Dataset` object represents a group of fields (key / value pairs) used to autofill parts of a screen. |
| [DateTransformation](DateTransformation.md) | Replaces a `https://developer.android.com/reference/kotlin/android/widget/TextView.html#` child of a `https://developer.android.com/reference/kotlin/android/service/autofill/CustomDescription` with the contents of a field that is expected to have a `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#forDate(kotlin.Long)`. |
| [DateValueSanitizer](DateValueSanitizer.md) | Sanitizes a date `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#` using a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.html#`. |
| --- | --- |
| [Field](Field.md) | This class is used to set all information of a field. |
| [FieldClassification](FieldClassification.md) | Represents the [field classification](AutofillService.md) results for a given field. |
| [FillCallback](FillCallback.md) | `FillCallback` handles autofill requests from the `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService` into the `https://developer.android.com/reference/kotlin/android/app/Activity.html#` being autofilled. |
| --- | --- |
| [FillContext](FillContext.md) | This class represents a context for each fill request made via `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onFillRequest(android.service.autofill.FillRequest,%20android.os.CancellationSignal,%20android.service.autofill.FillCallback)`. |
| [FillEventHistory](FillEventHistory.md) | Describes what happened after the last `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onFillRequest(android.service.autofill.FillRequest,%20android.os.CancellationSignal,%20android.service.autofill.FillCallback)` call. |
| [FillRequest](FillRequest.md) | This class represents a request to an autofill service to interpret the screen and provide information to the system which views are interesting for saving and what are the possible ways to fill the inputs on the screen if applicable. |
| --- | --- |
| [FillResponse](FillResponse.md) | Response for an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onFillRequest(android.service.autofill.FillRequest,%20android.os.CancellationSignal,%20android.service.autofill.FillCallback)`. |
| [ImageTransformation](ImageTransformation.md) | Replaces the content of a child `https://developer.android.com/reference/kotlin/android/widget/ImageView.html#` of a `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#` with the first image that matches a regular expression (regex). |
| [InlinePresentation](InlinePresentation.md) | Wrapper class holding a `https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#` and an `https://developer.android.com/reference/kotlin/android/widget/inline/InlinePresentationSpec.html#` for rendering UI for an Inline Suggestion. |
| --- | --- |
| [LuhnChecksumValidator](LuhnChecksumValidator.md) | Validator that returns `true` if the number created by concatenating all given fields pass a Luhn algorithm checksum. |
| [Presentations](Presentations.md) | Holds presentations used to visualize autofill suggestions for each available UI type. |
| [RegexValidator](RegexValidator.md) | Defines if a field is valid based on a regular expression (regex). |
| --- | --- |
| [SaveCallback](SaveCallback.md) | Handles save requests from the `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService` into the `https://developer.android.com/reference/kotlin/android/app/Activity.html#` being autofilled. |
| [SavedDatasetsInfo](SavedDatasetsInfo.md) | A result returned from `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onSavedDatasetsInfoRequest(android.service.autofill.SavedDatasetsInfoCallback)`. |
| [SaveInfo](SaveInfo.md) | Information used to indicate that an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService` is interested on saving the user-inputed data for future use, through a `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onSaveRequest(android.service.autofill.SaveRequest,%20android.service.autofill.SaveCallback)` call. |
| --- | --- |
| [SaveRequest](SaveRequest.md) | This class represents a request to an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService` to save applicable data entered by the user. |
| [TextValueSanitizer](TextValueSanitizer.md) | Sanitizes a text `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#` using a regular expression (regex) substitution. |
| [UserData](UserData.md) | Defines the user data used for [field classification](AutofillService.md). |
| --- | --- |
| [Validators](Validators.md) | Factory for `https://developer.android.com/reference/kotlin/android/service/autofill/Validator` operations. |
| [VisibilitySetterAction](VisibilitySetterAction.md) | Action used to change the visibility of other child view in a `https://developer.android.com/reference/kotlin/android/service/autofill/CustomDescription` `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#`. |
