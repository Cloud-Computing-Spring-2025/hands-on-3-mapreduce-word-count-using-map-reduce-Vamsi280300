Project Overview
This project implements a Word Count program using Hadoop MapReduce. The program processes a text file containing multiple lines of words and counts the occurrences of each word. The results are sorted in descending order of frequency.

Approach and Implementation
The implementation follows the MapReduce paradigm, consisting of:

1. Mapper (WordMapper.java)
Reads input text line by line.
Tokenizes each line into words.
Emits each word as a key and assigns the value 1.

2. Reducer (WordReducer.java)
Aggregates word occurrences by summing up values received from the mapper.
Stores word counts in a HashMap.
Sorts words in descending order based on frequency.
Outputs the sorted word count list.

3. Driver (Controller.java)
Configures and initializes the Hadoop job.
Sets up the Mapper and Reducer classes.
Specifies input and output paths.

Execution Steps
1. Build the Project
2. Upload Input File to HDFS
3. Run the Hadoop Job
4. Retrieve the Output

Sample Input and Output:

Sample Input 
kotlin
Copy
Edit
Hello world
Hello Hadoop
Hadoop is powerful
Hadoop is used for big data


Expected Output 
kotlin
Copy
Edit
hadoop 3
hello 2
is 2
used 1
for 1
big 1
data 1
powerful 1
world 1
