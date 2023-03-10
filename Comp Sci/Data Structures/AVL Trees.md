AVL Trees are Binary Search Trees, with the condition that for a vertex $v$ of the tree:
$$
|\text{height(v.leftSubtree) - height(v.rightSubtree)}| \le 1
$$
Because of this, they are ==self-balancing==.

The smallest AVL Trees can be

![[Pasted image 20230309150412.png|center]]

## Insertion
1. Insert a new node as normal
2. Update the heights in the ancestor nodes
3. If the node becomes unbalanced, rotate to [[#Balancing]] the node.

## Balancing
When a subtree violates the AVL property, need to balance by rotating.

### Left Rotation
1. Store the root of the subtree
2. Make the root the `oldRoot.left`
3. Make `root.left` point to the old root.

![[Pasted image 20230309150945.png|center]]

### Right Rotation
1. Store the root of the subtree
2. Make the root `oldRoot.right`
3. Make `root.right` point to the old root.

![[Pasted image 20230309151003.png|center]]



## Practice Problems
### For every AVL tree of height 3 has at least 7 vertices
This is **true**.

Consider an AVL tree of height 1. It has one vertex, the root.
A tree of height 2 has two cases:
- Two subtrees of height 1 each. The tree has ==3 vertices==.
- One subtree of height 2, and one of height 0. The tree has ==4 vertices==.

A tree of height three has a root node with two children, of which is a tree of height 2. With the subtrees of the root having at least 3 vertices each, as shown above, the tree has at least 7 vertices (subtrees + 1 root).

### For every AVL tree of height 4, it has less than 30 vertices
**True**
For a subtree of height 3, it [[#For every AVL tree of height 3 has at least 7 vertices|has at least 7 nodes]]. A tree of height 3 will have 4 subtrees of height 1, will have 2 extra vertices each.

### If an AVL tree has n vertices, then its height is at most log2(n).
**True**
If the tree is balanced, it has the same [[Binary Trees#Binary Tree Depth|height of a binary tree]].
$$\begin{align}
2^{h+1}-1&\le n\\
h+1&\le\log_{2}(n+1)\\
h&\le\log_{2}(n+1)-1\\
h&\le\log_{2}n
\end{align}$$

### Removal from an AVL tree always removes a leaf.
**True**

Removing a node from an AVL tree will look down the tree for the largest node in the subtree. It will always be at the bottom, as a leaf. It's value gets swapped with the node to be removed, before a rotation is formed. So, **the removal of a node from an AVL tree will always remove a leaf.**

### Insertion into an AVL tree always increases the number of leaves
**False**
