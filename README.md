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

   

---

## 27 November 2022



###### 1. Today I, learned about Template inheritance with static files in django

- ***extends*** tag is used to inherit templates

- `{% extends 'parent_template with location' %}` 

- ***block*** tag is used to override specific parts of template

- `{% block blockname %}` and for ending `{%endblock blockname%}` 

- **Rules**

  - If we use extend tag, it must be first template tag

  - Its better to use more blocks in parent template

  - Child template don't have to define all parent blocks

  - We can't define multple block having same name in same template

  - `{{block.super}}` is used along with block tag in child template to get the content of the block from parent template

    

###### 2. Today, I learned how to use Bootstrap and Font Awesome in django project

###### 3. Today, I learned to create Hyperlinks and Use url Tag in django

- ***url tag*** : retunrs an absolute path reference matching a given view and optional parameter
  - `{%url 'urlname' %}` `{%url 'urlname' as var %}` 

- ***path()***: returns an element for inclusion in urlpatterns

  - > path(route,view,kwargs=None,Name='urlname'/None)

###### 4. Today i  learned to include template inside another template

- ***include tag***: loads a template and renders it with the current context

  - `{%include temp_var_name%}` or `{%include 'templaye_name.html'%}` 

  - we can pass additional context explicitly to the template using `with` keyword
  - `{% include "any_template" with a="anything" b="another thing"%}``{% include "course.html" with d="Django" p="PHP"%}`
  - we can render the context only with the variables provided using `only` option
  - `{% include "course.html" with "PHP" only%}`

---

## 28 November 2022

###### 1. Today, I learned about github commit

- ***Commits***: are snapshots of entire repository at specific times... based around logical units of change
- **Tips for writing commit **:
  - Outline your narrative, and recognize commits to match it
  - Make each commit both "small" and "atomic"
  - Describe what you’re doing and why you’re doing it in the commit message.

---

## 29 November 2022

###### 1. Today, I learned about cookies

###### 2. Today I learned about ORM, QuerySet , Model, Fetching data from DB, admin application, register model class,ModelAdmin Class in Django

- ***ORM***: Object Relational Mapper, enables application to interact with database

  - ***ORM***  automatically creates a database schema from defined classes or models
  - ***ORM*** maps objects attributes to respective table fields

- ***QuerySet***: list containing all objects we have created using Django model

- ***QuerySet***: generally associated with CRUD applications

- ***Model***: single definitive source of information (essential fields and behavior) about data where each model maps to a single database table

- ***Model Class***: class which will represent a table in database

  - each model is a subclass of django.db.models.Model

  - each attribute of model represents a database field

  - syntax: 

    `class ClassName(models.Model):`

    ​	`field_name=models.FieldType(arg,options)`

    - this class will create a table with columns and their data types
    - Table name= ApplicationName_ClassName
    - Column name=field_name

- ***Migrations***: are Django's way of propagating changes in models into respective database schema
  - ***makemigrations***: responsible for creating new migrations based on the changes in models
  - ***migrate***: responsible for applying and unapplying migrations
  - ***sqlmigrate***: displays the SQL statements for a migratiom
  - ***showmigrations***: lists a project's migrations and their status

- ***all()***:returns a copy of current QuerySet or QuerySet Subclass
  `ModelClassName.objects.all()`

- ***get(pk=value)***:returns object having primary key==value `ModelClassName.objects.get(pk=2)`
- ***Super User***: used to login into admin interface of admin application
   `python manage.py createsuperuser`

- ***__str__()***:returns human-readable representation of model 
  we include this inside class in models.py folder 
  `def __str__(self):  `
  `return self.fieldName`

- ***ModelAdmin Class***: is the representation of model in admin interface we use this class inside admin.py file of application folder
  **Creating Class**: `Class ModelAdminClassName(admin.ModelAdmin):  ModelAdmin Options=('fieldname1','fieldname2'....)`

  **Register Class**: `admin.site.register(ModelClassName, ModelAdminClassName)`

  A **decorator** can be used to register ModelAdmin Classes
  `@admin.register(ModelClassName1,ModelClassName2,...)`
   `Class ModelAdminClassName(admin.ModelAdmin):  ModelAdmin Options=('fieldname1','fieldname2'....)`

  ***ModelAdmin Options***

  - list_display(): controls which fields are displayed on the change list page of admin (value must be list or tuple)

---

## 30 November 2022

###### 1. Today, i learned about Django Forms,id Attribute, dynamic initial values, ordering form field, rendering form fields,Loop Form, Form FIeld ,Form Arguments in Django

- Create Django Form using Form Class

  `from django import forms`

  `class FormClassName(forms.Form):`

  ​	`label=froms.FieldType()`

  ​	`label froms.FieldType(label='display_label')`
  `label=forms.FieldType(widget=forms.HiddenInput)` for hidden field

- Id Attribute can be configured using `auto_id` parameter while creating object of Form class
  - `auto_id = True` : use field name as its id for each form field
  - `auto_id='formatstring with %s'`: id attribute is based upon the format string
  - `auto_id = False` : will not include <label> tags nor id attributes
  - `auto_id = 'string without %s'` : acts as if auto_id is True

