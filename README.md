
# CTFSpace

CTFSpace is a command-line tool designed to simplify the creation and management of CTF (Capture The Flag) folders and projects. It allows users to easily organize ongoing, upcoming, and archived CTFs, create default folder structures, and sync writeups efficiently.

## Features

1. **Directory Structure**: 
   - The tool will automatically display the following structure:
   ```
   Ongoing  Tools  Upcoming  Writeups  Z-Archive Template Setup
   ```
   - When running `ctfspace`, it opens the CTF directory and activates a Python environment.

2. **Create New CTF Folders**: 
   - Users can create a new ongoing or upcoming CTF folder with:
     - `ctfspace -new-ongoing "ongoing-CTF"`
     - `ctfspace -new-upcoming "upcoming-CTF"`

3. **Archiving CTFs**: 
   - Archive completed CTFs by running:
     - `ctfspace -archive "ongoing-CTF"`
   - The archived CTF will be stored under `Z-Archive/{year}/ongoing-CTF`.

4. **Default Folder Structure and README.md Creation**: 
   - Every time a new CTF (ongoing or upcoming) is created, a default folder and `README.md` file are generated.
   - Example structure for an ongoing CTF:
   ```
   ongoing-CTF
   |- readme.md
   |- Category
   |  |- web
   |     |- chall-1
   |        |- readme.md
   |     |- chall-2
   |        |- readme.md
   |  |- cryptography
   |     |- chall-1
   |        |- readme.md
   |     |- chall-2
   |        |- readme.md
   |  |- forensic
   |     |- chall-1
   |        |- readme.md
   |     |- chall-2
   |        |- readme.md
   |  |- pwn
   |     |- chall-1
   |        |- readme.md
   |     |- chall-2
   |        |- readme.md
   |  |- steganography
   |     |- chall-1
   |        |- readme.md
   |     |- chall-2
   |        |- readme.md
   |- ongoing-CTF-Writeup
      |- readme.md
   ```

5. **Template-based CTF Creation**: 
   - Users can pass an option like:
     - `ctfspace -new-ongoing "ongoing-CTF" -template "template-name"`
   - The tool will use predefined templates to generate the structure for the new CTF.

6. **Template Example**:
   - A template can define what files and folders are created, including README.md files, category directories, and more.
   Example Template Structure:
   ```
   |- Default.txt
   |- Template-1.txt
   ```
   Template-1.txt example:
   ```
   # ========================== CTF readme.md ==========================
   # Create CTF readme.md file? YES/NO
   readme.md YES

   # =========================== CTF Writeup ===========================
   # Create Writeup folder? YES/NO
   writeup YES

   # Create writeup readme.md file? YES/NO
   readme.md YES

   # ======================= Category Directory ========================
   # Create Category Folder? YES/NO
   Category YES

   # ==================== Category Level Directory =====================
   # Create a level directory for each category?
   Category YES

   # ======================= Challenge Directory ========================
   # Challenge Folder YES/NO
   Challenge YES
   ```

7. **Tools Directory**: 
   - Under the `Tools` directory, you will find subfolders for each CTF category (e.g., web, pwn, cryptography, forensic, steganography).
   Example:
   ```
   Tools
   |- web
   |- cryptography
   |- forensic
   |- pwn
   |- steganography
   ```

8. **Writeup Syncing**: 
   - Every writeup folder in the ongoing or upcoming CTF (inside `Ongoing/ongoing-CTF` or `Upcoming/upcoming-CTF`) will sync to the `Writeups/{year}` folder, based on the current year.

9. **Automatic Year Folder Creation**: 
   - Each year, a new folder is created in `Writeups/{year}` for easy organization of writeups.

10. **Configuration Setup**: 
    - Under the `Setup` folder, there is a configuration file where users can specify their virtual Python environment or use the default `idkCTF-Venv/bin/activate`.

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

After installation, you can use `ctfspace` to manage your CTF challenges.

### Create a New Ongoing CTF

To create a new ongoing CTF folder:
```bash
ctfspace -new-ongoing "ongoing-CTF"
```

### Create a New Upcoming CTF

To create a new upcoming CTF folder:
```bash
ctfspace -new-upcoming "upcoming-CTF"
```

### Archive a CTF

To archive an ongoing CTF:
```bash
ctfspace -archive "ongoing-CTF"
```

### Using a Template to Create a CTF

To create a new CTF using a template:
```bash
ctfspace -new-ongoing "ongoing-CTF" -template "template-name"
```

## Contributing

If you'd like to contribute to CTFSpace, feel free to fork the repository and submit a pull request. Contributions, bug reports, and feature requests are always welcome!

## License

CTFSpace is open-source and available under the [MIT License](LICENSE).
