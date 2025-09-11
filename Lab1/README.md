
<h1 align="center">LAB1</h1>

<div align="center">
  <p>
    <span><strong> ER-diagram |</strong></span>
    <span> Bank</span>
  </p>
</div>

---

In this laboratory, a conceptual design of the database is performed using the ER model of data representation (the "entity-relationship" model). 
In the course of the work, an ER data model was developed for the Bank's database, taking into account the semantic limitations of a given subject area.

While  working  on the project, I  gained  practical  experience  in  solving  such  tasks  as: 1.  Analysis  and  modeling of business  processes in the subject  area  (using the  example of a bank).  2.  Designing the database  structure  from  scratch  and  forming an ER  diagram.  3.  Definition of entities,  attributes, and  relationships of various  capacities  (1:1,  1:M,  M:M).  4.  Developing a data  model taking into account the limitations of integrity  and  extensibility;

## Stages of development:
 1. ####  Entities were allocated for the bank model:
	 - Bank  branch  
	 - Address 
	 - Сountry  
	 - Passport  
	 - Employee  
	 - Position
	 - Client  
	 - Bill  
	 - Transaction
	 
 2. ####  Attributes have been  selected  for  each  entity:
	  - <b>Bank branch</b> - Each branch has a unique <u><em>name</em></u> that allows it to be identified. The department's contact details are recorded, such as <u><em>phone number</em></u>. The <u><em>opening hours</em></u> of the branch are indicated for the convenience of customers. Information about <u><em>the branch manager</em></u> is saved.
	 - <b>Address</b> - Each address includes the <u><em>city</em></u> in which the customer or the bank branch is located. The data about the <u><em>street</em></u> where the object is located is saved. The <u><em>house number</em></u> associated with the address is recorded. It is specified <u><em>postal code</em></u> to accurately identify the location.
	 - <b>Country</b> - each country has a unique <u><em>name</em></u>. The country's location <u><em>region</em></u> is recorded for additional classification. The system stores the <u><em>international country code</em></u>. The <u><em>official language</em></u> used in the country is indicated.
	 - <b>Passport</b> - Contains a <u><em>unique number</em></u> that is used to identify the client. The client's personal data is indicated, such as <u><em>first name, last name and patronymic</em></u>
	 - <b>Employee</b> - Has a <u><em>registration date</em></u> for a job at the bank, which is recorded in the system. The employee's current <u><em>salary</em></u> is recorded. The <u><em>work schedule</em></u> is displayed, which determines the employee's schedule. The <u><em>department</em></u> in which the employee works is indicated
	 - <b>Position</b> - Each position has a unique <u><em>name</em></u>. The list of responsibilities associated with this position is retained. The minimum <u><em>required experience</em></u> for holding this position is fixed. The <u><em>maximum salary</em></u> available for this position is indicated.
	 - <b>Client </b> - Stores contact information such as <u><em>email</em></u> and <u><em>phone number</em></u>. The user's registration date is indicated in the bank. The <u><em>type</em></u> of the user <u><em>for example, an individual or a legal entity</em></u> is also stored in the database
	- <b>Bill </b>- Each bill has a unique <u><em>number</em></u>. The current <u><em>balance</em></u> is recorded on the account, which displays the status of the client's funds. It is indicated <u><em>the currency of the account</em></u> in which the funds are stored. It is fixed <u><em>the account opening date</em></u>. 
	 - <b>Transaction</b> - each transaction has <u><em>the amount of the transaction</em></u> that was carried out between the accounts. The <u><em>currency</em></u> in which the operation was performed is fixed. For each transaction, the date and time of its execution are stored. The <u><em>operation status</em></u> is displayed, such as "completed", "cancelled" or "in processing".
	 
 3. #### Let's define the types of communication for entities:
	 - Client -> Passport (OtO)
	 - Client -> Bill (OtO)
	 - Client -> Transaction (OtM)
	 - Passport -> Country (MtO)
	 - Passport -> Address (OtM)
	 - Transaction -> Bill (MtO)
	 - Address -> Bank  branch (OtO)
	 - Employee -> Bank  branch (MtM)
	 - Employee -> Position (MtM)
	 - Employee -> Passport (OtO)
	 
 	---
 Based on this path, an ER diagram was developed, which has the designation ER-diagramm_Bank and is in this catalog in pdf format.  
	 
