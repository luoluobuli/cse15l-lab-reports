# Lab Report 4
### Step1: Log into ieng6
![Image](screenshot1.png)  
**Key pressed:** `ssh zhl106@ieng6-202.ucsd.edu<enter>`  
In the lab, I logged into ieng6 and it has some problems, so this time I logged into ieng6-202, and thus I typed everything on my own.  
This command logs me into another computer named ieng6.
### Step2: Clone your fork of the repository from your Github account (using the SSH URL)
![Image](screenshot2.png)  
**Key pressed:** `Ctrl R` `clone<enter>`  
I searched for the command `git clone git@github.com:luoluobuli/cse15l-lab7.git` I executed earlier in the command history.  
This command clones the repository from github to the local working directory.
### Step3: Run the tests, demonstrating that they fail
![Image](screenshot3.png)  
**Key pressed:** `cd cs<tab><enter>` `bash test.sh<enter>`  
I named the forked repository as cse15l-lab7, so I typed `cs` and `<tab>` to search for the directory. After that, I entered the bash script to run the test.  
`cd` changes the working directory to csel-lab7, and `bash` executes the bash script test.sh which compiles and runs ListExamplesTests.java.
### Step4: Edit the code file to fix the failing test
![Image](screenshot4-2.png)  
![Image](screenshot4-1.png)  
**Key pressed:** `vim Li<tab>.java<enter>` `r2` `:wq<enter>`  
I typed `Li` to search for `ListExamples.java` and `ListExamples` pop out so I typed `.java` to complete it. For some reason the cursor was already on the character I needed to edit, so I directly pressed r2 to change "index1" to "index2."  
`vim` opens the text editor that enables me to edit ListExamples.java, `r` replaces the original char 1 to 2, and `:wq` saves the file and quits the editor.
### Step5: Run the tests, demonstrating that they now succeed
![Image](screenshot5.png)  
**Key pressed:** `bash test.sh<enter>`  
This command runs the tests by running the bash script again.
### Step6: Commit and push the resulting change to your Github account (you can pick any commit message!)
![Image](screenshot6.png)  
**Key pressed:** `Ctrl R` `add<enter>`  
I searched for the command `git add ListExamples.java` I executed earlier in the command history.  
This command adds updated ListExample.java to staging.  
**Key pressed:** `Ctrl R` `commi<enter>`  
I searched for the command `git commit -m "change index1 to index2"` I executed earlier in the command history.  
This command is used to commit my change.  
**Key pressed:** `Ctrl R` `push<enter>`  
I searched for the command `git push -u origin main` I executed earlier in the command history.  
This command pushes my change to GitHub.
