## MySQL Database Design

### Table: appointments

- id: INT, Primary Key, Auto Increment
- doctor_id: INT, Foreign Key → doctors(id)
- patient_id: INT, Foreign Key → patients(id)
- clinic_id : INT, foreign Key → clinic_location_id
- appointment_time: DATETIME, Not Null
- duration: DOUBLE,
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
- payement_currency: VARCHAR(3),NOT NULL
- payement_status: VARCHAR(50), NOT NULL
- payement_type: VARCHAR(50), NOT NULL
- payement_chin: DOUBLE, NOT NULL

## MongoDB Collection Design

### Collection: prescriptions

{
"patientId": 1,
"doctorId": 2,
"appointmentId": 10,
"clinicId": 3,
"medications": [
{
"name": "Paracétamol",
"dosage": "500mg",
"frequency": "2 times per day",
"duration": "5 days"
}
],
"doctorNotes": "Take after meals",
"status": "ACTIVE",
"metadata": {
"issuedAt": "2026-03-30T10:00:00Z",
"updatedAt": "2026-03-30T12:00:00Z"
}
}

### Collection feedback

{
"patientId": 1,
"doctorId": 2,
"appointmentId": 10,
"rating": 4,
"comment": "Très bon service",
"tags": ["professional", "friendly"],
"metadata": {
"submittedAt": "2026-03-30T12:00:00Z"
}
}

### Collection: logs

{
"userId": 1,
"userRole": "ADMIN",
"action": "CREATE_APPOINTMENT",
"entity": "appointments",
"entityId": 10,
"status": "SUCCESS",
"metadata": {
"timestamp": "2026-03-30T13:00:00Z",
"ip": "192.168.1.1",
"device": "Chrome"
}
}

### Collection discution

{
"participants": [
{
"id": 1,
"role": "PATIENT"
},
{
"id": 2,
"role": "DOCTOR"
}
],
"appointmentId": 10,
"clinicId": 3,
"status": "ACTIVE",
"metadata": {
"createdAt": "2026-03-30T09:00:00Z",
"updatedAt": "2026-03-30T10:00:00Z"
}
}

### Collection: message

{
"discussionId": "disc001",
"senderId": 1,
"receiverId": 2,
"senderRole": "PATIENT",
"content": "Bonjour docteur",
"type": "TEXT",
"status": "SENT",
"metadata": {
"createdAt": "2026-03-30T10:05:00Z",
"readAt": null
}
}

### Collection: prescription_document

{
"prescriptionId": "presc001",
"patient": {
"id": 1,
"firstName": "Bilal",
"lastName": "Mokrani",
"dateOfBirth": "1995-06-15"
},
"doctor": {
"id": 2,
"firstName": "Dr. Ahmed",
"lastName": "Benali",
"specialization": "General Practitioner"
},
"clinic": {
"id": 3,
"name": "Central Clinic",
"address": "10 rue de Paris"
},
"medications": [
{
"name": "Paracétamol",
"dosage": "500mg",
"frequency": "2 times per day",
"duration": "5 days"
}
],
"notes": "Take after meals",
"qrCode": "BASE64_OR_URL",
"documentUrl": "/documents/prescriptions/presc001.pdf",
"status": "GENERATED",
"printHistory": [
{
"printedBy": "admin001",
"printedAt": "2026-03-30T14:00:00Z"
}
],
"metadata": {
"createdAt": "2026-03-30T13:30:00Z",
"updatedAt": "2026-03-30T14:00:00Z"
}
}

### Collection : payment_document

{
"paymentId": 101,
"appointmentId": 10,
"patient": {
"id": 1,
"firstName": "Bilal",
"lastName": "Mokrani"
},
"doctor": {
"id": 2,
"firstName": "Dr. Ahmed",
"lastName": "Benali",
"specialization": "General Practitioner"
},
"clinic": {
"id": 3,
"name": "Central Clinic",
"address": "10 rue de Paris"
},
"paymentDetails": {
"amount": 50.0,
"currency": "EUR",
"paymentType": "CARD",
"status": "PAID",
"paymentDate": "2026-03-30",
"paymentTime": "14:30:00"
},
"invoiceNumber": "INV-2026-0001",
"description": "Consultation médicale",
"documentUrl": "/documents/payments/invoice-0001.pdf",
"qrCode": "BASE64_OR_URL",
"printHistory": [
{
"printedBy": "admin001",
"printedAt": "2026-03-30T15:00:00Z"
}
],
"metadata": {
"createdAt": "2026-03-30T14:45:00Z",
"updatedAt": "2026-03-30T15:00:00Z"
}
}

### Collection: doctor_schedules

{
"doctorId": 2,
"clinicId": 3,

"weeklySchedule": [
{
"day": "MONDAY",
"slots": [
{
"startTime": "09:00",
"endTime": "12:00",
"status": "AVAILABLE"
},
{
"startTime": "14:00",
"endTime": "18:00",
"status": "AVAILABLE"
}
]
},
{
"day": "TUESDAY",
"slots": [
{
"startTime": "10:00",
"endTime": "16:00",
"status": "AVAILABLE"
}
]
}
],

"exceptions": [
{
"date": "2026-04-05",
"reason": "Vacation",
"status": "UNAVAILABLE"
},
{
"date": "2026-04-10",
"startTime": "09:00",
"endTime": "12:00",
"status": "UNAVAILABLE",
"reason": "Meeting"
}
],

"metadata": {
"createdAt": "2026-03-30T10:00:00Z",
"updatedAt": "2026-03-30T12:00:00Z"
}
}
