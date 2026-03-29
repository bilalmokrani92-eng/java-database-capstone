# User Story Template

**Title:**
As a [user role], I want [feature/goal], so that [reason]._

**Acceptance Criteria:**
1. [Criteria 1]
2. [Criteria 2]
3. [Criteria 3]

**Priority:** [High/Medium/Low]
**Story Points:** [Estimated Effort in Points]
**Notes:**
- [Additional information or edge cases]
**Title:**
As an administrator, I want to log in to the portal using my username and password, so that I can securely manage the platform.

**Acceptance Criteria:**

1. The administrator can enter a valid username and password.
2. The system authenticates credentials before granting access.
3. Access is denied if credentials are invalid.

**Priority:** High
**Story Points:** 3

**Notes:**

* Implement secure authentication (hashed passwords).
* Consider session management and timeout.

**Title:**
As an administrator, I want to log out of the portal, so that I can protect access to the system.

**Acceptance Criteria:**

1. The administrator can log out from any page.
2. The session is terminated after logout.
3. The user is redirected to the login page.

**Priority:** High
**Story Points:** 2

**Notes:**

* Ensure session invalidation on logout.

**Title:**
As an administrator, I want to add doctors to the portal, so that I can manage healthcare professionals.

**Acceptance Criteria:**

1. The administrator can input doctor details (name, specialty, etc.).
2. The system validates required fields.
3. The doctor is successfully saved in the database.

**Priority:** High
**Story Points:** 5

**Notes:**

* Validate unique identifiers (e.g., email).
**Title:**
As an administrator, I want to delete a doctor's profile, so that I can keep the system up to date.

**Acceptance Criteria:**

1. The administrator can select a doctor to delete.
2. The system confirms the deletion action.
3. The doctor is removed from the database.

**Priority:** Medium
**Story Points:** 3

**Notes:**

* Handle related data (appointments, history).

**Title:**
As an administrator, I want to execute a stored procedure to get the number of appointments per month, so that I can monitor system usage.

**Acceptance Criteria:**

1. The system executes a MySQL stored procedure successfully.
2. The result displays the number of appointments per month.
3. The data is accurate and reflects the database records.

**Priority:** Medium
**Story Points:** 5

**Notes:**

* Use MySQL CLI or backend integration.
* Consider displaying results in dashboard charts.

**Title:**
As a patient, I want to view a list of doctors without logging in, so that I can explore available options before signing up.

**Acceptance Criteria:**

1. The patient can access the doctor list without authentication.
2. The list displays relevant doctor details (name, specialty, availability).
3. The page is accessible publicly without login restrictions.

**Priority:** Medium
**Story Points:** 3

**Notes:**

* Consider pagination and filtering options.
**Title:**
As a patient, I want to register using my email and password, so that I can book appointments.

**Acceptance Criteria:**

1. The patient can enter a valid email and password.
2. The system validates and stores the user securely.
3. The account is created successfully after submission.

**Priority:** High
**Story Points:** 5

**Notes:**

* Password must be hashed.
* Validate email uniqueness.
**Title:**
  As a patient, I want to log in to the portal, so that I can manage my appointments.

**Acceptance Criteria:**

1. The patient can log in with valid credentials.
2. The system authenticates the user correctly.
3. Access is denied for invalid credentials.

**Priority:** High
**Story Points:** 3

**Notes:**

* Implement secure session handling.
**Title:**
As a patient, I want to log out of the portal, so that I can secure my account.

**Acceptance Criteria:**

1. The patient can log out from any page.
2. The session is terminated after logout.
3. The user is redirected to the login page.

**Priority:** High
**Story Points:** 2

**Notes:**

* Ensure session invalidation.
**Title:**
As a patient, I want to book a one-hour appointment with a doctor, so that I can receive medical consultation.

**Acceptance Criteria:**

1. The patient must be logged in to book an appointment.
2. The patient can select a doctor and a one-hour time slot.
3. The system prevents booking if the slot is unavailable.
4. The appointment is confirmed and saved successfully.

**Priority:** High
**Story Points:** 5

**Notes:**

* Prevent overlapping appointments.
* Consider notifications after booking.
**Title:**
As a patient, I want to view my upcoming appointments, so that I can prepare accordingly.

**Acceptance Criteria:**

1. The patient can see a list of upcoming appointments.
2. Each appointment displays date, time, and doctor details.
3. Only future appointments are shown.

**Priority:** Medium
**Story Points:** 3

**Notes:**

* Sort appointments by date.
**Title:**
  As a doctor, I want to log in to the portal, so that I can manage my appointments.

**Acceptance Criteria:**

1. The doctor can log in using valid credentials.
2. The system authenticates the doctor securely.
3. Access is denied if credentials are invalid.

**Priority:** High
**Story Points:** 3

**Notes:**

* Use secure authentication and session management.


**Title:**
As a doctor, I want to log out of the portal, so that I can protect my data.

**Acceptance Criteria:**

1. The doctor can log out from any page.
2. The session is terminated after logout.
3. The user is redirected to the login page.

**Priority:** High
**Story Points:** 2

**Notes:**

* Ensure session invalidation.
**Title:**
As a doctor, I want to view my appointment calendar, so that I can stay organized.

**Acceptance Criteria:**

1. The doctor can access their appointment calendar.
2. The calendar displays all scheduled appointments.
3. Appointments include date, time, and patient information.

**Priority:** High
**Story Points:** 5

**Notes:**

* Consider calendar view (daily/weekly/monthly).
**Title:**
As a doctor, I want to set my unavailability, so that patients only see available time slots.

**Acceptance Criteria:**

1. The doctor can mark time slots as unavailable.
2. Unavailable slots are excluded from booking options.
3. Changes are reflected immediately for patients.

**Priority:** High
**Story Points:** 5

**Notes:**

* Handle recurring unavailability (e.g., weekends).
**Title:**
As a doctor, I want to update my profile with my specialization and contact details, so that patients have accurate information.

**Acceptance Criteria:**

1. The doctor can edit specialization and contact details.
2. The system validates required fields.
3. Changes are saved and reflected in the system.

**Priority:** Medium
**Story Points:** 3

**Notes:**

* Ensure data consistency across views.
**Title:**
As a doctor, I want to view patient details for upcoming appointments, so that I can be prepared.

**Acceptance Criteria:**

1. The doctor can access patient details from appointments.
2. Relevant patient information is displayed.
3. Access is restricted to authorized doctors only.

**Priority:** High
**Story Points:** 5

**Notes:**

* Ensure compliance with data privacy regulations.
