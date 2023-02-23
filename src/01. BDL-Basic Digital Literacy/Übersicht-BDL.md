# Basic Digital Literacy

> Duration: **8 days** or **2 weeks**

- [WebDev](#webdev)
- [[#Viewing & Navigating]]
- [[#Creating & Manipulating]]
- [Installing](#installing)
- [[#BDL - Assessment I]]
- [Versioning](#versioning)
- [Publishing](#publishing)
- [Collaborating](#collaborating)
- [Review](#review)
- [[#BDL - Assessment II]]

## WebDev

| Topic                                 | Content                                                                                                       |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| _Course intro presentation (with PM)_ | - Technical setup of the laptops<br />- Web Dev curriculum overview                                           |
| _Intro to Linux_                      | - History, from Unix to Linus<br />- Distributions<br />- Desktop Environments                                |
| _Web Development_                     | - What is Web Development<br />- Frontend, Backend, Fullstack<br />- Markup languages & programming languages |


## Viewing & Navigating

| Topic                                               | Content                                                                                                                                                                        | Exercises                                                                                             |
| --------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------- |
| _Introduction_                                      | - The terminal prompt line                                                                                                                                                     |                                                                                                       |
| _Quick overview of paths in the a unix filesystem:_ | - The 'pwd' command<br />- The '/' folder<br />- The home folder and `~` shortcut                                                                                              |                                                                                                       |
| _Moving around_                                     | - The `cd` command<br />- Absolute paths (beginning with `/`)<br />- Relative paths: the `..` shortcut, navigating into sub folders<br />- The last directory shortcut: `cd -` | [BDL-navigating-movingaround](https://github.com/DigitalCareerInstitute/BDL-navigating-movingaround/) |
| _Reading directories_                               | - The `ls` command<br />- List directories and files: `ls -l`<br />- Showing hidden files: `ls -a` flag<br />- Combining flags `ls -la`<br />- The `ll` shortcut               | [BDL-viewing-read_dir](https://github.com/DigitalCareerInstitute/BDL-viewing-read_dir/)               |
| _Reading files_                                     | - The 'less' command<br />- The current directory shortcut: '.'                                                                                                                | [BDL-navigating-readingfiles](https://github.com/DigitalCareerInstitute/BDL-navigating-readingfiles/) |
| _Getting help_                                      | - The `man` command<br />- The `help` command                                                                                                                                  | [BDL-viewing-help](https://github.com/DigitalCareerInstitute/BDL-viewing-help/)                       |


## Creating & Manipulating

| Topic                          | Content                                                                                                                                                                 | Exercises                                                                                        |
| ------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| _Introduction_                 | - Organizing our files and folders                                                                                                                                      |                                                                                                  |
| _Creating Directories & files_ | - The `mkdir` command<br />- The `touch` command<br />- `nano` text editor                                                                                              | [BDL-creating-dir](https://github.com/DigitalCareerInstitute/BDL-creating-dir)                   |
| _Basic Authoring (Markdown)_   | - Text (bold, italic)<br />- Quotes<br />- Headlines<br />- Lists<br />- Preformatted text<br />- Markdown documentation                                                | [BDL-creating-markdown](https://github.com/DigitalCareerInstitute/BDL-creating-markdown/)        |
| _Introduction_                 | - The terminal cheat sheet                                                                                                                                              |                                                                                                  |
| _Copying_                      | - The `cp` command<br />- Copying a directory with `cp -r`<br />- Copying multiple paths into one location<br />- Using the `*` wildcard to copy the contents of a dir  | [BDL-manipulating-copying](https://github.com/DigitalCareerInstitute/BDL-manipulating-copying/)  |
| _Deleting_                     | - The `rm` command<br />- Removing directories with `rm -r`<br />- Removing directories with `rmdir`<br />- Force removing with `rm -f`<br />- Combining flags `rm -rf` | [BDL-manipulating-deleting](https://github.com/DigitalCareerInstitute/BDL-manipulating-deleting) |
| _Moving & Renaming_            | - The `mv` command<br />- Renaming with `mv`                                                                                                                            | [BDL-manipulating-mv](https://github.com/DigitalCareerInstitute/BDL-manipulating-mv/)            |


## Installing

| Topic                                       | Content                                                                                                                                                                                                                                                                                                                                                                                                                                     | Exercises                                                                           |
| ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| _Introduction: Package managers (npm, apt)_ |                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                     |
| _Using `apt`_                               | - Using the `sudo` command to allow installation<br />- Updating package list with `sudo apt update`<br />- Installing with `sudo apt install <package name>`<br />- Clearing unnecessary files with `sudo apt autoremove`<br />- Uninstalling with `sudo apt remove <package name>`                                                                                                                                                        | [BDL-installing-apt](https://github.com/DigitalCareerInstitute/BDL-installing-apt/) |
| _Using `npm`_                               | - Installing packages globally with `npm install -g <package name>`<br />- Using `npm list` to see installed packages and their dependencies<br />- Uninstalling with `npm uninstall -g <package name>`<br />- Updating using `nvm install <version_number>` and `nvm install --lts` (nvm documentation)<br />- Side note: what does "LTS" mean in versions<br />- Setting the version used by default `nvm alias default <version_number>` | [BDL-installing-npm](https://github.com/DigitalCareerInstitute/BDL-installing-npm)  |


## BDL - Assessment I


| Name                 | Links                                                                                                                                                                       |
| -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| _BDL - Assessment I_ | [English](<https://github.com/DigitalCareerInstitute/BDL-Review-Basic>)<br />[Deutsch](<https://github.com/DigitalCareerInstitute/BDL-Review-Basic/blob/main/README_DE.md>) |

## Versioning

| Topic            | Content                                                                                                                                                                                                                                                              | Exercises                                                                                     |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| _Introduction_   | - Version Control Systems (VCS)                                                                                                                                                                                                                                      |                                                                                               |
| _Initializing_   | - The `git` program<br />- Starting a repository with `git init`<br />- The `.git` folder                                                                                                                                                                            |                                                                                               |
| _Basic workflow_ | - Checking the status with `git status`<br />- Staging files with `git add`<br />- Using the `.` shortcut to add all files<br />- Creating a commit with `git commit`<br />- Viewing the history with `git log`<br />- Quick commits with `git commit -am <message>` | [BDL-versioning-workflow](https://github.com/DigitalCareerInstitute/BDL-versioning-workflow/) |
| _Branching_      | - Moving through the history with `git checkout <commit hash>`<br />- Branching out with `git checkout -b <branch name>`<br />- Viewing branches with `git branch`<br />- Merging with `git merge`                                                                   | [BDL-versioning-branches](https://github.com/DigitalCareerInstitute/BDL-versioning-branches/) |


## Publishing

| Topic                                            | Content                                                                                                                                                                                                                                                                                          | Exercises                                                                                                                                                                                        |
| ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| _Introduction_                                   | - How the internet works (quick overview of TCP/IP)                                                                                                                                                                                                                                              |                                                                                                                                                                                                  |
| _Internet Basics: Quick anatomy of a URL_        | - The protocol (brief overview): HTTP, HTTPS, SSH, FTP<br />- The address / host: IP addresses, DNS, domain name<br />- The resource path                                                                                                                                                        |                                                                                                                                                                                                  |
| _Github_                                         | - The Github website<br />- Connecting to GitHub with SSH<br />- Creating a repository on GH (w. readme)<br />- GitHub Publishing                                                                                                                                                                | [BDL-publishing-github](https://github.com/DigitalCareerInstitute/BDL-publishing-github/)                                                                                                        |
| _Advanced Authoring (Github Flavoured Markdown)_ | - External links<br />- Internal links (anchors)<br />- Images<br />- Emoji<br />- Checkboxes<br />- Tables                                                                                                                                                                                      | [BDL-publishing-authoring](https://github.com/DigitalCareerInstitute/BDL-publishing-authoring)                                                                                                   |
| _Locals and Remotes_                             | - Local repository vs. Remote repository<br />- Creating a repository on GH (no readme)<br />- Checking a repository's remotes: `git remote -v`<br />- Adding a remote: `git remote add <name> <url>`<br />- Pushing a branch for the first time:<br />`git push -u <remote name> <branch name>` | [BDL-publishing-changes](https://github.com/DigitalCareerInstitute/BDL-publishing-changes)<br /><br />[BDL-publishing-remotes](https://github.com/DigitalCareerInstitute/BDL-publishing-remotes) |


## Collaborating

| Topic                                                | Content                                                                                                                                                      | Exercises                                                                                            |
| ---------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------- |
| _Introduction: Working together with git and github_ |                                                                                                                                                              | [introduction-to-github](https://lab.github.com/githubtraining/introduction-to-github)               |
| _Conflicts_                                          | - Making changes to the same file (when merging)<br />- Resolving pull conflicts                                                                             | [BDL-collaborating-conflicts](https://github.com/DigitalCareerInstitute/BDL-collaborating-conflicts) |
| _Reviewing_                                          | - Creating a Pull Request on GitHub<br />- Pull Request review process<br />- Dealing with conflicts in Pull Request (Test merging)<br />- Merging on GitHub | [BDL-collaborating-review](https://github.com/DigitalCareerInstitute/BDL-collaborating-review/)      |


## Review

| Topic                   | Content                                                    |
| ----------------------- | ---------------------------------------------------------- |
| _Review and assessment_ | - Review basic concepts<br />- Discuss basic concepts, Q&A |


## BDL - Assessment II


| Name                  | Links                                                                                                                                                                             |
| --------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| _BDL - Assessment II_ | [English](<https://github.com/DigitalCareerInstitute/BDL-Review-Advanced>)<br />[Deutsch](<https://github.com/DigitalCareerInstitute/BDL-Review-Advanced/blob/main/README_DE.md>) |
