# QuickPython: Quick &amp; Painless Introduction to Python
### For adding Python to the data analysis toolbox as fast as possible!

#### Austin Rock, Data Engineer, IQVIA 2022 

This repository is geared towards those who know little, if anything of Python, or even programming as a whole. You may have heard about Python or are simply interested in utilizing its utilities to make your job easier. Whatever the reason, this tutorial will serve as a *quick* introduction to the language. 

* __Quick and Painless__: You will be spendling less time learning about things you don't need for your immediate job, and more time focusing on the core concepts that you will use right away.

* __For programing novices__: This tutorial was geared towards those who are comfortable in Excel or SQL, but have not mastered any object oriented programing languages.

* __Foundational__: I'm hoping to teach you the basic building blocks of the language and hopefully pique the your curiocity to learn more and dig deeper. If you understand the foundation and can *converse* in the lingo, you will be able to use the most foundational coding practice of all: __Stack Overflow__ to quickly expand your toolbox to whatever you need. 

## Table of Contents

#### BEGINNER PYTHON CONCEPTS
* [Lesson 1: Getting Started with Python and Downloading an IDE](#lesson-1-getting-started-with-python)
* [Lesson 2: First Steps into the Language](#lesson-2-introduction-to-data-types-and-basic-syntax)
* [Lesson 3: Introduction to Lists and Functions](#lesson-3-introduction-to-lists-and-functions)  

#### INTERMEDIATE PYTHON CONCEPTS

## Lesson 1: Getting Started with Python

The necessary (and truly only) starting point to your journey learning Python is to download the language! This requires you to download both the language package itself, as well as an Integrated Development Environment (IDE) that allows you to create Python programs and run them.

* __First__ navigate to [this link](https://code.visualstudio.com/) and download the applicable release of Microsoft Visual Studio Code. This is a lite IDE that includes many helpful things like a spellcheck, syntax suggestions, and other extentions developed by other folks that can make it easier to write and understand code. It will also allow us to create & run our Python programs. Follow the prompts to download the software and open it up once finished.

![image](https://user-images.githubusercontent.com/30609431/192852731-b3a48fb2-4e87-4206-af3a-b240b261df6a.png)

* __Once you have VS Code open__, the initial screen will look like this. Feel free to customize the theme to VS code and, if you'd like, create an account on the second bulletpoint to enable settings sync across different computers. Once you have finished setting up the IDE as you'd like, click "Mark All as Done" & press CTRL+SHIFT+X to open the Extentions tab. This will show all of the included language packages. To begin, search for Python using the top bar. Click on the first extention you see, authored by Microsoft, and Install. 

![image](https://user-images.githubusercontent.com/30609431/192854424-732b2a02-202d-4445-809b-0dbbc83ad42e.png)

* __Once Python installs__, you will see a Python specific welcome page. First, click on the prompt *Select a Python Interpreter*. This will select a version of Python that is installed on your machine & inform VS Code on how to compile the code. We will need to download Python in order to provide an interpreter. Follow [this link](https://www.python.org/downloads/) to dowload Python. __IMPORTANT__ it is critical that when you open the Python installer that you select *Add Python to PATH* before installing. Once you have followed the other prompts and Python has been installed, close the installer and restart VS Code. Once you have restarted the IDE, you should see that VS Code has automatically selected your installed version of Python as the interpreter. If this is not the case, click *Select Python Interpreter* and click on your preferred Python version to use. Regardless, you have finished downloading Python and setting up your IDE for programming! The next lesson will focus on our first program, and the basics of Python syntax.


## Lesson 2: Introduction to Data Types and Basic Syntax

Now that you have installed VS Code and Python onto your machine, it is time to create our first Python file. The way Python works, as opposed to Excel, is by creating an executible program file, denoted by the suffix *.py* rather than *.xlsx*. Once you have a program created, you will just execute the Python file and the program will run in the Python terminal.

* __Creating a Python Folder__. Open up VS Code, and you should see a blank screen. On the left side, navigate to the *Explorer* module, which will allow you to open up Python development folders. We will need to create a Python folder on your computer to house all of your programs and necessary datasets. So using the File Explorer on your computer, navigate to My Documents and create a Python folder for this tutorial. Feel free to name it whatever you'd like. After creating the folder, in VS Code click Open Folder and click on your new Python folder. Select it and follow the VS Code prompts to set it up for Python development. After doing so, you should see a page similar to the one below, with your Python folder present in the file explorer.

![image](https://user-images.githubusercontent.com/30609431/215582640-d77bae34-6d70-43dc-b65a-22c9230ee79b.png)

* __Creating our first Python file__. After we have a Python folder set up find it in the explorer on VS Code and click the *New File* button alongside it. Name it *Lesson_2.py*. Adding the .py suffix will tell VS Code that we will be writing in Python, so the software will open up a Python terminal to execute the program in. To confirm that you have created a Python file, you should see the Python logo alongside the file name at the top of the screen. In order to confirm we have no issues, please navigate to the top right of the screen and click the play button to *Run Python File*. If everything is OK, you will see no errors in the Python terminal and your screen should look like this. 

![image](https://user-images.githubusercontent.com/30609431/215584107-1c9b35a0-4bad-4762-ba85-83d412454371.png)

* __Introduction to Data Types__. Before we get started coding, we must first understand the different data types we will encounter in Python. In Excel, these are seen at the tops of columns where you may designate the data as: General, Numeric, Date etc. These core types are also present in Python. 

* Integer (`int` shorthand): This data type will cover whole numbers and associated mathematical functions. For example, if you wanted to perform the operation:
`126 + 223`, the result `349` would be an integer. Please write the following line of code in your Python file: `print(type(349))` and run the program. Print is a function (more on that later), that will print the following code to the terminal. The type function will tell you what data type the enclosed code returns. In this case, you will see the terminal output `<class 'int'>`. This tells us that 349 is an integer, because it is numeric and a whole number (non-decimal). 

* Float (`float`): Now what happens if we change the print statement to: `print(type(349.2))` and run the program? In the terminal it will return: `<class 'float'>`. Because 349.2 is a non-whole number. The float data type includes all integers with a decimal. This type is not present in Excel, but is necessary due to a complex computer science reason involving bits and how many bytes are allocated to the data type. For our purposes, just be aware that integers and floats are both numeric, but differ if the number is whole or not.

* String (`str`): Moving away from numeric data, a string type is simply any text-based data enclosed by double quotation marks " ". In Excel, this would be stored as Text or often, just General. To illustrate this, we will change the print statement to `print(type("Hi!"))`. When you run this code, the terminal will output `<class 'str'>`. This can also work with integer data, for example if we use the prior statement `print(type("349"))` and enclose the `int` value with double quotes, this will convert the integer to a string, or text. This is useful if you have one column of data that is stored as a string and another containing integers that you want to compare. As we will see later, data operations often require the data to be in the same type. Another note, if you are thinking of converting a string to an integer, you cannot simply remove the double quotes. `print(type(Hi!))` will return a syntax error because text cannot be simply converted to a number. To avoid syntax errors when working with strings, make sure to always remember your double quotes!

*  Boolean (`bool`): The final main data type we will look at here is Boolean data. This is something Excel does not have, but is very useful when it comes to logical comparisons. Simply, Boolean data is either `True` or `False`. For this reason, you can use this data for comparing different values. Or creatively in loops, which we will cover later, to stop a programmed loop if you reach a certain value or contstraint. Right now, type this in your Python file: `print(type(True))`. As you can see, although True and False look like text, they are not strings and we do not enclose them with double quotes. Doing so would simply convert the boolean to a string, `print(type("True"))`, which would not be useful for logical comparison. 

## Lesson 3: Introduction to Lists and Functions
