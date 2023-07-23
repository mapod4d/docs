# GITHUB MAPOD4D

Below is the workflow used by the community. This workflow is mandatory, and pull requests that do not follow it will not be accepted!

## 1. Definitions

- **MAPOD4D Repository:** a repository saved in the _GitHub_ profile of the **MAPOD4D** organization.
- **Personal Repository:** a repository saved in your own _GitHub_ profile.
- **Local Repository:** a repository saved on your PC's mass storage (e.g., Hard Disk, SSD).
- **Repo:** shorthand for repository.
- **Fork:** a copy of a repository from another user or organization to your own _GitHub_ profile.

## 2. Before Starting

- **Create a Workspace:** If you don't already have a workspace, create one. This will be used to store all the folders you use for community work (e.g., _development_area_).

- **Fork the MAPOD4D Repository:** To fork a repository, simply click the **_Fork_** button at the top right of the **Github** page of the repository. This will create a copy of the **MAPOD4D repository** in your _GitHub_ profile, which we will now call the **personal repository**.

<!-- add for large files -->

- **Get the Forked Repository Link:** Access your _GitHub_ profile and then your **personal repository**. Copy the link by clicking the green "**Code**" button, and a dropdown menu will appear containing the link.<!-- green button image --> The link will appear in the following format:

         https://github.com/[username]/[repository_name].git

- **Create the Repository Locally:**

        git clone --mirror https://github.com/[username]/[repository_name].git

- **Access the Repository:**

        cd [repository_name]

- **Set Up Remote References in the Local Repository:** To set up remotes, use the following commands:

        git remote add mapod4d https://github.com/mapod4d/[repository_name].git

  These commands will establish a connection to the main repository only for pulling data. **ATTENTION:** If you are an administrator, set push to NO PUSH (see references in the [**Are You an Administrator?**](#are-you-an-administrator) section).

Once our workspace is ready, we can start working on our tasks.

## 3. Simple Task Management

1.  Switch back to the master branch:

        git checkout master

1.  Fetch possible new updates from the main repository:

        git pull mapod4d master

    - Resolve conflicts if any.

1.  Clean the repository cache:

        git pull --prune

1.  Apply the changes to the local repository:

        git push origin master

1.  Create the dev branch (**if already created, proceed to step 6**):

        git branch dev

1.  Switch to the dev branch (**if did't create, proceed to step 5**):

        git checkout dev

1.  Merge the master into dev:

        git merge master

    - Resolve any conflicts.
    - Perform the task.
    - Add and commit whenever you reach work milestones:

          git add [file_name + .extension]

          git commit -m "[insert commit title]"

    - Finish working on the task.

1.  Push the changes to your personal repo:

        git push origin dev

_Repeat from step 1 until the task is completed._

## 4. Finished with the Task?

1.  Switch back to the master branch:

        git checkout master

1.  Fetch possible new updates from the main repository:

        git pull mapod4d master

    - Resolve conflicts if any.

1.  Merge dev into master:

        git merge dev

1.  Push the changes to your personal repo:

        git push origin master

    - Resolve conflicts if any.

1.  Proceed to the **What Happens Now?** section.

## 5. What Happens Now?

### Open a Pull Request

Access GitHub and create a **_Pull Request_** by clicking on **_Contribute_** and then clicking the green **Create Pull Request** button. In the new page, enter the task as the title, and then click the **Create Pull Request** button.

### What about the dev branch?

Before deleting the branch you worked on, wait for confirmation that the **_Pull Request_** has been accepted.

### Are You an Administrator?

- **Set Up Remotes in the Local Repo:** To set up remotes, use the following commands:

        git remote add mapod4d https://github.com/mapod4d/[repository_name].git
        git remote set-url --push mapod4d NOPUSH

  These commands will establish a connection to the main repository only for pulling data.