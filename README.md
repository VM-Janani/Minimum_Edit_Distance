*Minimum Edit Distance Algorithm*
**Summary**
This code implements the Minimum Edit Distance algorithm, a dynamic programming solution used to calculate the minimum number of operations required to transform one string into another. The algorithm supports three basic operations: insertion, deletion, and substitution, each with customizable costs. This implementation follows the pseudocode from Daniel Jurafsky's book, Speech and Language Processing.

**Features**
Customizable Costs: Define different costs for insertion, deletion, and substitution operations.
Dynamic Programming Approach: Efficient solution with a time complexity of O(m*n), where m and n are the lengths of the input strings.
Flexible Usage: The function can handle strings of varying lengths and returns the minimum cost to transform the source string into the target string.

**Example**
source = "intention"
target = "execution"
min_distance = min_edit_distance(source, target, del_cost=1, ins_cost=1, sub_cost=2)
print(f"Minimum edit distance between '{source}' and '{target}' is: {min_distance}")

Output:
Minimum edit distance between 'intention' and 'execution' is: 8
In this example, the substitution cost is set to 2, while insertion and deletion costs are both 1. The algorithm calculates the least costly sequence of operations to transform "intention" into "execution."

**How It Works**
Distance Matrix: A 2D matrix D[n+1, m+1] is constructed, where n is the length of the source string and m is the length of the target string.
Initialization: The first row and column represent the cost of transforming the string into an empty string.
Recurrence Relation: For each character in both strings, the algorithm computes the minimum cost of three possible operations:
Insertion
Deletion
Substitution
Result: The final value in the matrix D[n, m] gives the minimum edit distance between the two strings.

**Use Cases**
Spell Checking: Identifying the closest word to a misspelled input.
DNA Sequence Comparison: Analyzing differences between genetic sequences.
Autocorrect Systems: Correcting typos in text input.
Machine Translation Evaluation: Measuring differences between machine-generated and reference translations.
