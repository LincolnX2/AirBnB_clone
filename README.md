# AirBnB_clone
The AirBnB clone utilizes higher level programming skills to deploy a copy of the AirBnB website.

## Web Static
The web static starts building the front end of the AirBnB clone website through simple HTML static pages and style guides.

## Console
The console is a command interpreter that manages all AirBnB objects.

### Using the Console

#### Interactive Mode
##### Starting on Interactive Mode
Run `./console.py`to begin a session.

A prompt `(hbnb)` should appear where you can type commands followed by a new line.
After the command is run, you will be reprompted.
Empty lines also reprompt the user.
Type `help` to get a list of available commands.
Type `quit` to end the session.
```
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb)
(hbnb)
(hbnb) quit
```

#### Non-Interactive Mode
You can also use the console non-interactively.
##### Starting by using "echo"
You can "pipe" an input into the command by using `echo`, as seen below:
```
$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
```
##### Starting with a file of commands
You can also pipe in a file with one command per line, as seen below:
```
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
```
### Console Commands
Typing `help <command>` or `?<command>` will print information on how to utilize each command.

Below is a brief description of each command:
|                    command                    |                                                description                                                |
|:---------------------------------------------:|:---------------------------------------------------------------------------------------------------------:|
|                `all` or `all <class>`             | Prints all existing objects.  If class_name is specified, prints all existing objects of that class |
|              `create <class>`              |                                    Creates a new instance of class_name                                   |
|         `show <class> <id>`         |                            Prints the string representation of the instance by class_name with ID object_id                            |
| `update <class> <id> <attr_name> <attr_val>` |          Update the attribute attr_name with value attr_val for instance of class_name with ID id         |
|            `destroy <cls_name> <id>`            |                                   Delete instance of cls_name with ID id                                  |
|                      `quit`                     |                                              Exit the console                                             |
|                      `EOF`                      |                                              Exit the console                                             |

Some commands can also be run by calling on the class directly:
|                    command                    |                                                description                                                |
|:---------------------------------------------:|:---------------------------------------------------------------------------------------------------------:|
|                `<class>.all()`             | Prints all existing objects of that class name |
|              `<class>.count()`              |                                    Counts all existing objects of that class                                   |
|         `<class>.show("<id>")`         |       Prints the string representation of the instance by class_name with ID object_id                            |
| `<class>.update("<id>", "<attr_name>", "<attr_val>")` |          Update the attribute attr_name with value attr_val for instance of class_name with ID id         |
|            `<class>.update("<id>", {'<attr_name1>': '<attr_val1>', '<attr_name2>': '<attr_val2>'})`            |                                   Updates multiple attributes with key/value pairs for instance of class_name with ID id using dictionary representation         |
|            `<cls_name>.destroy("<id>")`            |                                   Delete instance of cls_name with ID id                                  |

### Available Classes
The console works with the following classes to manage AirBnB objects:
```
User
Review
City
Place
State
Amenity
```
All objects are accessed via storage, an instance of the FileStorage Class, for the above commands to be run.
FileStorage Class manages the dictionary of all objects as well as serialization/deserialization of objects to JSON file.


