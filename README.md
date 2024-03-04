<center> <h1>HBNB - The AirBnB Console</h1> </center>

This repository is  the initial stage of a Python implementation for an AirBnB clone, featuring a command-line interface (CLI) console, developed as part of a student project to replicate the functionality of the AirBnB website. The CLI console serves as the initial backend interface, facilitating user interaction and enabling CRUD (Create, Read, Update, Delete) operations on various data objects and user account management. It ensures data persistence through JSON serialization/deserialization between sessions, allowing users to manage program data effectively. This stage lays the groundwork for subsequent projects, including HTML/CSS templating, database storage, API development, and front-end integration, establishing core functionality and data management capabilities.

## Key Features:
- CLI console for managing AirBnB objects.
- Facilitates CRUD operations and user account management.
- Ensures data persistence through JSON serialization/deserialization.
- Lays the groundwork for subsequent stages, including HTML/CSS templating, database storage, API development, and front-end integration.

## Project Stages

**Stage 1: Console Development**
This initial stage involves the development of the command-line interpreter to manage AirBnB objects, serving as the foundation for the project.

**Stage 2: Static Page Development**
In the second stage, the project involves creating static pages essential for the AirBnB website to enhance the user interface and experience.

**Future Stages:**
Subsequent stages will focus on further enhancing functionality, integrating backend and frontend components, and achieving a fully functional AirBnB clone.

---

## Table Of Contents

