# Bash Cheatsheet

This page provides a quick reference for Bash shell commands and scripting.

## Basic Commands

```bash
# Display text
echo "Hello World"

# Set a variable
name="Linux"
echo "Hello $name"

# Command substitution
current_dir=$(pwd)
echo "Current directory: $current_dir"

# Arithmetic operations
result=$((5 + 3))
echo "5 + 3 = $result"
```

## Control Structures

### If-Else Statement

```bash
if [ "$name" = "Linux" ]; then
    echo "Name is Linux"
elif [ "$name" = "BSD" ]; then
    echo "Name is BSD"
else
    echo "Name is something else"
fi
```

### Loops

```bash
# For loop
for i in 1 2 3 4 5; do
    echo "Number: $i"
done

# While loop
count=1
while [ $count -le 5 ]; do
    echo "Count: $count"
    count=$((count + 1))
done

# Until loop
count=1
until [ $count -gt 5 ]; do
    echo "Count: $count"
    count=$((count + 1))
done
```

### Case Statement

```bash
case "$name" in
    "Linux")
        echo "It's Linux"
        ;;
    "BSD")
        echo "It's BSD"
        ;;
    *)
        echo "Unknown operating system"
        ;;
esac
```

## Functions

```bash
# Define a function
greet() {
    echo "Hello, $1!"
}

# Call the function
greet "World"
```

## String Operations

```bash
string="Hello World"

# String length
echo ${#string}

# Substring
echo ${string:0:5}  # "Hello"

# Replace
echo ${string/World/Linux}  # "Hello Linux"
```

## File Operations

```bash
# Check if file exists
if [ -f "/path/to/file" ]; then
    echo "File exists"
fi

# Check if directory exists
if [ -d "/path/to/directory" ]; then
    echo "Directory exists"
fi

# Read file line by line
while IFS= read -r line; do
    echo "$line"
done < "/path/to/file"
```

## Comparison Operators

### Numeric Comparisons

```bash
# Equal
[ "$a" -eq "$b" ]

# Not equal
[ "$a" -ne "$b" ]

# Greater than
[ "$a" -gt "$b" ]

# Less than
[ "$a" -lt "$b" ]

# Greater than or equal
[ "$a" -ge "$b" ]

# Less than or equal
[ "$a" -le "$b" ]
```

### String Comparisons

```bash
# Equal
[ "$a" = "$b" ]

# Not equal
[ "$a" != "$b" ]

# Less than (alphabetically)
[[ "$a" < "$b" ]]

# Greater than (alphabetically)
[[ "$a" > "$b" ]]

# Empty string
[ -z "$a" ]

# Non-empty string
[ -n "$a" ]
```

## Special Variables

```bash
$0    # Script name
$1    # First argument
$2    # Second argument
$@    # All arguments
$#    # Number of arguments
$?    # Exit status of last command
$$    # Process ID of the script
$!    # Process ID of last background command
$USER # Current username
$HOME # Home directory
$PWD  # Current directory
```

## Input/Output Redirection

```bash
# Redirect stdout to file
command > file.txt

# Append stdout to file
command >> file.txt

# Redirect stderr to file
command 2> error.txt

# Redirect both stdout and stderr to file
command &> all.txt

# Redirect stdout to stderr
command 1>&2

# Redirect stderr to stdout
command 2>&1

# Pipe output to another command
command1 | command2
```

## Useful One-liners

```bash
# Find and replace in multiple files
find . -type f -name "*.txt" -exec sed -i 's/old/new/g' {} \;

# Count lines in files
find . -type f -name "*.py" | xargs wc -l

# Monitor a log file
tail -f /var/log/syslog

# Find largest files
find . -type f -exec du -h {} \; | sort -rh | head -n 10

# Kill processes by name
pkill -f "process_name"
```