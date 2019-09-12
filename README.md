# WiTNY-Sample-Lesson

## Intro to Python

#### SWBATs:

* GENERAL PYTHON - explain that all programs are just lines of text read by a computer
* GENERAL PYTHON - demonstrate that python programs are read top to bottom
* GENERAL PYTHON - differentiate between data and key words
* STRINGS - explain what a string is and why it's used
* STRINGS - create strings using double quotes
* STRINGS - concatenate two strings using the `+` operator
* STRINGS - use common string functions
* PRINT - Explain what a print statement is and what it's used for
* INT - explain what an integer is and why it's used
* INT - use common mathematical operations with integers
* INT - use typical functions like float() and str() to mutate integers
* FLT - explain what a float is and why it's used
* FLT - understand that math with floats produces floats and math with integers produces integers (except in the case of division)
* FLT - use typical functions like int() and str() to mutate floats
* FLT - use common mathematical operations on floats
* STRINGS/VARIABLES - concatenate a variable or a function to a string
* VAR - use a variable in place of a piece of data
* VAR - assign integers to variables
* VAR - assign floats to variables
* VAR - reassign the value of a variable
* INPUT - take in user input using the input() function
* VAR - use correct syntax in naming variables
* CONDITIONALS - Explain the use of a boolean data type.
* CONDITIONALS - Explain what an if statement is and why it's used
* CONDITIONALS - Implement an if statement with 1, 2, and 3+ branches
* CONDITIONALS - Use comparison operators in a conditional statement
* GENERAL PYTHON - predict that the effect of text in python that is not data or a key word will throw an error
* GENERAL PYTHON - explain that an error will stop the execution of python code


#### Sequence

