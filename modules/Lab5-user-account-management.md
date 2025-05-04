# 5 File Contents and Comparing (Isi File dan perbandingannya)

- [x] 1. Creating a New User  
- [ ] 2. Creating a User with a Home Directory  
- [ ] 3. Setting a User Password  
- [ ] 4. Modifying User Properties  
- [ ] 5. Changing User Shell  
- [ ] 6. Adding a User to a Group  
- [ ] 7. Locking and Unlocking User Accounts 
- [ ] 8. Deleting a User  


 Pada praktikum kali ini akan di pandu untuk mempelajari 'dasar manajemen akun pengguna' di sistem lilux. Anda akan belajar membuat, mengubah dan menghapus user akun, serta mengatur dan mengubah katasandi. Ini adalah ketrampilan dasar untuk sistem administrasi linux.
 
 
 - [x] 1. Creating a New User (membuat user baru)
Let's start by creating a new user account named "joker".  membuat user dengan nama "joker"
```
sudo useradd joker
```  

Let's break this down:  

`sudo` is a command that gives you temporary superuser (administrator) privileges. We use it because creating a new user requires these higher-level permissions.  
`useradd` is the command to create a new user. (`useradd` merupakan perintah untuk membuat satu pengguna baru)  
`joker` is the username we're creating. (`joker` merupakan username yang kita buat)  
Note: If you try to run this command without `sudo`, you'll get a "permission denied" error. This is because regular users aren't allowed to create new user accounts - it's a task reserved for system administrators.  
Catatan: jika kamu mencoba menjalankan tanpa `sudo`, kamu akan menerima pesan error "permission denied". Hal ini karena user biasa tidak diizinkan untuk membuat akun pengguna baru - ini merupakan tugas untuk administrator sistem.  

This highlights the difference between a superuser and a common user. As a common user(sebagai pengguna biasa), you can't create new user accounts (kamu tidak dapat membuat akun user baru), but by using sudo (tapi dengan menggunakan `sudo`), you can temporarily elevate your privileges to perform this administrative task. (untuk sementara kamu dapat menjalankan hak istimewa untuk menjalankan tugas administrator)  

  |![Debian Tree](https://prnt.sc/IPFllXqiYHkG)|
This line shows:

Username: joker
Password: x (the actual password is stored securely elsewhere)
User ID: 5001
Group ID: 5001
Home Directory: /home/joker, but it hasn't been created yet
Default Shell: /bin/sh
  
  - [x] Changing User Shell (mengubah 
sudo usermod -s /bin/bash joker

  - [ ]   Summary
Congratulations! You've completed the Linux User Account Management lab. You've learned how to:

Create new user accounts
Set user passwords
Modify user properties like home directory and default shell
Add users to groups
Lock and unlock user accounts
Delete user accounts
You've also been introduced to important Linux concepts like the /etc/passwd file, home directories, shells, and user groups. These are fundamental skills for Linux system administration. Remember, in real-world scenarios, always follow your organization's security policies when managing user accounts
