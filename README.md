# ClinicAppointmentandDiagnosticsPlatform-WebDev2026-CC
Clinic Appointment and Diagnostics Platform – ER Diagram and database design for managing doctors, patients, appointments, consultations, diagnostic tests, reports, and payments in a modern clinic system.
# Clinic Appointment and Diagnostics Platform – ER Diagram

[[https://app.eraser.io/workspace/KUCJo8e0p5x2XBhLqiG9?origin=share](https://app.eraser.io/workspace/KUCJo8e0p5x2XBhLqiG9?origin=share)](https://app.eraser.io/workspace/KUCJo8e0p5x2XBhLqiG9?origin=share)

This project contains the Entity Relationship Diagram (ERD) for a modern clinic management platform.

The goal of this system is to help a clinic digitally manage:

- patients
- doctors
- departments and specialties
- appointments
- consultations / doctor visits
- diagnostic tests
- reports
- payments

This is designed as a clinic-level system, not for a large hospital, so the model is kept simple, practical, and scalable.---

## Problem Statement

A modern clinic wants to organize its daily operations digitally.

Patients should be able to:

- book appointments
- visit doctors
- undergo diagnostic tests if prescribed
- receive reports later
- make payments

Doctors may belong to different departments and specialties.

A patient can visit the clinic multiple times.

One consultation can lead to multiple diagnostic tests.

Reports may be generated later after the test is completed.

---

## Main Entities Used

The ER diagram includes the following entities:

- **Role**
- **User**
- **Doctor**
- **Patient**
- **Department**
- **Specialty**
- **Appointment**
- **Consultation**
- **DiagnosticTest**
- **ConsultationTest**
- **Report**
- **Payment**

---

## Important Design Decision

One of the most important design choices in this ERD is the difference between:

### Appointment
This is the scheduled booking.

Example:  
A patient books an appointment for Monday at 10:00 AM.

### Consultation
This is the actual doctor visit.

Example:  
The patient actually visits the doctor and gets diagnosed.

Not every appointment results in consultation.

For example:

- patient cancels
- no show
- rescheduled

This is why both are separate entities.

---

## Real Life Example

Example 1:

A **young mother brings her child** to a pediatric doctor.

- Patient = child
- Doctor = Pediatric specialist
- Appointment = booked for 4 PM
- Consultation = doctor visit happens
- Test prescribed = blood test
- Report generated = next day
- Payment completed = consultation + test charges

---

Example 2:

An **older male patient** visits a cardiologist.

- Doctor specialty = Cardiology
- Consultation diagnosis = chest pain
- Diagnostic tests = ECG + blood pressure + blood work
- Multiple reports generated
- Payment linked to consultation

---

Example 3:

A **working woman visits dermatology**

- appointment booked online
- consultation completed
- skin allergy test prescribed
- report uploaded later

This shows how the design supports men, women, children, and elderly patients.

---

## Why User Master Table is Used

A `User` table is used to store common details like:

- name
- phone
- email
- password
- gender

This avoids duplication.

Role-based design is used:

- Admin
- Doctor
- Patient

Then specific details are stored in:

- Doctor table
- Patient table

This is closer to real-world application architecture.

---

## Relationships Covered

- one patient can book many appointments
- one doctor can attend many patients
- one consultation can have many tests
- one test record can generate one report
- one consultation can have many payments

---

## Tools Used

- **Eraser** for ER Diagram
- **GitHub** for submission

---

## Author

Created as part of SQL / Database Design assignment practice.
