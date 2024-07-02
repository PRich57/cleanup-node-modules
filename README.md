# Nested Node Modules Cleanup Script

This Python script helps you reclaim disk space by removing `node_modules` directories from your projects. It can handle nested project structures, allowing you to clean up `node_modules` at various directory depths.

## Features

- Recursively searches for and removes `node_modules` directories
- Supports dry run mode to preview deletions without making changes
- Allows limiting the search depth
- Provides a summary of space freed and directories removed
- Works with both flat and nested project structures

## Requirements

- Python 3.6 or higher

## Installation

1. Clone this repository or download the `cleanup_nested_node_modules.py` script.
2. Ensure you have Python 3.6+ installed on your system.

## Usage

Run the script from the command line using Python. Here are some usage examples:

1. Basic usage:
   ```
   python cleanup_nested_node_modules.py /path/to/your/projects
   ```

2. Perform a dry run (no deletions, just show what would be removed):
   ```
   python cleanup_nested_node_modules.py /path/to/your/projects --dry-run
   ```

3. Limit the search depth (e.g., to 3 levels):
   ```
   python cleanup_nested_node_modules.py /path/to/your/projects --max-depth 3
   ```

4. Combine options:
   ```
   python cleanup_nested_node_modules.py /path/to/your/projects --dry-run --max-depth 2
   ```

If you run the script without specifying a directory, it will prompt you to enter one.

## Options

- `directory`: The root directory to start searching from.
- `--dry-run`: Perform a dry run without actually deleting anything.
- `--max-depth`: Maximum depth to search for node_modules directories.

## Caution

- Always run with `--dry-run` first to review which directories will be removed.
- Removing `node_modules` directories will require reinstalling dependencies when you next work on a project.
- This script permanently deletes directories. Make sure you have backups or version control in place.

## Contributing

Contributions to improve the script are welcome. Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).