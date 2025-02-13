# FiveM Map Collision Finder

## 📌 Overview
The **FiveM Map Collision Finder** is a Python script originally created by [puttydotexe](https://github.com/puttydotexe) to scan a specified directory for potential map file conflicts in FiveM. It identifies duplicate file names across multiple locations and outputs the results, including the file path, size, and last modified date.

## 🔥 Features
- Scans a directory for duplicate map-related files
- Supports ignoring specific file types
- Outputs results to a text file, including:
  - File name
  - Full file path
  - File size (in bytes)
  - Last modified date
- Works with various FiveM map file types (`.ytd`, `.ymt`, `.ydr`, `.ydd`, `.ytyp`, `.ybn`, `.ycd`, `.ymap`, `.ynv`, `.ypt`)

---

## 🛠 Installation
### **1. Clone the Repository**
To download the script, use the following command:
```
git clone https://github.com/JimmySackss/fivem-map-collision-finder.git
```
Then 'cd fivem-map-collision-finder'


**2. Install Python (If Not Installed)**

This script requires Python 3.6 or later. You can check your version with:

```
python --version
```

If you don’t have Python installed, download it from: [Python Official Site](https://www.python.org/downloads/)

**3. Install Dependencies**

No additional dependencies are required; the script utilizes Python's built-in libraries.
🚀 Usage

Run the script with the following command:
```
python checker.py <directory_to_scan> --ignore <ignored_file_patterns> --output <output_file>
```

Example Command
```
python checker.py "C:\FiveMServer\resources" --ignore "*.ydd" --output "C:\Users\Desktop\collision_results.txt"
```

Explanation:

    C:\FiveMServer\resources → The directory where FiveM map files are stored
    --ignore "*.ydd" → Ignores .ydd files from the scan
    --output "C:\Users\Desktop\collision_results.txt" → Saves the results to a text file

📄 Output Format

If any collisions are found, the script will generate an output similar to this:

Possible collisions: lr_sc1_1_strm.ymap
 - C:\FiveMServer\resources\map1\stream\lr_sc1_1_strm.ymap | Size: 2,345,678 bytes | Last Modified: 2025-02-12 14:30:22
 - C:\FiveMServer\resources\map2\stream\lr_sc1_1_strm.ymap | Size: 2,345,678 bytes | Last Modified: 2025-02-11 09:12:45
 - C:\FiveMServer\resources\backup\old_maps\lr_sc1_1_strm.ymap | Size: 2,345,678 bytes | Last Modified: 2025-01-15 18:45:10

Total collisions found: 1

If no collisions are found, the script will output:

`No collisions found.`

## **❗ Troubleshooting**
*Output File Not Generating?*

    Ensure you are using --output <filepath> correctly.
    Use a full path instead of just a filename.
    Run the script as administrator if needed.
    Check if the script prints Writing output to: before writing the file.

Need Help?

If you encounter any issues or have feature requests, feel free to open an issue on GitHub.

📜 License

This project is licensed under the MIT License, allowing you to freely use, modify, and distribute it.

Contributions are welcome! Again, thanks for Puttydotexe for all of their contributions! 
