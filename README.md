# Stanford Python Course Reader

Lecture 1: Welcome to Python

Goals:
  1. Develop skills with Python fundamentals, both old and new
  2. Learn to recognize and write "good" Python
  3. Gain experience with practical Python tasks
  4. Understand when to choose Python (or not)
  
\>>import this

The Zen of Python, by Tim Peters
Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than nested.
Sparse is better than dense
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right( now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!

# Programmers are more important than programs.

"Hello World" in Java
public class HelloWorld {
  public static void main(String[] args) {
    System.out.printlin("Hello World!");
  }
}

"Hello World" in C++
#include <iostream>
using namespace std;
int main() {
  cout << "Hello World!" << endl;
}

"Hello World" in Python
print("Hello world!")

#Python Basics
1. Interactive Interpreter
  - Open up terminal and type in "python3"
  - Perks
    - Immediate gratification!
    - Sandboxed environment to experiment with Python
    - Shortens code-test-debug cycle to seconds
2. Comments
  - Single line comments start with a "#"
  - Multiline strings can be written using three "s, and are often used as comments
3. Variables and Types
  - Variables
    - x = 2
    - x * 7 --> 14
    - x = "Hello, I'm "
    - x + "Python!" --> "Hello, I'm Python"
  - Types
    - int x = 0; (Java or C++)
    - x = 0 (Python)
    - Variables in python are dynamically-typed: declared without an explicit type
    - However, objects have a type, so Python knows the type of a variable, even if you don't
    - type(1) --> <class 'int'> <-- This is the same object as the literal type int
    - type("Hello") --> <class 'str'>
    - type(None) --> <class 'NoneType'>
    - type(int) --> <class 'type'>
    - type(type(int)) --> <class 'type'>
4. Numbers and Booleans
  - Numbers
    - 3 --> 3 (int)
    - 3.0 --> 3.0 (float)
    - 1 + 1 --> 2
    - 8 - 1 --> 7
    - 10 * 2 --> 20
    - 9 / 3 --> 3.0
    - 5 / 2 --> 2.5
    - 7 / 1.4 --> 5.0
    - 7 // 3 --> 2 (integer division)
    - 7 % 3 --> 1 (integer modulus) 
    - 2 ** 4 --> 16 (exponentiation)
  - Booleans
    - bool is a subtype of int, where True == 1 and False == 0   
    - True --> True
    - False --> False
    - not True --> False
    - True and False --> False
    - True or False --> True (short-circuits)
    - 1 == 1 --> True
    - 2 * 3 == 5 --> False
    - 1 != 1 --> False
    - 2 * 3 != 5 --> True
    - 1 < 10 --> True
    - 2 >= 0 --> True
    - 1 < 2 < 3 --> True (1 < 2 and 2 < 3)
    - 1 < 2 >= 3 --> False (1 < 2 and 2 >= 3)
5. Strings and Lists
  - Strings
    - No char in Python!
    - Both ' and " create string literals
    - greeting = 'Hello' --> unicode by default
    - group = "world"
    - greeting + ' ' + group + '!' --> 'Hello world!'
    - Indexing
      - s = 'Arthur'
      - s[0] = 'A'
      - s[1] == 'r'
      - s[4] == 'u'
      - s[6] --> Bad!
    - Negative Indexing
      - s[-1] == 'r'
      - s[-2] == 'u'
      - s[-4] == 't'
      - s[-6] == 'A'
    - Slicing
      - s[0:2] == 'Ar'
      - s[3:6] == 'hur'
      - s[1:4] == 'rth'
      - s[:2] == 'Ar' <-- implicitly starts at 0
      - s[3:] == 'hur' <-- implicitly ends at the end
      - s[1:5:2] == 'rh' <-- can also pass a step size
      - s[5:2:-2] == 'ut'
      - s[::-1] == 'ruhtrA' <-- reversign a string
    - Converting Values
      - int("42") --> 42
      - float("2.5") --> 2.5
      - float("1") --> 1.0
      - str(42) --> "42"
  - Lists
    - easy_as = [1,2,3] <-- square brackets delimit lists, commas separate elements
    - Versatile
    - Incredibly Common
    - ArrayList/Vector
    - Nested Lists
      - since lists can any contain any elements, they can also contain other lists
      - a = ['a', 'b', 'c']
      - n = [1, 2, 3]
      - x = [a, n]
      - print(x) --> [['a', 'b', 'c'], [1, 2, 3]]
      - print(x[0]) --> ['a', 'b', 'c']
      - print(x[0][1]) --> 'b'
      - slice lists just like strings
      - print(n[1:]) --> [2, 3]
      - print(a[:2]) --> ['a', 'b']
    - General Queries
      - Length (len)
        - len([]) --> 0
        - len("python") --> 6
        - len([4,5,"seconds"]) --> 3
      - Membership (in)
        - 0 in [] --> False
        - 'y' in 'python' --> True
        - 'minutes' in [4, 5, 'seconds'] --> False
6. Console I/O
  - Read a string from the user
    - >>> name = input("What is your name? ") --> What is your name? Sam
    - >>> print("I'm Python. Nice to meet you,", name) --> I'm Python. Nice to meet you, Sam.
7. Control Flow
  - if the_world_is_flat:
      print("Don't fall off!") --> No parentheses, Colon, No curly braces!, Use 4 spaces to indent
  - 4 spaces?!
    - Readability counts
    - Removes visually-cluttering punctuation
    - Editor Settings
      - {
          "tab_size":4,
          "translate_tabs_to_spaces": true,
      - }
  - If Statements
    - if some_condition:
        print('Some condition holds')
      elif other_condition:
        print('Other condition holds') <-- zero or more elifs
      else:
        print('Neither condition holds') <-- else is optional
    - An aside: Python has no switch statement, opting for if/elif/else chains
  - Palindrome?
    - Palindrome Check
    - word = input("Please enter a word: ")
    - reversed_word = word[::-1]
    - if word == reversed_word:
    -   print("Hooray! You entered a palindrome")
  - Truthy and Falsy
    - 'Falsy'
    - bool(None)
    - bool(False)
    - bool(0)
    - bool(0.0)
    - bool('')
    - Empty data structures are 'falsy'
    - bool([]) --> False
    - Everything else is 'truthy'
    - data = []
    - if data:
    -   process(data)
    - else:
    -   print("There's no data!")
    - *You should almost never test: "if expr == True"*
8. Loops
  - For Loops
    - for item in iterable: <-- loop explicitly over data (strings, lists, etc.). no loop counter!
    -   process(item)
  - range
    - Used to iterable over a sequence of numbers
    - range(3) --> generates 0, 1, 2
    - range(5, 10) --> generates 5, 6, 7, 8, 9
    - range(2, 12, 3) --> generates 2, 5, 8, 11
    - range(-7, -30, -5) --> generates -7, -12, -17, -22, -27
    - range(stop) or range(start, stop, step)
  - break and continue
    - for n in range(10): --> break breaks out of the smallest enclosing for or while loop
    -   if n == 6:
    -     break
    -   print(n, end=',') --> 0, 1, 2, 3, 4, 5
    - 
    - for n in range(10):
    -   if n % 2 == 0:
    -     print("Even", n)
    -     continue --> continue continues with the next iteration of the loop
    -   print("Odd", n)
9. Functions
  - Writing Functions
    - The def keyword defines a function
    - Parameters have no explicit types
    - def fn_name(param1, param2):
    -   value = do_something()
    -   return value --> return is optional; if either return or its value are omitted, implicitly returns None
  - Prime Number Generator
  - def is_prime(n):
  -   for i in range(2, n):
  -     if n % i == 0:
  -       return false
  -   return True
  - 
  - n = input("Enter a number: ")
  - for x in range(2, int(n)):
  -   if is_prime(x):
  -     print(x, " is prime")
  -   else: 
  -     print(x, " is not prime")
