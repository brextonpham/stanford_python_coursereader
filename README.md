# stanford_python_coursereader

Lecture 1: Welcome to Python

Goals:
  1. Develop skills with Python fundamentals, both old and new
  2. Learn to recognize and write "good" Python
  3. Gain experience with practical Python tasks
  4. Understand when to choose Python (or not)
  
>>import this

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
6. Console I/O
7. Control Flow
8. Loops
9. Functions
