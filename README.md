# Laragon-MySQL-8-Upgrade-Instructions
Laragon MySQL 8 Upgrade Instructions


These are the exact instructions to upgrade MySQL to version 8 on Largon v.4.0.16 on Windows 10 1909 x64. If you have already ran Mysql in Laragon you can skip to step 3.

BACK UP YOUR DATA FILE BEFORE YOU DO ANYTHING!

1- Install Laragon

2- Click Start All. This will create the mysql folder and files at C:\laragon\data\mysql

3- Stop Laragon.

4- Go to Quick Add Configuration (Menu->Tools->Quick add->Configuration)

5- Uncomment the mysql-8.0 (Line 12, delete # sign)

6- Edit the mysql version to current version. (Change mysql-8.0.13-winx64.zip TO mysql-8.0.20-winx64.zip )

7- Save & Close file

8- Go back to Quick Add and select mysql-8.0. Download will start.

9- After download, go to Menu->Mysql->Version and select mysql-8.0.20-winx64

10- Rename C:\laragon\data\mysql to C:\laragon\data\mysql-8 (BACK UP THE mysql FOLDER FIRST!!!!!)

11- Click Start All Button

12- If you get VCRUNTIME140_1 error, install updated Microsoft Visual C++ from https://aka.ms/vs/16/release/vc_redist.x64.exe

13- Stop Laragon.

14- Restart Laragon

15- If Windows Firewall opens give permissions for mysql

16- ALL DONE!

