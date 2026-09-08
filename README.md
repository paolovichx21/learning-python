
class Student:
    count = 0
    total_gpa = 0

    def __init__(self , name , gpa):
        self.name = name
        self.gpa = gpa
        Student.count +=1
        Student.total_gpa += gpa


    def get_info(self):
        return f"{self.name} = {self.gpa}"


    @classmethod

    def get_count(cls):
        return f"The number of students: {cls.count}"

    @classmethod

    def get_average_gpa(cls):
        if cls.total_gpa == 0:
            return "average gpa: 0.00"

        else:
            return f"Average gpa: {cls.total_gpa / cls.count:.2f}"

if __name__=="__main__":

    students = [Student("paolovich" , 4.00),
                Student("joo" , 3.77),
                Student("Mark" , 2.10)]

    for student in students:
        print(student.get_info())

print("_______________________________")
print(Student.get_count())
print(Student.get_average_gpa())
