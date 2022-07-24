**Problem:-**

Given a string s, find the first non-repeating character in it and return its index. If it does not exist, return -1.

**Input: -**

hackerrank

**Output :-**

3

**Exaplainatation :-** 

 > here we need to find the first  unique character from the given string (h,a,c,k,e,r,r,a,n,k),
 > Only character "c" and "e" are unique, in which "c" is coming first on index 3
 >  hence return 3

**Input: -** 

problems

**Output :-** 

1

**Exaplainatation :-** 


 > The given string (p,r,o,b,l,e,m,s), comes with all characters unique
 > 
 >  hence return 1


**Input: -** 

testes

**Output :-** 

-1

**Exaplainatation :-** 

 > The given string (t,e,s,t,e,s) has all characters reapting 
 >  hence return -1

**Code:-**

```python
def getUniqueCharacters(s):
  # If no string type or empty string passed to this method
  if not s:
    return -1
  # Creating disctionary (map) to store the count of characters
  hash = {}
  # Looping through the string and counting all the characters 
  for c in s:
    if c not in hash:
      hash[c] = 1
    else:
      hash[c] += 1
   for i in range(len(s)):
     # count of s[i] is 1, then its the first element present at the start of the string
     if hash[s[i]] == 1:
       return 1
   # if all the charaters are reapting, and no unique char found, then -1
   return -1
```
