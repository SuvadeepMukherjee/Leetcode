# Arrays and Strings 

- Python primarily uses lists instead of arrays
- Technically an array cant be resized , A dynamic array or list can be (In the context of algorithmic problems usually when people talk about arrays they are referring to dynamic arrays)
- Strings are immutable in Python 
  - Mutable ➡️ A type of data that can be changed
  - Immutable ➡️ A type of data that cannot be changed (If we want to change something immutable we will need to recreate the entire thing)
- Why should we care about something being mutable or immutable ?
  - Imagine you have a mutable array `arr = ["a", "b", "c"]` and an immutable string `s = "abc"`, and you want to change the `c` into a `d`. You can easily do `arr[2] = "d"`, but you cannot do `s[2] = "d"`. As such, if you wanted the string `s = "abd"`, you would need to create it entirely from scratch. With such a small  string, it's not a big deal. But sometimes you are dealing with strings  with 100,000 characters, so creating new versions just to modify one  character is very expensive (O(n), where n is the size of the string)

- Time and Space Complexity of array and string operations ![time-and-space-complexity](../../assets/time-and-space-complexity.png)