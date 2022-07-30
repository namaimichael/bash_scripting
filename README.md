# 1. BASH SCRIPTING TUTORIAL 

**Bash Scripting Input and Output**

**Exercise 1**

1. Write a Ruby or Bash script that will print usernames of all users on a Linux
system together with their home directories.

Step 1 

### Create a new file for your bash script from your working directory 

`$ touch usernames`

Step 2 

### Give you new created file execute user permission 
`$ sudo chmode 764 username` 

Step 3 

### Open your new file with your favourite editor and write your script
`$ nano usernames` 

<img width="524" alt="image" src="https://user-images.githubusercontent.com/44470462/181905796-b4705b74-7a7e-4202-8f70-9d9982ada452.png">

Step 4 

### Save your file and execute you script 

`sudo ./usernames`

Step 5 

### Check your script output from your log files 

`cat /var/log/current_users`

<img width="442" alt="image" src="https://user-images.githubusercontent.com/44470462/181905924-a58cdaa6-b31a-45af-82fb-aaf84e7b3b43.png">

`cat /var/log/user_changes`

<img width="430" alt="image" src="https://user-images.githubusercontent.com/44470462/181906049-0c05ff0e-1b4c-4049-9810-a9f024e3e00c.png">



# 2. CRON JOB TUTORIAL


Step 6 

### Create a cron job that runs every one hour 

`crontab -e` 

<img width="493" alt="image" src="https://user-images.githubusercontent.com/44470462/181906153-4c841772-dcb6-49e5-9bfc-4b6bd8a81160.png">


### Cron job will execute your script every one hour

`# Execute Cron Job every 1 hour
$ 0 * * * * /home/ubuntu/scripts/users/usernames`

<img width="510" alt="image" src="https://user-images.githubusercontent.com/44470462/181906190-d9be6d0f-c0f7-4908-96a4-9db5fa9ed492.png">


**Exercise 2**

3. Study the Git commit graph shown below. What sequence of Git commands
could have resulted in this commit graph?

<img width="662" alt="image" src="https://user-images.githubusercontent.com/44470462/181833105-312637d1-3879-484b-a593-659170df4977.png">

**Answer** 

1. The user executed first commit from main branch with comments first commit `git commit -m "first commit"`
2. The user executed second commit from main branch with comments second commit `git commit -m "second commit"`
3. The user created a new branch named feature-branch from the main branch and commited a new commit from the feature-branch with comments awesome feature `git commit -m "awesome feature"`
4. The user checked out back to the main branch and commited changes with third commit `git commit -m "third commit"`
5. The user from the main branch merged the feature-branch with main `git merge feature-branch`
6. The user from the main branch commited a commit with comments fourth commit `git commit -m "fourth commit"`


**Exercise 3** 

4. You’ve been hired to write a Git tutorial for beginners on: Using Git to implement a new feature/change without affecting the main branch

# 3. GIT TUTORIAL 
Local and remote repository set up 

### Create a repository on your remote or local Git and initialize it.

Step 1 

## On local terminal run 
`$ git init`

Step 2 

### Genarate public SSH KEYS from your local termial and copy the pub key to your remote repository server.
`$ ssh-keygen -t rsa` # public key output will be stored on this location `$ cat ~/.ssh/id_rsa.pub`

Step 3 

### Add your remote reposity server to your local Git and set Git global configs (i.e Default name, branch & email)
`$ git remote add origin git@github.com:namaimichael/bash_scripting.git && git branch -M main`

Step 4

### Git push your local changes to your remote repository 

`$ git push -u origin main`

Step 5 

### Make changes on you local code and add the changes to the local staging 
`$ git add *`
`$ git commit -m "first commit"`

Step 6 

## Add local changes commits and Push the local changes to the remote repository 
`$ git add *`
`$ git commit -m "second commit`
`$ git push`

Step 7 

### Commit new code changes and push the changes to your remote repo

`$ git add usernames`
`$ git push`

<img width="512" alt="image" src="https://user-images.githubusercontent.com/44470462/181836317-970d5771-03f6-4ffb-9113-a403f53ac45e.png">


