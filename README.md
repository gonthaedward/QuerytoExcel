![image](https://github.com/user-attachments/assets/1936e894-499f-433e-b3cf-cbcbed2c9606)![image](https://github.com/user-attachments/assets/abefc51a-dc8e-4cd1-af75-b9d188260946)# QuerytoExcel
Application to retrieve data from mysql into excel

Installation consist of 2 ways: 
- htdocs from XAMPP
- run .bat file

**htdocs from XAMPP: **

##how to install: 

- Download XAMPP (this app is using XAMPP for PHP ver. 7.4.33 but any version is ok) [https://www.apachefriends.org/download.html]
- Install XAMPP
- Download .zip from this page
- Move folder to htdocs in xampp (if you are installing xampp without customization the path of htdocs would be: **C:\xampp\htdocs**)
![image](https://github.com/user-attachments/assets/0b8ec6e8-f864-4286-bbad-1ecf35d97648)

- open XAMPP and run apache

![image](https://github.com/user-attachments/assets/e66ff762-040f-4a32-bf6e-7b1fba28f5d2)

- open http://localhost/querytoexcel/run.php


Note: You might get below error if you open it right away: 

![image](https://github.com/user-attachments/assets/01973c19-bed4-4bb7-96a4-fe96dfd22827)

To fix it you have to 
- open the folder QuerytoExcel on htdocs
- right click "run.php" and run it on Notepad, Notepad++, or Visual Studio Code
- update the part where there is comment "//database" into database you wanted to query

**run .bat file**
There is .bat file inside the zip, it can be used to run the application automatically by only double clicking it. 

![image](https://github.com/user-attachments/assets/57483c8c-4381-4c62-af31-02c0d7d7a602)

you can right click "run.bat" and run it on Notepad, Notepad++, or Visual Studio Code

the format i used in here is : 

path\to\php.exe path\to\run.php

example below is in run.bat

C:\xampp\php\php.exe C:\xampp\htdocs\Querytoexcel\run.php

This means the php.exe is in c:xampp\php\php.exe and will run the php in c:\xampp\htdocs\querytoexcel\run.php


For both of type there are some point you have to update it to run as you want: 

- $query: this is a query that will be used to get the data. [Make sure the query is using MYSQL and starting with SELECT and also LIMIT 10000 maximum so it will not trigger timeout]
- $saveDirectory : this is a path that will be used to save your data. 
[this is example of the save directory update into htdocs:
from:
    $saveDirectory = 'C:\\Users\\Eda\\Downloads';

to
    $saveDirectory = 'C:\\xampp\\htdocs\\QuerytoExcel';
]













