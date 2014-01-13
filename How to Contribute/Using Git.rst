Using Git to Contribute
============

If you have not already, you need to install and set up Git before you can perform these steps. If you need help with doing that see the Git Setup guide in the contributing folder.

The process you are about to preform is to fork a repository. Which makes a copy of it for your Github account. While SWGANH is open source, we do not allow direct commits. This is so developers can review the accuracy of the code. Accuracy can be a multitude of things, including: It's functionality, It's ability to perform, If it has bugs, or even if it is content is before publish 14.1.

Forking a Repository
----------

To start, you need to fork the repository you want to work with. In this instance we will say it is "swganh", the main server core. Forking adds a copy of the repository to your account. It is the first step in contributing.

.. image:: https://github-images.s3.amazonaws.com/help/Bootcamp-Fork.png

Cloning your Repository
----------

The next step is to clone your repository with Git. This is downloading it to your computer. To do so, run the following code.

.. code-block:: bash

	cd C:/Users/your-user-account/where-ever-you-want-your-repository
	# Goes to that specified location. That is where your files will get downloaded too.
	git clone https://github.com/**your-username**/swganh.git
	# Clones your fork of the repository into the current directory in terminal
	
	
Committing
----------

After you have changed a file in the source or added some content and you wish to submit it to be reviewed by the Developers, you can make a commit.

.. code-block:: bash

	git status
	# lists the status of the master. Telling you what files are different from the current public     
	# repository on github (if you used "cd C:/your-origin-whatever")

Find the files you want to change and type

.. code-block:: bash

	git add path-to-file.file-type
	# Adds the specified files.

If you alter multiple files and want to commit all of them, you can use:

.. code-block:: bash

	git add *
	
If you delete a file and want it to be completley removed/deleted from the repository when you commit, you can use:

.. code-block:: bash

	git rm * (or git rm path-to-file.file-type 
	
Then when you are ready to commit:

.. code-block:: bash
	git commit "Added Rebel Themepark"
	# Where the "" represents the commit message.

	
Submitting a Pull Request
----------

When you have a commit, or more than one commit ready to be sent for review you need to submit a "Pull Request" so developers can preview your changes, then approve or decline it. Do that on this page:

https://github.com/anhstudios/swganh/compare