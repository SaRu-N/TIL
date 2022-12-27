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

---

## 4 December 2022

###### 1. Today, I learned about built-in validators, custom form validators, match two field value, styling field error, save data to database using django form api

- Built-in validators are available in django.core module
  - `from django.core import validators`
    `fieldname=forms.FieldType(validators=[validators.<required validation>])`

- we can define our own validator as per requirement

  - suppose we have to take input starting with s :

    `def starts_with_s(value):`
    	` if value[0]!='s':`
    			` raise forms.ValidationError("Value must start with s")`

​			`fieldname=forms.FieldType(validators=[starts_with_s])`

- to render errors
  -  `{{field.errors}}` to display all errors in same field at the same time `{% for error in field.errors %}`
  - `{{form.non_field_errors}}` written at the top of the form and template lookup for errors on each field

- Styling Django form errors
  - we can use class `errorlist` to style errors
  - `error_css_class` and `required_css_class` : are class hooks that can be used to add class attributes to required rows or rows with errors.(rows should be given "error" and/or "required" classes as per requirement)

- To save data into database using django form api 

  - code inside function of views.py

    `if formvar.is_valid():`

    ​		`var1= formvar.cleaned_data['fieldname1']`

    ​	   `var2= formvar.cleaned_data['fieldname2']`

      	  `var=model_name(fieldname1=var1,fieldname2=var2)`

    ​        `var.save()`

  - here `save()` method is used to save data in database

  - if we provide specific id in var and save var it updates the value having that id

  - to delete specific data :

    - we only write that specific id in var 
    - instead of var.save() we write `var.delete()`

###### 2. Today i learned about model form in Django

-  ***ModelForm***: is a helper class provided by django that lets us create a Form class from a Django Model

  - create ModelForm class (Model class must be created)
    syntax: in forms.py

    ​	`class ModelFormClassName(forms.ModelForm):`

    ​		`class Meta:`
    ​				`model=ModelClassName`
    ​				`fields=['fieldname1','fieldname2','fieldname3']` form comes in the same order 

  

---

## 5 November 2022

###### 1. Today, I learned about Model Form, adding label,help text,error messages ,widgets, validators to fields of Model Form, CRUD using ModelForm

- some important points to be considered while using Model Form:
  - if model field has `blank=True` then required is st to False on that form field
  - form field's `label` is set to `verbose_name` of the model field, with first character capitalized
  - form field's `help_text` is set to the `help_text` of the model field

- adding label to fields
  `labels= {'fieldname1':'label1','fieldname2':'label2','fieldname2':'label2'}`

- adding help text to fields 

  `help_texts={'fieldname1':'help text here'}`

- adding error messages 
  `error_messages ={'fieldname1':{'required':'message here'}, 'fieldname2':{'required':'message here'}}`
- adding widgets 
  `widget={'fieldname1':widgetvalue,'fieldname2':widgetvalue}`
- adding validators (before Meta class)
  `'fieldname'=forms.FieldType(Validations Here)`
- **Save() Method**: creates and saves a database object from the data bound to the form.
  - subclass of ModelForm can accept an existing model instance as keyword argument instance, if this is supplied, save() will update that instance
  - if not supplied, save() will create a new instance of the specified model.
  - if the form hasn't been validated, calling `save()` will do so by checking form.errors
  - Syntax: `save(commit=False/True)` 

###### 2. Today i learned about Dynamic URL, Custom Path Converters in Django

- normal url pattern:
  `path(route,views,kwargs=None,name=None)`

- dynamic url pattern:
  `path(route/<id>,views,kwargs=None,name=anyname)`

  `path(route/<int:id>,views,kwargs=None,name=anyname)`
  `path(route/<int:id>/<int:subid>,views,kwargs=None,name=anyname)`

- **Path Converters**:
  - ***str***: matches any non-empty string excluding '/'. this is default if no path path converter is included
  - ***int***: matches zero or any positive integer. Returns an int
  - ***slug***: matches any slug string consisting of ASCII letters or numbers, hyphen, underscore characters
  - ***uuid***: matches a formatted UUID. Returns a UUID instance
  - ***path***: matches any non-empty string including '/'. this allows us to match against a complete URL path rather than a segment of a URL path as with str

