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
git clone https://github.com/arittASinha2003/HospitalManagementSystem.git
cd HospitalManagementSystem
```

### 2. Creating Virtual Environment (Recommended, but Optional)
```bash
python -m venv myenv
myenv/Scripts/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the following commands:
```bash
python manage.py makemigrations
python manage.py migrate
python manage.py runserver
```

### 5. Go to the website displayed on the terminal to view the website.
