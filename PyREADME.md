# SECTION E+F README
**PYTHON VERSION used:** 3.13 version

**Gradebook: OOP, exception handling, searching and sorting.**

Design choice: Duplicate names are rejected, thee full name is not case sensetive in the
lookup, allowing duplicates would make search and remove ambiguous.

**ARCHITECTURE and DESIGN CHOICES MADE**

•**Student Class:** Holds information for a single student, including their first name, last name, and a dictionary (self.grades) to track their scores for each subject.
• **Gradebook Class:** Manages the entire collection of students using a dictionary (dict) that links each student's unique, case-insensitive full name to their profile data.
