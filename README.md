# Laragon-MySQL-8-Upgrade-Instructions
Laragon MySQL 8 Upgrade Instructions


These are the exact instructions to upgrade MySQL to version 8 on Largon v.4.0.16 on Windows 10 1909 x64. If you have already ran Mysql in Laragon you can skip to step 3.

BACK UP YOUR DATA FILE BEFORE YOU DO ANYTHING!

1- Install Laragon

2- Click Start All. This will create the mysql folder and files at C:\laragon\data\mysql

3- Stop Laragon.

4- Go to Quick Add Configuration (Menu->Tools->Quick add->Configuration)

5- Uncomment the mysql-8.0 (Line 12, delete # sign)

6- Edit the mysql version to current version. (Change mysql-8.0.13-winx64.zip TO mysql-8.0.25-winx64.zip )

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


#upgrade to mysql 8 second way:

I would like to share My solution for this I used 64bit version and its in my PC "D" drive with no mysql root password

1.Install c++ redistribution package from Microsoft site "VC_redist.x64.exe"

1- Download mysql8.0.x-winx64.zip archive

2- Extract to "D:\laragon\bin\mysql" directory change drive letter accordingly

3- Stop laragon and and select mysql8.0-winx64 version from Laragon Menu ->version->mysql-8.0.x-win64

4- Now start the Service wait for few seconds to allow initialization

5- Stop mysql server go to directory "D:\laragon\bin\mysql\mysql-8.0.x-winx64\bin" run "mysqld stop" this will stop sql

6- Go to "D:\laragon\data" rename existing "mysql-8" folder to mysql.bk and rename "mysql" folder to mysql-8

7- Stop Laragon and restart it again

if you're still getting an error continue. other wise it's finish. :)

8- open cmd.exe as Administrator

9- go to directory "D:\laragon\bin\mysql\mysql-8.0.x-winx64" run "mysql_upgrade.exe -u root -p" I didnt have password so i left it blank after -p

Click Enter without password when prompted Wait for Few minutes to allow mysql do the upgrade

10- now go to mysql terminal from Laragon enter comand "mysql -u root -p" Click Enter without password

11- Now enter the following comand "ALTER USER 'root'@'localhost' IDENTIFIED BY 'NewPassword';" replace NewPassword with your own one

12- Now Restart Laragon again


