# Challenge: Reading Java Source

We have an actual application to inspect. With a partner or a small group, pair up and identify each piece of Java source code.

## Importing Libraries and Tools


```java
package com.example.codeforcoffee.myapplication;
import android.os.Bundle;
import android.support.v7.app.AppCompatActivity;
import android.support.v7.widget.Toolbar;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
```

## Defining an App's MainActivity

```java
public class MainActivity extends AppCompatActivity {
    // define some UI elements - EditText is a text input,
    // TextView is a label, Button is a ... button
    final EditText firstNumber = (EditText) findViewById(R.id.editText);
    final EditText secondNumber = (EditText) findViewById(R.id.editText2);
    final TextView output = (TextView) findViewById(R.id.textView1);
    final Button button = (Button) findViewById(R.id.button);
}
```

## Doing Math

```java
// declare an addNumbers method with a return type of Float
// accepts two Floats as arguments
protected Float addNumbers(float int1, float int2) {
    // adds the together and returns them
    Float ret = int1 + int2;
    return ret;
}
```

## Listening to Click Events

```java
@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    // create application view
    setContentView(R.layout.activity_main);
    // create toolbar (menu bar)
    Toolbar toolbar = (Toolbar) findViewById(R.id.toolbar);
    setSupportActionBar(toolbar);
    // listen for button clicks...
    button.setOnClickListener(new View.OnClickListener() {
        // button.onClick
        public void onClick(View v) {
            // convert EditText's content to String and parse the result as a Float
            Float val1 = Float.parseFloat(firstNumber.getText().toString());
            // repeat
            Float val2 = Float.parseFloat(secondNumber.getText().toString());
            // update the text for our output...
            output.setText(addNumbers(val1, val2).toString());
        }
    });
}
```
