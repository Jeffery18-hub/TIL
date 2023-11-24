# Set
1. Set data structure is used to represent collections of related items with no particular ordering. A programmer might use a set to store a users followers on a social media website. 

2. Set is mutable and you can use add, discard and remove function to add or delete some items

3. init set:
```python
nums1 = set() # empty
nums2 = set([1,2,3]) # parameter must be an iterable object like list
nums3= {1,2,3}
```

4. We cannot change the size of a set (wether adding or discarding elements) while within a for loop iterating through it.  

```python
my_set = {1, 2, 3, 4, 5}

for item in my_set:
    if item % 2 == 0:
        my_set.remove(item) # not ok here
```
RuntimeError: Set changed size during iteration
    for item in my_set

# List
1. The List data structure is used to store sequences of values. This is useful when multiple items need to be grouped together, and the ordering of the items needs to be maintained. 