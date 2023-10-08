# AirBnB Clone - The Console

The AirBnB Clone Console is the initial segment of the AirBnB project at Holberton School, designed to explore fundamental concepts of higher-level programming. The project's ultimate goal is to deploy a simplified replica of the AirBnB website (HBnB). In this segment, a command interpreter is created to manage objects for the AirBnB (HBnB) website.

## Functionalities of the Command Interpreter:
- Create a new object (e.g., a new User or a new Place).
- Retrieve an object from a file, a database, etc.
- Perform operations on objects (count, compute stats, etc.).
- Update attributes of an object.
- Destroy an object.

## Table of Contents
* [Environment](#environment)
* [Installation](#installation)
* [File Descriptions](#file-descriptions)
* [Usage](#usage)
* [Examples of Use](#examples-of-use)
* [Bugs](#bugs)
* [Authors](#authors)
* [License](#license)

## Environment
This project is interpreted and tested on Ubuntu 14.04 LTS using Python 3 (version 3.4.3).

## Installation
To get started with the AirBnB Clone Console, follow these steps:
1. Clone this repository: `git clone "https://github.com/alexaorrico/AirBnB_clone.git"`
2. Access the AirBnB directory: `cd AirBnB_clone`
3. Run the console interactively: `./console` and enter commands.
4. Run the console non-interactively: `echo "<command>" | ./console.py`

## File Descriptions
- [console.py](console.py): The console serves as the entry point for the command interpreter and supports the following commands:
  - `EOF`: Exits the console.
  - `quit`: Exits the console.
  - `<emptyline>`: Overwrites the default empty line method and does nothing.
  - `create`: Creates a new instance of `BaseModel`, saves it (to the JSON file), and prints the ID.
  - `destroy`: Deletes an instance based on the class name and ID (saves the change into the JSON file).
  - `show`: Prints the string representation of an instance based on the class name and ID.
  - `all`: Prints all string representations of all instances based on the class name.
  - `update`: Updates an instance based on the class name and ID by adding or updating attributes (saves the change into the JSON file).

- `models/` directory contains classes used for this project:
  - [base_model.py](/models/base_model.py): The BaseModel class serves as the foundation for future classes and includes essential methods like initialization, string representation, save, and to_dict.

Classes inherited from Base Model:
- [amenity.py](/models/amenity.py)
- [city.py](/models/city.py)
- [place.py](/models/place.py)
- [review.py](/models/review.py)
- [state.py](/models/state.py)
- [user.py](/models/user.py)

- `/models/engine` directory contains the File Storage class responsible for handling JSON serialization and deserialization:
  - [file_storage.py](/models/engine/file_storage.py): This class provides methods to work with serialized objects, including `all`, `new`, `save`, and `reload`.

- `/tests` directory contains unit test cases for this project, including:
  - [/test_models/test_base_model.py](/tests/test_models/test_base_model.py): Contains the TestBaseModel and TestBaseModelDocs classes.
  - [/test_models/test_amenity.py](/tests/test_models/test_amenity.py): Contains the TestAmenityDocs class.
  - [/test_models/test_city.py](/tests/test_models/test_city.py): Contains the TestCityDocs class.
  - [/test_models/test_file_storage.py](/tests/test_models/test_file_storage.py): Contains the TestFileStorageDocs class.
  - [/test_models/test_place.py](/tests/test_models/test_place.py): Contains the TestPlaceDoc class.
  - [/test_models/test_review.py](/tests/test_models/test_review.py): Contains the TestReviewDocs class.
  - [/test_models/test_state.py](/tests/test_models/test_state.py): Contains the TestStateDocs class.
  - [/test_models/test_user.py](/tests/test_models/test_user.py): Contains the TestUserDocs class.

## Examples of Use
```bash
vagrantAirBnB_clone$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  all  create  destroy  help  quit  show  update

(hbnb) all MyModel
** class doesn't exist **
(hbnb) create BaseModel
7da56403-cc45-4f1c-ad32-bfafeb2bb050
(hbnb) all BaseModel
[[BaseModel] (7da56403-cc45-4f1c-ad32-bfafeb2bb050) {'updated_at': datetime.datetime(2017, 9, 28, 9, 50, 46, 772167), 'id': '7da56403-cc45-4f1c-ad32-bfafeb2bb050', 'created_at': datetime.datetime(2017, 9, 28, 9, 50, 46, 772123)}]
(hbnb) show BaseModel 7da56403-cc45-4f1c-ad32-bfafeb2bb050
[BaseModel] (7da56403-cc45-4f1c-ad32-bfafeb2bb050) {'updated_at': datetime.datetime(2017, 9, 28, 9, 50, 46, 772167), 'id': '7da56403-cc45-4f1c-ad32-bfafeb2bb050', 'created_at': datetime.datetime(2017, 9, 28, 9, 50, 46, 772123)}
(hbnb) destroy BaseModel 7da56403-cc45-4f1c-ad32-bfafeb2bb050
(hbnb) show BaseModel 7da56403-cc45-4f1c-ad32-bfafeb2bb050
** no instance found **
(hbnb) quit
```

## Bugs
No known bugs at this time.

## Authors
Samuel Chigozie - [GitHub](https://github.com/samuelchigozie) 
Ifeoluwa Seriki - [GitHub](https://github.com/alicecodes1)

## License
Public Domain. No copyright protection.
