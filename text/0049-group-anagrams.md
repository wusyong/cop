- Start Date: 2021-01-20
- URL: [Group Anagrams](https://leetcode.com/problems/group-anagrams/)

# HashMap way

HashMap (HashTable) is a very efficient way to store key/value pairs. Since this problem is trying to group several
elements together. This data structure is perfect candidate. The key would be the condition we could group them and the
value would be a vector to append each element. What makes it even better is finding index in HashMap takes O(1), it
would be extremely efficient to run through to whole process. The final point is determining what key should be.

We want to group element that have the same amount of character variation. The easiest way could be sorting them, so
they can all become the same if the variation condition meets. This is the type of key we are looking for and almost all
languages support sorting strings. We then append each element to the hashMap with corresponding key.

After we build the HashMap, we just need to iterate it and collect the vector we want and return it.