Step 8 

### Create and switch to a new branch named feature-branch from the main branch 
`$ git checkout -b feature-branch` 

<img width="485" alt="image" src="https://user-images.githubusercontent.com/44470462/181837165-4643400d-9703-4ccd-81f3-8b88b52628b2.png">

Step 9

### Make features code changes on the new branch 

<img width="340" alt="image" src="https://user-images.githubusercontent.com/44470462/181837354-6b15f715-6c1d-4094-9df6-826bba8eaadd.png">

<img width="571" alt="image" src="https://user-images.githubusercontent.com/44470462/181837682-80d08b37-51d8-415e-8136-87edb278c2ed.png">

Step 10 

### Git stash the changes on the feature branch and switch to the main branch 

`$ git stash`

<img width="638" alt="image" src="https://user-images.githubusercontent.com/44470462/181838511-278af95f-8ce5-41c6-86a6-12419389ef9a.png">
<img width="397" alt="image" src="https://user-images.githubusercontent.com/44470462/181838642-88ddbd79-e63a-4f17-9fbc-e872fac1d076.png">


Step 10 

### Make code changes to main branch commit new changes to the main remote repository 

<img width="453" alt="image" src="https://user-images.githubusercontent.com/44470462/181839322-327edb1a-375d-4f53-a3f8-621317bd1abb.png">

`$ git commit -m "third commit"`

Step 11 

### Switch back to your feature branch and perform Git stash pop to restore your uncommited changes on the feature branch 

`$ git checkout feature-branch && git stash pop`

<img width="570" alt="image" src="https://user-images.githubusercontent.com/44470462/181840289-024bf2a7-f728-486c-b274-09b438e2c5b1.png">


Step 12 

### Commit your feature branch commit locally and push to the remote repository 

`git add usernames && git commit -m "awesome feature"`

<img width="624" alt="image" src="https://user-images.githubusercontent.com/44470462/181840715-749f3bfe-c889-4a43-8a0f-36adf97a3a4e.png">

`git push --set-upstream origin feature-branch` 

<img width="646" alt="image" src="https://user-images.githubusercontent.com/44470462/181841222-e893f1e2-4c99-4ed1-a800-a98bedae5634.png">

Step 13 

### Merge the feature branch with main branch 

**Git checkout to the main branch first  # local main branch needs to be up-to-date**

`$ git checkout main  && git pull && git checkout feature-branch && git merge main`


<img width="685" alt="image" src="https://user-images.githubusercontent.com/44470462/181842288-46bb91f2-c1e5-456b-aa92-bc4d3d685368.png">
<img width="579" alt="image" src="https://user-images.githubusercontent.com/44470462/181842473-9e1a5edc-7bdb-4c6c-bdf2-66d4b115525b.png">



<img width="579" alt="image" src="https://user-images.githubusercontent.com/44470462/181843291-52937193-48ce-4109-92b8-7206e32be631.png">


Step 14 

### Checkout the main branch and merge with the feature branch 

`$ git checkout feature-branch && git pull && git checkout main && git merge feature-branch`

<img width="579" alt="image" src="https://user-images.githubusercontent.com/44470462/181843291-52937193-48ce-4109-92b8-7206e32be631.png">


Step 15

### Delete feature-branch 

`git merge feature-branch && git branch -d feature-branch`

<img width="454" alt="image" src="https://user-images.githubusercontent.com/44470462/181845784-3972ea04-1fc3-4233-abb1-8d41606c14f5.png">


**Exercise 4**

5. What is a technical book/blog you read recently that you enjoyed? Please include a brief review of what you especially liked or didn’t like about it.

### Deploy a .NET Core API with Docker

https://dotnetplaybook.com/deploy-a-net-core-api-with-docker/

This is a technical tutorial blog on how to deploy a dotnet core api with docker. The blog is write in simple and intuitive language for beginners and advance users with example commands on how-to perform each task. The focus of this tutorial was to illustrate the ease with which you can deploy apps in Docker

**Exercise 5**

5. A user is complaining that it's taking a long time to load a page on our web application.



