# HospitalManagementSystem

### ABSTRACT

The goal of the project "HOSPITAL MANAGEMENT SYSTEM" is to computerize the hospital's front office management in order to produce software that is user pleasant, simple, rapid, and cost-efficient. It is concerned with the gathering of patient information, diagnostic data, and so on. It was traditionally, done by hand. The system's primary job is to register and retain patient and doctor information and access and change this information as needed. System input comprises patient and diagnosis information, while system output displays these facts on the screen. A username and password are required to access the Hospital Management System. It can be accessed by a receptionist or doctor and patients. Only they have access to the database. The information is easily accessible. The data is highly safeguarded for personal use, making data processing extremely simple.

### 1.	INTRODUCTION

Hospitals are a vital component of our society, providing the highest medical treatment to individuals suffering from various ailments caused by climate change, increasing workload, psychological stress, etc. Hospitals must keep track of their everyday activities.
The acts and documentation of the hospital's patients, doctors and their diagnosis and medical history facilitate its efficient functioning.
Keeping track of all activities and associated records on paper is laborious and susceptible to error. Considering the constant development of the hospital's population and patient load, the operation is inefficient and time-consuming. The recording and upkeep of these records are very unreliable, wasteful, and error-prone. In addition, it is not feasible economically or physically to store these records on paper.
Thus, keeping the functionality of the manual system as the cornerstone of our project. We have developed an automated version of the manual system, termed the "Hospital Management System." Our project's major purpose is to create a hospital that is 90% paperless. Additionally, it attempts to automate current processes cost-effectively and dependably. In addition, the system provides high levels of data security at all levels of user-system interaction, as well as trustworthy storage and backup services.

### 2.	OBJECTIVES OF THE SYSTEM

The objective of the "Hospital Management System" development project is to keep track of patients' diagnoses and medication information, physician lists, and so on. It is meant to achieve the following objectives:
1. Computerization of all patients, doctor, and their diagnostic information.
2. Making patient visits with doctors as convenient as possible for all parties.
3. Scheduling expert physician services and emergencies so that the hospital's facilities are fully used effectively and efficiently.
4. Patients' information should be kept current, and their records should be kept in the system for historical purposes.

### 3.	FUNCTIONAL REQUIREMENTS

1. Separate interfaces for patients and doctors. Patients and doctors should have separate logins.
2. Allow patients to book appointments and give previous medical history. 
3. Allow patients to view/update/cancel already booked appointments if necessary.
4. Allow doctors to cancel appointments.
5. Cancelled appointments should create free slots for other patients.
6. The system should avoid the clash of appointments.
7. The system should take into consideration hospital and doctor schedules and allow appointments only when a doctor is not already busy or does not have a break.
8. Doctors should be able to access patient history and profile and add to patient history. 
9. Doctors should be able to give diagnoses and prescriptions. 
10. Patients should be able to see complete diagnoses, prescriptions, and medical history user of the wrong or missing values in the paper. 

### 4.	SYSTEM DESIGN 

The purpose of the Design phase is to design a solution for the problem indicated in the requirements. The purpose of system design is to decide which modules should be included in the system, their requirements, and how they will interact to produce the desired results. The purpose of the design process is to create a model that can be used to build the system in the future. The produced model is referred to as the design of the system. System design is the process of developing a system's architecture, components, modules, interfaces, and data based on its requirements. The design process typically consists of two phases:                                          
•	Physical design                                                                                  
•	Frontend – React.js                                                                                   
•	Backend – Node.js                                                                            
•	Database - SQL
#### 4.1	 ER Diagram
Entity-Relationship A diagram is a graphical depiction of elements and their connections. It describes the relationships between data. A data entity is an item or notion about which information is recorded. A relationship describes how entities exchange information. In an E-R Diagram, there are three essential Components:

