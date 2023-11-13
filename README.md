
## Ex.No:3 Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.
## AIM:
To create a navigate button using Implicit Intent to display the google page using Android Studio. 

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project. 

Step 2: Then type the Application name as HelloWorld and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next. 

Step 4: Then select the Empty Activity and click Next. Finally click Finish. 

Step 5: Design layout in activity_main.xml 

Step 6: Display message give in MainActivity file. 

Step 7: Save and run the application

## PROGRAM:
/*
Program to print the text “Implicitintent”.

Developed by:Kulaganachi.R

Registeration Number :212221040086
*/
## Activity_main.xml
~~~
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:app="http://schemas.android.com/apk/res-auto"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context=".MainActivity">
 <Button
 android:id="@+id/button"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_marginEnd="48dp"
 android:text="NAVIGATE"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.219" />
 <EditText
 android:id="@+id/editTextTextPersonName"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_marginStart="32dp"
 android:ems="10"
 android:inputType="textPersonName"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.218" />
</androidx.constraintlayout.widget.ConstraintLayout>
~~~
## MainActivity.java
~~~
package com.example.ex3;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
import android.widget.Button;
import android.widget.EditText;
import android.os.Bundle;
public class MainActivity extends AppCompatActivity {
 Button button;
 EditText editText;
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 button = findViewById(R.id.button);
 editText = findViewById(R.id.editTextTextPersonName);
 button.setOnClickListener(view -> {
 String url=editText.getText().toString();
 Intent intent=new Intent(Intent.ACTION_VIEW, Uri.parse(url));
 startActivity(intent);
 });
 } }
~~~
## Output

![image](https://github.com/Kulaganachi/Implicit_explicit/assets/133641126/14da9bbe-d921-4f59-ae40-20ac9810a40c)


![image](https://github.com/Kulaganachi/Implicit_explicit/assets/133641126/7bacd308-c539-4ebe-871f-b021876e9331)



## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.
