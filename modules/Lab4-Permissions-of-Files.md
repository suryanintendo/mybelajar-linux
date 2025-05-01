# 4 Permissions-of-Files
- [x] 1. Examining File Contents  (Memeriksa isi file)
- [ ] 2. Comparing the Files ( membandingkan file)


      
Introduction  
In this lab (pada praktikum ini), we'll dive (kita akan mendalami) into the world of file permissions in Linux (ke dunia perizinan file di linux). We'll explore (kita akan menjelajahi) three essential commands (3 perintah penting): `chown`, `touch`, and `chmod`. These tools are crucial (Alat-alat ini penting) for managing access to files and directories (untuk mengelola aksess ke file dan direktori) on a Linux system (pada sistem linux). By the end of this lab (pada akhir dari praktikum ini), you'll have (kamu akan memiliki) a solid grasp on (pemahaman yang kuat) creating files (membuat file), changing file ownership (mengubah kepemilikan file), and modifying file permissions (dan memodifikasi hak aksess file).  
Understanding (memahami) these commands will (perintah perintah ini akan) empower you to control (memberdayakan anda untuk mengontrol) who can read, write siapa yang dapat membaca, menulis , and execute files on your system (dan menjalankan file pada sistem anda).

Achievements (pencapaian)  
After completing this lab, you'll be able to:  (setelah menyelesaikan praktikum ini, anda akan dapat untuk:)  

1. Use `chmod` to modify file permissions  (menggunakan `chmod` untuk memodifikasi hak aksess file)  
2. Use `chown` to change file ownership (menggunakan `chown` untuk mengganti kepemilikan file)  
3. Use `touch` to create new files and update timestamps of existing files (dapat membuat file baru dari file yang ada)  


- [x] 1. Examining File Contents  (Memeriksa isi file)  
The `ls -l` command (list with long format) provides detailed (menyediakan secara rinci) information about the file (informasi tentang file tersebut), including its (termasuk kategori berikut ini) __permissions, owner, and group__.

```
sudo chown root:root example.txt
```
Here's what this command does: (inilah penjelasan perintah tersebut)

`sudo` runs the command (menjalankan perintah) with root privileges (dengan hak aksess `root`). You'll likely be prompted for your password (anda munkin akan di minta sandi). 
`chown` requires elevated privileges because it's a powerful command that can affect system security. Without `sudo`, you'll get a "Permission denied" error.  
`chown` is the command to change ownership.
`root:root` specifies the new owner and group (both set to root). The syntax is owner:group.
`example.txt` is the target file.


If you still see labex instead of root, make sure you used sudo when running the chown command and entered your password correctly.  

  - [ ] Changing the Ownership of a Directory (Mengubah kepemilikan Directori)  
    The chown command can also change the ownership of entire directories and their contents.
Let's see this in action. This is particularly useful for managing complex directory structures where you want to ensure all files and subdirectories have the same owner.
First, let's create a new directory with some files:
```
mkdir -p new-dir/subdir
echo "Hello, world" > new-dir/file1.txt
echo "Another file" > new-dir/subdir/file2.txt
```
  Let's break down these commands:

`mkdir -p new-dir/subdir` creates the new-dir directory and its subdir subdirectory.  
The `-p` option tells (opsi pilihan) `mkdir` to create parent directories as needed (untuk membuat direktori induk sesuai kebutuhan).  
Without (tanpa) `-p`, if `new-dir` didn't exist (jika direktori baru tidak ada), creating new-dir/subdir would fail (akan gagal).  
echo "Hello, world" > new-dir/file1.txt creates a file named file1.txt inside the new-dir directory and writes the text "Hello, world" into it. The > symbol is used for redirection; it takes the output of the echo command and redirects it into the specified file.  
echo "Another file" > new-dir/subdir/file2.txt similarly creates a file named file2.txt inside the `new-dir/subdir` directory and writes the text "Another file" into it.
  
  - [x] Changing the Permissions of a File
        file permissions are represented by a series of letters or numbers. Let's explore how to read and change these permissions.   
  Understanding permissions is vital for securing your files and preventing unauthorized access.  
First, let's look at the current permissions of our example.txt
```  
ls -l example.txt
```  
  akan atambil seperti ini
