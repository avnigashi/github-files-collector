# GitHub Repository Downloader

## Overview
The GitHub Repository Downloader is a web application that allows users to download the contents of a public GitHub repository, view the JSON result, and export selected files as a JSON file. This tool is particularly useful for developers who need to retrieve repository data for analysis or backup purposes.

## Features
- Enter the full URL of a public GitHub repository to download its contents.
- Optionally, provide a GitHub token for higher rate limits.
- Configure advanced settings such as file extensions and branch name.
- Download and view the repository contents as JSON.
- Export selected files to a JSON file.
- Copy the JSON content to the clipboard.

## How to Use

### Basic Steps
1. **Enter Repository URL**: Input the full URL of a public GitHub repository (e.g., `https://github.com/user/repo`).
2. **Optional GitHub Token**: Add your GitHub token for higher rate limits.
3. **Configure Settings**: Configure advanced settings if needed.
4. **Download Repository**: Click the "Download" button to fetch the repository contents.
5. **View JSON Result**: The JSON result will appear in a text area below.
6. **Export JSON**: Use the "Export JSON" button to save the contents as a JSON file.
7. **Copy to Clipboard**: Use the "Copy to Clipboard" button to copy all contents.

### Advanced Options
- **GitHub Token**: Input your GitHub token to increase your rate limit.
- **Text Extensions**: Specify the file extensions to be included, separated by commas (default: `.txt,.md,.js,.py,.html,.css,.json,.xml,.yml,.yaml,.ini,.cfg,.conf,.sh,.bat,.ps1,.java,.c,.cpp,.h,.hpp,.cs,.php,.rb,.pl,.sql,.gitignore,.env,.log,.ts,.tsx,.jsx,.vue`).
- **Characters to Escape**: Define characters to escape in the JSON output, separated by commas (default: `&,<,>,",',`).
- **Branch Name**: Specify the branch name to fetch (leave empty for default branch).
- **Folder Path**: Specify the folder path within the repository (optional).

## Components
- **HTML**: Structure of the webpage including input fields, buttons, and result display areas.
- **CSS**: Styling provided by TailwindCSS and custom styles for better UI/UX.
- **JavaScript**: Handles the functionality of downloading repository contents, processing files, and updating the UI.

## Scripts
### Main Functions
- **startDownload()**: Initiates the download process, disables buttons, and updates the UI.
- **parseGitHubUrl(url)**: Parses the GitHub repository URL to extract owner and repo name.
- **downloadRepo(owner, repo, branch, token, folderPath)**: Orchestrates the downloading and processing of repository contents.
- **countTotalFiles(owner, repo, path, branch, token)**: Counts the total number of files in the repository.
- **processContents(owner, repo, path, branch, token)**: Fetches and processes the contents of the repository.
- **fetchFileContent(url, token)**: Fetches the content of a file from GitHub.
- **isTextFile(filename)**: Checks if a file is a text file based on its extension.
- **updateProgressBar()**: Updates the progress bar based on processed files.
- **displayResult()**: Displays the fetched repository contents as JSON.
- **displayFileList()**: Displays a list of files with checkboxes for selection.
- **exportSelectedFiles()**: Exports the selected files as a JSON file.
- **copyToClipboard()**: Copies the JSON content to the clipboard.

## Dependencies
- **TailwindCSS**: For styling the web page.
- **FileSaver.js**: To save files on the client-side.
- **Font Awesome**: For icons used in buttons and other elements.
