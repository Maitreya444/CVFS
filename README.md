1. Programming language used :
   To develope this project we select C programming as it is a Native Programming language.
2. OS used :
   As this project executes on a primary storage i.e RAM there is no special requirement of an OS.
3. Description :
   This project is a virtual representation of file system. File system is considered as the way of storing information about files and data from the files into the 
   secondary storage device.
   Every OS has its own type of filesystem such as NTFS, FAT32, UFS, etc.
   In this project we implement the layout of complete filesystem, hardisk, RAM.
   In this project we implement almost every related system call used in the file manipulation activity along with some important commands.
   This is a research based project.
   We develope this project to understand internals of data structures implementation of C programming.
4. File System Layout :
    ![Data Structures of File System](https://github.com/user-attachments/assets/12a29903-fcf2-404c-ba42-6f5c25e83f09)
    1. Boot block :
       It's a block of 1 kb size which contains the information used to start the OS.
       When we press the  power ON button of the laptop or desktop the code from the boot block gets executed.
    2. Super block :
       It is a block of 1 kb size which contains information about whole file system.
       This block contains the information about total number of INODES, used INODES, free INODES, total number of blocks, free blocks, used blocks etc.
    3. Disk INODE list block (DILB) :
       It is a linked list of INODES, INODE is considered as a structure which contains the information about the file.
       For every file there is a seperate INODE, OS will access the file by considering the contents stored inside an INODE.
       INODE contains below things in it :
       1. INODE number
       2. Name of file
       3. Size of file (Allocated memory)
       4. Actual size of file (size of data)
       5. Permissions of file
       6. Last access and modification time
       7. Link count
       8. Block number allocated to the file, etc.
     4. Data Block :
        This is one of the biggest section in a file system.
        The data block contains actual data that we store inside the file.
        Each block from the data block is of 1 kb size.
        Inside the data block there is no information about the file.
        This concept of filesystem is applicable in any type of OS.
        All the above information is related to hardisk only.
