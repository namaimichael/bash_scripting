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

`git push -u origin main`

Step 5 

## Make changes on you local code and add the changes to the local staging 
`git add *`
`git commit -m "first commit"`


** Exercise **

3. Study the Git commit graph shown below. What sequence of Git commands
could have resulted in this commit graph?

<img width="662" alt="image" src="https://user-images.githubusercontent.com/44470462/181833105-312637d1-3879-484b-a593-659170df4977.png">

Step 6 

## Add local changes commits and Push the local changes to the remote repository 
`git add *`
`git commit -m "second commit`
`git push`

Step 7 

### Commit new code changes and push the changes to your remote repo

`git add usernames`
`git push`






