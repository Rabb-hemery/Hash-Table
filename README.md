# Hash-Table
The HashTable class stores key/value pairs inside self.collection, a dictionary keyed by hash value. Each hash value maps to its own small dictionary of {key: value} pairs, so multiple keys that hash to the same value can coexist without overwriting each other (collision handling via chaining).
