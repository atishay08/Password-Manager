# Password-Manager

A secure password management application built with Python that provides encrypted storage of passwords with a user-friendly interface.

## Features

- Multiple password vaults with unique master passwords
- Strong password generation
- Real-time password strength checking
- Secure encryption of stored passwords
- User-friendly GUI interface
- Password retrieval system
- Password visibility toggle

## Requirements

```txt
customtkinter
cryptography 
zxcvbn
```

## Installation

1. Clone the repository
2. Install dependencies:
```sh
pip install -r requirements.txt
```
3. Run the application:
```sh
python main.py
```

## Usage

### Creating a New Vault

1. Launch the application
2. Click "Create New Vault" 
3. Enter a vault name (optional)
4. Create a strong master password
5. Confirm the master password

### Managing Passwords

1. Select a vault from the vault selection screen
2. Enter the master password to unlock
3. Add new passwords:
   - Enter service/website name
   - Enter username
   - Enter password or generate a strong one
   - Click "Save Password"
4. Retrieve passwords:
   - Enter the service name
   - Click "Retrieve Password"

### Security Features

- AES encryption for stored passwords
- Salted key derivation
- Password strength evaluation
- Secure master password requirements
- Encrypted vault files

## Project Structure

```
Password Manager/
├── main.py              # Main application file
├── requirements.txt     # Project dependencies
├── src/
│   ├── encryption.py          # Encryption utilities
│   ├── password_checker.py    # Password strength checking
│   ├── password_generator.py  # Strong password generation
│   └── vault.py              # Password vault management
└── vaults/                   # Encrypted vault storage
```

## Security Notes

- Master passwords are never stored, only used for key derivation
- All sensitive data is encrypted at rest
- Each vault has its own encryption key
- Password strength is enforced for master passwords
- Uses industry-standard cryptography libraries
