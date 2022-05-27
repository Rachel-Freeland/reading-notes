# Reading 30 --> Hash Tables

## Reading
* [Intro into Hash Tables](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)
* [Basics of Hash Tables](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)
<hr/>

* Hash tables are a data structure that use Key:Value pairs.
* Every `node` or `bucket` has a key AND a value.
* Hash tables have an O(1) time complexity when it comes to looking up a value.
* The hash function takes a key and returns an integer.
* A hash map uses a `hash function` to place each item at a precise location based on its key.
* The hash code is calculated in constant time and writing to an array at one index is O(1).
* The same key should always produce the same hash code... there should be NO randomness
* Hash tables are traditionally created from arrays.
* A **collision** happens when more than one key hashes to the same index in an array.
* To store values, hash maps:
  * accept a key
  * calculate the hash of the key
  * use modulus to convert the hash into an array index
  * store the key with the value py appending both to the end of a linked list
* To read a value, hash maps:
  * accept a key
  * calculate the hash of the key
  * use modulus to convert the hash into an array index
  * use the index to access the short linked list representing a bucket
  * search through the bucket looking for a node with a key:value pair that matches the key you were given

* Internal Methods for hash maps:
  * `add()` --> when adding a new key:value pair to a hashtable:
    * sends the key to the GetHash method
    * once the index is calculated, goes to that index
    * if something exists at that index already, if not... adds the key:value pair
    * if something does exist at that index then, it adds the new key:value pair to the data structure within that bucket
  * `find()` --> takes in a key, gets the hash, and goes to the index location specified. Once there, it is the 
     responsibility of the algorithm to iterate through the bucket and see if the key exists.
  * `contains()` --> will accept a key and return a bool if that key exists within the hashtable.
  * `getHash()` --> will accept a key as a string, conduct the hash, and return the index of the array where the 
     key:value should be placed.
  * 


## Watch
* [What is a hash table?](https://www.youtube.com/watch?v=MfhjkfocRR0)

### Bookmark & Skim
* [Hash Table wiki](https://en.wikipedia.org/wiki/Hash_table)