
## Reading

zyBooks Ch 3.4 - 3.6

### Spinner Widget

The Spinner widget allows for selecting a value from a drop down list. 
Interacting with the spinner displays a dropdown menu of available options. 
By default the Spinner shows the currently selected option.
 
### Steps to add a Spinner to your app:
 
1. To create a Spinner,  you need to add a <Spinner> to the XML layout.

``` <Spinner
    android:id="@+id/planets_spinner"
    android:layout_width="match_parent"
    android:layout_height="wrap_content" />
 ```
 
2. A Spinner's options are defined in an array in the strings.xml resource file. 
 
```
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <string-array name="planets_array">
        <item>Mercury</item>
        <item>Venus</item>
        <item>Earth</item>
        <item>Mars</item>
        <item>Jupiter</item>
        <item>Saturn</item>
        <item>Uranus</item>
        <item>Neptune</item>
    </string-array>
</resources>
```

3. In the Activity Java file use an instance of ArrayAdapter to supply the Spinner with the options from the array.
 

```Spinner spinner = (Spinner) findViewById(R.id.spinner);
// Create an ArrayAdapter using the string array and a default spinner layout
ArrayAdapter<CharSequence> adapter = ArrayAdapter.createFromResource(this,
        R.array.planets_array, android.R.layout.simple_spinner_item);
// Specify the layout to use when the list of choices appears
adapter.setDropDownViewResource(android.R.layout.simple_spinner_dropdown_item);
// Apply the adapter to the spinner
spinner.setAdapter(adapter);
 ```
 
4. When the user selects an item from the drop-down, the Spinner object receives an on-item-selected event.
To define the selection event handler for a spinner, implement the AdapterView.OnItemSelectedListener interface 
and the corresponding onItemSelected() callback method. 
For example, here's an implementation of the interface in an Activity:

``` public class SpinnerActivity extends Activity implements OnItemSelectedListener {
    ...
 
    public void onItemSelected(AdapterView<?> parent, View view,
            int pos, long id) {
        // An item was selected. You can retrieve the selected item using
        // parent.getItemAtPosition(pos)
    }
 
    public void onNothingSelected(AdapterView<?> parent) {
        // Another interface callback
    }
}
The AdapterView.OnItemSelectedListener requires the onItemSelected() and onNothingSelected() callback methods.
Then you need to specify the interface implementation by calling setOnItemSelectedListene
Spinner spinner = (Spinner) findViewById(R.id.spinner);
spinner.setOnItemSelectedListener(this);
 
``` 

### Example: UnitConverter App

Feel free to use as starter code for your homework, or challenge yourself and try coding the project from scratch.

![Unit Converstion](https://github.com/ava11235/UnitConverter/blob/main/conversion.JPG)

Code:
https://github.com/ava11235/UnitConverter


## Reference

https://developer.android.com/guide/topics/ui/controls/spinner

## Practice

zyBooks Ch 3.4 - 3.6 Practice (graded participation activity)

## Learning Outcomes
Upon successful completion of the material, students will be able to:

* Add a Spinner widget to their layouts and interact with the Spinner items from Java

