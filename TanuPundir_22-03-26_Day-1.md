# POTD-DAY1
## Remove Duplicates from Sorted Array
Given an integer array nums sorted in non-decreasing order, remove the duplicates in-place such that each unique element appears only once. 
The relative order of the elements should be kept the same. Consider the number of unique elements in nums to be k​​​​​​​​​​​​​​. 
After removing duplicates, return the number of unique elements k. 
The first k elements of nums should contain the unique numbers in sorted order. The remaining elements beyond index k - 1 can be ignored.

# LOGIC-
- Since the array is already sorted, we can compare elements and check if duplicates exist. 
- Then, if there is a duplicate we shift elements in such a way without creating a new array.
# solution
class Solution 
{
    public int removeDuplicates(int[] nums)   
    {  
        if(nums.length==0)  
        {  
            return 0;  
        }  
        int count=1;  
        for(int i=1;i<nums.length;i++)  
        {  
        if(nums[i]!=nums[i-1])  
        {  
        nums[count]=nums[i];  
        count++;  
        }  
        }  
        return count;  
        
<img width="1365" height="749" alt="Screenshot 2026-03-22 113334" src="https://github.com/user-attachments/assets/0f9b6af8-aa3d-44ef-8c6c-8a8487efd8cc" />

        

    
    }
}
