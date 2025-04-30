# Convert Repository to HTML
A lightweight Python script (<350 lines) that converts your repository contents to a single, well-formatted HTML document. I often use it for LLMs. 

## Why I use it?
- Doesn't require any external Python libraries, only uses the Python standard library.
- No security risks for Enterprise
- Easily exclude certain files / folders
- Quickly convert to PDF

## How I use it?

1. Create a folder called `repo-export` in your repository
2. Add the `repo_to_html.py` file to this folder
3. Navigate to the folder:
   ```bash
   cd repo-export
   ```
4. Run the script pointing to the parent directory:
   ```bash
   python repo_to_html.py ..
   ```
   This will generate `repository.html` in the current directory

## How I convert it to PDF?

### Option 1: Using VS Code Live Server (My go-to option)
1. Click on the generated HTML file in VS Code sidebar
2. Left click on the file to start the Live Server extension (click "Go Live" )
3. Use browser's print function (Ctrl+P or Cmd+P)
4. "Save as PDF"

### Option 2: Using Python's Built-in Server
If you don't have access to VS Code extensions:
```bash
python -m http.server
```
Then open http://localhost:8000 in your browser, navigate to `repository.html`, and print to PDF.
