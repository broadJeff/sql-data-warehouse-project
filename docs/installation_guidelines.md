## Installation and Set UP Guide:

### Introduction:
We will use MS SQL for the sql-data-warehouse-project. In order to use MS SQL, we will have to install:
1. SQL Server Management Studio (SSMS)
2. MS SQL Server 2022


### MS SQL Server installation:

For this project we will install the MS SQL 2022 using docker install instead of the local machine.
I am using the below command to install a MS SQL 2022 docker image.

docker run -e "ACCEPT_EULA=Y"\
-e "MSSQL_SA_PASSWORD={{{sa_password}}" \
-e "MSSQL_PID=Developer" \
-p 1433:1433 \
--name sql2022 \
-v sql2022_data:/var/opt/mssql \
-d mcr.microsoft.com/mssql/server:2022-latest

```
- I have named the docker container as sql2022
- So we can just use the command docker run sql2022 when we would to start it.
- Use docker stop sql2022 to stop it.
```


### SQL Server Management Studio (SSMS)
To install SSMS, please follow the instructions in the below link:  
https://learn.microsoft.com/en-us/ssms/install/install


### Connect the sql2022 docker container to SSMS:

Make sure to have the below config and then click on "Connect:

<img width="612" height="747" alt="image" src="https://github.com/user-attachments/assets/4d816a3d-352a-4573-8382-edcc55dcc624" />



