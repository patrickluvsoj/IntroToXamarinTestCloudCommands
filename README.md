# Intro to Xamarin Test Cloud Commands

This guide is an introduction the commands you will use and see with Xamarin Test Cloud.
The framework we will be exploring is called UITest -- written in the language of C#

You will see these commands in both Xamarin Test Recorder and in the REPL

This guide is meant as an explaination at first but then a cheat sheet that you can refer back to.
We will discuss the most commonly used commands

Definitions of the Commands Seen in Test Recorder:
1. app.Tap("button1"); 
* app.Tap("button1") is the most common guesture you'll use.  It mimics a user's tap on the app.  The "button1" represent a button marked with a "button1" id or label.
2. app.EnterText (x => x.Id ("edit_phone"), "Type this");</li>
* Use this command to enter text.  In the above command - the keyboard will type out "Type this" into a UIElement with the ID "edit_phone"
3. app.PressEnter();
* this is one way to submit the text you typed with EnterText - however, in some cases, you may want to dismiss the keyboard and press a Submit button 
4. app.DismissKeyboard();
* this is how you dismiss your keyboard after you enter text
5. app.WaitForElement("button2")
* this is how you get your test to wait for a particular element for up to 90 seconds.  This is really important when your app needs to do a lot of web requests or if the app takes some time to process your requests.  Rather than failing if the element doesn't appear right away, it will wait up to 90 seconds for the element to appear.  This is important when doing your local tests but even more important when you're doing your tests on the Xamarin Test Cloud.
6. app.Screenshot("User enters phone number")
* this is how you tell your application to take a screenshot -- in the Xamarin Test Cloud UI, each step will be denoted by the text you write in this method.  In the above case, it will be "User enters phone number" -- and the Xamarin Test Cloud web page will show a screenshot of your application.


<ul>Definitions of the Commands Seen in Test Recorder:
<li>app.Tap("button1"); 
* app.Tap("button1") is the most common guesture you'll use.  It mimics a user's tap on the app.  The "button1" represent a button marked with a "button1" id or label.
<li>app.DismissKeyboard ();</li>
<li>app.EnterText (x => x.Id ("edit_phone"), "5555555555");</li>
<li>app.PressEnter();
<li>app.ScrollUp ("CREATE", "linear_item");</li>
<li>app.ScrollDown ("CREATE", "linear_item");</li>
<li>app.ScrollDownTo ("CREATE", "linear_item");</li>
<li>app.Screenshot ("User enters phone number");</li>
<li>app.WaitForElement("button2");
</ul>



----
<ul>Common Notations and Terms seen in Test Recorder:
<li>app.Tap(x=>x.Marked("hello_button"));
<li>app.Tap(x=>x.Class("UIButton"));</li>
<li>app.Tap(x=>x.Id("hello_button"));</li>
<li>app.Tap(x=>x.Label("hello_button"));</li>
<li>app.Tap(x=>x.Text("Hello there!"));</li>
</ul>
----
<ul>Common repl commands:
<li>tree</li>
<li>app.Flash("myButton");</li>
<li>app.Flash(x=>x.All("*"));</li>
<li>app.Flash(x => x.All("*").Class("UITextFieldLabel").Text("User ID"));</li>
<li>app.TapCoordinates(153, 86);</li>
<li>app.Repl ();</li>
<li>copy
</ul>
----
<ul>
Common UI commands:
<li>app.DismissKeyboard ();</li>
<li>app.Screenshot ("User enters phone number");</li>
<li>app.EnterText (x => x.Id ("edit_phone"), "5555555555");</li>
<li>app.ScrollDownTo ("CREATE", "linear_item");</li>
<li>app.SwipeRightToLeft (c => c.Id ("txt_title"));</li>
<li>app.DragCoordinates (200, 400, 200, 800); // (from X, from Y, to X, to Y)</li>
<li>app.Query(x=>x.Class("FormsTextView").Index(0)) </li>
</ul>
<ul>
