# File Renamer

## Description

File Renamer is a Go-based command-line tool that renames files in a specified directory according to a predefined pattern. It's designed to organize files by adding a sequence number and formatting the filename.

## Features

- Renames files in a specified directory
- Adds sequence numbers to filenames (e.g., "1 of 5")
- Supports dry run mode to preview changes
- Handles file extensions correctly

## Installation

1. Ensure you have Go installed on your system. If not, download and install it from [golang.org](https://golang.org/).

2. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/file-renamer.git
   cd file-renamer
   ```

3. Build the project:
   ```bash
   go build
   ```

## Usage

Run the tool with the following command:

```bash
./file-renamer [flags]
```

### Flags

- `-dry`: Run in dry mode (default: true). Set to false to actually rename files.

### Example

To preview changes without renaming files:
```bash
./file-renamer
```

To rename files:
```bash
./file-renamer -dry=false
```

## How It Works

1. The tool walks through the "sample" directory.
2. It identifies files matching the pattern: `base_number.extension`.
3. Files are grouped by their base name and extension.
4. Each group is renamed to: `Base - X of Y.extension`, where X is the sequence number and Y is the total count of files in the group.

## Notes

- The tool currently processes files in the "sample" directory relative to where the program is run.
- Ensure you have necessary permissions to rename files in the target directory.
- Always run in dry mode first to preview changes before actual renaming.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).
