#Palindrome 2

Determine if a given string is a palindrome. A palindrome is a string that is the same forwards as backwards, ignoring letter case, punctuation marks and word dividers. For example, “racecar” and “Amor, Roma” are palindromes, “abcd” is not.

We limit the punctuation marks to ignore by the period, comma, question mark, exclamation point, apostrophe, colon, semicolon and hyphen.

**Input**

String

**Output**

Return True if the string is a palindrome, return False otherwise.

**Sample Input:**

'civic'

**Sample Output:**

True

***

# Solution (C++)

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */
    std::string input;
    while (std::cin) {
        getline(std::cin, input);
    }
    locale loc;
    std::string::iterator it = input.begin();
    std::string::reverse_iterator rit = input.rbegin();
    for (; it != input.end() && rit != input.rend(); ++it, ++rit) {
        if (tolower(*it, loc) != tolower(*rit, loc)) {
            std::cout << "False" << std::endl;
            return 0;
        }
    }
    std::cout << "True" << std::endl;
    return 0;
}
```
