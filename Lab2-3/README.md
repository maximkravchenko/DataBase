
<h1 align="center">LAB2-3</h1> <div align="center"> <p> <span><strong> Creating a relational data schema |</strong></span> <span> Bank</span> </p> </div>

----------

In this laboratory work, the ER-model of the "Bank" database developed earlier was transformed into a relational data schema using PostgreSQL.  
The main goal was to translate conceptual entities, attributes, and relationships into relational tables, taking into account normalization rules, integrity constraints, and the implementation of different types of relationships (1:1, 1:M, M:M).

While working on the project, I gained practical experience in solving such tasks as:

1.  Converting entities and attributes of the ER-diagram into relational tables and columns.
2.  Defining **primary keys** and **foreign keys**.
3.  Implementing relationships, including "many-to-many", through intermediate tables.
4.  Applying normalization techniques to avoid redundancy and ensure consistency.
5.  Using **pgAdmin 4** as a graphical tool for automated transformation and SQL generation.
    

## Stages of development:

1.  #### Entities and tables defined for the Bank model:
    
    -   **User** – client of the bank (id, email, phone, type, registration date, passport_id).
    -   **Passport** – passport data (id, number, full name, issue date, issued by, address_id, country_id).
    -   **Address** – address details (id, city, street, house number, postal code).
    -   **Bill** – bank account (id, number, balance, currency, opening date, user_id).
    -   **Transaction** – transaction details (id, amount, currency, date, time, status, bill_id, user_id).
    -   **Bank_Branch** – bank branch (id, name, phone, working hours, manager, address_id).
    -   **Position** – employee position (id, name, responsibilities, required experience, max salary).
    -   **Bank_Employee** – employee of the bank (id, salary, schedule, hire date, work period, department, passport_id, bank_branch_id).
    -   **Country** – country details (id, name, region, code, language).
        
    Additional intermediate tables for M:M relations:
    
    -   **Employee_Position** – links employees with positions (employee_id, position_id, start_date, end_date).
    -   **Employee_Branch** – links employees with branches (employee_id, branch_id, start_date, end_date).
        
2.  #### Types of relationships:
    
    -   User → Passport (1:1)
    -   Bank_Employee → Passport (1:1)
    -   Passport → Country (M:1)
    -   Passport → Address (M:1)
    -   Bank_Employee → Position (M:M, via Employee_Position)
    -   Bank_Employee → Bank_Branch (M:M, via Employee_Branch)
    -   Bank_Branch → Address (1:1)
    -   User → Bill (1:M)
    -   Bill → Transaction (1:M)
    -   User → Transaction (1:M)
        
3.  #### Paper-based relational transformation:
    
    -   ER-model entities were converted into relational tables.
    -   Attributes became columns, and unique attributes became primary keys.
    -   One-to-many relations were implemented with foreign keys.
    -   Many-to-many relations were implemented using intermediate tables.
    -   UML diagrams and mapping between ER and relational models were created.
        
4.  #### Automated transformation with pgAdmin:
    
    -   The ERD tool in **pgAdmin 4** was used.
    -   Tables were created visually, then SQL code was generated.
    -   SQL scripts created the relational schema in PostgreSQL.
    -   Tables, primary keys, foreign keys, and relationships were verified.
        

----------

## Conclusion

As a result of this laboratory work, the ER-model "Bank" was successfully transformed into a relational data schema using PostgreSQL. Tables were created for all entities, primary and foreign keys were defined, and relationships (1:1, 1:M, M:M) were implemented. Both "paper-based" and "automated" approaches were applied, which allowed for a deeper understanding of the design and verification process.

The resulting relational schema can now be used for building the **Bank database** in PostgreSQL, ensuring efficient storage and processing of client, employee, account, and transaction data, ultimately improving the quality of banking services.