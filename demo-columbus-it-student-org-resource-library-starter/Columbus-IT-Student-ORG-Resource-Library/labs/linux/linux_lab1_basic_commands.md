# Linux Lab 1 – Basic Commands
**Estimated time:** 15–20 minutes  
**Prereqs:** Linux VM (Ubuntu/Debian), terminal access  
**Objective:** Navigate the filesystem and manage files.

## Steps
1. Print current directory  
   ```bash
   pwd
   ```
2. List files (long + hidden)  
   ```bash
   ls -la
   ```
3. Create and remove a folder  
   ```bash
   mkdir demo && cd demo
   touch notes.txt
   rm notes.txt
   cd .. && rmdir demo
   ```
4. Find files by name  
   ```bash
   find ~ -name '*.txt' 2>/dev/null | head
   ```

## Validation
- You can navigate directories and manage files without errors.

## Cleanup
- None.
