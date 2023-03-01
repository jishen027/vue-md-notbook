@jishen027

# How to create a symbolic link on [SiteGround.com](https://www.siteground.co.uk/web-hosting.htm) using SSH

## Step 1
Using Siteground dev ssh tool to connect into the server

## Step 2 
After you connected to the server, go to the dirctory that you want to connect. use command `pwd` to show current path and copy the path.

## Step 3 
Go to the dirctory that you want to execute the link, use command `ln -s paste/the/path/here`

Or you want to link to the folder with different name, use the command `ln -s paste/the/path/here floder_name`. 


## final 
If you want to unlink the folder, use the commnad `unlink folder_name`. 


## To create a bare git repo on site ground
- Clone you repo with --bare tag
```bash
git clone --bare you-git-repo-address.git
```

- Copy your bare git [project_name].git file into the Siteground cli

- Init the git repo on your Siteground
```bash
git init --bare --shared
```

- Now you can clone your project from Siteground
```bash
git clone -c"core.sshCommand=ssh -i ./your-ssh-key" ssh://[user-name]@[host-name].uk:[port]/home/[user-name]/www/[domain-name].uk/git/[project-name].git
```
