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

## site ground bare repo path to clone 
git clone -c"core.sshCommand=ssh -i ./your-ssh-key" ssh://u2-cwxucau2m03r@ssh.eyesiteview.uk:18765/home/u2-cwxucau2m03r/www/castlegreendev.eyesiteview.uk/git/Backend.git

