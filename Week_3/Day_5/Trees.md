## Trees

![](/Week_3/Images/trees-node.PNG)
![](/Week_3/Images/trees-leaf.PNG)
![](/Week_3/Images/trees-children.PNG)
![](/Week_3/Images/trees-siblings.PNG)

## Tree Traversal

![Breadth First Traversal](/Week_3/Images/breadth-first-traversal.PNG)

### Breadth first traversal:

Start with the root node.
Then move onto the root's children.
Then move onto those node's children.
You'll have noticed that we access each node row-by-row. Breadth first traversal will always visit the nodes closest to the root node before moving on to the nodes that are farther away.

## Depth First Traversal

![Depth First](/Week_3/Images/depth%20first%20traversal.PNG)

### Sub Trees

A tree is a recursive data structure. A tree is actually made up of smaller sub trees, which themselves are made up of even smaller sub trees.

Every node in the tree, apart from the root node, is actually the root node of a smaller tree.

### Traversal
For depth first traversal, we're going to take advantage of the recursive nature of the tree and write a recursive algorithm.

Traverse tree:

1. Visit the root node of the tree.
2. Get the first unvisited child sub-tree of the current node.
3. Do step 1 with the sub-tree.

## Code
Here's what the implementation of this algorithm looks like:
```javascript
class Node {

  constructor(data) {
    this.data = data;
    this.parent = null;
    this.children = [];
  }

  depthFirstTraversal() {

    console.log(this); // 1

    for (const childNode of this.children) {
      childNode.depthFirstTraversal(); // 2
    }
  }
}
```

1. Visit the current node. In this case, we're just printing out the data.
2. Loop through every child of the current node and repeat the first step with that node.

We can use recursion to implement depth first traversal, so it's a little bit easier to implement than breadth first traversal because a tree is a recursive data structure.

