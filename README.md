<h1 align=center><b><i>Full Stack WD</i></b></h1>

## Basic Git Commands
- At a convenient location on your computer, create a folder named git-test.
- Open this git-test folder in your favorite editor.
- Add a file named index.html to this folder, and add the following HTML code to this file:

```
<!DOCTYPE html>
<html>
    <head></head>

    <body>
        <h1>This is a Header</h1>
    </body>
</html>
```
Initializing the folder as a Git repository

- Go to the git-test folder in your cmd window/terminal and type the following at the prompt to initialize the folder as a Git repository:

```
git init
```

Checking your Git repository status
- Type the following at the prompt to check your Git repository's status:

```
git status
```

Adding files to the staging area

- To add files to the staging area of your Git repository, type:

```
git add .
```

Commiting to the Git repository

- To commit the current staging area to your Git repository, type:

```
git commit -m "My first commit"
```

Checking the log of Git commits

- To check the log of the commits to your Git repository, type

```
git log --oneline
```

- Now, modify the index.html file as follows:

```
<!DOCTYPE html>
<html>
    <head></head>

    <body>
        <h1>This is a Header</h1>
        <p>This is a paragraph</p>
    </body>
</html>
```

- Add a sub-folder named templates to your git-test folder, and then add a file named test.html to the templates folder. Then set the contents of this file to be the same as the index.html file above.
- Then check the status and add all the files to the staging area.
- Then do the second commit to your repository
- Now, modify the index.html file as follows:

```
<!DOCTYPE html>
<html>
    <head></head>

    <body>
        <h1>This is a Header</h1>
        <p>This is a paragraph</p>
        <p>This is a second paragraph</p>
    </body>
</html>
```
- Now add the modified index.html file to the staging area and then do a third commit.

Checking out a file from an earlier commit
- To check out the index.html from the second commit, find the number of the second commit using the git log, and then type the following at the prompt:

```
git checkout <second commit's number> index.html
```

Resetting the Git repository
- To discard the effect of the previous operation and restore index.html to its state at the end of the third commit, type:

```
git reset HEAD index.html
```
- Then type the following at the prompt:

```
git checkout -- index.html
```

- You can also use git reset to reset the staging area to the last commit without disturbing the working directory.

