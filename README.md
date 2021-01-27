## binary-tree-search

# Requirements Summary
For this program, we were required to implement a binary search tree which had the requirements as follows:

* Maintain an asymptotic runtime for insertions
* Maintain an O(H) runtime for the functions where H is the height of the BST
* Write a function to place all values of the BST in a vector
* Write a function get_ith which returns the value at the specified place
* Write a function which returned the values greater than or equal to the parameter
* Write a function which returned the values that are less than or equal to the parameter
* Write a function which returned the values betweeen a specified range
* Assure the height of the binary search tree was log2(N) where N is the total number of nodes


# Solution
In order to implement the following requirements, my solutions were as follows:

* In order to keep the runtime asymptotic when rebalancing the BST, I made sure to only rebalance it when
one of the subtrees did not meet the required height because it was a costly function in terms of runtime
* In order to keep a O(H) runtime on the functions that were written, an integer variable was added to the node
data structure which kept track of the number of children belonging to each node. This change helped to
avoid traversing every individual node when trying to count nodes based on a requirement.
* Created a vector with BST values by recursively went through all nodes and children of nodes, then added
them to vector upon return
* Able to retrieve the value at the specified position this by using the property of BSTs where all nodes are in
order and the leftmost
one is the smallest value, from there I used a counter to traverse through
* Able to retrieve values greater than or equal to the parameter by traversing the BST recursively until the value
is found, or a value greater than the specified value is found,
then use the counter value in the node's data structure to return the total number of values that are greater
than or equal to the parameter
* Same approach as the point above, only with values less than or equal to the parameter
* Same approact as the greater than or equal to function, only with a range specified by the parameters
* Used a rebalancing function to check if there is an imbalance of the number of children in the parent everytime
a new node is deleted or added to the BST
