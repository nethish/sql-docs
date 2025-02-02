---
title: "Result-Generating and Result-Free Statements"
description: "Result-Generating and Result-Free Statements"
author: David-Engel
ms.author: v-davidengel
ms.date: "01/19/2017"
ms.service: sql
ms.subservice: connectivity
ms.topic: reference
helpviewer_keywords:
  - "result-generating statements [ODBC]"
  - "batches [ODBC], result-generating statements"
  - "batches [ODBC], result-free statements"
  - "SQL statements [ODBC], batches"
  - "result-free statements [ODBC]"
---
# Result-Generating and Result-Free Statements
SQL statements can be loosely divided into the following five categories:  
  
-   **Result Set-Generating Statements** These are SQL statements that generate a result set. For example, a **SELECT** statement.  
  
-   **Row Count-Generating Statements** These are SQL statements that generate a count of affected rows. For example, an **UPDATE** or **DELETE** statement.  
  
-   **Data Definition Language (DDL) Statements** These are SQL statements that modify the structure of the database. For example, **CREATE TABLE** or **DROP INDEX**.  
  
-   **Context-Changing Statements** These are SQL statements that change the context of a database. For example, the **USE** and **SET** statements in SQL Server.  
  
-   **Administrative Statements** These are SQL statements used for administrative purposes in a database. For example, **GRANT** and **REVOKE**.  
  
 SQL statements in the first two categories are collectively known as *result-generating statements*. SQL statements in the latter three categories are collectively known as *result-free statements*. ODBC defines the semantics of batches that include only result-generating statements. These semantics vary widely and are therefore data source-specific. For example, the SQL Server driver does not support dropping an object and then referring to or re-creating the same object in the same batch. Therefore, the term *batch* as used in this manual refers only to batches of result-generating statements.
