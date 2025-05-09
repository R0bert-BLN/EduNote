# EduNote 

## Description

EduNote is an application for managing student grades.
It features a dynamic frontend built with HTML, CSS, and JavaScript, and a robust backend in C++ using Crow framework.

*   **Admins:** Can manage users (add/remove students and professors).
*   **Professors:** Can create/delete courses, enroll/remove students from courses, and input/edit student grades for their courses.
*   **Students:** Can view their grades for all courses they are enrolled in.


![Login Page](./assets/login_page.png)
![Admin Page](./assets/admin_page.png)
![Professor Page](./assets/professor_page.png)
![Student Page](./assets/student_page.png)

## Features

*   Role-based access control (Admin, Professor, Student).
*   User management (Admin).
*   Course creation and management (Professor).
*   Student enrollment in courses (Professor).
*   Grade entry and editing (Professor).
*   Grade viewing for enrolled students (Student).

## Technologies Used

*   **Backend:**
    *   C++ 
    *   [Crow](https://crowcpp.org/) 
    *   [SOCI](http://soci.sourceforge.net/) 
    *   [libsodium](https://libsodium.gitbook.io/doc/) 
*   **Frontend:** HTML, CSS, JavaScript (Vanilla JS)
*   **Database:** PostgreSQL 
*   **Dependency Management:** [vcpkg](https://vcpkg.io/en/index.html)

## Prerequisites

Before you begin, ensure you have the following installed:

1.  **C++ Compiler:** A modern C++ compiler supporting C++17 or later (e.g., GCC, Clang, MSVC).
2.  **vcpkg:** The C++ library manager.
3.  **PostgreSQL Server:** A running instance of PostgreSQL server.

## Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/R0bert-BLN/EduNote.git
    cd EduNote
    ```

2.  **Install C++ Dependencies using vcpkg:**
    *   Make sure vcpkg is correctly installed and integrated.
    *   Run the following command from the **root directory of the vcpkg installation**:
        ```bash
        ./vcpkg install crow soci[postgresql] libsodium
        ```

3.  **Database Setup:**
    *   Create a database
    *   Execute the SQL commands found in `.sql`  to create the necessary tables. 

4.  **Environment Configuration:**
    *   Rename the `.env.example` file to `.env`.
    *   Edit the `.env` file and fill in your specific database connection details (host, port, database name, user, password).


## Running the Application

1.  Build the project and run the executable file.
2.  Open your web browser and navigate to: `http://localhost:18080`

## Usage

*   Access the application via the URL mentioned above.
*   Use the login page to authenticate as an Admin, Professor, or Student. 
*   Navigate through the interface based on your user role to perform the actions described in the Description section.

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.
