## MySQL Database Design

### Table: appointments

- id: INT, Primary Key, Auto Increment
- doctor_id: INT, Foreign Key → doctors(id)
- patient_id: INT, Foreign Key → patients(id)
- clinic_id : INT, foreign Key → clinic_location_id
- appointment_time: DATETIME, Not Null
- status: INT (0 = Scheduled, 1 = Completed, 2 = Cancelled)
- reason : VARCHAR(50)

### Table: patients

- id: INT, Primary Key, Auto Increment
- first_name: VARCHAR(50), NOT NULL
- laste_name: VARCHAR(50), NOT NULL
- phone : VARCHAR(13)
- eamil: VARCHAR(50)
- date_of_birth:DATE(),NOT NULL
- adresse : VARCHAR(100), NOT NULL
- localization: VARCHAR(100)

### Table: doctor

- id: INT, Primary Key, Auto Increment
- first_name: VARCHAR(50), NOT NULL
- laste_name: VARCHAR(50), NOT NULL
- phone : VARCHAR(13)
- eamil: VARCHAR(50)
- date_of_birth:DATE(),NOT NULL
- adresse : VARCHAR(100), NOT NULL
- grade : VARCHAR(20)
- spécialization: VARCHAR(50)

### Table: planning doctor

- id: INT, Primary Key, Auto Increment
- doctor_id: INT, Foreign Key → doctors(id)
- date_time_begin: DATE_TIME()
- date_time_end: DATE_TIME()
- clinic_id: INT, Foreign Key → clinic_locations(id)

### Table: Admin

- id: INT, Primary Key, Auto Increment
- first_name: VARCHAR(50), NOT NULL
- laste_name: VARCHAR(50), NOT NULL
- phone : VARCHAR(13)
- eamil: VARCHAR(50)
- date_of_birth:DATE(),NOT NULL
- adresse : VARCHAR(100), NOT NULL
- grade : VARCHAR(20)
- spécialization: VARCHAR(50)

### Table: clinic staff

- id: INT, Primary Key, Auto Increment
- first_name: VARCHAR(50), NOT NULL
- laste_name: VARCHAR(50), NOT NULL
- phone : VARCHAR(13)
- eamil: VARCHAR(50)
- date_of_birth:DATE(),NOT NULL
- adresse : VARCHAR(100), NOT NULL
- grade : VARCHAR(20)
- role : VARCHAR(20), NOT NULL
- spécialization: VARCHAR(50)

### Table: clinic_locations

- id: INT, Primary Key, NOT NULL
- name: VARCHAR(100), NOT NULL
- localisation: VARCHAR(100), NOT NULL
- adresse: VARCHR(100), NOT NULL

### Table: payement

- payement_id: INT, Primary Key, Auto Increment
- payement_date: DATE(), NOT NULL
- payement_time: TIME, NOT NULL
- payement_status: VARCHAR(50), NOT NULL
- payement_type: VARCHAR(50), NOT NULL
- payement_chin: DOUBLE, NOT NULL

## MongoDB Collection Design
