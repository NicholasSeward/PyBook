# Linked Lists

## What is a Linked List?

A linked list is like a scavenger hunt - each clue points to the next one. Instead of storing all items in one place, each item (called a "node") holds its data and a pointer to the next item.

## How Nodes Work

Each node has two parts:
- **Data**: The actual information (like a number, string, etc.)
- **Next**: A pointer to the next node in the list

```python
# Simple node structure
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

# Create a few nodes
first = Node("Alice")
second = Node("Bob")
third = Node("Charlie")

# Link them together
first.next = second
second.next = third
third.next = None  # End of list
```

## Why Use Linked Lists?

### Easy to Grow
- Add new items anywhere without moving everything else
- No need to pre-allocate space
- Perfect for lists that change size frequently

### Quick Insertions
- Insert in the middle without shifting other items
- This is the **only option** for fast middle insertions
- Arrays/lists have to move everything after the insertion point

### Only Need the Head
- You only need to remember the first node (called "head" or "root")
- Each node knows where the next one is
- Like following a trail of breadcrumbs

## Example: Adding Items

```python
# Start with empty list
head = None

# Add first item
head = Node("Alice")

# Add second item at beginning
new_node = Node("Bob")
new_node.next = head
head = new_node

# Add third item in middle
middle_node = Node("Charlie")
middle_node.next = head.next
head.next = middle_node
```

## Advantages vs Disadvantages

**Advantages:**
- Fast insertions anywhere
- Easy to grow and shrink
- No wasted space
- Flexible structure

**Disadvantages:**
- Can't jump to random positions quickly
- Need to follow the chain to find items
- Extra memory for pointers
- More complex than arrays

## Trees are Just Fancy Linked Lists

Trees are like linked lists where each node can point to multiple other nodes instead of just one "next" node. The same node concept applies, but with more connections.

## Key Points

- **Nodes**: Hold data and point to next item
- **Head**: Only need to remember the first node
- **Growing**: Easy to add items anywhere
- **Insertions**: Fast middle insertions (unique advantage)
- **Scavenger hunt**: Each clue points to the next
- **Trees**: Just linked lists with multiple connections
