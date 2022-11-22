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







