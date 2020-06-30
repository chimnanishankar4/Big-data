LAB 3.2 -> Exporting HDFS Data to an RDBMS
Objective -> Export data from HDFS into a MySQL table using Sqoop.
Following are the steps to be performed in this lab:-
step1.Create a new hdfs directory using mkdir command with name salarydata
![10](https://user-images.githubusercontent.com/63596198/86158290-358ff680-bb26-11ea-9516-974d8054616f.PNG)
step2.Put salarydata.txt into the salarydata directory in HDFS
![11](https://user-images.githubusercontent.com/63596198/86158444-6839ef00-bb26-11ea-8bb2-2ac0be1a1deb.PNG)
step3.Check whether the file is created on hdfs
![12](https://user-images.githubusercontent.com/63596198/86158544-8bfd3500-bb26-11ea-9195-07a51971dd4b.PNG)
step4.Create a new Table in the Database as salaries2 using following sql command
create table salaries2 ( gender varchar(1), age int, salary double, zipcode int);
step5.Now export data from hdfs to databaseCreate a new Table in the Database as salaries2 using following sql command
![13](https://user-images.githubusercontent.com/63596198/86158665-bd760080-bb26-11ea-942a-b7483bc33021.PNG)





