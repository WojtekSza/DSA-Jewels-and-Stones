# DSA-Jewels-and-Stones
You're given strings jewels representing the types of stones that are jewels, and stones representing the stones you have. Each character in stones is a type of stone you have. You want to know how many of the stones you have are also jewels.

Letters are case sensitive, so "a" is considered a different type of stone from "A".
```
Input: jewels = "aA", stones = "aAAbbbb"
Output: 3
```
```
from collections import Counter
class Solution:
    def numJewelsInStones(self, jewels: str, stones: str) -> int:
        ans=0
        jewels_set=set(jewels) #Time cost O(n)
        stones_count=Counter(stones) # Time cost O(m)
        for i,j in stones_count.items(): # Time cost O(n)
            if i in jewels_set: # Time cost O(1)
                ans+=j
        return ans #Space cost O(1)
    '''
    Total time cost 3O(n) = O(n)
    Total space cost O(1)
    '''
        
```
