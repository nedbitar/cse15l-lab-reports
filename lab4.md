Step 1: Login to ieng6
```
ssh cs15lwi23ajy@ieng6.ucsd.edu
```
Step 2: Cloning the Repo
```
git clone git@github.com:nedbitar/lab7.git
```
Step 3: Change Directory + Compile Tests + Running the Tests
```
cd lab7 &&
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java &&
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples
```
Step 4: Opening the File Editor:
```
nano ListExamples.java
```
Step 5: Editing the File:
<control><shift><-> 43
Then press the <Right Arrow> (12 times) <BackSpace> <2>

Step 6: Save and Exit:
<control><o><enter><control><x>
  
Step 7: Recompile and Run Tests:
```
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java &&
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples
```
Step 8: Adding the Changes:
```
<control><r> add <enter>
```
Step 8: Commiting the Changes:
```
<control><r> c <enter>
```
Step 9: Pushing the Changes:
```
<control><r> p <enter>
```
