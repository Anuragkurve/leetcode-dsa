Approach 1: Horizontal scanning
Intuition
For a start we will describe a simple way of finding the longest prefix shared by a set of strings LCP(S 
1
​
 …S 
n
​
 ).
We will use the observation that :

LCP(S 
1
​
 …S 
n
​
 )=LCP(LCP(LCP(S 
1
​
 ,S 
2
​
 ),S 
3
​
 ),…S 
n
​
 )

Algorithm
To employ this idea, the algorithm iterates through the strings [S 
1
​
 …S 
n
​
 ], finding at each iteration i the longest common prefix of strings LCP(S 
1
​
 …S 
i
​
 ) When LCP(S 
1
​
 …S 
i
​
 ) is an empty string, the algorithm ends. Otherwise after n iterations, the algorithm returns LCP(S 
1
​
 …S 
n
​
 ).

Finding the longest common prefix