# Understand basics of python:-
10**2=> 100

3 * 'anubhav'=> anubhavanubhavanubhav

10*2=> 20

# single slash => a/b => float division we will get value as float 20/10= 2.0
# double slash => a//b => integer division we will get value as integer 20//10= 2

# Inbuilt function to check the datatype is:-
type(1)=> int


type("hello")=> str


type(10.0)=>float


type(True)=> bool

# print statement:-
firstName="anubhav"

lastName="Choudhary"

print("my first name is {} and my last name is {} ".format(firstName,lastName))=>order matters

or

print("my first name is {first} and my last name is {last}".format(first=firstName,last=lastName)) order doesnt matter=> my first name is anubhav and my last name is Choudhary

my_str="hello"
print(my_str.endswith('o'))=>True
print(my_str.startswith('h'))=>True

# Mutable and Immutable
In python a memory is assigned not for the variable but for the value we are giving to it for example x=10 then x will be pointing to 10 and 10 will be in the memory as it is integer it will be a immutable datatype so we cannot change the value and if we put y=x then y will also start pointing to the value x is pointing and if we change the value of x=15 now x will be pointing to 15 but y will still be pointing to the 10,so in this manner we can decide a immutable and mutable datatypes. n mutable we can change the value in the memory. 
# The core idea;-
Names (variables) don’t “contain” data in Python. They point to objects.

Objects live in memory and have a type (int, list, str, …) and an identity (id(obj)).

Immutability = the object’s contents cannot change once created (e.g., int, str, tuple).

Mutability = the object’s contents can change in-place (e.g., list, dict, set).

Assignment (=) never copies; it just binds a name to an object.

# Question=> where will these names resides
* In Python, names are created inside namespaces—not in the “heap vs stack” sense, but in mapping-like scopes that bind a name (the label) to an object (the value).


# Python Iteration 

• Iterable vs Iterator
– Iterable = a thing you can loop over (list, string, dict, range, file, generator).
– Iterator = the “walker” that hands you items one by one.
– You get an iterator from an iterable using iter(obj).
– You pull the next item using next(it); when it’s over, next raises StopIteration.

• How a for-loop really works
– First it calls iter(iterable) once to get an iterator.
– Then it keeps calling next(...) to get items.
– When StopIteration happens, the loop ends.

• List iterators
– iter([1,2,3]) gives a new “cursor” object (list_iterator).
– It does not copy the list; it just remembers the current index.
– Every call to iter(the_same_list) gives a fresh, independent cursor.
– Iterators are single-use; once finished, make a new one.

• “Why does print show 0x…?”
– Printing an iterator shows a default identity string like <list_iterator at 0x…>.
– That’s just the object’s identity, not the first element. The real items come from next(...).

• Files act as their own iterators
– A file object already is an iterator over its lines (iter(f) is f is True).
– next(f) gives the next line; at end, StopIteration is raised.
– Use a with-block so files close automatically.
– Text lines usually include a trailing newline; strip it if you don’t want it.

• Generators (easy custom iterators)
– A function that uses yield automatically creates an iterator.
– Behaves like any other iterator: single pass, ends with StopIteration.

• Do’s and Don’ts
– Don’t modify a list while iterating it; if needed, iterate over a copy.
– For another pass over data, create a fresh iterator (or materialize to a list if it’s small).
– For huge data (files, streams), prefer iterators—they’re memory-friendly.

# String 
# Methods=> upper,lower,isaplhanum ,isdigit,isalpha,count,islower,isupper
str.isalphanum() ...

* split  str[2:9] to jump characters is string str

* [2:9:2] => it will jump every other character

* len(str)=> to find the length
for i in range(len(str)):
     return


# List(mutable,changeable,ordered sequence of elements):-

lst_example=[]
     or
lst_example=list() 
print(type(lst_example))=>list

# can contain elements with different datatypes
lst=['Mathematics', 'chemistry', 100, 1001, 200, 300] 

# type 
type(lst)=>list

# length of list
len(lst)=> 5 
# Methods=> append,extend,insert,pop,count,index,min,max 

# append
lst.append("anubhav")
print(lst)=> ['Mathematics', 'chemistry', 100, 1001, 200, 300, 'anubhav']

lst[:7:3]=> ['Mathematics', 1001, 'anubhav']
lst[1:5]=> ['chemistry', 100, 1001, 200]

