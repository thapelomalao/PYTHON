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


**Error Handling**:
The program handles errors safely without crashing, using these custom exceptions that I enforced in the code.

• **InvalidNameError**: It is shown or acts if a name is empty.

• **InvalidSubjectError**: It is shown and enacted if the subject isn't maths, science, or english.

• **InvalidGradeError**: Comes into play if a grade inserted is outside the 0–100 range.

• **StudentNotFoundError**: Comes into play if the user tries to look up or delete a name that doesn't exist inside of the Gradebook program.

• **DuplicateStudentError**: Comes into play if the user tries to add a student who is already in the system.


# Menu Options

• **Add Student**:	Creates a new profile and asks for grades. Rejects duplicate names immediately.

• **Add grade**:	Updates or adds a score for an existing student.

• **Remove**: Deletes a student profile using their full name.

• **Search**: Finds students using a partial, case-insensitive name match.

• **Sort name**: 	Sorts and displays the student list alphabetically from A to Z.

• **Sort average**:  Sorts from highest to lowest average grade. Empty grades count as 0.

• **Sort subject**:   Sorts from highest to lowest score in a specific subject. Missing grades are listed last.

• **Exit**: 	Closes the program cleanly.

# METHODS
There are methods used in the student class.An example of this is here; 

```text
class Student:
    def __init__(self, firstname, lastname, mathgrade=None, sciencegrade=None, englishgrade=None):
        self.firstname, self.lastname = check_name(firstname), check_name(lastname)
        self.grades = dict(zip(SUBJECTS, map(check_grade, (mathgrade, sciencegrade, englishgrade))))

    @property
    def name(self):
        return f"{self.firstname} {self.lastname}"

    def add_grade(self, subject, grade):
        if (g := check_grade(grade)) is None:
            raise InvalidGradeError("A grade is required.")
        self.grades[check_subject(subject)] = g

    def average(self):
        g = [x for x in self.grades.values() if x is not None]
        return sum(g) / len(g) if g else 0        # No grades should be less than 0

    def print_details(self):
        marks = ", ".join(f"{s}: {'-' if g is None else f'{g:g}'}" for s, g in self.grades.items())
        print(f"{self.name:<25} {marks} | average: 
```
The def add_grade(self, subject, grade),  def average(self) and def print_details(self) are methods found in the student Class.
