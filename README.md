# Addressbook-Management-System

A command-line contact management system built in **C**, demonstrating core programming concepts including data structures, file I/O, and search algorithms.

## Features

- **Create Contacts** – Add new contacts with name, phone, and email
- **Advanced Search** – Search contacts by name, phone, or email with flexible filtering
- **Edit Contacts** – Modify existing contact information
- **Delete Contacts** – Remove contacts from the address book
- **List All Contacts** – Display all stored contacts
- **Persistent Storage** – Automatically save/load contacts from file

## Technical Highlights

### Architecture
- **Modular design** with header/implementation file separation (`contact.h/c`, `file.h/c`, `populate.h/c`)
- **Struct-based data organization** for clean contact representation
- **Dynamic contact management** supporting up to 100 contacts

### Data Structure
```c
typedef struct Contact {
    char name[50];
    char phone[20];
    char email[50];
} Contact;

typedef struct {
    Contact contacts[MAX_CONTACTS];
    int contactCount;
} AddressBook;
```

### Key Functions
- `createContact()` – User input handling with validation
- `searchContact()` – Advanced filtering by contact fields
- `editContact()` – In-place contact modification
- `deleteContact()` – Contact removal with array reorganization
- `saveContactsToFile()` / `loadContactsFromFile()` – File persistence

## Getting Started

### Compilation
```bash
gcc main.c contact.c file.c populate.c -o addressbook
```

### Running
```bash
./addressbook
```

### Usage
The program presents an interactive menu:
```
Address Book Menu:
1. Create contact
2. Search contact
3. Edit contact
4. Delete contact
5. List all contacts
6. Save and Exit
```

**Example: Advanced Search**
```
Search by:
1. Name
2. Phone
3. Email
Enter choice: 1
Enter name to search: John
Results found...
```

## Skills Demonstrated

- **C Fundamentals** – Pointers, arrays, structs, memory management
- **File I/O** – Reading/writing contact data to persistent storage
- **Algorithm Design** – Linear search with filtering logic
- **Modular Programming** – Separation of concerns across modules
- **String Handling** – Safe string operations and validation

## Project Structure
```
├── main.c          – Menu loop and user interface
├── contact.c/h     – Contact operations (CRUD)
├── file.c/h        – File I/O operations
├── populate.c/h    – Data initialization
└── addressbook     – Compiled executable
```

## Limitations & Future Enhancements
- Fixed array size (100 contacts) — could be replaced with dynamic allocation
- Basic string search — could implement regex or fuzzy matching
- No encryption — contact data stored in plaintext
- Windows/Linux compatibility — tested on both platforms


---

*Built as a foundational project to master C programming concepts and system design principles.*
