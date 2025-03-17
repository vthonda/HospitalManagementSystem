# Hospital Management System

Python Django Project.

## Functions

### Admin

- Signup for their account, then login (No approval required).
- Can register/view/approve/reject/delete doctor (approve those doctor who applied for job in their hospital).
- Can admit/view/approve/reject/discharge patient (discharge patient when treatment is done).
- Can Generate/Download Invoice pdf (Generate Invoice according to medicine cost, room charge, doctor charge and other charge).
- Can view/book/approve Appointment (approve those appointments which is requested by patient).

### Doctor

- Apply for job in hospital, then login (Approval required by hospital admin, then only doctor can login).
- Can only view their patient details (symptoms, name, mobile) assigned to that doctor by admin.
- Can view their discharged (by admin) patient list.
- Can view their appointments, booked by admin.
- Can delete their appointment, when doctor attended their appointment.

### Patient

- Create account for admitting in hospital, then login (Approval required by hospital admin, then only patient can login).
- Can view assigned doctor's details (specialization, mobile, address).
- Can view their booked appointment status (pending/confirmed by admin).
- Can book appointments (approval required by admin).
- Can view/download Invoice pdf (Only when that patient is discharged by admin).

## Setup

### 1. Clone the Repository
```bash
git clone https://github.com/vthonda/HospitalManagementSystem.git
```
```bash
cd HospitalManagementSystem
```

### 2. Creating Virtual Environment (Recommended, but Optional)
```bash
python -m venv myenv
```
```bash
myenv/Scripts/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the following commands:
```bash
python manage.py makemigrations
```
```bash
python manage.py migrate
```
```bash
python manage.py runserver
```
(or)
```bash
python manage.py runserver 0.0.0.0:8000
```

### 5. Go to the website displayed on the terminal to view the website.

## Folder Structure

```bash
.
└── HospitalManagementSystem/
    ├── hospital/
    │   ├── migrations/
    │   │   ├── __init__.py
    │   │   ├── 0001_initial.py
    │   │   ├── 0002_delete_teacherextra.py
    │   │   ├── 0003_patient_admitdate.py
    │   │   ├── 0004_patientdischargedetails.py
    │   │   ├── 0005_appointment.py
    │   │   ├── 0006_appointment_status.py
    │   │   ├── 0007_auto_20200520_1023.py
    │   │   ├── 0008_doctor_profile_pic.py
    │   │   ├── 0009_auto_20200523_1118.py
    │   │   ├── 0010_auto_20200523_1122.py
    │   │   ├── 0011_auto_20200523_1325.py
    │   │   ├── 0012_auto_20200523_1336.py
    │   │   ├── 0013_patient_profile_pic.py
    │   │   ├── 0014_auto_20200526_1455.py
    │   │   ├── 0015_auto_20200526_1501.py
    │   │   ├── 0016_auto_20200622_1830.py
    │   │   ├── 0017_auto_20200622_1835.py
    │   │   └── 0018_auto_20201015_2036.py
    │   ├── __init__.py
    │   ├── admin.py
    │   ├── apps.py
    │   ├── forms.py
    │   ├── models.py
    │   └── views.py
    ├── hospitalmanagement/
    │   ├── __init__.py
    │   ├── asgi.py
    │   ├── settings.py
    │   ├── urls.py
    │   └── wsgi.py
    ├── static/
    │   ├── images/
    │   │   ├── admin.png
    │   │   ├── adminpropic.png
    │   │   ├── bg.jpg
    │   │   ├── doctor.png
    │   │   └── patient.jpg
    │   ├── profile_pic/
    │   │   ├── DoctorProfilePic/
    │   │   │   └── image
    │   │   └── PatientProfilePic/
    │   │       └── image
    │   ├── screenshots/
    │   │   ├── admin_dashboard.png
    │   │   ├── admin_doctor.png
    │   │   ├── homepage.png
    │   │   └── invoice.png
    │   └── style.css
    ├── templates/
    │   └── hospital/
    │       ├── aboutus.html
    │       ├── admin_add_appointment.html
    │       ├── admin_add_doctor.html
    │       ├── admin_add_patient.html
    │       ├── admin_appointment.html
    │       ├── admin_approve_appointment.html
    │       ├── admin_approve_doctor.html
    │       ├── admin_approve_patient.html
    │       ├── admin_base.html
    │       ├── admin_dashboard.html
    │       ├── admin_dashboard_cards.html
    │       ├── admin_discharge_patient.html
    │       ├── admin_doctor.html
    │       ├── admin_doctor_patient_card.html
    │       ├── admin_patient.html
    │       ├── admin_update_doctor.html
    │       ├── admin_update_patient.html
    │       ├── admin_view_appointment.html
    │       ├── admin_view_doctor.html
    │       ├── admin_view_doctor_Specialisation.html
    │       ├── admin_view_patient.html
    │       ├── adminclick.html
    │       ├── adminlogin.html
    │       ├── adminsignup.html
    │       ├── contactus.html
    │       ├── contactussuccess.html
    │       ├── doctor_appointment.html
    │       ├── doctor_base.html
    │       ├── doctor_dashboard.html
    │       ├── doctor_dashboard_cards.html
    │       ├── doctor_delete_appointment.html
    │       ├── doctor_patient.html
    │       ├── doctor_view_appointment.html
    │       ├── doctor_view_discharge_patient.html
    │       ├── doctor_view_patient.html
    │       ├── doctor_wait_for_approval.html
    │       ├── doctorclick.html
    │       ├── doctorlogin.html
    │       ├── doctorsignup.html
    │       ├── download_bill.html
    │       ├── footer.html
    │       ├── homebase.html
    │       ├── index.html
    │       ├── navbar.html
    │       ├── patient_appointment.html
    │       ├── patient_base.html
    │       ├── patient_book_appointment.html
    │       ├── patient_dashboard.html
    │       ├── patient_dashboard_cards.html
    │       ├── patient_discharge.html
    │       ├── patient_final_bill.html
    │       ├── patient_generate_bill.html
    │       ├── patient_view_appointment.html
    │       ├── patient_view_doctor.html
    │       ├── patient_wait_for_approval.html
    │       ├── patientclick.html
    │       ├── patientlogin.html
    │       └── patientsignup.html
    ├── db.sqlite3
    ├── LICENSE
    ├── README.md
    ├── manage.py
    └── requirements.txt
```
