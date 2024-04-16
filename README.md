# df-mod4-tools
## Module 4 Project
In this assignment, you will explore several activities critical to investigating, 
eliminating, tagging, and discovering digital evidence.

## Objectives 
Specifically, you will: 
1. Use Autopsy to import a pre-computed hash database of known files. 
2. Use Autopsy to find notable (possible evidence) files and generate a hash set of these possibly incriminating files. 
3. Install and use a Hex Editor to compare partial hashes (e.g. just a sector) - useful for matching file remnants. 
4. Use a Hex Editor to bit-shift content (a simple form of encryption) to hide and reveal contents. 
5. Optional Bonus: Explore how investigators can use Rainbow Tables to crack passwords.

## Exercise 1: Autopsy - Import Hash Database (of Known Files)
## Usefulness: 
Hash databases are crucial in digital forensics for quickly identifying known files, 
thus allowing investigators to focus on unique and potentially critical data. 
By importing a known hash database into Autopsy, 
analysts can filter out common files like standard Microsoft Office documents, 
which speeds up the investigation process.

## Skill Demonstrated: Utilizing hash databases to streamline digital forensic investigations.
### Step 1: Obtain the Latest Hash Database
- Navigating to and downloading large datasets from online repositories.
- Action: https://sourceforge.net/projects/autopsy/files/NSRL/ and get the latest hash database (1.3 GB zip file).
### Step 2: Import Hash Database into Autopsy
- Action: Unzip the downloaded file to extract the hash database.
- Then, import it into Autopsy to enable the identification of known files during forensic analysis.
To import a Hash Database of known files into Autopsy, you can follow these steps:
# Download NSRL Hashes:
Start by downloading the latest version of NSRL hashes
from the official website and unzip the file to a designated work folder.
# Open Autopsy:
Launch Autopsy for Windows and close the Welcome window.
# Access Options:
Click on ‘Tools’ and then ‘Options’ from the menu.
# Hash Databases:
In the Options window, select the ‘Hash Databases’ icon to open the relevant section.
# Import Database:
Click on the ‘Import database’ button and navigate to your work folder to select the NSRL file, then click ‘Open’ and ‘OK’.
# Complete Installation: 
Finally, click ‘OK’ in the Options window to finish the installation of the NSRL hashes in Autopsy.

To ensure that the NSRL hash database is up-to-date and corresponds to the version number with the highest value. 
This process will allow Autopsy to use the imported NSRL reference hashes to enhance searching for and eliminating known OS and 
application files during forensic analysis.


## Exercise 2: Autopsy - create Hash Database (of Evidence Files)
This exercise demonstrates the ability to use Autopsy to create a hash database 
of “known bad” or “notable” files, which is crucial for digital forensics investigations.
Hash databases help compare content across a network of machines, aiding in the identification of potential evidence.
## Skills Demonstrated
Mastery in using Autopsy for digital forensics tasks and ability to organize and tag files systematically.

In this case, files of interest are named "Special Project-A" with a .jpg or bmp extension. 
Find these, tag them, and create a hash database for these "known bad" files found. 
1. Open Autopsy. 
2. Create a new case.
3. Add the data source (InChap09.dd). Check the 5 boxes indicated to ingest the info needed for your investigation.
4. Use Autopsy to View File Types by Extension to find the images we're looking for and tag them. 
5. Use Autopsy to Generate Report of Tagged Results in Excel format so we can easily copy the hash values of our evidence files. 
6. Use Autopsy to create a new Tools / Option / Hash Database of these known bad (evidence) files.

## Exercise 3: Hex Editor - Match File Remnants
Files are stored in parts across the storage device. 
Deleting a file removes the link but not the actual data, which remains until overwritten. 
This exercise helps tie a criminal to a document by finding remnants of deleted files. 
It also enhances understanding of file systems and hex editing tools.

# Steps for the Exercise:
1.	Create Document: Generate a Word document.
2.	Hash Calculation: Use a hex editor to calculate the SHA-256 hash value and verify with PowerShell.
3.	Analyze Remnants: Open a specific document and calculate the hash value for the first sector using a hex editor.

This exercise is beneficial for those interested in cybersecurity and digital forensics. 
It provides practical experience with tools like hex editors and deepens the understanding of how operating systems handle file storage and deletion. 
This knowledge is crucial for forensic analysts who need to recover and analyze data from storage devices. 
By learning to match file remnants, one can uncover important evidence that could link individuals to digital activities, even after files have been “deleted.”

## Exercise 4: Bit Shifting (Simple Encryption)
# Objective: 
Understand and practice simple forms of encryption to hide and reveal file contents, which is crucial for investigators to decode evidence.
# Tools Used: 
CyberChef (https://gchq.github.io/CyberChef) - The Cyber Swiss Army Knife - a versatile web app for encryption, encoding, compression, and data analysis.
# Process:
Create a folder named ex4 in your repository. In the ex4 folder:
1. Create a text file with an original simple message and save it as evidence.txt. 
2. Copy the message into CyberChef Input area (see image below). 
3. Use the upper left search bar to find Vigenère Encode - and drag it to the Recipe area. 
4. Enter your key word to use for encrypting. 
5. Use your tool to encrypt the message and save the encrypted message as nothing.txt. 
6. Use the upper left search bar to find Vigenère Decode - and drag it to the Recipe area.
7. Enter your key word (the same one) to use for decrypting.
8. Use your tool to decrypt nothing.txt and save the recovered message as recovered.txt.
   
Bit manipulation, such as bit shifting, is a fundamental technique in digital forensics (DF) 
for analyzing and recovering evidence from digital data. 
It allows investigators to uncover hidden information and understand encryption methods used to conceal data. 
Understanding these concepts is essential for forensic analysis and evidence recovery.
