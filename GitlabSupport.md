# Question 1

---- 

### Bash Script to print usernames of all linux users



`awk -F: '{ print $1,":"$6}' /etc/passwd` 

----

### Run above script and coverts it to md5 hash and stores in /var/log/current_users



`awk -F: '{ print $1,":"$6}' /etc/passwd |md5sum  > /var/log/current_users.txt`

----

### cron job to run above script every hour



`0 * * * * awk -F: '{ print $1":",$6}' /etc/passwd |md5sum > /var/log/current_users.txt` 

----

# Question 2 

----

# Question 3

----

Below are sequence of Git commands that could have resulted in the commit graph

```
 git init

 git add . 

 git commit -m "First Commit" 
 
 git add .
 
 git commit -m "second Commit"
 
 git checkout -b feature-branch
 
 git add . 
 
 git commit -m "awesome feature"
 
 git checkout main 
 
 git add .

 git add .

 git commit -m "third commit"

 git merge feature-branch -m "Merge"

 git add . 

 git commit -m "fourth commit"
 
 ```
 
 ----
 
 # Question 4
 
 ----
 
 ## Using Git to implement a new feature/change without affecting the main branch
 
 This article seeks to provide steps neccesary to take so as to implement a new feature or change without affecting the main branch
 
 Below are the step by step guide on how you can achieve this. 
 
 - The first step is to create a new branch as this is neccesary so as not to affect the main branch or code. Use the git command ` git branch new-feature` to create a new branch named *new-feature*. 
   Changes made on this branch will not be reproduced on the main branch. The same applies to the changes made on the *new-feature* branch. 
 
 - The Second step is to switch to the newly created branch. This is important as any changed made on this branch will not affect the main branch. Use 
   the command ` git checkout new-feature` to switch to the *new-feature* branch. 
   >Alternatively you can use the command ` git checkout -b new-feature` to create a new branch *new-feature* and switch from the *master* branch to the *new-feature* branch. 
  
 - The third step is to add your files/code that implements your feature/change. This can be done in two ways, adding all the new files using the command ` git add . ` or adding specific files that are of interest using the command ` git add <<filename>> `. 
 
 