1. [Concepts](#concepts)
    - [Python packages](#python-packages)
    - [AirBnB clone](#airBnB-clone)
2. [Background Context](#background-context)
3. [Resources](#resources)
4. [Learning Objectives](#learning-objectives)
5. [Requirements](#requirements)
6. [GitHub](#github)
7. [More Info](#more-info)
8. [Outlined Project Tasks](#outlined_project_tasks)
9. [Structured Overview of Repository Contents](#structured-overview-of-repository-contents)
    - [0. README, AUTHORS](#0-readme-authors)
    - [1. Be pycodestyle compliant!](#1-be-pycodestyle-compliant)
    - [2. Unittests](#2-unittests)
    - [3. BaseModel](#3-base-model))
    - [4. Create BaseModel from dictionary](#4-create-base-model-from-dictionary)
    - [5. Store first object](#5-store-first-object)
    - [6. Console 0.0.1](#6-console-001)
    - [7. Console 0.1](#7-console-01)
    - [8. First User](#8-first-user)
    - [9. More classes!](#9-more-classes)
    - [10. Console 1.0]((#10-console-10)
    - [11. All instances by class name](#11-all-instances-by-class-name)
    - [12. Count instances](#12-count-instances)
    - [13. Show](#13-show)
    - [14. Destroy](#14-destroy)
    - [15. Update](#15-update)
    - [16. Update from dictionary](#16-update-from-dictionary)
    - [17. Unittests for the Console!](#17-unittests-for-the-console)
10. [Author](#author)

---

## Concepts

For this project, we expect you to look at these concepts:

<details>
  <summary><a href="#python-packages"><strong>Python packages</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/4N66PHVm/Python-packages.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
  <ul>
    <li>Links from screenshot
      <ul>
        <li><a href="https://docs.python.org/3.4/tutorial/modules.html#packages" title="Read: Packages">Read: Packages</a></li>
      </ul>
    </li>
  </ul>
</details>


<details>
  <summary><a href="#airBnB-clone"><strong>AirBnB clone</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/s2db8N23/Air-Bn-B-clone.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
  <ul>
    <li>Links from screenshot
      <ul>
        <li><a href="https://www.airbnb.com/" title="AirBnB website">AirBnB website</a></li>
        <li><a href="https://docs.python.org/3.4/library/unittest.html#module-unittest" title="Unittest">Unittest</a></li>
        <li><a href="https://strftime.org/" title="How to make it readable: strftime">How to make it readable: strftime</a></li>
      </ul>
    </li>
  </ul>
</details>

---

![HBNB image](https://i.postimg.cc/v8P4V0WZ/hbnb-image.png)

## Background Context

### Welcome to the AirBnB clone project!

Before starting, please read the **AirBnB** concept page.

**First step: Write a command interpreter to manage your AirBnB objects.**
This is the first step towards building your first full web application: the **AirBnB clone**. This first step is very important because you will use what you build during this project with all other following projects: HTML/CSS templating, database storage, API, front-end integration…

Each task is linked and will help you to:

* put in place a parent class (called `BaseModel`) to take care of the initialization, serialization and deserialization of your future instances
* create a simple flow of serialization/deserialization: Instance <-> Dictionary <-> JSON string <-> file
* create all classes used for AirBnB (`User`, `State`, `City`, `Place`…) that inherit from `BaseModel`
* create the first abstracted storage engine of the project: File storage.
* create all unittests to validate all our classes and storage engine

### What’s a command interpreter?

Do you remember the Shell? It’s exactly the same but limited to a specific use-case. In our case, we want to be able to manage the objects of our project:

* Create a new object (ex: a new User or a new Place)
* Retrieve an object from a file, a database etc…
* Do operations on objects (count, compute stats, etc…)
* Update attributes of an object
* Destroy an object

## Resources

**Read or watch:**

* [cmd module](https://docs.python.org/3.8/library/cmd.html)
* [cmd module in depth](http://pymotw.com/2/cmd/)
* **packages** concept page
* [uuid module](https://docs.python.org/3.8/library/uuid.html)
* [datetime](https://docs.python.org/3.8/library/datetime.html)
* [unittest module](https://docs.python.org/3.8/library/unittest.html#module-unittest)
* [args/kwargs](https://yasoob.me/2013/08/04/args-and-kwargs-in-python-explained/)
* [Python test cheatsheet](https://www.pythonsheets.com/notes/python-tests.html)
* [cmd module wiki page](https://wiki.python.org/moin/CmdModule)
* [python unittest](https://realpython.com/python-testing/)

## Learning Objectives
At the end of this project, you are expected to be able to [explain to anyone](https://fs.blog/feynman-learning-technique/), **without the help of Google**:

### General

* How to create a Python package
* How to create a command interpreter in Python using the `cmd` module
* What is Unit testing and how to implement it in a large project
* How to serialize and deserialize a Class
* How to write and read a JSON file
* How to manage `datetime`
* What is an `UUID`
* What is `*args` and how to use it
* What is `**kwargs` and how to use it
* How to handle named arguments in a function

## Requirements

### Python Scripts

* Allowed editors: `vi`, `vim`, `emacs`
* All your files will be interpreted/compiled on Ubuntu 20.04 LTS using python3 (version 3.8.5)
* All your files should end with a new line
* The first line of all your files should be exactly `#!/usr/bin/python3`
* A `README.md` file, at the root of the folder of the project, is mandatory
* Your code should use the pycodestyle (version `2.8.*`)
* All your files must be executable
* The length of your files will be tested using `wc`
* All your modules should have a documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
* All your classes should have a documentation (`python3 -c 'print(__import__("my_module").MyClass.__doc__)'`)
* All your functions (inside and outside a class) should have a documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'` and `python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'`)
* A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class or method (the length of it will be verified)

### Python Unit Tests

* Allowed editors: `vi`, `vim`, `emacs`
* All your files should end with a new line
* All your test files should be inside a folder `tests`
* You have to use the [unittest module](https://docs.python.org/3.4/library/unittest.html#module-unittest)
* All your test files should be python files (extension: `.py`)
* All your test files and folders should start by `test_`
* Your file organization in the tests folder should be the same as your project
* e.g., `For models/base_model.py`, unit tests must be in: `tests/test_models/test_base_model.py`
* e.g., For `models/user.py`, unit tests must be in: `tests/test_models/test_user.py`
* All your tests should be executed by using this command: `python3 -m unittest discover tests`
* You can also test file by file by using this command: `python3 -m unittest tests/test_models/test_base_model.py`
* All your modules should have a documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
* All your classes should have a documentation (`python3 -c 'print(__import__("my_module").MyClass.__doc__)'`)
* All your functions (inside and outside a class) should have a documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'` and `python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'`)
* We strongly encourage you to work together on test cases, so that you don’t miss any edge case

### GitHub

**There should be one project repository per group. If you clone/fork/whatever a project repository with the same name before the second deadline, you risk a 0% score.**

## More Info

### Execution

Your shell should work like this in interactive mode:

```
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) 
(hbnb) 
(hbnb) quit
$
```

But also in non-interactive mode: (like the Shell project in C)

```
$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
```

All tests should also pass in non-interactive mode: `$ echo "python3 -m unittest discover tests" | bash`

---

<center><h3>Repository Contents by Project Task</h3> </center>

![Project image](https://s3.amazonaws.com/intranet-projects-files/concepts/74/hbnb_step2.png)
![Sonny and Mariel high fiving.](https://content.codecademy.com/courses/learn-cpp/community-challenge/highfive.gif)


## Outlined Project Tasks

<details>
<summary><a href="./Readme.md"><strong>README</strong></a>, <a href="https://github.com/justinmajetich/AirBnB_clone/blob/dev/AUTHORS"><strong>AUTHORS</strong></a></summary>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/4dvrmsNF/0-README-AUTHORS.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
  <ul>
    <li>Links from screenshot
      <ul>
        <li><a href="https://github.com/moby/moby/blob/master/AUTHORS" title="Docker’s AUTHORS page">Docker’s AUTHORS page</a></li>
      </ul>
    </li>
  </ul>
</details>


<details>
  <summary><a href="#1-Be-pycodestyle-compliant"><strong>1. Be pycodestyle compliant!</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/fWcHXMQM/1-Be-pycodestyle-compliant.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
</details>


<details>
  <summary><a href="#2-Unittests"><strong>2. Unittests</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/mD4WB8G4/2-Unittests.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
</details>


<details>
  <summary><a href="#3-Base-Model"><strong>3. BaseModel</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/L5RyJby9/3-Base-Model.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
</details>


<details>
  <summary><a href="#4-Create-Base-Model-from-dictionary"><strong>4. Create BaseModel from dictionary</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/xCfdRK10/4-Create-Base-Model-from-dictionary.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
</details>


<details>
  <summary><a href="#5-Store-first-object"><strong>5. Store first object</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/3NP1mrFH/5-Store-first-object.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
</details>


<details>
  <summary><a href="#6-Console-0-0-1"><strong>6. Console 0.0.1</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/XYwWZpk4/6-Console-0-0-1.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
</details>


<details>
  <summary><a href="#7-Console-0-1"><strong>7. Console 0.1</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/DwjzfWv0/7-Console-0-1.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
</details>


<details>
  <summary><a href="#8-First-User"><strong>8. First User</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/3RwC40pq/8-First-User.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
</details>


<details>
  <summary><a href="#9-More-classes"><strong>9. More classes!</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/dVxCZ4Rc/9-More-classes.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
</details>


<details>
  <summary><a href="#10-Console-1-0"><strong>10. Console 1.0</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/L8YW10dz/10-Console-1-0.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
</details>


<details>
  <summary><a href="#11-All-instances-by-class-name"><strong>11. All instances by class name</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/fyH9DKBL/11-All-instances-by-class-name.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
</details>


<details>
  <summary><a href="#12-Count-instances"><strong>12. Count instances</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/bwrKywNN/12-Count-instances.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
</details>


<details>
  <summary><a href="#13-Show"><strong>13. Show</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/bwrKywNN/https://i.postimg.cc/CKVHvctT/13-Show.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
</details>


<details>
  <summary><a href="#14-Destroy"><strong>14. Destroy</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/MH8nwL7q/14-Destroy.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
</details>


<details>
  <summary><a href="#15-Update"><strong>15. Update</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/x1mBJFHW/15-Update.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
</details>


<details>
  <summary><a href="#16-Update-from-dictionary"><strong>16. Update from dictionary</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/tTcLV0SG/16-Update-from-dictionary.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
</details>


<details>
  <summary><a href="#17-Unittests-for-the-Console"><strong>17. Unittests for the Console!</strong></a></summary><br>
  <div align="center">
      <a href='https://postimages.org/' target='_blank'>
        <img src='https://i.postimg.cc/zfQrTRvQ/17-Unittests-for-the-Console.png' border='0' alt='image' style="max-width: 100%;">
      </a>
  </div>
  <ul>
    <li>Links from screenshot
      <ul>
        <li><a href="https://twitter.com/intent/post?text=I%20have%20successfully%20completed%20my%20AirBnB%20Console%20project%20on%20%23ALX_SE%20%40facesofalxse" title="Click here to tweet!">Click here to tweet!</a></li>
      </ul>
    </li>
  </ul>
</details>

<br>
<br>
<center> <h2>General Use</h2> </center>

1. First clone this repository.

2. Once the repository is cloned locate the "console.py" file and run it as follows:
```
/AirBnB_clone$ ./console.py
```
3. When this command is run the following prompt should appear:
```
(hbnb)
```
4. This prompt designates you are in the "HBnB" console. There are a variety of commands available within the console program.

##### Commands
    * create - Creates an instance based on given class

    * destroy - Destroys an object based on class and UUID

    * show - Shows an object based on class and UUID

    * all - Shows all objects the program has access to, or all objects of a given class

    * update - Updates existing attributes an object based on class name and UUID

    * quit - Exits the program (EOF will as well)


##### Alternative Syntax
Users are able to issue a number of console command using an alternative syntax:

	Usage: <class_name>.<command>([<id>[name_arg value_arg]|[kwargs]])
Advanced syntax is implemented for the following commands: 

    * all - Shows all objects the program has access to, or all objects of a given class

	* count - Return number of object instances by class

    * show - Shows an object based on class and UUID

	* destroy - Destroys an object based on class and UUID

    * update - Updates existing attributes an object based on class name and UUID

<br>
<br>
<center> <h2>Examples</h2> </center>
<h3>Primary Command Syntax</h3>

###### Example 0: Create an object
Usage: create <class_name>
```
(hbnb) create BaseModel
```
```
(hbnb) create BaseModel
3aa5babc-efb6-4041-bfe9-3cc9727588f8
(hbnb)                   
```
###### Example 1: Show an object
Usage: show <class_name> <_id>

```
(hbnb) show BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
[BaseModel] (3aa5babc-efb6-4041-bfe9-3cc9727588f8) {'id': '3aa5babc-efb6-4041-bfe9-3cc9727588f8', 'created_at': datetime.datetime(2020, 2, 18, 14, 21, 12, 96959), 
'updated_at': datetime.datetime(2020, 2, 18, 14, 21, 12, 96971)}
(hbnb)  
```
###### Example 2: Destroy an object
Usage: destroy <class_name> <_id>
```
(hbnb) destroy BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
(hbnb) show BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
** no instance found **
(hbnb)   
```
###### Example 3: Update an object
Usage: update <class_name> <_id>
```
(hbnb) update BaseModel b405fc64-9724-498f-b405-e4071c3d857f first_name "person"
(hbnb) show BaseModel b405fc64-9724-498f-b405-e4071c3d857f
[BaseModel] (b405fc64-9724-498f-b405-e4071c3d857f) {'id': 'b405fc64-9724-498f-b405-e4071c3d857f', 'created_at': datetime.datetime(2020, 2, 18, 14, 33, 45, 729889), 
'updated_at': datetime.datetime(2020, 2, 18, 14, 33, 45, 729907), 'first_name': 'person'}
(hbnb)
```
<h3>Alternative Syntax</h3>

###### Example 0: Show all User objects
Usage: <class_name>.all()
```
(hbnb) User.all()
["[User] (99f45908-1d17-46d1-9dd2-b7571128115b) {'updated_at': datetime.datetime(2020, 2, 19, 21, 47, 34, 92071), 'id': '99f45908-1d17-46d1-9dd2-b7571128115b', 'created_at': datetime.datetime(2020, 2, 19, 21, 47, 34, 92056)}", "[User] (98bea5de-9cb0-4d78-8a9d-c4de03521c30) {'updated_at': datetime.datetime(2020, 2, 19, 21, 47, 29, 134362), 'id': '98bea5de-9cb0-4d78-8a9d-c4de03521c30', 'created_at': datetime.datetime(2020, 2, 19, 21, 47, 29, 134343)}"]
```

###### Example 1: Destroy a User
Usage: <class_name>.destroy(<_id>)
```
(hbnb) User.destroy("99f45908-1d17-46d1-9dd2-b7571128115b")
(hbnb)
(hbnb) User.all()
(hbnb) ["[User] (98bea5de-9cb0-4d78-8a9d-c4de03521c30) {'updated_at': datetime.datetime(2020, 2, 19, 21, 47, 29, 134362), 'id': '98bea5de-9cb0-4d78-8a9d-c4de03521c30', 'created_at': datetime.datetime(2020, 2, 19, 21, 47, 29, 134343)}"]
```
###### Example 2: Update User (by attribute)
Usage: <class_name>.update(<_id>, <attribute_name>, <attribute_value>)
```
(hbnb) User.update("98bea5de-9cb0-4d78-8a9d-c4de03521c30", name "Todd the Toad")
(hbnb)
(hbnb) User.all()
(hbnb) ["[User] (98bea5de-9cb0-4d78-8a9d-c4de03521c30) {'updated_at': datetime.datetime(2020, 2, 19, 21, 47, 29, 134362), 'id': '98bea5de-9cb0-4d78-8a9d-c4de03521c30', 'name': 'Todd the Toad', 'created_at': datetime.datetime(2020, 2, 19, 21, 47, 29, 134343)}"]
```
###### Example 3: Update User (by dictionary)
Usage: <class_name>.update(<_id>, <dictionary>)
```
(hbnb) User.update("98bea5de-9cb0-4d78-8a9d-c4de03521c30", {'name': 'Fred the Frog', 'age': 9})
(hbnb)
(hbnb) User.all()
(hbnb) ["[User] (98bea5de-9cb0-4d78-8a9d-c4de03521c30) {'updated_at': datetime.datetime(2020, 2, 19, 21, 47, 29, 134362), 'name': 'Fred the Frog', 'age': 9, 'id': '98bea5de-9cb0-4d78-8a9d-c4de03521c30', 'created_at': datetime.datetime(2020, 2, 19, 21, 47, 29, 134343)}"]
```
<br>


## Contributors

For a list of contributors to this project, please refer to the [AUTHORS](https://github.com/deezyfg/AirBnB_clone/blob/master/AUTHORS) file.