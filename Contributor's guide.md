# Contributor's Guide

Thank you for investing your time in contributing to our project!

Wikisyllabus is collaborative project to build an evolving website/wiki to host, enhance, link, extend & update the university syllabus to help students find a way to connect their education to what’s new in the industry.
  
#### If you don't have Git Bash on your machine, [install it](https://git-scm.com/downloads).
If you are new to Git and Github, you need to [create a github account](https://github.com). It is advisable that you go through [Git Handbook](https://guides.github.com/introduction/git-handbook/) before moving to next step.  


## Fork the repository  
<img align="right" width="300" src="https://github.com/Angelrose19/WikiSyllabus/blob/main/Git%20%26%20GitHub%20Basics.md/assets/fork.jpg" />
Fork this repository by clicking on the fork button on the top of this page.
This will create a copy of this repository in your account.  

## Clone the repository  
Now clone the forked repository to your machine. Go to your GitHub account, open the forked repository, click on the code button and then click the copy to clipboard icon.

Open Git Bash and run the following git command:

```
git clone url 
```

where url  is the url you just copied! (your fork of this project).
<img align="right" width="300" src="https://github.com/Angelrose19/WikiSyllabus/blob/main/Git%20%26%20GitHub%20Basics.md/assets/code.png" />  
For example:

```
git clone https://github.com/username/Wikisyllabus.git
```

where `username` is your GitHub username. Here you're copying the contents of the Wikisyllabus repository on GitHub to your computer.  
  
## Make necessary changes

Open up the project in your favourite text editor, select the file you want to contribute to, and make your changes.Make sure to save the edits.

All the files in this project are ```.md``` files. You would need to have Markdown knowledge to contribute to this project.  
Markdown is a fast and easy way to take notes, create content for a website, and produce print-ready documents. It doesn't take long to learn the Markdown syntax, and once you know how to use it, you can write using Markdown just about everywhere. Visit [here to master Markdown](https://guides.github.com/features/mastering-markdown/) .

## Add and Commit your changes
Open Git Bash, navigate to the project directory and execute the command ```git status```, you'll see there are changes.
 Add those changes to the branch you just created using the `git add` command:

```
git add filename.md
```
You can also add all the unstaged files using : ```git add .```  

Now commit those changes using the `git commit` command:

```
git commit -m "commit message"
```
       
## Push changes to GitHub

Push your changes using the command `git push`:

```
git push origin main
```

## Create a pull request
  
Open the main page of your repository on your GitHub account in your browser and click on the Pull requests tab. Now, click on the ```New pull request``` button.  
Click Create Pull Request option. Enter a suitable title and description for the pull request. Now submit the pull request.  
  
Congrats! You just completed the standard fork -> clone -> edit -> pull request workflow that you'll encounter often as a contributor!


   

 

