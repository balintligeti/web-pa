# Programming Basics questions ### Data structures 
#### What is the purpose (cél) of a list (array in some programming languages) data structure? Name some methods of it! 
List is a collection which is ordered and changeable. Methods: append(), index(), sort(), insert(), count() 
#### What is the difference between a list/array and a set? 
Set is a collection which is unordered and unindexed. No duplicate members. 
#### What is the purpose and methods of a dictionary/map data structure? 
Dictionary is a collection which is unordered, changeable and indexed. Methods: get(), items(), keys(), values(), pop(), popitem() 
### Algorithms 
#### Fibonacci sequences. Write a method (or pseudo code), that generates the Fibonacci sequences. 
fibonacci.py 
#### How do you find a max value in a list/array if you can’t use any built-in functions? 
max.py 
#### How do you find the average of values in a list/array if you can’t use any built-in functions? 
average.py 
#### What do we call an *in-place* sort? 
Sort in place means to sort an existing list by modifying the element order directly within the list. 
#### Explain an algorithm which sorts a list! 
Az algoritmus újra és újra végigiterál a listán, összehasonlítja a lista szomszédos elemeit, és ha azok az elvárt rendezéshez képest fordítva vannak, akkor megcseréli őket. Első menetben a lista elejéről indul és a végéig megy. Ennek az első menetnek az eredményeként a legnagyobb elem (mint egy buborék) felszáll a lista végére. Így a következő menetben már elegendő az utolsó előtti elemig elvégezni a szomszédos elemek összehasonlítását és cseréjét. Az ezután következő menetben a lista utolsó két eleme lesz a helyén és így tovább... 
## Computer science 
### Programming paradigms - procedural 
#### What is the call stack? 
call stackba [_] bekerül (push) először a main() (paraméterekkel együtt) aztán bekerül mellé a main()-ban található első function paraméterekkel, lefut és kiesik (pop), bejön helyette a soron következő function, lefut, kiesik és így tovább, amíg vannak a mainben functionok (vagy még azokon belül is functionok). Ha minden lefutott a mainben, a main is kiesik. 
#### What is “Stack overflow”? 
A stack túltölti magát functionökkel, pl. túl sokszor hívja meg önmagát vagy túl sok alfunction van
#### What are the main parts of a function? 
name, body, parameters, return
### Programming languages - Python 
#### How do you use a dictionary in Python? 
Use {} curly brackets to construct the dictionary, and [] square brackets to index it. Separate the key and value with colons : and with commas , between each pair. Add a value to the dictionary example: released["iphone 5S"] = 2013 
#### What does it mean that an object is immutable in Python? 
These are of in-built types like int, float, bool, string, unicode, tuple. In simple words, an immutable object can’t be changed after it is created. 
#### What is conditional expression in Python? (feltételes kifejezés)
a if a > b else b (also known as ternary operator) 
#### What are different types of arguments in Python? 
Default Arguments(etc.: def greet(msg=‘Good morning!’)), Keyword Arguments(etc.: greet(name=“Bruce”,”Good morning!”)), Arbitrary Arguments(etc.:def greet(*names))—>use this if you don’t know how many arguments do you want to assign, **kwargs 
#### What is variable shadowing? (context: variable scope) 
Variable shadowing happens when we define a variable in a closure scope with a variable name and we have already defined a variable in outer scope with the same name. In other words, when a local variable has the same name as one of the instance variable, the local variable shadows the instance variable inside the method block. 
#### What can happen if you try to delete/drop/add an item from a List, while you are iterating over it in Python? 
It can raise IndexError. You are having an index error because you are modifying the list as you go. The for loop receive a etc.: range(4) but in the end etc.:lst[4] does not exist anymore as you have deleted some items. 
#### What is the "golden rule" of variable scoping in Python (context: LEGB)? What is the lifetime of variables? 
Python namespaces are containers to map names to objects. In Python, everything is an object and we specify a name to the object so that we can access it later on.
Python namespaces can be divided into four types. 
1.	Local Namespace: A function, for-loop, try-except block are some examples of a local namespace. The local namespace is deleted when the function or the code block finishes its execution. 
2.	Enclosed Namespace: When a function is defined inside a function, it creates an enclosed namespace. Its lifecycle is the same as the local namespace. 
3.	Global Namespace: it belongs to the python script or the current module. The global namespace for a module is created when the module definition is read. Generally, module namespaces also last until the interpreter quits. 
4.	Built-in Namespace: The built-in namespace is created when the Python interpreter starts up and it’s never deleted. 
Local —> Enclosed —> Global —> Built-in 
#### If you need to access the iterator variable after a for loop, how would you do it in Python? 
I would assign it into a variable before the for loop with iter() built-in function. etc.: b=iter() 
#### What type of elements can a list contain in Python? 
You can store every kind of data type in a list. 
#### What is slice operator in Python and how to use? 
The slice operator is used to slice a given sequence (string,tuple,list). etc.: string[start(optional),stop(not included),step(optional)] 
#### What arithmetic operators (+,*,-,/) can be used on lists in Python? What do they do? 
Only + operator and this operator extend a list with another list. 
#### What is the purpose of the in and not in membership operators in Python? 
The ‘in’ operator is used to check if a value exists in a sequence or not. ‘not in’ operator- Evaluates to true if it does not finds a variable in the specified sequence and false otherwise. 
#### What does the + operator mean when used with strings in Python? 
It will concatenate the strings. 
#### Explain f strings in Python? 
f-strings are string literals that have an f at the beginning and curly braces containing expressions that will be replaced with their values. 
#### Name 4 iterable types in Python! 
str, list, set, dictonary 
#### What is the difference between list/set/dictionary comprehension and a generator expression in Python? 
List comprehension:
It is an elegant way of defining and creating a list. List Comprehension allows us to create a list using for loop with lesser code. What normally takes 3-4 lines of code, can be compressed into just a single line.
V = [I for I in range(10)]
Generator expression:
Generator Expressions are somewhat similar to list comprehensions, but the former doesn’t construct list object. Instead of creating a list and keeping the whole sequence in the memory, the generator generates the next element in demand. // kb. Mint a lista csak nem tárolja el egyenként az összes elemet hanem 1 elemnyi helyre elmenti és később lehet átvinni abba, amibe szeretném (pl. list). (list)(I for I in range(10))

