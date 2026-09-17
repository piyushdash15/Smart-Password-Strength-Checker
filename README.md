# 🔐 Smart Password Strength Checker

A lightweight, beginner-friendly, and privacy-focused **Password Strength Checker built using Python and Tkinter**.

The application analyzes passwords in real time and evaluates their strength using multiple security factors such as password length, character diversity, entropy, common weak patterns, and excessive repetition. It then displays a clear strength rating along with useful suggestions to help users create stronger passwords.

---

## 📌 Project Overview

Weak and predictable passwords are one of the most common security risks faced by users today.

Many users still create passwords using common words, repetitive characters, simple number sequences, or patterns such as:

* `password`
* `12345`
* `qwerty`
* `admin`
* `letmein`

The **Smart Password Strength Checker** helps users understand how secure their password is before using it.

Unlike a basic password validator that only checks the presence of uppercase letters or numbers, this project evaluates passwords using multiple factors and provides real-time feedback through an interactive GUI.

---

## ✨ Features

### ⚡ Real-Time Password Analysis

Password strength is evaluated instantly while the user types.

The application uses Tkinter event handling to automatically analyze every change in the password field.

---

### 🔢 Password Strength Scoring

The application assigns a score based on multiple password characteristics including:

* Password length
* Lowercase letters
* Uppercase letters
* Numerical digits
* Special characters
* Password entropy
* Weak pattern detection
* Character repetition

The final score is converted into one of the following strength levels:

| Score Range | Strength       |
| ----------- | -------------- |
| `≤ 2`       | 🔴 Very Weak   |
| `3 – 4`     | 🟠 Weak        |
| `5 – 6`     | 🟡 Moderate    |
| `7 – 8`     | 🟢 Strong      |
| `> 8`       | 🔵 Very Strong |

---

## 🧮 Entropy Calculation

The application calculates password entropy to estimate how difficult a password would be to guess.

Entropy is calculated using:

```text
Entropy = Password Length × log₂(Character Set Size)
```

The estimated character set size depends on which character categories appear in the password.

| Character Type     | Character Pool |
| ------------------ | -------------: |
| Lowercase letters  |             26 |
| Uppercase letters  |             26 |
| Digits             |             10 |
| Special characters |             33 |

Higher entropy generally indicates a more unpredictable password.

---

## 🚨 Weak Pattern Detection

The program checks passwords against several commonly used insecure patterns.

Examples include:

```text
qwerty
asdf
zxcv
password
letmein
admin
welcome
iloveyou
12345
11111
```

If one of these patterns appears inside the password, the overall security score is reduced.

---

## 🔁 Repetition Detection

Passwords containing very few unique characters are also detected.

For example:

```text
aaaaaaaa
11111111
abababab
```

Passwords with excessive repetition receive a score penalty and the application recommends using more varied characters.

---

## 🎨 Visual Strength Meter

A dynamic, color-coded password strength bar provides immediate visual feedback.

The bar changes depending on the calculated password strength:

```text
Very Weak   → Red
Weak        → Orange
Moderate    → Yellow
Strong      → Green
Very Strong → Blue
```

The width of the bar also increases with the password score.

---

## 💡 Smart Improvement Suggestions

When a password does not meet recommended security criteria, the application provides useful suggestions such as:

* Increase the password length
* Add lowercase letters
* Add uppercase letters
* Add numbers
* Add special characters
* Avoid common password patterns
* Avoid excessive character repetition
* Increase password complexity and entropy

If the password satisfies the security checks, the application displays:

```text
Great password! No improvements needed.
```

---

## 🔒 Privacy-First Design

The application works completely **offline**.

It does not:

* Send passwords over the internet
* Store passwords in a database
* Upload password information
* Use external APIs
* Save password history

All analysis is performed locally on the user's computer.

This makes the application suitable for educational demonstrations of password security principles.

---

## 🛠️ Technologies Used

| Technology     | Purpose                                     |
| -------------- | ------------------------------------------- |
| Python         | Core application development                |
| Tkinter        | Graphical User Interface                    |
| `re`           | Regular-expression based character analysis |
| `math`         | Entropy calculation                         |
| Tkinter Canvas | Visual password strength meter              |

No external Python packages are required.

---

## 📂 Project Structure

```text
Smart-Password-Strength-Checker/
│
├── Password_vityarthi.py
│   └── Main Python application containing the GUI,
│       entropy calculation, scoring system,
│       weak-pattern detection, and suggestions.
│
├── README.md
│   └── Project documentation.
│
└── statement.md
    └── Problem statement, project scope,
        target users, and project features.
```

---

## ⚙️ Requirements

Before running the project, make sure you have:

```text
Python 3.8 or above
```

The project only uses Python's standard library.

