# EX 6C TRAVELLING SALES MAN PROBLEM
## DATE:
## AIM:
To Solve Travelling Sales man Problem for the following graph.

![image](https://github.com/user-attachments/assets/653921a4-3d7b-4691-9b41-735e80f7af0b)



## Algorithm
1.Start from a chosen city as the current city and mark it as visited. 
2.Find the nearest unvisited city from the current city. 
3.Move to that nearest unvisited city and mark it as visited. 
4.Repeat steps 2 and 3 until all cities have been visited. 
5.Return to the starting city to complete the tour and calculate the total distance.   

## Program:
~~~
To implement the program for TSP.


Developed by: RAKSHITHA K
Register Number:  212223230009


from sys import maxsize
from itertools import permutations
V = 4
def travellingSalesmanProblem(graph, s):
    #Write your code
    #Start here
    vertex = []
    for i in range(V):
        if i != s:
            vertex.append(i)
    min_path = maxsize
    next_permutation=permutations(vertex)
    
    for i in next_permutation:
        current_pathweight = 0
        k = s
        for j in i:
            current_pathweight += graph[k][j]
            k = j
        current_pathweight += graph[k][s]
        min_path = min(min_path, current_pathweight)
        
    return min_path
    #End here
if __name__ == "__main__":
    graph = [[0, 10, 15, 20], [10, 0, 35, 25],
        [15, 35, 0, 30], [20, 25, 30, 0]]
    s=0
    print(travellingSalesmanProblem(graph, s))
~~~

## Output:
![image](https://github.com/user-attachments/assets/1b5e41b9-222a-4804-93c2-b0a85f8615b2)

## Result:
Thus the program was executed successfully for finding the minimum cost to vist all cities.
