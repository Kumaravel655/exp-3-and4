
# Ex.No:4 Design an android application Send SMS using Intent.

## AIM:

To create and design an android application Send SMS using Intent using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “ex.no.4″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Send SMS and Display details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:

```
/*
Program to create and design an android application Send SMS using Intent.
Developed by:KUMARAVEL V
Registeration Number : 212220230027
*/
```
### MainActivity.java


```
package com.example.bala1;

import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Button mButton= (Button) findViewById(R.id.send_sms);
        mButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent=new Intent(Intent.ACTION_VIEW, Uri.fromParts("sms","+916369472659",null));
                intent.putExtra("sms_body","hii am kumaravel!!!");
                startActivity(intent);
            }
        });
    }
}
```
### activity_main.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="sms available now "
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.478" />

    <Button
        android:id="@+id/send_sms"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="send sms"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.6" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

## OUTPUT:
![Screenshot (6)](https://user-images.githubusercontent.com/75235334/165929226-6e510a40-615e-435c-919b-87a7b571d6a7.png)
![Screenshot (7)](https://user-images.githubusercontent.com/75235334/165929236-8b2d3d92-ec17-4a50-a758-f80523650e44.png)
![Screenshot (8)](https://user-images.githubusercontent.com/75235334/165929280-b3511073-65b0-4e15-8931-ddf7bad7faa7.png)

## RESULT:

Thus a Simple Android Application create and design an android application Send SMS using Intent using Android Studio is developed and executed successfully.
