#Starting Line
Let's get started. You are going to need a few things and going to have to do some small chores before we can start coding in C#.

The first thing we'll need is LINQPad. It is a program that you can type C# code into and test it to see if it works. You can download it from [this page](http://www.linqpad.net/). The "Low Impact Setup" for .NET 4.0 (referred to as FW 4.0 on the linqpad site) is recommended.

#<a name="expressive">Let's Get Expressive</a>
Once LINQPad is installed on your computer, run it by clicking on the desktop icon (or on LINQPad.exe if you downloaded the zip file).

You should be presented with a window that says "LINQPad 4" on the title bar, and has a tab inside it labeled "Query 1". Under "Query 1", you should see a little green "play" arrow (hereafter referred to as play arrow).

To the right of play arrow, you should see a drop-down list labeled "Language (hereafter referred to as "language picker"), by default "C# Expression" should be selected in the language picker. If it isn't, select "C# Expression" from the language picker.

Under the play arrow and the language picker, there is a big empty box. This is where you will type C# code. We'll call it the text window.

Click on the big empty box, then type "1 + 1". Now press the play arrow. You should see a "Results" window pop up with the number 2 in it. Congratulations! You just wrote and executed some code! Well, sort of…

An expression is the smallest executable bit of a program. The evaluation of an expression (i.e. 1 + 1) results in a value (i.e. 2). Expressions are important, but by themselves, they are useless.

#<a name="statement">Making a Statement</a>
From the language picker, select "C# Statement(s)". Now, where you previously typed "1 + 1", type the following (including quotation marks a.k.a. "dumb quotes"):
<pre>
"Hello World".Dump();
</pre>

Now push the play arrow. In the results window, you should see "Hello World". Let's talk about what just happened. Within LINQPad, there is a special method (if you are thinking, "What in the blue blazes is a method?" hold on) named "Dump". This method belongs to all objects <em>when you're working in LINQPad</em>.

The "Dump" method places things into the results window for you for your inspection. In the previous example you are placing the string (text) "Hello World", into the results window.

Next, let's try something a little bit wordier…

<pre>
var i = 1;
i++;
i.Dump();
</pre>

Type the above into your text window, and then press the play arrow. You should now see the number 2 in the results window. Let's take a closer look at what just happened.

The line "var i = 1;" creates the local variable "i" of type int (we'll get back to that) and assigns the integer value 1 to it. You can think of variables as buckets that hold things (in this case a number).

The line "i++;" takes the value of <em>i</em> increments that value (increases by one) and assigns the incremented value to <em>i</em>. In this line, we see our first operator (++, a.k.a. the increment operator).

The line "i.Dump();" places the value of i into the results window.

#<a name="program">Back to Your Regularly Scheduled Program</a>

From the language picker, select "C# Program". In the text window, type the following:
<pre>
void Main()
{
    for(var i = 1; i &lt;= 10; i++)
    {
        i.Dump();
    }
}
</pre>

We've just seen our first control flow statement (a [for](http://msdn.microsoft.com/en-us/library/aa664753\(v=vs.71\).aspx) statement to be precise). A *for* statement is a pretty simple little device. There are three optional expressions after the word *for* and between the *(* and *)*. They are: the initializer, the condition, and the iterator. The initializer creates a variable that only has scope (meaning) inside the for loop—between the *{* and *}*—and sets its value. The condition tells the for loop when to stop looping—in this case when the value of *i* is 11. The iterator can really be any expression (or comma separated list of expressions), but by convention, is usually used to increment the variable declared in the initializer expression.

The following would have exactly the same effect as the previous:

<pre>
void Main()
{
    var i = 1;
    for(; i &lt;= 10; i++)
    {
        i.Dump();
    }
}
</pre>

or

<pre>
void Main()
{
    var i = 1;
    for(; ; i++)
    {
        if(i==11) break;
        i.Dump();
    }
}
</pre>

#<a name="method">Getting Methodical</a>

Ensuring that you've got "C# Program" selected in the language picker, type in the following code:

<pre>
void Main()
{
    CountToTen();
}

void CountToTen()
{
    for(var i = 1; i &lt;= 10; i++)
    {
        i.Dump();
    }
}
</pre>

Execute the code by clicking on the play arrow. The result is the same, but the structure of the code is different. The code that begins with *void CountToTen()* is called a method. Methods help us organize our code by giving a name to the behavior that they carry out. The code *CountToTen();* is called a method call. Method calls (a.k.a. method invocation) are how we get methods to carry out their work. Taking what we know, let's write a program.