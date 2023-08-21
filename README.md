# Hospital Databse Management
A Database for tracking the typical day to day events in a hospital.
The hospital administrator wants a database to track nurse assignments to their wards and nurse interactions with their patients, patient admissions by their doctors and treatments administered by doctors to their patients, bed assignments for each patient and items charged to patients during their stay. Administrator wants to record each nurse’s name and address, phone number and alternate phone number, email and the medical specialties he or she is certified. Some nurses supervise one or more other nurses. No nurse has more than one supervisor, and some nurses are unsupervised.

Each ward at the hospital has a designated number, descriptive name, physical location and phone number. Each ward has at least one nurse assigned to it. A nurse is assigned to at least one ward and rotates assignments among other wards. The assignment is tracked by the specific date and the hours worked in the assigned ward by each nurse on that date. In addition to nurse assignments, each ward also has a charge nurse. The charge nurse is the custodian of the medical records for the ward. Not all nurses act in this capacity, but those that do oversee only one ward, and a ward only has one charge nurse.

A ward consists of hospital beds. The beds are inventoried to a specific ward. Information on beds including their size (small, large, extra-large) and their type (elevated electrically or manually) and if they are available to be assigned to a patient. Most of the beds are large and manual (this is the default setting). The data entry (checks) for beds is limited to S, L, XL for size; E or M for type; O for occupied and A for available. Availability defaults to occupied to avoid double booking by mistake. All these value formats are set by rule or check. When a patient is admitted to the hospital they are assigned to a specific bed. Not all beds are available for use all the time, and a bed may not be assigned to more than one patient. In this database we are only tracking bed assignment history and not bed occupancy or availability.

Workflow: The admitting official conducts a review of all beds to determine which beds are available to assign to a patient. Information on patients is recorded: name, gender, dob, address, phone, alternate phone, email. The patient’s calculated age is also tracked. The date the patient is admitted to the hospital, the admitting doctor, the date the patient is discharged, and discharging doctor are also tracked. Some doctors admit patients while others do not. Doctor information tracked: name, address, phone, alternate phone, email and their medical specialties.

The hospital tracks the treatments administered to patients and the treating doctor. Treatments are tracked by name, description, and charge. The hospital also tracks the date and time of each treatment administered and the results. Some doctors treat patients while others do not. A given patient may receive no treatments or may receive many, and some patients may receive their treatments from more than one doctor. Some treatments have yet to be used while others have been used often. In addition to treatments, patients incur other charges for items used during their stay. The hospital tracks these charges as “items” and stores information on what items have been charged to which patients, based on date and quantity. Information that is to be stored for each item includes the item name and charge. All patients incur at least one charge for consumable items used during their stay. Some items are used often while items may be new or unusual

in nature and might rarely or never be charged to any patients. Lastly, the hospital tracks nurse patient care. Each nurse-patient care interaction is an event. There are several types of events: wellness check, medication, food service, assistance, treatment admin, and “other.” Given the number of shifts and ward rotations, a patient will typically be seen by more than one nurse during their stay, and a nurse most likely will interact with the same patient over several events during a single shift.

Requirements (Actors and Roles)
Nurse – A nurse is assigned to a ward. A nurse can be supervised by only one supervisor nurse.
Ward – A nurse can be assigned to multiple wards.
Bed – A bed must be assigned to a ward. At one time one bed can be assigned to only one patient.
Patient- A patient must be assigned to a ward and must be assigned a bed. A patient must be admitted and discharged by a doctor.
Physician- A patient must be admitted and discharged by a physician only.
Item – A patient can be administered multiple items for treatment.
Treatment – The treatment a patient received will be decided by a physician.

![image](https://github.com/DataCounsel/hospital_mangement/assets/71335870/d617fb8b-62a1-4c64-b62c-c304d79caaf2)

Entity Relationship Diagram


![image](https://github.com/DataCounsel/hospital_mangement/assets/71335870/3288354b-2f9c-44ad-a120-2d1bc305b86e)

Hospital Relational Schema

![image](https://github.com/DataCounsel/hospital_mangement/assets/71335870/63f46391-33d6-45ec-bbcf-e0edd208fcfe)

Database Design Diagram
