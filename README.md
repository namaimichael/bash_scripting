# bash_scripting
Bash Scripting Input and Output




# Create a repository on your remote or local Git and initialize it.

Step 1 

## On local terminal run 
`$ git init`

Step 2 

## Genarate public SSH KEYS from your local termial and copy the pub key to your remote repository server.
`$ ssh-keygen -t rsa` # public key output will be stored on this location `$ cat ~/.ssh/id_rsa.pub`

Step 3 

## Add your remote reposity server to your local Git and set Git global configs (i.e Default name, branch & email)
`$ git remote add origin git@github.com:namaimichael/bash_scripting.git'
`$ git branch -M main`

Step 4

## Git push your local changes to your remote repository 

`$ git push -u origin main`

Step 5 

## Make changes on you local code and add the changes to the local staging 
`$ git add *`
`$ git commit -m "first commit"`


** Exercise **

3. Study the Git commit graph shown below. What sequence of Git commands
could have resulted in this commit graph?

<img width="662" alt="image" src="https://user-images.githubusercontent.com/44470462/181833105-312637d1-3879-484b-a593-659170df4977.png">

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

## Git stash the changes on the feature branch and switch to the main branch 

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










