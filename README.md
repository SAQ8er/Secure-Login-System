# 🔐 Secure Login System (C++)

## 📌 Overview

This project is a **console-based Secure Login System** implemented in **C++**, designed to demonstrate core cybersecurity principles such as password protection, authentication mechanisms, and brute-force attack mitigation.

The system simulates a real-world authentication workflow, including **salted password hashing**, **account lockout policies**, and **multi-factor authentication (MFA)** using One-Time Passwords (OTP).

---

## 🚀 Features

### 🔑 Secure Password Storage

* Passwords are **never stored in plain text**
* Each password is combined with a **random salt**
* Hashed using a built-in hashing mechanism (`std::hash`) for demonstration

### 🛡️ Brute-Force Protection

* Tracks failed login attempts
* Locks account after **3 consecutive failures**
* Prevents further login attempts once locked

### 📲 Multi-Factor Authentication (MFA)

* Generates a **6-digit OTP**
* Requires OTP verification after successful password entry
* Adds an additional layer of security

---

## 🧠 How It Works

### 1. Registration

* User enters username and password
* System generates a random salt
* Password + salt → hashed → stored securely

### 2. Login

* User enters credentials
* System hashes input password with stored salt
* Compares with stored hash

### 3. Security Checks

* If incorrect → failed attempts increase
* If ≥ 3 attempts → account is locked

### 4. OTP Verification

* On successful login, an OTP is generated
* User must enter correct OTP to gain access

---

## 🏗️ Project Structure

```
Secure-Login-System/
│── main.cpp
│── README.md
```

---

## ⚙️ Requirements

* C++ compiler (GCC / Clang / MSVC)
* Standard C++ libraries

---

## ▶️ How to Run

### Compile:

```bash
g++ main.cpp -o login_system
```

### Run:

```bash
./login_system
```

---

## 📸 Example Output

```
=== Secure Login System ===
1. Register
2. Login
3. Exit

Enter username: user1
Enter password: ****
User registered successfully!

Enter username: user1
Enter password: ****
OTP sent: 123456
Enter OTP: 123456
Login successful!
```

---

## ⚠️ Security Disclaimer

This project is intended for **educational purposes only**.

### Limitations:

* Uses `std::hash` (NOT secure for real applications)
* OTP is displayed in console (not securely delivered)
* Data stored in memory (no persistence)

### ✅ Recommended Improvements:

* Use secure hashing algorithms like:

  * **bcrypt**
  * **Argon2**
  * **PBKDF2**
* Store data in a database (SQLite, MySQL)
* Implement secure OTP delivery (Email/SMS)
* Add logging and monitoring
* Use HTTPS in real-world applications

---

## 📚 Learning Outcomes

By working on this project, you will understand:

* Authentication system design
* Password hashing and salting
* Brute-force attack prevention
* Basic MFA implementation

---

## 👨‍💻 Author

**Noor Safaa (98r)** 

---

## 📄 License

This project is open-source and available under the MIT License.

---