![image](https://github.com/Keerthireddy99/HospitalManagementSystem-/assets/145499897/02bc92ba-0dfe-4d38-b768-04be4c21f1ba)

#### 4.2	 Functional Dependencies and Normalization
##### 1. Patient: 
R = (Email, Password, Name, Address, Gender) 
FDs:
a. Email -> Password 
b. Email -> Name 
c. Email -> Address 
d. Email -> Gender 
The table is in 1NF since all attributes are atomic. 
The table is in 2NF since there is no partial dependency. 
The table is in 3NF due to the absence of any transitive dependency. 
##### 2. Medical History:
R = (id, Date, Conditions, Surgeries, Medication) 
FDs: 
a. id -> Password 
b. id -> Date 
c. id -> Conditions 
d. id -> Surgeries 
e. id -> Medication 
The table is in 1NF since all attributes are atomic. 
The table is in 2NF since there is no partial dependency. 
The table is in 3NF due to the absence of any transitive dependency. 
##### 3. Doctor:
R = (email, gender, password, name) 
FDs: 
a. email -> gender 
b. email -> password 
c. email -> name 
Table is in 1NF since all attributes are atomic. 
Table is in 2NF since there is no partial dependency. 
Table is in 3NF due to absence of any transitive dependency. 
##### 4. Appointment: 
R = (id, date, start time, end time, status) 
FDs: 
a. id -> date 
b. id -> start time 
c. id -> end time 
d. id -> status 
Table is in 1NF since all attributes are atomic. 
Table is in 2NF since there is no partial dependency. 
Table is in 3NF due to absence of any transitive dependency. 
##### 5. PatientsAttendAppointments: 
R = (patient, appointment, concerns, symptoms) 
FDs: 
a. (patient, appointment) -> concerns 
b. (patient, appointment) -> symptoms 
Table is in 1NF since all attributes are atomic. 
Table is in 2NF since there is no partial dependency. 
Table is in 3NF due to absence of any transitive dependency. 
##### 6. Schedule: 
R = (id, start time, end time, break time, day)
Since entire table is the key, it does not have partial and transitive dependencies. It also has atomic attributes. Hence it is in 3NF. 
##### 7. PatientsFillHistory: 
R = (Patient, History) 
FDs: 
a. History -> Patient 
Table is in 1NF since all attributes are atomic. 
Table is in 2NF since there is no partial dependency. 
Table is in 3NF due to absence of any transitive dependency. 
##### 8. Diagnose: 
R = (appointment, doctor, diagnosis, prescription) 
FDs: 
a. (appointment, doctor) -> diagnosis 
b. (appointment, doctor) -> prescription 
Table is in 1NF since all attributes are atomic. 
Table is in 2NF since there is no partial dependency. 
Table is in 3NF due to absence of any transitive dependency. 
##### 9. DoctorsHaveSchedules: 
R = (Schedule, Doctor) 
Since the entire table is the key, it does not have partial and transitive dependencies. It also has atomic attributes. Hence it is in 3NF. 
##### 10. DoctorViewsHistory: 
R = (history, doctor) 
Since the entire table is the key, it does not have partial and transitive dependencies. It also has atomic attributes. Hence it is in 3NF. 

#### 4.3	 Product Interface

The UI of the program will be straightforward, and menu-driven. The following screens will be shown.

![image](https://github.com/Keerthireddy99/HospitalManagementSystem-/assets/145499897/42240868-f5ea-4ad5-9643-23f77d49bbb9)

i. A Login Screen for entering the username, password, and role will be shown (Patient, Doctor). The user's employment will decide their access to different displays.
ii. A Search Form to Doctors for Patient Information
iii. The Form for creating a new patient and doctor will consist of text fields in which the Patient ID will be automatically generated, and the other information must be input manually.

##### 4.3.1	User Module - Patient 

• View the Appointment List and Status with Doctors                                                                           
• View Medication from the Doctor                                                                                    
• View Doctor List                                                                                                              
• View Medical History                                                                                                               
• View Appointment History.                                                                                                   
• Manage Own Profile – Updating password  

![image](https://github.com/Keerthireddy99/HospitalManagementSystem-/assets/145499897/82ab2a3d-6384-4c5d-af3a-0987b07a1ad2)

View Medical History – To check their medical history                                                                   
View Appointments – Past appointments of the patient                                                          
Schedule Appointment – To schedule a new appointment                                                                            

![image](https://github.com/Keerthireddy99/HospitalManagementSystem-/assets/145499897/7e78d78b-f2e8-46a4-a893-aae1175776df)

Medical history of a patient (Ranjith)

![image](https://github.com/Keerthireddy99/HospitalManagementSystem-/assets/145499897/af0ef7e7-0754-49e8-9459-9f1521abb3f1)

Appointment details of the patient

![image](https://github.com/Keerthireddy99/HospitalManagementSystem-/assets/145499897/29fae51a-3ec7-4af4-bd4c-1adbc0dca56e)

Scheduling screen for patients – They can choose the doctors from the dropdown of doctors and can select date time and then enter their concerns and symptoms and can schedule

![image](https://github.com/Keerthireddy99/HospitalManagementSystem-/assets/145499897/19301555-b08c-4390-afbd-644a27f9da0a)

Patients Registration form

##### 4.3.2	Doctor Module

• Manage patient. account opening and updating                                                                                     
• Manage appointments with patient                                                                                                   
• Create a prescription and enter diagnosis information for the patient	                                                                                            

![image](https://github.com/Keerthireddy99/HospitalManagementSystem-/assets/145499897/b28c7eae-f215-49ad-990c-ab479fd457a7)

Home Screen for Doctors, 
Appointments – To check their current appointments
View Patients – To check their patients’ medical records

![image](https://github.com/Keerthireddy99/HospitalManagementSystem-/assets/145499897/33424657-a281-45a7-85db-10dd5815aeab)

Appointments – To check their current appointments

![image](https://github.com/Keerthireddy99/HospitalManagementSystem-/assets/145499897/2e25634d-a944-49e0-923c-a690c0bb8362)

View Patients - Doctors can search their patients and check their medical history

![image](https://github.com/Keerthireddy99/HospitalManagementSystem-/assets/145499897/6ee52e8b-8479-44aa-aa3f-11f444ea140a)

Doctors Registration form – They have to click “I’m a doctor”

#### 5.	Future Enhancements
A Hospital Management System is the suggested system. We may improve this system by adding new features, such as a pharmacy system that tracks the stock of drugs in the pharmacy. Having such functionalities allows consumers to enter more comments into the system. Another additional feature can be to add a Billing module that produces bill includes fields such as Patient ID, Appointment No., Doctor charges, Hospital charges, etc. which will need to be filled up. In addition to these features, we can include another module that contains the lab reports such as MRI, X-ray etc.


#### 6.	Conclusion
The Hospital Management System (HMS) initiative aims to computerize hospital operations. It is a significant advancement over the manual system. The system's computerization has sped up the procedure. The front office management under the existing system is quite sluggish. The hospital management system has been carefully tested with fake data and is hence quite dependable. The software meets all of the needs of a typical hospital and is capable of storing information on patients who visit the hospital in a simple and efficient manner. As we are entering patient information electronically into the System, data will be protected. We may access a patient's history with a single click using this program. As a result, information processing will be faster. It ensures that Patient information is kept up to date. It quickly lowers the bookkeeping process, reducing human effort and increasing accuracy speed.

