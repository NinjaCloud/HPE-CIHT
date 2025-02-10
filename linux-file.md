# **Linux File System Lab**

## **Objective**
By the end of this lab, students will understand the Linux file system structure, essential directories, and how to navigate, manage, and manipulate files and directories.

## **Prerequisites**
- Basic knowledge of operating systems
- A Linux-based system (Ubuntu, CentOS, or any distribution)
- Access to a terminal with sudo privileges

---

## **Lab 1: Understanding the Linux File System Structure**
### **Step 1: Explore the Root Directory (`/`)**
1. Open a terminal.
2. Run the following command to list all directories in the root (`/`) file system:
   ```bash
   ls -l /
   ```
3. Observe the standard directories:
   - `/bin` → Essential binaries
   - `/etc` → Configuration files
   - `/home` → User directories
   - `/var` → Log and variable files
   - `/tmp` → Temporary files
   - `/dev` → Device files

### **Step 2: Display the Current Directory**
- Use the `pwd` command to check your current location:
  ```bash
  pwd
  ```

---

## **Lab 2: Navigating the File System**
### **Step 3: Change Directories (`cd`)**
- Move to the `/home` directory:
  ```bash
  cd /home
  ```
- Move back to the root directory:
  ```bash
  cd /
  ```
- Go to your home directory:
  ```bash
  cd ~
  ```
- Move up one directory:
  ```bash
  cd ..
  ```

### **Step 4: List Directory Contents (`ls`)**
- View files and directories in the current directory:
  ```bash
  ls
  ```
- Show detailed information:
  ```bash
  ls -l
  ```
- View hidden files:
  ```bash
  ls -la
  ```

---

## **Lab 3: File and Directory Management**
### **Step 5: Create and Remove Directories (`mkdir`, `rmdir`)**
- Create a new directory:
  ```bash
  mkdir mydir
  ```
- Remove an empty directory:
  ```bash
  rmdir mydir
  ```
- Remove a directory with files:
  ```bash
  rm -r mydir
  ```

### **Step 6: Create and Delete Files (`touch`, `rm`)**
- Create an empty file:
  ```bash
  touch myfile.txt
  ```
- Delete a file:
  ```bash
  rm myfile.txt
  ```

---

## **Lab 4: File Operations**
### **Step 7: Copy and Move Files (`cp`, `mv`)**
- Create a test file:
  ```bash
  touch testfile.txt
  ```
- Copy the file to another location:
  ```bash
  cp testfile.txt /tmp/
  ```
- Move (rename) a file:
  ```bash
  mv testfile.txt newfile.txt
  ```

### **Step 8: View File Contents**
- Use `cat` to view file content:
  ```bash
  cat /etc/os-release
  ```
- Use `less` or `more` for large files:
  ```bash
  less /etc/passwd
  ```
- Use `head` and `tail` to view parts of a file:
  ```bash
  head -5 /etc/passwd
  tail -5 /etc/passwd
  ```

---

## **Lab 5: File Permissions and Ownership**
### **Step 9: Check Permissions**
- Display file permissions:
  ```bash
  ls -l
  ```

### **Step 10: Modify Permissions (`chmod`)**
- Give read, write, and execute permissions:
  ```bash
  chmod 777 myfile.txt
  ```
- Set read and write permissions for the owner only:
  ```bash
  chmod 600 myfile.txt
  ```

### **Step 11: Change Ownership (`chown`)**
- Change file owner:
  ```bash
  sudo chown user:user myfile.txt
  ```

---

## **Lab 6: Disk Usage and File System Information**
### **Step 12: Check Disk Usage (`df`, `du`)**
- View available disk space:
  ```bash
  df -h
  ```
- Check directory size:
  ```bash
  du -sh /var/log
  ```

### **Step 13: Check Mounted File Systems (`mount`, `umount`)**
- View mounted filesystems:
  ```bash
  mount
  ```
- Unmount a USB drive (replace `/dev/sdb1` with the correct device):
  ```bash
  sudo umount /dev/sdb1
  ```

---
