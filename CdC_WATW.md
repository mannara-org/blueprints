
# 1. Context Overview

In this section, we'll only cover *les grandes lignes* without going into details, we will address further specifics in the [[#3. Use Cases]] section.

In a typical Algerian university, the pedagogical structure follows a standard grouping of students defined by the LMD system.

"LMD" is an educational framework that organizes higher education into a Licence-Master-Doctorat degree structure. It defines each degree program's academic structure as a  hierarchy of academic levels, each with predefined semesters that in turn contain modules/courses.

Students of each academic level are first divided in sections and subsequently in groups. A section is a cohort of students that attend the same lectures and likewise, groups take their  labs together (as well as practical work tutorials, francophonly refered to as "TD" for "Travaux Dirigés").

A professor may fufill one of two roles when teaching a class:
- **Chargé de TD/TP:** responsible of the students of that group, including exam and assiduity grading.
- **Chargé de Cour:** responsible of the students of that section, including exam and assiduity grading.

The grading for each class is composed of two complementing criterias:
- **Controle Continue (CC):** worth 40% of the final grade. Depends on assigned homework, test grades, attendance, and the appreciation of the Chargé de TD/TP.
- **Examen Théorique de Longue/Courte Durée (ETLD/ETCD):** worth 60% of the final grade.

Other types of exams:
- **Remplacements:** Controvertial replacement exam for students who couldn't make it the day of the original exam
- **Resit Sessions:** les rattrapages
- **Retakes:** dettes (or debts)
- **Doublants:** repeating the year
Each with its own **grading policy.**

# 2. Scope

This app should be centered arround the use of a single professor to manage his classes.

# 3. Use Cases
 
We'll start by defining the basic use cases that the user will have in this software.

## ⁠3.1. Manage courses

**Courses change with the semester**<br>Resit sessions take place towards the end of the year, the software must operate on a year-to-year basis. One possible implementation is to allow the user to select courses according to the semester of the degree program.

We can imagine the following selection orders:

**Which course?**
1. Degree Program
2. Academic Level
3. Semester
4. Course
> **Result:** list of all the sections that the user is in charge of for in that specific course

**Which group?**
1. Section
2. Group
> **Result:** list of students!

**What to do?**<br>The app should incorporate two principal workflows:
- **Le Suivi d'Assiduité:** Weekly and per period/session
- **Final grade management:** for all types of exams and their corresponding grading policy.