## Setting up an Online Git repository
- Sign up for an account either at Bitbucket (https://bitbucket.org) or GitHub (https://github.com).

- Then set up an online Git repository named **git-test.** Note the URL of your online Git repository. Note that private repositories on GitHub requires a paid account, and is not available for free accounts.

Set the local Git repository to set its remote origin

- At the prompt, type the following to set up your local repository to link to your online Git repository:

```
git remote add origin <repository URL>
```

Pushing your commits to the online repository

- At the prompt, type the following to push the commits to the online repository:
```
git push -u origin master
git push -f origin master  //if above not work used forced method
```
Cloning an online repository

- To clone an online repository to your computer, type the following at the prompt:

```
git clone <repository URL>
```

<h2 align=center><b><i>Node Js</i></b></h2>

### Download Nodejs [here](https://nodejs.org/en/download/) 

Initializing package.json
- At the command prompt in your **git-test** folder, type
```
npm init
```
- Follow along the prompts and answer the questions as follows: accept the default values for most of the entries, except set the entry point to index.html
  This should create a package.json file in your **git-test** folder.
  
- Installing an NPM Module

- Install an NPM module, lite-server, that allows you to run a Node.js based development web server and serve up your project files. To do this, type the following at the prompt:

```
npm install lite-server --save-dev
```
- You can check out more documentation on lite-server [here](https://github.com/johnpapa/lite-server).
- Next, open package.json in your editor and modify it as shown below. Note the addition of two lines, line 7 and line 9.

![](https://github.com/Psingh12354/Full-Stack-WD/blob/main/Weak%201/Node%20init.PNG)

```
{
  "name": "git-test",
  "version": "1.0.0",
  "description": "This is the Git and Node basic learning project",
  "main": "index.html",
  "scripts": {
    "start": "npm run lite",
    "test": "echo \"Error: no test specified\" && exit 1",
    "lite": "lite-server"
  },
  "repository": {
    "type": "git",
    "url": "git+https://jogesh_k_muppala@bitbucket.org/jogesh_k_muppala/git-test.git"
  },
  "author": "",
  "license": "ISC",
  "homepage": "https://bitbucket.org/jogesh_k_muppala/git-test#readme",
  "devDependencies": {
    "lite-server": "^2.2.2"
  }
}
```

- Next, start the development server by typing the following at the prompt:
```
npm start
```

- This should open your index.html page in your default browser.

- If you now open the index.html page in an editor and make changes and save, the browser should immediately refresh to reflect the changes.

Setting up .gitignore

- Next, create a file in your project directory named **.gitignore** (Note: the name starts with a period)Then, add the following to the .gitignore file

```
node_modules
```

- Then do a git commit and push the changes to the online repository. You will note that the node_modules folder will not be added to the commit, and will not be uploaded to the repository.

Setting up the Project Folder

- Go to a convenient folder location on your computer and download the Bootstrap4-starter.zip file using the link provided at the top of this page.
- Unzip the file to see a folder named Bootstrap4 and a sub-folder under it named conFusion created. Move to the conFusion folder.
- Open a cmd window/terminal and move to the conFusion folder.
- At the prompt type

```
npm install
```

- This will install the lite-server node module to your project.
- Next, initialize a Git repository in the project folder, and then set up a .gitignore file with the contents as shown below:

```
node_modules
```

- Now do a commit of your project folder to the Git repository with the message "Initial Setup". You will be doing a commit of your project at the end of each exercise so that you retain the completed files of each exercise.
- Set up an online Git repository and synchronize your project folder with the online repository.

### Downloading Bootstrap

- You will use npm to fetch the Bootstrap files for use within your project. Thereafter you need to install JQuery and Popper.js as shown below since Bootstrap 4 depends on these two. At the prompt, type the following to fetch Bootstrap files to your project folder:

```
npm install bootstrap@4.0.0 --save
npm install jquery@3.3.1 popper.js@1.12.9 --save
```

- This will fetch the Bootstrap files and store is in your node_modules folder in a bootstrap folder. The bootstrap->dist folder contains the precompiled Bootstrap CSS and JS files for use within your project.
- Open your project folder in your editor, and then open the index.html file in the conFusion folder. This is your starting web page for the project. We have already created the web page with some content to get you started. We will use Bootstrap to style this web page, and learn Bootstrap features, classes and components along the way.
- Start your lite-server by typing **npm start** at the prompt. The index.html file should now be loaded into your default browser.

### Getting your Web page Bootstrap ready

- Open the index.html file in your favourite text editor. If you are using Visual Studio Code, Brackets, Sublime Text or similar editors, you can open the project folder in the editor and then view index.html.
- Insert the following code in the <head> of index.html file before the title.

```
    <!-- Required meta tags always come first -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    <meta http-equiv="x-ua-compatible" content="ie=edge">

    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.min.css">
 ```
    
- This will include Bootstrap CSS into your web page. Note the subtle change in the fonts of the content of the web page. This is the Bootstrap typography effect coming into play. The default Bootstrap typography sets the font to Helvetica Neue and selects the appropriate font size based on the choice of the heading style and paragraph style for the content.
- At the bottom of the page, just before the end of the body tag, add the following code to include the JQuery library, popper.js library and Bootstrap's Javascript plugins. Bootstrap by default uses the JQuery Javascript library for its Javascript plugins. Hence the need to include JQuery library in the web page.

```
    <!-- jQuery first, then Popper.js, then Bootstrap JS. -->
    <script src="node_modules/jquery/dist/jquery.slim.min.js"></script>
    <script src="node_modules/popper.js/dist/umd/popper.min.js"></script>
    <script src="node_modules/bootstrap/dist/js/bootstrap.min.js"></script>
 ```
 
- Now, do a Git commit with the message "Intro. to Bootstrap". You may push the commit to your online repository.
