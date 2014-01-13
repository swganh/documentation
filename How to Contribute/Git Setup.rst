Installing and Setting Up Git
============

At the heart of GitHub is an open source version control system (VCS) called Git*. Created by the same team that created Linux, Git is responsible for everything GitHub related that happens locally on your computer.

`Download and install the latest version of Git. 
<http://git-scm.com/downloads/>`_.

Use the default options for each step.

Setup Git
----------

Now that you have Git installed, it's time to configure your settings. To do this you need to open Git Bash (not the Windows command line).

Git Configuration
----------

**Username**

First you need to tell git your name, so that it can properly label the commits you make.

.. code-block:: bash

	git config --global user.name "Your Hame Here"
	# Sets the default name for git to use when you commit

**Email**

Git saves your email address into the commits you make. We use the email address to associate your commits with your GitHub account.

.. code-block:: bash

	git config --global user.email "your_email@example.com"
	# Sets the default email for git to use when you commit

Your email address for Git should be the same one associated with your GitHub account. If it is not, see this guide for help adding additional emails to your GitHub account. If you want to keep your email address hidden, this guide may be useful to you.


Password caching
----------

The last option we need to set will tell git that you don't want to type your username and password every time you talk to a remote server.

Tip: You need git 1.7.10 or newer to use the credential helper To use this option, you need install a credential helper.

GitHub for Windows includes this helper, and provides a git shell so you don't need to install and configure git manually.

If you don't want to use GitHub for Windows, you can download the helper for your OS here:

Windows Vista, 7, & 8 (.NET 4.0 required) Source Unzip the file and run the git-credential-winstore.exe program inside. This will start up the helper and update your git config to use it.