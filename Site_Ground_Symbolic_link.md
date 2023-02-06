@jishen027

# How to create a symbolic link on [SiteGround.com](https://www.siteground.co.uk/web-hosting.htm) using SSH

## Step 1
Using Siteground dev ssh tool to connect into the server

## Step 2 
After you connected to the server, go to the dirctory that you want to connect. use command `pwd` to show current path and copy the path.

## Step 3 
go to the dirctory that you want to execute the link, use command `ln -s paste/the/path/here`

or you want to link to the folder with different name, use the command `ln -s paste/the/path/here floder_name`. 


## final 
if you want to unlink the folder, use the commnad `unlink folder_name`. 