#### Does the order of the function definitions matter in Python? Why? 
It doesn't matter in which order the functions are created. It only matters when the call to the function is done. 
#### What does unpacking mean in Python? 
We can use * to unpack the list so that all elements of it can be passed as different parameters. We can use *(tuple) or **(dictionary) when we are calling a function to unpack a sequence or a dictionary into a series of individual parameters. 
#### What happens when you try to assign the result of a function which has no return statement to a variable in Python? 
The function will return None. 
## Software engineering ### Debugging 
#### What techniques can you use while debugging a program in Python? 
We can use debugger. We can use pdb. Finally, we can print out the values, but this is not a professional technique. 
#### What does step over, step into and step out mean while using the debugger? 
Step Into will cause the debugger to go into the next function call and break there.
Step Over will tell the debugger to execute the next function and break afterwards. 
Step Out will tell the debugger to finish the current function and break after it. 
#### How can you start to debug a program from a certain line using the debugger? 
We can use breakpoints.
 ### Version control 
#### What are the advantages of using a version control system? 
Collaboration, Storing versions, Restore older versions, Understanding what happened with commits, Backup 
#### What is the difference between the working directory, the staging area and the repository in git? 
Working tree: The Working Tree is the area where you are currently working. It is where your files live. This area is also known as the “untracked” area of git. Any changes to files will be marked and seen in the Working Tree. Here if you make changes and do not explicitly save them to git, you will lose the changes made to your files. If you make changes to files in your working tree git will recognize that they are modified. Command: git status 
Staging area: The Staging Area is where git starts tracking and saving changes that occur in files. These saved changes reflect in the .git directory. If I want to track specific files from Working Tree git will move from it to Staging Area. Commands: git status, git add
Local repository: The Local Repository is everything in your .git directory. Mainly what you will see in your Local Repository are all of your checkpoints or commits. It is the area that saves everything. git commit will add items from Staging area to Local repository. Command: git log (brings up a log of all previous checkpoints in my repository), git show #commit# (see what was changed at that specific checkpoint.) 
#### What are remote repositories in git? 
A remote in Git is a common repository that all team members use to exchange their changes. In most cases, such a remote repository is stored on a code hosting service like GitHub. In contrast to a local repository, a remote typically does not provide a file tree of the project's current state. Instead, it only consists of the .git versioning data. 
#### Why does a merge conflict occur? 
A merge conflict is an event that occurs when Git is unable to automatically resolve differences in code between two commits. When there are conflicting changes on the same lines, a “merge conflict” occurs because Git doesn’t know which code to keep and which to discard. 
#### Through what series of commands could you put a new file into a remote repository connected to your existing local repository? 
0. git status
1. git add #filename# or #.# 2. git commit -m “message” 3. git push origin master 
#### What does it mean atomic commits and descriptive commit messages? 
Atomic (kicsi) commits: minél kisebb szakaszokat commitolj, hogy a hibák jobban lekövethetőek és javíthatóak legyenek. 
Descriptive commit messages: frappáns leírás a commitról
#### What’s the difference between git and GitHub? 
git: Git is a version control system for tracking changes in computer files and coordinating work on those files among multiple people. It is primarily used for source code management in software development.
GitHub: Git is the version control software, and Github is a git repository hosting service which offers all the source code management provided in git. Github is where you upload your git repository. 
## Software design ### Clean code 
#### What does clean code mean? 
Clean code is code that is easy to understand, easy to change, easy to maintain, easy to test and easy to spot bugs. 
#### What steps do we usually do during a clean code refactoring? 
1.	Read through the whole code 
2.	Summarize what is the purpose of the script in one sentence. 
3.	Run the code to see what is the end result 
4.	The code should keep runnable and show the same content when you finish 
the refactor 
5.	Do not forget to run the code frequently to check you are on the right track 
6. How to refactor it? 
o	Remove clutter: Clutter is anything in your code that does not add value 
o	▪  Format your code 
o	▪  Delete comments 
o	Remove complexity: 
o	▪  bad names 
o	▪  long methods 
o	▪  deep conditionals 
o	▪  improper variable scopes (global, local) 
o	Remove cleverness: If it's simple and elegant you wouldn't refer to it as 'clever' 
o	Remove the duplications: This can be applied by extracting the duplicated code parts into functions 
### Error handling 
#### What is exception handling? 
Exception handling is the process of responding to exceptions when a computer program runs. An exception occurs when an unexpected event happens that requires special processing. Examples include a user providing abnormal input, a file system error being encountered when trying to read or write a file, or a program attempting to divide by zero. Exception handling attempts to gracefully handle these situations so that a program (or worse, an entire system) does not crash. 
#### What are the basics of exception handling in Python? 
To handle possible exceptions, we use a try-except block. Python will try to process all the statements inside the try block. If an error occurs at any point as it is executing them, the flow of control will immediately pass to the except block, and any remaining statements in the try block will be skipped. 
#### In which case should we catch an exception? Why? 
user providing abnormal input, a file system error being encountered when trying to read or write a file, or a program attempting to divide by zero —> because this kind of errors crash the program 
#### What can/should we do with an exception in the ‘except’ block? 
We should write out some informative message about the error and why it was occurred. 
#### What does the else and finally statement do in a try-except block in Python? 
else: else will be executed only if the try clause doesn’t raise an exception finally: The finally clause will be executed at the end of the try-except block no matter what – if there is no exception, if an exception is raised and handled, if an exception is raised and not handled, and even if we exit the block using break, continue or return. 
## Software Development Methodologies 
#### What is the main goal of a retrospective meeting? 
A retrospective is an opportunity to learn and improve. It is time set aside – outside of day-to-day routine – to reflect on past events and behaviors. In its simplest form you answer 3 questions: 
•	What worked well? 
•	What didn’t work well? 
•	What are we going to try to do differently? 
Set some SMART actions:
Specific (clearly defined,)
Measurable (outcomes can be measured)
Achievable (the actions are realistic)
Responsible (responsibility for implementation is identified) Time bound (there is a clear timeframe –start and end date) 
## Programming environment ### Unix 
#### What is UNIX and what is Linux? 
UNIX: Unix is an operating system. It supports multi-tasking and multi-user functionality. Unix is most widely used in all forms of computing systems such as desktop, laptop, and servers. On Unix, there is a Graphical user interface similar to windows that support easy navigation and support environment. 
Linux: Linux is a Unix-like, open source and community-developed operating system for computers, servers, mainframes, mobile devices and embedded devices. Every Linux-based OS involves the Linux kernel—which manages hardware resources—and a set of software packages that make up the rest of the operating system. 
#### What do we call the shell in Linux? 
A Shell provides you with an interface to the Unix system. It gathers input from you and executes programs based on that input. When a program finishes executing, it displays that program's output. Shell is an environment in which we can run our commands, programs, and shell scripts. There are different flavors of a shell, just as there are different flavors of operating systems. Each flavor of shell has its own set of recognized commands and functions. 
#### What does root means in a Linux environment? 
root has access to all files and commands in any Unix-like operating system and it is often referred to as the superuser for that reason. 
#### How do you access your personal files in Linux? 
/home 
#### How can you install an application in Linux? 
sudo dnf install 
#### What is package management in Linux, what are repositories? 
In few words, package management is a method of installing and maintaining (which includes updating and probably removing as well) software on the system. Package managers are designed to eliminate the need for manual installs and updates. 
Repository: A Linux repository is a storage location from which your system retrieves and installs OS updates and applications. 
#### How do you navigate in the filesystem with the command line? 
ls: list the files in the directory
cd: open a directory
cd..: move you up one directory
pwd: writes the full pathname of the current working directory 
#### What does the following commands do: mkdir, rm, cat, cp, touch? 
mkdir #name#: create a directory with name rm #name#: remove a file with name
cat: view a file or create a file it depends on cp: copy a file 
touch: create a file 
#### How can you look up what does a command do in Linux if you have no internet connection? 
man #command# —> short description about the command 
#### What does the following commands do: head, tail, more, less? 
head: display first lines of a file
tail: display the last part of a file
more: display the contents of a file in a console
less similar to more, less command allows you to view the contents of a file and navigate through file. The main difference between more and less is that less command is faster because it does not load the entire file at once and allows navigation though file using page up/down keys. 
#### How do you download a file from internet using the terminal? 
curl -O #link# 

