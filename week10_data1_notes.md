## Reading

zyBooks Ch 6.1 - 6.3

## Shared Preferences

One of the several ways Android provides for storing the data of an application is Shared Preferences.

Shared Preferences allow you to save and retrieve the data as a key,value pair. 


This is accomplished by calling a method getSharedPreferences().
The  SharedPreference instance points to the file containing the values.

```
SharedPreferences sharedpreferences = getSharedPreferences(MyPREFERENCES, Context.MODE_PRIVATE);
```

The first parameter is the key and the second parameter is the MODE. 

Commonly, the mode is PRIVATE, but there are other mode options as well. 

MODE_APPEND This will append the new preferences with the already existing preferences

MODE_ENABLE_WRITE_AHEAD_LOGGING Database open flag. When it is set , it would enable write ahead logging by default

MODE_MULTI_PROCESS This method will check for modification of preferences even if the sharedpreference instance has already been loaded

MODE_PRIVATEBy setting this mode, the file can only be accessed using calling application

MODE_WORLD_READABLE This mode allows other application to read the preferences

MODE_WORLD_WRITEABLE This mode allow other application to write the preferences


To save a key value pair, use the SharedPreferences.Editor class:

```
Editor editor = sharedpreferences.edit();editor.putString("key", "value");editor.commit();
```

Other methods available in the editor class that allow manipulation of data inside shared preferences include: 


*apply()* This is an abstract method. Commit your changes back from editor to the sharedPreference object you are calling

*clear()* Remove all values from the editor

*remove(String key)* Remove the value whose key has been passed as a parameter

*putLong(String key, long value)* Save a long value in a preference editor

*putInt(String key, int value)* Save a integer value in a preference editor

*putFloat(String key, float value)* Save a float value in a preference editor


### Working with Files

Android provides several types of storage for application data, such as shared preferences, internal and external storage, SQLite database, or the cloud.

By default application files are private and can only be accessed by the application.  The files are deleted when the user deletes the application.

To write data to a file, call the openFileOutput() method with the name of the file and the mode. 
The mode can be private , public.

```
FileOutputStream fOut = openFileOutput("myfile",MODE_PRIVATE);
```

The method openFileOutput() returns an instance of FileOutputStream which has the write method to write data on the file:

```
String str = "some text";
fOut.write(str.getBytes());
fOut.close();
```

To read from the file,  call the openFileInput() method with the name of the file.
It returns an instance of FileInputStream.

```
FileInputStream fin = openFileInput(file);
```

To read one character at a time from the file and then you can print it, use:

```
int c;
String temp="";
while( (c = fin.read()) != -1){

  temp = temp + Character.toString((char)c);

} //string temp contains all the data of the file.

fin.close();
```

Additional  methods are provided by the FileOutputStream. 


### Examples:
Todo List app (zyBooks)


## Reference
https://developer.android.com/reference/android/content/SharedPreferences

https://developer.android.com/guide/topics/data/


## Practice

zyBooks Ch 5.1 - 6.3 Practice (graded participation activity)

## Learning Outcomes
Upon successful completion of the material, students will be able to:

* Identify different strategies for saving data
* Working with shared preferences to store key value pairs
* Identify Android internal and external storage areas.* Save to internal and external storage
