```
lst1 = [1,2,3]
lst2 = [4,5,6]

# parameter should be iterable objects
zipped = zip(lst1, lst2)

print(type(zipped))

'''
there's an important aspect to consider: once a zip object is iterated over, 
it becomes exhausted. This means that if you've already iterated over zipped before this loop (for example,
 to convert it to a list or tuple), the loop won't print anything, as the zip object will be empty. To successfully iterate over and print elements from a zip object, ensure it hasn't been iterated over since its creation.
'''

# iterable object
for e in zipped:
    print(type(e), e)
    
```
