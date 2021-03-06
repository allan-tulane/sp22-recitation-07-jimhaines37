# CMPS 2200 Recitation 7
## Answers

**Name:**_________________________


Place all written answers from `recitation-07.md` here for easier grading.



- **d.**

File | Fixed-Length Coding | Huffman Coding | Huffman vs. Fixed-Length
----------------------------------------------------------------------
f1.txt    |1340|826|0.61641791


alice29.txt    |         1039367            |      676374          | 0.65075570


asyoulik.txt    |           873253          |        606448        | 0.69209235


grammar.lsp    |         26047            |        17356        | 0.66633393


fields.c    |          78050           |        56206        | 0.72012812

Yes, Huffman coding always seems to cost less than fixed length encoding. It seems that Huffman coding takes about 65% of the cost that it takes fixed length coding to do the same task.


- **e.**

To obtain the Huffman cost we determine the number of binary digits required to make up 1 character and multiply this by the frequency of that character, we do this for each character and sum them. In this situation, each frequency is the same, so any 2 characters can be selected to create a new node (like in make_huffman_tree), so we will usually have a balanced tree. A balanced tree has a root node and 2 children, and each of those children have 2 children and so on, one side does not have any more children than the other and the tree depth should be equal for all nodes if the number of characters allows for this. I have included a visual below. This means that Huffman has a cost closer to fixed length coding in this scenario and is only a little better, not a lot better like for the above examples. 



         N
       /   \
      N     N
     / \   /  \ 
    N  N  N    N .....
