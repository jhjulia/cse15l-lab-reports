## CSE15L Lab 5: Week 9 Lab Report

### **```grade.sh``` code :**
```
set -e
CPATH=".:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar"
rm -rf student-submission
git clone $1 student-submission
cp TestListExamples.java student-submission/
cp -r lib student-submission
cd student-submission

javac -cp $CPATH *.java
java -cp $CPATH org.junit.runner.JUnitCore TestListExamples
```

---
<br/>
### Student submission 1:
![image](Screenshot51.png)
> * Student submission of https://github.com/ucsd-cse15l-f22/list-methods-lab3, which has the same code as the starter from lab 3.   

<br/>
<br/>

### Student submission 2:
![image](Screenshot52.png)
> * Student submission of https://github.com/ucsd-cse15l-f22/list-methods-compile-error, which has a syntax error of a missing semicolon.
> * In grade.sh, ```set -e``` allows the termial to show the error if it exists in the student submission. Then, ```CPATH=``` stores the class path as a variable, and ```rm -rf student-submission``` removes the student-submission directory. After that, ```git clone $1``` clones the repository of the student-submission in a new directory. Then, ```cp``` copies TestListExamples.java in the student-submission, and ```cp -r``` copies the student-submission to lib. After that, ```cd``` changes the current working directory to the student-submission. Finally, ```javac -cp``` compiles every java files in ```$CPATH```, and ```java -cp``` runs TestListExamples in ```$CPATH``` and print out the error saying there is a syntax error of a missing semicolon in ```result.add(0, s)```. 
> * ```set -e``` returns 1, ```CPATH=``` returns 1, ```rm -rf``` returns 1, ```git clone $1``` returns 1, ```cp``` returns 1, ```cp -r``` returns 1, ```cd``` returns 1, ```javac -cp``` returns 1, and ```java -cp``` returns 0. 
> * Therefore, every commands is working, except for the last line of ```java -cp $CPATH org.junit.runner.JUnitCore TestListExamples``` because there is an compile error in the code file.
<br/>
<br/>

### Student submission 3:
![image](Screenshot53.png)
> * Student submission of https://github.com/ucsd-cse15l-f22/list-methods-signature, which has the types for the arguments of ```filter``` in the wrong order, so it does not match the expected behavior.  



