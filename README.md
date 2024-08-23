# giftwrapy

giftwrapy (pronounced "gift-wrap-ee") is a Python tool that converts a project, folder, or repository into a single long markdown file. This is particularly useful for use with AI assistants, allowing you to easily share the structure and contents of your project.

## Features

- Generates a tree structure of your project
- Includes file contents for specified extensions
- Allows ignoring specific directories and files
- Customizable output file name
- No dependencies outside of the Python standard library

## Installation

You can install giftwrapy using pip:

```bash
pip install giftwrapy
```

## Usage

After installation, you can use giftwrapy from the command line:

```bash
giftwrapy /path/to/your/project
```

For more options:

```bash
giftwrapy --help
```

### Basic Usage Example

```python
from giftwrapy import dir_to_markdown

dir_to_markdown(
    directory=".",
    extensions=[".py", ".html", ".sql", ".css", ".md"],
    output_file="project_contents.md",
)
```

### Command Line Options

- `directory`: The path to the directory to convert.
- `--extensions`: List of file extensions to include (default: [".py", ".html", ".sql", ".css", ".md"]).
- `--ignore-dirs`: List of directory names or patterns to ignore.
- `--ignore-files`: List of file names or patterns to ignore.
- `--use-default-ignore-pats`: Whether to use the default ignore patterns (default: True).
- `--output`: Name of the output markdown file (default: "project_contents.md").

## Default Ignore Patterns

giftwrapy uses default ignore patterns for both the tree structure and file contents. These include common directories and files like `__pycache__`, `.git`, `.vscode`, and others. You can add to these patterns using the `--ignore-dirs` and `--ignore-files` options.

## Using with AI Assistants

giftwrapy is designed to make it easy to share your project structure and contents with AI assistants. Here's an example of how the output can be used:

![Example usage with an AI assistant](usage.png)

This screenshot demonstrates how the markdown file generated by giftwrapy can be used in a conversation with an AI assistant, allowing for more context-aware and project-specific interactions.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
