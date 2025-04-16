
# CTFSpace

CTFSpace is a command-line tool designed to simplify the organization and automation of CTF (Capture The Flag) challenges. It allows CTF participants to efficiently manage their CTF folders, sync writeups, and maintain a clean structure for ongoing, upcoming, and archived CTFs.

## Features

- **Organized Folder Structure**: Automatically creates and manages folders for CTFs with templates.
- **Writeup Syncing**: Sync writeups between different folders and years.
- **Template-based Setup**: Define folder structures using `.txt` files and automatically set up environments.
- **Python Virtual Environment Support**: Automatically activate Python virtual environments.
- **GitHub Distribution**: Easy distribution and sharing of CTF setup with GitHub.

## Installation

To install `ctfspace`, clone the repository and install the necessary dependencies:

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ctfspace.git
   ```

2. Navigate into the project directory:
   ```bash
   cd ctfspace
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

After installing, you can use `ctfspace` to manage your CTF challenges.

### Initialize a New CTF

To create a new CTF folder structure, use the following command:
```bash
ctfspace init <ctf_name> [optional_template_file]
```

### Sync Writeups

To sync writeups for ongoing and upcoming CTFs:
```bash
ctfspace sync
```

### Activate Python Virtual Environment

To activate a Python virtual environment for your CTF project:
```bash
ctfspace venv activate
```

### List CTFs

To list all the available CTFs in the current directory:
```bash
ctfspace list
```

### Archive CTFs

To move completed CTFs to an archived folder:
```bash
ctfspace archive <ctf_name>
```

## Contributing

If you'd like to contribute to CTFSpace, feel free to fork the repository and submit a pull request. Contributions, bug reports, and feature requests are always welcome!

## License

CTFSpace is open-source and available under the [MIT License](LICENSE).
