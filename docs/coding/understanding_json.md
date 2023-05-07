# Understanding JSON

JSON (JavaScript Object Notation) is a lightweight data interchange format that is easy for humans to read and write, and easy for machines to parse and generate. It is language-agnostic and is commonly used for data exchange between a client and a server, as well as for configuration files and data storage.

JSON has a simple structure, consisting of two primary data structures:

1. Objects: An object is an unordered collection of key-value pairs, enclosed within curly braces `{}`. The keys are strings and must be unique within an object. The values can be strings, numbers, booleans, objects, arrays, or `null`.

Example of a JSON object:

```json
{
  "firstName": "John",
  "lastName": "Doe",
  "age": 30,
  "isStudent": false
}
```

2. Arrays: An array is an ordered collection of values, enclosed within square brackets `[]`. The values in an array can be of any data type, including strings, numbers, booleans, objects, arrays, or `null`.

Example of a JSON array:

```json
[
  {
    "firstName": "John",
    "lastName": "Doe",
    "age": 30,
    "isStudent": false
  },
  {
    "firstName": "Jane",
    "lastName": "Doe",
    "age": 28,
    "isStudent": true
  }
]
```

In your work with APIs and ML, JSON is likely used to transmit data between your Python code and various services or endpoints. Since you work in Python, you can easily convert JSON data to Python objects (like dictionaries and lists) using the built-in `json` library:

```python
import json

# Convert JSON string to Python object
json_string = '{"firstName": "John", "lastName": "Doe", "age": 30, "isStudent": false}'
python_dict = json.loads(json_string)

# Convert Python object to JSON string
json_string_back = json.dumps(python_dict)
```

### Tl;Dr JSON is good for people and machines

JSON provides a simple, human-readable, and easily parseable format for data exchange, which is why it's so widely used in modern applications.

## JSON vs Python dictionaries

A JSON object and a Python dictionary may seem similar, but they are fundamentally different. A JSON object is a string that represents data using the JSON format, while a Python dictionary is a native data structure in Python that stores key-value pairs.

The key difference lies in the fact that JSON is a data interchange format (a way to represent data as text), while a Python dictionary is an actual data structure that exists in memory.

When you want to print a JSON object, you are essentially trying to print a string that is formatted as JSON. However, if you have a Python dictionary and want to print it, you can directly print the dictionary object without needing any conversion.

Here's a simple example to illustrate the difference:

Python dictionary:
```python
person = {
  "firstName": "John",
  "lastName": "Doe",
  "age": 30,
  "isStudent": False
}

print(person)
```

JSON object (as a string):
```python
json_string = '{"firstName": "John", "lastName": "Doe", "age": 30, "isStudent": false}'

print(json_string)
```

To convert between JSON objects (strings) and Python dictionaries, you need to use the `json` library. The reason you need to convert them is that they are different data types - one is a string, and the other is a native Python data structure. The `json` library provides methods like `json.loads()` and `json.dumps()` to perform these conversions.

For example, if you have a JSON object (string) and want to manipulate it as a Python dictionary, you can use `json.loads()`:

```python
import json

json_string = '{"firstName": "John", "lastName": "Doe", "age": 30, "isStudent": false}'
python_dict = json.loads(json_string)

# Now you can manipulate the data as a Python dictionary
python_dict["age"] = 31

# Convert the dictionary back to a JSON string
json_string_back = json.dumps(python_dict)
print(json_string_back)
```

### Tl;Dr JSON is a string

A JSON object is a string representing data in the JSON format, while a Python dictionary is a native data structure for storing key-value pairs. To work with JSON data in Python, you need to convert between JSON objects and Python dictionaries using the `json` library.

## Converting JSON to Python

You can load JSON into a Python data structure, or you can dump a Python data structure into JSON.

The primary difference between `json.loads()` and `json.load()` is the type of input they expect for parsing JSON data:

1. `json.loads()`: This function parses a JSON-formatted string and returns a Python object (dictionary or list, depending on the input JSON structure). The "s" in "loads" stands for "string". It takes a JSON string as its argument:

```python
import json

json_string = '{"firstName": "John", "lastName": "Doe", "age": 30, "isStudent": false}'
python_dict = json.loads(json_string)
```

2. `json.load()`: This function reads a JSON-formatted file and returns a Python object (dictionary or list, depending on the input JSON structure). It takes a file-like object with a `.read()` method, such as a file opened with the built-in `open()` function:

```python
import json

with open("file.json", "r") as file:
    python_dict = json.load(file)
```

Similarly, there are two functions for converting Python objects to JSON:

1. `json.dumps()`: This function takes a Python object and returns a JSON-formatted string. The "s" in "dumps" stands for "string":

```python
import json

python_dict = {"firstName": "John", "lastName": "Doe", "age": 30, "isStudent": False}
json_string = json.dumps(python_dict)
```

2. `json.dump()`: This function takes a Python object and writes it to a JSON-formatted file. It takes a file-like object with a `.write()` method, such as a file opened with the built-in `open()` function:

```python
import json

python_dict = {"firstName": "John", "lastName": "Doe", "age": 30, "isStudent": False}

with open("file.json", "w") as file:
    json.dump(python_dict, file)
```

### Tl;Dr The S stands for string, no S is for files
`json.loads()` and `json.dumps()` work with JSON-formatted strings, while `json.load()` and `json.dump()` work with JSON-formatted files.