lst.append(["garima","anubhav"])=>['Mathematics', 'chemistry', 100, 1001, 200, 300, 'anubhav',["garima,"anubhav"]]
# use extend instead of append if you do not want nested list inserted
lst.extend(["garima","anubhav"])=>['Mathematics', 'chemistry', 100, 1001, 200, 300, 'anubhav','garima','anubhav']

# to target insert we have insert mention the index and insert to that particular index.
lst.insert(1,"choudhary")
# pop will remove the last element or the index provided in the paranthesis
lst.pop() 
# count will count the occurences of element in the list 
lst.count("Mathematics")=> 1
# index it will tell between which indexes you want to find the occurences of a particular element
lst.index("Mathematics",1,7)=> 0 => because Mathematics is at 0th index but we are searching b/w 1 & 7


# Operation sum, **operations and methods are two different things remember**
# sum will try to do the sum if the list is of integers
list1=[2,3,4,5,6]
print(sum(list1))=> 20

# list comprehension in list :
nums=[x**2 for x in range(2,15)]
print(nums) => [4, 9, 16, 25, 36, 49, 64, 81, 100, 121, 144, 169, 196]

# Mutable and Immutable concept in lists
* As lists are mutable so if we create two lists namely l1 and l2 and l1=[1,2,3] and in l2 we say l2=l1 then they are refrencing same continuos memory at this time but is we say now l1=2 now l1 is taking refernce from a integer value 2 , but if we re assign the same list as previously l1=[1,2,3] now they both are taking refernce from different continuos memory to test that we can change any element present in l1 like l1[0]=44 now if we print both l1 and l2 we will get l1 => [44,2,3] but l2 => [1,2,3] because list is mutable so new memory is created. because if user changes any thing in one list it will affect other so thats why we see these discrpencies and it is not actually a discrepency. 

and there is one shortcut also if we assign like this l2= l1[:] now a copy of the same value is assigned now they are referencing different continuous memory at this time.

or  we can import copy
and then assign l1=[1,2,3]
l2=copy.copy(l1)

# Or we can check if l1 is l2
l1=[1,2,3]

l2=l1

print(l1==l2)

print(l1 is l2)

l2=[1,2,3]

print(l1==l2)

print(l1 is l2)

* output:- 
True
True
True
False


# Dictionary
number_of_students_in_each_subject={"physics":30,"Mathematics":50,"Chemistry":20}
number_of_students_in_each_subject={"physics":30,"Mathematics":50,"Chemistry":20}
print(number_of_students_in_each_subject)
print(number_of_students_in_each_subject["Mathematics"]) => {'physics': 30, 'Mathematics': 50, 'Chemistry': 20}
50
# Nested dict
beverages={"hot":{"tea":"lemon",coffee:"capchino"},"cold":{"tea":"ice tea","coffee":"cold coffee"}}
print(beverages) => {'hot': {'tea': 'lemon', 'coffee': 'capchino'}, 'cold': {'tea': 'ice tea', 'coffee': 'cold coffee'}}
print(beverages["hot"]["tea"]) => lemon

# list comprehension in dictionary
square_roots={x:x**2 for x in range(3,15)}
print(square_roots) => {3: 9, 4: 16, 5: 25, 6: 36, 7: 49, 8: 64, 9: 81, 10: 100, 11: 121, 12: 144, 13: 169, 14: 196}

# Creating a dict from list
tea=["Masala","ginger","lemon"]
default_value="tasty"

new=dict.fromkeys(tea,default_value) => {'Masala': 'tasty', 'ginger': 'tasty', 'lemon': 'tasty'}
new=dict.fromkeys(tea,tea) => {'Masala': ['Masala', 'ginger', 'lemon'], 'ginger': ['Masala', 'ginger', 'lemon'], 'lemon': ['Masala', 'ginger', 'lemon']}

# Function
 * syntax
def definitionORfunction_name(parameters):
     return

# lambda function
cube=lambda x: x**3
print(cube(2)) => 8

# function with unknown number of parameters
def sum(*args):
     sum(args)

     or
def sum(*args):
     sum=0
     for i in args:
          sum+=i
     return sum

def print_in_kwargs(**kwargs):
     for key,value in kwargs.items():
          print(f"{key}:{value}")

print_in_kwargs("name"="shaktiman","power"="Lazer","enemy":"dr. jaykaal")

# Yield instead of Return in functions or definitions

def even_generator(limit):
    for i in range(2,limit,2):
        yield i
for num in even_generator(10):
    print(num)

# Scope Closure

def chaicoder(num):
    def actual(x):
        return x**num
    return actual

f=chaicoder(2)
g=chaicoder(3)

print(f(2)) => 4
print(g(2)) => 8

# OOPS