Functions in activity.kt / all methods
// get reference to button[findViewById]
(when kotlinx.android..synthetic.main.activity_main.*) isn’t imported 
Or else there is no need to use the findviewbyid method...directly button can be used to set all different properties as well action using the id of the button...can also be used to set different properties for different attributes like..) 
 
 
 
val btn_click_me = findViewById(R.id.btn_click_me)    // as Button
// set on-click listener
btn_click_me.setOnClickListener {
//this pops up when the button is pressed
    Toast.makeText(this@MainActivity, "You clicked me.",Toast.LENGTH_SHORT).show()
}
setOnClickListener method :setOnClickListener method to trigger an action when the button is clicked.







When  kotlinx.android..synthetic.main.activity_main.* this is not imported then we need to first give a reference to that button and and we can use setonclicklistener method and define action to be done by the button on clicking the button 

package com.tutorialkart.myapplication
import android.support.v7.app.AppCompatActivity
import android.os.Bundle
import android.widget.Button
import android.widget.Toast
 
class MainActivity : AppCompatActivity() {
 
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
 
        // get reference to button
        val btn_click_me = findViewById(R.id.btn_click_me) as Button
        // set on-click listener
        btn_click_me.setOnClickListener {
            // your code to perform when the user clicks on the button
            Toast.makeText(this@MainActivity, "You clicked me.", Toast.LENGTH_SHORT).show()
        }
    }
}
 












When kotlinx.android.synthetic.main.activity_main.* is used 
We can use modify or set the action or properties of different attributes  of button textview and all that without referencing them using findviewbyid method...
 
 
package com.tutorial kart.disable all caps in button
import android.support.v7.app.AppCompatActivity
import android.os.Bundle
import kotlinx.android.synthetic.main.activity_main.*
 
class MainActivity : AppCompatActivity() {
 
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        btn.text = “hello”  // btn is id here 
    }
}





 
 
exp4j dependency to the project by adding implementation 'net.objecthunter:exp4j:0.4.8' to the dependencies in build.gradle. This library is used to evaluate the input in the String format
  Dependencies and library to be used..
Implementation 'net.objecthunter:exp4j:0.4.8 // added in dependencies to use to expressionbuilder to evaluate the input in string format
import net.objecthunter.exp4j.ExpressionBuilder
Then use evaluate ()  to evaluate the expression by expressionbuilder 
 





How to calculate the output is defined in the onEqual function.
We have ensured that the TextView will always show a valid input expression (For example, it may be 20*5+3). It is highly complex to extract the operands and operators from this input. This is where the Exp4j library becomes a lifesaver. Exp4j library can process an expression in String format and return the result. Therefore, in the onEquals method, we feed the String value of the txtInput.text to the ExpressionBuilder and evaluate the result.






To use this solve to set a value we need to make function fun solve(String: string, del : boolean){
// here we write the action to be performed on when this function called is called  ….it sets two value cause two arguments and del is true so that if condition can  be executed and perform the action needed

}


package com.example.calculator

import android.appcompat.app.AppCompatActivity
import android.os.Bundle
import kotlinx.android.synthetic.main.activity_main.*
import android.widget.Button
import net.objecthunter.exp4j.ExpressionBuilder

class MainActivity : AppCompatActivity() {
   override fun onCreate(savedInstanceState: Bundle?) {
       super.onCreate(savedInstanceState)
       setContentView(R.layout.activity_main)


one.setOnClickListener {
   solve("1", del = true)   //  two arguments passed na it will set 1 as text on clicking the button with id one 
}

two.setOnClickListener {
   solve("2", del = true)
}

three.setOnClickListener {
   solve("3", del = true)
}
four.setOnClickListener {
   solve("4", del = true)
}

five.setOnClickListener {
   solve("5", del = true)
}

six.setOnClickListener {
   solve("6", del = true)
}

seven.setOnClickListener {
   solve("7", del = true)
}

eight.setOnClickListener {
   solve("8", del = true)
}

nine.setOnClickListener {
   solve("9", del = true)
}

zero.setOnClickListener {
   solve("0", del = true)
}

/*Operators*/

plus.setOnClickListener {
   solve("+", del = true)
}

minus.setOnClickListener {
   solve("-", del = true)
}

divide.setOnClickListener {
   solve("/", del = true)
}

star.setOnClickListener {
   solve("*", del = true)
}



equal.setOnClickListener {
   val text = exp.text.toString()
   val expression = ExpressionBuilder(text).build() // Create an Expression (A class from exp4j library)

   val r = expression.evaluate() // to evaluate the arithmetic operations on inputs given and the expression created by ExpressionBuilder(text).build()

   val longResult = r.toLong()
   if (r == longResult.toDouble()) {
       result.text ="= "+ longResult.toString()
   }
   else {
       result.text= "= "+ r.toString()
   }

}


-----------------------------------------------------------------------
This is the solve function which do the appending job...wherever any button is clicked this function is called

private fun solve(string: String, del: Boolean) {
   if(del) {
       result.text = ""
       exp.append(string)  // will do the job of appending the value whenever any button or any operator buttons are clicked ...
   } else {
       exp.append(result.text)
       exp.append(string)
       result.text = ""
   }





In Android, the OnClickListener() interface has an onClick(View v) method that is called when the view (component) is clicked. The code for a component's functionality is written inside this method, and the listener is set using the setOnClickListener() method.


To define the click event handler for a button, add the android:onClick attribute to the <Button> element in your XML layout. The value for this attribute must be the name of the method you want to call in response to a click event. The Activity hosting the layout must then implement the corresponding method.

If you have more than one button click event, you can use switch case to identify which button is clicked. Link the button from the XML by calling findViewById() method and set the onClick listener by using setOnClickListener() method. setOnClickListener takes an OnClickListener object as the parameter.

































--------------------------------------------------------------------------------------------------------------------------
Imported libraries/dependencies(gradle)


how to use kotlinx.android.synthetic.main.activity_main.*
build.gradle(module x.app) then paste the code below and syn the gradle...

apply plugin: 'com.android.application'
apply plugin: 'kotlin-android'
apply plugin: 'kotlin-android-extensions'



to  import net.objecthunter.exp4j.ExpressionBuilder

include this in gradle/dependencies
implementation 'net.objecthunter:exp4j:0.4.8'







How to create an apk...
To create an apk 
Click build as an apk 

   


Location where we have out apk
C:\Users\wasif\AndroidStudioProjects\appname\app\build\outputs\apk













How to make or change the default apk icon/app icon

Go to res ->mipmap 
Right click and new->image asset 
The make changes…



Then click next to overwrite the already present default icon...




--------------------------------------------------------------------------------------------------------------------------
How to reduce size of app
Reduce size of image…
Way 1
Converting the image imported to WebP

