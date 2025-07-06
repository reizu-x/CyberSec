# Detection Notes

## SQL Injection

- Inserting or injecting malicious SQL statements
- Manipulate expected database queries
    - Retrieve sensitive information
    - Extract hashed passwords
    - Bypass authentication logic
- Look for SQL Keywords
    - SELECT
    - FROM
    - WHERE
    - UNION
- Look for injection characters
    - Single/Double quotes, semi colons, comment indicators (dashes)

### SQL Injection Characters

| Character    | Normal Character | URL-Encoded Character |   
| ------------ | ---------------- | --------------------- |
| Single Quote | '                | %27                   |
| Double Quote | "                | %22                   |
| Space        |                  | %20                   |
| Semicolon    | ;                | %3B                   |
| Dash         | -                | %2D                   |

## Data Queries

`Select`
: Retrieve data from a database table

`From`
: Specifies the table to retrieve data from

`Where`
: Filter records based on conditions

`Order by`
: Sort the results (ascending or descending)

`Group by`
: Group rows with identical values into summaries

## Data Manipulation

`Insert into`
: Adds new rows of data into a table

`Update`
: Modifies existing data in a table

`Delete`
: Removes existing rows from a table

`Drop`
: Deletes a table or database from the system

`Join`
: Combines rows from two or more tables based on a column

`Inner Join`
: Returns records that have matching values in multiple tables

`Union`
: Combines the results of two or more SELECT statements

### Comparative Operations

`Like`
: Searches for a specific pattern in a column

`IN`
: Checks if a value matches any value in a list or a query

## Cross-Site Scripting

- Executing malicious code by injection JavaScript
    - Hijack user sessions
    - Steal Cookies
    - Deface websites
- Look for ```<script>``` tag indicators
- Look for event handlers
    - Onload, Onclick, Onmouseover
- Special Characters
    - <, >, ", ', &, %, ;
- URL-Encoded injection characters

## Command Injection

- Executing arbitary OS commands
    - ; , | | , &&
- Look for references to commands or utilities
    - ls, echo, bash, cat, cd, cmd.exe, curl, wget
    - ping, sudo, chmod, rm, nc.exe, sh

## Path Traversal / Local File Inclusion

- Accesing files outside of the web root
    - Include or execute uninetended files/scripts
- Path Traversal
    - Access files/directories outside of the web root
    - Enumerate the system, read hardcoded credentials
- Local File inclusion (LFI)
    - Include a local file from the system  
    - Enumerate the system, read hardcoded credentials
    - Execute scripts / remote code execution
- Look for path traversal sequences
    - URL-Encoded characters
- Look for sensitive file paths
