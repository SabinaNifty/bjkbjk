# Testing Program

This Java program generates JSON data representing repository statistics.

## How to Run

To run this program, you need to have Java installed on your system. Follow these steps:

1. **Download the JAR File**: Download the latest version of the JAR file from the "Releases" section of this repository.

2. **Open Terminal (or Command Prompt)**: Open your terminal or command prompt.

3. **Navigate to the Directory with the JAR File**: Use the `cd` command to navigate to the directory where you downloaded the JAR file.

4. **Run the Program**: Execute the following command to run the program:
5. **View the Output**: Once the program finishes running, the JSON output will be displayed in the console.

## Sample Output

```json
{
"location": "/a/b/c",
"stat_of_repository": {
 "number_of_commits": 101,
 "avg_of_num_java_files": 30.2,
 "avg_of_num_warnings": 193.2
},
"stat_of_warnings": {
 "AbstractClassWithoutAbstractMethod": 1908,
 "AvoidReassigningCatchVariables": 2020
 // Add other warning types here if needed
}
}
