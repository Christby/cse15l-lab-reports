# Week6 Lab Report

## Step 1: Copy the whole markdown-parse directory to ieng6 account
Use the command `pwd` to check the markdown-parse directory and `ls` to ckeck all the files in it.

Then use the command `scp -r . cs15lwi22aot@ieng6.ucsd.edu:~/markdownparseCopy` to create a markdownCopy directory on the server and copy the markdown-parse directory recursively to it. 

![Image](pic1.1)
![Image](pic1.2)


## Step 2: log in your ieng6 acount after copying the directory and compiling and running the tests for your repository
Use the command `ssh cs15lwi22aot@ieng6.ucsd.edu` to log in the  account and change the working directory to markdownparseCopy by entering the command `cd mdcopy`
![Image](pic2)

Then use the command of compiling and running, which are `javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParse.java MarkdownParseTest.java` and `java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest` to run the JUnit tests on the server. 
![Image](pic3)


## Step 3: run the tests in one line
Combine the commands in one line, which resulted in the command `scp -r . cs15lwi22aot@ieng6.ucsd.edu:~/markdownparseCopy2; ssh cs15lwi22aot@ieng6.ucsd.edu "cd markdownparseCopy2/;/software/CSE/oracle-java-se-14/jdk-14.0.2/bin/javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParse.java MarkdownParseTest.java; /software/CSE/oracle-java-se-14/jdk-14.0.2/bin/java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest"`

Use this command to copy all the files to the remote server and run the JUnit tests.

![Image](pic4.1)
![Image](pic4.2)