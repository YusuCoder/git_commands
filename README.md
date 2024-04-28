![Git Merge](https://media.giphy.com/media/cFkiFMDg3iFoI/giphy.gif)
# git_commands
>_Here you can find a useful git commands, which you will need during your core curriculum._

>_If you want to push you project to the multiple remotes, such as your own github or gitlab you can use the following command to push you repo to multiple remotes:
- To check the remotes run the following command:

 ```
        git remote -v
 ```

- Add the remote to the origin, by default the origin name should be ```origin```

 ```
      git remote set-url --add --push origin <your git url>
      git remote set-url --add --push origin <your intra url>
 ```

>If you want to add all the permissions like ```fetch``` and ```pull``` run this commands:

```
    git remote add <remote-name> <github-url>
    git remote --add --push origin <intra-url>
    git remote --add --push origin <github-url> 
```
 - Example:

```
    git remote --add github https://example.com/my/repository.git
    git remote --add --push origin git@vogsphere.42heilbronn.de:vogsphere/intra-uuid-a0266de3-afab-48a3-a0df-e066c48fadb5-5652121-ryusupov
    git remote --add --push origin https://example.com/my/repository.git
```
- Then check if the changes are applied, it should look like this:

![Image Description](https://github.com/YusuCoder/git_commands/blob/master/imgs/Screen%20Shot%202024-04-28%20at%201.47.12%20PM.png)

>Now Push the changes and test it if it's working properly:

```
   git add *
   git commit -m "your commit"
   git push
```

### NOTE: If your branch is ```main``` recommend to change it to ```master```
>To change in already existing repository:
- 1 . Go to repository page.
- 2 . Go to the settings
- 3 . In ```General``` change the ```Default branch``` to ```master```

>To make the branch always master:
- 1 . Go to the profile settings
- 2 . Go to the repositories in settings
- 3 . Change the default branch to ```master```

### Fatching and Pulling changes:
```
   git fetch --all
   git merge origin/master --allow-unrelated-histories
   git merge [github-origin]/master --allow-unrelated-histories
```
### Adding ```Submodules``` to your repositoreis:
>If you want to use some repository which you already have you can use them as a submodule in your current project:
```
   git submodule --add <link from preffered repository>
   git init
   git submodule update
```

### NOTE: If you faced the issue like: when you clone you project and the submodule cloned withoud files inside, to fix it just run the following command:
```
   git submodule update --init
```

### ERRORS and SOLUTIONS

>Its usual to have errors while using git and especially if you're new in git
>Below i'll provide some error cases that i've faced with
- error: failed to push some refs to ''github.com/example_git/example_project.git''


![error: failed to push some refs to <some github url>](https://github.com/YusuCoder/git_commands/blob/master/imgs/Screen%20Shot%202024-04-28%20at%205.27.42%20PM.png)

- to fix this error there some commands possible:
- fetch all the changes
- force push the the `origin with error`
```
   git fetch --all
   git pull origin master
   git push -f origin master
```

## GOOD LUCK ;-)
