### **EHF Lecture**

**Topic Covered:** Windows Terminal Basics  
Today, we explored the **fundamentals of Windows command-line interface**. The focus was on how to handle file and folder operations directly from the terminal.

| Command                       | Description                               |
| ----------------------------- | ----------------------------------------- |
| `dir`                         | Lists files and directories               |
| `cd`                          | Changes current directory                 |
| `cd [folder]`                 | Enters the specified folder               |
| `mkdir` / `md [folder]`       | Creates a new folder                      |
| `rename` / `ren [src] [dest]` | Renames a file/folder                     |
| `del [filename]`              | Deletes a file                            |
| `rmdir`                       | Removes an empty directory                |
| `copy`                        | Copies files                              |
| `move`                        | Moves files                               |
| `cls`                         | Clears the screen                         |
| `exit`                        | Exits the terminal                        |
| `help`                        | Provides help on commands                 |
| `time`                        | Displays or sets the system time          |
| `ipconfig`                    | Displays network configuration            |
| `systeminfo`                  | Displays system configuration             |
| `ping`                        | Tests network connectivity                |
| `tracert`                     | Traces route to a network host            |
| `getmac`                      | Displays MAC address                      |
| `shutdown /r`                 | Restarts the system                       |
| `shutdown`                    | Shuts down the system                     |
| `echo off`                    | Turns off command echoing                 |
| `prompt`                      | Changes the command prompt                |
| `color a`                     | Changes terminal text color to green      |
| `dir /`                       | Lists contents with additional formatting |
| `tree`                        | Displays folder structure as a tree       |
| `netsh`                       | Network configuration command             |
| `control`                     | Opens the control panel                   |
| `start`                       | Opens a new command prompt or application |
| `start powershell`            | Launches PowerShell terminal              |
| `path`                        | Displays or sets a search path            |
| `regedit`                     | Opens the Windows registry editor         |

### **Data Structures (DS) Lecture**

**Topic Introduced:** Hashing & File Organization  
Chapters 2 and 3 (Linear and Non-Linear Data Structures) will be handled later by the HOD or HOI. For now, **Drishti Ma’am** has started with **Chapter 4: Hashing and File Structures**.

####  Notes on File Organization:

**Basic Concepts:**

- **Field:** A single piece of data (e.g., Name, Age)
- **Record:** A group of related fields (e.g., one row of a student database)
- **File:** A collection of related records

---

#### **Types of File Organization:**

1. **Sequential File Organization:**
    - Records are stored in a specific order (usually sorted).
    - Efficient for batch processing, not ideal for frequent access.
2. **Indexed File Organization:**
    - An index is used to quickly access records.
    - Similar to a book index with page numbers.
    - Often used in **index-sequential files**.
3. **Relative (Random) File Organization:**
    - Records are stored at specific locations using a hashing technique.
    - Accessed directly via a key value.
4. **Direct File Organization:**
    - A subset of relative organization with direct access using hash keys.

---

#### **File Types:**

- **Simple File:** Basic structure, straightforward storage.
- **Clustered File:** Multiple related records stored together to optimize access.