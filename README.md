# 📚 BookHaven - Online Book Catalog & Library

**Course:** Software Development Practices: Staff Graded Assessment - 2  
**Student Name:** KATAKAM VIVEK  
**Student ID:** 2024EB01720  
**GitHub Repository:** [https://github.com/KatakamVivek1210/BookHaven](https://github.com/KatakamVivek1210/BookHaven)  

A lightweight, responsive web catalog application for managing and exploring digital collections of books, novels, and literature. Built as a practical demonstration of end-to-end **Git & GitHub Version Control Workflows (Question 1)** and **Software Test Case Design (Question 2)** strictly conforming to the assignment rubric.

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
├── .git/                            # Git metadata, objects, and branch tracking
├── .gitignore                       # Ignore patterns for *.log files and temp/ directory
├── index.html                       # Main landing page with Featured Books list
├── about.html                       # About page with Contact & Support information
├── git_commands.txt                 # Comprehensive reference for all Git commands used
├── README.md                        # Project documentation and Software Test Case Suite
├── report.html                      # HTML source template for the 4-page assignment report
├── BookHaven_Assignment_Report.pdf  # Final submission 4-page PDF report
├── debug.log                        # [Ignored] Local runtime log file
└── temp/                            # [Ignored] Temporary directory
    └── cache.txt                    # [Ignored] Temporary cache file
```

---

## 🔄 Part 1: Git Workflow & Milestones (Question 1)

1. **Repository Initialization:**
   Initialized Git repository with `git init` and standardized the primary branch to `main` via `git branch -M main`.
2. **Author Configuration:**
   Configured Git identity locally (`KatakamVivek1210` / `katakamvivek1@gmail.com`).
3. **Step 1 (Initial Commit):**
   Committed initial HTML templates `index.html` and `about.html`.
4. **Step 2 (Second Commit):**
   Added curated "Featured Books" list to `index.html` and committed changes.
5. **Step 3 (Branching):**
   Created and checked out the `feature` branch using `git checkout -b feature`.
6. **Step 4 (Feature Commit):**
   Added the "Contact & Support" section to `about.html` and committed the update onto `feature`.
7. **Step 5 (Merge):**
   Switched back to `main` (`git checkout main`) and merged `feature` via fast-forward merge.
8. **Step 6 (Commit History):**
   Inspected and verified commit graph using `git log --oneline --graph --all`.
9. **Step 7 (.gitignore):**
   Configured `.gitignore` to disregard `*.log` files and the `temp/` folder. Created `debug.log` and `temp/cache.txt` to verify with `git status`, then committed `.gitignore`.
10. **Step 8 (Undo Operation):**
    Created and committed `temporary.txt`, then executed `git revert HEAD --no-edit` to cleanly delete the file and create a compensating commit without rewriting history. Verified deletion with `Test-Path temporary.txt` (False).
11. **Step 9 (Documentation):**
    Authored and committed `git_commands.txt` detailing all commands used with clear 1-2 line explanations.
12. **Step 10 (Remote Synchronization):**
    Linked remote repository to `https://github.com/KatakamVivek1210/BookHaven.git` and pushed both `main` and `feature` branches.

---

## 📊 Git Commit Graph

Below is the verified Git commit topology generated using `git log --oneline --graph --all`:

```text
* [HEAD -> main] Add BookHaven Assignment Submission Report PDF and source template
* Add professional README.md documentation and test cases
* Add git_commands.txt with all Git commands and explanations
* Revert "Add temporary.txt for testing revert"
* Add temporary.txt for testing revert
* Add .gitignore to ignore log files and temp directory
* [feature] Add contact section to about.html
* Update index.html: add featured books collection
* Initial commit: add index.html and about.html
```

---

## 🧪 Part 2: Test Case Design (Question 2)

**Application Under Test:** Login System with Username, Password, and Login Button.  
**Functional Requirements:**
- Username must not be empty.
- Password must be at least 6 characters long.
- Valid credentials allow successful login.
- Invalid credentials display a specific error message.
- Account locked after 3 consecutive failed login attempts.

### Test Case Table

| Test Case ID | Test Scenario | Input Data | Expected Output |
|:---:|:---|:---|:---|
| **TC_01** | Valid Login | Username="user1"<br>Password="password123" | Login successful; redirected to user dashboard. |
| **TC_02** | Boundary: Exact 6 Characters | Username="user1"<br>Password="pass12" (length = 6) | Login successful; minimum character requirement met. |
| **TC_03** | Invalid Username | Username="unregistered_user"<br>Password="password123" | Login denied; Error message displayed: "Invalid username or password". |
| **TC_04** | Invalid Password | Username="user1"<br>Password="wrongpassword" | Login denied; Error message displayed: "Invalid username or password". |
| **TC_05** | Boundary: Less than 6 Characters | Username="user1"<br>Password="12345" (length = 5) | Form submission blocked; Validation message displayed: "Password must be at least 6 characters long". |
| **TC_06** | Edge Case: Empty Username | Username=""<br>Password="password123" | Form submission blocked; Validation message displayed: "Username must not be empty". |
| **TC_07** | Edge Case: Empty Password | Username="user1"<br>Password="" | Form submission blocked; Validation message displayed: "Password must not be empty". |
| **TC_08** | Security: Account Lockout | Username="user1"<br>3 consecutive failed login attempts | Account locked; Error message displayed: "Account locked due to 3 consecutive failed login attempts. Please try again after 15 minutes." |

---

## 🚀 How to Run the Project Locally
1. Clone or open the project folder in any terminal.
2. Launch `index.html` in any web browser:
   ```powershell
   Start-Process index.html
   ```
3. Navigate between the **Home** and **About** pages using the navigation links.
