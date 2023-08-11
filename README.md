## Git and GitHub Workflow:

### 1) Initial Setup:

1. **Initialize Repository and Add Remote:**
   ```bash
   git init
   git remote add origin <project_remote_url.git>
   ```

2. **Fetch Remote Branches:**
   Fetch remote branches to ensure you have the latest information from the remote repository:
   ```bash
   git fetch origin
   ```

3. **Create and Switch to a Working Branch:**
   Create and switch to a branch where you will work on your features or fixes:
   ```bash
   git checkout -b <working_branch_name>
   ```

4. **Create .gitignore File:**
   Create a `.gitignore` file to specify files and directories that Git should ignore. This is especially important to exclude sensitive or unnecessary files from being committed:
   ```bash
   touch .gitignore
   ```

### 2) Working on Your Code:

1. **Pull Recent Changes from Master:**
   Before starting work, pull the most recent changes from the main branch (e.g., `master`) to ensure your working branch is up-to-date:
   ```bash
   git checkout master
   git pull origin master
   git checkout <working_branch_name>
   ```

2. **Work on Your Code:**
   Begin coding and making changes to your project.

3. **Stage Changes and Commit:**
   Stage the changes you want to commit:
   ```bash
   git add .
   ```
   Commit the staged changes with a descriptive message:
   ```bash
   git commit -m "Add feature X" 
   ```

4. **Push Working Branch and Create Pull Request:**
   Push your changes to the remote repository:
   ```bash
   git push origin <working_branch_name>
   ```
   On GitHub, navigate to the repository and create a pull request from your working branch to the main branch (`master` or another branch). Provide a description of the changes you made.

5. **Iterate and Make Changes:**
   Reviewers may provide feedback on your pull request. Make any necessary changes, add new commits, and push the changes to the same working branch. The pull request will be updated automatically.

6. **Review and Merge:**
   Once your pull request is approved, a maintainer can merge it into the main branch.

7. **Clean Up:**
   After your changes are merged, you can delete the working branch (if no longer needed):
   ```bash
   git branch -d <working_branch_name>
   ```

And that's a basic Git and GitHub workflow! Remember that this is a simplified process, and real-world projects might involve additional complexities and steps based on your team's collaboration practices and project requirements.

## Useful commands:

Display commit tree with: 
```
git log --decorate --all --graph --oneline
```

# General Info:
`origin` is simply an alias for your remote repository
`remote` add origin <remote_repo_url.git>
translates to: remote repo's origin location is at 

`HEAD` is sentinal pointer to current branch
`master` is not a special branch name, just like any other
- best practice to use for maintaing stable version


Pull Requests are like an additional staging area, where other collaborators 
can review changes you've made on your branch BEFORE merging to master
- as a result, master branch is never being updated/pushed on directly
- updates to master will only come up PR approval 

___
## PRs and Feature branch Workflow
Here's a step-by-step guide on how to set up a feature branch, make commits, and create a pull request in a Git-based project. For this example, let's assume you're working on your Node.js, Express, and MongoDB blog app.

### Step 1: Create a Feature Branch

1. **Clone the Repository:**
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Create a New Branch:**
   ```bash
   git checkout -b feature/add-template-engine
   ```

   Replace `feature/add-template-engine` with a meaningful name for your feature.

### Step 2: Work on Your Feature

1. **Make Changes:**
   Make your code changes, such as setting up the Express-Edge template engine and refactoring the HTML pages.

2. **Stage Changes:**
   ```bash
   git add .
   ```

3. **Commit Changes:**
   ```bash
   git commit -m "Implement Express-Edge template engine and refactor HTML pages"
   ```

### Step 3: Push Feature Branch

1. **Push the Branch to Remote:**
   ```bash
   git push origin feature/add-template-engine
   ```

### Step 4: Create a Pull Request

1. **Open Repository on GitHub:**
   Navigate to your repository on GitHub.

2. **Click on "Pull Requests":**
   Click on the "Pull Requests" tab in your repository.

3. **Click on "New Pull Request":**
   Click on the "New Pull Request" button.

4. **Select Branches:**
   - On the "base" dropdown, select the branch you want to merge into (usually `main` or `master`).
   - On the "compare" dropdown, select your feature branch (`feature/add-template-engine`).

5. **Review Changes:**
   Review the changes you made and ensure they are as expected.

6. **Create Pull Request:**
   Click the "Create Pull Request" button.

7. **Add Details:**
   Fill in a title and description for your pull request. Describe the changes you made, why you made them, and any context that reviewers might need.

8. **Assign Reviewers:**
   Assign reviewers to your pull request if necessary.

9. **Create Pull Request:**
   Click the "Create Pull Request" button again to finalize the pull request.

### Step 5: Respond to Feedback

1. **Feedback and Review:**
   Other contributors will review your pull request. Address any feedback and make necessary changes by committing and pushing to the same feature branch.

2. **Discussion and Iteration:**
   Use the "Review Comments" and "Conversations" sections of the pull request to discuss changes and iterate on your code until it's approved.

### Step 6: Merge Pull Request

1. **Approval:**
   Once the pull request is approved by reviewers, you can click the "Merge Pull Request" button.

2. **Delete Branch:**
   After merging, you can choose to delete the feature branch if it's no longer needed.

That's it! You've successfully set up a feature branch, made commits, created a pull request, and merged your changes. Remember that this is a basic guide, and the actual process might vary depending on your team's workflow and the specific tools you're using.

