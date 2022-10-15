## CSE15L Lab 3: Week 3 Lab Report

### **Part 1**
![image](Screenshot3.1)
> * For the base window, the method "getPath()" and "String.format() are used. "getPath()" method returns the path of "url", and "String.format()" method help show the return value on the website. At this time, the url browser shows the empty array. 
> * One of the values for the relevant arguments to "getPath()" is the argument "/." Using "getPath" method, we can notice if the path of "url" has "/". Since the path of "url" was equals to "/", the first window shows the empty ArrayList called "search." 
> * If the value of "/" changes to other String value, the code would work and the browser shows the same first window only if the path of "url" has that exact String value.
![image](Screenshot3.2)
> * For the path supporting to add a new string to the list, I called the methods 
"getPath()" and "getQeury()." "getPath" method is the method returning the path of url as I said above, and "getQuery()" is for returning the query of url. 
> * The value of the relevant arguments to "getPath()" and "getQeury()" methods is also the argument "/add." Since we add a new String using the path, the code returns the String value on the browser using "getQuery" method if it contains the String "/add", checked by "getPath()" method.
> * If the value "/add" changes to another String value of argument, the code would work if we type the exact value in the search tap. 
![image](Screenshot3.3)
> * For the path supporting for querying the list of strings and returning a list of all strings that have a given substring, I called the methods "getPath()" and 
"getQuery()" to get the path and query for the "url."
> * The value of the relevant arguments to the methods is "search." In this code, we check the path of "url" using "getPath()" to see if it contains the String "search." If yes, we also check if the "parameter" that we are looking for is in the query of "url". If the query of "url" contains the paramter, the code returns the value of parameter that we searched.
> * If the value changes to another String value, the code should work if we type the changed value in the search tap.

---
### **Part 2**

![image](Screenshot3.4)
> * The failure-inducing input was the test code only having one element in the array.
> * The symptom was AssertionError because the code removes all the numbers equal to the lowest number when it should just leaves out only one. **(I got the actual assertion error before I got the another assertion error shown in the screenshot.)** 
> * The bug was on the line 38 to 41 in the screenshot. Since the original code removes all the values same as the lowest, I just added all the elements in the array and divide the sum by arr.length - 1 after I subtract the lowest number from the sum.
> * Since the symptom shows that my assertion on the test is wrong because the bug causes the wrong actual value by removing more than one value. 

![image](Screenshot3.5)
> * The failure-inducing input was the test code having different output order from the actual output.
> * The sympton was java.lang.OutOfMemoryError, which occurs when java heap has limited memory at that moment.
> * In line 57, we need to increment index2 by index2++ because the code never stop under the condition of index2 < list2.size().
> * Since the bug produces the non-stopping code, it causes the symptom of java.lang.OutOfMemoryError. 