1. [Setting Up](#setting-up)
2. [Hello World](#hello-world)
3. [Math](#math)
4. [Variables and Concatenation](#variables-and-interpolation)
5. [User Input](#user-input)
6. [Control Flow](#control-flow)
7. [Datatype Conversion](#datatype-conversion)
8. [For Loops](#for-loops)

# Part 1

## Setting up

Students will benefit from a walkthrough, as most just started interacting with the command line for the first time this morning.

```bash
mkdir day-one
cd day-one
touch hello.py
```

CFU by having students identify that their prompt ends in `day-one`, and by identifying a hello.py file on the left side of the screen.  

This lesson introduces a lot of really foundational vocabulary words. This is a CRITICAL time to make a **datatypes anchor chart**, and include integers, floats, strings, and booleans.

## Hello World

In the python file:
```python
print("hello world!")
```

Explain that anything in quotes is a **String** of characters. A string essentially represents a word or phrase.

In the console:
```bash
python hello.py
```

#### Playtime

* Print out a 5-sentence story with 5 different statements
* Google the phrase "ASCII-art" and try to make your program print it out to the console

## Math

In the console:
```bash
touch math.py
```

In the python file:
```python
print("4" + "3")
print(4 + 3)
print(4.0 + 3.0)
```

Name the datatypes Int and Float, but avoid explaining the difference.
Ask students to make a prediction about what each line will print before moving on.

In the console:
```bash
python math.py
```

#### Playtime

* Ask students to try these operators and see if they can figure out what each does.
* Also ask them if they can figure out the difference between 4 and 4.0 and the way they behave with each of them.
    * `+`, `-`, `*`
    * `/`, `**`
    * `%`
* Ask students whether it's possible to mix datatypes, like `print("hello" * 3)` or `print(4 / 3.0)`
*Note: this practice section may be easier to run in a REPL in the console. If you're interested, just type "python" in the console. Type "quit()" to exit.*

#### Takeaways

* STRINGS - explain what a string is and why it's used
* STRINGS - create strings using double quotes
* PRINT - Explain what a print statement is and what it's used for
* INT - explain what an integer is and why it's used
* INT - use common mathematical operations with integers
* FLT - explain what a float is and why it's used
* FLT - understand that math with floats produces floats and math with integers produces integers, except in the case of division where a float is always produced
* FLT - use common mathematical operations on floats

## Variables and Concatenation

In the console:
```bash
touch greet.py
```

In the python file:
```python
name = "Lauren"

print("Good morning " + name + "!")
```

Identify that the word "name" isn't a string, since it doesn't have quotes around it. Identify that it is a **variable** that *contains* a string.
Ask students to predict what will be printed to the console.

In the console:
```bash
python greet.py
```

Ask students to explain what happened. Identify that this method of adding strings together with the contents of a variable is called **concatenation**. Explain that this is one of two ways to do this. The other is called **string formatting**.

In the python file:
```python
name = "Lauren"
name2 = "Manuel"

print("Good morning " + name + "!")
print("Good morning %s!" % name2)
```

Stop and ask students whether they prefer concatenation or string formatting and have them explain why. Explain that we'll be using concatenation more often in this class, because it's more universal

#### Built-in Functions

In the python file:
```python
name = "Lauren"

print("Good morning " + name + "!")
print("Your name has " + str(len(name)) + " letters in it!")
```

Ask students to predict what will be printed. Ask them what will be printed if they change Lauren's name to their own. Let them test it out. Explain that len() is a built-in function which takes a string as an **argument**.

Ask students why it's better to have the computer compute the length of Lauren's name rather than just hard-coding in the number 6.

Explain that str() converts the integer length of the name into a string, but not to worry if this is confusing. It will make sense later when they create the ageCheck program. Feel free to demo the error that arises if you try to concatenate without converting and show students how to read this type of error.

#### Playtime

* Ask students to change the string "Lauren" to another name.
* Ask students to add a variable called age that has a string inside of it and try concatenating (or string formatting) TWO variables into one string.

#### Takeaways

* STRINGS/VARIABLES - concatenate a variable or a function within a string
* VAR - use a variable in place of a piece of data
* STRINGS - use common string functions

## Break for Labs
Students now have everything they need to do the John Jacob Jingleheimerschmidt lab.
Students who progress quickly through that can move on to the DNA lab.
Neither requires user input or control flow.  

# Part 2

## User Input

Continue modifying the greet program. ID that when we write a program, we won't know the user's name.

In the python file:
```python
name = input("What is your name?")

print("Greetings, " + name + "! Welcome to the program.")
```

Ask students to predict what will happen when this program is run.

In the console:
```bash
python greet.py
```

#### Takeaways

* INPUT - take in user input using the input() function
* VAR - use correct syntax in naming variables

## Control Flow

#### Basic control flow

In the python file:
```python
name = input("What is your name?")

if name == "Beyonce":
  print("Welcome, queen B.")
else:
  print("Greetings, " + name + "! Welcome to the program.")
```

Before running, ask students to predict what will happen if the user says their name is Beyonce. Then ask what will happen if the user gives a different name. Be prepared for students to notice that 'beyonce' with a lowercase b will not work.

Ask students to try running this program to get both results. Preface this with the fact that about HALF the students will get errors.

#### Takeaways

* CONDITIONALS - Explain what an if statement is and why it's used
* CONDITIONALS - Implement an if statement with 1, 2, and 3+ branches

## Datatype Conversion

Challenge students to build a program that does all of the following:
* Asks the user for their age
* Stores that age in a variable
* Prints out whether or not they are old enough to vote
* Stretch - also checks whether or not they are old enough to drive, rent a car, or get a senior discount

In the console:
```bash
touch ageCheck.py
```

In the python file:
```python
age = input("How old are you?")

if age >= 18:
  print("You're old enough to vote!")
else:
  print("You're not old enough to vote.")
```

In the console:
```bash
python ageCheck.py
```

We're intentionally triggering an error: `'>=' not supported between instances of 'str' and 'int'`. Talk with students about the importance of *reading* their errors, not just freaking out. Whether students arrive at the correct conclusion or not, make sure to direct their thinking by asking the following questions:
* What's the difference between `"18"` and `18`?
* Optional: Ask students which is greater, "green" or "brown" to help them see that using a greater-than operator on strings makes no sense.

In the python file:
```python
age = input("How old are you?") # Read this as "Set age equal to whatever string the user types."
age = int(age) # We reassign the variable information here.
# In essence, "Set age equal to an integer expression of whatever the user typed."

if age >= 18:
  print("You're old enough to vote!")
else:
  print("You're not old enough to vote.")
```

Explain that str(len(name)) in the greeter program earlier was converting the integer length of name to a string, the same way int(age) here converts the string age to an integer.

#### Playtime

Stretch challenges / lab time:
* Include other age cutoffs for activities like driving, renting a car, or retiring.
* Go back to the greeter and add code to ask for the user's age.
    * Write code to respond if Beyonce's age is incorrect.
* Go back to the greeter and add to the user base by making sure it can greet Jackie Chan, Will Smith and a few other celebrities. Consider giving them unique passwords.
* Invite them to go back and finish any of the earlier labs that were giving them trouble.

#### OPTIONAL: Compound operators and branching if statements
> THIS content is actually usually better introduced if students ask for it - they almost always will as part of the above practice.

In the python file:
```python
name = input("What is your name?")
password = input("Please enter your password.")

if name == "Beyonce" and password == "Lemonade1":
  print("Welcome, queen B.")
elif password != "Lemonade1":
  print("WARNING. Incorrect password")
else:
  print("Greetings, " + name + "! Welcome to the program.")
```

Ask students what the password is for the program. Ask students to run this program with combinations of answers to get all three results. Explain that they can expect errors, and celebrate those errors as learning opportunities.

#### Takeaways

* GENERAL PYTHON - explain that an error will stop the execution of python code
* GENERAL PYTHON - Students understand that errors provide useful information about what's going wrong
* VAR - reassign the value of a variable
* INT - use typical functions like float() and str() to mutate integers
* FLT - use typical functions like int() and str() to mutate floats

## Subscripting
#### OPTIONAL - Subscripting is a useful primer for lists, but not necessary for a successful day 1.

One of the most useful features of Python is how simply it can break one piece of information (like a String) into its component parts (letters/characters).

We will see LOTS of examples of this later, but for now, show students this small bit of sample code and then ask the questions that follow.

```python
print("hello"[1])
```
Before running the code:
* How many letters do you think will be printed?
* Which letter(s) do you expect will be printed?
After running the code:
* Why do you think the second letter came out instead of the first?
* How could you access the first letter?

Please note that usually half the students in a classroom have had some coding experience before, and those students are VERY eager to call out that indexing starts at zero - encourage them to JUST predict the letter instead of justifying their answers. You want to try to avoid a situation where a new coder hears the phrase like "indexing starts at zero, everyone knows that" - so be explicit about this rationale - "IF you already know exactly what I'm driving at, just think it quietly instead of calling it out. I want to give an opportunity for first-timers to figure this out."

#### Playtime
* Use subscripting to print out the third letter of your name.
* Use subscripting to print out the first three letters of your name.
* Use subscripting to print out the last letter of your name.

> Note that there are multiple ways to do the second and third challenge here. Please affirm all approaches.

## For Loops
#### OPTIONAL - For loops will be covered with lists, so don't feel pressured to cover it here.

One other cool thing worth knowing is that you will often want to access all the items in a string one at a time using a process called iteration. If you wanted to teach someone how to spell the word "Hello", you could do it one character at a time like this:
```python
print("Hello"[0]) # The first character...
print("Hello"[1]) # The second character...
print("Hello"[2]) # etc.
print("Hello"[3])
print("Hello"[4])
```
But iterating manually like this could get tedious really quickly.

Instead you can just write the command "for every letter in python, print that letter". Here's what that looks like as code:
```python
for letter in "Hello":
  print(letter)
```

Bear in mind that we could use any word in place of `letter` for this process, but other variable names like `x` or `somevariable` are less descriptive, and we want our code to readable.

One of the coolest seeds to plant here is another way of reversing a word, but consider withholding this if students are feeling panicked, and be clear that this isn't critical understanding to move forward.   
```python
newWord = "" # start with a blank string.
for letter in "hello":
  newWord = letter + newWord # add the current letter to the FRONT of the blank string.
  print(newWord)
```

This is a REALLY useful seed to plant both in terms of how to use iteration to solve challenging problems, and in terms of helping students see the benefit of declaring an empty list, string, or dictionary to be modified after the fact.

#### Playtime
* Use a `for` loop and your name to print the statement "My name has the letter ____ in it!" filling in the blank once for every letter in your name.
* Use a `for` loop and a 20-letter word to print "Hello!" 20 times.
* Use a `for` loop and a 20-letter word to print the numbers 1-20.
