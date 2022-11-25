# Today I Learned

---

## 21 November 2022

###### 1. Today, I learned about git-hub

##### Basic Commands

- *git init*                                                  //Initialize Local Git Repository

- git add                                               //Add Files 

- *git status*                                            *//Checks Status of Working Tree*

- *git commit*  *-m "Initial commit"*      //Commit Changes 

- *git remote*  *-v*                                  //shows remote repositories url

- *git clone*                                      *// to copy an existing Git repository from a server to the local machine.*

- *git push*                                        //updates the remote repository 

- git revert {commit-id}               //removes the commit  (use if code is pushed)

- git reset  --hard                       //removes commit and rewrites history (can use commit-id or HEAD, HEAD^, HEAD~2, HEAD~3...)

- git branch                                   //shows the branches being worked on locally

- git pull                                         // updates the local repository

- git fetch                                      //shows changes made in remote repository

- git merge                                   //combines changes made on two distinct branches

- git log                                         //shows commit history

- git remote add upstream        // tracks upstream

  

###### I learned how to connect to git-hub with ssh key.

###### I learned how to create a pull request

###### I learned about fork, upstream and origin

###### I learned how to resolve merge conflicts.

merge conflicts occur  when two people have changed the same lines in a file

###### 2. Today, I learned about Templates in Django

templates are of two types  i) static and ii) dynamic

templates can be saved inside each app also common template can be used

---



## 22 November 2022

###### 1. Today, i learned more about templates in django

both common and separate templates folder can be used at the same time 

###### 2. Today , i learned about static files in django

files like JS, CSS, images, videos are static files

we must load static files before using in templates using 

> {%load static%}

 ###### common variables

- **STATIC_URL** : is the URL to use when referring to static file located in STATIC_ROOT
- **STATIC_ROOT**: is absolute path to directory where collectstatic will collect static files for deployment
- **STATICFILES_DIRS**: defines the additional locations 
- **STATICFILES_STORAGE**: is file storage engine to use when  collecting static files

###### 3. Today, i learned about exception handling in python 

---

## 23 November 2022

###### 1. Today , i learned about  iterators, generators, closure, decorators, property, regular expression in python

- **closure** in python is technique by which some data gets attached to the code
- python **decorator** is a function that takes in a function, adds some functionality to it and returns original function
- An underscore `_` at the beginning is used to denote private variables in Python
- In Python, **property()**  is a built-in function that creates and returns a property object. 
- `property(fget=None, fset=None, fdel=None, doc=None)`
- A **Regular Expression (RegEx)** is a sequence of characters that defines a search pattern. 
- we use r or R prefix to denote raw string while working with RegEx

---

## 24 November 2022

###### 1. Today, i learned about datetime module ,time module, handling timezone, multi-threading in python

**Commonly used classes in datetime modules**

- ***datetime.date*** : any date object represents a day (year, month and day)
- ***datetime.time*** : any time object represents local time
- ***datetime.datetime***: contains both date and time objects
- ***datetime.timedelta***: any timedelta object represents the difference between two dates or times (can perform arithmetic operation)
- ***datetime.fromtimestamp()***:returns local date and time from timestamp
- ***datetime.timestamp()***:returns timestamp from a datetime

**Commonly used time-related functions**

- ***time.time()***:returns number of seconds passed since epoch
- ***time.sleep()***:delays execution of the current thread for the given number of seconds
- ***time.localtime()***: returns `struct-time` in local time

**Methods to handle datetime format**

we make use of format codes here like %m for months %d for day %Y for year and many more

- ***strftime()***: returns string representing date and time for datetime object
- ***strptime()***:creates datetime object from a given string

To handle timezone in python we use model pytz

**we use `threading.Thread(target=<value>` to perform multi-threading in python** 

---

## 25 November 2022

###### 1. Today, I learned about OOPS concepts in python

- ***Class***: blueprint for object

- ***Object***: instance of class

- ***Encapsulation***: way to restrict the direct access to some components of an object (to define private we use `_` or` __`)

- ***Inheritance***: way of creating a new class for using details of an existing class without modifying it

- ***Polymorphism***: ability to use a common interface for multiple forms

- ***super()***:returns proxy object that allows us to access methods of base class

- ***Operator Overloading***: extended meaning beyond predefined operational meaning of operators (we use **Magic Methods** to overload operators)

- ***Method Resolution Order (MRO)***:the set of rules used to find the search order in multiple inheritance

- ***Magic Methods***: special methods that start and end with the double underscores

   









