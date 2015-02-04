**1. Implement an algorithm to determine if a string has all unique characters. What if you cannot use additional data structures?**
<br />
**SOLUTION**
<br />
You may want to start off with asking your interviewer if the string is an ASCII string or a Unicodestring.This is an important question, and asking it will show an eye for detail and a deep understanding of Computer Science.
We'll assume for simplicity that the character set is ASCII. If not, we would need to increase the storage size, but the rest of the logic would be the same.
Given this, one simple optimization we can make to this problem is to automatically return **false** if the length of the string is greater than the number of unique characters in the alphabet. After all, you can't have a string with 280 unique characters if there are only 256 possible unique characters.
Our first solution is to create an array of boolean values, where the flag at index **i** indicates whether character i in the alphabet is contained in the string. If you run across this character a second time, you can immediately return **false**.
The code below implements this algorithm.

```

public boolean isUniqueChars2(String str) 
{
  if (str.lengthQ > 256)
    return false;
  
  boolean[] char_set = new boolean[256]; 
  for (int1 = 0; i < str.lengthQ; i++) 
  {
    int val = str.charAt(i);
    if (char_set[val]) 
    { // Already found this char in string
      return false;
    }
    char_set[val] = true;
  }
  return true;
}
```

The time complexity for this code is <code> O(n) </code>, where `n` is the length of the string. The space complexity is <code>O(1)</code>.
We can reduce our space usage by a factor of eight by using a bit vector. We will assume, in the below code, that the string only uses the lowercase letters <code>a</code> through `z`. This will allow us to use just `a` single `int`.
```
public boolean isUniqueChars(String str) 
{
  int checker = 0;
  for (int 1=0; i < str.length(); i++) 
  {
    int val = str.charAt(i) - 'a';
    if((checker & ( 1 « val)) > 0)
    { 
      return false;
    }
    checker |= (1 « val);
  }
  return true;
}
```
Alternatively, we could do the following:

1. Compare every character of the string to every other character of the string. This will take `O(n2)` time and `O(1)` space.
2. If we are allowed to modify the input string, we could sort the string in `O(n log(n))` time and then linearly check the string for neighboring characters that are identical. Careful, though: many sorting algorithms take up extra space.
These solutions are not as optimal in some respects, but might be better depending on the constraints of the problem.
