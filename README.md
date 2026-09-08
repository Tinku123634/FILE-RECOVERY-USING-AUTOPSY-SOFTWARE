# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:
Recovered Deleted File List and Details

<img width="1600" height="899" alt="1" src="https://github.com/user-attachments/assets/c6931e9b-d447-4137-b198-f4ab13de4e82" />

<img width="1600" height="899" alt="2" src="https://github.com/user-attachments/assets/98e59821-d8a9-489f-b797-ed17ed36b2f2" />

<img width="1600" height="900" alt="3" src="https://github.com/user-attachments/assets/27a3412a-c12a-4e55-86e3-efc3bc722b0b" />

<img width="1600" height="899" alt="4" src="https://github.com/user-attachments/assets/829b376c-3e29-44d3-bb2d-60fa63333fcf" />


<img width="1600" height="892" alt="5" src="https://github.com/user-attachments/assets/d8490b02-525f-4544-955a-d1cecf8fb9a1" />

<img width="1600" height="899" alt="6" src="https://github.com/user-attachments/assets/d15c090e-4610-49e6-a7a8-855370dbeb87" />

<img width="1600" height="898" alt="7" src="https://github.com/user-attachments/assets/5080deb7-ac0e-4bc4-b2e2-181eaef2275b" />


<img width="1600" height="899" alt="8" src="https://github.com/user-attachments/assets/134e6b45-85aa-4ab8-81c3-aeb57c4eeed5" />

<img width="1600" height="895" alt="9" src="https://github.com/user-attachments/assets/97c81a7b-82c7-4515-832e-3f284037d0ab" />

<img width="1600" height="899" alt="10" src="https://github.com/user-attachments/assets/e57a9999-43a8-48c2-972b-90e7b6888eac" />

<img width="1482" height="926" alt="11" src="https://github.com/user-attachments/assets/30b5c6aa-5320-4497-ac28-0add15f3b4ce" />








## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
