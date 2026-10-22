# SECTION E+F README
**PYTHON VERSION used:** 3.13 version

**Gradebook: OOP, exception handling, searching and sorting.**

Design choice: Duplicate names are rejected, thee full name is not case sensetive in the
lookup, allowing duplicates would make search and remove ambiguous.

**ARCHITECTURE and DESIGN CHOICES MADE**

•**Student Class:** Holds information for a single student, including their first name, last name, and a dictionary (self.grades) to track their scores for each 
subject.

• **Gradebook Class:** Manages the entire collection of students using a dictionary (dict) that links each student's unique, case-insensitive full name to their
profile data.

• **Supported subjects:** There are only 3 subjects that are accepted and used by the program, that being: Maths, English and Science.

• **Grade validation:** For the grade section only integers are accepted and the marks should be in the range of 0 to 10.


**Error Handling**
The program handles errors safely without crashing, using these custom exceptions that I enforced in the code.

• **InvalidNameError**: It is shown or acts if a name is empty.

• **InvalidSubjectError**: It is shown and enacted if the subject isn't maths, science, or english.

• **InvalidGradeError**: Comes into play if a grade inserted is outside the 0–100 range.

• **StudentNotFoundError**: Comes into play if the user tries to look up or delete a name that doesn't exist inside of the Gradebook program.

• **DuplicateStudentError**: Comes into play if the user tries to add a student who is already in the system.

