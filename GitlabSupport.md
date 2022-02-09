# Question 1

---- 

### Bash Script to print usernames of all linux users

----

`awk -F: '{ print $1,":"$6}' /etc/passwd` 

----

### Run above script and coverts it to md5 hash and stores in /var/log/current_users

----

`awk -F: '{ print $1,":"$6}' /etc/passwd |md5sum  > /var/log/current_users.txt`

----

### cron job to run above script every hour

----

`0 * * * * awk -F: '{ print $1":",$6}' /etc/passwd |md5sum > /var/log/current_users.txt` 

----

# Question 2 

----

# question 3

----

Below are sequence of Git commands that could have resulted in the commit graph

```
 git init

 git add . 

 git commit -m "First Commit" 
 
 ```


