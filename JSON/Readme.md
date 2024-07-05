# JSON (JavaScript Object Notation)

## Table of Contents
1. [What is JSON?](##what-is-json)
2. [JSON Data](##json-data)
3. [JSON Object](##json-object)
4. [How to Create a JSON File](##how-to-create-a-json-file)
5. [How to Access JSON Data](##how-to-access-json-data)
6. [JSON to Object](##json-to-object)
7. [Object to JSON](##object-to-json)
8. [Advantages and Disadvantages of JSON](##advantages-and-disadvantages-of-json)

## What is JSON?

JSON (JavaScript Object Notation) is a lightweight, text-based, language-independent data interchange format. It's easy for humans to read and write and easy for machines to parse and generate. JSON is derived from the JavaScript programming language but is supported by many programming languages.

## JSON Data

JSON data is represented in two structures:

1. A collection of name/value pairs (realized as an object, record, struct, dictionary, hash table, keyed list, or associative array in various languages)
2. An ordered list of values (realized as an array, vector, list, or sequence in various languages)

JSON supports the following data types:
- String
- Number
- Boolean
- Array
- Object
- null

## JSON Object

A JSON object is enclosed in curly braces `{}` and contains key-value pairs. The keys must be strings, and values can be valid JSON data types.

Example:
```bash
{
  "name": "Abhay Vidja",
  "age": 20,
  "city": "Ahmedabad"
}
```

## How to Create a JSON File

- Open a text editor (e.g., Notepad, VS Code)

- Write valid JSON data

- Save the file with a .json extension

- Example (data.json) :

```bash
{
  "employees": [
    {
      "name": "Abhay",
      "position": "Developer",
      "age": 20
    },
    {
      "name": "Shyam",
      "position": "Designer",
      "age": 19
    }
  ]
}
```

## How to Access JSON Data

Accessing JSON data depends on the programming language you're using. Here's an example in JavaScript:

```bash
// Assuming we have a JSON string
const jsonString = '{"name": "Abhay", "age": 20}';

// Parse JSON string to JavaScript object
const data = JSON.parse(jsonString);

// Access data
console.log(data.name); // Output: Abhay
console.log(data.age);  // Output: 20
```

## JSON to Object

To convert a JSON string to an object:

```bash
const jsonString = '{"name": "Abhay", "age": 20}';

const data = JSON.parse(jsonString);
```

## Object to JSON

To convert an object to a JSON string:

```bash
const obj = {"name": "Abhay", "age": 20};

const data = JSON.stringify(obj);
```

## Advantages and Disadvantages of JSON

**Advantages** :

- Lightweight and easy to read/write

- Language independent

- Easy to parse and generate

- Supports nested structures

- Can be easily transmitted over networks

**Disadvantages** :

- No support for functions or complex data types

- No built-in date data type

- No comments allowed

- Can be less efficient for large datasets compared to binary formats

- Limited data validation capabilities


