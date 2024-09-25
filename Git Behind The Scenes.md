### Git Behind the Scenes: Learn and Community

Explore our diverse range of courses! We also have a **Discord community** where you can ask questions and get help from fellow learners.

---

### Git Behind the Scenes

Git is a **version control system** designed to track changes in files and folders over time. It’s an essential tool for managing code efficiently. In this section, we’ll dive into how Git works behind the scenes, providing a glimpse into its core structure.

#### Git Snapshots
In Git, a **snapshot** represents a specific version of your code at a given point in time. Each snapshot is uniquely identified by a **hash code**, a string of characters generated based on the contents of the snapshot. These snapshots allow you to view or revert to previous versions of your code.

Although we refer to them as "snapshots," they aren’t images. Instead, Git stores these snapshots in a locally stored **key-value database**. Every piece of information is stored as an **object**, each with its unique hash code. These objects play a key role in Git's efficiency.

---

### The Three Key Git Objects (The 3 Musketeers)
The internal structure of Git revolves around three main objects:

1. **Commit Object**
2. **Tree Object**
3. **Blob Object**

Let’s break down each one:

#### 1. Commit Object
A **commit object** represents a specific commit in your Git project. It contains critical metadata that helps you track changes. A typical commit object includes:
- **Tree Object** (represents the state of the project at that commit)
- **Parent Commit Object** (links to the previous commit)
- **Author** (the person who wrote the code)
- **Committer** (the person who committed the code)
- **Commit Message** (describes the changes made)

Each commit is stored in the `.git` folder.

#### 2. Tree Object
The **tree object** serves as a container for all the files and directories in your project at the time of the commit. It organizes the project’s structure and includes:
- **File Mode** (permissions for the file)
- **File Name**
- **File Hash** (unique identifier for the file)
- **Parent Tree Object** (reference to the parent directory)

Essentially, the tree object maps the files to their corresponding hash values, which allows Git to quickly find files.

#### 3. Blob Object
The **blob object** is the simplest of the three. It stores the **actual content** of a file. The blob object is referenced in the tree object, but unlike the tree or commit objects, it only holds raw data, like the file's contents.

---

### Useful Git Commands
Here are some useful commands to explore Git’s internals:

1. **Show the raw commit object**:
   ```bash
   git show -s --pretty=raw <commit-hash>
   ```

2. **Retrieve the tree object from the commit**:
   Grab the tree ID from the previous command and use it in:
   ```bash
   git ls-tree <tree-id>
   ```

3. **Retrieve the blob object (file contents)**:
   Use the tree ID to get the blob object:
   ```bash
   git show <blob-id>
   ```

4. **Display the commit object**:
   To see the entire commit object:
   ```bash
   git cat-file -p <commit-id>
   ```

These commands allow you to navigate through the internals of Git, helping you see how each commit, tree, and blob object ties together to form the repository’s history.

--- 

With this understanding of Git’s core objects and internal structure, you'll have a much deeper appreciation of how Git efficiently tracks changes and manages version history!
