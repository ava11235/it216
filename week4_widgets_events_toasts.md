## Reading

zyBooks Ch 2.4 - 2.7

### Widgets and Event Handling

Widgets are used as part of the UI development of an App.  Examples of widgets include TextView, EditText and Button.

A user triggers an even with a widget. An event listener handles the event with a callback method. Technically, the event listener is an interface in the View class.

The Toast class and its makeText() and show() methods create and display a Toast, a message that pops up on the screen for a timed duration, e.g. 3 seconds.

The Button object creates a button widget in the layout. An ImageButton creates a button with a background icon and no text. Floating action button (FAB) is a circular button that appears to float about the UI and performs the primary action of the view.

Material Design is the official style guideline for Android design patterns.

The TextView widget displays text. Use the android:textXXX attributes to set various attributes of the widget, such as android:text or android:textColor.

The EditText widget is used to input text or numbers. The android:inputType specifies the data type of the input.

Several widgets are used for selecting options. They include the ToggleButton, the Switch, and the SwitchCompat for older devices.

Ther OnCheckedChangeListener and OnCheckedChanged() callback methods are triggered when the button is turned on and off.

RadioButtons, created within the RadioGroup are used to specify a single option.

CheckBox is used for checking one more option.

The Spinner is used to select an option from an array of strings.  The AdapterView.OnItemSelectedListener interface and its  onItemSelected() callback method are called  when a spinner item is selected.


## Reference

https://developer.android.com/reference/android/widget/Toast

https://developer.android.com/reference/android/widget/Button

https://developer.android.com/reference/android/widget/TextView

https://developer.android.com/reference/android/widget/EditText

https://material.io/develop/android


## Practice

zyBooks Ch 1.10,  2.4 - 2.7  Practice (graded participation activity)

## Learning Outcomes
Upon successful completion of the material, students will be able to:

* Add TextView, EditText and Button widgets to their apps.
* Handle events on the widgets
* Use Toasts in their apps
