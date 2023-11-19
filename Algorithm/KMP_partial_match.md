KMP is a string search algorithm.

1. Partial matching table (an import term in this algo)is an array of integers.

2. prefix and sufix of a string:
- eg. abcdab
- prefix: ab, abc, abcd, abcda (you can see that prefix is a substring of the string including the first character and not including
the last one)
- sufix: bcdab, cdab, dab, ab (you can see that sufix is a substring of the string including the last character and not including the first one)
- longest common substring: ab
- so the partial matching table is:
[0, 0, 0, 0, 1, 2]

3. The essence of partial match: 
sometimes the head part and the tail part of a string is the same, so we can move the head part to the tail part to reduce the number of comparisons.



