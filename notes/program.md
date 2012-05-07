#Right Tool for the Job
LinqPad is great for testing out small bits of code, but no one would want to write more than the simplest of programs using it exclusively.

A [text editor](http://en.m.wikipedia.org/wiki/Text_editor) , particularly one that can keep several files open simultaneously and perform syntax highlighting, is a much more practical choice for authoring programs. Notepad (on Windows—it can be run by pressing Windows + R on the keyboard, and then typing "notepad" into the Run Dialog) is a fair enough basic editor, but for writing complex programs, [Notepad++]( http://notepad-plus-plus.org/) is recommended. Go download and install Notepad++.

#A Short Program
Run Notepad++. It should create a blank unsaved file for you to type your code into. Write the following in that file:
<pre>
using System;

class Program
{
    public static void Main(string[] args)
    {
        CountToTen();
    }

    private static void CountToTen()
    {
        for(var i=1; i<=10; i++)
        {
            Console.WriteLine(i);
        }
    }
}  
</pre>

#Saving your work
Now press the *Ctrl* key and the *S* key together (Ctrl + S—pronounced "Control S"); doing so will bring up the *Save As* dialog. Down the left hand column of the *Save As* dialog, click the *Desktop* icon. In the text box labeled *File name* at the bottom of the *Save As* dialog, type in a name of *Program.cs*. From the *Save as type* drop down list, choose "C# source file". Then, click the *_S_ave* button (or press Alt+S).

#Compiling
You should now have a file sitting on your desktop with the name *Program.cs*. The [path](http://en.wikipedia.org/wiki/Path_\(computing\)) of this file should be C:\Users\*YourUsername*\Desktop\Program.cs.

Start a command window by pressing *Windows*+*R* and typing *cmd* in the *Run* box. Inside the command window, you should see a flashing cursor. Type the following:

<pre>
cd Desktop
</pre>

Now the prompt should look like "C:\Users\*YourUsername*\Desktop&gt;". At the prompt, type in the following:

<pre>
%WINDIR%\Microsoft.NET\Framework\v4.0.30319\csc.exe Progam.cs
</pre>

This will compile your program and create an executable file on your Desktop. At the prompt, type:

<pre>
Program.exe
</pre>

This should result in the output:

<pre>
1
2
3
4
5
6
7
8
9
10
</pre>