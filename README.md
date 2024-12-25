# Huffman Coding Project

## Overview
The **Huffman Coding Project** demonstrates an efficient compression algorithm by leveraging the tree data structure. Huffman Coding minimizes the space required to represent text data by assigning shorter codes to frequently occurring characters and longer codes to less frequent ones. This project showcases the practical application of trees, queues, and file I/O in compressing and decompressing text files.

The implementation includes building a Huffman tree, generating binary encodings, encoding text files into compressed files, and decoding compressed files back into their original form.

---

## Features

### Task Implementations

### 1. Build Sorted Frequency List
- **Purpose**: Analyzes the frequency of each character in the input file and creates a sorted list of characters based on their occurrence probabilities.
- **Input**: A text file containing the data to be compressed.
- **Output**: A sorted list of `CharFreq` objects representing each character and its frequency.
- **Usage**: Demonstrates the creation and sorting of frequency data for efficient compression.

### 2. Build Huffman Tree
- **Purpose**: Constructs a binary tree (Huffman tree) using the sorted frequency list to determine the optimal encoding for each character.
- **Steps**:
  - Use a priority queue to merge nodes iteratively.
  - Create a tree where leaf nodes represent characters and internal nodes represent combined frequencies.
- **Output**: The root node of the Huffman tree.
- **Usage**: Highlights tree construction and priority-based operations.

### 3. Generate Encodings
- **Purpose**: Traverses the Huffman tree to generate binary encodings for each character.
- **Steps**:
  - Traverse the tree recursively, assigning '0' for left and '1' for right.
  - Store encodings in an array indexed by ASCII values.
- **Output**: An array containing binary strings for each character.
- **Usage**: Demonstrates recursive tree traversal and encoding generation.

### 4. Encoding
- **Purpose**: Converts input text into a binary string based on the generated encodings and writes it to an output file.
- **Input**: A text file and the generated encodings.
- **Output**: A binary file containing the compressed data.
- **Usage**: Highlights file handling and efficient data compression.

### 5. Decoding
- **Purpose**: Reads the binary compressed file, decodes it using the Huffman tree, and outputs the original text.
- **Input**: A binary file containing compressed data.
- **Output**: A text file containing the decompressed data.
- **Usage**: Demonstrates decoding algorithms and file handling.

---

## Implementation Notes
1. **Code Structure**:
   - All files are located in the `src/huffman/` directory.
   - Predefined files like `CharFreq.java`, `Queue.java`, and `TreeNode.java` simplify tree and queue operations.
   - The main implementation is in `HuffmanCoding.java`.

2. **Algorithms**:
   - Huffman Tree construction using a priority queue.
   - Recursive traversal for encoding generation.
   - Iterative decoding using the Huffman tree.

3. **File Handling**:
   - `StdIn` and `StdOut` are used for reading input and writing output files.
   - Binary data is written using the `writeBitString` method.
   - Binary data is read using the `readBitString` method.

---

## What I Learned
This project provided hands-on experience with the following:

1. **Tree Data Structures**:
   - Constructing and traversing binary trees.
   - Applying tree-based algorithms to practical problems.

2. **Algorithm Implementation**:
   - Implementing the Huffman coding algorithm from scratch.
   - Combining sorting, queue operations, and tree traversal.

3. **File Compression**:
   - Understanding the fundamentals of data compression.
   - Encoding and decoding files efficiently.

4. **File I/O in Java**:
   - Handling text and binary files.
   - Writing and reading data with precision.

5. **Problem-Solving Skills**:
   - Breaking down a complex problem into manageable steps.
   - Debugging and optimizing algorithms for real-world use.

---

## How to Run

1. **Setup**:
   - Ensure Java is installed on your system.
   - Clone this repository and navigate to the `HuffmanCoding` directory.

2. **Compile**:
   ```bash
   javac -d bin src/huffman/*.java
3. **Run**:
   ```bash
   # Run the driver program for interactive testing
   java -cp bin huffman.Driver

   # Example usage:
   # Encode a text file
   java -cp bin huffman.HuffmanCoding encode input.txt encoded.bin

   # Decode an encoded file
   java -cp bin huffman.HuffmanCoding decode encoded.bin output.txt

---

## Conclusion
The Huffman Coding Project was an exciting experience that provided insights into compression techniques, tree data structures, and file handling in Java. By implementing Huffman Coding, I gained a deeper understanding of efficient algorithms and their real-world applications. This project showcased the importance of balancing theoretical knowledge with practical problem-solving to create meaningful software solutions.
