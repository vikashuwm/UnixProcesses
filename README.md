# 🛠️ C++ Unix Utilities – Mini CLI Toolkit

This project is a implementation of common UNIX command-line tools in modern C++. Each utility is implemented as a standalone CLI tool, showcasing key concepts in systems programming, command-line parsing, file I/O, and performance-conscious design.


### 1. `cat` — Concatenate and Display Files

**Usage:**
```bash
cat file1.txt file2.txt
cat -n file.txt      # Line numbers
Features:

Reads and prints files line by line.

Supports -n for line numbering.

Skills Demonstrated:

File I/O (std::ifstream)

CLI arguments

Basic loop control

2. wc — Count Lines, Words, Characters
Usage:

bash
Copy
Edit
wc -lwm file.txt
Flags:

-l: Line count

-w: Word count

-m: Character count

Skills Demonstrated:

String tokenization

Efficient stream processing

Bit-flag parsing for multiple options

3. echo — Print Input
Usage:

bash
Copy
Edit
echo "Hello, World!"
echo -n "No newline"
Skills Demonstrated:

Argument parsing

Handling quoted and special characters

Optional flags

🟡 Medium Tools
4. grep — Pattern Search
Usage:

bash
Copy
Edit
grep "error" file.txt
grep -in "pattern" file.txt
Features:

Case-insensitive search (-i)

Line numbering (-n)

Regex matching

Skills Demonstrated:

std::regex

Case handling

Robust input processing

5. head / tail — View Top/Bottom of Files
Usage:

bash
Copy
Edit
head -n 10 file.txt
tail -n 10 file.txt
Skills Demonstrated:

File stream management

Buffer control

Use of std::deque or seeking for tail

6. sort — Sort File Lines
Usage:

bash
Copy
Edit
sort input.txt
sort -r input.txt   # Reverse
Skills Demonstrated:

Vector sorting

Custom comparators

Optional case-insensitivity

🔴 Advanced Tools
7. find — Search Files by Pattern
Usage:

bash
Copy
Edit
find . -name "*.cpp" -type f
Skills Demonstrated:

Filesystem recursion (<filesystem>)

Pattern matching

Type filtering

8. diff — Compare Files Line-by-Line
Usage:

bash
Copy
Edit
diff file1.txt file2.txt
Features:

Shows line-level differences

Optionally implements Longest Common Subsequence (LCS) algorithm

Skills Demonstrated:

Dynamic programming

Text diffing

Memory efficiency

9. cut / xargs — Input Transformers
Usage:

bash
Copy
Edit
cut -d "," -f 1 file.csv
echo "a b c" | xargs -n 1
