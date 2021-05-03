## Reading

zyBooks Ch 2.9, 2.10, 3.1 - 3.3

### Styles and Themes

A style is a collection of attributes such as font size, font color or background color that is applied to a View.
 
A theme is a collection of attributes that's applied to an entire app or activity. 

Styles and themes are declared in the resource file  res/values/styles.xml.

![themes](https://github.com/ava11235/it216/blob/main/themes.JPG)


### Activity Lifecycle

The activity lifecycle of an app goes through different states from when the app is created to when it is destroyed.
The Activity class provides six callback methods to call as the activity enters new states: onCreate(), onStart(), onResume(), onPause(), onStop(), and onDestroy().

The onCreate() method is called when the activity is first started.

The onStart() method is called after onCreate() as the activity is prepared to be visible. 

The onResume() method is called when the activity enters the foreground.

The onPause() method is called when the activity pauses but is still visible.

The onStop() method is called after onPause() when the activity is stopped and no longer visible.

The onDestroy() method is called after onStop() and  before the activity is destroyed.

![activity lifecycle](https://github.com/ava11235/it216/blob/main/activity-lifecycle.JPG)

### Saving and restoring activity state

As the activity begins to stop, the system calls the onSaveInstanceState() method to save its state to an instance state bundle. 
The default implementation of the method saves information about the state of the activity's sych as the text in an EditText widget or the scroll position of a ListView widget.
To save additional instance state information for your activity, you must override onSaveInstanceState() and add key-value pairs to the Bundle object. 
If you override onSaveInstanceState(), you must call the superclass implementation so that the state of the view hierarchy is saved.

```
static final String STATE_SCORE = "playerScore";
static final String STATE_LEVEL = "playerLevel";
// ...


@Override
public void onSaveInstanceState(Bundle savedInstanceState) {
    // Save the user's current game state
    savedInstanceState.putInt(STATE_SCORE, currentScore);
    savedInstanceState.putInt(STATE_LEVEL, currentLevel);

    // Always call the superclass so it can save the view hierarchy state
    super.onSaveInstanceState(savedInstanceState);
}
```


## Reference
https://developer.android.com/guide/topics/ui/look-and-feel/themes

https://developer.android.com/guide/components/activities/activity-lifecycle

https://developer.android.com/guide/components/activities/activity-lifecycle#saras


## Practice

zyBooks Ch 2.9, 2.10, 3.1 - 3.3 Practice (graded participation activity)

## Learning Outcomes
Upon successful completion of the material, students will be able to:

* Use style attributes to enhance the visual appearance of their apps.
* Apply themes (collections of styles) to activities or entire apps.
* Apply knowledge of the activity lifecycle methods to their apps.
* Save and restore app data as needed during the activity lifecycle.
