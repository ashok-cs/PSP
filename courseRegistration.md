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
 
  
};

class Course{
  private:
    string courseName;
    int count;
    Student participants[10];
  public:
    Course(string cName){
      courseName = cName;
      count = 0;
    }
    
    int enroll(Student s){
      participants[count] = s;
      count++;
    } 
    
    int display(){
      for(int i=0; i<count; i++){
        cout<<participants[i].getName()<<endl;
        
      }
      cout << "Total participants: "<< count <<endl;
    }
};

int main(){
  Student s1("John",1,"CSE");
  Student s2("Ajay",2,"CSE");
  Course java("Java");
  java.enroll(s1);
  java.enroll(s2);
  java.display();
}
```
