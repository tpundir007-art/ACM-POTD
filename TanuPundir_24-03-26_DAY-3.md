# POTD- DAY 3

# problem- Best Time to Buy and Sell Stock
You are given an array prices where prices[i] is the price of a given stock on the ith day.
You want to maximize your profit by choosing a single day to buy one stock and choosing a different day in the future to sell that stock.
Return the maximum profit you can achieve from this transaction. If you cannot achieve any profit, return 0.

# APPROACH-
- we have to check what profit we can get if we sell the stock at that index and is it greater than our previous profits
- then we need to also check if current price of stock is less than the minCost we have been keeping track of

# SOLUTION

class Solution     
{  
    public int maxProfit(int[] prices) {  
        int min = Integer.MAX_VALUE;  
        int profit =0;  
        for(int i=0; i<prices.length; i++){  
              if(prices[i]<min) min = prices[i];  
            if(prices[i]-min>profit)  
                profit = prices[i]-min;    
        }  
        return profit;  
    }  
}  

<img width="1908" height="684" alt="image" src="https://github.com/user-attachments/assets/cbbfc07c-5d83-4e2f-af2e-98977c212d9d" />

