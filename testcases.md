# Test Cases - Podman, Trino, Iceberg, Quarkus, and GUI Integration

**Submitted By:**  Pankaj Kumar Pandey  
**Submitted To:** Mr. Vipin Tripathi  
**Test Case Version:**  1
**Reviewer Name:** Ms. Moumita Roy 

## Goal

The goal of this project is to build a fully functional data processing pipeline using Podman, Apache Iceberg, Trino, and Java Quarkus, with a user-friendly GUI for interaction. The setup involves:

    1. Running Apache Iceberg inside a Podman container
    2. Setting up and configuring Trino to query Iceberg
    3. Developing a Java Quarkus application to interact with Iceberg through Trino
    4. Designing a GUI to make the system easy to use

## Test Cases


**Test Case 1 – Verify Podman installation**  
**Scenario:** Ensure Podman is installed correctly.  
**Remark:** Verify Podman version after installation.  
**Given:** A system with Podman installed.  
**When:** The command podman --version is executed.  
**Then:** The Podman version should be displayed.  
**Test Run Date:**  
**Result:** Pending/Pass/Fail  

**Test Case 2 – Verify Iceberg installation inside Podman**  
**Scenario:** Validate Iceberg service deployment.  
**Remark:** Ensure Iceberg starts without errors.  
**Given:** Iceberg is deployed inside a Podman contaner.  
**When:** The container logs are checked.  
**Then:** Iceberg service should start without errors.  
**Test Run Date:**  
**Result:** Pending/Pass/Fail  
 

**Test Case 3 – Check connectivity between Trino and Iceberg**  
**Scenario:** Ensure Trino can query Iceberg tables.  
**Remark:** Trino should execute queries successfully.  
**Given:** A Trino instance connected to Iceberg.  
**When:** The query SELECT * FROM iceberg.default.test_table LIMIT 1; is run.  
**Then:** The query should execute successfully.  
**Test Run Date:**  
**Result:** Pending/Pass/Fail  


**Test Case 4 – Create an Iceberg Table**  
**Scenario:** Validate table creation in Iceberg.  
**Remark:** Ensure table creation completes without errors.  
**Given:** A running Iceberg instance.  
**When:** The query CREATE TABLE iceberg.default.users (id INT, name STRING); is executed.  
**Then:** The table should be created successfully.  
**Test Run Date:**  
**Result:** Pending/Pass/Fail  

**Test Case 5 – Insert Data into Iceberg Table**  
**Scenario:** Verify data insertion into Iceberg.  
**Remark:** Ensure data is stored correctly.  
**Given:** A created Iceberg table.  
**When:** The query INSERT INTO iceberg.default.users VALUES (1, 'Alice'); is executed.  
**Then:** The data should be inserted without errors.  
**Test Run Date:**  
**Result:** Pending/Pass/Fail  

**Test Case 6 – Retrieve Data from Iceberg Table**  
**Scenario:** Verify data retrieval.  
**Remark:** Ensure correct data is fetched.  
**Given:** An Iceberg table with data.  
**When:** The query SELECT * FROM iceberg.default.users; is executed.  
**Then:** The correct data should be retrieved.  
**Test Run Date:**  
**Result:** Pending/Pass/Fail  



**Test Case 7 – Update an Iceberg Table Record**  
**Scenario:** Validate record update in Iceberg.  
**Remark:** Iceberg may not support direct updates; verify alternative approaches.  
**Given:** An existing table iceberg.default.users with records.  
**When:** The query UPDATE iceberg.default.users SET name = 'Bob' WHERE id = 1; is executed.  
**Then:** The record should be updated successfully, or an alternative approach should be used.  
**Test Run Date:** _(To be filled)_  
**Result:** Pending/Pass/Fail  



**Test Case 8 – Delete Data from Iceberg Table**  
**Scenario:** Validate data deletion in Iceberg.  
**Remark:** Ensure data deletion completes without errors.  
**Given:** A record exists in the iceberg.default.users table.  
**When:** The query DELETE FROM iceberg.default.users WHERE id = 1; is executed.  
**Then:** The data should be deleted successfully.  
**Test Run Date:** _(To be filled)_  
**Result:** Pending/Pass/Fail  



**Test Case 9 – Validate Schema Evolution**  
**Scenario:** Validate the addition of a new column in Iceberg table.  
**Remark:** Ensure the schema evolves correctly without errors.  
**Given:** A created Iceberg table.  
**When:** The query ALTER TABLE iceberg.default.users ADD COLUMN age INT; is executed.  
**Then:** The column age should be added successfully to the table.  
**Test Run Date:** _(To be filled)_  
**Result:** Pending/Pass/Fail  



**Test Case 10 – Insert Data via GUI**  
**Scenario:** Validate data insertion via GUI.  
**Remark:** Ensure data is stored correctly in Iceberg.  
**Given:** A running GUI form for inserting data.  
**When:** A user with id=2 and name='Charlie' is inserted through the GUI.  
**Then:** The data should be stored in Iceberg without errors.  
**Test Run Date:** _(To be filled)_  
**Result:** Pending/Pass/Fail  

---

**Test Case 11 – Update Data via GUI**  
**Scenario:** Validate data update via GUI.  
**Remark:** Ensure data is updated correctly in Iceberg.  
**Given:** A running GUI form with editable user data.  
**When:** A user’s name is edited via the GUI and saved.  
**Then:** The data should be updated correctly in Iceberg.  
**Test Run Date:** _(To be filled)_  
**Result:** Pending/Pass/Fail  

---

**Test Case 12 – Delete Data via GUI**  
**Scenario:** Validate data deletion via GUI.  
**Remark:** Ensure data is removed correctly from Iceberg.  
**Given:** A running GUI with user data to delete.  
**When:** A record is deleted from the GUI.  
**Then:** The record should be removed from Iceberg.  
**Test Run Date:** _(To be filled)_  
**Result:** Pending/Pass/Fail  

## NFR Test Case
**Test Case 1** – Verify Successful Submission Within 2 Seconds  
**Scenario**: Check if the system processes submissions quickly.  
**Remark**: The process should be fast and responsive.  
**Given**: A valid input is provided.  
**When**: The user submits the request.  
**Then**: The system should response within 2 seconds.  
**Test Run Date:** _(To be filled)_    
**Result:** Pending/Pass/Fail    
