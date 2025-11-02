# 🎓 Woldia University - Student Course Completion Portal

This is a static web application designed for Woldia University to allow students to securely look up their completed courses by searching their full name or first name.

The project is hosted entirely using **GitHub Pages** and operates without a traditional backend database. All student course data is stored in a static JSON file that must be manually updated by an administrator.

---

## 🔗 Live Portal Access

* **Student Portal (Public Access):** `[Your GitHub Pages URL]/index.html` (e.g., `https://username.github.io/repo-name/`)
* **Admin Panel (Restricted Access):** `[Your GitHub Pages URL]/admin.html`

---

## 👩‍💻 For Students: How to Use the Portal

1.  Navigate to the **Student Portal** link above.
2.  Enter your **Full Name** (e.g., "Admasu Tesfaye Kebede") or your **First Name** (e.g., "Admasu") in the search bar.
3.  Click **"Search My Courses"**.
4.  If your name is found, a list of your completed courses will be displayed.

---

## 👨‍💼 For Administrators: Data Management Guide

The Admin Panel (`admin.html`) is used to process updated Excel files and generate the static JSON data required for the portal.

### **1. Admin Login**

* **Access:** Open the `admin.html` page.
* **Password:** Enter the default admin password: `admin123`
    * *(Note: This password is in the client-side code and is for access control only; it is NOT secure.)*

### **2. Prepare the Data File (Excel)**

The system expects data from an Excel file (`.xlsx` or `.xls`) with specific column headers:

| Header Name | Purpose |
| :--- | :--- |
| `Full_Name` | The unique identifier for the student. |
| `First_Name` | Used for students who search using only their first name. |
| `Course` | The name of the completed course. |

* *Multiple rows with the same `Full_Name` will automatically be grouped into a single student record.*

### **3. Process and Generate JSON**

1.  In the Admin Panel, click **"Choose File"** and select your prepared Excel file.
2.  Click **"Process File"**.
3.  Wait for the **"Success"** message.
4.  Click **"Show JSON Data"**.

### **4. CRITICAL STEP: Update and Commit `students.json`**

Since GitHub Pages cannot save files directly, the Admin must manually commit the new data:

1.  Click the **"Copy to Clipboard"** button below the JSON output.
2.  Navigate to your GitHub repository on a computer.
3.  Go to the file path: `data/students.json`
4.  Click the **Edit** button (pencil icon).
5.  **Paste the copied JSON data** into the file, replacing all existing content.
6.  Scroll down and click **"Commit changes"**.

Once committed, the updated student information will be available on the public portal within a few seconds to a minute.
Testing:
Rebuild....
---

## ⚙️ Project Structure
