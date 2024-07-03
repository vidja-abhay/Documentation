# Session Storage

The **sessionStorage** object let you store **key/value** pairs in the browser.

It stores data only for session. It means that the data stored in sessionStorage will be deleted when the browser is closed.

Session Storage is pretty much **same as local storage**.

The **only difference** is that it has an **expiration date**.

## Methods used in sessionStorage

- **setItem()** : This method is used to store the data in form of key-value pairs.

```bash
sessionStorage.setItem("name" , uName);
```

- **getItem()** : This method is used to fetch the data using key.

```bash
sessionStorage.getItem('name');
```

- **removeItem()** : This method is used to delete a key-value air from sessionStorage.

```bash
sessionStorage.removeItem('name');
```

- **clear()** : This method is used to clear the entire sessionStorage.

```bash
sessionStorage.clear();
```

- **length** : This method is used to get the total number of items stored in sessionStorage.

```bash
sessionStorage.length;
```