- Dynamic Initial value `initial` is used to declare initial value of form fields at runtime.
- ***Ordering Form Field***:
  `fm=FormClassName()`
  `fm.order_fields(field_order=['fieldname1','fieldname2',...])`
- FIeld Arguments:
  - `required`: specifies that the field value is required or not
  - `label`: specifies the 'human-friendly' label for field
  - `label_suffix`: lets us to override the form's label_suffix on a per-field basis
  - `initial`: lets us specify initial value in an unbound Form
  - `disabled`: when true it desables a form field 
  - `help_text`:lets us specify descriptive text for this Field
  - `error_messages`: lets us override default messages that the field will rise
  - `validators`: lets us provide a list of validation functions for the field
  - `localize`: enables the localization of form data input as well as rendered output
  - `widget`: is Django's representation of HTML input elements and lets us specify a widget class to use when rendering the field

---

## 1 December 2022

###### 1. Today, I learned about Widget in Django Form, GET and POST method, CSRF token, Field Validation, HttpesponseRedirect, FieldType, Cleaning and Validating Specific Field

- **Widget** is Django's representation of HTML input elements and lets us specify a widget class to use when rendering the field
- **Widget** deals with rendering of HTML form input elements on the web page and extraction of raw submitted data
- Built-in Widgets
  - TextInput, NumberInput, EmailInput, URLInput, PasswordInput, HiddenInput, DateInput ,DateTimeInput, TimeInput, Textarea, Select, SelectMultiple, RadioSelect, FileInput, etc. 

- **is_valid()**: method used to run validation 
  syntax: `Form.is_valid()` 

- ***cleaned_data***: attribute used to access clean data

- we use **HttpResponseRedirect** to redirect to any other page

  - ```
    response = HttpResponseRedirect(response item)
    ```

- Built-in Fields

> <table>
>     <tr>
>         <th>Fields</th>
>         <th>Default widget</th>
>         <th>Validators</th>
>         <th>Error Message Keys</th>
>     </tr>
>     <tr>
>         <td>CharField</td>
>         <td>TextInput</td>
>         <td> MaxLengthValidator, MinLengthValidator</td>
>         <td> required, max_length, min_length</td>
>     </tr>
>     <tr>
>         <td>BooleanField</td>
>         <td>CheckBoxInput</td>
>         <td>-</td>
>         <td> required</td>
>     </tr>
>     <tr>
>         <td>IntegerField</td>
>         <td>NumberInput when Field.localize is False, else TextInput</td>
>         <td>MaxValueValidator, MinValueValidator</td>
>         <td> required, invalid, max_value, min_value</td>
>     </tr>
>      <tr>
>         <td>FloatField</td>
>         <td>NumberInput when Field.localize is False, else TextInput</td>
>         <td>MaxValueValidator, MinValueValidator</td>
>         <td> required, invalid, max_value, min_value</td>
>     </tr>
>     <tr>
>         <td>DecimalField</td>
>         <td>NumberInput when Field.localize is False, else TextInput</td>
>         <td>MaxValueValidator, MinValueValidator</td>
>         <td>required, invalid, max_value, min_value, max_digits,max_decimal_places, max_whole_digits</td>
>     </tr>
>     <tr>
>         <td>SlugField</td>
>         <td>TextInput</td>
>         <td>validate_slug, or validate_unicode_slug</td>
>         <td> required, invalid</td>
>     </tr>
>     <tr>
>         <td>EmailField</td>
>         <td>EmailInput</td>
>         <td>EmailValidator</td>
>         <td> required, invalid</td>
>     </tr>
>     <tr>
>         <td>URLField</td>
>         <td>URLInput</td>
>         <td>URLValidator</td>
>         <td> required, invalid</td>
>     </tr>
>     <tr>
>         <td>DateField</td>
>         <td>DateInput</td>
>         <td>datetime.date, datetime.datetime</td>
>         <td> required, invalid</td>
>     </tr>
>     <tr>
>         <td>TimeField</td>
>         <td>TimeInput</td>
>         <td>datetime.date, datetime.datetime</td>
>         <td> required, invalid</td>
>     </tr>
>     <tr>
>         <td>FileField</td>
>         <td>ClearableFileInput</td>
>         <td>-</td>
>         <td> required, invalid, missing,empty,max_length</td>
>     </tr>
>     <tr>
>         <td>ImageField</td>
>         <td>ClearableFileInput</td>
>         <td>FileExtensionValidator</td>
>         <td> required, invalid, missing, empty, invalid_image</td>
>     </tr>
> </table>

- ***clean_<fieldname>()***: used in form subclass to validate specific field
  `def clean_fieldname(self): `

  ​	`var =self.cleaned_data['fieldname']`

  ​	`//validation code here`	

- ***clean()***: in form subclass is responsible for running __python(),validate() and run_validators() to validate complete Django form at once`Form.clean()`

​		`def clean(self): `

​			`cleaned_data =super().clean()`

​			`var =self.cleaned_data['fieldname1']`

​			`//validation code here`	

​			`var =self.cleaned_data['fieldname2']`

​			`//validation code here`	

