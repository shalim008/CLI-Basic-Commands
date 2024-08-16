1. Search for "SQL Plus" and click
2. RUN "/ as sysdba" - Login as sysdba 
3. RUN "show pdbs"  - Show all database
4. RUN "conn sys/sys@orcl as sysdba" - connect with orcl global database
5. RUN "conn sys/sys@orclpdb as sysdba" - connect with sysdba database
6. TNS configuration -
   Go to your oracle_home folder, in my case "F:\Oracle\Oracle19c_db_home\network\admin"
   Open tnsnames.ora and connection block like in below -

  ORCLPDB =
  (DESCRIPTION =
    (ADDRESS = (PROTOCOL = TCP)(HOST = localhost)(PORT = 1521))
    (CONNECT_DATA =
      (SERVER = DEDICATED)
      (SERVICE_NAME = orclpdb)
    )
  )

7. Let's unlock an existing user to use, because I don't want to use sys user anymore.
   HR default user unlock command -
   
   If you database not open RUN - "ALTER DATABASE OPEN;"

   Then "alter user hr account unlock identified by hr;"
   
6. Create new user - "CREATE USER shalim IDENTIFIED BY shalim;"
7. Assigning Role - "GRANT CONNECT, RESOURCE, DBA TO shalim;"
8. Next you’ll want to ensure the user has privileges to actually connect to the database and create a session using GRANT CREATE SESSION.
   
   "GRANT CREATE SESSION TO shalim WITH ADMIN OPTION;"
   
10. We also need to ensure our new user has disk space allocated in the system -

    "GRANT UNLIMITED TABLESPACE TO shalim;"
