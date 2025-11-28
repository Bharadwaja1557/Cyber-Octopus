# Login Brute-force Experiment – Instructions

This project demonstrates, in a controlled and authorized environment, how automated scripts can attempt multiple username/password combinations to test login mechanisms.  
It is intended **strictly for educational, research, and authorized testing purposes**.

---

## 🔧 Prerequisites

- Python 3 (recommended: 3.8+)  
- A list of test passwords in a file (e.g., `passwords.txt`)  
- A testing web application or lab environment you are authorized to access  

> ⚠️ Do **not** use this script on any real systems you do not own or do not have explicit permission to test.

---

## 🏗️ Setup

1. Copy both project files into a single folder.
2. Open a terminal **inside that folder**.
3. Run the main Python script:

    ```bash
    python3 login-bruteforcer.py
    ```

### ▶️ Inputs

When prompted, provide:

1. **Target URL** (for the authorized test environment)  
2. **Username**  
3. **Password file name** (contains a list of potential passwords)  
4. **Error message displayed on login failure**  
5. **Cookie value** (optional – can be skipped by pressing Enter)

---

## 🧠 How It Works (Technical Explanation)

1. The script reads the password file line by line.  
2. It attempts to submit login requests to the target URL using the given username and each password.  
3. After each attempt, it checks the server response for the **error message** to determine whether the login failed or succeeded.  
4. If a password matches, the script prints the correct combination.  
5. If no match is found in the list, it indicates that the password is **not present** in the file.

---

## 💡 Tips for Learning

- Use small, known password lists in controlled environments to safely observe behavior.  
- Adding commonly used passwords can help understand how attackers might attempt simple brute-force attacks.  
- Analyze server responses to see how authentication mechanisms handle repeated failed logins.  
- Consider implementing safe rate-limiting or sleep intervals to simulate realistic scenarios.

---

## ⚠️ Disclaimer

- This script is for **educational purposes only**.  
- Do **not** use it on websites or applications without explicit authorization.  
- Unauthorized attempts to access accounts are illegal and unethical.
