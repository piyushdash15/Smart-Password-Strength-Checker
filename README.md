Smart Password Strength Checker is a lightweight, offline Python GUI application (Tkinter) that evaluates password strength in real time.
It analyzes length, character diversity (lowercase, uppercase, digits, special characters), entropy, weak patterns (e.g. “qwerty”, “12345”, “password”), and excessive repetition, then gives a clear strength rating, entropy value, color-coded visual bar, and actionable improvement suggestions.

Key Features:
Real-time analysis – Strength updates instantly as you type (<KeyRelease> binding).
Entropy calculation – Uses Shannon-style entropy in bits based on the size of the character set used.
Weak pattern detection – Flags common insecure sequences: qwerty, asdf, zxcv, password, letmein, admin, welcome, iloveyou, 12345, 11111, etc.
Character diversity scoring – Rewards presence of lowercase, uppercase, digits, and special characters.
Repeating character penalty – Detects passwords that use only 1–2 unique characters.
Visual strength meter – Canvas-based color bar that grows and changes color:
Very Weak → Red
Weak → Orange
Moderate → Yellow
Strong → Green
Very Strong → Blue
Helpful suggestions – Clear, specific recommendations when the password can be improved.
Privacy-first – Everything runs locally; no network calls, no data storage.

How Scoring Works (Simplified):
CriteriaPoints / EffectLength ≥ 16+3Length ≥ 12+2Length ≥ 8+1Contains lowercase+1Contains uppercase+1Contains digits+1Contains special chars+1High entropy (> 60 bits)+1Contains weak pattern–2Too many repeating chars–2
Final score maps to the strength labels and colors shown above.

Requirements:
Python 3.8 or higher
Standard library only (tkinter, math, re) – no external packages needed

Installation & Usage:
Bash# Clone the repository
git clone https://github.com/piyushdash15/Smart-Password-Strength-Checker.git
cd Smart-Password-Strength-Checker

# Run the application
python Password_vityarthi.py
A window titled “Smart Password Checker” will open. Type any password (it is masked by default) and watch the strength, entropy, bar, and suggestions update live.
Example Test Cases
PasswordExpected Result12345Very Weak / low entropy / many suggestionspasswordWeak (common pattern)qwerty123Weak / ModerateaaaaaaaVery Weak (repetition)Str0ng!P@ssw0rdStrong / Very Strong

Project Structure
textSmart-Password-Strength-Checker/
├── Password_vityarthi.py   # Main application
├── README.md               # This file
└── statement.md            # Detailed project statement / problem description

Future Improvements (Ideas)
Show/hide password toggle
Estimated crack-time display
Optional Have I Been Pwned (k-anonymity) check
Dark mode / better theming
Export report as PDF

Important Instruction
This project is open-source. Feel free to use, modify, and share it for educational or personal purposes.
