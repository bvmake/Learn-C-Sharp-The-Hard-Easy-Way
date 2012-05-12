#A Little Light Reading
Most computer programs need a way to import and export data. One means of doing this is through your computer's file system.

In Notepad++, create a new file (*Ctrl*+*N*) and copy the following text into it.

<pre>
Monday: delegate-A delegate is a type that references a method. Once a delegate is assigned a method, it behaves exactly like that method.
Tuesday: closure-a closure is a function together with a referencing environment for the non-local variables of that function.
Wednesday: generics-Generic methods and classes defer of the specification of one or more type parameters until the class or method is declared and instantiated by client code
Thursday: interface-An interface contains only the signatures of methods, properties, events or indexers. 
Friday: destructor-Destructors are used to destruct instances of classes.
</pre>

Save your new file to your desktop with the name *word_of_the_day.txt*

The above text will give us something to read into our program. Modify *Program.cs* as follows:

<pre>
using System;
using System.IO;

class Program
{
    public static void Main(string[] args)
    {
        using (StreamReader reader = new StreamReader("word_of_the_day.txt")) 
  	{
			Console.WriteLine(reader.ReadToEnd());
		}
    }
}
</pre>

Compile *Program.cs* by calling the C# compiler:

<pre>
%WINDIR%\Microsoft.NET\Framework\v4.0.30319\csc.exe Program.cs
</pre>

Running *Program.exe* from the command line should print the contents of *word_of_the_day.txt* to the screen.