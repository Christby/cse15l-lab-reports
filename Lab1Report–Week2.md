# How to log into course specific account

## Step1: Install Visual Studios Code
download visual studios code from [https://code.visualstudio.com/](https://code.visualstudio.com/) and open it up
![Image](p1.png) 

## Step2: Remotely Connecting
Go to website [https://sdacs.ucsd.edu/~icc/index.php](https://sdacs.ucsd.edu/~icc/index.php) and get you account for CSE15L. 
Activate your account by resetting the password.

Open the terminal on VScode.
Enter `ssh cs15lwi22zz@ieng6.ucsd.edu` 
Then input the password as it ask you to do so.
You'll be connected to the server if the password is correct.
![Image](p2.png)

## Step3: Trying Some Commands
Here are some specific useful commands to try:
```
cd ~
cd
ls -lat
ls -a
ls <directory> where <directory> is /home/linux/ieng6/cs15lwi22/cs15lwi22abc, where the abc is one of the other group members’ username
cp /home/linux/ieng6/cs15lwi22/public/hello.txt ~/
cat /home/linux/ieng6/cs15lwi22/public/hello.txt
```
![Image](p3.png)

## Step4: Moving Files with scp
Create a file on your computer called WhereAmI.java and put the following contents into it:
```
class WhereAmI {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}
```
Then, after compiling and running the code with `javac` and `java`, which has an output as this:
![Image](p4.png)
run this command in the terminal from the directory where you made this file:
```
scp WhereAmI.java cs15lwi22zz@ieng6.ucsd.edu:~/
```
If you `javac` and `java` it again, you'll see a different directory of this file:
![Image](p5.png)

## Step5: Setting an SSH Key
Use the `ssh-keygen` command to save the private and public password in two files, which are `id_rsa` and `id_rsa.pub` respectively.
After doing that, you'll be able to log in to the account on the terminla without the need to enter the password.
![Image](p6.png)

## Step 6: Optimizing Remote Running
Edit the file and use commands to do whatever you feel comfortable with.
![Image](p7.png)
As the above image shows, using quotation marks at the end of ssh log in when running the commond on remote server
and then exit can save 3 keystrokes.

Also, using the "upper arrow" and "enter" command to run the previous commands only includes 2 keystrokes, but typing 
ssh `ssh cs15lwi22aot@ieng6.ucsd.edu` includes 32 keystrokes. Therefore using the upper arrow is clearly a better choice.

