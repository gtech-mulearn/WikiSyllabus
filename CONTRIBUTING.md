# Contributing to Wikisyllabus
Thank you for investing your time in contributing to our project✨
  
#### If you don't have Git Bash on your machine, [install it](https://git-scm.com/downloads).
If you are new to Git and Github, you need to [create a Github Account](https://github.com). It is advisable that you go through [Git Handbook](https://docs.github.com/en/github) before moving to next step.  


## Fork the repository  
<img align="right" width="300" src="https://github.com/gtechatfg/WikiSyllabus/blob/main/docs/assets/fork.jpg" />
Fork this repository by clicking on the fork button on the top of this page.
This will create a copy of this repository in your account.  

## Clone the repository  
Now clone the forked repository to your machine. Go to your GitHub account, open the forked repository, click on the code button and then click the copy to clipboard icon.

Open Git Bash and run the following git command:

```
git clone url 
```

where url  is the url you just copied! (your fork of this project).
<img align="right" width="300" src="https://github.com/gtechatfg/WikiSyllabus/blob/main/docs/assets/code.png" />  
For example:

```
git clone https://github.com/username/Wikisyllabus.git
```

where `username` is your GitHub username. Here you're copying the contents of the Wikisyllabus repository on GitHub to your computer.  

## Create an issue

What's an [issue?](https://docs.github.com/en/issues/tracking-your-work-with-issues/quickstart)  
  
To create an issue, On the main page of your repository, click  Issues. Click New issue.  
Click Get started next to the type of issue you'd like to open. Or, click Open a blank issue if the type of issue you'd like to open isn't included in the available options.  
Type a title and description for your issue. Then click Submit new issue.

  
## Make necessary changes

Open up the project in your favourite text editor, select the file you want to contribute to, and make your changes.Make sure to save the edits.
...
# Adding Files to Wikisyllabus

If you fork and clone the WikiSyllabus Repository, follow these steps:

## Go to the `src` Folder

1. Navigate to the `Wikisyllabus` folder.
2. If you are contributing materials for other universities, create a new folder with the university's name (e.g., `foldername: MG`). Inside this folder, add a `SUMMARY.md` file and type the university's name (e.g., `MG`).

For contributions to KTU (Kerala Technological University):

3. There are two folders: `2019_scheme` and `2015_scheme`.
4. Inside each of these folders, there are seven folders, `S1&S2` to `S8`.
5. Go to the folder corresponding to the semester you want to contribute.
6. Create a new folder with the course code as its name.
7. Add a `SUMMARY.md` file inside this folder and type the current folder's name, and the subject name. Add its index that your going to contribute md files 
    Example :-(If your Subject is C-programming)
    ```
    # EST 102 - C PROGRAMMING
    #### INDEX

    - [Introduction to C Programming](./1intro.md)
    - [Variables and Keywords](./2variables_keywords.md)
    - [Datatypes](./3datatypes.md)
    ```
   
9. You can create one or more `.md` files in this folder. The names of these files should be specific to their content.

## Adding Content to the `.md` File

1. If you have a PDF file, you can copy the text from the PDF and paste it into the `.md` file.
2. If there are any pictures in the PDF, take a screenshot and upload it at the appropriate position in the `.md` file.
   - If you are using GitHub for editing, you can easily drag and drop the image at the desired position.
3. If the study material you want to contribute is already present, do not add it again. However, if there are any changes or additions to the existing content, you can edit the corresponding `.md` file and add your content below the current one.

## Adding Your Name to the Contributors List

1. Open the `README.md` file in the repository.
2. Add a new `<td>` inside the table like this: `<table><tr><td></td></tr></table>`.
3. Inside the `<td>` tag, add your details in the following format:

```html
<td align="center">
  <a href="https://github.com/your_github">
    <img src="link_of_your_image_from_github" width="100px;" alt="" />
    <br />
    <sub><b>Your_Name</b></sub>
  </a>
  <br />
  <a href="your_commit_link" title="File_type">Give a symbol</a>
</td>
```

4. Commit your changes and create a pull request.

All the files in this project are ```.md``` files. You would need to have Markdown knowledge to contribute to this project.    
   
Markdown is a fast and easy way to take notes, create content for a website, and produce print-ready documents. It doesn't take long to learn the Markdown syntax, and once you know how to use it, you can write using Markdown just about everywhere. Visit [here](https://guides.github.com/features/mastering-markdown/) to master Markdown.  
  
You could add Notes, Useful Website links, Youtube lecture links or anything you find useful in learning the specific topic.

## Earning Karma Points

An individual can earn 200 karma points for each contribution. You can contribute twice in a month to earn more karma points.

...


## Add and Commit your changes
Open Git Bash, navigate to the project directory and execute the command ```git status```, you'll see there are changes.
 Add those changes to the branch you just created using the `git add` command:

```
git add filename.md
```
You can also add all the unstaged files using : ```git add .```  

Now commit those changes using the `git commit` command:
<img align="right" width="300" src="https://github.com/gtechatfg/WikiSyllabus/blob/main/docs/assets/commit.png" /> 

```
git commit -m "commit message"
```
       
## Push changes to GitHub

Push your changes using the command `git push`:

```
git push origin main
```

## Create a pull request
  
<img align="right" width="300" src="https://github.com/gtechatfg/WikiSyllabus/blob/main/docs/assets/pr.PNG" /> 
Open the main page of your repository on your GitHub account in your browser and click on the Pull requests tab.  
Now, click on the New Pull Request button.  
Click Create Pull Request option. Enter a suitable title and description for the pull request. Now submit the pull request.    

  
What is a [pull request?](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests)    
  
You can find more GitHub Commands [here](https://www.geeksforgeeks.org/list-useful-github-commands/)
  
__Congrats! You just completed the standard fork -> clone -> edit -> pull request workflow that you'll encounter often as a contributor!🎉__
  
## To Add your details in contributors 

Comment on Issue or Pull Request, asking @all-contributors to add your details.

`@all-contributors please add @<username> for <contributions>`

eg: 

`@all-contributors please add @userid for coding`

Make sure to add this comment after merging one of your PR to `main`



## Setting Up mdBook (Optional)
mdBook is a command line tool and Rust crate to create books with Markdown. You can edit the markdown files (.md) in a text editor of your choice, but you wouldn’t be able to view the rendered output in the book form with formatting. To view the book as intended, you will need to set up the mdBook CLI on your system. 
  
mdBook can be installed with cargo, the package manager for Rust extensions. Cargo installation procedure is different depending on the OS you’re running.
  
### Linux/MacOS
* Install rustup and cargo by running this command in the terminal. (Note : You may need to reopen the terminal after this command executes.)  
```curl https://sh.rustup.rs -sSf | sh```  
  
* Install the mdBook CLI from cargo  
```cargo install mdbook``` 
  
* Check version of mdBook installed to verify the installation was successful
```cargo -V```  
  
### Windows
* Install [rustup and cargo](https://www.rust-lang.org/tools/install)  
  
* To use cargo, you may need to have C/C++ Build tools. If you don’t have it installed, there are two options, choose either one.  
  * GNU C Compiler : Install it using the following commands  ```rustup toolchain install stable-x86_64-pc-windows-gnu``` ```rustup default stable-x86_64-pc-windows-gnu```  
  * Visual Studio C++ Build Tools : Install C++ build tools from this [link](https://visualstudio.microsoft.com/visual-cpp-build-tools)
  
* Install the mdBook CLI from cargo  : ```cargo install mdbook```    

* Check version of mdBook installed to verify the installation was successful	: ```cargo -V```

You could go through [mdBook Handbook](https://phaiax.github.io/mdBook/README.html) to get more familiar with mdBook.




 

