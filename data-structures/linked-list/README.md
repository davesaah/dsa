# Linked Lists

- Unlike arrays, they do not demand elements to be in a contiguous block of
memory.
- It's elements can live anywhere in memory as long as one knows where each one
is.
- Each element in a linked list is called a node, and every node contains two 
things: the actual data value and a pointer to the next node. The last node's
pointer is set to null.
- Why traversal is O(n): There's no address formula. The computer has no idea 
where node [4] lives. It only knows where HEAD is. To get to [4], it must follow
the chain: HEAD → [0] → [1] → [2] → [3] → [4]. In the worst case, you walk the 
entire list.
- Why insert at HEAD is O(1): You just create a new node, point it at the old 
HEAD, and declare it the new HEAD. No elements move.
- Delete a node: It is making the previous node's pointer skip over it. The 
deleted node becomes unreachable, There is no shifting required. But you still
have to find it first, which costs O(n).

## Real world examples

- A browser's back/forward history: cheap to add/remove pages at either end.
- A music queue: easy to insert a song right after the currently playing one.
- An undo history in a text editor: each action points to the previous state.

## Questions to test understanding

### Question 1: Conceptual

You have a linked list with 1 million nodes. You want to read the value at 
position 999,999 (the last node). How many steps does it take, and what is the 
Big O notation?

### Question 2: Real world

You're building a text editor's undo system. Every action the user takes gets 
added to the history, and the user can only ever undo the most recent action. 
Would a linked list or an array be a better fit? Why?

### Question 3 — Tricky

A linked list can insert at the HEAD in O(1). But what if you wanted to also 
insert at the TAIL in O(1)? With a standard linked list, inserting at the tail 
is O(n) — you have to traverse the whole list to find the last node. How might
you modify the linked list structure to make tail insertion O(1) too?
