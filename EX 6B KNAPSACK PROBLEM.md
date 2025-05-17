# EX 6B KNAPSACK PROBLEM
## DATE:
## AIM:
To demonstrate a python program using dynamic programming for 0/1 knapsack problem.



## Algorithm
1.Initialize a 2D array dp with zeros, dimensions (n+1) x (W+1) where n = number of items, W = capacity.
2.For each item i from 1 to n, do: 
3.For each capacity w from 0 to W, do: 
4.If weight[i] <= w, set dp[i][w] = max(dp[i-1][w], value[i] + dp[i-1][w - weight[i]]). 
5.Else, set dp[i][w] = dp[i-1][w].   

## Program:
~~~
To implement the program for 0/1 knapsack problem.


Developed by: RAKSHITHA K
Register Number: 2212223230009


def knapSack(W, wt, val, n):
    ########## Add your code here #########
    #Start here
	if n == 0 or W == 0 :
		return 0
	if (wt[n-1] > W):
		return knapSack(W, wt, val, n-1)
	else:
		return max(val[n-1] + knapSack(W-wt[n-1], wt, val, n-1), knapSack(W, wt, val, n-1))
	#End here
x=int(input())
y=int(input())
W=int(input())
val=[]
wt=[]
for i in range(x):
    val.append(int(input()))
for y in range(y):
    wt.append(int(input()))

n = len(val)
print('The maximum value that can be put in a knapsack of capacity W is: ',knapSack(W, wt, val, n))
~~~

## Output:
![image](https://github.com/user-attachments/assets/07205f71-38b7-4017-9eb6-0daf01c72ec9)

## Result:
Thus the program was executed successfully for finding the maximum value that can be put in a knap sack of capacity .
