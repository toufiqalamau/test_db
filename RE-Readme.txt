I feel that adding a few things as explanation will help a lot to the novices such as myself.
When we download the zip file of test_db, and if I am using windows, I should know exactly where I am downloading the file and subsequently where I am unzipping the whole folder.
Next, find the employees.sql file and then look for the word "source". This word tells your server to find the ".dump" files. You can edit the '.sql' files with any text editor. I used "WordPad" on Windows 10 and it works just fine.
Now, after the word "source" you must typein or copy-paste the address of the folder you have unzipped your test_db files in. For example, in my case it was "D:/reading items/FE resources/Programming books/sql/test_db-master/test_db-master/". Now, you must remember to notice the "/". Usually when you open windows explorer and single click on the address bar you will get something like this "D:\reading items\FE resources\Programming books\sql\test_db-master\test_db-master". Here, notice the "\". So, all you have to do is to change the "\" to "/".
Now, change the location for all "source" words in the file.
Next, fire up the mysql shell.
type the following commands:

mysql>show databases;

Create a new schema called employees if it is not already there. Or, in fact you can name the schema 'test_db' or anything you wish.

mysql> create schema employees;

mysql> use employees; [This command will start using the schema/database 'employees']

Next, you will need to run the 'employee.sql' file. I will type in what I used.

mysql> source D:/reading items/FE resources/Programming books/sql/test_db-master/test_db-master/employees.sql;

Now, sit back and wait as the sql script is being run and the database being populated.

When, everything is done, you can use the database to test your sql command skills.

Enjoy!!!