# Local Storage

**HTML5** specification introduce the **localStorage** as way to store data with no expiration date in the web browser.

- In another words, the **the data stored in browser** will persist even after you close the browser windows.

- The localStorage is unique per "protocol://host:port".

- If you wish to store objects, lists or array you must convert them into a string using **JSON.sringify()**.

## Accessing localStorage

You can access the **localStorage** via the property of the **window object**.

```bash
window.localStorage
```

## Local Storage's Methods

**1. setItem(key,value)** : 

- This method used to store a key-value pair in the localStorage.
- As mentioned before, we must stringfy object before we store them in localStorage.

```bash
const Student = {
    name : "Abhay Vidja",
    branch : "Computer"
};

localStorage.setItem('student', JSON.sringify(Student));
```

**2. getItem(key)** :

- This method is used to access or retrive data from localStorage. A key is used as parameter.

- You should convert it to an object using **JSON.parse()**.

```bash
const student = localStorage.getItem('student');
// '{ name : "Abhay Vidja", branch : "Computer" }'

const pStudent = JSON.parse(localStorage.getItem('student'));
// { name : "Abhay Vidja", branch : "Computer" }
```

**3. removeItem(key)** :

This method is used to delete an item from localStorage. A key is used as parameter.

```bash
localStorage.removeItem('student');
```

**4. key(index)** :

This method retrives a value from a specific location.

```bash
let answer = localStorage.key(2);
// this statement will retrive the value of the third item from the localStorage.
```

**5. clear()** :

This method is used clear all values stored in localStorage.

```bash
localStorage.clear();
```

**6. length** :

This property used to get the number of name-value pairs from localStorage.

```bash
console.log(localStorage.length);
