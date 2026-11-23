# WORKSHOP : ANDROID ADDITION OF TWO NUMBERS 
## NAME : SHREYESHKAR SEKAR
## REGISTRATION NUMBER : 212224220099

## AIM:

To develop a program to develop a simple calculator in Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min.required Artic Fox)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as calculator and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout using UI components in activity_main.xml.

Step 6: Display the calculator operation in MainActivity file.

Step 7: Save and run the application.


## PROGRAM :

Mainactivity.java

```
package com.example.addition;

import android.os.Bundle;
import android.widget.EditText;
import android.widget.Button;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText num1, num2, result;
    Button addBtn;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        num1 = findViewById(R.id.num1);
        num2 = findViewById(R.id.num2);
        result = findViewById(R.id.result);
        addBtn = findViewById(R.id.addBtn);

        addBtn.setOnClickListener(v -> {
            double a = Double.parseDouble(num1.getText().toString());
            double b = Double.parseDouble(num2.getText().toString());

            double sum = a + b;
            result.setText(String.valueOf(sum));
        });
    }
}
```

activity_main.xml

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp"
    android:gravity="center">

    <EditText
        android:id="@+id/num1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter first number"
        android:inputType="numberDecimal"/>

    <EditText
        android:id="@+id/num2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter second number"
        android:inputType="numberDecimal"/>

    <Button
        android:id="@+id/addBtn"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Add"/>

    <EditText
        android:id="@+id/result"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Result"
        android:focusable="false"
        android:inputType="numberDecimal"/>

</LinearLayout>
```
## OUTPUT :

<img width="1917" height="1137" alt="Screenshot 2026-11-20 143028" src="https://github.com/user-attachments/assets/c42ec238-fc3a-4b3b-b9ae-d1a7dc531979" />


<img width="1917" height="1133" alt="Screenshot 2026-11-20 143101" src="https://github.com/user-attachments/assets/4caefcb4-ecc2-4e3e-a636-0b3d62f8b886" />

## RESULT :
Thus a Simple Android Application develop a program to create simple addition in Android Studio is developed and executed successfully.
