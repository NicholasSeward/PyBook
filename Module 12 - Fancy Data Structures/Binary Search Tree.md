# Binary Search Tree

## What is a Binary Search Tree?

A binary search tree (BST) is a special tree structure that makes searching very fast. It's like organizing books on shelves where each book tells you which shelf to look at next.

## Tree Rules

A BST must follow these rules:
- Each node has at most **2 children** (left and right)
- **Left child** must be **smaller** than its parent
- **Right child** must be **larger** than its parent
- This rule applies to **every node** in the tree

## Basic Structure (Python Code)

```python
class Node:
    """Represents a single node in the binary search tree."""
    def __init__(self, value):
        self.value = value
        self.left = None   # Points to smaller values
        self.right = None  # Points to larger values

class BinarySearchTree:
    """A binary search tree implementation."""
    def __init__(self):
        self.root = None
```

## Example Tree

```
       8
      / \
     3   10
    / \    \
   1   6    14
      / \
     4   7
```

In this tree:
- 8 is the root
- Left subtree (3, 1, 6, 4, 7) - all values < 8
- Right subtree (10, 14) - all values > 8
- Each subtree follows the same rules

## Why This Gives O(log n) Lookups

### The Magic of Halving
Every time you look at a node, you eliminate **half** the remaining possibilities:
- Look at root (8)
- Is your target < 8? Go left (eliminate right half)
- Is your target > 8? Go right (eliminate left half)
- Repeat until you find it

### Example Search for 4
1. Start at 8: 4 < 8, go left
2. Look at 3: 4 > 3, go right  
3. Look at 6: 4 < 6, go left
4. Found 4!

## Code Implementation

### Searching for a Value

```python
def search(self, value):
    """Search for a value in the BST. Returns True if found, False otherwise."""
    return self._search_recursive(self.root, value)

def _search_recursive(self, node, value):
    """Helper method that recursively searches the tree."""
    # Base case: empty node means value not found
    if node is None:
        return False
    
    # Found it!
    if node.value == value:
        return True
    
    # Value is smaller, search left subtree
    if value < node.value:
        return self._search_recursive(node.left, value)
    
    # Value is larger, search right subtree
    if value > node.value:
        return self._search_recursive(node.right, value)
```

This search method demonstrates the O(log n) performance:
- Each recursive call eliminates half the remaining nodes
- Average case: O(log n) for balanced trees
- Worst case: O(n) for completely unbalanced trees

### Why O(log n)?
- Each step eliminates half the remaining nodes
- Like binary search in a sorted list
- If you have n nodes, you need at most log₂(n) steps
- Even with 1 million nodes, you need at most 20 steps!

## Tree Shapes Matter

### Good Tree (Balanced)
```
   5
  / \
 3   7
/ \ / \
1 4 6 8
```
- O(log n) performance
- Each level is roughly half full

### Bad Tree (Unbalanced)
```
1
 \
  2
   \
    3
     \
      4
       \
        5
```
- O(n) performance (like a linked list)
- No branching, just a straight line

## Inserting Values

```python
def insert(self, value):
    """Insert a new value into the BST."""
    self.root = self._insert_recursive(self.root, value)

def _insert_recursive(self, node, value):
    """Helper method that recursively finds the correct position to insert."""
    # Base case: create new node if we've reached a leaf
    if node is None:
        return Node(value)
    
    # Value is smaller, insert in left subtree
    if value < node.value:
        node.left = self._insert_recursive(node.left, value)
    
    # Value is larger, insert in right subtree
    elif value > node.value:
        node.right = self._insert_recursive(node.right, value)
    
    # If value already exists, we don't insert duplicates
    # (Some BST implementations allow duplicates - this one doesn't)
    
    return node  # Return the (possibly modified) node
```

### Example: Building the Tree from the Example

```python
# Create a new BST
bst = BinarySearchTree()

# Insert values in any order
bst.insert(8)
bst.insert(3)
bst.insert(10)
bst.insert(1)
bst.insert(6)
bst.insert(14)
bst.insert(4)
bst.insert(7)

# Now the tree looks like:
#       8
#      / \
#     3   10
#    / \    \
#   1   6    14
#      / \
#     4   7
```

## Traversing the Tree

### In-Order Traversal (Prints Values in Sorted Order)

```python
def in_order_traversal(self):
    """Visit all nodes in sorted order (left, root, right)."""
    self._in_order_recursive(self.root)
    print()  # New line after traversal

def _in_order_recursive(self, node):
    """Helper method for in-order traversal."""
    if node is not None:
        self._in_order_recursive(node.left)   # Visit left subtree
        print(node.value, end=" ")            # Visit current node
        self._in_order_recursive(node.right)  # Visit right subtree

# Example usage:
# bst.in_order_traversal()
# Output: 1 3 4 6 7 8 10 14
```

## Complete Example

```python
class Node:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None

class BinarySearchTree:
    def __init__(self):
        self.root = None
    
    def insert(self, value):
        """Insert a new value into the BST."""
        self.root = self._insert_recursive(self.root, value)
    
    def _insert_recursive(self, node, value):
        if node is None:
            return Node(value)
        if value < node.value:
            node.left = self._insert_recursive(node.left, value)
        elif value > node.value:
            node.right = self._insert_recursive(node.right, value)
        return node
    
    def search(self, value):
        """Search for a value in the BST."""
        return self._search_recursive(self.root, value)
    
    def _search_recursive(self, node, value):
        if node is None:
            return False
        if node.value == value:
            return True
        if value < node.value:
            return self._search_recursive(node.left, value)
        return self._search_recursive(node.right, value)
    
    def in_order_traversal(self):
        """Print all values in sorted order."""
        self._in_order_recursive(self.root)
        print()
    
    def _in_order_recursive(self, node):
        if node is not None:
            self._in_order_recursive(node.left)
            print(node.value, end=" ")
            self._in_order_recursive(node.right)

# Example usage:
bst = BinarySearchTree()
bst.insert(8)
bst.insert(3)
bst.insert(10)
bst.insert(1)
bst.insert(6)

print(bst.search(6))  # True
print(bst.search(5))  # False
bst.in_order_traversal()  # 1 3 6 8 10
```

## Real-World Examples

**Good BST uses:**
- Dictionary lookups
- Database indexes
- File system organization
- Game AI decision trees

**When BSTs struggle:**
- Data that comes in sorted order
- Frequently changing data
- Need for guaranteed balance

## Key Points

- **Rules**: Left < Parent < Right
- **Structure**: Each node has at most 2 children
- **Performance**: O(log n) when balanced
- **Magic**: Each step eliminates half the possibilities
- **Balance**: Tree shape affects performance
- **Use case**: Fast searching in organized data