- **Custom Path Converters**:

  - we can create custom path converter by following below steps

    1. **create a path converter class inside converters.py file**

    `class ClassName:`

    ​	`regex = 'your regex here'`

    ​	`def to_python(self,value):`
    ​				`return int(value)`

       `def to_url(self,value):`
    	             `return '%04d' % value`

    Here,

    - ***regex*** is an attribute, as a string
    - ***to_python(self,value)*** method handles converting the matched string into the type that should be passed to the view function.
    - ***to_url(self,value)*** method handles conveting the Python type into a string to be used in the URL
      2. **Register path converter in urls.py**
         `from django.urls import register_converter`
         `from . import converters`
         `register_converter(converters.ClassName,'anyname')`
         `path('route/<anyname:value>/',views,kwargs,name)` 

- **Kwargs**: this argument allows us to pass additional arguments to view function or method. It should be a dictionary

  - `path(route/views,{'check':'Ok},name=None)` here {'check':'Ok} is kwargs this goes in views function

---

## 7 December 2022

###### 1. Today, i learned about selecting modelForm Fields, ModelForm Inheritance, Messages Framework

- Selecting ModelForm Field
  - using fieldname
    `fields=['fieldname1','fieldname2','fieldname3']`
  - using `__all__`
    `fields='__all__'`
  - using exclude: this excludes the mentioned field and display other fields as form
    `exclude=['fieldname']`

- ModelForm Inheritance

  - Base Class

    ​	`class ModelFormBaseClassName(forms.ModelForm):`

    ​		`class Meta:`
    ​				`model=ModelClassName`
    ​				`fields=['fieldname1','fieldname2','fieldname3']` 

  - Derived Class

    ​	`class ModelFormDerivedClassName(ModelFormBaseClassName):`

    ​		`class Meta(ModelFormBaseClassName.Meta:`
    ​				`fields=['fieldname1','fieldname2','fieldname3']` 

- The message framework allows us to temporarily store messages in one request and retrieve them for display in a subsequent request

- **Message Level**: allows us to group messages by type so they can be filtered or displayed differently in views and templates

- **Message Tag**: are a string representation of the message level plus any extra tags that were added directly in the view.

  > <table>
  >     <tr>
  >         <th>Level</th>
  >         <th>Tag</th>
  >         <th>Value</th>
  >         <th>Purpose</th>
  >     </tr>
  >     <tr>
  >         <td>DEBUG</td>
  >         <td>debug</td>
  >         <td>10</td>
  >         <td>development related messages that will be ignored or removed in a production deployment</td>
  >     </tr>
  >     <tr>
  >     	<td>INFO</td>
  >         <td>info</td>
  >         <td>20</td>
  >         <td>information messages for the user</td>
  >     </tr>
  >         <tr>
  >     	<td>SUCCESS</td>
  >         <td>success</td>
  >         <td>25</td>
  >         <td>an action was successful</td>
  >     </tr>
  >         <tr>
  >     	<td>WARNING</td>
  >         <td>warning</td>
  >         <td>30</td>
  >         <td>a failure did not occur but may be imminent</td>
  >     </tr>
  >         <tr>
  >     	<td>ERROR</td>
  >         <td>error</td>
  >         <td>40</td>
  >         <td>an action was not successful or some other failure occured</td>
  >     </tr>
  > </table>

- How to use message framework

  - ***Write Message***: `add_message(request,level,message, extra_tags='',fail_silently=False)`  - this methid is used to add/write messages.

    `from django.contrib import messages`
    `messages.add_message(request,level,message,  extra_tags='')`

  - ***Write message by Shortcut method***:

    `from django.contrib import messages`
    `messages.tag(request,message)`

  - ***Display Message***:

    `{% if messages %}`
             `{% for m in messages %}`
                         `{% if m.tags %} {{m.tags}} {% endif %}`
                          `{{m}}`

    ​        ` {% endfor %}`

    `{% endif %}`

    

---

## 8 December 2022

###### 1. Today, i learned about Methods, Changing Tags in Message Framework

-  Methods

  - ***get_level()***: this method is used to retrieve the current effective level.

    `current_level =messages.get_level(request)`

  - ***set_level()***: this method is used to set minimum recorded level
    `messages.set_level(request,messages.DEBUG)` this will record messages with a level of DEBUG and higher

  - ***get_messages(request)***:this method is used to get message  (if we want to get message outside template)
    `from django.contrib.messages import get_messages`
    `storage = get_messages(request)`
    `for message in storage:`

    `do_whatever_you_want_to_do_with_message(message)`

- Change Tags
  - open settings.py
    `from django.contrib.messages import constants
    MESSAGE_TAGS={constants.level:'new_tag'}`

###### 2. Today, i learned about authentication and authorization, User Authentication System in Django, Change user password with or without old password

- **Authentication**: is about validating credentials to verify identity
- **Authorization**: is the process to determine whether the authenticated user has access to the particular resources.
- Django authentication provides both authentication and authorization together
- User Object Fields
  - username: may contain alphanumeric,_,@,+,.and - characters and max_length=150, required
  - first_name:optional, max_length=30
  - last_name:optional, max_length=150
  - email:optional
  - password: required, django doesn't store raw password
  - groups: Many-to-many relationship to Group
  - user_permissions: Many-to-many relationship to permission
  - is_staff: Designates whether this user can access the admin site
  - is_superuser:Designates that this user has all permissions without explicitly assigning them
  - is_active:Designates whether this user account should be considered active
  - last_login: a datetime of user's last login
  - date_joined: a datetime designating when account was created
  - is_authenticated: way to tell if the user has been authenticated
  - is_anonymous: way of differentiating user and anonymous user objects

- User Objects Method
  - get_username(): returns username for the user
  - get_full_name(): returns first_name and last_name with space in between
  - get_short_name(): returns the first_name
  - set_password(raw_password): sets user's password to the given raw string, taking care of the password hashing
  - check_password(raw_password): returns true if the given raw string is the correct password for the user.
  - get_user_permission(obj=None):returns a set of permission strings that the user has directly
  - email_user(subject,message, from_email=None,**kwargs):sends an email to the user

- UserManager Methods
  - create_user(username,email=None,password=None,**extra_fields):creates,saves and returns an User
  - create_superuser(username,email=None,password=None,**extra_fields):same as create_user(), but sets is_staff and is_superuser to True

- Group Object Fields
  - name: required, max_length=150
  - permissions: Many-to-many field to permission

- Permission Object Fields
  - name: required, max_length=255
  - content_type: a reference to django_content_type database table, which contains a record for each installed model, requires
  - codename: required, max_length=100

- ***authenticate(request=None, \*\*credentials)***: used to verify a set of credentials
- ***login(request,user, backend=None)***: to log a user in from a view use login()
- ***logout(request)***: to log out a user who has been logged in via django.contrib.auth.login() 
- to change password using old password we use  `PasswordChangeForm()`
- to change password without using password we use `SetPasswordForm()` 
  both  `PasswordChangeForm()` and `SetPasswordForm()`  are defined in django.contrib.auth.forms

---

## 9 December 2022

###### 1. Today, i learned about User Profile, Admin Profile , Permission and Authorization in Django

- Django admin site uses permissions as follows (these are automatically generated by Django when model is created):
  - view
  - add
  - change
  - delete

- Some methods
  - myuser.groups.set([group_list]): sets group
  - myuser.groups.add(group, group, ...): adds group
  - myuser.groups.remove(group,group, ...):  removes group
  - myuser.groups.clear(): clears group
  - same for user_permission too (myuser.user_permissions.set([permission_list]))

- Permission name follows a specific naming convention `appname.action_modelname`
- The currently logged-in user's permissions are stored in the template variable {{perms}}.
       example:
              `{% if perms.appname.action_modelname %} 
              // code here 
                {% endif %}`

---

## 13 December 2022

###### 1. Today, I learned about cookies in django

- ***cookies***: is a small piece of text data set by web server that resided on the client's machine
- ***set_cookie()***: is used to **set/create/sent cookies**
  syntax : `HttpResponse.set_cookie(key, value='', max_age=None,expires=None,path='/', domain=None, secure=False, httponly=False, samesite=None)`
  - key: name of the cookie
  - value=value of the cookie (this value is stored on the clients computer)

- ***HttpRequest.COOKIES***:directory containing all cookies, Keys, and values are strings.
  syntax: `request.COOKIES['key'];`
  `request.COOKIES.get('key', default)`
- ***delete_cookie()***: used to delete the cookie based on given key with same domain and path if they were set
  syntax: `HttpResponse.delete_cookie(key,<other attribute if set>)`

- Creating Signed Cookies
  - ***set_signed_cookie()***:
    syntax: `HttpResponse.set_signed_cookie(key, value,salt='', max_age=None,expires=None,path='/', domain=None, secure=False, httponly=False, samesite=None)`

- Getting Signed Cookies
  - ***get_signed_cookie()***:
    syntax: `HttpResponse.get_signed_cookie(key,default=RAISE_ERROR,salt='',max_age=None)`

---

## 14 December 2022

###### 1. Today, i learned about Session in Django

- Session stores data on server side and abstracts the sending and receiving of cookies . Cookies contain a session Id not the data itself.
- Types of sessions
  - database-backed sessions: must add `django.contrib.sessions` in INSTALLED_APPS
  - file-based sessions :set the SESSION ENGINE setting to `django.contrib.sessions.backends.file` 
  - cookie-based sessions: set the SESSION ENGINE setting to `django.contrib.sessions.backends.signed_cookies`
  - cached sessions
- Using sessions in views
  - Set Item:
    `request.session['key']='value'`
  - Get Item
    `returned_value = request.session['key']`
    `returned_value = request.session.get('key', default=None)`
  - Delete Item
    `del request.session['key']`
  - contains
    `key in request.session`

- Session Methods
  - keys(): returns a view object that displays a list of all the keys in the dictonary 
    syntax: `dict.keys()`
  - items(): returns the list with all dictionary keys with values
    syntax: `dict.items()`
  - clear(): used to erase all the elements of list
    syntax: `dict.clear()`
  - setdefault(): returns the value of a key if the key is in dictionary else inserts key with a value to the dictionary 
    syntax: `dict.setdefault(key,default_value)`
  - flush(): deletes current session data from the session and deletes the session cookie
    syntax: `dict.flush()`
  - get_session_cookie_age(): returns the age of session cookies, in seconds.
  - set_expiry(value): sets the expiration time for the session
  - get_expiry_age(): returns number of seconds until this session expires
  - get_expiry_date(): returns the date this session will expire
  - get_expire_at_browser_close(): returns either True or False
  - clear_expires(): removes expired sessions from the session store
  - set_test_cookie(): sets a cookie to determine whether the user's browser supports cookies.
  - test_cookie_worked(): returns either True or False, depending on whether the user's browser accepted the test cookie.
  - delete_test_cookie(): deletes the test cookie

- Session Settings
  - SESSION_CACHE_ALIAS: while using cache-based session, this selects the cache to use. Default= 'default'
  - SESSION_COOKIE_AGE: age of session in seconds. Default = 1209600 
  - SESSION_COOKIE_DOMAIN: domain to use for session cookies
  - SESSION_COOKIE_HTTPONLY: whether to use HttpOnly flag on the session cookie. Default=True
  - SESSION_COOKIE_NAME: name of the cookie to use for sessions
  - SESSION_COOKIE_PATH: path set on session cookie
  - SESSION_COOKIE_SAMESITE: value of SameSite flag on session cookie, this flag prevents cookie from being sent in cross-site requests
  - SESSION_COOKIE_SECURE: whether to use a secure cookie for the session cookie
  - SESSION_ENGINE: controls where Django stores session data 
  - SESSION_EXPIRE_AT_BROWSER_CLOSE: whether to expire the session when the user closes their browser. Default:false
  - SESSION_FILE_PATH: while using file-based session storage, this sets the directory in which Django will store session data
  - SESSION_SERIALIZER: full import path of the serializer class to use for serializing session data.

---

## 16 December 2022

###### 1. Today, i learned about QuerySet API Methods that return QuerySets

- QuerySet is a list containing all those objects we have created using Django model

- QuerySet allow us to read the data from the database, filter it and order it

- query property: this is used to get sql query of query set
  syntax: `queryset.query`
  
- **Methods that returns new QuerySets**
  
  - Retrieving all objects 
    ***all()***: returns a copy of current QuerySet.
    
  - Retrieving specific objects
    - ***filter(\*\*kwargs)***: returns a new QuerySet conatining objects that match the given 'lookup parameters'
    
    - ***exclude(\*\*kwargs)***: returns a new QuerySet object that do not match the given 'lookup parameters'
    
    - ***order_by(\*fields)***: orders the field ('field':Asc Order, '-field':Desc Order, '?':Randomly)
    
    - ***reverse()***: this works only when there is ordering in queryset
    
    - ***values(\*fields,\*\*expressions)***: returns a QuerySet that returns dictonaries, rather than model instances, when used as an iterable. 
    
    - ***values_list(\*fields,flat=False,named=False)***: similar to values() except that instead of returning dictonaries, it returns tuples when iterated over
    
    - ***using(alias)***: used for controlling which database the queryset will be evaluated against if you are using more than one database. this takes only argument which is alias of database, as defined in DATABASES
    
    - ***dates(field,kind,order='ASC')***: returns a QuerySet that evaluates to a list of datetime.time objects representing all available dates of a paerticular kind within the contents of the QuerySet
      kind: year , month , week or day
    
    - ***datetimes(field_name,kind, order='ASC', tzinfo=None)***: returns a QuerySet that evaluates to a list of datetime objects representing all available dates of a particular kind within the contents of the QuerySet.
    
    - ***none()***: calling none will create a QuerySet that never returns any objects and no query will be executed when accessing the results.
    
    - ***union(\*other_qs,all=False)***: uses SQL's UNION operator to combine the results of two or more QuerySets.
    
    - ***intersection(\*other_qs)***: uses SQL's INTERSECT operator to return the shared elements of two or more QuerySets.
    
    - ***difference(\*other_qs)***: uses SQL's EXCEPT operator to keep only elements present in the QuerySets but not in some other QuerySets
    
    - Other Methods
      ***select_related(\*fields)***    
    
      ***defer(\*fields)***    
    
      ***only(\*fields)***  
    
      ***prefetch_related(\*lookups)***    
    
      ***extra(select =None, where=None,params=None,tables=None,order_by=None,select_params=None)***    
    
      ***select_for_update(nowait=False,skip_locked=False,of=())***    
    
      ***annonate(\*args,\*\*kwargs)***    

- **Operators that return new QuerySets**
  - AND(&): combines two QuerySets using the SQL AND operator
  - OR(|): combines two QuerySets using SQL OR operator

---

## 19 December 2022

###### Today, i learned about 

###### 1. QuerySet API Methods that do not return QuerySets

- Retrieving a single object 
  ***get()***: returns one single object.

  ***first()***: returns first object matched by the queryset

  ***last()***: returns last object matched by the queryset

  ***latest(\*fields)***: returns latest object in the table based on the given field(s).

  ***earliest(\*fields)***: returns earliest object in the table based on the given field(s).

  ***exists()***:returns True if the QuerySet contains any results, and False if not.

- CRUD
  ***create(\*\*kwargs)***: convenience method for creating an object and saving it all in one step.

  ***get_or_create(defaults=None,\*\*kwargs)***: convenience method for looking up an object with the given kwargs, creating one if necessary.

  ***update(\*\*kwargs)***: performs an SQL update query for the specified fields, and returns the number of rows matched.

  ***update_or_create(defaults=None,\*\*kwargs)***: convenience method for updating an object with the given kwargs, creating a new one if necessary.

  ***bulk_create(objs,batch_size=None,ignore_confilcts=False)***: this method inserts the provided list of objects into the database in an efficient manner.

  ***bulk_update(objs,fields,batch_size=None)***: this method efficiently updates the given fields on the provided model instances, generally with one query.

  ***in_bulk(id_list=None, field_name='pk')***: takes a list of field values (id_list) and the field_name for those values, and returns a dictionary mapping each value to an instance of the object with the given field value.

  ***delete()***: this immediately deletes the object and returns the number of objects deleted and dictionary with the number of deletions per object type

  ***count()***: returns an integer representing the number of objects in the database matching the QuerySet.

  ***explain(format=None,\*\*options)***:returns a string of the QuerySet's execution plan, which details how the database would execute the query, including any indexes or joins that would be used.

  ***aggregate(\*args,\*\*kwargs)***

  ***as_manager()***

  ***iterator(chunk_size=2000)***

###### 2. QuerySet API Field Lookups in Django

- **Field Lookups** are how we specify the meet of an SQL WHERE clause.

  syntax: `field__lookuptype=value`

  - ***exact***: Exact match.
  - ***iexact***: Exact match but case insensitive.
  - ***contains***: Case sensitive containment test.
  - ***icontains***: Case insensitive containment test.
  - ***in***: In a given iterable; often a list, tuple, or queryset. 
  - ***gt***:Greater than
  - ***gte***:Greater than or equal to
  - ***lt***:Less than
  - ***lte***:Less than or equal to
  - ***startswith***:Case sensitive starts_with
  - ***istartswith***:Case insensitive starts_with
  - ***endswith***:Case sensitive ends_with
  - ***iendswith***:Case insensitive ends_with
  - ***range***:Range test (inclusive)
  - ***date***: for datetime fields, casts the value as date, ***year***,***month***,***day***,***week***,***week_day***,***quarter***,***time***,***hour***,***minute***,***second***
  - ***isnull***:
  - ***regex*** and ***iregex***

###### 3. QuerySet API Aggregation

- ***aggregate()***: is a terminal clause for a QuerySet that, when invoked, returns a dictionary of name-value pairs.

  syntax: `aggregate(name=agg_function('field'),  name=agg_function('field'),)`

- Django Provides the following aggregation functions in the `django.db.models` module

  - ***Avg(expression,output_field=None,distinct=False,filter=None,\*\*extra)***: returns the mean value of given expression which must be numeric unless you specify a different output_field.

    Default alias: `<field>__avg`

  - ***Count(expression,distinct=False,filter=None,\*\*extra)***: returns the number of objects that are related through the provided expression

    Default alias: `<field>__count`

  - ***Max(expression,output_field=None,filter=None,\*\*extra)***:returns the maximum value of given expression.

    Default alias: `<field>__max`

  - ***Min(expression,output_field=None,filter=None,\*\*extra)***:returns the minimum value of given expression.

    Default alias: `<field>__min`

  - ***Sum(expression,output_field=None,distinct=False,filter=None,\*\*extra)***:computes the sum of all values of given expression.

    Default alias: `<field>__sum`

  - ***StdDev(expression,output_field=None,sample=False,filter=None,\*\*extra)***:returns the standard deviation of the data in the provided  expression.

    Default alias: `<field>__stddev`

  - ***Variance(expression,output_field=None,sample=False,filter=None,\*\*extra)***:returns the variance of the data in the provided  expression.

    Default alias: `<field>__variance`

---

## 20 December 2022

###### Today I learned about

###### 1. Q Objects

- Q Object is an object used to encapsulate a collection of keyword arguments. we can use Q Objects to execute more complex queries

- Q Objects can be combined using & and | operators. When an operator is used on two Q objects, it yields a new Q object.

- Using Q Objects

  `from django.db.models import Q`

  - & Operator
  - | Operator
  - ~ Operator

###### 2. Limiting QuerySets

- use a subset of Python's array-slicing syntax to limit our QuerySet to a certain number of results.

  Model.objects.all()[:5]- returns First 5 objects

  Model.objects.all()[5:10]- returns sixth through tenth objects

  Model.objects.all()[-1]- this is not valid

  Model.objects.all()[:10:2]- returns a list of every second object of the first 10.

###### 3. Cache and per site Cache in Django

- Cache is an information technology for the temporary storage of web documents, such as Web Pages, images, and other types of Web multimedia to reduce server tag

- Caching is one of the methods which a website implements to become faster

- Options of caching:
  - Database Caching
  - File System Caching
  - Local Memory Caching

-  Implement Caching
  - ***the per-site cache***: Once the cache is set up, the simplest way to use caching is to cache your entire site.
  - ***the per-view cache***: more granular way to use the caching framework is by caching the output of individual views.
  - ***Template fragment Caching***: gives us more control what to cache

- **Per Site Cache**:

  `MIDDLEWARE=[` // must maintain this order

  `'django.middleware.cache.UpdateCacheMiddleware',`

  `'django.middleware.Common.CommonMiddleware',`

  `'django.middleware.cache.FetchFromCacheMiddleware',`

  `]`

  Variables:

  - CACHE_MIDDLEWARE_ALIAS: cache alias to use for storage
  - CACHE_MIDDLEWARE_SECONDS: number of seconds each page should be  cached
  - CACHE_MIDDLEWARE_KEY_PREFIX: if cache is shared across multiple sites using the same Django installation, set this to the name of the site, or some other string that is unique to this Django instance, to prevent key collisions

- **Database Caching**

  Django can store its cached data in our database

  `CATCHES-{'default':{ `

  ​      `'BACKEND':'django.core.cache.backends.db.DatabaseCache',`

  ​      ` 'LOCATION':'my_cache_table', `

  `}}`

  Before using the database cache, we must create the cache table with this command:

  `python manage.py createcachetable`

- **Cache Arguments**: each cache backend can be given additional arguments to control caching behavior
  - ***TIMEOUT***: defalut timeout, in seconds, to use for the cache
  
  - ***OPTIONS***: options that should be passed to the cache backend.
  
    cache backends that implement their own cullling strategy will honor the following options:
  
    - MAX_ENTRIES: maximum no. of entries allowed in the cache before old values are deleted.
    - CULL_FREQUENCY: the fraction of entries that are culled when MAX_ENTRIES is reached.

---

## 22 December 2022

###### 1. Today i learned

###### per site Cache in Django

- **Filesystem caching**

  - serializes and stores each cache value as a separate file.

    `CATCHES-{'default':{ `

     `'BACKEND':'django.core.cache.backends.filebased.FileBasedCache',`

    ​      ` 'LOCATION':'path_of_cache_file', `

    `}}` 

- **Local memory Caching**

  - this is default cache if another is not specified in your settings file. this cache is per-process and thread-safe.

  - `CATCHES-{'default':{ `

     `'BACKEND':'django.core.cache.backends.locmem.LocMemCache',`

    ​      ` 'LOCATION':'unique-snowflake', `

    `}}` 

###### 2. per view Cache in Django

- a more granular way to use caching framework is by caching the output of individual views.

  > from django.views.decorators.cache import cache_page
  >
  > @cache_page(timeout,cache,key_prefix)
  >
  > def view(request):

  specifying per-view cache in URLconf

  > from django.views.decorators.cache import cache_page
  >
  > urlpatterns=[
  >
  > ​	path('route/',cache_page(timeout,cache,key_prefix)(view_function)),
  >
  > ]

###### 3. Template Fragment Cache in Django

- This gives more control what to cache

  {% load cache %}  this gives access to cache tag in template

  {% cache %} this tag caches the contents of the block for a given amount of time.

  Syntax: `{% cache timeout name variable using=""%}........{% endcache name %}`

---

## 23 December 2022

###### Today i learned

###### 1. Model manager in Django

- A manager is interface through which database query operations are provided to Django models.
- to rename a manager for a given class, define a class attribute of type models.Manager() on that model. by default it is objects
- **Custom Model Manager**
  - can use custom manager in a particular model by extending base Manager and inserting custom Manager in our model.

- **Modify the initial QuerySet**

  - can override the Manager's base queryset by overriding the Manager.get_queryset() method get_queryset() should return the new QuerySet of our choice

    > class CustomManager(models.Manager):
    >
    > ​	def get_queryset(self):
    >
    > ​		return super().get_queryset().order_by('name')

- **Add extra Manager methods**
  - adding extra Manager methods is the preferred way to add 'table-level' functionality to the models

>  class CustomManager(models.Manager):
>
> ​	def  custom_methodname(self):
>
> ​				//desired code

---

## 26 Deceber 2022

###### Today I learned about model relationship in django

- Model Relationship
  1. One to One Relationship
  2. One to Many Relationship
  3. Many to Many Relationship

****

- **One to One Relationship**

  - to define, use **OneToOneField**
    syntax:  `OneToOneField(to,on_delete,parent_link=False, **options)`

  - **on_delete**: when an object referred by a ForiegnKey is deleted, Django will emulate the behaviour of the SQL constraint specified by the on_delete argument.

    - CASCADE: Cascade deletes.  Django emulates the behaviour of  SQL constraint ON DELETE CASCADE also deleted the object containig the ForiegnKey.
    - PROTECT: Prevent deletion of the referenced object by raising ProtectectError, a subclass of django.db.IntegrityError
    - SET_NULL
    - SET_DEFAULT
    - SET()
    - DO_NOTHING

    
