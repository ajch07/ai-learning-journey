# Understand basics of python:-
10**2= 100
3 * 'anubhav'=> anubhavanubhavanubhav
10*2= 20

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

# Question where will these names resides
* In Python, names are created inside namespaces—not in the “heap vs stack” sense, but in mapping-like scopes that bind a name (the label) to an object (the value).

# String 
# Methods=> upper,lower,isaplhanum ,isdigit,isalpha,count,islower,isupper
str.isalphanum() ...

* split  str[2:9] to jump characters is string str[2:9:2] => it will jump every other character
len(str)=> to find the length
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




