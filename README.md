## **Overview**
This project involved the design and implementation of an automated attendance tracking system for university classes. It was developed as part of an academic assignment and includes class diagrams, file-based data management, and interaction via card readers.

## **Implementation Stages**
1. **Core Classes & Unit Testing:**
   
    Implemented classes based on the class diagram:

   - User (abstract), Student, Teacher, Class, Absence, and Attendance

   - Key methods were developed for user authentication, attendance tracking, and absence justification.

   - Some minor changes from the original specification were made for practicality (e.g., moved justifyAbsence() from Student to Absence).

2. **Data File Handling:**
   
    Implemented file readers to load student, teacher, and class data from JSON files using the Gson library:

   - UserDataReader: Processes and separates students and teachers.

   - ClassDataReader: Loads class schedules and details.

3. **Card Reader Application:**
   
    Developed a time-sensitive interface that:

   - Verifies if a teacher started the class.

   - Tracks student check-ins in real-time (full or partial attendance based on timing).

   - Registers absences if a student fails to check in within the time window.

   - Updates and writes data to output files.

4. **System Management Interface:**
   
    Features separate menus for students and teachers:

   - **Students** can: justify absences, view their attendance report, and list absences.

   - **Teachers** can: view users, change absence statuses, view class or student attendance statistics, and filter students by absence percentages.

## **Key Functional Highlights**
 
 - Dynamic handling of presence, partial presence, and absence.

 - Absence status can be changed (justified/unjustified) by teachers.

 - Clear separation of user roles and permissions.

 - Attendance statistics and justification tracking.

 - File persistence ensures data consistency after each session.

## **Tools & Technologies**
 
 - Java

 - Gson (for JSON parsing)

 - Text-based file input/output

 - Console-based interface
