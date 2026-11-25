# Ex.No:3a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

### Developed By : VIMALRAJ B
### Register Number : 212224230304
## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1:Start the application.

Step 2:Create the user interface using XML layout.

Step 3:Create an EditText to enter the URL.

Step 4:Create a Button to perform the search operation.

Step 5:Initialize the EditText and Button using findViewById().

Step 6:Set an OnClickListener() for the Button.

Step 7:Get the URL entered by the user using getText().toString().

Step 8:Create an implicit Intent using Intent.ACTION_VIEW.

Step 9:Convert the entered URL into a URI using Uri.parse().

Step 10:Pass the Intent to startActivity() to open the appropriate application.

Step 11:Android identifies a suitable application, such as a web browser, to handle the request.

Step 12:Stop

## PROGRAM:
### MainActivity.java
```java
package com.example.ex_1;

import android.os.Bundle;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
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

        button = findViewById(R.id.btn);
        editText = (EditText) findViewById(R.id.editText);

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
activity_main.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <EditText
        android:id="@+id/editText"
        android:layout_width="374dp"
        android:layout_height="60dp"
        android:background="@android:drawable/edit_text"
        android:backgroundTint="#95D3FD"
        android:hint="Enter the URL"
        android:inputType="text"
        android:padding="15dp"
        android:singleLine="true"
        android:textAlignment="center"
        android:textColor="#000000"
        android:textColorHint="#000000"
        android:textSize="20sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.432"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.326" />

    <Button
        android:id="@+id/btn"
        android:layout_width="288dp"
        android:layout_height="48dp"
        android:layout_marginTop="20dp"
        android:backgroundTint="#5146E5"
        android:text="SEARCH"
        android:textColor="#FFFFFF"
        android:textSize="16sp"
        android:textStyle="bold"
        app:cornerRadius="14dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.495"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@id/editText"
        app:layout_constraintVertical_bias="0.26" />

  </androidx.constraintlayout.widget.ConstraintLayout>
```

## OUTPUT
<img width="1535" height="1021" alt="Screenshot 2026-11-25 195739" src="https://github.com/user-attachments/assets/dcca8335-7208-4fe5-87ab-1711761650cf" />
<img width="1582" height="1017" alt="Screenshot 2026-11-25 195751" src="https://github.com/user-attachments/assets/aaaeda43-af4c-4f75-9b95-8e2252e3c1ef" />


<img width="462" height="888" alt="Screenshot 2026-11-25 195804" src="https://github.com/user-attachments/assets/1a4fd787-a23f-49b9-a51c-1cf9d14e979e" />
<img width="431" height="887" alt="Screenshot 2026-11-25 200002" src="https://github.com/user-attachments/assets/87fa521c-6936-4b78-b9d1-2e6dbb2fa3f2" />

<img width="421" height="881" alt="Screenshot 2026-11-25 200456" src="https://github.com/user-attachments/assets/733639c5-b6fd-4579-818f-c82cd6b77a8e" />

## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


