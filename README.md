# Embed Images in Markdown Files as Base64
This Python script is designed to embed images in Markdown files as base64 strings, making the Markdown files self-contained without requiring external image references. The script will search for Markdown files in a specified directory and convert linked images to embedded base64 images if available.

Designed and tested with Obsidian in mind but should work with other editors.

## Features
- Converts image links in Markdown (`.md`) files to base64 strings.
- Removes image links if the image file is not found.
- Supports relative image paths for Markdown files.

## Requirements
- Python 3.x
- Basic Python libraries (`os`, `base64`, `re`, `argparse`)

## Usage
To use the script, run it from the command line with the following command:

```sh
python embed_images_in_md.py <vault_path>
```

- `<vault_path>`: The path to your Obsidian vault or directory containing the Markdown files.

### Example
```sh
python embed_images_in_md.py "C:\Users\JohnDoe\Documents\MyVault"
```
This command will process all Markdown files in the specified directory and convert the linked images to base64 embedded images.

## How It Works
1. The script takes a directory path (`vault_path`) as input.
2. It traverses through the given directory and finds all `.md` files.
3. It reads each Markdown file and searches for image links (`![alt text](image/path.jpg)`).
4. If the image is found, it converts the image to a base64 string and replaces the link with an embedded image in the Markdown file.
5. If the image file does not exist, the link is removed.

## Notes
- The script supports only image links with relative paths or absolute paths that can be resolved.
- URL-encoded characters (e.g., `%20` for spaces) are decoded to correctly locate the files.

## License
This script is open source and can be used and modified freely.

## Troubleshooting
- **Image not found and link removed**: This message indicates that the script couldn't locate the linked image file. Make sure the images are correctly placed relative to the Markdown files.

## Author
JSON SEC
