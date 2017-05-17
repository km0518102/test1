# 大標題test1

## 中標題

### 小標題

#### 小小標題

Test測試用

Last login: Wed May 17 18:41:04 on console
Mike-Hungde-MacBook-Pro:~ mikehung$ dir
-bash: dir: command not found
Mike-Hungde-MacBook-Pro:~ mikehung$ ls
Applications	Downloads	Music		Untitled.ipynb	Untitled3.ipynb
Desktop		Library		Pictures	Untitled1.ipynb
Documents	Movies		Public		Untitled2.ipynb
Mike-Hungde-MacBook-Pro:~ mikehung$ cd Desktop
Mike-Hungde-MacBook-Pro:Desktop mikehung$ ls
Mike-Hungde-MacBook-Pro:Desktop mikehung$ mkdir MyGit
Mike-Hungde-MacBook-Pro:Desktop mikehung$ ls
MyGit
Mike-Hungde-MacBook-Pro:Desktop mikehung$ open
Usage: open [-e] [-t] [-f] [-W] [-R] [-n] [-g] [-h] [-s <partial SDK name>][-b <bundle identifier>] [-a <application>] [filenames] [--args arguments]
Help: Open opens files from a shell.
      By default, opens each file using the default application for that file.  
      If the file is in the form of a URL, the file will be opened as a URL.
Options: 
      -a                Opens with the specified application.
      -b                Opens with the specified application bundle identifier.
      -e                Opens with TextEdit.
      -t                Opens with default text editor.
      -f                Reads input from standard input and opens with TextEdit.
      -F  --fresh       Launches the app fresh, that is, without restoring windows. Saved persistent state is lost, excluding Untitled documents.
      -R, --reveal      Selects in the Finder instead of opening.
      -W, --wait-apps   Blocks until the used applications are closed (even if they were already running).
          --args        All remaining arguments are passed in argv to the application's main() function instead of opened.
      -n, --new         Open a new instance of the application even if one is already running.
      -j, --hide        Launches the app hidden.
      -g, --background  Does not bring the application to the foreground.
      -h, --header      Searches header file locations for headers matching the given filenames, and opens them.
      -s                For -h, the SDK to use; if supplied, only SDKs whose names contain the argument value are searched.
                        Otherwise the highest versioned SDK in each platform is used.
Mike-Hungde-MacBook-Pro:Desktop mikehung$ open .
Mike-Hungde-MacBook-Pro:Desktop mikehung$ git init
Initialized empty Git repository in /Users/mikehung/Desktop/.git/
Mike-Hungde-MacBook-Pro:Desktop mikehung$ ls -al
total 16
drwx------+  6 mikehung  staff   204  5 17 18:54 .
drwxr-xr-x+ 25 mikehung  staff   850  5 15 18:49 ..
-rw-r--r--@  1 mikehung  staff  6148  5 17 18:53 .DS_Store
drwxr-xr-x   9 mikehung  staff   306  5 17 18:54 .git
-rw-r--r--   1 mikehung  staff     0  5 13 19:44 .localized
drwxr-xr-x   2 mikehung  staff    68  5 17 18:53 MyGit
Mike-Hungde-MacBook-Pro:Desktop mikehung$ ls -al
total 16
drwx------+  6 mikehung  staff   204  5 17 18:54 .
drwxr-xr-x+ 25 mikehung  staff   850  5 15 18:49 ..
-rw-r--r--@  1 mikehung  staff  6148  5 17 18:53 .DS_Store
drwxr-xr-x   9 mikehung  staff   306  5 17 18:54 .git
-rw-r--r--   1 mikehung  staff     0  5 13 19:44 .localized
drwxr-xr-x   2 mikehung  staff    68  5 17 18:53 MyGit
Mike-Hungde-MacBook-Pro:Desktop mikehung$ echo test > octocat.txt
Mike-Hungde-MacBook-Pro:Desktop mikehung$ open .
Mike-Hungde-MacBook-Pro:Desktop mikehung$ git add octocat.txt
Mike-Hungde-MacBook-Pro:Desktop mikehung$ git status
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   octocat.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	.DS_Store
	.localized

Mike-Hungde-MacBook-Pro:Desktop mikehung$ git commit -m "Test Commit"
[master (root-commit) 54eb299] Test Commit
 Committer: Mike Hung <mikehung@Mike-Hungde-MacBook-Pro.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 1 insertion(+)
 create mode 100644 octocat.txt
Mike-Hungde-MacBook-Pro:Desktop mikehung$ echo test > blue_octocat.txt
Mike-Hungde-MacBook-Pro:Desktop mikehung$ echo test > red_octocat.txt
Mike-Hungde-MacBook-Pro:Desktop mikehung$ open .
Mike-Hungde-MacBook-Pro:Desktop mikehung$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	.DS_Store
	.localized
	blue_octocat.txt
	red_octocat.txt

nothing added to commit but untracked files present (use "git add" to track)
Mike-Hungde-MacBook-Pro:Desktop mikehung$ git add *.txt
Mike-Hungde-MacBook-Pro:Desktop mikehung$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   blue_octocat.txt
	new file:   red_octocat.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	.DS_Store
	.localized

Mike-Hungde-MacBook-Pro:Desktop mikehung$ git commit -m 'Add all files'
[master ffd8c03] Add all files
 Committer: Mike Hung <mikehung@Mike-Hungde-MacBook-Pro.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 2 files changed, 2 insertions(+)
 create mode 100644 blue_octocat.txt
 create mode 100644 red_octocat.txt
