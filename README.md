# Contacts Management CLI

This is a simple Node.js CLI application for managing a list of contacts. The application allows you to list, add, remove, get, and update contacts stored in a JSON file.

## Features

- List all contacts
- Get a contact by ID
- Add a new contact
- Remove a contact by ID
- Update a contact by ID (only specified fields are updated)

## Usage

- node index.js -a list
- node index.js -a get -i <contact-id>
- node index.js -a add -n "John Doe" -e "john@example.com" -p "1234567890"
- node index.js -a remove -i <contact-id>
- node index.js -a update -i <contact-id> -n "New Name" -e "newemail@example.com" -p "9876543210"

Note: When updating a contact, only the specified fields (-n, -e, -p) will be updated. Fields not provided will remain unchanged.

## Example Contact Format

{
"id": "unique-id",
"name": "John Doe",
"email": "john@example.com",
"phone": "1234567890"
}

## Dependencies

- commander: For parsing CLI commands and options.
- nanoid: For generating unique IDs.
- Node.js built-in modules:  
    - fs/promises: For file system operations.  
    - path: For handling file paths.
