# Git Workshop 🤓

## What to do?

* [Learn why you need Git and GitHub](#learn-why-you-need-git-and-gitHub)
* [Learn how to use Git](#learn-how-to-use-git)
* [Try it out!](#try-it-out)
* [Discuss usage in our lab](#discuss-usage-in-our-lab)
* [Learn about other cool things you can do on GitHub](#learn-about-other-cool-things-you-can-do-on-github)

## Learn why you need Git and GitHub

### Git, to keep track of versions of your projects and collaborate

http://www.cs.toronto.edu/~kenpu/articles/cs/git-intro.html

In summary:

* Be nice to yourself and your teammates
* Let Git be organized and remember your workflow instead of you
* Don't lose your code
* Be able to collaborate with other coders
* **Be a good and transparent scientist**

### GitHub, to share your Git repository with your favorite labmates

https://github.com/HartmannLab

We have a [GitHub organization](https://github.com/HartmannLab) for our group. This is a place to collect all our repositories and scripts. You can `git push` your repository there. Then, you and others in the group can access it anywhere, anytime. They may modify it without interfering with your local copy until you `git pull` the modified version from GitHub, and merge it with your own.  
Note that repositories in the `HartmannLab` can be private (only accessible by other members) or public (accessible by anyone on the internet). You can start developping your scripts in a private repository and make it public once you're satisfied with it (which should be when a manuscript is submitted at the latest).


## Learn how to use Git


### Beguinner's guide

https://www.freecodecamp.org/news/introduction-to-git-and-github/

### Branches

https://learngitbranching.js.org/
Some topics are quite advanced and you will hopefully never need them, but tutorials in `Main > Introduction Sequence` and in `Remote > Push & Pull -- Git Remotes!` are quite useful.


### Essential links

Don't memorize everything, just know what can be done and where to find the information. Here are a few life-saving links:

[Git guide: a handy cheatsheet](http://rogerdudler.github.io/git-guide/).  
[Oh shit git: when things go awry](https://ohshitgit.com/)


## Try it out


### Making changes online
A lot of operations can be done [on GitHub in your browser](https://docs.github.com/en/get-started/quickstart/hello-world).
Suggestion: test yourself by doing the following:

* Find the repository including this tutorial, in the HartmannLab on GitHub
* Create a new branch with your name and switch to it
* Add and commit a text file with your favorite joke, or a link to your favorite GIF (think `git add`)
* Create a pull request to add your changes to the `main` branch. 

### Making changes locally
The most flexible way to use Git is in the terminal (or *command prompt* for Windows users). If you need a refresher, here is [a command line cheat sheet](https://www.git-tower.com/blog/command-line-cheat-sheet/). Feel free to also use [a graphical user interface](https://www.hostinger.com/tutorials/best-git-gui-clients), but this is less standard and won't be covered here.  

Prerequisites (required only the first time you want to connect to GitHub):

1) You need a GitHub account and to be part of the HartmannLab orga. If you're seeing this page, congrats, you already fulfil these requirements.    
2) You will need to be able to run Git on your machine. In Linux and Mac, Git is installed by default. In Windows, you might need to [download and install Git first](https://docs.github.com/en/get-started/quickstart/set-up-git#setting-up-git). To know if Git is installed, open a terminal (or command prompt for Windows users) and type `git --version`.
3) Set up your user name and email 
``` 
git config --global user.name "Your Name"
git config --global user.email "your_email@whatever.com"
``` 
4) To secure your connection with GitHub and avoid typing your password all the time you can [generate an SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh). Note that you should clone GitHub repos using their SSH address starting with *git@*, for instance `git@github.com:HartmannLab/GitWorkshop.git` for this repo. 
5) You might be required to use 2-factor authentication. You can either validate your connection using your mobile phone or do it directly from your computer using [Authy desktop](https://authy.com/).

Suggestion: you can directly use Git for your projects, or test yourself by doing the following:

* Find the repository including this tutorial, in the HartmannLab on GitHub (think `git clone git@github.com:HartmannLab/GitWorkshop.git`)
* Clone the repository on your computer
* Create a new branch with your name and switch to it
* Add a text file with your favorite joke, or a link to your favorite GIF (think `git add`)
* Save your changes (think `git commit`)
* Upload it on GitHub (think `git push`)


## Discuss usage in our lab

The way our lab works with GitHub should not be set in stone. Here are a couple of suggestions:  

* Maintain one private repository with all example notebooks relevant to the lab (e.g. ark, scyan, misty). People looking for a starting point to analyse their images should find everything in this folder. 
* For each project, store your analyses in a dedicated repository. This should document how you went from the images to the results and plots in the final publication. 

Note 1: The repo for your analyses will need to be public once you submit your manuscript but can be kept private before that. Usually there's no much risk in having it public unless there's a clear and novel scientific finding that may be scooped, or if you include the raw data in the repository by mistake.
Note 2: Keeping track of what you did so you can come back to it after a while is essential, explaining and documenting your workflow to others is great, and making your whole analysis reproducible is ideal.

* Common approaches to make your analyses reproducible include using [conda](https://docs.conda.io/en/latest/), [nextflow](https://www.nextflow.io/), [snakemake](https://snakemake.readthedocs.io/en/stable/) or [docker](https://www.docker.com/). 
* How to structure your project (i.e. where to put data, notebooks, scripts, plots and so on) depends on your goal and your preferences but [cookiecutter](https://github.com/cookiecutter/cookiecutter) is a good starting point. Be carefule that GitHub does not like large files and your data should typically not be included in your repository but distributed separately, for instance with [figshare](https://figshare.com/) or [dryad](https://datadryad.org/stash).

Here are a few open questions:
* Do we want to use GitHub as a knowledge base (e.g. list of tools for spatial analyses) instead of spreadsheets?
* Do we want to make use of Kanban boards on GitHub, for instance for [project ideas](https://github.com/orgs/HartmannLab/projects/1) or to distribute tasks?
* Do we want a logo or something?


## Learn about other cool things you can do on GitHub

### Online editor, codespaces and GitHub Copilot
You can edit files directly online with Visual Studio, which offers many convenient features to work on code. For that, simply change `github.com` to `github.dev` in your address bar.  For instance you could [edit this repository directly](https://github.dev/HartmannLab/GitWorkshop).  
GitHub also offers *Codespaces*, which is a virtual machine in which you can run your code directly from your browser and interact using Visual Studio. It also supports things like Jupyter Notebooks, and can be used for collaborating on the same code in real time.  
GitHub offers a smart code completion tool integrated within its editor and codespaces (something like chatGPT for code). These options come at a cost but can be free [for students and researchers](https://education.github.com/).


### GitHub actions and continuous development
GitHub can automate a lot of tasks using so-called *GitHub actions*. For instance, a script can be triggered each time something is commited to the main branch. This can be used to test your code and make sure it works in different environments. This allows *Continuous development*, a software engineering principle that ensures that you're code is functional and can be run by users of different machines and operating systems. Simpler uses are also common, such as automatic updates or code linting (making sure your code is formatted according to the guidelines).

### Make your code citable
You can specify exactly which version of the code was used in your paper by associating a given release of your repository to a unique DOI [using Zenodo](https://zenodo.org/)

### Other tricks

#### Set up a README:

The file named `README.md` is always the one displayed first when you visit a repo on GitHub. This is why it's used as a starting point to explain what your repository is for, and how to run its code.

#### Commit often:
Ideally each time you're done adding a new feature, function or plot, and each time you correct a bug.

#### Commit working code:
If someone clones the repository, they should be able to compile/run the code without debugging. If you need to commit a buggy version, do it an other branch and keep the latest compiling version of your code in the main branch.
 
#### Tag your code:
You can tag the latest commit in your active branch to give it a name and find it easily later on (for instance when reaching a stable release or before publishing).
	
	git tag -a versionName -m "Description of the version"

#### Remember what's staged and what's not:
If you create a new file and want it in your repository, `git add`. If you remove a file in your git folder with `rm`, it will still be part of your repository unless you use `git rm`.

#### Git push regularly:
If it's on GitHub, it's really safe and people (including Future-you) can have a look at your code if they need it.

