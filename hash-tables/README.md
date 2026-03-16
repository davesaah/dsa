# Hash Tables

- Unlike an array that uses numeric index to find data, a hash table lets you
use other values as a key. Under the hood, it converts the key into a numeric
index using a hash function, then stores the value in an array at that index.
- The 3 steps a hash table does:
    - Take your key.
    - Run it through a hash function -> produces a number.
    - Store or retrieve the value at index in the underlying array.
- There can be collisions from the result of a hash function. This happens when
different keys result to the same numeric value. A good hash function has fewer
collisions.
- The most common fix for a collision is chaining. This is when each value is a
linked list of all the entries that have the same numeric value from different
keys.
- Insertion/lookup is O(1) on average and O(n) if all keys collide.

> Hash tables are built on top of arrays and collisions are handled with linked
lists.


## Real world example

- A dictionary in Python: keys can be any string, lookup is instant.
- A database index: find a row by username without scanning the whole table.
- Your computer's DNS cache: domain names mapped to IP addresses.

## Questions to test understanding

### Question 1: Conceptual

You look up the key "alice" in a hash table with 1 million entries. How many 
steps does it take? What about in the worst case, and what causes that worst 
case?

### Question 2: Real world

You're building a spell checker. It needs to verify whether a word exists in a 
dictionary of 200,000 words as fast as possible. Which of the three data 
structures would you choose, and why? Options = array, linked list, hash table.

### Question 3: Connecting the dots

We said hash tables are built on top of arrays, and that collision chaining uses
linked lists. Can you describe in your own words why an array is used as the 
base structure, but a linked list is used for the chains and not the other way 
around?
