Python - Almost a circle

In this assignment, I demonstrated proficiency in Python object-oriented programming by creating three interrelated classes to depict rectangles and squares. I developed a custom test suite using the unittest module to thoroughly assess the functionality of each class.

The three classes incorporated a variety of Python tools, including:

Import statements Exception handling Private attributes Getter and setter methods Class and static methods Inheritance File input/output operations Handling of args and kwargs Serialization and deserialization using JSON and CSV formats Implementation of unittests

base Class:

The "Base" class serves as the foundation for all other classes in the project. It incorporates the following features:

Private class attribute __nb_objects initialized to 0. Public instance attribute id. Class constructor def init(self, id=None): If id is None, increments __nb_objects and assigns its value to the public instance attribute id. If id is provided, sets the public instance attribute id to the provided id. Static method def to_json_string(list_dictionaries): returns the JSON string serialization of a list of dictionaries. Returns "[]" if the list is None or empty. Class method def save_to_file(cls, list_objs): writes the JSON serialization of a list of objects to a file named .json. If list_objs is None, saves an empty list. Static method def from_json_string(json_string): returns a list of objects deserialized from a JSON string. Returns an empty list if json_string is None or empty. Class method def create(cls, **dictionary): instantiates an object with provided attributes from the given dictionary. Class method def load_from_file(cls): returns a list of objects instantiated from a JSON file named .json. Returns an empty list if the file does not exist. Class method def save_to_file_csv(cls, list_objs): writes the CSV serialization of a list of objects to a file named .csv. If list_objs is None, saves an empty list. Serializes objects in the specified format. Class method def load_from_file_csv(cls): returns a list of objects instantiated from a CSV file named .csv. Returns an empty list if the file does not exist. Static method def draw(list_rectangles, list_squares): draws Rectangle and Square instances in a GUI window using the turtle module. Parameters are lists of Rectangle and Square objects, respectively.

Rectangle Class:

The Rectangle class inherits from the Base class and includes the following features:

Private instance attributes __width, __height, __x, and __y, each with its own getter/setter. Class constructor def init(self, width, height, x=0, y=0, id=None): performs attribute validation and assignment. Public method def area(self): returns the area of the Rectangle instance. Public method def display(self): prints the Rectangle instance to stdout using the # character, respecting coordinates. Overwritten str method to print a Rectangle instance in the format [Rectangle] () /. Public method def update(self, *args, **kwargs): updates a Rectangle instance with the given attributes from *args or **kwargs. Public method def to_dictionary(self): returns the dictionary representation of a Rectangle instance.

Square Class:

The Square class inherits from the Rectangle class and includes the following features:

Class constructor def init(self, size, x=0, y=0, id=None): assigns the size value to both width and height. Overwritten str method to print a Square instance in the format [Square] () /. Public method def update(self, *args, **kwargs): updates a Square instance with the given attributes from *args or **kwargs. Public method def to_dictionary(self): returns the dictionary representation of a Square instance
