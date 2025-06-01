# 🏥 Hospital Management System - Java OOP Project

This Java project models a simple Hospital Management System using object-oriented programming principles. It includes entities such as patients, doctors, nurses, and staff with basic interactions like prescribing treatments and recording patient vitals.

---

## 🧱 Class Overview

### 👤 `Person` (Superclass)
- Attributes: `givenName`, `familyName`, `birthDate`, `gender`, `phone`
- Derived attribute: `fullName` (combines givenName and familyName)
- Provides `getFullName()` method

### 🧑‍⚕️ `Patient` (Extends `Person`)
- Attributes: `id`, `age`, `acceptedDate`, `sickness`
- Represents a patient in the hospital

### 👨‍⚕️ `Staff` (Extends `Person`)
- Attributes: `joinedDate`, `position`
- Base class for hospital staff members like doctors and nurses

### 👨‍⚕️ `Doctor` (Extends `Staff`)
- Additional attribute: `specialty`
- Behavior: `prescribe(Patient patient)` — simulates prescribing treatment

### 👩‍⚕️ `Nurse` (Extends `Staff`)
- Behavior: `recordVitals(Patient patient)` — simulates recording patient vitals

---

## 💡 Design Highlights

- **Inheritance:** Common properties are defined in `Person`. `Staff` extends `Person`, and specialized staff (`Doctor`, `Nurse`) extend `Staff`.
- **Encapsulation:** Class fields are private; access via getters or methods.
- **Method Overriding:** Staff subclasses add specialized methods.
- **Clear separation of concerns:** Patients and staff have distinct attributes and behaviors.

---

## 🖥 How to Run

1. Save the source code in a file named `HospitalManagementSystem.java`.
2. Compile and run using the terminal or IDE:

```bash
javac HospitalManagementSystem.java
java HospitalManagementSystem
