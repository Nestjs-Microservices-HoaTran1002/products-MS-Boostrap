## Dev

1. Clone the repository
2. Create an .env based on the .env.template
3. Run the command 'git submodule update --init --recursive' to rebuild the sub-modules
4. Run the 'docker compose up --build' command

### Steps to create the Git Submodules

1. Create a new repository on GitHub
2. Clone the repository to the local machine
3. Add the submodule, where 'repository_url' is the url of the repository and 'directory_name' is the name of the folder where you want the sub-module to be saved (it must not exist in the project)
```
git submodule add <repository_url> <directory_name>
```
4. Add changes to the repository (git add, git commit, git push)
Ex:
```
git add .
git commit -m "Add submodule"
git push
```
5. Initialize and update Sub-modules, when someone clones the repository for the first time, they must run the following command to initialize and update the sub-modules
```
git submodule update --init --recursive
```
6. To update the sub-module references
```
git submodule update --remote
```

## Important
If you work on the repository that has the sub-modules, **first update and push** on the sub-module and **then** on the main repository.

If you do it the other way around, you will lose the references of the sub-modules in the main repository and you will have to resolve conflicts.