```  
-rw-rw-r-- 1 root root 0 Jul 29 15:11 example.txt
```
pada -rw-rw-r-- part represents the file permissions. This is where the numeric and symbolic notations come in. Let's break it down:  

1. The first character (-) indicates this is a regular file. Other common indicators are d for directory and l for symbolic link.  
2. The next three characters (rw-) represent the owner's permissions (read and write, but not execute).  
  - r stands for read permission: The owner can open and read the file.  
  - w stands for write permission: The owner can modify the file.  
  - x stands for execute permission: The owner can run the file (if it's a program or script). A - means the permission is denied.  
3. The next three (rw-) are for the group. They have the same meaning as above, but apply to members of the file's group.  
4. The last three (r--) are for others (everyone else). They also have the same meaning, but apply to users who are neither the owner nor members of the file's group.  
 Kode :  
4: Read permission  
2: Write permission   
1: Execute permission    
0: No permission   

  
Now, let's change these permissions using the chmod command. chmod stands for "change mode," and it allows you to modify these permissions.   
```  
sudo chmod 700 example.txt
```  
In this command:  

700 is a numeric representation of permissions:  
The first digit (7) represents the owner's permissions.  
The second digit (0) represents the group's permissions.  
The third digit (0) represents the others' permissions.  
Each digit is a number from 0 to 7, calculated by adding the values for read (4), write (2), and execute (1) permissions:  

4: Read permission  
2: Write permission  
1: Execute permission  
0: No permission  
So, 7 (first digit) gives the owner read (4), write (2), and execute (1) permissions: 4+2+1=7  
0 (second digit) gives the group no permissions (0+0+0=0).  
0 (third digit) gives others no permissions (0+0+0=0).  

Therefore, 700 means: Owner: read, write, execute. Group: none. Others: none.  

```
-rwx------ 1 root root 0 Jul 29 15:11 example.txt
```  
  
  - [ ]   Changing the Permissions of a Directory
          Changing permissions for directories works similarly to changing permissions for files. Let's practice by creating a new directory and modifying its permissions. Directory permissions control who can list the directory's contents, create new files within the directory, and access files already in the directory.  
          Buat:
       ```
      mkdir ~/test-dir
      chmod 700 ~/test-dir
       ```
       tampilkan dengan
      ```
      ls -ld ~/test-dir
      ```
        
       The -d option in ls -l tells ls to list the directory itself, rather than its contents. Without -d, ls would list the files and subdirectories inside test-dir, which is empty right now. You should see:  
      ```
      drwx------ 2 labex labex 4096 Jul 29 15:45 /home/labex/test-dir
      ```  
      The d at the beginning indicates that it's a directory. The rwx------ indicates that the owner has read, write, and execute permissions, while the group and others have no permissions. For directories:

      Read permission (r) allows you to list the contents of the directory using ls.  
      Write permission (w) allows you to create new files and subdirectories within the directory.  
      Execute permission (x) allows you to access files and subdirectories within the directory (i.e., cd into it).  
  
    Sekarang ubah - Now, let's change the permissions:
    ```
    chmod -R 755 ~/test-dir
    ```
    In this command:

    -R applies the change recursively to all files and subdirectories (though our directory is empty in this case). It's good practice to include it when dealing with directories, even if they're currently empty, in case you add files later.
    755 gives read, write, and execute permissions to the owner, and read and execute permissions to group and others.  
    Let's break down 755:  

    Owner (7): Read (4) + Write (2) + Execute (1) = 7  
    Group (5): Read (4) + Execute (1) = 5  
    Others (5): Read (4) + Execute (1) = 5  

    Jika dipanggil dengan `ls -ld ~/test-dir` akan tampil :
    ```
      drwxr-xr-x 2 labex labex 4096 Jul 29 15:45 /home/labex/test-dir
    ```
    This clearly shows the change in permissions,
    from only the owner having access (700) to the owner having full access while others can read and execute (755).  
    Now, anyone can list the contents of test-dir and access files within it, but only the owner can create new files or modify existing ones.  


#   Using Symbolic Notation for Permissions

- [ ] 2. Comparing the Files (tampilkan ini konten dengan nomor baris)  
