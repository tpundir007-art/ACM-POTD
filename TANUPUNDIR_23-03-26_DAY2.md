POTD-2 
# Subarray Sum Equals K
Given an array of integers nums and an integer k, return the total number of subarrays whose sum equals to k.
A subarray is a contiguous non-empty sequence of elements within an array

# Approach- we create a map of values to keep track of sum so far. Basically we are calculating prefix sum in this problem to find subarrays that have sum equal to k.

# SOLUTION
'''java
class Solution   
{  
    public int subarraySum(int[] a, int k)   
    {  
        HashMap<Integer,Integer> m=new HashMap<>();  
        m.put(0,1);  
        int sum=0;  
        int c=0;  
        for( int x:a)  
        {  
            sum+=x;  
            if(m.containsKey(sum-k))  
            {  
                c+=m.get(sum-k);  
            }  
            m.put(sum,m.getOrDefault(sum,0)+1);  
        }  
        return c;  
    }  
}  
  '''
  <img width="1410" height="685" alt="image" src="https://github.com/user-attachments/assets/65a60671-6dc8-49b7-acc6-5865e37f1ae1" />

