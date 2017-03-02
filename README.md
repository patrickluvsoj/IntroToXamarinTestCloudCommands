# Intro to Xamarin Test Cloud Commands

This guide is an introduction the commands you will use and see with Xamarin Test Cloud.
The framework we will be exploring is called UITest -- written in the language of C#

You will see these commands in both Xamarin Test Recorder and in the REPL

This guide is meant as an explaination at first but then a cheat sheet that you can refer back to.
We will discuss the most commonly used commands

<ul>Common Commands Seen in Test Recorder:
<li>app.Tap();<li>
<li>app.DismissKeyboard ();</li>
<li>app.EnterText (x => x.Id ("edit_phone"), "5555555555");</li>
<li>app.PressEnter();
<li>app.ScrollUp ("CREATE", "linear_item");</li>
<li>app.ScrollDown ("CREATE", "linear_item");</li>
<li>app.ScrollDownTo ("CREATE", "linear_item");</li>
<li>app.Screenshot ("User enters phone number");</li>
<li>app.WaitForElement("button2");
</ul>

<ul>Common Notations and Terms seen in Test Recorder:
<li>app.Tap(x=>x.Marked("hello_button"));<li>
<li>app.Tap(x=>x.Class("UIButton"));</li>
<li>app.Tap(x=>x.Id("hello_button"));</li>
<li>app.Tap(x=>x.Label("hello_button"));</li>
<li>app.Tap(x=>x.Text("Hello there!"));</li>
</ul>

<ul>Common repl commands:
<li>tree</li>
<li>app.Flash("myButton");</li>
<li>app.Flash(x=>x.All("*"));</li>
<li>app.Flash(x => x.All("*").Class("UITextFieldLabel").Text("User ID"));</li>
<li>app.TapCoordinates(153, 86);</li>
<li>app.Repl ();</li>
<li>copy
</ul>

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
