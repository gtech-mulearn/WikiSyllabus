# Contributing to Wikisyllabus
Thank you for investing your time in contributing to our project!
  
#### If you don't have Git Bash on your machine, [install it](https://git-scm.com/downloads).
If you are new to Git and Github, you need to [create a github account](https://github.com). It is advisable that you go through [Git Handbook](https://guides.github.com/introduction/git-handbook/) before moving to next step.  


## Fork the repository  
<img align="right" width="300" src="https://github.com/Angelrose19/WikiSyllabus/blob/main/docs/assets/fork.jpg" />
Fork this repository by clicking on the fork button on the top of this page.
This will create a copy of this repository in your account.  

## Clone the repository  
Now clone the forked repository to your machine. Go to your GitHub account, open the forked repository, click on the code button and then click the copy to clipboard icon.

Open Git Bash and run the following git command:

```
git clone url 
```

where url  is the url you just copied! (your fork of this project).
<img align="right" width="300" src="https://github.com/Angelrose19/WikiSyllabus/blob/main/docs/assets/code.png" />  
For example:

```
git clone https://github.com/username/Wikisyllabus.git
```

where `username` is your GitHub username. Here you're copying the contents of the Wikisyllabus repository on GitHub to your computer.  
  
## Make necessary changes

Open up the project in your favourite text editor, select the file you want to contribute to, and make your changes.Make sure to save the edits.

All the files in this project are ```.md``` files. You would need to have Markdown knowledge to contribute to this project.  
Markdown is a fast and easy way to take notes, create content for a website, and produce print-ready documents. It doesn't take long to learn the Markdown syntax, and once you know how to use it, you can write using Markdown just about everywhere. Visit [here](https://guides.github.com/features/mastering-markdown/) to master Markdown.

## Add and Commit your changes
Open Git Bash, navigate to the project directory and execute the command ```git status```, you'll see there are changes.
 Add those changes to the branch you just created using the `git add` command:

```
git add filename.md
```
You can also add all the unstaged files using : ```git add .```  

Now commit those changes using the `git commit` command:
<img align="right" width="300" src="https://github.com/Angelrose19/WikiSyllabus/blob/main/docs/assets/commit.png" /> 

```
git commit -m "commit message"
```
       
## Push changes to GitHub

Push your changes using the command `git push`:

```
git push origin main
```

## Create a pull request
  
<img align="right" width="300" src="https://github.com/Angelrose19/WikiSyllabus/blob/main/docs/assets/pr.png" /> 
Open the main page of your repository on your GitHub account in your browser and click on the Pull requests tab. Now, click on the ```New pull request``` button.  
Click Create Pull Request option. Enter a suitable title and description for the pull request. Now submit the pull request.  
  
  
### Congrats! You just completed the standard fork -> clone -> edit -> pull request workflow that you'll encounter often as a contributor!

## Setting Up mdBook (Optional)
mdBook is a command line tool and Rust crate to create books with Markdown. You can edit the markdown files (.md) in a text editor of your choice, but you wouldn’t be able to view the rendered output in the book form with formatting. To view the book as intended, you will need to set up the mdBook CLI on your system. 
  
mdBook can be installed with cargo, the package manager for Rust extensions. Cargo installation procedure is different depending on the OS you’re running.
  
### Linux/MacOS
Install rustup and cargo by running this command in the terminal. (Note : You may need to reopen the terminal after this command executes.)  
```curl https://sh.rustup.rs -sSf | sh```  
  
Install the mdBook CLI from cargo  
```cargo install mdbook``` 
  
Check version of mdBook installed to verify the installation was successful
```cargo -V```  
  
### Windows
Install [rustup and cargo](https://www.rust-lang.org/tools/install)  
  
To use cargo, you may need to have C/C++ Build tools. If you don’t have it installed, there are two options, choose either one.  
* GNU C Compiler : Install it using the following commands
```rustup toolchain install stable-x86_64-pc-windows-gnu```
```rustup default stable-x86_64-pc-windows-gnu```
* Visual Studio C++ Build Tools : Install C++ build tools from this [link](https://visualstudio.microsoft.com/visual-cpp-build-tools)
  
Install the mdBook CLI from cargo  
```cargo install mdbook```
  
Check version of mdBook installed to verify the installation was successful	
```cargo -V```








   

 

