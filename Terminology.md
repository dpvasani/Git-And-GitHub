### Terminology: Learn and Community

Explore our diverse range of courses! We also have a **Discord community** where you can ask questions and receive support from fellow learners.

When it comes to Git, the terminology can differ from everyday language. For instance, what most people refer to as a **folder**, Git users call a **repository**. Similarly, instead of an **alternative timeline**, they use the term **branch**. While I personally think "alternative timeline" sounds cooler, Git's terminology is the standard! 😁

---

### Git and GitHub

#### Checking Your Git Version
To find out what version of Git is installed on your system, run the following command in your terminal:

```bash
git --version
```

This will display your installed Git version. From my experience, Git is quite stable and usually avoids breaking changes.

#### What is a Repository?
A **repository** is a collection of files and directories stored together, allowing you to manage your code effectively. While it resembles a regular folder on your computer, it offers more functionality—it can hold files, folders, and even other repositories. Think of a repository as a container for all your code.

It's important to note that tracking a repository with Git differs from just having software on your system. You can check the current state of your repository at any time by running:

```bash
git status
```

#### Understanding Your Config Settings
GitHub provides a plethora of settings you can customize, such as your username and email. When you make a commit, Git records this information. All your configurations are stored in a `.gitconfig` file. You can set global options as well as repository-specific settings.

Let’s configure your email and username. I recommend creating a GitHub account first and using that email and username:

```bash
git config --global user.email "your-email@example.com"
git config --global user.name "Your Name"
```

You can verify your configuration settings with:

```bash
git config --list
```

This command will display all the settings you've modified.

---

### Creating a Repository
Creating a repository involves initializing a new folder on your system to track with Git. It’s simply a regular folder for your project, but by using Git, you're asking it to keep track of changes. Use the following commands:

```bash
git init
git status
```

The `git init` command initializes a new repository by adding a hidden `.git` folder to your project.

#### Understanding Commits
A **commit** is your way of saving changes to your repository. It acts as a snapshot of your code at a specific time. When you commit, you instruct Git to permanently store your changes, allowing you to revisit that state later.

Here's how the usual flow works:

1. Initialize a new repository with `git init`.
2. Stage your files with `git add`.
3. Commit your changes with `git commit`.
4. Push your commits to GitHub using `git push`.

#### Staging Files
To stage files for tracking, use:

```bash
git add <file1> <file2>
git status
```

This command stages your files, indicating that they are ready to be committed.

#### Committing Changes
To commit your staged changes, use:

```bash
git commit -m "Your commit message"
git status
```

The `-m` flag allows you to include a brief message describing your changes. If you omit the `-m` flag, your default editor (often VIM) will open for you to enter a message. We'll change this to VSCode in a later section.

#### Viewing Commit Logs
To see the history of your commits, run:

```bash
git log
```

This command displays all commits made to the repository. You can simplify the output with the `--oneline` flag to view just the commit messages.

☕️ - Check the Git log documentation for more details.

Using **atomic commits** ensures that each commit is a self-contained unit of work. This way, if one commit encounters an issue, you can revert to a previous commit without complications, helping to maintain a clear and organized project history.

---

### Changing Your Default Code Editor
If you'd like to set VSCode as your default code editor, run:

```bash
git config --global core.editor "code --wait"
```

---

### Using .gitignore
The **.gitignore** file specifies which files and folders Git should ignore, preventing them from being tracked. Create a `.gitignore` file and list the files or folders you want to exclude, for example:

```
node_modules
.env
.vscode
```

Now, running `git status` won't show these ignored folders as being tracked.

---

### Conclusion
In this section, we've covered the basics of Git and how to use it for tracking changes in your files and folders. You’ve also learned about essential commands like `init`, `add`, `commit`, and `log`. By the end of this guide, you should feel confident in using Git effectively to manage your code.
