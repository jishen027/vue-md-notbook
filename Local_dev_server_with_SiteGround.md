### automation using local dev server with siteground

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


## On your local machine
```sh
git remote add production ssh://user-name@host-name:port/path-tu-your-project/project-name.git

git config core.sshCommand "ssh -i ~./your-ssh-key"
```

