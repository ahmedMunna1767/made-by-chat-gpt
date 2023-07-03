# AWK command in Linux

`awk` is a powerful command-line tool used in Linux and Unix-like systems for processing and manipulating text files. It is primarily used for data extraction, reporting, and text processing tasks. `awk` operates on a line-by-line basis, reading input files, applying specified patterns, and executing associated actions.

The basic syntax of the `awk` command is as follows:
```
awk 'pattern { action }' input-file
```

Here's a breakdown of the components:

- `pattern`: The pattern specifies a condition that must be matched for the associated action to be executed. It can be a regular expression, a comparison, or any other condition. If the pattern is omitted, the action will be applied to all input lines.

- `{ action }`: The action specifies the operation to be performed on the input lines that match the pattern. It can be a series of commands enclosed in curly braces. Multiple actions can be separated by semicolons.

- `input-file`: This is an optional parameter that specifies the input file(s) for `awk` to process. If no input file is provided, `awk` reads from standard input (e.g., output from a previous command or piped input).

Now, let's dive into some common use cases and examples to illustrate the power and versatility of `awk`:

1. Print specific fields from a file:
   ```
   awk '{ print $1, $3 }' input.txt
   ```
   This command prints the first and third fields of each line in the `input.txt` file.

2. Filter lines based on a condition:
   ```
   awk '$2 > 50 { print $1, $2 }' input.txt
   ```
   This command prints the first and second fields of lines where the second field is greater than 50.

3. Perform calculations:
   ```
   awk '{ sum += $1 } END { print sum }' input.txt
   ```
   This command calculates the sum of the values in the first field of `input.txt` and prints the result at the end.

4. Use built-in functions:
   ```
   awk '{ print length($0) }' input.txt
   ```
   This command prints the length of each line in the `input.txt` file.

5. Apply conditional statements:
   ```
   awk '{ if ($1 > 50) print "High"; else print "Low" }' input.txt
   ```
   This command prints "High" if the value of the first field is greater than 50, and "Low" otherwise.

These examples provide a glimpse of the capabilities of `awk`. It offers numerous features, including variables, arrays, string manipulation functions, control flow statements, and more, making it a versatile tool for text processing and data manipulation in the Linux environment.

For a more comprehensive understanding of `awk`, I recommend referring to the official documentation and exploring online tutorials and guides that cover its various features and usage patterns.



## AWK Command Examples

| Category            | Function                           | Simple Use Case                                        | Example Code                                          |
|---------------------|------------------------------------|-------------------------------------------------------|-------------------------------------------------------|
| String Functions    | `length(string)`                   | Calculate the length of a string                      | `awk '{len = length($0); print len}' data.txt`         |
|                     | `index(string, substring)`          | Find the position of a substring in a string          | `awk '{pos = index($0, "world"); print pos}' data.txt` |
|                     | `substr(string, start, length)`     | Extract a substring from a string                     | `awk '{sub = substr($0, 2, 4); print sub}' data.txt`   |
|                     | `split(string, array, separator)`   | Split a string into an array of substrings             | `awk '{split($0, arr, " "); print arr[2]}' data.txt`   |
|                     | `toupper(string)`                   | Convert a string to uppercase                         | `awk '{str = toupper($0); print str}' data.txt`        |
|                     | `tolower(string)`                   | Convert a string to lowercase                         | `awk '{str = tolower($0); print str}' data.txt`        |
|                     | `gsub(regex, replacement, string)`  | Replace all occurrences of a pattern in a string      | `awk '{gsub("world", "hello", $0); print}' data.txt`   |
| Mathematical Functions | `sqrt(x)`                          | Calculate the square root of a number                 | `awk 'BEGIN{num = 16; sqrt_val = sqrt(num); print sqrt_val}'` |
|                        | `exp(x)`                           | Calculate the exponential value of a number           | `awk 'BEGIN{num = 2; exp_val = exp(num); print exp_val}'` |
|                        | `log(x)`                           | Calculate the natural logarithm of a number           | `awk 'BEGIN{num = 10; log_val = log(num); print log_val}'` |
|                        | `sin(x)`                           | Calculate the sine value of an angle                  | `awk 'BEGIN{angle = 45; sin_val = sin(angle); print sin_val}'` |
|                        | `cos(x)`                           | Calculate the cosine value of an angle                | `awk 'BEGIN{angle = 60; cos_val = cos(angle); print cos_val}'` |
|                        | `tan(x)`                           | Calculate the tangent value of an angle               | `awk 'BEGIN{angle = 30; tan_val = tan(angle); print tan_val}'` |
|                        | `rand()`                           | Generate a random number                              | `awk 'BEGIN{random_val = rand(); print random_val}'` |
| Array Functions     | `length(array)`                     | Get the number of elements in an array                | `awk 'BEGIN{arr[1]=10; arr[2]=20; len = length(arr); print len}'` |
|                     | `delete array[index]`               | Delete an element from an array                       | `awk 'BEGIN{arr[1]=10; arr[2]=20; delete arr[1]; print arr[1]}'` |
|                     | `in array[index]`                   | Check if an index exists in an array                  | `awk 'BEGIN{arr[1]=10; if (1 in arr) print "Index exists"; else print "Index does not exist"}'` |
|                     | `split(string, array, separator)`   | Split a string into an array based on a separator     | `awk '{split($0, arr, " "); for(i in arr) print arr[i]}' data.txt` |
| Input Functions     | `getline`                           | Read the next input record                             | `awk '{getline input_line; print input_line}' data.txt` |
|                     | `NF`                                | Get the number of fields in the current input record  | `awk '{num_fields = NF; print num_fields}' data.txt` |
|                     | `NR`                                | Get the current record number                          | `awk '{record_num = NR; print record_num}' data.txt` |
|                     | `FNR`                               | Get the record number in the current file              | `awk '{file_record_num = FNR; print file_record_num}' data.txt` |
|                     | `$0`                                | Get the entire input record                            | `awk '{print $0}' data.txt` |
| Control Flow Functions | `if-else`                          | Conditionally execute code                            | `awk '{if ($1 > 10) print "Greater"; else print "Smaller"}' data.txt` |
|                       | `for`                               | Iterate over a range of values                        | `awk 'BEGIN{for(i=1; i<=10; i++) print i}'` |
|                       | `while`                             | Repeat code while a condition is true                 | `awk 'BEGIN{i=1; while(i<=10) {print i; i++}}'` |


Please note that the example code provided assumes that `data.txt` is the input file. You can replace it with your actual data file or modify the code according to your specific use case.
