# blind-1-75
two sum 
Gonna start something important.

Blind 75

part-1/75

Two sum question



Basically we use a dictionary/hash map 

run through array,check if complement(target-num) is already present in hash map.

if yes,return the indices of 2 elements that sum upto target.

else ,update hash map with current element and index (use enumerate).

time complexity : O(n)

space compllexity: O(n) may be for hash map.

The fact that search and update operations are O(1) in hash map /dictionary on average has helped to navigate through this problem easily


class Solution(object):
    def twoSum(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: List[int]
        """
        x={}
        for i,num in enumerate(nums):
            y=target-num
            if y in x:
                return [x[y],i]
            else:
                x[num]=i
        