Required modules:

```python
tkinter
math
re
```

---

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/piyushdash15/Smart-Password-Strength-Checker.git
```

### 2. Navigate to the Project Folder

```bash
cd Smart-Password-Strength-Checker
```

### 3. Run the Application

```bash
python Password_vityarthi.py
```

If your system uses `python3`, run:

```bash
python3 Password_vityarthi.py
```

---

## 🖥️ How to Use

1. Run the Python program.
2. The **Smart Password Checker** window will open.
3. Enter a password in the password field.
4. The password is hidden using `*` characters.
5. Password strength is analyzed automatically.
6. Check the:

   * Strength rating
   * Entropy value
   * Color-coded strength bar
   * Security improvement suggestions

No additional button is required because analysis occurs automatically while typing.

---

## 🧪 Example Test Cases

| Password              | Expected Observation        |
| --------------------- | --------------------------- |
| `12345`               | Very Weak                   |
| `password`            | Weak due to common pattern  |
| `qwerty123`           | Weak / Moderate             |
| `aaaaaaaa`            | Very Weak due to repetition |
| `Hello123`            | Moderate                    |
| `Str0ng!Password`     | Strong                      |
| `Str0ng!P@ssw0rd2026` | Strong / Very Strong        |

Actual results may vary depending on the calculated score and entropy.

---

## 🧠 How the Scoring System Works

The password starts with a score of `0`.

### Length Score

```text
Length ≥ 16  → +3
Length ≥ 12  → +2
Length ≥ 8   → +1
```

### Character Diversity

```text
Lowercase letter present   → +1
Uppercase letter present   → +1
Digit present              → +1
Special character present  → +1
```

### Entropy

```text
Entropy > 60 bits → +1
Entropy < 40 bits → Improvement suggestion
```

### Security Penalties

```text
Common weak pattern detected → -2

Too few unique characters
or excessive repetition       → -2
```

The resulting score determines the final password strength category.

---

## 🎯 Project Objectives

The main objectives of this project are to:

* Understand password security fundamentals
* Learn practical password evaluation techniques
* Demonstrate entropy-based password analysis
* Detect commonly used insecure patterns
* Practice regular expressions in Python
* Understand GUI development using Tkinter
* Implement event-driven programming
* Provide useful cybersecurity awareness to users

---

## 👥 Target Users

### 🎓 Students and Learners

Useful for understanding Python GUI development, entropy, regular expressions, and basic cybersecurity concepts.

### 👤 General Users

Can be used to evaluate a password before using it for an online account.

### 💻 Developers

The password-scoring logic can be adapted and integrated into larger Python applications.

### 🏫 Educational Institutions

Can be used as a simple demonstration project for Python programming or introductory cybersecurity courses.

---

## 🔮 Future Improvements

Several features can be added in future versions:

* 👁️ Show/Hide password button
* 🌙 Dark mode
* 🔐 Secure password generator
* ⏱️ Estimated password crack-time
* 📊 Detailed password security report
* 📄 Export analysis as PDF
* 🗂️ Larger common-password dictionary
* 🧠 Advanced pattern recognition
* 🔡 Sequential character detection such as `abcd` and `1234`
* ⌨️ Keyboard-pattern detection
* 🌐 Optional breached-password checking using the Have I Been Pwned API with k-anonymity
* 🧪 Unit testing
* 📦 Executable version using PyInstaller

---

## ⚠️ Security Disclaimer

This project is designed primarily for **educational and password-awareness purposes**.

Password entropy and rule-based scoring provide useful estimates, but they do not guarantee that a password cannot be compromised.

For important accounts, users should also consider:

* Using long and unique passwords
* Avoiding reused passwords
* Using a trusted password manager
* Enabling multi-factor authentication
* Avoiding personal information inside passwords

---

## 🤝 Contributing

Contributions and suggestions are welcome.

To contribute:

```bash
git fork
```

or manually:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Commit your improvements.
5. Push the changes to your fork.
6. Create a Pull Request.

Possible contributions include:

* Improving the user interface
* Adding additional password security rules
* Improving scoring logic
* Adding automated tests
* Adding password generation functionality
* Improving documentation

---

## ⭐ Support

If you find this project useful:

* ⭐ Star the repository
* 🍴 Fork the project
* 🐛 Report issues
* 💡 Suggest improvements
* 🤝 Contribute through pull requests

---

## 👨‍💻 Author

**Piyush Kumar Dash**

---

## 📜 Important Instruction

This project is intended for educational and personal use.

You are free to study, modify, and extend the project according to the applicable repository license.

---

<div align="center">

### 🔐 Build Stronger Passwords. Build Safer Digital Habits.

Made with ❤️ using Python and Tkinter

</div>
