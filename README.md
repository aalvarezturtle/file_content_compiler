# file_content_compiler
## Overview

`file_content_compiler.py` is a Python script designed to compile the contents of files from a specified directory into a single output file. It allows you to specify which file extensions to include, as well as directories and individual files to exclude from the compilation process. This script is particularly useful for aggregating code files or configuration files into a single document for review or archival purposes.

## Features

- **Directory Traversal**: Recursively searches through a specified directory to find files with specified extensions.
- **File Filtering**: Allows exclusion of specific directories and files from the compilation.
- **Content Aggregation**: Compiles the contents of the collected files into a single output file, with clear demarcations between files.
- **Summary Output**: Provides a summary of the number of files and total lines compiled.

## Usage

1. **Specify the Directory**: Set the `directory` variable to the path of the directory you want to search.

2. **Define File Extensions**: Use the `extensions` tuple to specify which file types to include (e.g., `.py`, `.json`).

3. **Exclude Directories**: List any directories you want to exclude in the `exclude_dirs` list.

4. **Exclude Files**: List any specific files you want to exclude in the `exclude_files` list.

5. **Set Output File Name**: Define the name of the output file in the `output_file` variable.

6. **Run the Script**: Execute the script to compile the files. The output will be saved to the specified output file.

## Example

```python
# Directory/folder of code to compile into single .txt file
directory: str = os.path.join(os.path.expanduser("~"), "Documents")

# Specific file extensions to include in compilation
extensions: Tuple[str, ...] = (".py", ".json")

# List of directories/folders to exclude in the compilation
exclude_dirs: List[str] = [
    "TRASH", 
    "__pycache__", 
    "build"
]

# List of individual files to exclude in compilation
exclude_files: List[str] = [
    "example.py", 
    "config.json"
]

# Name of output_file
output_file: str = "compiled_file_contents.txt"
```

## Output

The script will generate an output file named `compiled_file_contents.txt` (or your specified name) containing the contents of the included files. Each file's content is prefixed and suffixed with markers indicating the file name and the number of lines.

## Requirements

- Python 3.x
- Standard Python libraries: `os`, `typing`

## License

This script is open-source and available for modification and distribution under the MIT License.

https://e2.udemymail.com/ls/click?upn=u001.J6oXy5r8ccZ1oJmAL5RD97klFUYdeQ6e0A61WDAhalCx-2BzwOQMDEDGu6Yp69OFP9HMjozM1uGojn02SKno1rwC9PjoF6LZlKigacSbHHm5BSJDdqvkOH9QMpk6R1Ub1kBpOBJ-2BUPoPUe1-2Fy8UX9PHjLuNSlQTmuulY6alz8iiNDKgjyliBmNh04FrhYYjlVxcMoIaAd4cxcGkmSaEPzu4aVHsda4-2BDjqSzj6EqiEM3b6E1ZR5qvXXOrfLjJXNIO9bVEu8HmNS3JiCdRzS40f1g-3D-3DzCNQ_QXnTW6f9jV7ots26-2Fd0iCLooQ3OELZTHnoB4tNHcQaB4X9F6g7OOHzxRO6xCtGAUcQPkjadHYQGOmBQ-2B-2F4KGxKJJqwmnvF-2BmIVU7euIWSBw8gfEBaVhMZhPEtJ-2B-2BGlrYkM1abd4fKNvClSCRIqUz3TetSj0-2FjzIeI8rAcLjiE8tqlu18XhFiM5M-2FlVFrQyiX8boV2I1vnC902TkxtdMcFSBxOb5JWatkVfShOlGqkTCOZ6T7lJuN7mFMW4qmsz0jpMxqkROFEUi8GpHe91V4OMT-2FugKVuHfVwstgqsd65-2FEqCMnfFuf-2Bm3W-2FegjqnuXfuw7n-2FHHv6l-2BezAUrJo5eAIc6t60a24I35NqxAJEnsJg-3D
