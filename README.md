# Hash Table

> This project was built as part of the "Data Structures" certification on freeCodeCamp.

A simple hash table implementation in Python, using a sum-of-character-codes
hash function and chaining (nested dictionaries) to handle collisions.

## Description

The `HashTable` class stores key/value pairs inside `self.collection`, a
dictionary keyed by hash value. Each hash value maps to its own small
dictionary of `{key: value}` pairs, so multiple keys that hash to the same
value can coexist without overwriting each other (collision handling via
chaining).

### Methods

- `hash(string_key)` : computes a hash by summing the Unicode code point
  (`ord`) of every character in the key.
- `add(key, value)` : stores `value` under `key`, creating a new bucket at
  that hash value if needed.
- `remove(key)` : deletes `key` (and its value) from its bucket, if present.
- `lookup(key)` : returns the value stored under `key`, or `None` if the key
  isn't found.

## Usage

```python
from hashtable import HashTable

ht = HashTable()
ht.add("name", "Alice")
ht.add("age", 30)

print(ht.lookup("name"))  # Alice
ht.remove("age")
print(ht.lookup("age"))   # None
```
