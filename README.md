# Node Modules Cleanup Script

This Python script helps you reclaim disk space by removing `node_modules` directories from your projects. It can handle nested project structures and provides options for dry runs and depth limitations.

## Features

- Recursively searches for and removes `node_modules` directories
- Supports dry run mode to preview deletions without making changes
- Allows limiting the search depth
- Provides a summary of space freed and directories removed
- Works with both flat and nested project structures
- Cross-platform compatibility (Windows, macOS, Linux)
- Follows Python best practices and clean code principles

## Requirements

- Python 3.9 or higher

## Installation

1. Clone this repository or download the `cleanup_node_modules.py` script.
2. Ensure you have Python 3.6+ installed on your system.

## Usage

Run the script from the command line using Python. Here are some usage examples:

1. Basic usage:
   ```
   python cleanup_node_modules.py /path/to/your/projects
   ```

2. Perform a dry run (no deletions, just show what would be removed):
   ```
   python cleanup_node_modules.py /path/to/your/projects --dry-run
   ```

3. Limit the search depth (e.g., to 3 levels):
   ```
   python cleanup_node_modules.py /path/to/your/projects --max-depth 3
   ```

4. Combine options:
   ```
   python cleanup_node_modules.py /path/to/your/projects --dry-run --max-depth 2
   ```

If you run the script without specifying a directory, it will prompt you to enter one.

## Notes for Windows Users

When using the script on Windows, you may need to adjust how you input file paths with backslashes. Here are three ways to correctly input Windows paths:

1. Wrap the path in quotes:
   ```
   python cleanup_node_modules.py "C:\path\to\your\projects"
   ```

2. Use forward slashes instead of backslashes:
   ```
   python cleanup_node_modules.py C:/path/to/your/projects
   ```

3. Escape each backslash with another backslash:
   ```
   python cleanup_node_modules.py C:\\path\\to\\your\\projects
   ```

## Options

- `directory`: The root directory to start searching from.
- `--dry-run`: Perform a dry run without actually deleting anything.
- `--max-depth`: Maximum depth to search for node_modules directories.

## Best Practices Implemented

- Modular design with separate functions for distinct operations
- Use of type hints for improved code readability and potential static type checking
- Clear separation of concerns in function responsibilities
- Descriptive variable names and self-documenting code
- Consistent error handling and user feedback
- Cross-platform path handling using the `pathlib` library

## Caution

- Always run with `--dry-run` first to review which directories will be removed.
- Removing `node_modules` directories will require reinstalling dependencies when you next work on a project.
- This script permanently deletes directories. Make sure you have backups or version control in place.

## Contributing

Contributions to improve the script are welcome. Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).