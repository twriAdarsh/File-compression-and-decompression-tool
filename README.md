Huffman Coding Compression Algorithm

This project implements Huffman Coding, a lossless, bottom-up compression algorithm. It can efficiently compress and decompress any text files by using variable-length codes for encoding characters based on their frequencies.

Implementation
This project supports two main functions:

1.Encode: Compresses the input file.

2.Decode: Decompresses a Huffman coded file back to its original form.
Data Structures

1.struct Node: Represents a node of the Huffman Tree. It stores character data, its frequency, Huffman code, and two pointers that point towards the left or right node if they exist.

2.Huffman Class: Contains two public functions, compress() and decompress(), and a constructor which accepts the input file and output file.

How to Use
Compressing a File (compress())
1.createMinHeap(): Reads the input file and stores the frequency of all characters. It then creates a Min Heap structure based on these frequencies using a priority queue.

2.createTree(): Generates the Huffman Tree by duplicating the Min Heap. It pops the two nodes with the lowest frequency, assigns them as left and right nodes to a new node (with the sum of the two frequencies), and pushes this new node back to the Min Heap. This continues until the Min Heap has only one node.

3.createCodes(): Traverses the Huffman Tree and assigns binary codes to every node.

4.saveEncodedFile(): Saves the Huffman encoded input file to the output file.

Output File Structure
The output file (.huf) contains:

Min Heap data: ({character data} {huffman code for that character}) * minheapsize

Encoded input file characters

count0: Number of '0's appended at the end of the binary string to make it a multiple of 8 bits.

Decompressing a File (decompress())

1.getTree(): Reads the Min Heap from the beginning of the file and reconstructs the Huffman Tree.

2.saveDecodedFile(): Reads the encoded file and decodes it using the Huffman Tree to reconstruct the original file.

 How to  use?
 
![image](https://github.com/twriAdarsh/File-compression-and-decompression-tool/assets/143320903/181e3b4c-fe49-4558-99e1-37b9a812403d)
