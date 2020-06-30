LAB 3.1 -> Importing RDBMS Data into HDFS
Following are the steps to be performed in this lab:-
step1.Create an Amazon RDS database.
step2.Connect this database with MySQL Workbench.
step3.Now create a new salaries table using following sql command.
    create table salaries 
    (
        gender varchar(1),
        age int,
        salary double,
        zipcode int
    );
step4. Load the data given in salaries.txt file into this salaries table using following sql command
load data infile '/salaries.txt' into table salaries fields terminated by ',' ;
[Note] -> If you get an infile error while inserting the data follow below steps:-
 *  Close current SQL connection
 *  Right click on your Connection and select 'Edit Connection'
 *  Click on Advanced
 *  Add following line to 'Others'
         OPT_LOCAL_INFILE=1
 * Now Reconnect to your database
step5. Now, ssh to your EMR cluster and make sure Sqoop is pre installed in this cluster.
step6. Run sqoop import command to import data from sql database to hdfs.
![1](https://user-images.githubusercontent.com/63596198/86156482-a681df00-bb23-11ea-8b33-bddba977db4e.PNG)
step7. Now check whether salaries directory is created on hdfs with 5 files present as shown below
![2](https://user-images.githubusercontent.com/63596198/86156670-f2cd1f00-bb23-11ea-9617-4062588371a9.PNG)
step8. To verify whether data is present in these file use cat command
![3](https://user-images.githubusercontent.com/63596198/86156784-1c864600-bb24-11ea-8333-67204055b087.PNG)
step9.Now we will import only salary and age data from the database and put it into new directory named salaries2
![4](https://user-images.githubusercontent.com/63596198/86156928-45a6d680-bb24-11ea-8aaa-16ce1742907f.PNG)
step10.Now check whether salaries2 directory is created on hdfs with 2 files present as shown below
![5](https://user-images.githubusercontent.com/63596198/86157018-68d18600-bb24-11ea-8afe-d615b77ddc9b.PNG)
step11.To verify whether data is present in this file use cat command
![6](https://user-images.githubusercontent.com/63596198/86157113-8868ae80-bb24-11ea-9ef8-2820e4425070.PNG)
step12.Now we will use --split-by command to split our data accoring to a certain column value and put it into new directory named salaries3
![7](https://user-images.githubusercontent.com/63596198/86157172-a1715f80-bb24-11ea-87d2-f14711893971.PNG)
step13.Now check whether salaries3 directory is created on hdfs with 3 files present as shown below
![8](https://user-images.githubusercontent.com/63596198/86157258-c1088800-bb24-11ea-8374-f5d2feeb4900.PNG)
step14.To verify whether data is present in this file use cat command
![9](https://user-images.githubusercontent.com/63596198/86157318-d67db200-bb24-11ea-81f1-d9a9416f9575.PNG)








