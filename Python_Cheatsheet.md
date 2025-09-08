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


