class Student:
    def __init__(self, name, roll_number, cgpa):
        self.name = name
        self.roll_number = roll_number
        self.cgpa = cgpa

    def __str__(self):
        return f"{self.name} (Roll Number: {self.roll_number}, CGPA: {self.cgpa})"

def sort_students(student_list):
    # Sort the student_list in descending order based on CGPA
    sorted_students = sorted(student_list, key=lambda student: student.cgpa, reverse=True)
    return sorted_students

# Example usage:
students = [
    Student("Alice", "A101", 3.8),
    Student("Bob", "B102", 3.9),
    Student("Charlie", "C103", 3.7),
    Student("David", "D104", 3.95),
    Student("Eve", "E105", 3.85),
]

sorted_students = sort_students(students)

# Printing the sorted list of students
for student in sorted_students:
    print(student)