# Jupyter Lab Tutorial for Beginners

Welcome to Jupyter Lab, the gold standard for organizing code in data science. You can think of Jupyter as being like a lab notebook for "dry-lab" research that's based on coding. All of your code, comments, and outputs are organized into "notebooks" and should be easy for yourself and others to review and understand. Let's dive into the basics:

## 1. Starting the Bash Kernel
- Open Jupyter Lab.
- Click on 'Launcher' or 'File' > 'New Notebook'.
- Select 'Bash' from the kernel options.
- *Note:* we also have an option for Python, and an option for R if we install the R kernel, but we don't need to worry about this today. The general steps outlined below are the same for all of these kernels, while only the code is different.
- *What exactly is a kernel anyway?* A kernel is a program that interprets and executes code written in a specific programming language, acting as a mediator between the language and the computer's processing capabilities.

## 2. Creating Cells
- **Using Toolbar**: Click the '+' button on the toolbar to create a new cell.
- **Keyboard Shortcuts**: Press `A` to insert a cell above or `B` to insert below the current cell.

## 3. Code Blocks vs. Text Blocks: What type of cell do we want?
- **Code Blocks**: For writing and executing code. Specify by selecting 'Code' in the dropdown menu in the toolbar.
- **Text Blocks**: For writing text, use Markdown. Choose 'Markdown' from the same dropdown.
- **Keyboard Shortcuts**: Toggle between them using `Y` for code and `M` for Markdown. Alternatively, use the drop-down menu in the toolbar to indicate which you want.

## 4. Running Cells
- **Individual Cell**: Click the 'Play' button in the toolbar or use `Shift + Enter`.
- **Run All Cells**: Go to 'Run' > 'Run All Cells' in the menu.

## 5. Markdown in Jupyter Lab
- **Headers**: Start a line with `#` for a header. More `#`s for smaller headers.
- **Formatting**: Put one `*` on either side of your text to italicize it (e.g., `*italic*`). Put two to bold (e.g.,`**bold**`). Three for both bold and italics.
- **Running Markdown Cell**: Your formatting appears after running the cell with `Shift + Enter`.

Jupyter can have a bit of the learning curve, but it's more than worth being able to keep code well-organized... and can thus help to reduce many other learning curves in the future!