Mike-Hungde-MacBook-Pro:Desktop mikehung$ git log
commit ffd8c0300851fd6defe9e87d28ae134ac6ad03fe
Author: Mike Hung <mikehung@Mike-Hungde-MacBook-Pro.local>
Date:   Wed May 17 19:04:12 2017 +0800

    Add all files

commit 54eb29980371441db72bbe08c5ee2e77b8258492
Author: Mike Hung <mikehung@Mike-Hungde-MacBook-Pro.local>
Date:   Wed May 17 19:00:18 2017 +0800

    Test Commit
Mike-Hungde-MacBook-Pro:Desktop mikehung$ ls -al
total 40
drwx------+  9 mikehung  staff   306  5 17 19:02 .
drwxr-xr-x+ 25 mikehung  staff   850  5 15 18:49 ..
-rw-r--r--@  1 mikehung  staff  6148  5 17 19:02 .DS_Store
drwxr-xr-x  12 mikehung  staff   408  5 17 19:04 .git
-rw-r--r--   1 mikehung  staff     0  5 13 19:44 .localized
drwxr-xr-x   2 mikehung  staff    68  5 17 18:53 MyGit
-rw-r--r--   1 mikehung  staff     5  5 17 19:01 blue_octocat.txt
-rw-r--r--   1 mikehung  staff     5  5 17 18:56 octocat.txt
-rw-r--r--   1 mikehung  staff     5  5 17 19:02 red_octocat.txt
Mike-Hungde-MacBook-Pro:Desktop mikehung$ git remote add orgin https://github.com/km0518102/MyGit.git
Mike-Hungde-MacBook-Pro:Desktop mikehung$ git push -u origin master
fatal: 'origin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
Mike-Hungde-MacBook-Pro:Desktop mikehung$ git push -u origin master
fatal: 'origin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
Mike-Hungde-MacBook-Pro:Desktop mikehung$ git remote add origin https://github.com/km0518102/MyGit.git
Mike-Hungde-MacBook-Pro:Desktop mikehung$ git push -u origin master
Username for 'https://github.com': km0518102
Password for 'https://km0518102@github.com': 
Counting objects: 5, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (5/5), 471 bytes | 0 bytes/s, done.
Total 5 (delta 0), reused 0 (delta 0)
To https://github.com/km0518102/MyGit.git
 * [new branch]      master -> master
Branch master set up to track remote branch master from origin.
Mike-Hungde-MacBook-Pro:Desktop mikehung$ git log
commit ffd8c0300851fd6defe9e87d28ae134ac6ad03fe
Author: Mike Hung <mikehung@Mike-Hungde-MacBook-Pro.local>
Date:   Wed May 17 19:04:12 2017 +0800

    Add all files

commit 54eb29980371441db72bbe08c5ee2e77b8258492
Author: Mike Hung <mikehung@Mike-Hungde-MacBook-Pro.local>
Date:   Wed May 17 19:00:18 2017 +0800

    Test Commit
Mike-Hungde-MacBook-Pro:Desktop mikehung$ ls -all
total 40
drwx------+  9 mikehung  staff   306  5 17 19:02 .
drwxr-xr-x+ 25 mikehung  staff   850  5 15 18:49 ..
-rw-r--r--@  1 mikehung  staff  6148  5 17 19:02 .DS_Store
drwxr-xr-x  12 mikehung  staff   408  5 17 19:13 .git
-rw-r--r--   1 mikehung  staff     0  5 13 19:44 .localized
drwxr-xr-x   2 mikehung  staff    68  5 17 18:53 MyGit
-rw-r--r--   1 mikehung  staff     5  5 17 19:01 blue_octocat.txt
-rw-r--r--   1 mikehung  staff     5  5 17 18:56 octocat.txt
-rw-r--r--   1 mikehung  staff     5  5 17 19:02 red_octocat.txt
Mike-Hungde-MacBook-Pro:Desktop mikehung$ git pull origin master
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
From https://github.com/km0518102/MyGit
 * branch            master     -> FETCH_HEAD
   ffd8c03..9ac4cdf  master     -> origin/master
Updating ffd8c03..9ac4cdf
Fast-forward
 octocat.txt | 3 +++
 1 file changed, 3 insertions(+)
Mike-Hungde-MacBook-Pro:Desktop mikehung$ git log
commit 9ac4cdff900ee795c368a4f1ad155507de0c675f
Author: km0518102 <km0518102@gcloud.csu.edu.tw>
Date:   Wed May 17 19:14:26 2017 +0800

    Update octocat.txt

commit ffd8c0300851fd6defe9e87d28ae134ac6ad03fe
Author: Mike Hung <mikehung@Mike-Hungde-MacBook-Pro.local>
Date:   Wed May 17 19:04:12 2017 +0800

    Add all files

commit 54eb29980371441db72bbe08c5ee2e77b8258492
Author: Mike Hung <mikehung@Mike-Hungde-MacBook-Pro.local>
Date:   Wed May 17 19:00:18 2017 +0800

    Test Commit
Mike-Hungde-MacBook-Pro:Desktop mikehung$ cat octocat.txt
test

adfskl
adfa
Mike-Hungde-MacBook-Pro:Desktop mikehung$ 
