# Compare_Tool
compares text file can merge they still under development
Overview of the Code:
The provided code is a Python-based graphical user interface (GUI) application that integrates tools for comparing code and identifying semantic duplicates using the Tkinter library. Here's a summary of its components:

1. Overall Structure:
The code is organized into three main classes:

CodeComparatorApp: A tool for comparing two code files with options to ignore whitespace, case, comments, and blank lines.
SemanticDeduplicationApp: A tool for identifying duplicate functions and classes between two code files using Abstract Syntax Tree (AST) analysis.
MultiToolApp: A wrapper class integrating both tools into a Tkinter notebook interface for multi-tab functionality.
2. Features of Each Tool:
CodeComparatorApp
Inputs: Two text areas for users to input or load Python code files.
Comparison Options:
Ignore whitespace.
Ignore case sensitivity.
Ignore comments.
Ignore blank lines.
Functionalities:
Compare Code: Highlights differences between two code snippets using the difflib.unified_diff function.
Load Code: Allows loading of Python files into the text areas.
Save Result: Saves the comparison results to a text file.
File History: Maintains a history of loaded files for quick access.
Real-Time Comparison: Automatically compares code when changes are made to the input fields.
Preprocessing: Modifies the code based on selected options before comparison.
SemanticDeduplicationApp
Inputs: Two text areas for users to input or load Python code files.
Comparison Options:
Ignore whitespace.
Ignore case sensitivity.
Functionalities:
Duplicate Detection: Identifies duplicate functions and classes between two code snippets using AST parsing.
Load Code: Allows loading of Python files into the text areas.
Save Merged Code: Saves the contents of the second text area into a Python file.
Display Duplicates: Shows duplicate functions or classes in a list box.
3. Core Functionalities in Detail:
AST Parsing: Utilizes Python's ast module to parse and analyze code structure for semantic equivalence (functions and classes).
File Operations: Supports loading and saving Python files using tkinter.filedialog.
Dynamic UI Updates: Updates the status bar and automatically processes input changes for improved interactivity.
Tkinter Notebook: Combines the tools in a tabbed interface for easy navigation.
4. User Interface:
Tkinter Framework: Manages the layout and design using Text, Checkbutton, Button, Listbox, and Notebook widgets.
Grid Layout: Organizes elements in rows and columns for a clean, structured appearance.
Real-Time Feedback: Uses key bindings and trace listeners to automatically update comparisons or status when user inputs change.
5. How It Works:
Code Comparator Tab:

User loads or types code into two text areas.
Optional preprocessing options can be toggled.
Upon clicking "Compare Code," differences are displayed in a results text area.
Semantic Deduplication Tab:

User loads or types code into two text areas.
Upon clicking "Find Duplicates," the system identifies and lists duplicate functions and classes.
Merged or deduplicated code can be saved.
Integration:

Both tools are accessible through separate tabs in a unified notebook interface.
