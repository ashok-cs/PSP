## Display the course participants

```c++
#include<iostream>
#include<string>
using namespace std;

class Student{
  private:
    string name;
    int rollno;
    string dept;  
  public:
    Student(){}
    Student(string sname, int rno, string sdept )
    {
      name = sname;
      rollno = rno;
      dept = sdept;
    }
    string getName(){
      return name;
  }
  friend int Course::enroll(Student s);
  
};

class Course{
  private:
    string courseName;
    int totalEnrolled;
    Student participants[10];
  public:
    Course(string cName){
      courseName = cName;
      totalEnrolled = 0;
    }
  int enroll(Student s){
      participants[totalEnrolled] = s;
      totalEnrolled++;
    } 
    
    int display(){
      for(int i=0; i<totalEnrolled; i++){
        cout<<participants[i].getName();
      }
    }
    int getTotal(){
      return totalEnrolled;
    }
  
};

int main(){
  Student s1("John",1,"CSE");
  cout << s1.getName() <<endl;
  Course java("Java");
  java.enroll(s1);
  cout << java.getTotal() <<endl;
  java.display();
}
```
