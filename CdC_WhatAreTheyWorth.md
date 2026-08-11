
> [!TODO]
> define the terms `group`, `section`, `class` etc...

This app should be centered arround the use of a single professor to manage his classes. We'll start by defining the basic use cases that the user will have in this software:

# ⁠Manage courses

Let's start by asking the question: what does 'managing a course' mean? Will he be in charge of a group of students that course? he'll be able to manage multiple groups within it as is usually the case in my experience. But sometimes a professor may be teaching a course without being in charge of any lab (TP) or tutorial/recitation (TD) withing that class. In such a case, the professor should still be able to manage the aggregate grades of all groups within his classes without managing the weekly *assiduity, attendance, test* trilogy.

TL;DR
There are two principal workflows that the app should cover
1. Weekly and per period/session suivie
2. Final grade management: recite (rattrapage), re-takes (dettes), doublants (repeating the year), note de "controle continue" variable selon le context

**Courses change with the semester**

Since the 'resit' sessions come at the end of the year that means that the software must operate on a year. What that means is that you should be able to manage courses according to the current semester of the cycle and specialty.

The selection menu would therefore work in the following order:

- Semester
- Course
> **Result:** list of groups that the user is responsible for in that specific course/semester!

- Section
- Group
> **Result:** list of students!

> [!NOTE]
> since specialties can share courses among them there shouldn't be a separation by specialty.

let's make a preliminary modelization based off of this workflow.
