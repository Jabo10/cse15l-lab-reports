# Lab Report 4 - CLDQ – CSE Labs “Done Quick” (Week 7) 
# This version has a pre-setup that includes how to bypass having to input a password everytime when remote connecting to ieng6 servers found [here](https://ucsd-cse15l-w23.github.io/week/week7/#github-and-login-command-line-setup)
# Step 1 
* in terminal use your login with ssh `cs15lwi23XXX@ieng6.ucsd.edu` for me all I had to do was `<up><up><enter>`
If the pre-setup was done correctly logging into ieng6 should look as such, again no password needed 
<img width="454" alt="image" src="https://user-images.githubusercontent.com/122490992/221690850-d732838b-95f2-45d0-8691-314f68c1d913.png">
# Step 2
* Clone your fork of the repository from your Github account using `git clone git@github.com:ucsd-cse15l-w23/lab7.git` 
* This was done by pressing though history 17 times `<up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><enter>` it should look as such
 <img width="721" alt="image" src="https://user-images.githubusercontent.com/122490992/221697760-b6dc5f4f-fa6f-4302-a02d-ac9968e21a8a.png">
# Step 3
*  Make sure you change directory into lab7 with `cd lab7/`
*  Run the tests, demonstrating that they fail using
`javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java `
 then 
`java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples`
* Compiling was done by pressing through history 15 times `<up><up><up><up><up><up><up><up><up><up><up><up><up><up><up><enter>`
* and then another 14 times to run `<up><up><up><up><up><up><up><up><up><up><up><up><up><up><enter>`
* when entered it should look as such showing it failed
<img width="1218" alt="image" src="https://user-images.githubusercontent.com/122490992/221702040-bc0d2a22-98cf-4f39-a9d8-42a14981ea75.png">

# Step 4
* Edit the code file to fix the failing test by using `nano ListExamples.java` 
* I had to press through history up 13 times `<up><up><up><up><up><up><up><up><up><up><up><up><up><enter>`
* once in this file through `nano` it should look as such 
<img width="1218" alt="image" src="https://user-images.githubusercontent.com/122490992/221699038-149b5b4d-8ed3-4a85-aeb5-6614571ad941.png">
* I scrolled through the file by using my down arrow key to line 43 then changing `index1 += 1;` into `index2 += 1;` 
* once this is changed, press `ctrl + o` to write out then `enter` then `ctrl + x` to exit this should exit out of `nano` 

# Step 5
* Run the tests, demonstrating that they now succeed using 
`javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java `
 then 
`java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples`
 This time it was only up arrow 3 times then up arrow 3 times as such `<up><up><up><enter>` then `<up><up><up><enter>`
 * The result should look as such 
 <img width="1218" alt="image" src="https://user-images.githubusercontent.com/122490992/221702322-1d7373b6-91ee-49f5-acd9-59ebefb22517.png">

# Step 6
* Commit and push the resulting change to your Github account
* I used  `git add --all` which I manually typed and did not have in my history 
* then used   `git commit -m "finished"` also manually typed because I did not have in my history 
* the result should look as such 
<img width="1218" alt="image" src="https://user-images.githubusercontent.com/122490992/221706341-4a61bbe4-f87f-4e32-bcf3-0cb2683db512.png">
I did not use `tab` during this run a single time just used my history and or manually typed. 
 






