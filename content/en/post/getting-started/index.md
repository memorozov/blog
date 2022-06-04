---
title: Git version control.
subtitle: Here you can familiarize yourself with the git version control system. All the necessary information for working with git is provided here.

# Summary for listings and search engines
summary: Git version control.Here you can familiarize yourself with the git version control system. All the necessary information for working with git is provided here.

# Link this post with a project
projects: []

# Date published
date: '2020-12-13T00:00:00Z'

# Date updated
lastmod: '2020-12-13T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin
  - 吳恩達

tags:
  - Academic
  - 开源

categories:
  - Demo
  - 教程
---

##Version control systems. General concepts



Version Control Systems (VCS) are used when several people work on one project. Usually, the main project tree is stored in a local or remote repository, to which access is configured for project participants. When making changes to the project content, the version control system allows you to fix them, combine changes made by different project participants, roll back to any earlier version of the project, if required.



In classical version control systems, a centralized model is used, assuming a single repository for storing files. Most version control functions are performed by a special server. The project participant (user) receives the version of files he needs before starting work through certain commands. After making changes, the user places the new version in the repository. At the same time, previous versions are not deleted from the central repository and you can return to them at any time. The server may not save the full version of the modified files, but perform a so—called delta compression - save only changes between successive versions, which reduces the amount of data stored.



Version control systems support the ability to track and resolve conflicts that may arise when several people work on a single file. You can merge (merge) the changes made by different participants (automatically or manually), manually select the desired version, cancel the changes altogether

or lock files for modification. Depending on the settings, the lock does not allow other users to get a working copy or prevents changing the working copy of the file by means of the OS file system, thus providing privileged access to only one user working with the file.Version control systems can also provide additional, more flexible

functionality. For example, they can support working with multiple versions of a single file, keeping a common history of changes up to the point of branching versions and their own change histories of each branch. In addition, information is usually available about which of the participants, when and what changes were made. Usually this kind of information is stored in the change log, access to which can be restricted.



Unlike the classical ones, in distributed version control systems, a central repository is not mandatory.Among the classic VCS, the most famous are CVS, Subversion, and among the distributed ones — Git, Bazaar, Mercurial. The principles of their work are similar, they differ mainly in the syntax of the commands used in the work.



					##Basic git commands

				The most commonly used git commands:

	– creation of the main repository tree:

		git init

	– getting updates (changes) of the current tree from the central repository:

		git pull

	– sending all changes made to the local tree to the central repository:

		git push

	– view the list of modified files in the current directory:

		git status

	– view current changes:

		git diff

 

				Saving current changes:

	– add all modified and/or created files and/or directories:

		git add .

	– add specific modified and/or created files and/or directories:

		git add file_name

	delete a file and/or directory from the repository index (while the file and/or directory remains in the local directory):

		git rm file_name



				Saving added changes:

	– save all added changes and all modified files:

		git commit -am 'Commit description'

	-save the added changes with a comment through the built-in editor:

		git commit

	– creating a new branch based on the current one:

		git checkout -b_name

	– switching to a certain branch:

		git checkout branch name

	(when switching to a branch that is not yet in the local repository, it will be created and linked to the remote one)

	– sending changes of a specific branch to the central repository:

		git push origin_name

	– merging a branch with the current tree:

		git merge --no-ff_name



				Deleting a branch:

	– deleting a local branch already merged with the main tree:

		git branch -d branch_name

	– forced deletion of a local branch:

		git branch -D branch_name

	– deleting a branch from the central repository:

		git push origin :branch name









