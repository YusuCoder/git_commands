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
    git remote --add myremote https://example.com/my/repository.git
    git remote --add --push origin git@vogsphere.42heilbronn.de:vogsphere/intra-uuid-a0266de3-afab-48a3-a0df-e066c48fadb5-5652121-ryusupov
    git remote --add --push origin https://example.com/my/repository.git
```
- Then check if the changes are applied:
```
    git remote -v
```



