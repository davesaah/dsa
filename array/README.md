# Arrays

- A fixed-size ordered collection of elements stored in a contiguous 
(side-by-side) memory.
- Because elements are packed together, the computer can jump to any element 
instantly using simple arithmetic.
- Why reading is O(1): The computer knows exactly where every element lives. If
the array starts at memory address 0x1000 and each integer takes 4 bytes, then 
element [5] is always at 0x1000 + 5*4 (0x14) = 0x1014. No searching, no 
following pointers; one calculation and you're there.
- Why insert/delete is O(n): Arrays demand contiguous memory. If you insert 
something in the middle, every element after it must physically move one slot 
to make room. With a million-element array, one insert near the front costs a 
million moves.

## Real world examples

- Video frames: stored as an array, seeked by frame number in one jump.
- RGB pixel data: every pixel at a known offset from the image start.
- A leaderboard: sorted array of scores, read and updated by rank position.

## Questions to test understanding

### Question 1: Conceptual

An array stores 1000 elements. How many steps does it take to read the element 
at index 999 compared to reading the element at index 0?

### Question 2: Real world

You're building a music app. You have a playlist of 50 songs stored in an array.
A user clicks "jump to song 37". Is an array a good choice for this feature? 
Why or why not?

### Question 3: Tricky

You need to frequently add and remove songs from the middle of the playlist. 
Does your answer to Question 2 change? What does this tell you about choosing 
the right data structure?

### Bonus

If an array starts at memory address 0x2000, each element takes 8 bytes, and you
want to access index [6] — what is the memory address of that element?
