---

layout: col-sidebar
title: OWASP Damn Vulnerable Thick Client Application
tags: DVTA DVTA2.0
level: 1
type: other
pitch: A Vulnerable Thick Client Application developed using C# to demonstrate vulnerabilities in legacy 2-tier applications.

---

# DVTA 2.0 

(Requires .NET version 4.5)

Damn Vulnerable Thick Client Application (DVTA) is a Vulnerable Thick Client Application developed in C# .NET

## Some of the vulnerabilities covered in this Application:

1. Insecure local data storage
2. Insecure logging
3. Weak cryptography
4. Lack of code obfuscation
5. Exposed decryption logic
6. SQL Injection
7. CSV Injection
8. Sensitive data in memory
9. DLL Hijacking
10. Clear text data in transit
11. Client side protection bypasses using Reverse Engineering

## Usage:
- Get the compiled binary from releases. Alternatively, clone the project and compile from the source.

- Set up SQL Server and FTP Server - instructions shown here https://youtu.be/rx8mtI1HU5c

- Queries used in the video:

    - QUERY TO CREATE "USERS" TABLE:

    CREATE TABLE "users" ( "id" INT IDENTITY(0,1) NOT NULL, "username" VARCHAR(100) NOT NULL, "password" VARCHAR(100) NOT NULL, "email" VARCHAR(100) NULL DEFAULT NULL, "isadmin" INT NULL DEFAULT '0', PRIMARY KEY ("id") )

    - QUERY TO INSERT DATA INTO "USERS" TABLE:

    INSERT INTO dbo.users (username, password, email, isadmin) VALUES ('admin','admin123','admin@damnvulnerablethickclientapp.com',1), ('rebecca','rebecca','rebecca@test.com',0), ('raymond','raymond','raymond@test.com',0);

    - QUERY TO CREATE "EXPENSES" TABLE:

    CREATE TABLE "expenses" ( "id" INT IDENTITY(0,1) NOT NULL, "email" VARCHAR(100) NOT NULL, "item" VARCHAR(100) NOT NULL, "price" VARCHAR(100) NOT NULL, "date" VARCHAR(100) NOT NULL, "time" VARCHAR(100) NULL DEFAULT NULL, PRIMARY KEY ("id") )

- Configure the client application to communicate with SQL Server and FTP Server - Instructions shown here https://youtu.be/IBdk2uOessc

- Explore and exploit
