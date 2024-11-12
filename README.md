# JS (Java Script) Downloader

A simple command-line download manager built with **Node.js** that supports downloading files from direct URLs and torrent links. This tool provides visual feedback during downloads through a progress bar.

![js downloader](https://github.com/user-attachments/assets/30b4ff09-7a9d-42ae-ba18-1f901a362c94)

**Features**

*   Download files from direct HTTP/HTTPS links.
*   Download files from magnet links using WebTorrent.
*   Read multiple download links from a **.txt** file.
*   Progress bar display for ongoing downloads.
*   Automatically creates a downloads directory on the desktop.

**Requirements**

*   Node.js (version 12 or higher)
*   npm (Node Package Manager)

**Installation**

*   Clone this repository or download the script file.
*   Navigate to the project directory in your terminal.
*   Install the required packages:
	```bash
	npm install webtorrent
	```

## Usage

To use the download manager, run the script with a URL or a path to a **.txt** file containing URLs. The script supports both direct download links and magnet links.

**Command Line Usage**

```bash
node jsdownloader.js <url/magnet link/.txt>
```

**Examples**

1.  Download a single file
    
    ```bash
    node jsdownloader.js https://example.com/file.zip
    ```
    
2.  Download a magnet link
    
    ```bash
    node jsdownloader.js "magnet:?xt=urn:btih:..."
    ```
    > Magnet link require "quotes".
    
3.  Download multiple files from a **.txt** file. Create a **downloads.txt** file with the following contents:
    
    ```bash
    https://example.com/file1.zip
    https://example.com/file2.zip
    "magnet:?xt=urn:btih:..."
    ```
    Then run
    
    ```bash
    node jsdownloader.js downloads.txt
    ```
	> Drag and drop link to terminal are supported.
		
## Visual

This script draws colored progress-bar on the console based on the provided progress. The progress bar will indicate the download status, changing colors based on the progress:

### Progress Bar

|Progress  | Color |
|--|--|
|0-49% | Red |
|0-49% | Yellow |
|0-49% | Green |

### Download Directory

Downloaded files will be saved in a **downloads** directory on your desktop, which will be created automatically if it does not exist.

*   Windows: Desktop/downloads (default)
*   macOS: Desktop/downloads (default)
*   Linux: Desktop/downloads (default)

### Error Handling

If an error occurs during the download process, the script will log the error message to the console and continue downloading the next file if applicable.

### Support

The script uses Node.js and several native modules **(https, fs, path, os)**. Cross platform, **(Windows/macOS/Linux)**. 

### Contributing

Contributions are welcome! Feel free to submit a pull request or open an issue for any enhancements or bug fixes.

## Acknowledgments

*   **WebTorrent** for enabling torrent downloads.
*   **Node.js** for providing a powerful runtime for building this application.
