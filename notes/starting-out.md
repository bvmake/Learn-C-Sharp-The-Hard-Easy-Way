#Starting Line
Let's get started. You are going to need a few things and going to have to do some small chores before we can start coding in C#.

The first thing we'll need is LINQPad. It is a program that you can type C# code into and test it to see if it works. You can download it from [this page](http://www.linqpad.net/). The "Low Impact Setup" for .NET 4.0 (referred to as FW 4.0 on the linqpad site) is recommended.

#Let's Get Expressive
Once LINQPad is installed on your computer, run it by clicking on the desktop icon (or on LINQPad.exe if you downloaded the zip file).

You should be presented with a window that says "LINQPad 4" on the title bar, and has a tab inside it labeled "Query 1". Under "Query 1", you should see a little green "play" arrow (hereafter referred to as play arrow).

To the right of play arrow, you should see a drop-down list labeled "Language (hereafter referred to as "language picker"), by default "C# Expression" should be selected in the language picker. If it isn't, select "C# Expression" from the language picker.

Under the play arrow and the language picker, there is a big empty box. This is where you will type C# code.

Click on the big empty box, then type "1 + 1". Now press the play arrow. You should see a "Results" window pop up with the number 2 in it. Congratulations! You just wrote and executed some code! Well, sort of…

An expression is the smallest executable bit of a program. The evaluation of an expression (i.e. 1 + 1) results in a value (i.e. 2). Expressions are important, but by themselves, they are useless.

#Making a Statement
From the language picker, select "C# Statement(s)". Now, where you previously typed "1 + 1", type the following (including quotation marks a.k.a. "dumb quotes"):
<pre>
"Hello World".Dump();
</pre>

Now push the play arrow. In the results window, you should see "Hello World". Let's talk about what just happened. Within LINQPad, there is a special method (if you are thinking, "What in the blue blazes is a method?" hold on) named "Dump". This method belongs to all objects <em>when you're working in LINQPad</em>.

The "Dump" method places things into the results window for you for your inspection.

Next, let's try something a little bit wordier…

<pre>
var i = 1;
i++;
i.Dump();
</pre>