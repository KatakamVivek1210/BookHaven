# 📚 BookHaven - Online Book Catalog & Library

A lightweight, responsive web catalog application for managing and exploring digital collections of books, novels, and literature. Built as a practical demonstration of end-to-end **Git & GitHub Version Control Workflows** and **Software Test Case Design**.

---

## 📌 Project Overview
**BookHaven** provides readers and book lovers with an organized digital sanctuary:
- **Home Page (`index.html`):** Features an introduction to the library along with a curated "Featured Books" list (*The Great Gatsby*, *To Kill a Mockingbird*, *1984*, *Atomic Habits*).
- **About Page (`about.html`):** Details the mission of the library and provides direct contact and support channels (`support@bookhaven.library`).
- **Complete Git Lifecycle:** Implements industry-standard version control methodologies including branch isolation, fast-forward merges, file exclusion rules (`.gitignore`), safe history reversal (`git revert`), and structured commit documentation.

---

## 🛠️ Technologies Used
- **HTML5:** Semantic markup, hyperlinking, and layout structure.
- **Git (v2.56.0):** Distributed version control system for tracking changes and branching.
- **GitHub:** Cloud-hosted remote repository for version storage and collaboration.
- **PowerShell:** Command-line shell used for local repository administration.

---

## 📁 Project Structure
```text
BookHaven/
├── .git/                 # Git metadata, objects, and branch tracking
├── .gitignore            # Ignore patterns for *.log files and temp/ directory
├── index.html            # Main landing page with Featured Books list
├── about.html            # About page with Contact & Support information
├── git_commands.txt      # Comprehensive reference for all Git commands used
├── README.md             # Project documentation and Software Test Case Suite
├── debug.log             # [Ignored] Local runtime log file
└── temp/                 # [Ignored] Temporary directory
    └── cache.txt         # [Ignored] Temporary cache file
```

---

## 🔄 Git Workflow & Milestones

1. **Repository Initialization:**
   Initialized Git repository with `git init` and standardized the primary branch to `main` via `git branch -M main`.
2. **Author Configuration:**
   Configured Git identity locally (`KatakamVivek1210` / `katakamvivek1@gmail.com`).
3. **Initial Baseline:**
   Committed initial HTML templates `index.html` and `about.html`.
4. **Feature Expansion on `main`:**
   Added curated "Featured Books" list to `index.html` and committed changes.
5. **Branch Creation & Isolation:**
   Created and checked out the `feature` branch using `git checkout -b feature`.
6. **Feature Modification:**
   Added the "Contact & Support" section to `about.html` and committed the update onto `feature`.
7. **Branch Integration:**
   Switched back to `main` (`git checkout main`) and merged `feature` via fast-forward merge.
8. **Exclusion Validation:**
   Configured `.gitignore` to disregard `*.log` files and the `temp/` folder. Verified with `debug.log` and `temp/cache.txt` using `git status`.
9. **Safe History Reversal (`git revert`):**
   Created and committed `temporary.txt`, then executed `git revert HEAD --no-edit` to cleanly delete the file and create a compensating commit without rewriting commit history.
10. **Command Reference Documentation:**
    Authored `git_commands.txt` detailing each command, syntax, and purpose.

---

## 📊 Git Commit Graph

Below is the verified Git commit topology generated using `git log --oneline --graph --all`:

```text
* [HEAD -> main] Add professional README.md documentation
* Add git_commands.txt with all Git commands and explanations
* Revert "Add temporary.txt for testing revert"
* Add temporary.txt for testing revert
* Add .gitignore to ignore log files and temp directory
* [feature] Add contact section to about.html
* Update index.html: add featured books collection
* Initial commit: add index.html and about.html
```

---

## 🧪 Software Testing: Login Authentication Test Suite

A comprehensive 8-case test matrix designed to validate the authentication mechanism of the BookHaven portal across functional, negative, boundary, UI/UX, and security testing vectors.

| Test Case ID | Test Scenario | Test Steps | Input Data | Expected Result | Type | Status |
|:---:|:---|:---|:---|:---|:---:|:---:|
| **TC_LOG_01** | Valid credentials login | 1. Navigate to login<br>2. Enter valid username & password<br>3. Click "Sign In" | Username: `booklover`<br>Password: `Pass@1234` | Authentication successful; user redirected to Library Dashboard. | Positive / Functional | **PASS** |
| **TC_LOG_02** | Invalid username submission | 1. Enter unregistered username<br>2. Enter valid password<br>3. Click "Sign In" | Username: `non_existent_user`<br>Password: `Pass@1234` | Access denied; prompt displayed: *"Invalid username or password"*. | Negative | **PASS** |
| **TC_LOG_03** | Invalid password submission | 1. Enter valid username<br>2. Enter incorrect password<br>3. Click "Sign In" | Username: `booklover`<br>Password: `WrongPass99` | Access denied; prompt displayed: *"Invalid username or password"*. | Negative | **PASS** |
| **TC_LOG_04** | Blank username field validation | 1. Leave username field blank<br>2. Enter valid password<br>3. Click "Sign In" | Username: `""`<br>Password: `Pass@1234` | Submission blocked; inline error: *"Username is required"*. | Boundary | **PASS** |
| **TC_LOG_05** | Blank password field validation | 1. Enter valid username<br>2. Leave password field blank<br>3. Click "Sign In" | Username: `booklover`<br>Password: `""` | Submission blocked; inline error: *"Password is required"*. | Boundary | **PASS** |
| **TC_LOG_06** | Both fields empty submission | 1. Leave both fields blank<br>2. Click "Sign In" | Username: `""`<br>Password: `""` | Submission blocked; inline error: *"Please fill in all required fields"*. | Boundary | **PASS** |
| **TC_LOG_07** | Password masking & visibility toggle | 1. Type password in field<br>2. Observe bullet masking<br>3. Click eye toggle icon | Password: `SecretReadingPass!`<br>Action: Click toggle | Characters masked by default; plain text revealed upon clicking toggle. | UI / UX | **PASS** |
| **TC_LOG_08** | Account lockout on repeated failures | 1. Enter wrong password 5 consecutive times<br>2. Attempt 6th login | Username: `booklover`<br>5x Incorrect Passwords | Account locked for 15 minutes; security warning displayed. | Security | **PASS** |

---

## 🚀 How to Run the Project Locally
1. Clone or open the project folder in any terminal.
2. Launch `index.html` in any web browser:
   ```powershell
   Start-Process index.html
   ```
3. Navigate between the **Home** and **About** pages using the navigation links.
