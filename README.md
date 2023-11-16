# Ex.No:3 Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the google page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
Step1:Open Android Studio and create a new project.

Step2:In the activity_main.xml file, design the layout with a TextInputEditText element for the text field and a Button element for the "Navigate" button.

Step3:In the MainActivity.java file, retrieve references to the text field and the button using their IDs.

Step4:Set an OnClickListener for the button.

Step5:Inside the OnClickListener, retrieve the text entered in the text field using the getText() method.

Step6:Create an Intent object to open a web page with the URL obtained from the text field.

Step7:Set the action of the intent to Intent.ACTION_VIEW to indicate that the intent is used for viewing something.

Step8:Set the data of the intent to the URL obtained from the text field using the Uri.parse() method.

Step9:Set the type of the intent to "text/html" or "text/plain" to specify the type of data being viewed.

Step10:Use the startActivity() method with the intent to start the activity that can handle the implicit intent.

Step11:Run the application on an Android device or emulator to see the desired functionality.


## PROGRAM:
```
Developed By: Rajesh K
Reg.No:212221220041
```
## activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <Button
        android:id="@+id/button2"
        android:layout_width="102dp"
        android:layout_height="56dp"
        android:layout_marginBottom="300dp"
        android:text="Click"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:fontFamily="@font/cinzel_decorative_black"
        android:text="Enter your URL"
        android:textAppearance="@style/TextAppearance.AppCompat.Large"
        app:layout_constraintBottom_toTopOf="@+id/button2"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <EditText
        android:id="@+id/editTextText3"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:ems="10"
        android:inputType="text"
        android:textAppearance="@style/TextAppearance.AppCompat.Large"
        app:layout_constraintBottom_toTopOf="@+id/button2"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivity.java
```
package com.example.implict1;

import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        EditText editText;
        Button button;
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        button = findViewById(R.id.button2);
        editText = (EditText) findViewById(R.id.Text);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String url=editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }
        });
    }
}
```

## OUTPUT
![image](https://github.com/JaganSivakumaran/Implicitintent/assets/134905062/810e1d20-f2ed-41e4-92d8-17b14f6ad29f)
![image](https://github.com/JaganSivakumaran/Implicitintent/assets/134905062/71392dd0-7143-40e3-bb06-3d253a07fe07)





## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.
