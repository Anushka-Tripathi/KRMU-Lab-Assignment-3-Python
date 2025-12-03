# KRMU-Lab-Assignment-3-Python
# Library Inventory Manager

A command-line library management system built with Python, demonstrating Object-Oriented Programming principles, file persistence, and robust error handling.

## Features

- **Book Management**: Add, issue, return, and search books
- **Persistent Storage**: JSON-based data storage
- **Search Functionality**: Search by title or ISBN
- **Robust Error Handling**: Comprehensive exception handling and logging
- **User-Friendly CLI**: Interactive menu-driven interface
- **OOP Design**: Clean class-based architecture

## Project Structure

```
library-inventory-manager/
│
├── library_manager/          # Main package
│   ├── __init__.py          # Package initialization
│   ├── book.py              # Book class definition
│   └── inventory.py         # LibraryInventory class
│
├── cli/                      # Command-line interface
│   └── main.py              # Main CLI application
|
├── library_data.json         # Data storage (created on first run)
├── requirements.txt          # Dependencies
├── .gitignore               # Git ignore file
└── README.md                # This file
```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/library-inventory-manager-anushka.git
cd library-inventory-manager-anushka
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

Run the application:
```bash
python -m cli.main
```

Or:
```bash
python cli/main.py
```

### Menu Options

1. **Add Book**: Add a new book to inventory
2. **Issue Book**: Issue an available book
3. **Return Book**: Return an issued book
4. **View All Books**: Display complete inventory
5. **Search by Title**: Find books by title (partial match)
6. **Search by ISBN**: Find a specific book by ISBN
7. **Exit**: Save and exit the application

## Example Usage

```
--- Add New Book ---
Enter book title: Python Crash Course
Enter author name: Eric Matthes
Enter ISBN: 978-1593279288

✓ Book 'Python Crash Course' added successfully!
```

## Technical Details

### Book Class
- **Attributes**: title, author, isbn, status
- **Methods**: issue(), return_book(), is_available(), to_dict()
- **Magic Methods**: __init__(), __str__()

### LibraryInventory Class
- **Attributes**: books (list), data_file (Path)
- **Methods**: add_book(), search_by_title(), search_by_isbn(), display_all()
- **File Operations**: save_to_file(), load_from_file()

### Error Handling
- JSON decode errors for corrupted files
- File I/O exceptions
- Input validation
- Duplicate ISBN prevention

### Logging
- INFO level: Operations and searches
- ERROR level: Exceptions and failures
- Output: Console and library.log file

## Requirements

- Python 3.7+
- pathlib (standard library)
- json (standard library)
- logging (standard library)

## Contributing

This is an academic assignment. Please do not copy code directly.

## License

MIT License - Educational purposes

## Author

[Anushka Tripathi]  
[anushka.official1911@gmail.com]  
K.R. Mangalam University

## Acknowledgments

- Course: Programming for Problem Solving using Python
- Instructor: sameer.farooq@krmangalam.edu.in

## Resources Referenced

- Python Official Documentation: https://docs.python.org/3/
- PEP 8 Style Guide: https://pep8.org/
