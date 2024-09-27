### Difference Between Git Stash and Tags  
Explore our wide range of courses and connect with our community on Discord for assistance and insights!

---

### Git Diff

`git diff` is an essential command that shows the differences between various commits, files, or branches. It compares changes made in different versions of files and displays the differences.

#### How to Read a Diff:
- **a** → Original file
- **b** → Modified file
- `---` represents file A (original)
- `+++` represents file B (modified)
- `@@` indicates the line number where changes occurred.

Git provides a preview of the changes made in different file versions, helping developers understand where modifications took place.

#### Key Diff Commands:

- **Comparing Working Directory and Staging Area**  
  ```bash
  git diff
  ```  
  This shows unstaged changes in the working directory.

- **Comparing Staging Area with the Repository**  
  ```bash
  git diff --staged
  ```  
  This shows changes between the last commit and the staging area.

- **Comparing Branches**  
  ```bash
  git diff <branch-name-one> <branch-name-two>
  ```  
  Or  
  ```bash
  git diff branch-name-one..branch-name-two
  ```  
  This compares two branches.

- **Comparing Specific Commits**  
  ```bash
  git diff <commit-hash-one> <commit-hash-two>
  ```  
  Use this to compare two specific commits.

---

### Git Stash

`git stash` is a useful feature that temporarily saves your work without committing it. It allows you to store uncommitted changes when you need to switch branches or work on something else without losing your progress.

#### Key Stash Commands:

- **Saving Changes Temporarily**  
  ```bash
  git stash
  ```  
  This saves your changes in a temporary stash.

- **Naming the Stash**  
  ```bash
  git stash save "Work in progress on feature X"
  ```  
  Give your stash a name for easy reference.

- **Viewing the Stash List**  
  ```bash
  git stash list
  ```  
  This shows all stashes.

- **Applying the Stash**  
  ```bash
  git stash apply
  ```  
  This reapplies the most recent stash.

- **Applying a Specific Stash**  
  ```bash
  git stash apply stash@{0}
  ```  
  Use the stash ID to apply a specific stash.

- **Applying and Dropping a Stash**  
  ```bash
  git stash pop
  ```  
  This applies the stash and removes it from the stash list.

- **Clearing the Stash**  
  ```bash
  git stash clear
  ```  
  Clears all stashes.

---

### Git Tags

Tags in Git mark specific points in your project’s history. They’re commonly used to identify key releases or important commits. Unlike branches, tags do not change over time—they serve as a permanent reference.

#### Key Tag Commands:

- **Creating a Tag**  
  ```bash
  git tag <tag-name>
  ```  
  This creates a simple tag for the current commit.

- **Creating an Annotated Tag**  
  ```bash
  git tag -a <tag-name> -m "Release 1.0"
  ```  
  This creates an annotated tag with a description.

- **Tagging a Specific Commit**  
  ```bash
  git tag <tag-name> <commit-hash>
  ```  
  Tags a specific commit using its hash.

- **Listing All Tags**  
  ```bash
  git tag
  ```  
  Lists all the tags in the repository.

- **Pushing Tags to a Remote Repository**  
  ```bash
  git push origin <tag-name>
  ```  
  Pushes the tag to the remote repository.

- **Deleting a Tag**  
  ```bash
  git tag -d <tag-name>
  ```  
  Deletes the tag locally.

- **Deleting a Tag on the Remote Repository**  
  ```bash
  git push origin :<tag-name>
  ```  
  Deletes the tag from the remote repository.

---

### Conclusion

In this section, we explored the differences between Git diff, stash, and tags. While they may not be the most frequently used commands, they are powerful tools for managing code changes and version history. By mastering these, you can improve your Git workflow and collaboration in projects.
